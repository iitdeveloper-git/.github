# IITDEVELOPER AI-Assisted Engineering Standard

**Version**: 1.0  
**Scope**: Organization-wide Engineering Practice  
**Applies to**: All developers, contractors, and automated AI agents contributing to `iitdeveloper-git`  

---

## 🎯 Purpose & Philosophy

At **IITDEVELOPER**, we actively incorporate AI engineering agents (such as Claude Code, OpenAI Codex, and Google Antigravity) into our daily development lifecycle. We view AI agents as powerful force multipliers that accelerate implementation velocity, broaden test coverage, and improve documentation quality.

However, **AI systems do not replace engineering judgment, architectural discipline, or security accountability**. 

We maintain a firm **Human-in-the-Loop** model:

> *"AI agents assist and scaffold; human engineers verify, architect, and approve."*

---

## 🤖 Division of Responsibilities

```
┌──────────────────────────────────────────────┐
│             AI CODING AGENTS                 │
│  Research  •  Scaffolding  •  Unit Tests     │
│  Documentation  •  Refactoring Proposals     │
└──────────────────────┬───────────────────────┘
                       │ (Proposals / Drafts)
                       ▼
┌──────────────────────────────────────────────┐
│           HUMAN LEAD ENGINEERS               │
│  Architecture  •  Security & Auth  •  Review │
│  Data Migrations  •  Production Deployment   │
└──────────────────────────────────────────────┘
```

---

### 1. What AI Agents May Assist With
AI coding agents are encouraged to assist with:
* **Exploratory Research**: Comparing libraries, surveying API specs, and parsing documentation.
* **Code Scaffolding**: Generating initial project skeletons, standard boilerplate, and CRUD controllers.
* **Unit & Integration Test Generation**: Writing boundary-case test fixtures, mock data generators, and regression suites.
* **Documentation & OpenAPI Specs**: Generating docstrings, Markdown summaries, and API schema annotations.
* **Static Analysis & Refactoring**: Identifying dead code, suggesting idiomatic typing, and modernizing legacy patterns.

---

### 2. Mandatory Human Review & Authority
A qualified human engineer **must explicitly review and approve** any code affecting:
* **Authentication & Authorization**: Identity tokens, OAuth2 / OIDC flows, JWT verification, session cookies, RBAC policies.
* **Cryptography & Hashing**: Key generation, encryption algorithms, hashing salts, certificates.
* **Data Migrations & Schema Changes**: Database alter statements, index creation, cascading deletes, migration scripts.
* **Infrastructure & Cloud Permissions**: IAM roles, GitHub Actions secret handling, ingress security rules, Kubernetes manifests.
* **Billing & External Side Effects**: Payment gateway integrations, external billing triggers, mass email/SMS dispatches.
* **Production Deployments**: Merge to release branches and deployment approvals.

---

## 📂 Standard for Agent Configuration Files

To give AI agents accurate project context without conflicting instructions, flagship repositories should maintain standard agent instruction files:

### 1. Canonical `AGENTS.md`
Place `AGENTS.md` at the repository root. This file serves as the single source of truth for all AI agents.

```markdown
# Repository Agent Guidelines

## Tech Stack & Architecture
- Language: Python 3.12 (FastAPI)
- Database: PostgreSQL with SQLAlchemy Async
- Cache/Broker: Redis & RabbitMQ

## Build & Test Commands
- Run Tests: `pytest`
- Lint: `ruff check .`
- Type Check: `mypy src/`

## Critical Invariants
- Never commit hardcoded secrets or passwords.
- Always use async database sessions.
- Preserve existing docstrings and typing.
```

### 2. Tool-Specific References (`CLAUDE.md`, `.cursorrules`, etc.)
To prevent drift across different AI tools, tool-specific files must reference the canonical `AGENTS.md`:

```markdown
# Claude Code Guidelines
Please adhere to the repository standards defined in [AGENTS.md](./AGENTS.md).
```

---

## 🚫 Prohibited Practices

1. **No Unverified Hallucinations**: Never commit code referencing unverified third-party libraries, fake APIs, or made-up URLs.
2. **No Blind Commit & Push**: Never allow an automated agent to push directly to protected branches (`main`/`master`) without human pull request review.
3. **No Exaggerated Marketing Claims**: Do not label projects with unrealistic phrases such as *"100% Autonomous AI-Built"* or *"Zero-Human Software"*. Be honest about the engineering craftsmanship behind our systems.
