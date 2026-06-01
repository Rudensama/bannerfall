## 11. Randomness & Seeding [LOCKED + DRAFT]

- **Seeded RNG everywhere [LOCKED].** All randomness (field spawn, ammo pool shuffle, shop contents) derives from a master seed → reproducible runs (bug repro, run-sharing, fair leaderboards, easier balancing).
- **Separate RNG streams per system [LOCKED].** Field-spawn, ammo-pool shuffle, and shop each get their **own** independent stream seeded from the master. This guarantees one system's randomness can't desync from another based on incidental player actions — e.g. the stage-3 shop is identical regardless of how stages 1–2 were played. (Standard roguelite practice.)
- **Field generation = weighted + patterned + noised [LOCKED], not pure random.** Incoming rows are arranged so that:
  - **Weighted** — color frequencies can be tuned (and always drawn from the ammo pool's color set, §3).
  - **Patterned** — clusters/adjacencies are seeded so setups and chains are *possible* (pure random tends to scatter and kill chaining).
  - **Noised** — light randomness on top so it never feels deterministic.

### 11a. Seed policy [DRAFT — chosen approach]
Raw "ban any seed that fails to pass stage 5" doesn't work: pass/fail is dominated by **player skill**, not the seed, and with fully-random seeds almost no two players share one, so there's nothing to aggregate. Workable approaches:

- **Normal mode:** fully random seeds + **robust generation constraints** (the weighted/patterned/noised rules above) so no board is ever unwinnable. Tune the *algorithm* from aggregate data, not seed-by-seed.
- **Optional curated pool (allowlist):** if same-seed fairness is wanted, assign runs from a **vetted seed pool**; auto-flag a pooled seed for review only when its win-rate is far below the pool average **within the same skill bracket** (controls for the skill confound). Retire flagged seeds. This is an allowlist, never a blocklist of infinity.
- **Daily challenge:** one hand-tested shared seed per day; players compare runs on identical conditions.

> Recommended: random seeds + strong generation constraints for normal play, plus a curated daily seed. Same-seed competitive ladder only if you want that mode.