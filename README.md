# Cartly — Legal Pages Source

This folder contains the full source of the Cartly public website (`cartly.app`), including the Privacy Policy and Terms of Service. It is a self-contained Jekyll site.

## Files in this folder

| File | Purpose |
|------|---------|
| `index.md` | Landing page at `cartly.app/` |
| `privacy.md` | Privacy Policy served at `cartly.app/privacy/` |
| `terms.md` | Terms of Service served at `cartly.app/terms/` |
| `_config.yml` | Jekyll site configuration |
| `_layouts/default.html` | Page layout (used by all three pages) |
| `CNAME` | GitHub Pages custom-domain config (`cartly.app`) |
| `LAUNCH-OPS.md` | Step-by-step runbook for deploying this site (not published publicly) |

## Where this lives in production

These files are intended to be copied to the **root of a new public repository** (e.g. `cartly-site`) and served by GitHub Pages. See `LAUNCH-OPS.md` for exact deployment steps.

## Why it lives here in the app repo too

The markdown files are source-of-truth for the legal text referenced in the iOS app. Keeping them in-repo:
- lets the app team review legal changes in the same PR flow as app code,
- preserves a diff history of every wording change to the Privacy Policy and Terms (required for GDPR / CCPA auditability), and
- makes it trivial to regenerate the public site if the hosting repo is ever recreated.
