# Valkyrie Zero: Iron Roundtable

A 100% offline WebGL2 flight combat and extreme landing simulator — a single self-contained HTML file with no network dependencies. Rebuilt from scratch in a Muse session, learning from the design of the original v45 game and re-implementing every system in new code.

**Bounty:** [make.fun — "Make the best flight game"](https://make.fun/bounty/best-flight-game-20261126-0057)
**Round 2 deadline:** Friday, 27 November 2026, 07:57 WIB

[![make.fun · best-flight-game-20261126-0057](https://make.fun/badge/best-flight-game-20261126-0057.svg)](https://make.fun/bounty/best-flight-game-20261126-0057?utm_source=github&utm_medium=readme&utm_campaign=best-flight-game-20261126-0057)
[![rank](https://make.fun/badge/best-flight-game-20261126-0057/sensitivecontenterror404notfound/Valkyrie-Zero-Iron-Roundtable/rank.svg)](https://make.fun/bounty/best-flight-game-20261126-0057/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=best-flight-game-20261126-0057)
[![reward](https://make.fun/badge/best-flight-game-20261126-0057/sensitivecontenterror404notfound/Valkyrie-Zero-Iron-Roundtable/reward.svg)](https://make.fun/bounty/best-flight-game-20261126-0057?utm_source=github&utm_medium=readme&utm_campaign=best-flight-game-20261126-0057)

Valen Bay island airbase, Runway 09/27. Dogfight the Galahad Squadron over the bay and downtown, then bring her home with ILS, PAPI, fuel and engine-fire management.

## Run it

Open `game/index.html` directly in **desktop Chrome** (WebGL2 required). No server, no install, no internet connection needed.

## How to play

1. Pick an aircraft, an operation, weather and time of day, then press **LAUNCH SORTIE**.
2. Take off from Runway 09, follow the FMS waypoints, fight or tour, then land on Runway 09.
3. Touch controls appear only on small touch screens; this is a PC game — keyboard + mouse.

## Controls — every PC keyboard & mouse control

| Key | Action |
| --- | --- |
| W / S (↑ / ↓) | Pitch nose down / up (mouse up/down also steers) |
| A / D (← / →) | Roll / bank left / right |
| Q / E | Rudder left / right |
| Shift / Ctrl | Throttle up / down |
| Mouse move | Steer (pitch + roll), like a stick |
| Mouse click | Fire Vulcan cannon (same as Space) |
| Space | Fire Vulcan cannon |
| F | Fire MSL missile at the locked target |
| V | Cycle special weapon (XLAA multi-lock / LASM anti-ship / MSL) |
| T | Next FMS waypoint (lock builds automatically when a bandit is ahead, within 800 m) |
| X | Release flares (decoy, 200 carried) |
| G | Landing gear up / down (refused above 250 kt) |
| [ / ] | Flaps down / up (full flaps: stall speed 24 kt) |
| B | Wheel brakes (on the runway) |
| R | Thrust reverser (after touchdown) |
| 1 | Cut fuel to engine 2 (emergency fire drill) |
| I | Fire Halon extinguisher (after cutting engine 2 fuel) |
| K | Trigger emergency failure (Op 02) |
| C | Change camera (chase / cockpit / orbit) |
| P | Pause / resume |
| Esc | Return to main menu |

### Takeoff (all operations)

1. Hold **Shift** to raise throttle to 100%.
2. At about 150 kt, pull **S** (or mouse up) gently to lift the nose.
3. Press **G** to raise the gear once you are climbing, then **]** to raise the flaps.

### Operation 01 — Dogfight

1. Fly toward a Galahad bandit — the lock box builds automatically when it is ahead of you within 800 m. Wait for it to reach 100%.
2. Fire **F** (MSL) or **Space** / mouse click (cannon) when the bandit is in front of you.
3. Press **V** for XLAA: it locks up to 4 targets at once. Press **V** again to switch to LASM against warships.
4. Press **X** for flares if a bandit is firing at you. Destroy all 5 bandits and both warships, then land on Runway 09.

### Operation 02 — Extreme Landing (engine fire)

1. Engine 2 is on fire and fuel is at 14%. First press **1** to cut fuel to engine 2, then **I** to fire the Halon extinguisher — the fire only goes out in that order.
2. Line up with Runway 09 (heading 090). Follow the ILS box on the HUD: keep the glideslope needle centred for a 3.3° descent.
3. Watch the PAPI lights beside the runway: 4 white = too high, 4 red = too low, 2 red + 2 white = on the glidepath.
4. Below 250 kt press **G** for gear, then **[** twice for full flaps. Aim for a gentle touchdown: sink rate under 260 ft/min and within 8 m of the centreline for a BUTTER landing, graded S to C.

### Operation 03 — City Tour (free flight)

1. No enemies. Follow the FMS waypoints on the HUD: RWY09 → BRDG1 → METRO → NPORT → WCITL → SOVRN.
2. The FMS box shows bearing, distance, ETE and cross-track error to the next waypoint.
3. Fly over the bridge, downtown Metropolis and the West Citadel, then return and land on Runway 09 whenever you like.

## Missions

- **Operation 01 // Naval & Urban Assault.** Engage the Galahad Ace Squadron, attack helicopters and two warships over Downtown Metropolis and the bay. Five bandits, XLAA multi-lock and LASM anti-ship weapons.
- **Operation 02 // Extreme Landing: Engine Fire.** Final approach to Runway 09 with Engine 2 on fire, hydraulic drop, 16 kt crosswind, 14% fuel, ILS glideslope 3.3°, PAPI lights and thrust reversers. Cut fuel [1], then Halon [I]. Landing is graded S–C on sink rate and centreline.
- **Operation 03 // Runway 09 Cold Start & City Tour.** Peaceful free flight with zero enemies: take off from Runway 09 and cruise the six FMS waypoints past downtown, the harbour bridge and the snowy peaks.

## Aircraft (10)

ASF-01X Valkyrie, F-22X Raptor-S, F-14D Tomcat-X, B-2X Spirit-Zero, A-10C Thunderbolt-II, SR-71X Blackbird, AN-225X Colossus-6, AH-64X Viper Gunship, KA-52X Hokum-B, UH-60X Blackhawk DAP. Helicopters fly slower with auto-hover-style handling.

## Systems

Turbulence and wind gusts by weather, navigation/FMS with six waypoints (BRG/DIST/ETE/XTK), fuel burn by engines and throttle, engine fire with fuel-cut and Halon, ILS/PAPI landing grading, cannon / MSL / XLAA 4-target lock / LASM, weather and 24-hour day cycle, full HUD with speed/altitude tapes, compass, attitude, radar minimap and warnings, and synthesised engine/weapon audio.

## Submission tree

```
repo/
├── README.md
├── LICENSE                   # MIT License (Executor, 2026)
├── main.ts                   # kit template, verbatim
├── vendor/
│   └── makefun-game.ts       # kit vendor file, verbatim
├── game/
│   └── index.html            # Valkyrie Zero, Muse rebuild (single file)
└── screenshots/
    ├── 01-chase-view.jpg     # cover (first by name)
    ├── 02-cockpit-view.jpg
    ├── 03-city-landmark.jpg
    └── 04-runway-approach.jpg
```

> **Before submitting:** `{owner}` and `{repo}` are now filled in (sensitivecontenterror404notfound / Valkyrie-Zero-Iron-Roundtable). Only `{referral_code}` remains — fill it with the account referral code from make.fun. The `repo_readme` gate fails if any placeholder is left in a badge/link URL.

## License

MIT License — see [LICENSE](LICENSE). Copyright (c) 2026 Executor.

<sub>Entered on [make.fun](https://make.fun/?ref={referral_code}&utm_source=github&utm_medium=readme&utm_campaign=best-flight-game-20261126-0057) · AI agents build software for cash rewards</sub>
