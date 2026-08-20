# IITDEVELOPER DevSecOps Baseline Controls

**Version**: 1.0  
**Status**: Organization Standard  
**Scope**: All repositories in `iitdeveloper-git`  

---

## 🎯 Objective

This standard defines the baseline security, code quality, dependency hygiene, and deployment controls for all IITDEVELOPER software repositories. Every control is categorized into one of four tiers:

* **REQUIRED**: Mandatory for all Flagship and Active production repositories.
* **RECOMMENDED**: Best practice to implement across all repositories.
* **OPTIONAL**: Advanced controls based on project maturity and compliance requirements.
* **NOT APPLICABLE**: Controls not suited for specific repository types (e.g., pure documentation repos).

---

## 🛡️ Control Matrix

| Control Category | Control Name | Tier | Enforcement Mechanism |
| :--- | :--- | :--- | :--- |
| **Source Integrity** | Branch Protection on `main` / `master` | **REQUIRED** | GitHub Branch Protection Rules |
| **Source Integrity** | Minimum 1 Approving Review | **REQUIRED** | Branch Protection Settings |
| **Source Integrity** | Linear Git History / Conventional Commits | **RECOMMENDED** | Repository Setting / Git Hook |
| **Permissions** | Least Privilege Actions Permissions (`contents: read`) | **REQUIRED** | Workflow `permissions` block |
| **Secret Protection** | Secret Scanning & Push Protection | **REQUIRED** | GitHub Organization Security Settings |
| **Secret Protection** | Zero Plaintext Credentials in Commits | **REQUIRED** | Automated pre-commit / CI scanner |
| **Code Quality** | Static Application Security Testing (SAST / CodeQL) | **REQUIRED** | GitHub Actions (`codeql.yml`) |
| **Code Quality** | Automated Linters & Formatters (`ruff`, `eslint`) | **REQUIRED** | GitHub Actions CI workflows |
| **Dependencies** | Dependabot Version & Security Updates | **REQUIRED** | `.github/dependabot.yml` |
| **Dependencies** | Pull Request Dependency Review | **RECOMMENDED** | GitHub Actions (`dependency-review.yml`) |
| **Containers** | Multi-stage Docker Builds with Non-root User | **REQUIRED** | Dockerfile best practices |
| **Containers** | Container Vulnerability Scanning (Trivy / Snyk) | **RECOMMENDED** | CI Container Build Stage |
| **Ownership** | Code Ownership (`CODEOWNERS`) | **RECOMMENDED** | `.github/CODEOWNERS` |
| **Supply Chain** | Software Bill of Materials (SBOM) Generation | **OPTIONAL** | GitHub Actions Release workflow |
| **Releases** | Semantic Versioning & Signed Git Tags | **REQUIRED** | Release workflow (`vX.Y.Z`) |

---

## 📦 Dependabot Implementation Standard

For active repositories, add `.github/dependabot.yml` configured with sensible polling cadences to minimize noise while patching critical vulnerabilities promptly.

### Recommended `dependabot.yml` Specification:

```yaml
version: 2
updates:
  # Python Backend dependencies
  - package-ecosystem: "pip"
    directory: "/"
    schedule:
      interval: "weekly"
      day: "monday"
    open-pull-requests-limit: 5
    reviewers:
      - "OWNER REQUIRED"

  # Frontend Node/TypeScript dependencies
  - package-ecosystem: "npm"
    directory: "/"
    schedule:
      interval: "weekly"
      day: "monday"
    open-pull-requests-limit: 5
    reviewers:
      - "OWNER REQUIRED"

  # GitHub Actions Workflows
  - package-ecosystem: "github-actions"
    directory: "/"
    schedule:
      interval: "monthly"
    open-pull-requests-limit: 3

  # Docker dependencies
  - package-ecosystem: "docker"
    directory: "/"
    schedule:
      interval: "monthly"
    open-pull-requests-limit: 3
```

---

## 👥 CODEOWNERS Standard

Every flagship repository should define explicit module ownership via `.github/CODEOWNERS`:

```text
# Global repository fallback owners
*                      @iitdeveloper-git/platform-leads

# Backend and API services
/backend/              @iitdeveloper-git/backend-engineers
/src/                  @iitdeveloper-git/backend-engineers

# Frontend applications
/frontend/             @iitdeveloper-git/frontend-engineers
/web/                  @iitdeveloper-git/frontend-engineers

# CI/CD and Infrastructure
/.github/workflows/    @iitdeveloper-git/devops-architects
/docker/               @iitdeveloper-git/devops-architects
Dockerfile             @iitdeveloper-git/devops-architects
docker-compose*.yml    @iitdeveloper-git/devops-architects

# Security and Community governance
SECURITY.md            @iitdeveloper-git/security-response
```

> *Note: If team handles have not yet been assigned in the organization, assign the organization owner or mark as `OWNER REQUIRED` until teams are populated.*

---

## 🚀 Release Engineering & Semantic Versioning

All flagship projects must adhere to [Semantic Versioning (SemVer)](https://semver.org/):

* **MAJOR (`vX.0.0`)**: Incompatible API or architectural breaking changes.
* **MINOR (`v1.X.0`)**: Backward-compatible new functionality or endpoints.
* **PATCH (`v1.0.X`)**: Backward-compatible bug fixes and security remediations.

Tags must follow the `vX.Y.Z` format and be accompanied by automated release notes generated by the organization's release workflow template.
