# Equipment source review — 17 October 2026

> **Presence-status update:** the supervisor has subsequently checked the inventory. See [Inventory confirmations](INVENTORY_CONFIRMATIONS.md) for the current confirmed / to-verify split. The historical status conclusions below describe the earlier review; source discrepancies remain relevant.

Local review only. No commit, push or remote setting change. Only seven existing Equipment pages and their index are changed; these administrator notes are outside Hugo content. Global styling, configuration, navigation, slugs, other sections and student repositories are unchanged. Administrator notes are not website content but are **not confidential** in a public source repository.

Ownership evidence is the existing local inventory / purchase source **PVW2602335**, not a supplier's stock indicator. Confirmed purchase is not a live availability, training or readiness statement. All seven records retain `confirmed`; all thirteen historical records below remain `to-verify`.

## A. Confirmed equipment

Paths are relative to the repository. Links in each actual page identify every product source and available document. No external product image was downloaded.

| Page | Manufacturer / model identity | Sources used | Local image | Page status |
|---|---|---|---|---|
| `content/equipment/onda-v-10-plus/index.md` | ONDA V-10 PLUS; Labbox Labware CE declaring entity, OEM not identified | Local inventory; Labbox product page; PDS-1268 (31 March 2026); MANU_1268 (undated); CE-1268 (24 September 2024) | Supplier image exists, explicitly excluded by user; no BioLab photo | confirmed; completed with discrepancies |
| `content/equipment/metria-plus-analytical-balance/index.md` | METRIA PLUS, 220 g, internal calibration; exact BAMP-220-001 | Local inventory; Labbox page; PDS-1744 (28 August 2025); MANU_EN_1744 (undated) | None | confirmed; completed with discrepancies |
| `content/equipment/lbx-mc15k-mini-centrifuge/index.md` | LBX Instruments MC15K, MCEN-15K-001 | Local inventory; Labbox page; PDS-455 (10 September 2025); MANU_455 (undated) | None | confirmed; completed with discrepancies |
| `content/equipment/volt-h-compact-electrophoresis/index.md` | VOLT H-Compact, ELFH-50V-001 | Local inventory; Labbox Spain exact product page; PDS-1937 (3 February 2026) | None | confirmed; completed; manual missing |
| `content/equipment/blue-light-led-transilluminator/index.md` | LBX Instruments supplier brand; model identified by TRLM-BLB-001 and 210 × 120 mm area | Local inventory; Labbox Export exact product page; MANU_EN_1935 (undated) | None | confirmed; completed; datasheet retrieval gap |
| `content/equipment/proclean-3010-microwave/index.md` | Cecotec ProClean 3010 / 01522; supplier MCRW-20L-001 | Local inventory; Cecotec page and manufacturer family manual (undated); Labbox page; PDS-1399 (25 September 2025) | None | confirmed purchase; manufacturer excludes laboratory use |
| `content/equipment/glass-laboratory-thermometers/index.md` | METRIA supplier brand; THER-050-010, −10 to +50 °C, 300 mm, ten units | Local inventory; Labbox page; PDS-561 (7 April 2026) | None | confirmed; accuracy terminology unresolved |

For supplier brands, the brand is identified without claiming a separate OEM factory. No bundled accessory is treated as physically checked. The existing ONDA `build.publishResources: false` is retained so its unused supplier JPEG is not copied automatically into production output. That JPEG is preserved and untracked; it is not private or safe to stage simply because it is omitted from the website.

## B. Historical equipment — all to-verify

The existing `admin/inventory-to-verify.md` is preserved. No historical item has been added to public equipment navigation/search. Two useful identification drafts are in `admin/equipment-drafts/`; all other items remain checklist entries, avoiding duplicate or speculative equipment pages.

