APLORE TERMUX TOOLKIT - Repository README.md
markdown
<p align="center">
  <img src="https://img.shields.io/badge/Platform-Termux-%2334A853?style=for-the-badge&logo=android" alt="Platform">
  <img src="https://img.shields.io/badge/License-MIT-%23e6005c?style=for-the-badge" alt="License">
  <img src="https://img.shields.io/badge/Status-ACTIVE-%23FF6B00?style=for-the-badge" alt="Status">
</p>

<h1 align="center">
  <br>
  <img src="https://raw.githubusercontent.com/aplore/termux-toolkit/main/.github/logo.png" alt="APLORE Termux Toolkit" width="200">
  <br>
  APLORE TERMUX TOOLKIT
  <br>
</h1>

<h4 align="center">The ultimate, all-in-one mobile penetration testing arsenal for the ethical hacker on the move.</h4>
<h4 align="center">Designed for <code>Aplore Cybersecurity</code> students to turn any Android device into a powerful security lab.</h4>

<p align="center">
  <a href="#-overview">Overview</a> •
  <a href="#-features">Features</a> •
  <a href="#-quick-deployment">Deployment</a> •
  <a href="#-tool-categories">Tools</a> •
  <a href="#-usage--ethics">Ethics</a> •
  <a href="#-support">Support</a>
</p>

![Demo Banner](https://raw.githubusercontent.com/aplore/termux-toolkit/main/.github/demo.gif)

## 🔥 OVERVIEW

Welcome to the **official mobile field kit** for Aplore Cyber Guardians. This toolkit condenses the power of a desktop security distro into your pocket, providing over 50 curated tools for reconnaissance, scanning, exploitation, and forensics—all operable from a mobile device.

> **⚠️ WARNING & LEGAL DISCLAIMER**
> This toolkit is developed **strictly for educational purposes, authorized penetration testing, and security research**. Unauthorized use against systems you do not own or have explicit permission to test is **ILLEGAL**. By using this software, you pledge to adhere to the <a href="https://github.com/aplore/cybersecurity-roadmap/blob/main/00-WELCOME/APLORE_CYBER_PLEDGE.md">Aplore Cyber Pledge</a>. You are solely responsible for your actions.

## ⚡ FEATURES

*   **One-Command Deployment**: Get your lab running in under 5 minutes with our automated `install.sh` script.
*   **Curated Tool Suite**: No bloat. Only the most effective and updated tools for real-world scenarios.
*   **Offline-First Design**: Core modules and scripts function without an internet connection, perfect for field work.
*   **Aplore Integration**: Includes custom scripts that align with our course modules and CTF challenges.
*   **Regular Updates**: Tools and dependencies are checked and updated monthly by our security team.

## 🚀 QUICK DEPLOYMENT

**Prerequisites**: A device running Android 7+ with [Termux](https://termux.com/) installed from F-Droid (recommended).

```bash
# 1. Update Termux and clone the toolkit
pkg update -y && pkg upgrade -y
pkg install git -y
git clone https://github.com/aplore/termux-toolkit
cd termux-toolkit

# 2. Run the installer (This will request storage permissions)
chmod +x install.sh
./install.sh

# 3. Launch the toolkit main menu
./aplore-menu
The installer handles dependencies, tool compilation, and configuration. Grab a coffee while it works.

🛠️ TOOL CATEGORIES
Category	Key Tools	Purpose
📡 Reconnaissance	Sublist3r, theHarvester, PhoneInfoga	Domain, email, and phone number intelligence gathering.
🔍 Scanning	Nmap, RustScan, dnsrecon	Network port discovery, service enumeration, and vulnerability mapping.
🗡️ Exploitation	Metasploit (msfvenom), SQLmap, Hydra	Proof-of-concept exploitation and credential testing.
📶 Wireless	Aircrack-ng, Wifite, Reaver	WiFi network assessment and security testing.
🔐 Cryptography	John the Ripper, Hashcat (basic), fcrackzip	Password cracking and hash analysis.
🛡️ Aplore Custom	aplore-recon, aplore-report, ctf-helper	Scripts specifically for Aplore labs and CTF challenges.
For the complete, detailed list, see the TOOLS.md file.

📖 USAGE & ETHICS
Core Philosophy
We believe in offensive security for defensive purposes. Every tool here is a double-edged sword; mastery requires understanding not just how to use it, but when and why it is ethical to do so.

Getting Started
After installation, run ./aplore-menu to access the interactive menu. Start with the "Aplore Lab Exercises" section, which contains guided scenarios that match your coursework.

Responsible Disclosure
Discovering a vulnerability? Fantastic! Follow these steps:

STOP immediately. Do not proceed beyond what is needed to confirm the issue.

DOCUMENT your steps, URLs, and inputs precisely.

REPORT responsibly to the asset owner via their security contact or to your Aplore mentor.

🆘 SUPPORT
You are not hacking alone. The Aplore community is here for you.

🔗 Official Channels:

Discord: Join #cybersecurity-general on our Aplore Server

Telegram: Aplore Cyber Group

Email: aploreofficial@yahoo.com

📚 Course Integration: This toolkit is a core component of the Aplore Cybersecurity & Ethical Hacking course. For module-specific help, tag your mentor on Discord.

🐛 Reporting Issues: Found a bug or have a tool request? Please open a detailed GitHub Issue.

⚖️ LICENSE
Distributed under the MIT License. See the LICENSE file for details.
By the Community, for the Community.

<p align="center"> <strong>MASTER THE TOOLS. HONOR THE PLEDGE. SECURE THE FUTURE.</strong> <br> <sub>© 2024 APLORE | Building Africa's Next Generation of Ethical Hackers</sub> </p> ```
