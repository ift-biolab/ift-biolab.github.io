# Markdown inventory maintenance

Public records live in Markdown front matter under `inventory`: one record on each equipment page, and lists on each compact Materials page. There is no database or procurement integration. Edit the corresponding public Markdown table/text at the same time as its metadata. `admin/inventory-to-verify.md` holds items not approved for public availability lists.

Each record supports `name`, `category`, `status`, `manufacturer`, `model`, `reference`, `quantity`, `unit`, `notes`, `source`. Unknown values are `null` (not zero). Allowed inventory statuses are exactly `confirmed`, `reported`, `to-verify`; these differ from protocol statuses. Keep manufacturer and model null unless explicitly confirmed separately; product names retain the wording supplied by the team. Numeric sizes in references must never be decoded into specifications or quantities.

Confirmed equipment/materials may appear in available-resource indexes. A reported item may appear **as available** only after an explicit publication approval is recorded in `notes`; otherwise keep it in the clearly labelled reported/verification-pending group. No reported item in this initial inventory has been approved as confirmed available. `to-verify` items remain only in the administrator checklist. Existing example equipment is hidden from navigation/listings and remains a placeholder at its original URL, not an inventory item.

PVW2602335 is the supplied source identifier for confirmed 2026 purchases, not a published procurement document. Amounts are purchase-list amounts, not live stock. Reconfirm current stock/access/readiness manually. Names, source identifiers and sizes may be displayed; no purchase prices, chemical storage locations or inferred chemical properties are included. Do not add operational chemical instructions or treat this site as an SDS.

Consumable references and counts were not supplied in the handoff. Retain null until an actual product reference/count is supplied; do not infer them from similar products. No purchase-list file beyond the user's supplied text was found in the workspace.

The inventory validation in the handoff checks all statuses, required metadata keys, public-table/metadata correspondence, seven equipment page outlines and exclusion of administrator checklist names from generated HTML/search. New source data should be reviewed before publishing. Administrator files in this public repository are non-public-facing website sources, not access-controlled storage.
