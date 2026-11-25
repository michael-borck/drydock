# Drydock

> Working title. Alt: Keel, Liferaft, Anvil.

**Keep the fleet printing.**

A maintenance project for Prusa MK2 and MK3 printers: tested restore procedures, firmware builds per board, calibration profiles, and a parts list you can still buy. The goal is a printer that produces the same quality as a new machine for functional work, at Prusa speed, with no cloud and no vendor account.

Sister project to [Amalgam](../amalgam): Amalgam builds a printer from two donors. This keeps the printers you already own alive.

---

## Why this exists

The MK2 and MK3 are not obsolete. They are paid for, repairable, offline, and documented. What they lose is speed. They do not lose print quality for functional parts, and they do not lose the ability to be fixed with a bearing, a belt, and a hotend you can still order.

Meanwhile the market has spent five years selling speed, cloud accounts, and apps. When a printer's board dies under that model, the owner is stuck. This project is the other path: a machine you own outright, can repair indefinitely, and never has to phone home.

We are honest about the trade. An MK3 prints a good part in an hour that a CoreXY prints in twenty minutes. If you sell print time, buy the CoreXY. If you need a machine you can keep running for a decade, this is for you.

## What this is

- A tested recipe to bring an MK2 or MK3 back to like-new mechanical condition.
- A firmware matrix: which board, which build, which options.
- Calibration profiles for PrusaSlicer and Orca, tuned per machine.
- A parts list with current sources and substitutes.
- A place to record what each machine is, so the knowledge outlives the person who knew it.

## What this is not

- A speed project. For 300 mm/s, buy a CoreXY.
- A clone-piracy guide.
- A showcase for mods you cannot source next year.

## Who it is for

People who inherited or cheaply bought a Prusa. Schools and makerspaces that cannot run cloud-locked hardware. Small shops that want a second machine without a subscription. Anyone who wants a printer they can still fix in ten years.

## Structure

```
README.md
docs/
  manifesto.md        The pitch and the refusal
  expectations.md     Honest quality table: what matches, what doesn't
  philosophy.md       Why preservation beats replacement
adr/                  Architecture Decision Records
  adr-0001-preserve-not-modernise.md
machines/             Per-board notes: mk2-rambo, mk3s-einsy, mk3s-xbuddy, mini
runbooks/             Restore, mechanical refresh, firmware build, calibration
parts/                BOM, sources, spares and donor registry
profiles/             PrusaSlicer and Orca profiles
_archive/             Old imports, kept for reference. Not part of the project.
```

## Status

| Area | Status |
|------|--------|
| Pitch and framing | Done |
| Honest expectations table | Draft |
| Restore runbook | Planned |
| Firmware matrix | Planned |
| Calibration profiles | Planned |
| Fleet registry | Planned |

## Lineage

RepRap and Prusa have always been open machines. This project keeps that true.

- Prusa MK2/MK3 firmware: [prusa3d/Prusa-Firmware](https://github.com/prusa3d/Prusa-Firmware) (GPLv3)
- Klipper: [Klipper3d/klipper](https://github.com/Klipper3d/klipper)
- Sister project: [Amalgam](../amalgam)

## License

Docs: CC BY-SA 4.0. Code and configs: GPLv3, matching Amalgam and the firmware we build on.
