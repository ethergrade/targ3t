<p align="center">
  <svg viewBox="0 0 150 150" width="120" height="120" xmlns="[http://www.w3.org/2000/svg](http://www.w3.org/2000/svg)">
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
  <img src="[https://img.shields.io/badge/release-stable%201.0.0-00F0FF.svg?style=flat-square](https://img.shields.io/badge/release-stable%201.0.0-00F0FF.svg?style=flat-square)" alt="Release">
  <img src="[https://img.shields.io/badge/made%20with-bash-A000FF.svg?style=flat-square](https://img.shields.io/badge/made%20with-bash-A000FF.svg?style=flat-square)" alt="Language">
  <img src="[https://img.shields.io/badge/license-GPLv3-blue.svg?style=flat-square](https://img.shields.io/badge/license-GPLv3-blue.svg?style=flat-square)" alt="License">
  <img src="[https://img.shields.io/badge/tested%20on-Kali%20Linux-red.svg?style=flat-square](https://img.shields.io/badge/tested%20on-Kali%20Linux-red.svg?style=flat-square)" alt="TestedOn">
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
