# Meaningless-vibe-code-project-2 

**Project Codename:** Meaningless Vibe Code Project 2

A single-stage, browser-based retro run-and-gun action tribute inspired by the 1992 SNES classic *Contra III: The Alien Wars*. Built as a self-contained single-file HTML5 Canvas 2D arcade experience with original procedural pixel art and synthesized Web Audio API sound effects and music.

---

## Gameplay Features

- **Complete Single-Stage Urban Warzone:** Battle through 5 escalating zones of an occupied futuristic city (4224px scrolling stage) with 3-layer parallax scrolling, elevated one-way platforms, destructible barricades, and explosive barrels.
- **Responsive Commando Controls:** Fast horizontal movement, crisp arcade jumping, drop-through platforms (`Down + Jump`), and full **8-directional aiming** with optional stationary Aim-Lock (`Shift`).
- **Dual Weapon System:** Carry two weapons simultaneously and swap on the fly (`K`) without losing upgrades:
  - **Assault Rifle (`AR`)** — Reliable rapid-fire starter weapon.
  - **Spread Gun (`S`)** — 5-pellet wide fan burst.
  - **Laser (`L`)** — High-velocity piercing beam.
  - **Homing (`H`)** — Auto-tracking missiles.
- **Special Abilities:**
  - **Spin-Jump Attack (`L`)** — Airborne 360° dual-weapon radial barrage on a cooldown.
  - **Screen-Clearing Bomb (`I`)** — Limited-use explosive blast that clears enemy projectiles and deals heavy area damage.
- **Enemy Archetypes:** Infantry troopers, aggressive Jumping Aliens, sine-wave Flying Drones, and heavily armored Troopers.
- **3-Phase Boss Encounter — THE BIO-MECH COLOSSUS:**
  - *Phase 1 (Suppression):* Shoulder turret volleys and mortar arcs with telegraphed flashes.
  - *Phase 2 (Core Exposure):* Vulnerable glowing core weak point, sweeping charge laser, and alien reinforcements.
  - *Phase 3 (Final Assault):* Overloaded rapid attacks and telegraphed falling debris leading to a chained-explosion defeat sequence and Stage Clear screen.
- **Retro Audio Engine:** Original Web Audio API synthesized sound effects and a 145 BPM chiptune action soundtrack with volume slider and mute toggle.
- **Difficulty Modes & UI:** Easy, Normal, and Hard difficulties, Title screen, Controls modal, Pause menu, Game Over, and Stage Clear summary.

---

## Controls

| Action | Keyboard |
|---|---|
| Move Left | `A` / `Left Arrow` |
| Move Right | `D` / `Right Arrow` |
| Aim Up | `W` / `Up Arrow` |
| Aim Down / Crouch | `S` / `Down Arrow` |
| Jump / Drop Through | `Space` (`S`/`Down` + `Space` to drop) |
| Shoot (hold for auto-fire) | `J` |
| Switch Weapon | `K` |
| Spin-Jump Attack | `L` |
| Bomb | `I` |
| Aim-Lock (stationary aim) | `Shift` |
| Pause / Resume | `Escape` |

- **Gamepad Support:** Basic Gamepad API support is included for standard controllers.
- **Touch Controls:** A toggleable on-screen touch overlay is available via the `TOUCH` button for mobile/tablet browsers.

---

## How to Run Locally

No build tools, package managers, or server required:

1. Clone or download this repository.
2. Open `index.html` directly in any modern desktop browser (Google Chrome, Microsoft Edge, or Mozilla Firefox).
3. Click **START MISSION** to initialize audio and begin playing.

---

## Browser Compatibility

- **Primary:** Google Chrome, Microsoft Edge, Mozilla Firefox (desktop).
- **Secondary:** Mobile browsers via the built-in `TOUCH` overlay.

---

## Technical Architecture

The entire game lives inside a single self-contained `index.html` file with zero external dependencies:

- **Rendering:** 384×216 logical HTML5 Canvas 2D (`imageSmoothingEnabled = false`, pixelated CSS scaling) with procedural pixel-art sprites, hit-flashes, muzzle flashes, multi-frame explosions, screen shake, and floating score popups.
- **Loop & Physics:** `requestAnimationFrame` with a 60 Hz fixed-timestep simulation (`dt = 1/60`) and clamped frame deltas.
- **Audio:** Real-time Web Audio API synthesis (oscillators, noise buffers, filters, and lookahead BGM sequencer).

---

## Known Limitations

- Single-player only (no 2-player co-op).
- Single stage demo (Stage 1: Occupied Futuristic City); overhead stages and full campaign are intentionally out of scope.
- Key remapping is not currently implemented; default keyboard bindings are fixed.

---

## Acknowledgement

This project is deeply inspired by **Contra III: The Alien Wars** (1992), originally created, developed, and published by **Konami** for the Super Nintendo Entertainment System (SNES). We do **not** claim ownership of the original game concept, run-and-gun design identity, or any intellectual property belonging to Konami. All credit for the original game idea and classic inspiration goes to Konami and the original *Contra III* development team.

---

## Fan-Project Disclaimer & Copyright Attribution

This project is an **unofficial, non-commercial fan-inspired homage** to *Contra III: The Alien Wars* (1992, Konami). It is not affiliated with, endorsed by, or associated with Konami Digital Entertainment Co., Ltd.

All code, procedural pixel art, visual effects, sound effects, and synthesized music in this repository are **100% original creations**. No original Konami source code, ROM data, sprites, backgrounds, or audio recordings are used or distributed.

Licensed under the [MIT License](LICENSE).
