# NotPetya (2017): The Most Destructive Attack in History

[![Type](https://img.shields.io/badge/Type-Technical_Essay_(Unpublished)-lightgrey)](#overview)
[![Year](https://img.shields.io/badge/Year-2026-blue)](#overview)
[![Domain](https://img.shields.io/badge/Domain-Cybersecurity_%26_Systems_Architecture-darkred)](#key-topics-analyzed)

**Author:** Davide Donati[cite: 1]  
**Affiliation:** Department of Information Engineering (DEI), University of Padua, Italy  
**Type:** Technical Security Analysis / University Coursework Essay (2026)[cite: 1]

---

## Folder Contents

* [`NotPetya_Technical_Analysis.pdf`](./NotPetya_Analysis.pdf) — Full technical essay (PDF).

---

## Overview

An architectural and forensic deep dive into the **June 27, 2017 NotPetya cyberattack**, which paralyzed critical infrastructure across Ukraine before propagating autonomously worldwide and causing over **$10 billion** in global damages[cite: 1]. Rather than functioning as financially motivated ransomware, reverse engineering of the binary (`perfc.dat`) revealed an irreversible wiper engineered to permanently destroy endpoints and maximize operational disruption[cite: 1].

---

## Key Topics Analyzed

1. **Supply-Chain Subversion (`M.E.Doc` / `EzData.dll`):**[cite: 1]
   * Infiltration via compromised updates of the Ukrainian accounting platform M.E.Doc (`Medoc.Zvit.exe` / `MeDocHelper`), leveraging XML-RPC telemetry, EDRPOU tax ID filtering, and staged in-memory CIL/C# payload execution[cite: 1].
2. **Memory-Resident Execution & Privilege Escalation:**[cite: 1]
   * Export `#1` execution via `rundll32.exe`, `SeDebugPrivilege` and `SeShutdownPrivilege` token adjustments, process-tree privilege inheritance without triggering UAC, and local kill-switch/vaccination file checks[cite: 1].
3. **Credential Harvesting & Dual-Vector Lateral Movement:**[cite: 1]
   * In-memory LSASS scraping using a custom 32/64-bit Mimikatz implementation (`msv1_0`, `wdigest`, `kerberos`) combined with WMI (`Win32_Process`), embedded PsExec (`psexesvc.exe`), and SMBv1 exploits—specifically **EternalBlue (`CVE-2017-0144`)** and **EternalRomance (`CVE-2017-0145`)**[cite: 1].
4. **Low-Level Filesystem Destruction:**[cite: 1]
   * Direct physical disk handle manipulation (`\\.\PhysicalDrive0`), Master Boot Record (MBR) overwriting with custom 16-bit bootloader code, Master File Table (MFT) encryption using a modified Salsa20 cipher where the generated keystream is discarded (rendering recovery impossible), and forced BSoD reboots via `NtRaiseHardError`[cite: 1].
5. **Enterprise Impact & Post-NotPetya Resilience:**[cite: 1]
   * Real-world infrastructure casualty breakdowns (**A.P. Moller–Maersk**, **Merck**, **FedEx/TNT**) and the architectural shift from flat perimeter networks to **Zero-Trust Microsegmentation (ZTA)**, **Credential Guard**, **Just-in-Time (JIT)** privileged access, SMBv1 deprecation, and immutable air-gapped backups[cite: 1].
