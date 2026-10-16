# Space Grotesk — self-hosted heading font

Original project: https://github.com/floriankarsten/space-grotesk

Retrieved 2026-10-16 at upstream commit `03507d024a01282884232081fc6011c09ff4e849`.

Unmodified source file: `fonts/woff2/SpaceGrotesk[wght].woff2` (49,256 bytes).
Local filename: `space-grotesk-wght.woff2`.
Git blob identity: `0c4d65824309f9107f096fb4421e14782cb3ec81`.
SHA256: `8e085aa438094f11487a836652edd5c054fa6a96f63fc7c282105ee3a4b08c07`.

License: SIL Open Font License 1.1, full upstream copyright and license in `OFL.txt`.
The accompanying license was retrieved at the same commit; Git blob
`cb512b9af44ff61e75e1aad387b7424cdfab36a3`.

The original variable WOFF2 supplies weights 500, 600 and 700 through a single
`@font-face` declaration in `assets/css/custom.css`, with `font-display: swap`.
It is used for semantic headings and the IFT BioLab title only.
No font conversion, subsetting, Node/npm, build plugin or external font request
is required. The font itself has not been modified or renamed internally.

To replace it, change `--ift-font-heading` to a different available/system family.
To provide another web font, replace the `@font-face` declaration and retain that
font's own source and licensing information. Remove this directory if no longer used.
