# 3D Portfolio (Static) — Technical Notes

## Overview

A static 3D-style portfolio built with HTML, CSS, and JavaScript. It includes a main portfolio page, a CV page, a downloadable resume, and deployment files for Docker, Wrangler, and GitHub Actions.

## Folder structure

```text
frontend/
  index.html          Main portfolio
  cv.html             CV page
  css/styles.css
  js/config.js
  js/scene.js         3D scene logic
  js/scene-extras.js
  profile.svg
  resume.pdf
  Dockerfile
  wrangler.toml
infra/
  Dockerfile
  wrangler.toml
  .github/workflows/  Azure and generic deployment workflows
```

## Preview

Open `frontend/index.html` directly, or serve the folder:

```powershell
cd frontend
python -m http.server 8082
```

Then open <http://localhost:8082/>.

## Deployment

- **Docker**: build from `frontend/` or `infra/` using the included Dockerfile.
- **Cloudflare Pages/Wrangler**: use `frontend/wrangler.toml` or `infra/wrangler.toml`.
- **GitHub Actions**: workflows are under `infra/.github/workflows/`.

Review the workflow files and replace placeholder project names, account IDs, and secrets before using them.

## Verification evidence (2026-11-09)

| Check | Result |
|---|---|
| Static pages and assets | HTTP 200 |
| Local links | Checked |

## Limitations

- Static site only; the contact form and resume are client-side files.
- Deployment workflows were not executed.
- Replace placeholder deployment configuration before publishing.
