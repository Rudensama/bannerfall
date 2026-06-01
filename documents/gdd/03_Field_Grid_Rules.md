## 3. The Field & Grid Rules [LOCKED]

- **Grid:** fixed columns (= lanes) × rows. New rows push in from the top.
- **Spawn colors = ammo pool colors [LOCKED].** The field only spawns colors that exist in the player's ammo pool — you can only ever face what you can shoot. Consequence: a **single-color ammo pool is degenerate** (every shot wipes the board), so pools always carry **multiple** colors. **More color types = harder** (matching is rarer); this is a primary difficulty lever. Equal per-color counts (§8) keep the spawn distribution balanced.
- **Spawn counter:** ticks down 1 per fire; at zero a new row pushes in and it resets. Reset value is a per-stage modifier (every 1 / 2 / 4 shots…).
- **Correct hit:** destroys the struck ball + **flood-fills** all 4-directionally connected same-color balls (H/V only, **no diagonals**). Whole connected group clears.
- **Mismatch:** fired ball **becomes a real ball at the front** of that lane (closest to wall, most dangerous). Does not push the column. Double cost: a ball spent *and* the field worsened.
- **Gravity:** after a clear, balls slide **down toward the wall**, can trigger **cascade** chains.
- **3a — Wall buffer: BRUTAL [LOCKED].** No safety buffer. A front-landing mismatch when the lane is at the wall = instant loss.