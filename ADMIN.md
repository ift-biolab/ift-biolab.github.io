# Main-site administrator runbook

## Visual identity

See [BRANDING.md](BRANDING.md) for the IFT BioLab palette, editable SVG assets, typography, contrast choices and the small local Relearn customization. Identity changes require local visual review before publication.

The site is maintained by administrators or designated maintainers in the existing **ift-biolab** organization. Keep student write access limited to their own repositories; do not grant main-site access by default. The main site and its public content are separate from student sites. No custom secrets, backend or content aggregation are used.

## Content maintenance

Use `content/` for all scientific and operational pages. Copy an example bundle or an unpublished file from `templates/` into a new `content/<section>/<slug>/index.md`. Replace every placeholder and update its Markdown links. Keep images beside their page. Protocol status and its visible warning must agree. Do not mark a protocol Validated without the team's review process and supporting record. Last-updated / last-tested values are explicit Markdown fields, not generated Git dates.

Projects and Students are ordinary Markdown indexes, updated manually. Publish only confirmed public information. Student sites retain independent histories and content; links do not import or duplicate their pages. Template changes do not propagate to existing repositories. The shared visual files are independent copies: test updates in the demo and manually patch affected repositories when needed. No batch updater is included.

## First publication — instructions only, after approval

The organization already exists. Create **only** an empty **public** repository named `ift-biolab.github.io` under `ift-biolab`. Do not initialize it with a README, license or `.gitignore`. The exact name makes it the organization root site, <https://ift-biolab.github.io/>. Do not change either student repository.

Use Git with browser / Git Credential Manager authentication. Never put a token in a command, file or remote URL. The commands below have **not** been executed. From this handoff workspace, using Git on PATH:

```powershell
Set-Location 'D:\DVIC\these\plateformeIFT biolab\ift-biolab-agent-handoff\repos\main-site'
git init -b main
git config user.name "Vivien Roussel"
git config user.email "7760193+vivi3n@users.noreply.github.com"
git config --local --get user.name
git config --local --get user.email
git remote add origin https://github.com/ift-biolab/ift-biolab.github.io.git
git remote -v
git check-ignore --no-index .local-tools/probe .validation/probe public/probe resources/probe .hugo_build.lock
git add .
git diff --cached --name-only
git diff --cached --check
git status --short
```

Before continuing, inspect the staged list: only the main site's source files should appear. No `.local-tools`, `.validation`, `public`, `resources`, `.cache`, build lock, credentials or parent/student files may be staged. Confirm both remote URLs are exactly `https://github.com/ift-biolab/ift-biolab.github.io.git`. If Git is not on PATH, invoke the installed Git executable by its full path instead. Do not change global configuration.

After that review and explicit publication approval:

```powershell
git commit -m "Add IFT BioLab main documentation site"
git push -u origin main
```

If authentication is required, complete it through the browser or Git Credential Manager. Do not request or paste a personal access token. If the empty repository has acquired remote commits, stop and inspect them instead of force-pushing.

## Enable GitHub Pages — manual steps, after approval

1. Open **ift-biolab/ift-biolab.github.io → Settings → Pages** (not Settings → Actions → General).
2. Under **Build and deployment → Source**, select **GitHub Actions**. Leave custom domain empty. Do not choose a branch-based Pages build.
3. Ensure organization/repository policy permits the official pinned actions in `.github/workflows/pages.yml`. Keep default workflow permissions read-only; the deploy job explicitly requests `pages: write` and `id-token: write`. No PAT or custom repository secret is required.
4. Open **Actions → Build and deploy Pages → Run workflow**, choose **main**. An initial push before Pages enablement may have failed; enable Pages and run again.
5. If the `github-pages` environment has deployment protection, its designated reviewer must approve. Confirm it permits `main`. Do not bypass organization policy.
6. Wait for **both build and deploy** to be green. Open the environment's deployment URL; it must be <https://ift-biolab.github.io/>.
7. Test all seven sections, search for `sample naming`, the placeholder project's image and the demo student link. Inspect an Edit link: it must point to this repository's `main/content/` path.
8. Edit a neutral Markdown sentence, commit, wait for green deployment and verify the published change. This live deployment test requires GitHub and remains pending until publication is approved.

The workflow derives the Pages base URL, verifies the pinned Hugo download checksum, verifies module checksums, builds with warnings treated as errors and deploys the artifact through the `github-pages` environment. Root and project-subpath builds use the same source structure.

## Local build / validation

See README for Hugo/Go versions and preview commands. From the parent handoff workspace:

```powershell
. ./tools/env.ps1
& 'C:/Users/Vivie/.cache/codex-runtimes/codex-primary-runtime/dependencies/python/python.exe' tools/check-phase2.py
```

This standard-library check writes fresh build outputs and exact commands under ignored `.validation/phase2-*`, validates root/subpath links and images, lints Actions, checks visual-source parity, and simulates Markdown/image edits on an isolated copy. Browser layout and search checks are recorded separately in the Phase 2 report. The validation script belongs to the handoff, not the deployable main-site repository.

## Recover a failed change

1. Open **Actions**, select the failed run and note its commit ID and failing step. Compare with the last successful deployment. Hugo normally reports the affected Markdown filename and line.
2. Open that file and **History**. Check malformed front matter, missing images, broken relative links, accidental technical changes or deleted section indexes. Correct the Markdown with the GitHub editor, preview and commit. No student account is required.
3. To undo a merged pull request, use its **Revert** action, review and merge the reversal PR. For direct commits, GitHub has no universal Revert button: inspect each file at the previous good revision and restore that content in a new commit, removing any newly added broken files.
4. To restore a deleted file, find the deletion commit and browse its parent revision. Recreate the original path with **Add file → Create new file**, copying the old content. Download and re-upload deleted images from that revision if needed.
5. Command-line alternative, only after reviewing a clean checkout: `git pull --ff-only`, `git show <bad-commit>`, `git revert <bad-commit>`, then an approved `git push`. Ask an experienced maintainer about merge commits rather than guessing the mainline parent. Avoid force pushes.
6. Confirm a green **build and deployment**, reload the published affected page and verify its images/navigation. A failed build leaves the last successfully deployed site live.

Keep version pins consistent across README, go.mod and workflow. Test before changing them; do not follow a moving theme branch. Relearn's custom CSS extension and native Markdown features avoid a theme fork. This repository has no selected project-wide license; the supplied font retains its own OFL license and the theme its upstream license.
