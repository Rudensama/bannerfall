# Game Design Document — *(working title: **Bastion** / **Rampart** / **Last Volley**)*

> **Status:** Skeleton v2. **[LOCKED]** = decided. **[DRAFT]** = my proposal, react to it. **[OPEN]** = needs your call.

---

## ⏭️ PICK UP HERE NEXT TIME (note to self)

**Where we are: the GDD is COMPLETE.** Every step is locked — core loop & grid (§2/§3), controls (§4), ammo pool (§5), specials (§5a), scoring + slot-order math (§6), run structure + numbers pass (§7), bosses (§7b), shop economy (§8), Banners (§9), Dock + monetization (§10), seeding (§11), art & audio (§12), and the MVP looping tuning-harness scope (§14). No open design forks remain.

**Next artifact: the TDD (Technical Design Document)** — all engine/architecture/implementation detail moves there, starting from §14's MVP scope. First TDD questions: engine (Unity vs Godot), scene/system architecture, how the range-slider tuning harness + per-stage randomizer are built, data schema for the swappable ball identity (§12a), and the field-generation algorithm (§11: weighted + patterned + noised).

**Deliberately deferred to MVP playtesting (feel → numbers):** final grid height (§3a/§14), the §7c constants, and finish-tightness. The harness exists to answer these.

**Working title still undecided:** Bastion / Rampart / Last Volley.
