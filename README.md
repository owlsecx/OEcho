# 🦉 OEcho

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OReconnaissance-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-2.0-cyan?style=flat-square"/>
</p>

> **OEcho** — ICMP Host Discovery & Ping Sweep

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OEcho performs multi-threaded ICMP host discovery and ping sweeps across CIDRs, ranges, or host lists. It measures latency, optional reverse DNS, TTL heuristics, and TCP connect-ping fallback when ICMP is filtered. Monitor and traceroute modes support ongoing reachability checks on networks you are authorised to probe.

---

## ✨ Features

- CIDR, start–end range, and file-based sweep targets
- Single-host multi-packet ping and continuous monitor modes
- Traceroute helper alongside sweep discovery
- TCP connect-ping fallback when ICMP is blocked
- Reverse DNS, exclude lists, and latency-oriented timing controls
- TXT/JSON/CSV/JSONL export for inventory pipelines

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OEcho --sweep 10.0.0.0/24 --threads 100 --rdns
./OEcho --ping 10.0.0.1 --count 5 --json
./OEcho --monitor 10.0.0.1 --interval 2 --txt live.txt
./OEcho --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
