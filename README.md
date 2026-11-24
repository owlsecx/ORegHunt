# 🦉 ORegHunt

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **ORegHunt** — Offline Windows Registry Hive Hunter

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

ORegHunt is an offline forensic parser and auditor for Windows registry hives. Using a pure-standard-library regf parser, it walks the key tree, extracts forensic artifacts and runs MITRE-mapped audit rules over read-only hive files. It reports metadata only — it never extracts password hashes or decrypts LSA secrets.

---

## ✨ Features

- Pure-stdlib regf/hbin parser for raw hive files
- Key-tree printing, single-key dumps and value inspection
- Artifact extractors (autoruns, services, USB, UserAssist, ShimCache, ShellBags and more)
- MITRE-mapped forensic audit with FILETIME timeline and date filtering
- Deleted-cell scanning and hive header/cell information
- TXT/MD/JSON/CSV/SARIF export with severity filtering and a synthetic self-test

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./ORegHunt --hive SYSTEM --audit
./ORegHunt --hive NTUSER.DAT --tree --values
./ORegHunt --hive SOFTWARE --artifact autoruns -f json -o out.json
./ORegHunt --help
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
sudo strace -f -e trace=network ./ORegHunt --help   # watch every network call
firejail --net=none ./ORegHunt --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
