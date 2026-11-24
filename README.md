# 🦉 OEcho

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OReconnaissance-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
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

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OEcho --help   # watch every network call
firejail --net=none ./OEcho --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
