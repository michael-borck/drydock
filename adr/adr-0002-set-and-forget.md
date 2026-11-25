---
pagetitle: "ADR-0002: The Prusa feel, set and forget"
---

# ADR-0002: The Prusa feel, set and forget

**Status:** Accepted

**Date:** 2026-11-25

**Supersedes:** ADR-0001

## Context

ADR-0001 set out to preserve the fleet and trim it to two or three machines. The fleet registry then listed twenty-nine machines, six of them under construction. Four of those (the LulzBot AO-101, the MakerFarm i3v, the wooden-frame MK2.6S+ clone and the Prusa Mendel) are being restored for nostalgia, then used to see how far Prusa firmware can be pushed with E3D hotends. ADR-0001 rule 5, "the rest become cold spares and donors, not projects", does not describe that.

What ADR-0001 left out is the reason. The first MK3S, coming from an Ender, felt like set and forget. Everything in this project is an attempt to get that feeling back, or to get it onto hardware that never had it.

## Decision

The mission is three lines:

1. **Give a printer the Prusa feel: set and forget.**
2. **It is not speed.** If you need to print faster, get another printer, as cheaply as you can.
3. **Don't retire a machine that still works** because something newer came along.

Five working rules follow. The first three carry ADR-0001 forward. The last two replace its experiment exception and its trim rule.

1. **Preservation first.** Restore to like-new before modifying.
2. **No speed chasing on 8-bit hardware.** A stock MK3S is an 8-bit Einsy with an ~200 mm/s travel ceiling, and Klipper on the Einsy helps only a little. If a machine must go faster, the path is the MK3.5 xBuddy board or another printer.
3. **Stock firmware is the default for keepers.** We build Prusa's firmware per board. Experiments may change it; that is what makes them experiments.
4. **Experiments are a line of work, not an exception.** A machine marked as an experiment in the registry exists to find how far set and forget can be pushed, and the result is written up.
5. **The fleet is not trimmed to a number.** The registry records what each machine is for: a keeper, an experiment, a donor, or for sale.

## Consequences

- "Set and forget" is the MK3S standard as remembered after an Ender, not a promise of modern auto-calibration. `docs/expectations.md` stays published, and stays honest about where the machines are behind.
- The nostalgia builds are in scope, marked as experiments in `machines/registry.md`.
- Machines that Amalgam's donor guide rates well become donors. The registry's donor rules say how.
- The project is still not a speed project or a modification showcase. An experiment is judged by how little attention the printer needs, not by what was added to it.
