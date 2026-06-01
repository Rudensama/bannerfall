## 5. The Ammo Pool [LOCKED]

- **The ammo pool is a persistent run-wide loadout, NOT a per-stage budget.** If your ammo pool is 20 balls, **every stage starts with all 20**, reshuffled. Stages do **not** permanently consume ammo — the ammo pool is fully restored at the start of each stage. The only thing that changes the ammo pool is **you**, at the shop (adding copies, specials, upgrading values).
- **Within a stage:** you draw through the ammo pool in a **single finite pass** (§5c). Drawing it dry before hitting the goal = loss (condition #2). Next stage, the full ammo pool returns.
- **Conveyor (left):** feeds the next ball from the shuffled ammo pool. **Random/shuffled order, can't choose the color.** Shows **N-ahead preview** (start: 1; upgradeable).
- **Shelf (right):** hold/swap. Starts at **1 slot**, upgradable per run. Bank an off-color or a special for the right moment.
- **Specials** are drawn from the conveyor exactly like normal balls **[5b LOCKED]** — it's the player's choice to fire or shelf them.
- **Running out = loss** (condition #2 above).

> **5c — RESOLVED [LOCKED].** Single finite pass per stage; ammo pool fully restored & reshuffled next stage. Ammo is a real resource *within* a stage but a fixed capability *across* the run.

### 5a. Special Balls Roster [LOCKED — MVP set of 5]

| # | Name | Rarity | Effect | Notes |
|---|------|--------|--------|-------|
| 1 | **Ram** (Vertical) | Common | Destroys the entire lane fired up, ignoring color. | Panic button for a stacked lane. |
| 2 | **Sweep** (Horizontal) | Common | Destroys the entire row at impact, ignoring color. | Clears a front line. |
| 3 | **Bombard** (Radius) | Common | Destroys all balls within radius R of impact, ignoring color. | R upgradeable. |
| 4 | **Chain Shot** | Rare | On hit, also destroys up to **X** same-type balls **anywhere on the field, regardless of distance** (Candy-Crush style). X upgradeable. | The color-logic AoE; scales via X. |
| 5 | **Wildcard** | Rare | Counts as whatever color it touches → guaranteed match + chain. | Flexible, gated. |

**Rarity [LOCKED]:** Common (Ram / Sweep / Bombard) — cheaper, appears more often in the shop pool. Rare (Chain Shot / Wildcard) — pricier, gated so the strong tools don't show up turn one. Gives the shop texture.

**Combo interaction [LOCKED]:** Firing **Ram, Sweep, Bombard, or Chain Shot grants +1 combo**, treated exactly like landing a minimum qualifying chain (≥N) — *regardless of how many balls it actually clears*. These specials **never reset** combo (they are neither a sub-N poke nor a mismatch). **Wildcard** builds combo through the normal §6c rule, since it produces a real color match. Net: every special advances the multiplier, so a special is never a dead turn for the build, while raw clear-count still doesn't inflate scoring on its own.

> **Cut from MVP (post-launch candidates):** **Anchor** (delayed two-step payoff, collided with the front-landing rule) and **Painter** (high UX cost — player must pick a color; advanced-tier). Parked, not deleted.

> **5d — RESOLVED [LOCKED].** Once bought, a special is **permanent for the rest of the run** (stays in the ammo pool until the run ends, like everything else in the loadout).