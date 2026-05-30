# Rocky Idle Plugin Manager

![Rocky Idle Plugin Manager](social-preview.png)

Plugin manager for the Steam game **Rocky Idle**. Updated for the **May 2026** game build (`index-CVsOJkcy.js` and related bundles).

## Repository layout

| Path | Purpose |
|------|---------|
| `Rocky Plugin Manager/RPM.exe` | Plugin manager (run this) |
| `Rocky Plugin Manager/plugins/` | Your local install folder — copy `.plugin` files here |
| `plugins/` | Standard plugins |
| `plugins/cheats/` | Cheat-style plugins |
| `plugins/utility/` | Utility plugins |

Typical install folder:

```
Rocky Plugin Manager/
├── RPM.exe
├── state.json          (created after first use)
└── plugins/
    ├── kill_tracker.plugin
    ├── multi_skill.plugin
    └── …
```

## Setup

1. Download or clone this repo.
2. Copy `.plugin` files from **`plugins/`**, **`plugins/cheats/`**, or **`plugins/utility/`** into `Rocky Plugin Manager/plugins/`.
3. Run `Rocky Plugin Manager/RPM.exe`.
4. Click **Locate Game Folder** and select your Rocky Idle install (e.g. `Steam/steamapps/common/Rocky Idle`).
5. Click **↓** on a plugin to install, **↑** to uninstall.

Only install plugins you want — each one patches or injects into the game when enabled.

## After Rocky Idle updates

Game updates change minified JS bundles and can break plugins until they are updated.

1. Open RPM.
2. **Uninstall** affected plugins.
3. If the game was verified/reinstalled, grab the latest `.plugin` files from this repo.
4. **Install** again.
5. Fully restart Rocky Idle.

Uninstall → reinstall is the safest way to re-apply patches cleanly.

---

## Standard plugins (`plugins/`)

| File | What it does |
|------|----------------|
| `autoplanter.plugin` | **AP** toggle on one bush/tree card at a time — auto-claims finished runs and replants that crop. **Keep the Farming runs tab open** while AFKing; best for a single bush/tree session, not offline automation. |
| `auto_boost.plugin` | Auto-clicks combat and skilling boost buttons when off cooldown. |
| `buyable_keys.plugin` | Adds Easy, Medium, Hard, and Expert keys to the **Other** shop — matching contract + 1M / 5M / 12M / 25M gold. |
| `kill_tracker.plugin` | Kill counter and kills/hr for your current combat session (panel under combat UI). |
| `multi_skill.plugin` | Combat and skilling at the same time — start combat first, then start a skill. |
| `offline_infinity.plugin` | Removes the 24-hour offline progress cap; offline UI shows infinity. |
| `osrs_scythe.plugin` | Adds **Scythe of Vitur** (2× Stingar hammer stats, 2.00 attack speed, 120 Melee req). Craft in **Assembling**: 4× Stingar hammer → 1 scythe. |
| `slayer_auto_task.plugin` | **Repeat task** row under Expert in Slayer Difficulties; when on, finishing a task re-assigns the same master and length. |
| `slayer_point_rebalance.plugin` | Slayer Buy (except Auto Eat) and Offline unlock costs ÷10; Extend task costs 75% off. |
| `supply_timer.plugin` | Estimates time until runes, arrows, food, or boost run out — KC-style panel below combat attack bars (days/hours). |
| `toaster_tracker.plugin` | Tracks XP from toast popups; shows per-skill XP/hr and total XP/hr panel. |
| `tree_boost_burn.plugin` | Bush/tree run timers reduced by 2% per skilling boost tier (max 80% at tier 40). |
| `mode_1daat.plugin` | Changes the Countryside mode badge text to **1DAAT**. |

> **Note:** `toaster_tracker.plugin` replaces the old `xp_tracker.plugin` (removed).

---

## Cheat plugins (`plugins/cheats/`)

Use at your own discretion — these significantly affect progression.

### Boost multipliers

Install **only one** multiplier at a time. Uninstall the current one before switching.

| File | Effect |
|------|--------|
| `boost_multiplier_2x.plugin` | Active skilling boosts (Speed, Batch) ×2 |
| `boost_multiplier_5x.plugin` | Active skilling boosts ×5 |
| `boost_multiplier.plugin` | Active skilling boosts ×10 |
| `drop_multiplier_5x.plugin` | Monster kill drops ×5 (quantities and drop rolls) |

### Other cheats

| File | What it does |
|------|----------------|
| `1_minute_farming.plugin` | All bush/tree farming runs complete in 1 minute. |
| `inf_boost.plugin` | Infinite boost duration (**Perma**), no cooldown — auto-activates on install; fully restart the game after installing. |

---

## Utility plugins (`plugins/utility/`)

| File | What it does |
|------|----------------|
| `devtools.plugin` | Re-enables Developer Tools (F12 / Ctrl+Shift+I). |

---

## Removed plugins

These are no longer in this repo:

- `xp_tracker.plugin` → use **`toaster_tracker.plugin`**
- `skill_stars.plugin` → removed
- `slayer_auto_task_legit.plugin` → replaced by **`slayer_auto_task.plugin`** (repeat toggle, no forced 250 kills)
- `contract_buyout.plugin` → removed (broken on current game build)
- `60secondfarming.plugin` → renamed to **`1_minute_farming.plugin`**

---

## Links

- [GitHub repository](https://github.com/TheFootDev/RockyIdlePluginManager)
- Rocky Idle on [Steam](https://store.steampowered.com/app/2920300/Rocky_Idle/)
