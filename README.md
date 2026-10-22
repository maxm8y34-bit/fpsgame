# Shadow Strike

Shadow Strike is an offline, single-player browser FPS built with Three.js. It uses procedural 3D geometry and Web Audio synthesis, so it has no external art, audio, account, or network-service requirement after dependencies are installed.

## Run

```powershell
npm.cmd install
npm.cmd run dev
```

Open the local URL printed by Vite (normally `http://127.0.0.1:5173`). For a production build run `npm.cmd run build`.

## Controls

| Control | Action |
| --- | --- |
| Mouse | Aim / fire |
| WASD | Move |
| Shift | Sprint |
| Ctrl | Crouch / slow walk |
| Space | Jump |
| 1–3 | Select loadout weapon |
| R | Reload |
| Q | Inspect weapon |
| Esc | Pause |

Click the game view to lock the mouse. The first click also enables browser sound.

## Included systems

- Three distinct procedural maps: Cargo, Industrial, and Desert Outpost.
- First-person controller with pointer lock, sprint, crouch, jump, gravity, wall collision, sway, bob, recoil, and HUD.
- Ten original procedural multi-part weapon designs, including rifle, AK-style rifle, SMGs, shotgun, sniper, pistols, knife, and dagger.
- Hitscan combat, headshots, mags/reserves/reload, tracers, impact feedback, respawns, kill feed, TDM, FFA, Practice, and offline Ranked.
- Visible procedural humanoid bots with difficulty-dependent reaction/accuracy, line-of-sight checks, last-seen search, patrol/chase/attack states, cover-aware waypoint selection, reloads, respawns, and team logic.
- Persistent local progression: XP, level, credits, service record, rank rating, inventory, equipped finishes, loadout, and settings. Ranked offers 1v1 and 2v2 offline formats, both first to six eliminations. Save data is versioned and safely falls back to a default state if invalid.
- Four functional case types, probabilistic rarity system, reward reel tied to the actual saved reward, skins, inventory filtering, skin inspection/equipping, weapon loadout, settings, and owner-local admin tools.
- Procedural Web Audio UI, firing, hit, jump, and result sounds; volume controls apply immediately.

## Local owner panel

Admin is intentionally a local development feature; it can change credits, XP, cosmetic ownership, and reset progress. It is not authentication or multiplayer anti-cheat.

## Asset attribution

No third-party art, model, image, font, or sound assets are bundled. All visuals are created with Three.js primitives and all sounds are generated through the Web Audio API.

## Verification performed

- Production bundling with Vite.
- Build-time module resolution check.
- Browser gameplay interaction has not been verified in this environment.

## Known limitations

- Bots use lightweight cover-aware waypoint navigation rather than a baked NavMesh, keeping the project compact and allowing all maps to remain procedural.
- This release is deliberately offline versus AI; it contains no networking, matchmaking, or server-side anti-cheat.
