# cheehow lee — link-in-bio site

Single self-contained `index.html` (no build step, no framework, no package.json). Everything — CSS and JS — is inlined in the one file, including a vendored copy of the `qrcode-generator` library (MIT, Kazuhiko Arase) used to render the "scan to save my contact" vCard QR code.

Deployed via GitHub → Vercel (Vercel auto-deploys on push to `main`, no build command needed — it's served as-is).

When editing: keep it a single static file. Don't introduce a bundler, framework, or external CDN dependencies — the point is instant load for QR-code scans on mobile.
