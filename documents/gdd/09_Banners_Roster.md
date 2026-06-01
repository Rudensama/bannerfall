## 9. Banners Roster [LOCKED — MVP set]

Banners = Balatro-style passives. Built in-run, **wiped** at run end. Apply in slot order (§6a). Mix of scoring + economy + utility effects.

**Banner slots [LOCKED]:** start at **3**, **expandable via the shop** (+Banner slot is a purchasable in-run upgrade, §8). This bounds the build and makes "which 3 do I keep, and in what order" the core decision.

**Score-Banner typing [LOCKED]:** each score Banner is **additive** (`+flat`) or **multiplicative** (`×factor`); they apply in slot order and do not commute (§6a). Order is skill.

**Rarity [LOCKED]:** Common (appears often, cheap) / Rare (gated, pricier) / Legendary (build-defining, rare + expensive). Numbers below are tuning targets (base ball value = 10, §7c).

**Tiered Banners [LOCKED]:** utility Banners come in numbered tiers (I / II / III) — a higher tier grants more, and **rarity climbs with tier** (I = Common, II = Rare, III = Legendary).
- **Tier prerequisite to *buy*:** purchasing a higher tier requires already holding the immediately-lower tier — Long March II needs Long March I in hand, Long March III needs II. (Same for Quartermaster's Flag.)
- **Appears regardless:** a higher tier can still **show up in the shop** even if the player lacks the prerequisite — it's displayed but **locked/unpurchasable** (e.g. greyed with "requires Long March I") until the prereq is owned. The shop window can tease the climb.
- **Upgrade-in-place:** buying the next tier **consumes the lower tier and occupies the same slot** (climb 1 → 2 → 3, paying coins each step). The tier-up never costs extra Banner slots — it just deepens one. *(This tier mechanic could later extend to the coin/score families — e.g. Crimson ×2 → ×3 — but for MVP only utility is tiered.)*

#### Filler / Common — early-game padding (deliberately low-impact; fades as the build scales)
| Banner | Rarity | Type | Op | Effect |
|--------|--------|------|----|--------|
| **Footman's Banner** | Common | Score | +flat | +50 score on any shot that clears ≥N. |
| **Drummer's Banner** | Common | Score | +flat | +10 score per ball cleared this shot. |
| **Standard Bearer** | Common | Score | ×factor | All clears score ×1.25 (weak universal multiplier — training wheels for the color family). |
| **Almsbanner** | Common | Coin | — | +2 coins per stage cleared (a weaker Tithe). |

#### Core Common
| Banner | Rarity | Type | Op | Effect |
|--------|--------|------|----|--------|
| **Tithe Banner** | Common | Coin | — | +X coins per stage cleared (flat). |
| **Usurer's Banner** | Common | Coin | — | Leftover-ammo coins multiplied ×1.5. |
| **War Tax** | Common | Coin | — | +1 coin per shot fired this stage *(anti-synergy with Usurer's; deliberate tension)*. |
| **Long March I** | Common | Utility | — | +1 conveyor preview. *(Primary source of preview — pulled from shop, §8.)* |
| **Quartermaster's Flag I** | Common | Utility | — | +1 shelf slot. *(Primary source of shelf — pulled from shop, §8.)* |

#### Rare
| Banner | Rarity | Type | Op | Effect |
|--------|--------|------|----|--------|
| **Crimson Standard** | Rare | Score | ×factor | A chosen color's clears score ×2. *(One variant per color — Azure, Verdant, etc.)* |
| **Cascade Pennant** | Rare | Score | base-mod | Each cascade step adds extra combo multiplier (boosts the combo term in base, before the slot pass). |
| **Banner of Spite** | Rare | Score | +flat | Mismatched balls score a flat bonus when later cleared (mistakes → setups). |
| **Long March II** | Rare | Utility | — | +2 conveyor preview. |
| **Quartermaster's Flag II** | Rare | Utility | — | +2 shelf slots. |

#### Legendary
| Banner | Rarity | Type | Op | Effect |
|--------|--------|------|----|--------|
| **Pyrebrand** | Legendary | Score | shot-mod | Every 5th shot's fired ball becomes a free Bombard (also +1 combo via §5a). Not part of the additive/multiplicative pass. |
| **Long March III** | Legendary | Utility | — | +3 conveyor preview. |
| **Quartermaster's Flag III** | Legendary | Utility | — | +3 shelf slots. |

> **§9 — RESOLVED [LOCKED].** 3 slots, shop-expandable. Score Banners typed additive/multiplicative so slot order is a real lever (§6a). +shelf / +preview live **only** as tiered utility Banners (removed from the shop's direct-upgrade list to kill redundancy) — consequence: a run that never finds them stays at 1 shelf / 1 preview. Filler commons pad the early pool and teach the additive/multiplicative idea gently. Synergy is the fun — deliberate pairs (an additive Banner slotted *before* Crimson Standard) and tensions (Usurer's vs War Tax) are the design spine.