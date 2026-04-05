# 🏓 OEcho

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux%20%2F%20Windows-informational?style=flat-square&logo=linux&logoColor=white&color=0a0c10"/>
  <img src="https://img.shields.io/badge/Category-ORec%20%2F%20Host%20Discovery-cyan?style=flat-square"/>
  <img src="https://img.shields.io/badge/Dependencies-None%20(stdlib)-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-v1.0-cyan?style=flat-square"/>
</p>

> **OEcho** is a fast multi-threaded ICMP ping sweep tool for host discovery. It scans IP ranges or CIDR blocks, detects live hosts, measures latency, performs reverse DNS lookup, and generates clean reports.

**Note:** Requires root/sudo on Linux for raw ICMP. Some firewalls block ICMP — no response does not always mean the host is offline.

---

## 📌 Overview

OEcho performs efficient ICMP echo requests across large IP ranges or subnets. It supports three operation modes: full network sweep, single-host detailed ping, and continuous monitoring with state-change alerts.

Designed for quick network reconnaissance and live host mapping.

---

## 🖥️ Modules

| # | Module                    | Description |
|---|---------------------------|-------------|
| **[1]** | **Ping Sweep**            | Scan CIDR or IP range — discover live hosts |
| **[2]** | **Single Host Ping**      | Multi-packet ping with RTT statistics |
| **[3]** | **Continuous Monitor**    | Monitor a host and alert on UP/DOWN changes |

---

## 📊 Key Features

- **Multi-threaded Ping Sweep** — Up to 500 concurrent threads
- **CIDR & Range Support** — Full subnet scanning or custom start-end range
- **Latency Measurement** — Displays RTT for each live host
- **Reverse DNS Lookup** — Optional hostname resolution
- **Live Progress** — Real-time progress bar and statistics
- **Continuous Monitoring** — Alerts when hosts go up or down
- **Structured Reports** — Clean TXT export with summary
- **Pure stdlib** — No external dependencies required

---

## ⚙️ Requirements

- **No dependencies** — Uses only Python standard library
- **Linux** → Run with `sudo` for raw ICMP sockets
- **Windows** → Works without administrator privileges

**Standalone executable** — Runs as `./OEcho` when built with PyInstaller.

---

## 🚀 Usage

```bash
sudo ./OEcho

📁 Output

Live Terminal — Real-time colored results showing [UP], IP, RTT, and hostname
Summary — Hosts scanned, live hosts, dead hosts, scan rate, elapsed time
Report File (in oecho_reports/):
oecho_YYYYMMDD_HHMMSS.txt — Human-readable report with all live hosts, RTT, and hostnames



📦 Part of OwlSec Toolkit
This tool is part of the OwlSec suite — a collection of 300+ security and privacy tools.
🔗 owlsec.org

©️ License
Proprietary — © Khaled S. Haddad
Tools are distributed as pre-built executables. Source code is proprietary.
AUTHORISED USE ON NETWORKS YOU OWN OR ARE PERMITTED TO TEST
