# 🛡️ Vault Guardian CI

[![DevSecOps Pipeline](https://github.com/pluss192/vault-guardian-ci/actions/workflows/security.yml/badge.svg)](https://github.com/pluss192/vault-guardian-ci/actions/workflows/security.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Security: Gitleaks](https://img.shields.io/badge/Security-Gitleaks%20Enabled-blue.svg)](https://github.com/gitleaks/gitleaks)
[![Scanner: Trivy](https://img.shields.io/badge/Vulnerability%20Scan-Trivy-orange.svg)](https://trivy.dev/)

An automated DevSecOps continuous integration pipeline providing shift-left security enforcement: scanning codebases for exposed secrets and auditing Docker container images for CVE vulnerabilities.

---

## ⚡ Features

- **Automated Secret Detection:** Employs [Gitleaks](https://github.com/gitleaks/gitleaks) across all commits and PRs to intercept leaked API keys, tokens, and credentials.
- **Container Vulnerability Auditing:** Uses [Aqua Security Trivy](https://trivy.dev/) to scan Docker images for `CRITICAL` and `HIGH` CVEs prior to deployment.
- **Least-Privilege Docker Build:** Uses a multi-stage Alpine build running under a non-root (`node`) runtime user to mitigate privilege escalation.
- **Zero-Dependency Health Microservice:** Native Node.js HTTP server configured for deterministic container health probes.

---

## 🛠️ Security Gate Architecture
