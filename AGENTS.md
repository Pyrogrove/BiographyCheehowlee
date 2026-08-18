# AGENTS.md

Provider-neutral instructions for any coding agent working in this repository.

## Source priority
1. Direct instructions from the human operator in the current session.
2. `CLAUDE.md` — project-specific constraints (this is a single static HTML file; no bundler, framework, or external CDN dependencies).
3. This file (`AGENTS.md`).
4. `README.md` / `PROJECT.md` for background context.

## Allowed work
- Editing `index.html` in place, keeping it a single self-contained static file (inline CSS/JS, no build step).
- Adding or updating documentation files.
- Read-only inspection: git history, file contents, running the page in a browser for verification.

## Not allowed without explicit human authorization
- Introducing a bundler, framework, package manager, or external CDN dependency.
- Committing, pushing, deploying, or creating releases/tags autonomously.
- Modifying deployment configuration (Vercel project settings, GitHub repo settings).
- Deleting or rewriting `CLAUDE.md`.

## Verification expectations
There is no automated test suite. Before considering a change complete:
- Open `index.html` in a browser and visually confirm the change.
- Check both a mobile viewport (~375px) and a desktop viewport (~1280px).
- If contact links or the vCard QR payload are touched, confirm the exact link/vCard text is correct (e.g. by inspecting the rendered DOM or decoding the generated payload), not just that something renders.

## Git rules
- Do not commit unless explicitly asked.
- Do not push unless explicitly asked, even after committing.
- Do not amend or force-push existing commits.
- Keep commits scoped to one logical change with a clear message.
- Never commit secrets or credentials (none currently exist in this repo).

## Deployment / release
- Do not deploy or trigger a Vercel deployment autonomously.
- Do not create GitHub releases or tags autonomously.
- Any of the above requires explicit, in-the-moment authorization from the human operator — a prior approval does not carry forward to future sessions or unrelated changes.
