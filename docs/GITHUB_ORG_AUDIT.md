# IITDEVELOPER GitHub Organization Comprehensive Audit

**Date**: August 2026  
**Auditor**: Principal Platform & DevOps Architect  
**Organization**: `https://github.com/iitdeveloper-git`  
**Total Public Repositories Audited**: 21  

---

## 📊 Executive Audit Summary

The IITDEVELOPER GitHub organization (`iitdeveloper-git`) comprises 21 public repositories spanning platform services (IAM, GNS), commercial web portals, reusable CI/CD tooling, and client demo projects.

### Key Findings:
1. **Core Engineering Platforms**: High-value implementations exist in `iam` (Identity & Access Management with Keycloak & FastAPI), `ett_gns` (Generic Notification Service), `iitdeveloper-website` (Corporate Platform), `demo_website_growixa` (Growixa AI Growth Canvas & Product Suite), and `iitdeveloper-git-shared-workflows` (Reusable GitHub Actions CI/CD & Deployment Dispatchers).
2. **PulsarIP Positioning Clarification**: `pulsarip` is an intellectual property (IP) and legal-tech services platform (trademarks, copyrights, patents, business services) engineered with Next.js, TypeScript, and Docker. It is classified as `SHOWCASE / CLIENT PROJECT`, not as a core infrastructure product.
3. **Growixa Representation**: `demo_website_growixa` currently hosts the Growixa AI growth canvas interface and product showcase. It represents the Growixa product line until the canonical production Growixa repository is made public.
4. **Demo & Client Repository Sprawl**: Client-specific deliverables and demo mockups (`demo_hospital1`, `demo_hospital2`, `hotel_demo1`, `hotel_demo2`, `Shyama-Public-School`, `wisdom-wings-public-school`, `ghar-ka-dabba`, `Shri-Ji-Mandapam`) should be governed under a dedicated client showcase structure.

---

## 📋 Comprehensive Repository Audit Table

| # | Repository | Vis. | Primary Lang | Last Activity | CI/CD | Docker | README | License | Dependabot / CodeQL | Security / Contrib | Purpose & Tech | Recommended Action |
| :- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | **iam** | Public | Python | 2026-08-13 | 5 Workflows | Yes | Yes (Rich) | No | None | Agents/Docs present | Identity & Access Management (FastAPI, Keycloak OIDC, PostgreSQL, Redis, Next.js) | **FLAGSHIP** |
| 2 | **ett_gns** | Public | Python | 2026-06-27 | 5 Workflows | Yes | Yes (Rich) | No | None | Agents/Docs present | Generic Notification Service (FastAPI, RabbitMQ, Redis, Celery) | **FLAGSHIP** |
| 3 | **iitdeveloper-website** | Public | TypeScript | 2026-08-17 | None | Yes | Yes | MIT | None | Docs present | Official IITDEVELOPER Corporate Platform (Next.js, TypeScript, Tailwind) | **FLAGSHIP** |
| 4 | **demo_website_growixa** | Public | TypeScript | 2026-08-08 | None | No | Missing | No | None | None | Growixa AI Growth Canvas & Product Suite (Next.js, React, Tailwind) | **FLAGSHIP (Proxy)** |
| 5 | **iitdeveloper-git-shared-workflows** | Public | Python | 2026-08-20 | 1 Workflow | No | Yes (Rich) | No | None | None | Reusable GitHub Actions, Telegram deployment alerts, platform automations | **FLAGSHIP** |
| 6 | **pulsarip** | Public | TypeScript | 2026-07-13 | 1 Workflow | Yes | Yes | No | None | Claude config | Intellectual Property (IP) & legal services portal (Next.js, TypeScript, Docker) | **SHOWCASE / CLIENT** |
| 7 | **touchmark** | Public | Markdown / Docs | 2026-08-13 | None | No | Yes | MIT | None | PRD & Specs | Auto-documentation platform specifications & research | **EXPERIMENT** |
| 8 | **prompts** | Public | Markdown | 2026-06-25 | None | No | Yes | No | None | Skills structure | Prompt engineering repository & AI agent execution skills | **INTERNAL** |
| 9 | **.github** | Public | Markdown | 2026-08-20 | Reusable | No | Configured | CC0 | Configured | CoC, Contrib, Sec | Organization Control Center & default community templates | **INTERNAL** |
| 10 | **ett-frontend** | Public | JavaScript | 2025-11-11 | None | No | Boilerplate | No | None | Oryne Docs | Legacy Oryne Next.js frontend scaffold | **ARCHIVE CANDIDATE** |
| 11 | **oryne_web** | Public | HTML | 2026-04-25 | None | No | Minimal | No | None | Multitenancy Report | Static landing page for legacy Oryne project | **ARCHIVE CANDIDATE** |
| 12 | **demo_hospital1** | Public | Blade / PHP | 2026-07-02 | 1 Workflow | Yes | Yes | No | None | Docs present | AarogyaCare Hospital ERP & Clinic Management | **CLIENT** |
| 13 | **demo_hospital2** | Public | Astro | 2026-07-21 | None | No | Yes | No | None | Content guides | Cardiology Doctor Portfolio & Medical Site (Astro, Tailwind) | **CLIENT** |
| 14 | **hotel_demo1** | Public | TypeScript | 2026-07-02 | None | No | Missing | No | None | None | Luxury Hotel & Resort Showcase (Next.js, TypeScript) | **CLIENT** |
| 15 | **hotel_demo2** | Public | TypeScript | 2026-07-08 | None | No | Missing | No | None | None | Boutique Hotel showcase iteration 2 (Next.js, TypeScript) | **CLIENT** |
| 16 | **Shyama-Public-School** | Public | HTML | 2026-06-27 | None | No | Yes | No | None | Client notes | School institutional website (HTML, CSS, JS) | **CLIENT** |
| 17 | **wisdom-wings-public-school** | Public | HTML | 2026-07-06 | None | No | Yes | No | None | Client notes | Wisdom Wings School institutional website | **CLIENT** |
| 18 | **demo_wisdom-wings-public-school** | Public | HTML | 2026-07-05 | None | No | Yes | No | None | Client notes | Demo iteration for Wisdom Wings School | **ARCHIVE CANDIDATE** |
| 19 | **ghar-ka-dabba** | Public | CSS / Node | 2026-07-07 | None | No | Yes | No | None | AGENTS.md, CLAUDE.md | Tiffin & Meal Delivery platform (Node.js, Vanilla CSS/JS) | **CLIENT** |
| 20 | **Shri-Ji-Mandapam** | Public | TypeScript | 2026-07-23 | None | No | Yes | No | None | UI components | Banquet & Event Venue portal (Next.js, TypeScript) | **CLIENT** |
| 21 | **demo_shriji_mandapam** | Public | TypeScript | 2026-07-23 | None | No | Yes | No | None | UI components | Duplicate demo branch of Shri-Ji-Mandapam | **ARCHIVE CANDIDATE** |

