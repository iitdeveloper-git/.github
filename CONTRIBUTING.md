# Contributing to IITDEVELOPER Repositories

Thank you for your interest in contributing to **IITDEVELOPER** projects. We welcome high-quality contributions from developers, platform engineers, and AI researchers across our open-source and public repositories.

---

## 🧭 Code of Conduct

All contributors and participants must adhere to our [Code of Conduct](./CODE_OF_CONDUCT.md). Please read it before engaging in any project activity.

---

## 🛠️ Development & Contribution Workflow

We practice a disciplined, trunk-based or GitHub-flow development workflow.

### 1. Find or Open an Issue
Before submitting non-trivial changes, open an issue using the appropriate template:
- **Bug Report**: Reproducible problem with error logs.
- **Feature Request**: Clear problem statement, architectural proposal, and alternatives.
- **Documentation**: Corrections or additions to guides, APIs, and setup docs.

### 2. Branch Naming Conventions
Always create a focused branch from the default branch (`main` or `master` depending on the repository):

| Branch Type | Syntax | Example |
| :--- | :--- | :--- |
| **Feature** | `feature/<component>/<short-desc>` | `feature/iam/oidc-provider-sync` |
| **Bug Fix** | `fix/<component>/<short-desc>` | `fix/gns/rabbitmq-reconnect-backoff` |
| **Documentation** | `docs/<topic>` | `docs/iam-api-architecture` |
| **Refactoring / Chore** | `chore/<component>/<short-desc>` | `chore/deps/bump-pydantic-v2` |
| **CI / DevOps** | `ci/<component>/<short-desc>` | `ci/actions/add-codeql-analysis` |

### 3. Commit Message Standards
We adhere to the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```text
<type>(<scope>): <short summary>

[optional body explaining WHY and WHAT changed]

[optional footer(s) such as Closes #123]
```

Allowed types:
- `feat`: A new feature or capability
- `fix`: A bug fix
- `docs`: Documentation changes only
- `refactor`: Code change that neither fixes a bug nor adds a feature
- `test`: Adding missing tests or correcting existing tests
- `ci`: Changes to CI/CD workflows and automation scripts
- `chore`: Maintenance tasks, dependency updates, tooling config
- `security`: Security patches, CVE remediation, hardening

*Example:* `feat(iam): implement rate limiting middleware for auth endpoints`

---

## 🧪 Quality & Testing Expectations

Every Pull Request must satisfy the repository's automated gates:
1. **Linting & Formatting**: Follow repository style guidelines (e.g., `ruff` / `black` / `flake8` for Python, `eslint` / `prettier` for TypeScript).
2. **Automated Tests**: All new logic must include corresponding unit/integration tests.
3. **No Breaking Changes Without Notice**: Backward-incompatible changes must be flagged in the PR summary and discussed prior to implementation.
4. **No Secrets**: Never commit tokens, `.env` files with credentials, or private certificates.

---

## 🤖 AI-Assisted Contribution Policy

IITDEVELOPER embraces modern AI coding tools (Claude, Codex, Antigravity, GitHub Copilot). However, contributors utilizing AI agents must adhere to the following rules:

1. **Human Ownership**: You are 100% responsible for the code, tests, and documentation you submit.
2. **No Unverified Hallucinations**: Verify all imported packages, API signatures, and external URLs. Do not submit code referencing non-existent dependencies.
3. **Security Review**: AI-generated code dealing with authentication, authorization, cryptography, SQL queries, or file I/O must undergo rigorous manual review.
4. **License Integrity**: Ensure generated code does not infringe on copyrighted or incompatible third-party open-source licenses.

---

## 📬 Submitting a Pull Request

1. Fill out the complete [Pull Request Template](./.github/PULL_REQUEST_TEMPLATE.md).
2. Ensure CI checks pass on your branch.
3. Link related issues (e.g., `Closes #42`).
4. Be responsive to code review feedback.

---

## 🔒 Security Vulnerabilities

If you discover a security vulnerability, **DO NOT** open a public issue. Please follow the instructions in [SECURITY.md](./SECURITY.md).
