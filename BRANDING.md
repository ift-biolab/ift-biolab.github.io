# IFT BioLab final branding assets

The public name remains **IFT BioLab**. Final supplied PNGs are used exactly as received; no image is redrawn, traced, cropped, recolored, recompressed or converted. Existing typography and approved palette remain unchanged.

## Source and byte-identical copies

The supplied files were found directly in `_media-inbox/`, rather than its proposed `branding/` subdirectory. Originals remain there untouched and ignored.

| Original | Public asset | Dimensions |
|---|---|---|
| `_media-inbox/ift-biolab-logo-horizontal.png` | `static/images/shared/ift-biolab-logo-horizontal.png` | 1405 × 350 px |
| `_media-inbox/ift-biolab-mark.png` | `static/images/shared/ift-biolab-mark.png` | 419 × 350 px |

SHA-256 is checked between originals, public copies and clean build output. No new PNG derivative, thumbnail or favicon conversion is generated. Any background or embedded text is preserved as part of the supplied artwork. The user explicitly authorised the horizontal image's existing embedded phrase after reviewing the conflict with the earlier no-slogan instruction. No additional slogan or branding text is added.

## Responsive placement

- Desktop/tablet at 48rem and above: the final horizontal PNG is the sidebar identity and homepage identity.
- Below 48rem: `picture` selects the compact PNG, with the existing HTML name **IFT BioLab** beside it. Mobile uses no separate slogan.
- Favicon: the local favicon partial links directly to the compact PNG, using its original bytes and dimensions.
- The homepage keeps one semantic H1. Its HTML title remains available to assistive technology; on desktop it is visually hidden because the supplied horizontal image already contains the wordmark. On mobile the HTML title is visible beside the compact mark. The CSS clipping rule applies only to the duplicate HTML text, never an image.
- Both images use proportional CSS sizing with `height: auto`, no filters, fixed-ratio boxes or cropping. Original backgrounds and whitespace are retained.

The earlier SVG designs remain in source history and on disk but are no longer referenced by the active logo, homepage or favicon. They are not altered in this task.

## Configuration and CSS

`hugo.toml` contains `[params.logo]` paths for `src` (horizontal PNG) and `compactSrc` (compact PNG). Both go through Hugo `relURL` in the local partials, preserving GitHub Pages subpaths.

The existing `assets/css/custom.css` is the only custom stylesheet. Palette:

```css
--ift-charcoal: #1F2A26;
--ift-off-white: #F6F4EC;
--ift-algae: #6B7F63;
--ift-sage: #C9D4B8;
--ift-amber: #D8933A;
```

Sizing variables:

```css
--ift-logo-width: 14rem;
--ift-home-logo-width: 40rem;
--ift-home-mark-width: clamp(5rem, 12vw, 8rem);
```

Below 48rem the sidebar compact mark is 3.5rem wide. Existing Space Grotesk headings/identity and Relearn body/mono fonts are retained. No new font, remote dependency or JavaScript is introduced.

## Theme boundary

Hugo 0.168.0 / Relearn 9.2.1 and existing dependency/workflow pins stay unchanged. No theme/module files are edited.

Local documented Relearn hooks:

- `layouts/partials/logo.html`: responsive picture inside the existing sidebar home link, with one accessible name.
- `layouts/partials/heading.html`: homepage-only responsive identity; other pages use the same native title helper and H1 markup as before.
- `layouts/partials/favicon.html`: original compact PNG favicon; overrides detection of the older SVG.

No content architecture, navigation, scientific Markdown or student repository changes. Homepage copy is untouched. The actual local repository is the source of both preview and production build; there is no parallel source site.

## Local review

Preview: **http://127.0.0.1:1340/**. Build logs, original/copy/output hashes, screenshots, exact commands and responsive checks are stored in ignored `.validation/final-brand-assets-20261017/`.

Do not commit, push or change GitHub until the user separately approves publication of this integration.
