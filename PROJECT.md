---
project_name: BiographyCheehowlee
repository: https://github.com/Pyrogrove/BiographyCheehowlee
project_type: static-site
lifecycle: active
stack: HTML/CSS/JS (static, no framework, no build tool)
tags: [link-in-bio, static-site, qr-code, personal-website]
deployment: vercel (github-integrated auto-deploy on push to main; live at biographycheehowlee.vercel.app, verified 2026-08-18 this session — UNVERIFIED from repo/Git history alone)
last_verified: 2026-08-18
---

# PROJECT.md

PyroGrove project metadata. Facts below are verifiable from this repository and its Git history unless marked `UNVERIFIED`.

- **Project name:** BiographyCheehowlee (link-in-bio site for cheehow lee)
- **Repository:** `Pyrogrove/BiographyCheehowlee` on GitHub (remote `origin`: `https://github.com/Pyrogrove/BiographyCheehowlee.git`)
- **Purpose:** Single-page "link in bio" site — contact hub (WhatsApp, Telegram, LinkedIn) with a scannable vCard QR code, meant to be reached primarily via QR-code scan on mobile.
- **Lifecycle / status:** Active, minimal — 2 commits on `main`, both dated 2026-08-17. No open branches other than `main`, no tags.
- **Stack:** Single static `index.html` (HTML/CSS/JS inline). No framework, no package manager, no build tool. Vendors a copy of the MIT-licensed `qrcode-generator` library (inlined, not installed via a package manager).
- **Current capability:**
  - Renders a link-in-bio page with name, role, and about text.
  - Three outbound contact links: WhatsApp (`wa.me`), Telegram (`t.me`), LinkedIn profile.
  - Client-side generated vCard QR code ("Scan to save my contact").
  - Mobile-first responsive layout; CSS motion effects with `prefers-reduced-motion` support.
- **Deployment:** `CLAUDE.md` (tracked in repo) documents the intended method — GitHub → Vercel, auto-deploy on push to `main`, no build command. **UNVERIFIED from repo/Git history:** the actual live URL, current deployment status, and Vercel project configuration — none of this is recorded in tracked files (no `vercel.json`, no `.vercel/`, no CI config referencing Vercel).
- **Verification:** No automated tests exist in the repo. **UNVERIFIED from repo/Git history:** whether/how the site has been manually tested (browser checks, viewport checks) — not recorded in any tracked file.
- **Known limitations:**
  - No automated tests or CI.
  - Contact info duplicated in two places inside `index.html` (link buttons + vCard payload).
  - No `.gitignore` or `LICENSE` file present in the repo.
- **Last material update:** Commit `da55001`, 2026-08-17 — "Add save-contact QR code and project notes" (added the vCard QR feature and `CLAUDE.md`).
- **Next action:** UNVERIFIED — no roadmap, issue tracker, or TODO is recorded anywhere in the repository or Git history.
