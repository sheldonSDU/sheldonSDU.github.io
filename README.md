# MkDocs Material Template (ESP32 Guide Style)

This repository is a **ready-to-use** MkDocs + Material template, similar to `ESP32-Guide` style sites.

## Quick Start (Local)
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
source .venv/bin/activate

pip install -r requirements.txt
mkdocs serve
```
Open: http://127.0.0.1:8000/

## Deploy to GitHub Pages (Auto via Actions)
1. Create a GitHub repo (e.g., `<REPO_NAME>`) and push this code.
2. In GitHub repo: **Settings → Pages**
   - Build and deployment: **GitHub Actions**
3. Push to `main` branch → site auto-deploys.

## Backup
- Git already stores all history. Clone anywhere:
```bash
git clone https://github.com/<YOUR_GITHUB_USERNAME>/<REPO_NAME>.git
```
- Build static HTML:
```bash
mkdocs build
```
Output: `site/` (can be zipped and moved anywhere)

## Migrate
- Move to a new repo/domain: update `site_url` in `mkdocs.yml`.
- Custom domain: set GitHub Pages Custom domain and add DNS CNAME.

---
Generated on: 2026-01-02