---

## 🏷️ Actionable Repository Metadata Table

The following metadata should be updated in repository settings on GitHub by organization administrators:

| Repository | Recommended Description | Recommended Homepage | Recommended Topics | Classification | Pinned? | Archive? | Manual Review? |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **`demo_website_growixa`** | `AI-powered growth acceleration and marketing automation platform engineered with Next.js, TypeScript, and AI canvas workflows.` | `https://growixa.com` | `iitdeveloper, ai-agents, growth-hacking, nextjs, typescript, react, tailwind, saas` | FLAGSHIP (Proxy) | **Yes (Pin 1)** | No | Yes (Replace with canonical repo when available) |
| **`iam`** | `Enterprise Identity & Access Management platform with Keycloak OIDC integration, FastAPI backend, and Next.js admin console.` | `https://iitdeveloper.com` | `iitdeveloper, identity-management, keycloak, fastapi, postgresql, redis, oidc, docker` | FLAGSHIP | **Yes (Pin 2)** | No | No |
| **`ett_gns`** | `High-throughput, event-driven multi-channel notification service supporting email, push, and messaging with RabbitMQ and FastAPI.` | `https://iitdeveloper.com` | `iitdeveloper, notifications, rabbitmq, fastapi, python, redis, event-driven, microservices` | FLAGSHIP | **Yes (Pin 3)** | No | No |
| **`iitdeveloper-website`** | `Official corporate platform and engineering portfolio for IITDEVELOPER — Intelligence, Innovation & Technology.` | `https://iitdeveloper.com` | `iitdeveloper, company-website, nextjs, typescript, react, tailwindcss, docker` | FLAGSHIP | **Yes (Pin 4)** | No | No |
| **`iitdeveloper-git-shared-workflows`** | `Organization-wide reusable GitHub Actions workflows, custom composite actions, and automated Telegram deployment notifications.` | `https://iitdeveloper.com` | `iitdeveloper, github-actions, devops, ci-cd, automation, telegram-bot, platform-engineering` | FLAGSHIP | **Yes (Pin 5)** | No | No |
| **`pulsarip`** | `Intellectual property (IP), trademark, patent, and legal services platform engineered with Next.js, TypeScript, and Docker.` | `https://pulsarip.com` | `iitdeveloper, intellectual-property, legal-tech, trademark, patent, nextjs, typescript, docker` | SHOWCASE / CLIENT | **Yes (Pin 6 - Temp)** | No | Yes (Replace when Labs is launched) |
| **`touchmark`** | `Automated developer documentation engine specifications, product requirements, and architecture research.` | `https://touchmark.dev` | `iitdeveloper, documentation-tool, developer-tools, research, specs` | EXPERIMENT | No | No | No |

---

## 🔒 Security Summary

* **Private Vulnerability Reporting**: Enabled via GitHub Settings on public flagship repositories.
* **Reporting Contact**: `info@iitdeveloper.com` (`security@iitdeveloper.com` recommended for future mailbox setup).
* **Vulnerability Disclosure Policy**: Outlined in [`SECURITY.md`](../SECURITY.md).
