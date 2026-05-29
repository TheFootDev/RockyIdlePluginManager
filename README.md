# (OUTDATED)Rocky Idle Plugin Manager

![Rocky Idle Plugin Manager](social-preview.png)

Plugin manager for the Steam game **Rocky Idle**. Updated for the May 2026 game build.

## Repository layout

- `Rocky Plugin Manager/` — app folder (run `RPM.exe` from here)
- `Rocky Plugin Manager/RPM.exe` — plugin manager executable
- `Rocky Plugin Manager/plugins/` — drop `.plugin` files here for the app to load
- `*.plugin` at repository root — normal plugins (easy download)
- `Cheats/` — cheat-style plugin builds

## Setup

1. Download the **`Rocky Plugin Manager`** folder (or clone this repo).
2. Download `.plugin` files from the repo root (normal) or from `Cheats/` (cheaty).
3. Put those `.plugin` files into `Rocky Plugin Manager/plugins/`.
4. Run `Rocky Plugin Manager/RPM.exe`.
5. Click **Locate Game Folder** and select your Rocky Idle install.
6. Install plugins from the manager.

## After Rocky Idle updates

1. Open the manager.
2. Uninstall affected plugins.
3. Install them again.

Uninstall and reinstall is the safest way to re-apply patches after game file changes.

## Plugins

- `auto_boost.plugin` — Auto-clicks combat and skilling boost buttons when available.
- `kill_tracker.plugin` — Combat session KC gained and KC per hour.
- `multi_skill.plugin` — Combat and skilling at the same time (start combat first).
- `offline_infinity.plugin` — Removes the offline 24-hour cap; labels show infinity.
- `slayer_auto_task.plugin` — Repeat task toggle under Expert; re-assigns the same task on completion.
- `toaster_tracker.plugin` — Per-skill and total XP/hr from in-game toasts.
- `tree_boost_burn.plugin` — Faster bush/tree actions when skilling boosts are high.
- `mode_1daat.plugin` — Changes the displayed mode to 1DAAT.

## Cheaty plugins

### Multiplier cheats

1. Pick **one** boost multiplier variant (`2x`, `5x`, or `10x`).
2. Install and enable only one multiplier at a time.
3. When switching, uninstall the old one first.

- `60secondfarming.plugin` — Forces bush/tree farming run timers to 60 seconds.
- `boost_multiplier_2x.plugin` — Multiplies active skilling boosts by 2x.
- `boost_multiplier_5x.plugin` — Multiplies active skilling boosts by 5x.
- `boost_multiplier.plugin` — Multiplies active skilling boosts by 10x.
- `contract_buyout.plugin` — Buy out contracts for coins (Easy 1m … Expert 10m).
- `devtools.plugin` — Enables devtools in the game client.
- `inf_boost.plugin` — Removes boost cooldown; keeps boosts running (Perma).
- `slayer_point_rebalance.plugin` — Lowers slayer shop/offline point costs.

Some plugins are cheaty. Use inf boost and multipliers only if you want a much faster run — they shorten the game significantly.

## Building from source (developers)

Source lives in the separate dev tree (`plugins/` folders). To rebuild GitHub release assets:

```powershell
python tools/build_github_release.py
```

That packs `.plugin` archives and copies `RPM.exe` into this repository layout.
