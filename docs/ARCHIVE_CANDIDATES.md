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
* **Reason**: Initial demonstration mock for a client school website. A dedicated production repository `wisdom-wings-public-school` exists with refined assets and finalized code.
* **Last Meaningful Activity**: July 5, 2026
* **Replacement / Canonical Version**: `https://github.com/iitdeveloper-git/wisdom-wings-public-school`
* **Risk**: Low. Ensure no unique client assets or historical branches exist that aren't merged into the main repo.
* **Recommendation**: **ARCHIVE CANDIDATE** (or make private). Mark README with a deprecation notice pointing to `wisdom-wings-public-school`.

---

### 2. `demo_shriji_mandapam`
* **Repository**: `demo_shriji_mandapam`
* **Reason**: Direct duplicate of `Shri-Ji-Mandapam` created during demo staging. Both contain identical Next.js frontend codebases.
* **Last Meaningful Activity**: July 23, 2026
* **Replacement / Canonical Version**: `https://github.com/iitdeveloper-git/Shri-Ji-Mandapam`
* **Risk**: Very Low. Codebase is an identical clone.
* **Recommendation**: **ARCHIVE CANDIDATE** (or delete/make private after verifying DNS/deployment webhooks).

---

### 3. `ett-frontend`
* **Repository**: `ett-frontend`
* **Reason**: Legacy initial Next.js scaffold for the early Oryne prototype. Unmodified since November 2025. Contains default `create-next-app` boilerplate with early design notes.
* **Last Meaningful Activity**: November 11, 2025
* **Replacement / Canonical Version**: Modern platform architectures under `iam` and `ett_gns`.
* **Risk**: Low. Ensure design notes in `docs/` are archived or migrated to company knowledge base.
* **Recommendation**: **ARCHIVE CANDIDATE**. Archive repository with read-only status.

---

### 4. `oryne_web`
* **Repository**: `oryne_web`
* **Reason**: Single HTML landing page and architecture markdown file for legacy Oryne project. Unmodified since April 2026.
* **Last Meaningful Activity**: April 25, 2026
* **Replacement / Canonical Version**: Current IITDEVELOPER website and platform services.
* **Risk**: Very Low.
* **Recommendation**: **ARCHIVE CANDIDATE**. Mark as archived read-only showcase or consolidate docs into internal archive.

---

## ⚠️ Client Repository Separation Strategy

Several repositories in the organization represent client projects:
* `demo_hospital1` (AarogyaCare ERP)
* `demo_hospital2` (Cardiology doctor portfolio)
* `hotel_demo1` / `hotel_demo2` (Hotel booking showcase)
* `Shyama-Public-School`
* `wisdom-wings-public-school`
* `ghar-ka-dabba`
* `Shri-Ji-Mandapam`

### Recommended Action Plan for Client Repos:
1. **Sanitization Pass**: Verify that no live SMTP credentials, database passwords, or customer PII exist in `.env`, `.env.example`, or commit history.
2. **Classification**: Group under a dedicated "Client Showcases" section or transition to an internal `iitdeveloper-client-delivery` organization/team structure.
3. **Branding**: Ensure each repository has an informative README attributing IITDEVELOPER as the engineering architect.