| Item | Identity and sources | Missing information | Draft |
|---|---|---|---|
| Magnetic stirrer | Historical [ASIN B07GR772K7](https://www.amazon.fr/dp/B07GR772K7/); listing inaccessible; no reliable exact identity obtained | Manufacturer, model, reference, presence, matching manual | No; checklist only |
| Overhead stirrer | Historical [ASIN B079S28RJ2](https://www.amazon.fr/dp/B079S28RJ2/); listing inaccessible; no reliable exact identity obtained | Manufacturer, model, reference, presence, matching manual | No; checklist only |
| Large laboratory autoclave | No exact product reference in local files or supplied history | **Exact model identification required.** Presence and applicable documentation also unresolved | No |
| Motic BA-310 microscope | Candidate BA310 LED trinocular from supplied history; [official Motic page](https://www.motic.com/As_ls_UM_BA310/product_473.html); historical Labbox URL inaccessible | Model plate, presence, head, illumination, objectives/accessories; matched manual; manufacturer head-description conflict | Yes: `equipment-drafts/motic-ba310.md` |
| Microscope camera | No exact model/reference found locally | Identity, presence and manufacturer documentation | No |
| Conductivity equipment | Candidate DFRobot K=1 / DFR0300: [historical Go Tronic listing](https://www.gotronic.fr/art-sonde-de-conductivite-k1-dfr0300-27863.htm), [manufacturer wiki](https://wiki.dfrobot.com/dfr0300) | Probe, board revision, controller and complete measurement assembly must each be identified and checked | Yes: `equipment-drafts/dfrobot-conductivity.md` |
| Laboratory support stand | Historical [ASIN B08P6Z5L68](https://www.amazon.fr/dp/B08P6Z5L68/); listing inaccessible | Exact accessory/reference and presence | No; simple checklist entry |
| Paper drying rack | [Historical supplier family page](https://www.geant-beaux-arts.fr/sechoir-a-papier-en-metal.html) found; exact purchased variant unidentified | Reference, variant, dimensions and presence; no dimensions inferred | No; support checklist entry |
| Laboratory wall drying rack | [Current Labbox family page](https://labbox.fr/produit/egouttoir-mural-pour-materiel-de-laboratoire/) found; historical fra.labbox.com URL inaccessible | Purchased variant/reference and presence; no family specifications assigned | No; accessory checklist entry |
| UV insect lamp | Historical [Beslands ASIN B09WY68FY6](https://www.amazon.fr/Beslands-Lampe-Anti-Moustique-El%C3%A9ctrique-Moustiques/dp/B09WY68FY6/); inaccessible | Exact model/reference, presence and instructions; Beslands is only a candidate from the URL | No; insect-control support only, not UV analysis/sterilisation/curing equipment |
| Large beakers | Local historical checklist, no product reference | Sizes, quantities, identity and presence | No; glassware/accessories |
| PU / PVC / Plexiglas trays | Local historical checklist, no exact reference | Material, sizes, quantities and presence | No; accessories |
| Laboratory cleaning equipment | Local historical facility/support checklist | Actual tools, quantity and presence | No; not major Equipment |

Miracloth, immersion oil, mannitol, bacitracin, peptone, agar, chemicals and consumables remain outside Equipment. Their existing Materials/checklist records are unchanged.

## C. Source conflicts and interpretation

Dates below are document revision dates when supplied, not download dates. Undated means no revision date was identified. Sources were accessed 17 October 2026. A dated supplier datasheet is used where no manufacturer technical datasheet was found. Disagreements are visible on the relevant page; no averages were calculated.

### ONDA V-10 PLUS

Sources: [PDS-1268, 31 March 2026](https://labbox.fr/wp-content/uploads/FT/PDS-1268.pdf), [undated manual](https://labbox.fr/wp-content/uploads/Manuales/MANU_1268.pdf), [current supplier page](https://labbox.fr/produit/spectrophotometre-visible-modele-onda-v-10-plus/).

| Parameter | Dated datasheet | Undated manual | Handling |
|---|---|---|---|
| Wavelength repeatability | ±1 nm | 0.8 nm | Datasheet in public table |
| Dimensions | 440 × 360 × 180 mm | 490 × 360 × 210; units not printed in that row | Datasheet; no invented axis order |
| Instrument mass | 8 kg | 14 kg | Datasheet; its separate 10 kg logistics figure is not instrument mass |
| Supply | 85–265 V, 50–60 Hz | AC 110/220 V, 50/60 Hz; installation narrows to 110±11 V / 60±1 Hz or 220±22 V / 50±1 Hz | Datasheet; applicability/nameplate check required |

Manual internally: installation 16–35 °C / 45–80% humidity versus specification table 15–35 °C / 15–70% RH. No operating environment chosen. English introduction says UV-20 and utility instructions mention D2 despite V-10 PLUS cover; no UV capability inferred. Manual warranty one year versus current product/datasheet two years; commercial warranty not published as a BioLab entitlement. CE declaration is for SPTR-V01 family; it identifies Labbox Labware as declaring entity, not an OEM factory or local calibration.

### METRIA PLUS BAMP-220-001

Sources: [PDS-1744, 28 August 2025](https://labbox.fr/wp-content/uploads/FT/PDS-1744.pdf), [undated English manual](https://labbox.fr/wp-content/uploads/Manuales/MANU_EN_1744.pdf).

- Dimensions: datasheet 350 × 212 × 322 mm; manual 310 × 212 × 350 mm. Datasheet used.
- Supply: datasheet 110–230 V, 50–60 Hz; manual table AC110–240 V; troubleshooting text 110–220 V. Datasheet used; no merged range.
- Interfaces: datasheet USB + RS232C; manual describes RS232, omitting USB. This is a documentation omission, not proof USB is absent. Datasheet used.
- Manual net mass 5,500 g versus datasheet logistics mass 5.60 kg: different contexts; no net weight inferred from shipping data.
- Exact internal-calibration model is BAMP-220-001; BAMP-22E-001 is external calibration. Manual's calibration weight/glove packaging note applies to external-calibration models; generic supplier accessories are not proof of our internal-calibration unit's contents.

### LBX MC15K

Sources: [PDS-455, 10 September 2025](https://labbox.es/wp-content/uploads/FT/PDS-455.pdf), [undated manual](https://labbox.fr/wp-content/uploads/Manuales/MANU_455.pdf).

- Datasheet Spanish dimensions 140 × 250 × 245 mm versus English 140 × 255 × 245 mm. Same revision, no justified language preference: both remain explicitly unresolved on the public page.
- Manual specifies L255 × W245 × H140 mm. This is consistent with the English dimensions after reordering; no spurious extra axis-order conflict is asserted.
- Supply: datasheet 200–240 V / 50–60 Hz; manual 110–240 V / 50–60 Hz, 3 A. Dated datasheet used.
- Noise phrasing differs: Spanish “below 54 dB”, English “≤54 dB”. No noise boundary is published.
- Standard rotor MCEN-A05-001 is documented for 12 × 1.5/2.0 mL; 0.2/0.5 mL require additional adapters. No optional adapter ownership inferred.

### VOLT H-Compact

Sources: [PDS-1937, 3 February 2026](https://labbox.es/wp-content/uploads/FT/PDS-1937.pdf), [undated current supplier page](https://labbox.es/producto/sistema-todo-en-uno-para-electroforesis-horizontal-volt-h-compact/).

Datasheet tray sizes are abbreviated to 60, 65, 130 mm; page gives 130 × 135, 130 × 65, 60 × 65 mm. This is incomplete datasheet information, not a proved numerical contradiction. Complete formats are explicitly attributed to the product page. The 500 mL chamber capacity is not a chamber dimension; internal dimensions were not located. Integrated power supply belongs to this exact product, but accessories still require checking.

### Blue-light transilluminator

Sources: [current supplier page](https://labbox.eu/product/blue-light-led-transilluminator/), [undated English manual](https://labbox.eu/wp-content/uploads/Manuales/MANU_EN_1935.pdf).

Manual headings/part names say “UV” despite its 470 nm specification and the blue-light product identity. Treat it as blue-light equipment; no UV function inferred. Cleaning wording mentions ethanol >70% in one section and anhydrous ethanol elsewhere. No cleaning recipe is selected or reproduced. Supplier marketing claims about protective glasses or “non-toxic” dyes are not adopted as BioLab safety guidance. The 210 × 120 mm reference is distinguished from other viewing-area variants.

### Cecotec ProClean 3010

Sources: [manufacturer page, undated](https://www.storececotec.fr/fr/micro-ondes/proclean-3010), [manufacturer family manual, undated](https://cdn.cecotec.cloud/media/files/proclean-3010_user_manual_de.pdf), [supplier PDS-1399, 25 September 2025](https://labbox.fr/wp-content/uploads/FT/PDS-1399.pdf).

| Parameter | Supplier datasheet | Manufacturer page | Handling |
|---|---|---|---|
| External dimensions | 445 × 355 × 255 mm | 44 × 34.7 × 25.5 cm = 440 × 347 × 255 mm | Dated datasheet shown with both values disclosed; actual unit requires check |
| Internal dimensions | 285 × 277 × 175 mm | 27.8 × 29.2 × 17.4 cm = 278 × 292 × 174 mm | Same handling; no averaging |

No separate manufacturer technical datasheet was located; the product page is undated, so it cannot establish a more recent revision than the dated supplier PDS. Manufacturer manual is authoritative for intended use: explicitly domestic, not industrial/laboratory. Local purchase confirms ownership only. The page does not endorse laboratory use. 700 W is microwave output; 1,150 W is electrical consumption, not a conflicting output figure. Supplier logistics 11 kg is not established net weight.

### Glass thermometers THER-050-010

Sources: local purchase information and [PDS-561, 7 April 2026](https://labbox.fr/wp-content/uploads/FT/PDS-561.pdf).

Local record calls 0.5 °C accuracy; French/English supplier table calls ±0.5 °C resolution, German readability. These terms are not interchangeable. The public table preserves the supplier field label with an explicit unresolved-accuracy note. No calibration certificate inferred. Pack quantity ten is not current usable stock.

### Historical candidates

- Motic undated official BA310 LED Trinocular page calls its observation tube “Binocular head” while documenting trinocular light splitting. Physical configuration and matched manual required; no BA310E/digital/accessory specifications assigned to the BioLab.
- DFRobot current undated wiki (V2 board) gives 3.0–5.0 V and probe detection 0–20 mS/cm / recommended 1–15 mS/cm; undated historical Go Tronic page describes 5 V and 0–15 mS/cm. Different version/range context may explain this, but local revision is unknown. Kept in identification draft, no public specification claim.

## D. Missing documentation / unresolved evidence

| Equipment | Gap |
|---|---|
| ONDA | OEM identity; manual applicability conflicts; no internally validated BioLab protocol |
| METRIA PLUS | Separate OEM document set; supplier CE download could not be retrieved |
| MC15K | Separate OEM document set; supplier CE download could not be retrieved; dimension conflict unresolved |
| H-Compact | User manual not located; CE file could not be retrieved; internal chamber dimensions missing |
| Blue-light transilluminator | Advertised datasheet and CE file could not be retrieved; separate OEM documents not identified; manual terminology/cleaning conflicts |
| ProClean 3010 | Separate manufacturer technical datasheet and model-specific CE declaration not retrieved; dimension and laboratory-use applicability unresolved |
| Thermometers | Manual, separate OEM datasheet and calibration certificate not located; accuracy terminology unresolved |
| Motic candidate | Exact local variant, matched manual and conformity documentation unresolved |
| Conductivity candidate | Exact local hardware revision / assembled system unresolved; current and older documentation must not be merged |
| Remaining historical items | Reliable exact model/variant and physical confirmation required before matching documentation |

All seven public pages use the exact protocol-in-preparation blockquote. None has an internally validated equipment operating protocol; the generic placeholder protocol is not linked as operating guidance. No prices, chemical locations or new chemical procedures are included.

## E. Relevant directory tree

```text
content/equipment/
├── _index.md
├── blue-light-led-transilluminator/
│   ├── index.md
│   └── images/.gitkeep
├── example-equipment/
│   └── index.md                 (existing hidden placeholder, unchanged)
├── glass-laboratory-thermometers/
│   ├── index.md
│   └── images/.gitkeep
├── lbx-mc15k-mini-centrifuge/
│   ├── index.md
│   └── images/.gitkeep
├── metria-plus-analytical-balance/
│   ├── index.md
│   └── images/.gitkeep
├── onda-v-10-plus/
│   ├── index.md
│   └── images/
│       ├── .gitkeep
│       └── SPTR-V01-001.jpg      (pre-existing supplier image, excluded)
├── proclean-3010-microwave/
│   ├── index.md
│   └── images/.gitkeep
└── volt-h-compact-electrophoresis/
    ├── index.md
    └── images/.gitkeep

admin/equipment-drafts/
├── motic-ba310.md               (to-verify; not website content)
└── dfrobot-conductivity.md      (to-verify; not website content)
```

## F. Git and local validation

Build/test logs, command list, Git status/diff snapshots, before/after file hashes and generated validation output are stored in ignored `.validation/equipment-review-20261017/`. This directory contains only review evidence/output, not a parallel editable site; both Hugo production output and preview use the actual repository sources.

Pre-existing changes preserved: `.gitignore`, page-local image `.gitkeep` files in Equipment/Methods/Projects/Protocols, shared image placeholder and the excluded ONDA supplier JPEG. The ONDA page already had uncommitted documentation work; it is now standardised with the other six.

Task changes: eight Equipment Markdown files (index plus seven existing pages), this report, and two administrator identification drafts. No Git staging/commit/push or GitHub command is part of this task. Review the ignored `validation.txt`, `git-status.txt`, `git-diff-stat.txt` and `commands.md` for the actual check results.

Validation results: two clean Hugo 0.168.0 builds passed with `--gc --minify --panicOnWarning`, 50 pages each, root URL and `/review/` subpath. All generated local links/assets resolve. Each confirmed page renders one H1, nine standard sections, its exact reference and the required notice. Generated search contains all seven references, excludes the two administrator candidates, and no administrator directory is built. The supplier JPEG is absent from both outputs and unchanged byte for byte. File hashes confirm only the eight intended existing content files changed since the task baseline; other content, images, CSS, layouts and shared assets are untouched. All seven actual local preview URLs returned HTTP 200. Browser navigation index → balance was observed; this was not a full responsive/interactive-search audit. `git diff --check` passed; Git's existing `.gitignore` LF/CRLF advisory is unrelated to this content work.

Preview is the existing Hugo server at `http://127.0.0.1:1340/equipment/`. If it is stopped, use the inline environment setup and exact `hugo server` command in `.validation/equipment-review-20261017/commands.md`; no execution-policy change is necessary. Nothing is published pending local visual review.
