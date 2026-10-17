---
title: "DFRobot conductivity equipment — identification draft"
manufacturer: "DFRobot"
model: "Gravity K=1 / DFR0300 — candidate only; hardware revision unknown"
supplier: "Go Tronic (historical link)"
reference: "DFR0300 (candidate)"
status: "confirmed"
---

> **Superseded for presence status — 17 October 2026:** the supervisor has now confirmed presence. The public local record is `content/equipment/conductivity-equipment/index.md`. The identification cautions below remain research history, not the current inventory status.

# Conductivity equipment — To verify

Administrator draft outside Hugo content: not rendered, indexed or listed as available. Not confidential. Reviewed 17 October 2026.

## What the sources establish

The [historical supplier page](https://www.gotronic.fr/art-sonde-de-conductivite-k1-dfr0300-27863.htm) identifies DFRobot K1 / DFR0300 and describes a probe-and-interface kit. It does not prove that this kit or all its parts are physically present at the BioLab.

The [official DFRobot documentation](https://wiki.dfrobot.com/dfr0300) distinguishes:

| Part | Documentation | BioLab confirmation |
|---|---|---|
| Conductivity probe | K=1 cell constant; BNC connection to conditioner | Not confirmed |
| Interface / signal conditioner | V2 analog-output board documented separately | Not confirmed; hardware revision unknown |
| Meter / controller | Manufacturer examples use a separate controller, such as Arduino | No complete meter or controller identified locally |

Do not call this a standalone conductivity meter. Do not substitute the K=10 DFR0300-H variant. Do not assume calibration solutions, temperature sensor, controller or cables are owned.

## Version and specification discrepancy

The undated Go Tronic listing describes a 5 V / 0–15 mS/cm system. The undated current DFRobot wiki specifies a V2 conditioner at 3.0–5.0 V, a probe detection range of 0–20 mS/cm and a recommended range of 1–15 mS/cm. These may describe different revisions or different meanings of range. Do not merge them or publish a range for an unidentified local assembly.

## Before any public page

- [ ] Confirm physical presence and exact probe label / K value.
- [ ] Identify interface board revision and its condition.
- [ ] Identify an actual controller/display, if present.
- [ ] Check remaining parts and applicable manufacturer instructions separately.
- [ ] Record the inventory source and obtain supervisor review before presenting anything as available.

## Sources

- [Go Tronic historical supplier listing](https://www.gotronic.fr/art-sonde-de-conductivite-k1-dfr0300-27863.htm), undated; accessed 17 October 2026.
- [DFRobot K=1 / DFR0300 manufacturer documentation](https://wiki.dfrobot.com/dfr0300), undated; accessed 17 October 2026; includes a separate older-version documentation link.

No BioLab measurement/calibration procedure is supplied. Responsible person: Vivien Roussel.
