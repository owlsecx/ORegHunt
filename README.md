# 🦉 ORegHunt

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
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

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
