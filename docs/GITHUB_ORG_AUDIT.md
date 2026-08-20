# IITDEVELOPER GitHub Organization Comprehensive Audit

**Date**: August 2026  
**Auditor**: Principal Platform & DevOps Architect  
**Organization**: `https://github.com/iitdeveloper-git`  
**Total Public Repositories Audited**: 21  

---

## 📊 Executive Audit Summary

The IITDEVELOPER GitHub organization (`iitdeveloper-git`) comprises 21 public repositories spanning enterprise platform services (IAM, GNS), commercial web portals, reusable CI/CD tooling, and client demo projects. 

### Key Findings:
1. **Core Flagship Platforms**: High-value, actively developed architectures exist in `iam` (Enterprise Identity & Access Management), `ett_gns` (Generic Notification Service), `iitdeveloper-website` (Corporate Platform), `demo_website_growixa` (AI Growth Canvas), and `iitdeveloper-git-shared-workflows` (Reusable CI/CD & Deployment Actions).
2. **Metadata & Presentation Gaps**: Most repositories currently lack repository descriptions, homepage URLs, and GitHub topics, making discoverability sub-optimal.
3. **Demo & Client Repository Sprawl**: Several repositories represent client-specific websites or demonstration mockups (e.g. `demo_hospital1`, `demo_hospital2`, `hotel_demo1`, `hotel_demo2`, `Shyama-Public-School`, `wisdom-wings-public-school`). These should be categorized and curated to prevent brand dilution.
4. **DevSecOps Readiness**: While core platforms (`iam`, `ett_gns`, `pulsarip`, `iitdeveloper-git-shared-workflows`) possess CI/CD and Docker setups, organization-wide CodeQL, Dependabot, and branch protection standards require formalization.

---

## 📋 Comprehensive Repository Audit Table

| # | Repository | Vis. | Primary Lang | Last Activity | CI/CD | Docker | README | License | Dependabot / CodeQL | Security / Contrib | Purpose & Tech | Recommended Action |
| :- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | **iam** | Public | Python | 2026-08-13 | 5 Workflows | Yes | Yes (Rich) | No | None | Agents/Docs present | Enterprise IAM platform (FastAPI, Keycloak, PostgreSQL, Redis, Next.js) | **FLAGSHIP** |
| 2 | **ett_gns** | Public | Python | 2026-06-27 | 5 Workflows | Yes | Yes (Rich) | No | None | Agents/Docs present | Generic Notification Service (FastAPI, RabbitMQ, Redis, Celery) | **FLAGSHIP** |
| 3 | **iitdeveloper-website** | Public | TypeScript | 2026-08-17 | None | Yes | Yes | MIT | None | Docs present | Official IITDEVELOPER Corporate Platform (Next.js, TypeScript, Tailwind) | **FLAGSHIP** |
| 4 | **demo_website_growixa** | Public | TypeScript | 2026-08-08 | None | No | Missing | No | None | None | Growixa AI Growth Canvas & Product Suite (Next.js, React, Tailwind) | **FLAGSHIP** |
| 5 | **iitdeveloper-git-shared-workflows** | Public | Python | 2026-08-20 | 1 Workflow | No | Yes (Rich) | No | None | None | Reusable GitHub Actions, Telegram deployment alerts, platform automations | **FLAGSHIP** |
| 6 | **pulsarip** | Public | TypeScript | 2026-07-13 | 1 Workflow | Yes | Yes | No | None | Claude config | IP intelligence and network lookup service (Next.js, TypeScript, Docker) | **SHOWCASE** |
| 7 | **touchmark** | Public | Markdown / Docs | 2026-08-13 | None | No | Yes | MIT | None | PRD & Specs | Auto-documentation platform specifications & research | **EXPERIMENT** |
| 8 | **prompts** | Public | Markdown | 2026-06-25 | None | No | Yes | No | None | Skills structure | Prompt engineering repository & AI agent execution skills | **INTERNAL** |
| 9 | **.github** | Public | Markdown | 2026-08-20 | Reusable | No | Newly Created | CC0 | Configured | CoC, Contrib, Sec | Organization Control Center & default community templates | **INTERNAL** |
| 10 | **ett-frontend** | Public | JavaScript | 2025-11-11 | None | No | Boilerplate | No | None | Oryne Docs | Legacy Oryne Next.js frontend | **ARCHIVE CANDIDATE** |
| 11 | **oryne_web** | Public | HTML | 2026-04-25 | None | No | Minimal | No | None | Multitenancy Report | Static landing page for Oryne | **ARCHIVE CANDIDATE** |
| 12 | **demo_hospital1** | Public | Blade / PHP | 2026-07-02 | 1 Workflow | Yes | Yes | No | None | Docs present | AarogyaCare Hospital ERP & Clinic Management | **CLIENT** |
| 13 | **demo_hospital2** | Public | Astro | 2026-07-21 | None | No | Yes | No | None | Content guides | Cardiology Doctor Portfolio & Medical Site (Astro, Tailwind) | **CLIENT** |
| 14 | **hotel_demo1** | Public | TypeScript | 2026-07-02 | None | No | Missing | No | None | None | Luxury Hotel & Resort Showcase (Next.js, TypeScript) | **CLIENT** |
| 15 | **hotel_demo2** | Public | TypeScript | 2026-07-08 | None | No | Missing | No | None | None | Boutique Hotel showcase iteration 2 (Next.js, TypeScript) | **CLIENT** |
| 16 | **Shyama-Public-School** | Public | HTML | 2026-06-27 | None | No | Yes | No | None | Client notes | School institutional website (HTML, CSS, JS) | **CLIENT** |
| 17 | **wisdom-wings-public-school** | Public | HTML | 2026-07-06 | None | No | Yes | No | None | Client notes | Wisdom Wings School institutional website | **CLIENT** |
| 18 | **demo_wisdom-wings-public-school** | Public | HTML | 2026-07-05 | None | No | Yes | No | None | Client notes | Demo iteration for Wisdom Wings School | **ARCHIVE CANDIDATE** |
| 19 | **ghar-ka-dabba** | Public | CSS / Node | 2026-07-07 | None | No | Yes | No | None | AGENTS.md, CLAUDE.md | Tiffin & Meal Delivery platform (Node.js, Vanilla CSS/JS) | **CLIENT** |
| 20 | **Shri-Ji-Mandapam** | Public | TypeScript | 2026-07-23 | None | No | Yes | No | None | UI components | Banquet & Event Venue portal (Next.js, TypeScript) | **CLIENT** |
| 21 | **demo_shriji_mandapam** | Public | TypeScript | 2026-07-23 | None | No | Yes | No | None | UI components | Duplicate/demo branch of Shri-Ji-Mandapam | **ARCHIVE CANDIDATE** |

