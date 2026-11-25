---
pagetitle: "ADR-0001: Preserve and maintain, do not modernise"
---

# ADR-0001: Preserve and maintain, do not modernise

**Status:** Superseded by [ADR-0002](adr-0002-set-and-forget.md)
**Date:** 2026-11-25

## Context

We have a fleet of Prusa MK2 and MK3 machines, one with a high-flow/high-temperature hotend, plus a Mini. The temptation is to chase speed: Klipper on the Einsy, a 32-bit board, Bear frames, high-flow hotends on every machine. Each of those is a real upgrade and each costs money and hours.

The alternative reading is that the machines are already good, and what they need is maintenance, documentation, and honest framing, not a rebuild.

## Decision

1. **Preservation first.** Treat the MK2/MK3 as machines worth keeping in original or near-original form. Restore to like-new before modifying.
2. **Do not chase speed on 8-bit hardware.** A stock MK3S is an 8-bit Einsy with an ~200 mm/s travel ceiling. Klipper on the Einsy helps modestly and does not change the ceiling. If a machine must go faster, the sanctioned path is the MK3.5 xBuddy board, or buy a CoreXY.
3. **Stock firmware is the default.** Prusa's firmware is well-tuned (thermal model, linear advance) and GPL. We build it per board rather than replacing it, unless a machine is a deliberate experiment.
4. **One fast machine for throughput.** If speed is a business requirement, buy one modern CoreXY. Do not spend fleet money turning nine bed slingers into four slow ones.
5. **Trim the fleet.** Keep 2-3 machines that earn their keep. The rest become cold spares and donors, not projects.

## Consequences

- The project is a maintenance and documentation project, not a modification showcase.
- We publish an honest quality table (`docs/expectations.md`) so the community is not over-promised.
- Klipper remains in scope, but as a documented option for specific machines, not the default.
- Speed requests from users get routed to "buy a CoreXY" or "MK3.5", not to fleet-wide hotend upgrades.
- The sister project, Amalgam, covers the build-from-scrap case; this project covers the keep-what-you-have case.
