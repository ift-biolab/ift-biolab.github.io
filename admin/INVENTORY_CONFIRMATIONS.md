# Supervisor inventory confirmations — 17 October 2026

This update supersedes the presence-status conclusions in `EQUIPMENT_REVIEW.md` and the two earlier identification drafts. Their technical source conflicts remain relevant. This administrator report is outside Hugo content; it is not confidential in the public source repository. No commit or push is authorised or performed.

## Interpretation of the edited checklist

The supervisor marked **11 lines `[Y]`**, including “6x 2L” for beakers and “+ camera motic dessus” on the microscope line. The camera is therefore a **twelfth presence confirmation**, not an inferred accessory. Presence is confirmed; neither a scientific protocol nor equipment readiness is validated by these marks.

The machine-readable inventory metadata and visible checklist are now consistent. `[Y]` has been normalised to Markdown `[x]`. The original user-edited file is preserved in ignored `.validation/inventory-confirmations-20261017/user-checklist-original.md`. Shopping-list/tracking URL parameters were removed from displayed links, while product identifiers remain intact.

## Confirmations applied

| Record | Result | Remaining identification or quantity check |
|---|---|---|
| Cleaning tools | confirmed; administrator facility/support inventory only | Exact product/model and quantity; ASIN B01HTTQ6FC not retrieved |
| Magnetic stirrer | confirmed; `content/equipment/magnetic-stirrer/index.md` | Model, manual, quantity; ASIN B07GR772K7 inaccessible; no heating or speed inferred |
| Overhead stirrer | confirmed; `content/equipment/overhead-stirrer/index.md` | Model, manual, quantity; ASIN B079S28RJ2 inaccessible; no torque/speed/accessory inferred |
| Large beakers | confirmed; existing Materials / Consumables glassware table | **6 × 2 L**, GLASSCO family identified by supervisor link; exact pack reference not assigned |
| Wall drying rack | confirmed; `content/equipment/laboratory-wall-drying-rack/index.md` | Labbox family supplied; exact variant, dimensions, fittings and quantity unknown |
| Support stand | confirmed; `content/equipment/laboratory-support-stand/index.md` | Exact model, dimensions, attachments and quantity; ASIN B08P6Z5L68 inaccessible |
| Motic BA-310 microscope | confirmed; `content/equipment/motic-ba310-microscope/index.md` | Head, illumination, objectives, exact configuration and quantity not newly supplied |
| Motic camera on microscope | confirmed by explicit note; `content/equipment/motic-microscope-camera/index.md` | Camera model, sensor, interface, software and matching manual unknown |
| Conductivity equipment | confirmed; `content/equipment/conductivity-equipment/index.md` | Probe, interface-board revision and separate controller require individual identification; no complete standalone meter inferred |
| Mannitol | confirmed; existing Materials / Molecular Biology & Microbiology table | Container reference, grade, remaining quantity and pack size unknown |
| Bacteriological peptone | confirmed; same existing Materials table | Container reference, grade, remaining quantity and pack size unknown |
| Bacteriological agar | confirmed; same existing Materials table | Container reference, grade, remaining quantity and pack size unknown; distinct from the existing LB agar purchase record |

The seven previously documented purchased equipment pages are unchanged. Seven newly confirmed equipment records are added using the same page-bundle structure and standard headings. No duplicate historical public pages existed. New image folders contain only empty `.gitkeep` files; no image is downloaded, moved, edited or embedded.

## Still to verify — seven records

- Paper drying rack.
- Miracloth (Materials, not Equipment).
- Large autoclave — **Exact model identification required.**
- PU / PVC / Plexiglas trays.
- Insect UV lamp (support device, not laboratory UV instrumentation).
- Microscope immersion oil — omitted from the edited checklist; omission does not confirm presence or absence.
- Bacitracin — omitted from the edited checklist; omission does not confirm presence or absence.

These remain `to-verify` in the administrator inventory and are not newly listed as available on the website. The pre-existing 33 `reported` chemicals and their statuses are unchanged.

## Documentation checked

All links below were reviewed on 17 October 2026. No new quantitative equipment specification was imported from a catalogue into an unidentified local model.

- [Labbox GLASSCO low-form beakers](https://labbox.fr/produit/becher-forme-basse-glassco/): family confirmed. The current 2 L catalogue pack is four, whereas the supervisor confirms six individual beakers. These are different units/count contexts; do not change the confirmed quantity to four or assign a pack reference as a purchase reference.
- [Labbox wall drying rack](https://labbox.fr/produit/egouttoir-mural-pour-materiel-de-laboratoire/): exact local variant unknown; no family dimensions assigned.
- [Supplied Fourni-Labo microscope link](https://www.fourni-labo.fr/produit/microscope-de-biologie-superieur-motic-modeles-ba-310-et-ba-310-numerique): could not be retrieved. The [official Motic BA310 LED Trinocular candidate page](https://www.motic.com/As_ls_UM_BA310/product_473.html) remains candidate documentation and retains its previously reported head-description inconsistency. No objectives/camera configuration inferred from it.
- [Go Tronic conductivity listing](https://www.gotronic.fr/art-sonde-de-conductivite-k1-dfr0300-27863.htm) and [official DFRobot documentation](https://wiki.dfrobot.com/dfr0300): probe/conditioner/controller distinguished; prior revision/range discrepancy unresolved for the actual assembly.
- Current Labbox pages recovered from the inaccessible historic `fra.labbox.com` links: [mannitol](https://labbox.fr/produit/d-mannitol-pour-bacteriologie-agr-acs/), [bacteriological peptone](https://labbox.fr/produit/peptone-bacteriologique-bac/), [bacteriological agar](https://labbox.fr/produit/gelose-agar-bac/). Linked as product-family documentation only; no catalogue purity, pack size, container reference, CAS number, hazards, storage location or preparation instructions assigned to local stock.
- Historical Amazon listings for stirrers/stand remain inaccessible. Their ASINs are retained as identification aids, not manufacturer models. The supplied cleaning-tool link is retained without a model claim.

## Scope and validation

No theme, layout, JavaScript, Hugo configuration, top-level navigation, student repository or GitHub setting was changed. Existing root and subpath deployment structure remains in use. Equipment index groups are extended and Materials counts updated; the seven new equipment pages and existing materials tables are the actual sources used by Hugo preview/build.

Build logs, exact local commands, starting Git status/HEAD, before-hashes, original user checklist and final checks are in ignored `.validation/inventory-confirmations-20261017/`. Local review starts at `http://127.0.0.1:1340/equipment/` and `http://127.0.0.1:1340/materials/`.

Results: clean root and `/review/` Hugo builds passed (57 pages each, warnings treated as errors); generated local links/assets and search-data checks passed. The seven new equipment pages are served by the actual existing local preview. Twelve confirmed / seven to-verify administrator records and checkboxes agree. Source hashes confirm the original seven equipment pages, images, design and all other sections are unchanged; only the Equipment index and three existing Materials files changed among pre-existing content. Git HEAD is unchanged; no files staged, committed or pushed. This round did not add an interactive browser/search or responsive visual audit; local visual review remains with the supervisor.
