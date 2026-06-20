<p align="center">
  <svg viewBox="0 0 150 150" width="120" height="120" xmlns="http://www.w3.org/2000/svg">
    <path d="M 75,10 A 65,65 0 0,0 75,140" fill="none" stroke="#A000FF" stroke-width="5" stroke-linecap="round" />
    <path d="M 75,140 A 65,65 0 0,0 75,10" fill="none" stroke="#00F0FF" stroke-width="5" stroke-linecap="round" />
    <circle cx="75" cy="75" r="40" fill="none" stroke="#00F0FF" stroke-width="1.5" stroke-dasharray="6 6" />
    <circle cx="75" cy="75" r="10" fill="#A000FF" />
    <line x1="75" y1="0" x2="75" y2="20" stroke="#00F0FF" stroke-width="3" stroke-linecap="round" />
    <line x1="75" y1="130" x2="75" y2="150" stroke="#00F0FF" stroke-width="3" stroke-linecap="round" />
    <line x1="0" y1="75" x2="20" y2="75" stroke="#00F0FF" stroke-width="3" stroke-linecap="round" />
    <line x1="130" y1="75" x2="150" y2="75" stroke="#00F0FF" stroke-width="3" stroke-linecap="round" />
  </svg>
</p>

<h1 align="center">TARG3T</h1>

<p align="center">
  <strong>Next-Gen Security Automation Engine for Penetration Testing</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/release-stable%201.0.0-00F0FF.svg?style=flat-square" alt="Release">
  <img src="https://img.shields.io/badge/made%20with-bash-A000FF.svg?style=flat-square" alt="Language">
  <img src="https://img.shields.io/badge/license-GPLv3-blue.svg?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/tested%20on-Kali%20Linux-red.svg?style=flat-square" alt="TestedOn">
</p>

---

## 🌌 About
**Targ3t** is an offensive security automation engine engineered to seamlessly orchestrate the initial stages of a penetration test. It focuses on high-speed **Information Gathering** (reconnaissance) and precise **Vulnerability Assessment**.

All intelligence gathered during execution is dynamically structured into a clean, intuitive directory tree, ensuring effortless navigation even when analyzing complex multi-target environments.

---

## 🛠️ Technical Architecture

Targ3t integrates and automates industry-standard security binaries across two core operational phases:

### 1. Information Gathering & Reconnaissance
* **Network Mapping:** Comprehensive port scanning and passive/active service fingerprinting via **Nmap**.
* **Web Enumeration:** High-speed discovery of hidden directories, endpoints, and web assets via **Dirb**.

### 2. Vulnerability Assessment & Intelligence
* **Web Auditing:** Automated web application vulnerability mapping pairing **Nikto** and **Dirb**.
* **Exploit Vector Analysis:** Cross-referencing active services with **Metasploit** templates.
* **Exploit Intelligence:** Instant queries against localized exploit databases using **Searchsploit**.
* **Dictionary Auditing:** Automated credential stress-testing via **Hydra** for critical protocols:
  * `SSH` | `POP3` | `IMAP` | `RDP` | `SMB`

---

## 🚀 Usage & Execution Modes

Targ3t supports flexible deployment configurations to match your operational pipeline:

### 🕹️ Interactive Mode
Launch the wizard directly in your terminal and let the environment guide you through target setup:
```bash
targ3t
🤖 Non-Interactive Mode (Headless / CI-CD)
For automated pipelines or headless console operations, pass explicit operational arguments:

Bash
targ3t -t <target_ip> -f <report_path> [-p one_or_more_phases]
📖 System Help Manual
To print the full parameters, arguments help, and environment flags:

Bash
targ3t -h
🎛️ Engine Customization
You can fine-tune the dictionary paths, wordlists, and file structures by modifying the global variables declared inside the main script file:

Bash
# TARG3T_PATH='' # CORE PATH ENVIRONMENT (LEAVE EMPTY TO USE CURRENT DIR)

if [[ "$TARG3T_PATH" == '' ]]; then
	TARG3T_PATH='.'
fi

# TARGETED USER DICTIONARIES
USERLIST_HYDRA_SSH="$TARG3T_PATH/user_wordlist_short.txt"
USERLIST_HYDRA_POP3="$TARG3T_PATH/user_wordlist_short.txt"
USERLIST_HYDRA_IMAP="$TARG3T_PATH/user_wordlist_short.txt"
USERLIST_HYDRA_RDP="$TARG3T_PATH/user_wordlist_short.txt"
USERLIST_HYDRA_SMB="$TARG3T_PATH/user_wordlist_short.txt"

# TARGETED PASSWORD DICTIONARIES
PASSLIST_HYDRA="$TARG3T_PATH/fasttrack.txt"
PASSLIST_HYDRA_SSH="$PASSLIST_HYDRA"
PASSLIST_HYDRA_POP3="$PASSLIST_HYDRA"
PASSLIST_HYDRA_IMAP="$PASSLIST_HYDRA"
PASSLIST_HYDRA_RDP="$PASSLIST_HYDRA"
PASSLIST_HYDRA_SMB="$PASSLIST_HYDRA"

# WEB NAVIGATION DICTIONARIES
HTTP_WORDLIST="$TARG3T_PATH/custom_url_wordlist.txt"
HTTP_EXTENSIONS_FILE="$TARG3T_PATH/custom_extensions_common.txt"

# CORE EXPLOIT PLUGINS
METASPLOIT_SCAN_SCRIPT='./metasploit_scan_script'
⚡ Core Features
Subnet Scaling: Concurrent asset scanning optimized to support up to 254 live hosts simultaneously (Class-C segments).

CVE-to-Metasploit Mapping: Instantly correlates discovered CVE identifiers with working Metasploit execution modules.

Non-Canonical Port Tracking: Automatically flags standard services disguised on non-standard entry ports (e.g., HTTP on port 7000).

Exfiltration Vault: Securely logs, isolates, and formats all successfully cracked active credentials into independent reports.

Streamlined Directory Tree: Clear workspace structures that generate intuitive folder hierarchies for raw text and log assets.

🔮 Complementary Tooling
During the development of the primary automation suite, a companion layout named trigmap (Trigger Nmap) was built.

[!TIP]
While Targ3t leverages a wide array of separate ecosystem binaries (Nikto, Hydra, Dirb), trigmap focuses entirely on maximizing the raw scriptability of Nmap NSE modules. Running both utilities concurrently across a target provides a much deeper, cross-verified evidence dossier.

⚖️ Disclaimer
[!WARNING]
CRITICAL SECURITY NOTICE: The developer assumes absolutely no liability and is not responsible for any malicious misuse, unauthorized network disruption, or data loss caused by this script.

Targ3t is distributed strictly for authorized penetration testing environments and educational security research. It is provided "AS IS" without any explicit or implied warranty of merchantability or fitness for a particular purpose.

📄 License
This repository is open-source software distributed under the terms of the GPLv3 License. Review the main project LICENSE parameters for complete copyleft conditions.