---

## 🔍 Detailed Analysis by Classification

### 1. Flagship Repositories (5)
* **`iam`**: Enterprise-grade identity engine. Features FastAPI microservices, Keycloak federation, multi-tenant RBAC, Next.js admin frontend, Docker multi-container compose, and comprehensive deployment workflows.
* **`ett_gns`**: Multi-channel notification pipeline. High-throughput event handling via RabbitMQ, FastAPI, and Redis workers.
* **`iitdeveloper-website`**: Corporate flagship site representing IITDEVELOPER. Clean Next.js + Tailwind codebase.
* **`demo_website_growixa`**: Core product interface for Growixa AI Growth platform. High-potential product needing formal README and CI pipeline.
* **`iitdeveloper-git-shared-workflows`**: Central platform engineering asset hosting reusable CI/CD workflows and automated Telegram deployment dispatchers.

### 2. Showcase & Active Repositories (2)
* **`pulsarip`**: Modern IP lookup tool. Features clean Docker containerization, CI workflow, and TypeScript frontend.
* **`touchmark`**: Early-stage documentation automation engine with detailed PRD and research documentation.

### 3. Client & Vertical Solutions (7)
* Repositories representing client deliverables: `demo_hospital1`, `demo_hospital2`, `hotel_demo1`, `hotel_demo2`, `Shyama-Public-School`, `wisdom-wings-public-school`, `ghar-ka-dabba`, `Shri-Ji-Mandapam`.
* Recommendation: Retain in organization or move to private/client visibility after client approval. Apply standardized sanitization so that no client credentials or sensitive configs are exposed.

### 4. Archive Candidates (4)
* **`demo_wisdom-wings-public-school`**: Superseded by `wisdom-wings-public-school`.
* **`demo_shriji_mandapam`**: Direct duplicate of `Shri-Ji-Mandapam`.
* **`ett-frontend`**: Stale legacy Oryne prototype (unmodified since Nov 2025).
* **`oryne_web`**: Stale static demo landing page.

---

## 🔒 Security Audit Summary

* **Credentials & Secrets**: No plaintext database passwords or live cloud API keys exposed in committed code. Environment templates correctly use `.env.example` across key repos.
* **Configuration Safety**: `frontend/.env.development` in `iitdeveloper-website` and `ett_gns_app/secrets.py` in `ett_gns` contain environment property keys; these should continue to be managed via GitHub Actions Secrets rather than checked-in values.
* **Dependency Vulnerabilities**: Dependabot should be enabled across Python (`pip`) and Node.js (`npm`) ecosystems.

---

## 🎯 Recommended Next Actions

1. Pin the **Top 6 Repositories** to the organization landing page (`iam`, `ett_gns`, `demo_website_growixa`, `iitdeveloper-website`, `iitdeveloper-git-shared-workflows`, `pulsarip`).
2. Add rich descriptions, homepage links, and curated topics to all active repositories.
3. Establish DevSecOps baseline controls across all tier-1 repositories.
