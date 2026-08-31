# Academic website — Lukas Basler

Quarto site, deployed to GitHub Pages.

## 1. Before going live

All text placeholders are filled in. Two things remain:

**Files to add:**

- `images/profile.jpg` — portrait, square crop, roughly 600×600 px
- `images/favicon.png` — 512×512 px; generate at <https://favicon.io>
- `files/CV_Basler.pdf` — the public version of your CV

**Content to check:**

- `imprint.qmd` — read the comment at the top of the file before publishing

## 2. Preview locally

Requires [Quarto](https://quarto.org/docs/get-started/).

```bash
quarto preview
```

## 3. Publish

1. Create a GitHub repository named exactly `lukas-basler.github.io` (public, no README, no .gitignore, no licence — an empty repository).
2. Push this directory to its `main` branch.
3. In the repository, go to **Settings → Pages** and set the source to **Deploy from a branch → `gh-pages` → `/ (root)`**. The `gh-pages` branch is created by the first workflow run, so do this after the first push completes.

Every subsequent push to `main` re-renders and redeploys the site automatically via `.github/workflows/publish.yml`.

## 4. Publications (later)

When there are papers to list, export the `.bib` from Overleaf into `publications.bib`, add a `publications.qmd` with `bibliography: publications.bib` and a `csl:` style file, and reference the entries with `nocite`. That keeps the website and the manuscripts on one source of truth — no duplicate maintenance.
