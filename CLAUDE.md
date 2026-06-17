# Academic CV – Melgris José Becerra Ruiz

Hugo-based academic CV site built with [HugoBlox Kit](https://hugoblox.com) (Academic CV template, Matcha theme).
Deployed automatically to **https://mjbecerra.github.io** via GitHub Actions on every push to `main`.

## Tech stack

| Layer | Tool | Version |
|-------|------|---------|
| Static site generator | Hugo Extended | 0.163.2 (minimum — see gotcha below) |
| Theme / UI framework | HugoBlox blox module | `20260527025321` (pinned in `go.mod`) |
| CSS | Tailwind CSS v4 via `@tailwindcss/cli` npm package | — |
| JS package manager | pnpm | v10+ |
| Deployment | GitHub Actions → `peaceiris/actions-gh-pages` → `gh-pages` branch | — |
| Hosting | GitHub Pages | `https://mjbecerra.github.io` |

## Before running Hugo locally

`node_modules` is gitignored. Always install before building:

```bash
pnpm install
hugo server        # dev server at http://localhost:1313
hugo --minify      # production build → public/
```

## Critical gotcha: Hugo version

The HugoBlox module (`go.mod`) requires **Hugo ≥ 0.163.x**. Using 0.162.0 or older causes a fatal `nil map` error in `build_links.html`. Both `hugoblox.yaml` and `.github/workflows/deploy.yml` are pinned to `0.163.2`.

## Project structure

```
config/_default/
  hugo.yaml          # baseURL, build settings
  params.yaml        # site identity, theme (Matcha), SEO description
  menus.yaml         # active nav: Bio · Papers · Experience · Projects

content/
  _index.md          # homepage sections (biography, featured papers, recent papers)
  experience.md      # experience, skills, awards, languages pages
  publications/      # 14 publications (one folder per paper)
  blog/              # template example posts (not Melgris's content — can be deleted)
  courses/           # template example (not used — removed from menu)
  projects/          # placeholder projects (update with real ones)
  events/            # placeholder event (not used — removed from menu)

data/authors/me.yaml # author profile: bio, education, experience, skills, languages, links

assets/media/
  authors/me.png     # profile photo placeholder (replace with real photo)

static/
  favicon.svg        # SVG favicon (forest-green "MB" initials)
  site.webmanifest   # PWA manifest
  uploads/resume.pdf # CV PDF for the "Download CV" button

layouts/_partials/hooks/head-end/
  seo.html           # Person JSON-LD schema, meta keywords, manifest link
  github-button.html # GitHub star button (template default)
```

## Author data

All personal info lives in `data/authors/me.yaml`. Edit this file to update:
- Bio, role, affiliations
- Links (email, LinkedIn, GitHub, Google Scholar, ORCID, Scopus)
- Education and work experience
- Skills, languages, awards

## Publications

Each publication is a folder under `content/publications/<slug>/index.md`.
Schema: `publication_types` uses CSL standard (`article-journal`, `chapter`, `book`, `dataset`, `report`).
DOIs go under `hugoblox.ids.doi` (top-level `doi:` is deprecated and causes build warnings).

```yaml
# Example
title: "Title of the paper"
authors: [me, "Co-Author Name"]
date: "2024-06-29T00:00:00Z"
publication_types: ["article-journal"]
publication:
  name: "Journal Name"
hugoblox:
  ids:
    doi: "10.xxxx/xxxxx"
peer_reviewed: true
open_access: true
featured: false   # set true for top publications (appear in grid on homepage)
tags: ["tag1", "tag2"]
links:
  - type: pdf
    url: "https://doi.org/..."
```

## Deploy

Push to `main` → GitHub Actions builds with Hugo + pnpm → pushes `public/` to `gh-pages` branch → GitHub Pages serves the site.

Workflow file: `.github/workflows/deploy.yml`
GitHub Pages config: repo Settings → Pages → Deploy from branch `gh-pages`

## Pending tasks

- [ ] Replace `assets/media/authors/me.png` with the real profile photo
- [ ] Add `static/uploads/resume.pdf` (real PDF; current file is a placeholder)
- [ ] Clean up or replace placeholder blog posts in `content/blog/`
- [ ] Clean up placeholder projects in `content/projects/` (pandas, pytorch, scikit)
- [ ] Add real events/talks to `content/events/` if needed (and re-enable in menu)
