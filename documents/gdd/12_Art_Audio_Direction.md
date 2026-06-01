## 12. Art & Audio Direction (Step 8) [LOCKED]

**Tone [LOCKED]: stylized-characterful medieval.** Not grimdark, not cutesy. Guiding rule: **restraint on the playfield, personality in the frame.** The board (balls, lanes) stays clean and high-contrast so it parses instantly; the castle wall, flying Banners, cannon, and boss sigils carry the medieval-siege character. Confident and readable (Balatro-like restraint, dressed as a siege), distinctive in the casual market, and consistent with the playful-grounded naming (Quartermaster's Flag, The Pillager, Crimson Standard).

### 12a. Ball identity system [LOCKED] — readability + colorblind safety
Every ball is legible by **shape, not color alone** (the wall is instant-loss, §3a; ~8% of players are colorblind). Color + a distinct silhouette symbol, redundant by design. MVP starting set (names tie to the Banner color family, §9):

| Color | Hue | Symbol |
|---|---|---|
| **Crimson** | red | triangle |
| **Azure** | blue | diamond |
| **Verdant** | green | square |
| **Amber** | gold | star |

> **Scalable & swappable [LOCKED — architectural constraint].** The ball identity (color + shape + symbol + score behavior) must be **data-driven** (e.g. a ScriptableObject / config table), never hard-coded. Adding, removing, or reskinning a color must require **no gameplay-code changes** — the Dock's expanding color-count baseline (§10) and any future palettes depend on this. Build the identity as data from day one.

### 12b. The frame [LOCKED]
- **Castle wall** across the bottom — what you defend; it visibly cracks as lanes approach (danger language).
- **Cannon** on the wall, swivels between lanes.
- **Conveyor** (left) = supply chute; **Shelf** (right) = quartermaster's crate.
- **Banners** fly as heraldic flags along the top HUD (your held loadout, in slot order).
- Incoming balls descend like a slow siege from the top.

### 12c. Danger language [LOCKED — non-negotiable game feel]
Because a front-landing mismatch at the wall is instant loss, the threat must be felt a turn early: as a lane nears the wall, the wall section beneath cracks and reddens, the front ball pulses, and a low rumble rises. Every danger cue has a visual form (mobile is often played muted).

### 12d. Combo & score juice [LOCKED] — the core reward
- Combo multiplier = a war-banner that physically grows/raises as it climbs.
- Cascades pop in sequence with a rising pitch ladder.
- A big combo fires a screen-wide payoff (banner snaps taut, score numbers fly, light shake).
- The "score explosion" moment should feel disproportionately good — it's what the whole loop builds toward.

### 12e. Boss identity [LOCKED]
Each boss takes the top of the screen with a dark heraldic sigil, debuff **telegraphed visually**: The Fog fogs the preview; The Blight tints the cursed color sickly grey-green; The Pillager shows the shelf crate smashed; The Tide darkens the spawn line; The Inert greys the dead color's chaining; The Demanding flies a higher-N standard. Read the threat at a glance.

### 12f. Audio [LOCKED]
- Clear = satisfying clay "tok"; **combo climbs a rising pitch ladder** (audio is half the combo dopamine); cascades = arpeggio.
- Mismatch = dull thud + danger cue. Big combo = triumphant stinger. Boss = ominous entry stinger + themed ambient.
- Music: **light medieval** — plucked strings + hand percussion, not bombastic orchestral — with adaptive intensity rising as wall pressure mounts.
- **Every critical audio cue has a visual twin** — nothing lives in sound alone.

### 12g. Mascot [DEFERRED — post-MVP]
A cannoneer/defender character (personality + store/marketing appeal) is a documented future option but **explicitly out of MVP** to keep the solo-dev asset load manageable. Revisit after first playable.

> **§12 — RESOLVED [LOCKED].** Stylized-characterful medieval; restraint on board / personality in frame. Data-driven, swappable ball identity (4-color MVP set, shape+color redundant, colorblind-safe). Explicit danger language for the brutal wall. Juice concentrated on the combo/score payoff. Light-medieval adaptive audio with visual twins. No mascot for MVP.