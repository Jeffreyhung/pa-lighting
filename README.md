# 聲光技術筆記 · Sound & Lighting Notes

Technical notes on live sound (PA) and stage lighting, in 中文 and English, built with
[MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and published on GitHub Pages.
The language switcher in the header keeps you on the same page when you change language.

## Publish on GitHub Pages

1. Create a new repository on GitHub and push this folder to its `main` branch.
2. In the repository, open **Settings → Pages** and set **Source** to **GitHub Actions**.
3. The included workflow (`.github/workflows/pages.yml`) builds and deploys on every push to `main`.
   The site appears at `https://<your-user>.github.io/<your-repo>/` (中文) and `…/en/` (English).

Optional: set `site_url` and `repo_url` at the top of `mkdocs.yml` once you know the address.

## Preview locally

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve          # http://127.0.0.1:8000
```

## Layout

```
docs/
  zh/            中文 pages (default language, served at /)
  en/            English pages (served at /en/)
  assets/img/    all figures, shared by both languages
                 name.png     = original figure
                 name-en.png  = English version of a figure
mkdocs.yml       site config and navigation
requirements.txt pinned build dependencies
```

Each page exists at the same path in `docs/zh/` and `docs/en/`; that is what lets the
language switcher jump between translations. When you add a page, add it in both folders
under the same file name and list it once in `nav:` in `mkdocs.yml`.

## Security notes

- The site is fully static and makes no third-party requests: fonts are system fonts
  (`font: false`) and search runs in the browser from a local index.
- Build dependencies are pinned in `requirements.txt`; GitHub Actions are pinned to commit SHAs
  and the workflow uses least-privilege permissions. Update the pins deliberately.
