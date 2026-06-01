## 7. Run Structure [DECIDED — tunable]

You asked me to pick. Proposal:

- **A run = 8 stages.**
- **Boss on stage 4 and stage 8.** Stage 8 boss = the **loop/win point**.
- After stage 8, optional **Endless** mode with escalating goals (leaderboard / high-score chasing).
- **Score goals scale** each stage; bosses carry a higher goal + a disruptive modifier.
- Rough threat pacing: early stages = small ammo pools, slow spawn (ammo is the threat). Later/boss stages = bigger ammo pools, fast spawn (the wall is the threat).

### 7b. Boss Stage Roster [LOCKED — MVP set of 6]

**Selection [LOCKED]:** which boss fills the stage-4 slot and the stage-8 slot is **pure seeded randomness** (§11) — no rarity, no difficulty tiering. Both slots draw from the same 6-boss pool. (Different draw per slot within a run.) Bosses carry a higher score goal (§7c curve) **plus** their disruptive override below.

| Boss | Effect | Override |
|------|--------|----------|
| **The Demanding** | Raises the chain length needed to keep combo — forces bigger setups. | N: 3 → **4** for the stage. |
| **The Fog** | Fire blind — the conveyor preview is gone. | Conveyor preview → **0** (regardless of Banner tier). |
| **The Inert** | One seeded ammo-pool color **won't chain** — striking it clears only the single struck ball, never the connected group. Attacks *clearing/chaining* (that color can't make a ≥N chain). | 1 seeded color: flood-fill disabled. |
| **The Blight** | One seeded ammo-pool color **won't score** — it still chains and clears normally (so it's usable for survival and still builds combo), but its cleared balls are worth **0 points**. Attacks *scoring* — earn the goal off the other 3 colors. | 1 seeded color: ball_value → **0** for the stage. Chain length still counts toward combo. |
| **The Tide** | A new row every single shot — doubles the spatial pressure. | Spawn counter → **1 row / shot** (from base 1/2). |
| **The Pillager** | Your stores are raided — no shelf to bank or swap. Must fire straight from the conveyor. | Shelf slots → **0** (regardless of Quartermaster's Flag tier). |

> The Inert (no chain) and The Blight (no score) are a deliberate **color-debuff pair** — one attacks clearing, the other scoring. Both target a *seeded* color so the threat varies per run. The Fog (no preview) and The Pillager (no shelf) are a **utility-stripper pair** — each nullifies one of the utility Banners' benefits.

> **§7b — RESOLVED [LOCKED].** 6-boss MVP pool, seeded-random selection per slot, no rarity. Overrides are tuning targets (the N bump, the spawn rate, etc. move with playtest data). **Cut from MVP (post-launch candidates):** **The Mason** (stone balls — risked a hard-wall soft-lock for special-less players; revisit with a safety rule) and **The Mirror** (horizontal field shuffle — felt unfair to play around and undercut the seeded-determinism value, §11).

---

### 7c. Numbers Pass — Loop 1, Stages 1–8 [LOCKED — formula-driven, tunable at MVP]

**Design principle:** there is **no hand-authored per-stage difficulty.** The *only* lever is the **rising score goal**, and it pressures both fail states at once. Spawn rate and ammo pool stay constant on normal stages, so a higher goal forces more clears → more turns → more rows at the wall (spatial pressure) *and* more score squeezed from the same finite ammo pool (ammo pressure). Raise one number, both threats tighten automatically. The shop is the player's only answer. Pure Balatro: blinds scale, the build keeps up.

#### Constants [LOCKED — adjust during MVP testing]

| Constant | Value | Notes |
|---|---|---|
| Starting ammo pool | **4 colors × 5 = 20** | MVP baseline (§14). |
| **N** (combo threshold) | **3** | Clear ≥3 connected to grow combo (§6c). |
| Base ball value | **10** | Clean math; per-color value upgrades multiply from here (§8). |
| Combo step | **+1, uncapped** | Runaway is intended — that's the build. |
| Base spawn counter | **1 row / 2 shots** | Constant on normal stages; bosses override (e.g. The Tide = 1/shot). |
| Grid (visible rows) | **TBD at MVP** | The wall-breach runway. Decided on feel during first-playable, not pre-tuned. |
| Finish tightness | **TBD at MVP** | How much leftover ammo a clean run keeps is tuned on feel, not pre-authored. |

#### Ammo pool output math (why the curve is shaped this way)

Score per shot = `balls_cleared × 10 × combo`. Combo climbs **+1 per qualifying chain**, so the combo term is a **triangular number** — that's where score explodes, not ball count. For a fresh 20-ball pool:
- **Conservative** (avg 3 cleared/shot, combo climbs every shot): `30 × (20·21/2)` = **6,300** ceiling (perfect play).
- **Realistic** (combo breaks a few times, ends ~×10): **~3,000–4,000**.

So a fresh ammo pool does **~3.5k realistic / ~6.3k perfect**.

#### Goal curve

Within a loop: **`Goal(s) = 1500 × 1.6^(s-1)`**

| Stage | Goal | vs. fresh ammo pool |
|---|---|---|
| 1 | 1,500 | trivial — teaches the loop |
| 2 | 2,400 | comfortable |
| 3 | 3,840 | near realistic output — play tight or start shopping |
| **4 (boss)** | **6,144** | **at perfect-play ceiling → first real wall; shop build must show up** |
| 5 | 9,830 | shopped builds only |
| 6 | 15,729 | |
| 7 | 25,166 | |
| **8 (boss/win)** | **40,265** | loop/win point |

**Design target met:** stages 1–3 clearable on the starting ammo pool (teach the loop), stage-4 boss is the crossover where shop investment becomes mandatory.

#### Per-loop scaling

**`Goal(s, L) = 1500 × 1.6^(s-1) × q^(L-1)`**, with **`q ≈ 1.6^8 ≈ 43`** so loop 2 picks up **continuously** where loop 1 ended (no discontinuous wall, endless ramp). `q` is the gentlest knob to revisit if loop 2 feels too steep.

> **7c — RESOLVED [LOCKED, tunable].** Difficulty is the goal curve alone (no authored stage difficulty). `G1 = 1500`, per-stage `r = 1.6`, crossover at the stage-4 boss, combo `+1` uncapped, base value `10`, continuous loop scaling. Grid height and finish-tightness are deliberately deferred to MVP playtesting. All values are tuning targets, not sacred — the *structure* is locked, the *constants* move with playtest data.