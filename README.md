# cheehow lee — Link-in-Bio Site

A single-page "link in bio" site for cheehow lee, Freelance Workflow Transformation Consultant. Designed to be opened via QR-code scan on a phone.

## What this is
- One self-contained `index.html` — no build step, no framework, no `package.json`.
- WhatsApp, Telegram, and LinkedIn contact links.
- A "Scan to save my contact" vCard QR code (generated client-side using a vendored copy of the MIT-licensed `qrcode-generator` library by Kazuhiko Arase).
- Warm, mobile-first design with subtle motion (CSS animations, tap feedback), respects `prefers-reduced-motion`.

## Running it locally
No install, no server required:
1. Clone the repo.
2. Open `index.html` directly in any browser (double-click, or `file://` path).

There is no dev server, package manager, or build tooling — it's a static file.

## Deployment
Per `CLAUDE.md`, this project is intended to deploy via **GitHub → Vercel**: Vercel auto-deploys on push to `main`, with no build command (served as static files as-is). The specific live URL is not tracked in this repository — check the project's Vercel dashboard for the current deployment.

## Known limitations
- No automated tests — verification is manual (open in browser, check links, check responsive layout).
- No CI/CD pipeline defined in-repo.
- The vendored QR library is inlined directly into `index.html` rather than imported as a dependency, since the project intentionally has no package manager.
- Contact details (phone number, Telegram, LinkedIn) are hardcoded in both the vCard QR payload and the link buttons — updating them requires editing `index.html` in two places.
