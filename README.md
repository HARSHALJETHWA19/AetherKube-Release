# AetherKube Releases

> **Official public release artifacts and documentation for AetherKube — AI-native Kubernetes Operations Platform**

[![Release](https://img.shields.io/badge/release-v1.0.0%20Private%20Beta-cyan?style=flat-square)](https://github.com/HARSHALJETHWA19/aetherkube-releases/releases/latest)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Docker-blue?style=flat-square)](#downloads)
[![License](https://img.shields.io/badge/license-Commercial-orange?style=flat-square)](LICENSE)

---

## What is AetherKube?

AetherKube is an autonomous, AI-native Kubernetes operations and self-healing control plane designed for SRE, Platform Engineering, and DevOps teams.

Key capabilities:
- **Deterministic Diagnostics** — Automated detection and root-cause analysis for `CrashLoopBackOff`, `OOMKilled`, scheduling failures, and network partition issues with zero hallucination.
- **Universal Cluster Connection** — 9-stage connection diagnostics supporting kubeconfig, Bearer Token, EKS, AKS, GKE, K3s, Kind, Minikube, Docker Desktop, and bare-metal Kubernetes.
- **Human-in-the-Loop Remediation** — Dry-run preview → explicit approval gate → audited remediation execution with automated cooldowns.
- **AI Copilot (BYOK)** — Bring Your Own Key support for OpenAI, Anthropic, or local Ollama with deterministic offline fallback.
- **100% Operational Sovereignty** — Local-first execution with zero inbound ports and zero telemetry leakage.

> **Note:** The core product source code is maintained in a private repository. This repository is dedicated exclusively to public release distribution, checksum verification, and public documentation.

---

## Current Release: v1.0.0 (Private Beta)

| Version | Status | Release Date | Target Platforms |
| :--- | :--- | :--- | :--- |
| **v1.0.0** | Private Beta | October 2026 | Windows (x86_64), Docker |

---

## Downloads & Verification

All official release artifacts are signed and published on the [GitHub Releases](https://github.com/HARSHALJETHWA19/aetherkube-releases/releases/tag/v1.0.0) page.

| Artifact | Platform / Type | Size | SHA-256 Checksum |
| :--- | :--- | :--- | :--- |
| [`AetherKube-Windows-v1.0.0.exe`](https://github.com/HARSHALJETHWA19/aetherkube-releases/releases/download/v1.0.0/AetherKube-Windows-v1.0.0.exe) | Windows Setup Wizard | 33.6 MB | `5B2B02AA2B85AF01685ED510336B78E50DD8E4FC6189C6B2C1FCFDEB3D6ED273` |
| [`AetherKube-Windows-v1.0.0.zip`](https://github.com/HARSHALJETHWA19/aetherkube-releases/releases/download/v1.0.0/AetherKube-Windows-v1.0.0.zip) | Windows Portable Archive | 42.3 MB | `A1F56FAC514DAE871AC3AF76DAA0C7A74EEF23249EF581BC274A8FDC71C194AA` |
| [`AetherKube-Docker-v1.0.0.zip`](https://github.com/HARSHALJETHWA19/aetherkube-releases/releases/download/v1.0.0/AetherKube-Docker-v1.0.0.zip) | Docker Bundle Package | 19 KB | `3756EAF5A2743547310481EF72845F115EFBBB3DC5DBDAF4EA53FBE59EB98DB0` |
| [`docker-compose.commercial.yml`](https://github.com/HARSHALJETHWA19/aetherkube-releases/releases/download/v1.0.0/docker-compose.commercial.yml) | Compose Specification | 1.7 KB | `E70C2A74B4F02ED4383B959D358E0445760B4E83573DEE44F768E1532878E2F1` |
| [`SHA256SUMS.txt`](https://github.com/HARSHALJETHWA19/aetherkube-releases/releases/download/v1.0.0/SHA256SUMS.txt) | Checksum File | 344 B | Cryptographic checksum list |

Official Download Portal: **[https://aetherkube.pages.dev/download](https://aetherkube.pages.dev/download)**

---

## Quick Start Guides

### Option 1: Windows Setup Wizard (.exe)
1. Download [`AetherKube-Windows-v1.0.0.exe`](https://github.com/HARSHALJETHWA19/aetherkube-releases/releases/download/v1.0.0/AetherKube-Windows-v1.0.0.exe).
2. Verify integrity in PowerShell:
   ```powershell
   Get-FileHash .\AetherKube-Windows-v1.0.0.exe -Algorithm SHA256
   ```
3. Run the installer and complete the setup wizard.
4. Launch **AetherKube** from the Desktop shortcut or Start Menu.
5. Access the console at **[http://localhost:8080/login/](http://localhost:8080/login/)**.

### Option 2: Windows Portable (.zip)
1. Download [`AetherKube-Windows-v1.0.0.zip`](https://github.com/HARSHALJETHWA19/aetherkube-releases/releases/download/v1.0.0/AetherKube-Windows-v1.0.0.zip).
2. Extract the archive into any directory (no administrator rights needed).
3. Run `AetherKube.exe`.
4. Access the console at **[http://localhost:8080/login/](http://localhost:8080/login/)**.

### Option 3: Docker Compose
```bash
# 1. Download official commercial compose file
curl -fsSL https://github.com/HARSHALJETHWA19/aetherkube-releases/releases/download/v1.0.0/docker-compose.commercial.yml -o docker-compose.yml

# 2. Launch container stack
docker compose up -d

# 3. Access web console
# http://localhost:8080/login/
```

---

## Checksum Verification

Verify the SHA-256 hash before running:

**PowerShell (Windows):**
```powershell
Get-FileHash .\AetherKube-Windows-v1.0.0.exe -Algorithm SHA256
```

**Linux / macOS:**
```bash
sha256sum -c SHA256SUMS.txt
```

---

## Security & Responsible Disclosure

- Security reports should be filed confidentially — see [SECURITY.md](SECURITY.md).
- Email: **security@aetherkube.io**
- Private Security Advisory: [Create Private Advisory](https://github.com/HARSHALJETHWA19/aetherkube-releases/security/advisories/new)

---

## Feedback & Community

- **Issues & Bug Reports:** [Open an Issue](https://github.com/HARSHALJETHWA19/aetherkube-releases/issues)
- **Documentation:** [https://aetherkube.pages.dev/beta-guide](https://aetherkube.pages.dev/beta-guide)

---

## License

AetherKube is commercial software. See [LICENSE](LICENSE) for terms.

Copyright © 2026 AetherKube Systems Inc. All rights reserved.
