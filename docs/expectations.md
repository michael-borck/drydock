# Expectations: what an MK2/MK3 can and cannot match

Publish this. The fastest way to lose a community is to promise speed and deliver an hour-long benchy.

Two reference machines:
- **This project:** maintained MK3S, stock 8-bit Einsy, good hotend, fresh mechanics, tuned profile.
- **Modern:** 2026 CoreXY, e.g. Bambu A1/P1S or a Klipper Voron-lineage machine like the Two Trees SK1.

| Capability | Maintained MK3S | Modern CoreXY | Notes |
|---|---|---|---|
| Best-case quality, slow and tuned | Equal | Equal | Dimensional and surface quality are a wash here. |
| Quality at 150-300 mm/s | Behind | Ahead | Physics. Bed slinger mass, 8-bit step rate. |
| Dimensional accuracy | Equal | Equal | Both hold roughly +/-0.1 mm when tuned. |
| Tall, thin parts | Behind | Ahead | The moving bed throws tall parts. CoreXY does not. |
| Overhangs and cooling | Slightly behind | Ahead | Modern ducts and dual fans are better. |
| ABS / ASA | Equal with enclosure | Ahead out of the box | Modern enclosed machines win on convenience, not quality. |
| Multi-material | Behind | Ahead | MMU3 works but is fiddly. AMS is easier. |
| First-run consistency, no tuning | Behind | Ahead | Auto-cal and baked profiles hide a lot. |
| Repairability | Ahead | Behind | Open boards, commodity parts, published schematics. |
| Long-term parts availability | Ahead | Behind | Rods, belts, bearings, hotends stay in production. |
| Firmware openness | Ahead | Behind | Prusa firmware is GPL. Most modern firmware is not. |
| Cloud requirement | None | Often yes | This is a hard blocker for schools and makerspaces. |
| Power per part (PLA) | Roughly equal | Slightly lower | Faster machines use less energy per part by finishing sooner. Idle draw is similar. Keeping a Prusa costs you time, not watts. |
| Cost to keep running | Ahead | Behind | Belts, bearings and nozzles are cheap and universal. |

## The honest summary

For functional parts, at Prusa speed, a maintained MK3 matches a new printer. It cannot match it at speed, on tall geometry, or on the first print with no tuning.

Use that sentence. It is defensible, and it is the version that earns trust.
