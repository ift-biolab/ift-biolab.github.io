# IFT BioLab visual identity

The public name is **IFT BioLab**. The identity uses a native branching SVG and separate HTML text. It adds no scientific content, site sections, JavaScript or remote assets. Student repositories are independent and have not been changed.

## Palette and typography

The single existing stylesheet, `assets/css/custom.css`, defines:

```css
--ift-charcoal: #1F2A26;
--ift-off-white: #F6F4EC;
--ift-algae: #6B7F63;
--ift-sage: #C9D4B8;
--ift-amber: #D8933A;

--ift-font-body: var(--INTERNAL-MAIN-font, "Roboto Flex", Helvetica, Arial, sans-serif);
--ift-font-heading: "Space Grotesk", system-ui, "Segoe UI", Arial, sans-serif;
--ift-font-mono: var(--INTERNAL-CODE-font, Consolas, menlo, monospace);
--ift-logo-width: 3.5rem;
--ift-home-mark-width: clamp(5rem, 12vw, 8rem);
```

Existing `--biolab-*` aliases map this palette into the editorial styling and supported Relearn color variables. Muted text, secondary surfaces and borders use documented solid color mixes of approved colors; no gradients. The body retains Relearn's resolved reading face. Headings and identity retain the already self-hosted Space Grotesk variable font (weights 500–700), with its existing OFL license. No font was added or downloaded.

Measured WCAG contrast ratios:

| Pair | Ratio | Use |
|---|---|---|
| Charcoal / off-white | 13.45:1 | Body, links, headings, callout text |
| Charcoal / pale sage | 9.59:1 | Table headers |
| Off-white / charcoal | 13.45:1 | Available inverse pairing |
| Algae / off-white | 3.94:1 | Graphic details, not small text |
| Amber / off-white | 2.34:1 | Decorative accent node only, outlined in charcoal |

Links are charcoal and underlined in article content; hover increases underline thickness. Keyboard focus uses a 3 px charcoal outline with 4 px offset. Algae marks active navigation. Amber appears only in one logo endpoint, not as the universal link/warning color. Relearn warning/caution/note colors remain on callout borders/icons; labels/body use charcoal on off-white. This avoids the theme's default white-on-warning-red label ratio of 4.26:1 without removing semantic labels or replacing all statuses with amber.

## Assets and placement

| Asset | Purpose |
|---|---|
| `static/images/shared/ift-biolab-mark.svg` | Main palette mark, sidebar and home title |
| `static/images/shared/ift-biolab-mark-mono-dark.svg` | Same geometry, charcoal, for light surfaces |
| `static/images/shared/ift-biolab-mark-mono-light.svg` | Same geometry, off-white, for dark surfaces |
| `static/images/favicon.svg` | Same paths with slightly stronger small-size strokes; automatic OS light/dark adaptation |

The main mark has one origin and four curved terminal directions, five circles total. Paths/circles remain editable; no raster, text outlines, gradients, scripts, external references or dependencies. The SVG has a transparent background. The sidebar image is decorative (`alt=""`) beside the real HTML site title, so the home link has one accessible name. The homepage's existing semantic H1 remains its HTML wordmark; a decorative CSS pseudo-element places the same mark beside it. No duplicate H1 or marketing hero is introduced.

Change the logo path in `hugo.toml` under `[params.logo]`. If replacing the home mark too, update the one `background` URL in the home-only rule in `custom.css`. CSS asset URLs resolve relative to the generated stylesheet and are tested with a Pages subpath. Change the title using the existing `title` setting. SVG colors are explicit attributes for reliable standalone reuse; update those attributes when intentionally revising the identity.

## Relearn customization boundary

Hugo **0.168.0**, Relearn **9.2.1** and their existing module/workflow pins are unchanged. No files inside the cached theme module are modified.

- Extend the existing native `assets/css/custom.css` extension; there is no competing stylesheet.
- `[params.logo]` records the approved mark path and sidebar row layout.
- The local `layouts/partials/logo.html` override is five lines. The native image helper rejected this required `static/` asset as “not a resource”; the override therefore renders a normal image while retaining Relearn's home permalink helper and familiar logo classes. It uses Hugo `relURL` to preserve subpaths. No other layout is overridden.
- Native favicon auto-detection finds `static/images/favicon.svg`; no favicon template override is needed.
- The homepage changes only the existing lead paragraph's CSS classes (`.lead .ift-home`); all editorial text, navigation, content paths and page architecture are unchanged.

Official customization references: [logo/title/favicon](https://mcshelby.github.io/hugo-theme-relearn/configuration/branding/logo/index.html), [custom CSS extension](https://mcshelby.github.io/hugo-theme-relearn/configuration/customization/extending/index.html).

## Local reference and reuse

The supplied reference was found at `_media-inbox/ift-biolab-brand-reference.png` (directly inside the inbox). It was viewed, not moved or edited. The inbox stays ignored and is not published. Only its visual proportions and approved palette inform the SVG; none of the raster artwork or reference text is embedded.

The same token block, assets and tiny logo override can later be copied into the student template after approval. There is no network dependency on the main site. No student template, demo or student repository is changed in this task.

To remove this identity later, restore the previous `custom.css`, remove the `[params.logo]` block, local logo partial, SVG files and `.ift-home` class. Scientific Markdown and page bundles require no redesign.

## Review and validation

The actual repository is previewed at **http://127.0.0.1:1340/**. The already running server was reused. Its failed intermediate logo rebuild was cleared by reloading the corrected config; final preview and production build use exactly the same source files. No parallel source site exists.

Screenshots, responsive measurements, build/link checks and exact command log are kept in ignored `.validation/branding-20261017/`. Wide/narrow desktop, tablet and mobile widths are **1440 / 1100 / 820 / 390 px**. The homepage, ONDA page and existing project image/caption are checked. Mobile menu/search/keyboard focus remain supported. Equipment currently has no approved local machine photographs; the excluded supplier JPEG remains untouched and unpublished. Existing page-bundle image behavior is tested with the unchanged project SVG.

Only local source work is authorised. No staging, commit, push or GitHub changes are part of this identity review.
