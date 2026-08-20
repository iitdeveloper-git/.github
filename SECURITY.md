# Security Policy

At **IITDEVELOPER**, security, data privacy, and operational integrity are paramount. We appreciate the responsible disclosure of security vulnerabilities by security researchers, engineers, and community members.

---

## 🛡️ Supported Versions

We provide security updates and patches for active flagship platforms and major branches.

| Project / Repository | Supported Branches / Versions | Security Support Status |
| :--- | :--- | :--- |
| **IITD IAM** (`iam`) | `main`, latest tagged releases | ✅ Actively supported |
| **GNS** (`ett_gns`) | `main`, latest tagged releases | ✅ Actively supported |
| **IITDEVELOPER Website** (`iitdeveloper-website`) | `master` | ✅ Actively supported |
| **Growixa** (`demo_website_growixa`) | `main` | ✅ Actively supported |
| **Shared Workflows** (`iitdeveloper-git-shared-workflows`) | `main` | ✅ Actively supported |
| *Legacy Demos / Archived Repos* | None | ❌ Unsupported / Demonstration only |

---

## 🚨 Reporting a Vulnerability

**DO NOT report security vulnerabilities through public GitHub issues, pull requests, or discussions.**

If you believe you have discovered a security vulnerability in any IITDEVELOPER repository or service, please report it privately:

* **Primary Security Contact**: [security@iitdeveloper.com](mailto:security@iitdeveloper.com)
* **General Fallback Contact**: [info@iitdeveloper.com](mailto:info@iitdeveloper.com)
* **Subject Line**: `[SECURITY VULNERABILITY] <Project/Repository Name> - <Brief Summary>`

### What to Include in Your Report

To help us triage and resolve the issue quickly, please provide:
1. **Repository / Component**: The exact repository name, branch, or URL affected.
2. **Vulnerability Type**: (e.g., Authentication bypass, SQL injection, SSRF, RCE, IDOR, sensitive data exposure).
3. **Impact Assessment**: Explanation of how the vulnerability could be exploited and potential impact.
4. **Step-by-Step Proof of Concept (PoC)**: Clear, reproducible steps, curl commands, or script snippets.
5. **Mitigation Suggestion**: Any proposed remediation or code patches (if available).

---

## ⏱️ Response & Triage Process

1. **Acknowledgment**: We aim to acknowledge receipt of your vulnerability report within **48 hours**.
2. **Assessment & Validation**: Our platform engineering team will validate and assess severity within **5 business days**.
3. **Remediation**: Validated critical issues will be prioritized for remediation and deployed promptly.
4. **Public Disclosure / Credit**: We coordinate public disclosure with the reporter once a fix is released. We gladly credit researchers who follow responsible disclosure practices.

---

## 🔒 Security Best Practices for Contributors

* Never commit API keys, database credentials, SSH private keys, or `.env` files containing live secrets.
* Always use environment variables and GitHub Action Secrets for credential management.
* Enable two-factor authentication (2FA) on your GitHub account.
