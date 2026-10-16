# IFT BioLab

Protocols, equipment, methods and experimental projects.

**Maintainers normally edit only `content/`.** Markdown and page-local images are committed to Git, built with Hugo and published by GitHub Actions to GitHub Pages. No Hugo knowledge or local installation is needed to edit content on github.com. See [Start Here](content/start-here/_index.md) for the editing steps and [ADMIN.md](ADMIN.md) for publication and recovery.

**This repository and its future site are public.** Do not commit passwords, personal data, confidential partner information, unpublished proprietary protocols or restricted research data. Equipment and Materials contain supplied inventory records with explicit status labels. Other example records remain incomplete placeholders, not usable procedures or verified standards.

## Content map

| Path | Purpose |
|---|---|
| `content/_index.md` | Homepage introduction and access to every section |
| `content/start-here/_index.md` | Reader and editor guide |
| `content/protocols/` | Protocol records with visible status |
| `content/equipment/` | Confirmed equipment purchase records |
| `content/materials/` | Confirmed materials/consumables and separately labelled reported chemicals |
| `admin/` | Inventory maintenance notes and non-public-facing to-verify checklist (repository remains public) |
| `content/methods/` | Nine method prompts to complete and review |
| `content/courses/` | Course structure and teaching resources |
| `content/projects/` | Manual index and project overviews |
| `content/students/_index.md` | Manual student index; deployment demo only for now |
| `templates/` | Unpublished Markdown structures for copying into `content/` |

To add a page on GitHub, copy an example bundle into `content/<section>/<new-slug>/index.md`, replace its front matter and all placeholders, upload images to the same folder and update relative links. The published Start Here guide explains the workflow. Interface labels remain English; prose may be English or French. Students' own documentation stays in their separate repositories: **Project / Experiments / Notebook**. No content is imported automatically.

## Tested versions

- Hugo standard **0.168.0**; Go **1.27.2**.
- Relearn **9.2.1**, module commit `657eb0c78b6b`, locked as `v0.0.0-20261011111622-657eb0c78b6b` with `go.sum` checksums.
- Official actions pinned to full commit hashes in `.github/workflows/pages.yml`: checkout **7.0.1**, setup-go **7.0.0**, configure-pages **6.0.0**, upload-pages-artifact **5.0.0**, deploy-pages **5.0.1**.
- Validation: actionlint **1.7.12**; Python 3.11+ standard library for the parent workspace's local checks. These are not student dependencies.

Hugo exceeds [Relearn's documented minimum 0.166.0](https://mcshelby.github.io/hugo-theme-relearn/introduction/quickstart/); its standard edition is sufficient. This reuses the approved student toolchain. See [Hugo Modules](https://gohugo.io/hugo-modules/use-modules/), [Relearn release](https://github.com/McShelby/hugo-theme-relearn/releases/tag/9.2.1), and [official Pages workflow guidance](https://gohugo.io/host-and-deploy/deploy-to-github-pages/). No Node, npm, custom JavaScript, custom layout or theme fork is used.

## Local preview

With those Hugo/Go versions and Git installed, run from this repository:

```powershell
hugo mod graph
hugo mod verify
hugo --gc --minify --panicOnWarning
hugo server --bind 127.0.0.1 --baseURL http://127.0.0.1:1320/ --port 1320 --disableFastRender
```

Open <http://127.0.0.1:1320/>. Stop with Ctrl+C. In the supplied handoff workspace, `. ../../tools/env.ps1` supplies its local tools before these commands. Production builds default to `https://ift-biolab.github.io/`; a fresh destination plus `--baseURL https://example.github.io/biolab-preview/` can test project-path compatibility without changing configuration.

Generated `public/`, `resources/`, `.hugo_build.lock`, `.cache/`, `.local-tools/` and `.validation/` are ignored. Never publish the parent workspace or tool caches.

## Visual system

`assets/css/custom.css` is the approved student stylesheet copied without changes, loaded by Relearn's native customization mechanism. It uses neutral backgrounds, restrained teal, semantic headings, visible focus outlines, responsive images and scrolling tables. No institutional logo is supplied. Space Grotesk headings are self-hosted under SIL OFL 1.1; license and immutable provenance are in `static/fonts/space-grotesk/`. Relearn's body typeface remains unchanged.

Administrators can adjust these variables at the top of that one CSS file:

| Variable | Initial value / role |
|---|---|
| `--biolab-accent` | `#32665f`, links and focus |
| `--biolab-background` | `#fbfaf7`, page background |
| `--biolab-text` | `#252b28`, text |
| `--biolab-muted` | `#5b655f`, secondary text |
| `--biolab-surface` | `#f0f1eb`, sidebar and callout background |
| `--biolab-border` | `#d8ddd5`, separators |
| `--biolab-page-width` | `58rem` |
| `--ift-font-body` | Relearn's resolved reading font (Roboto Flex with system fallbacks) |
| `--ift-font-heading` | Space Grotesk, system-ui, Segoe UI, Arial, sans-serif |
| `--ift-font-mono` | Relearn's resolved monospace font |

Change `--ift-font-heading` to replace the display family; for another hosted font replace the single `@font-face` and retain its license. Body and mono variables alias the theme's resolved fonts; do not map `--MAIN-font` back to the body alias, which creates a cycle. Display typography is restricted to headings and the IFT BioLab title. Removing this CSS restores standard Relearn presentation.

Future logo: use Relearn's auto-detected `assets/images/logo.svg`, or set `logo = { src = '/images/approved-logo.svg' }` inside `[params]` for an approved asset. Optional favicon: `assets/images/favicon.png`, `.svg` or `.ico`. These are theme asset paths resolved by Relearn; retest root and subpaths after branding changes. Site title, fallback URL and edit link are in `hugo.toml`. No CNAME or institutional domain integration is configured.

See [CONTENT_CHECKLIST.md](CONTENT_CHECKLIST.md) for what the BioLab team still needs to supply. Future repository: `ift-biolab/ift-biolab.github.io`. Local implementation only until publication is approved.
