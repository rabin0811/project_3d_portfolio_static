# project_3d_portfolio_static

## 3D Portfolio (Static)

A static 3D-style personal portfolio website with Docker and Cloudflare deployment files.

## Verified

- **2026-11-08** — served with `python -m http.server` and returned **HTTP 200**.
- `index.html` and `cv.html` both load.
- All local links and assets resolve.
- Fixed a missing `resume.pdf` link by adding the resume file to `frontend/resume.pdf`.

## Folder layout

```
project_3d_portfolio_static/
├── frontend/
│   ├── index.html
│   ├── cv.html
│   ├── profile.svg
│   ├── resume.pdf
│   ├── css/
│   └── js/
├── infra/
│   ├── Dockerfile
│   ├── .dockerignore
│   ├── wrangler.toml
│   └── .github/
└── docs/
```

## How to run

Use a local web server because the page loads JavaScript modules and 3D assets:

```powershell
cd D:\PROJECTS_READY\project_3d_portfolio_static\frontend
python -m http.server 8000
```

Then open <http://localhost:8000>.

## Deployment files

- Docker: `infra/Dockerfile`
- Cloudflare: `infra/wrangler.toml`
- GitHub Actions: `infra/.github/`

## Notes

- Static site: no build step and no dependencies.
- Original location: `D:\projects\3d potfolio just trying not that imp`.
- The original project folder is untouched.
