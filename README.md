🔐 Repository : Termux Toolkit
github.com/aplore/termux-toolkit
text
termux-toolkit/
├── README.md
├── INSTALL.sh
├── LICENSE
├── .github/
│   └── workflows/
│       └── security-scan.yml
├── scripts/
│   ├── setup.sh
│   ├── update-tools.sh
│   ├── backup-config.sh
│   └── cleanup.sh
├── tools/
│   ├── reconnaissance/
│   │   ├── subfinder/
│   │   ├── assetfinder/
│   │   ├── amass/
│   │   └── httprobe/
│   ├── vulnerability/
│   │   ├── nuclei/
│   │   ├── sqlmap/
│   │   ├── xsstrike/
│   │   └── wfuzz/
│   ├── web/
│   │   ├── dirsearch/
│   │   ├── gobuster/
│   │   ├── ffuf/
│   │   └── nikto/
│   ├── network/
│   │   ├── nmap/
│   │   ├── masscan/
│   │   ├── netcat/
│   │   └── tcpdump/
│   └── mobile/
│       ├── apktool/
│       ├── jadx/
│       ├── frida/
│       └── objection/
├── configs/
│   ├── termux.properties
│   ├── bashrc.aplore
│   ├── aliases.sh
│   └── colorscheme.conf
├── payloads/
│   ├── android/
│   ├── web/
│   ├── windows/
│   └── linux/
├── wordlists/
│   ├── aplore-common.txt
│   ├── aplore-api.txt
│   ├── aplore-dirs.txt
│   └── aplore-params.txt
├── labs/
│   ├── web-pentest/
│   ├── network-challenges/
│   ├── crypto-exercises/
│   └── stego-practice/
├── docs/
│   ├── GETTING_STARTED.md
│   ├── ETHICS_GUIDE.md
│   ├── TERMUX_TIPS.md
│   └── TROUBLESHOOTING.md
├── templates/
│   ├── report-template.md
│   ├── notes-template.md
│   └── cheatsheet-template.md
└── tests/
    └── test_installation.sh
INSTALL.sh:

bash
#!/bin/bash
# Aplore Termux Toolkit Installer
# Official: https://github.com/aplore/termux-toolkit

echo "🔧 Aplore Termux Toolkit Setup"
echo "=============================="

# Colors
RED='\033[0;31m'
GREEN='\033[0;32m'
YELLOW='\033[1;33m'
NC='\033[0m'

# Check if running in Termux
if [[ ! -d /data/data/com.termux ]]; then
    echo -e "${RED}[!] This script must run in Termux${NC}"
    exit 1
fi

# Update packages
echo -e "${YELLOW}[*] Updating packages...${NC}"
pkg update -y && pkg upgrade -y

# Install dependencies
echo -e "${YELLOW}[*] Installing dependencies...${NC}"
pkg install -y git python nodejs ruby golang \
    php perl nmap hydra sqlite curl wget \
    openssh proot-distro

# Clone repository
echo -e "${YELLOW}[*] Cloning Aplore toolkit...${NC}"
git clone https://github.com/aplore/termux-toolkit ~/aplore-toolkit
cd ~/aplore-toolkit

# Run setup
echo -e "${YELLOW}[*] Running setup script...${NC}"
chmod +x scripts/setup.sh
./scripts/setup.sh

# Configure environment
echo -e "${YELLOW}[*] Configuring environment...${NC}"
cat configs/bashrc.aplore >> ~/.bashrc
cp configs/aliases.sh ~/.aplore_aliases

echo -e "${GREEN}[✓] Installation complete!${NC}"
echo -e "${YELLOW}[!] Restart Termux or run: source ~/.bashrc${NC}"
echo -e "${YELLOW}[*] Join our community:"
echo -e "    Discord: https://discord.gg/tPe8fqXFN"
echo -e "    WhatsApp: https://whatsapp.com/channel/0029VbAyihY2UPBMDSJd3V0l${NC}"
