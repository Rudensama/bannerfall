# Bannerfall

Bannerfall is a mobile-first Godot prototype for a turn-based lane-defense color-matching roguelite. Players fire colored balls straight up from a cannon to clear matching groups, while a descending field and a finite ammo pool create dual pressure: survive the wall advance and reach the score goal before running out of balls.

## High Concept

- **Genre:** Casual / roguelite puzzle
- **Platform:** Mobile (portrait)
- **Engine:** Godot 4.6
- **Working title:** Bannerfall
- **Core loop:** slide → swap → fire → resolve clears/cascades → field advances → repeat

## Gameplay

- Fire from a cannon into one of several discrete lanes.
- Matching a shot destroys the connected group of same-color balls.
- Mismatch places the ball at the front of the lane, increasing pressure.
- After each shot resolves, the field advances based on a stage-specific spawn counter.
- The field only spawns colors that exist in the current ammo pool.
- Lose by either:
  - wall breach (any ball reaches the wall), or
  - out of ammo before the score goal is reached.

## MVP Scope

This repository is currently aimed at a continuous tuning prototype rather than full meta progression.

- 4 lanes × 4 colors
- finite, shuffled ammo pool per stage
- randomized stage parameters within developer-set ranges
- self-looping run: win or lose triggers a fresh randomized stage
- tuning harness displays current stage values for feel-based balancing
- no persistent progression, shop, bosses, or monetization are implemented in MVP

## Project Structure

- `project.godot` — Godot project configuration
- `scenes/` — main game scenes, including `Main.tscn`
- `assets/` — imported art assets
- `documents/gdd/` — game design documents describing concept, mechanics, controls, scoring, and MVP scope

## How to Open

1. Install Godot 4.6.
2. Open this folder in Godot.
3. Load `project.godot`.
4. Run the main scene or inspect the project structure.

## Notes

- The design is based on the GDD files found in `documents/gdd/`.
- This README is intended as a GitHub-facing summary of the current game vision and prototype direction.

## License

Add your preferred license here.
