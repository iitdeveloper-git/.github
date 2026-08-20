# Organization Archive Candidates Review

**Policy Notice**: Repositories are **never** archived, renamed, or deleted automatically. This document identifies candidates for administrative review to declutter the public GitHub organization, maintain brand prestige, and protect proprietary or client-specific code.

---

## 📋 Evaluation Criteria

A repository is evaluated as an **Archive Candidate** if it meets one or more of the following:
1. **Duplicate or Superseded**: Another repository actively supersedes this codebase with superior features.
2. **Abandoned Demonstration / PoC**: Temporary exploratory spike or client demo that has completed its lifecycle and has had no commits for over 6 months.
3. **Low Public Value / Incomplete**: Empty, broken, or boilerplate-only repositories that dilute public organization quality.

---

## 🗄️ Detailed Candidate Evaluations

### 1. `demo_wisdom-wings-public-school`
* **Repository**: `demo_wisdom-wings-public-school`
* **WHY**: Initial demonstration mock for a client school website. A dedicated production repository `wisdom-wings-public-school` exists with finalized assets and clean code.
* **REPLACEMENT**: `https://github.com/iitdeveloper-git/wisdom-wings-public-school`
* **DEPENDENCIES**: Static HTML/CSS/JS assets.
* **DEPLOYMENTS**: Static web hosting / Netlify staging demo.
* **NETLIFY / Vercel / CI Dependencies**: Check if any live staging subdomain points to this repository's webhooks.
* **CLIENT IMPACT**: None once DNS points to the production repository deployment.
* **RISK**: Low. Verify all custom media assets are preserved in `wisdom-wings-public-school`.
* **Recommendation**: **ARCHIVE CANDIDATE** (Make read-only / archive after webhook audit).

---

### 2. `demo_shriji_mandapam`
* **Repository**: `demo_shriji_mandapam`
* **WHY**: Direct clone of `Shri-Ji-Mandapam` created for client preview staging. Both contain identical Next.js frontend codebases.
* **REPLACEMENT**: `https://github.com/iitdeveloper-git/Shri-Ji-Mandapam`
* **DEPENDENCIES**: Next.js 14, React, TailwindCSS.
* **DEPLOYMENTS**: Vercel preview deployment.
* **NETLIFY / Vercel / CI Dependencies**: Verify whether Vercel preview URLs are bound to this specific repo.
* **CLIENT IMPACT**: None if canonical domain points to `Shri-Ji-Mandapam`.
* **RISK**: Very Low.
* **Recommendation**: **ARCHIVE CANDIDATE** (Archive after verifying domain redirects).

---

### 3. `ett-frontend`
* **Repository**: `ett-frontend`
* **WHY**: Legacy initial Next.js scaffold for the early Oryne prototype. Unmodified since November 2025. Contains default `create-next-app` boilerplate with early design notes.
* **REPLACEMENT**: Modern platform architectures under `iam` and `ett_gns`.
* **DEPENDENCIES**: Legacy Node dependencies.
* **DEPLOYMENTS**: None active.
* **NETLIFY / Vercel / CI Dependencies**: None.
* **CLIENT IMPACT**: None. Internal architectural notes already documented.
* **RISK**: Low.
* **Recommendation**: **ARCHIVE CANDIDATE** (Archive with read-only status).

---

### 4. `oryne_web`
* **Repository**: `oryne_web`
* **WHY**: Single HTML landing page and architecture markdown file for legacy Oryne project. Unmodified since April 2026.
* **REPLACEMENT**: Current IITDEVELOPER website (`iitdeveloper-website`).
* **DEPENDENCIES**: Standalone static HTML file.
* **DEPLOYMENTS**: None active.
* **NETLIFY / Vercel / CI Dependencies**: None.
* **CLIENT IMPACT**: None.
* **RISK**: Very Low.
* **Recommendation**: **ARCHIVE CANDIDATE** (Archive with read-only status).

---

## ⚠️ Client Repository Governance & Safety

Several repositories in the organization represent client deliverables:
* `demo_hospital1` (AarogyaCare ERP)
* `demo_hospital2` (Doctor portfolio)
* `hotel_demo1` / `hotel_demo2` (Hotel booking showcase)
* `Shyama-Public-School`
* `wisdom-wings-public-school`
* `ghar-ka-dabba`
* `Shri-Ji-Mandapam`
* `pulsarip` (Intellectual Property & Legal Services platform)

### Recommended Action Plan:
1. **Sanitization Pass**: Verify that no live SMTP credentials, database passwords, or customer PII exist in `.env` or commit history.
2. **Classification**: Group under a dedicated client showcase section or migrate to private repositories upon client contract requirements.
3. **Attribution**: Ensure each repository has an informative README attributing IITDEVELOPER as the platform engineering architect.
