## 14. MVP Scope (Step 9) [LOCKED — design scope; implementation lives in the TDD]

**The MVP is a self-looping tuning harness** — a continuous prototype that doubles as a feel-finding machine. It plays stage after stage endlessly, **auto-advancing to a fresh randomized stage on every win *or* loss**, so you experience the core loop many times across many configurations in one sitting. This simultaneously tests the core-fun bet *and* surfaces the deferred tuning answers (§3a, §7c) by feel-then-readout. (Engine, panel UI, and architecture are TDD concerns, not here.)

### 14a. The loop
- **Continuous / kinda endless:** on win (goal hit) **or** loss (wall breach / ammo dry), immediately roll and start the next stage. No menus between — just loop.
- Each stage's parameters are **rolled randomly within developer-set ranges** (§14c).
- Ammo pool reshuffled (random order) each stage.
- **4 lanes × 4 colors**, fixed for MVP; balls use the data-driven identity from §12a (programmer-art shapes are fine).

### 14b. Real / faked / out
- **REAL (the loop under test):** slide + fire straight up; conveyor feed with 1-ahead preview; 1 shelf slot (hold/swap); finite shuffled ammo pool, single pass; correct-hit flood-fill clear; gravity + cascades; mismatch lands at the front; spawn counter pushing rows; **both lose conditions**; and the **danger visual** (§12c — part of whether the wall feels fair).
- **FAKED:** stage parameters are randomized rather than authored; programmer-art balls; sound optional on the first pass.
- **OUT entirely (not even stubbed):** specials, Banners, bosses, shop, Dock, coins/Renown, monetization, all meta. They're not what's being tested.

### 14c. Tuning panel — RANGE sliders [the key MVP feature]
A dev panel sets a **min–max range** per parameter; each new stage rolls a random value inside that range, so one looping session sweeps many stage shapes. Candidate ranges:

| Parameter | Candidate range |
|---|---|
| Grid height (visible rows) | 3 – 10 |
| Spawn counter (shots per new row) | 1 – 4 |
| N (combo threshold) | 2 – 5 |
| Score goal | tunable range |
| Ammo count per color | 3 – 8 *(rolled once, applied to all 4 colors to keep §8b equal-count balance; optional per-color toggle to stress-test imbalance)* |

**On-screen readout** displays the current stage's rolled values, so when a stage feels great you can record its config — turning feel into the concrete numbers that finalize §7c / §3a.

### 14d. Success criteria (the questions the harness must answer)
1. **One-more-run pull** across looping stages? (the core fun bet)
2. Does the **brutal no-buffer wall** (§3a) feel *fair* or *cheap*?
3. Does the **combo rule** (chain ≥N or reset) feel satisfying with random ammo?
4. **Which ranges/values feel right?** — captured from the readout, these become the final §7c constants and the §3a grid height.

> **§14 — RESOLVED [LOCKED].** MVP = a continuous, self-looping prototype that auto-rolls a randomized stage on each win/loss, driven by a range-slider tuning panel with an on-screen value readout. Proves the dual-pressure firing loop is fun *and* discovers the deferred numbers in the same build. All meta is out. The how (engine/architecture) is the TDD's job.