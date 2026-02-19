# RSL Helper Sellfile Creator

Build, preview, and export sell rules for RSL Helper with a simple UI.

> This is an independent, fan‑made tool. Not affiliated with Plarium, Raid: Shadow Legends, or RSL Helper. Trademarks belong to their owners.

## Features
- Build rules and save them: create recipes and keep a library you can reuse.
- Sellfile Preview toggle: flip between the Rules table and the Rule Tester table right from the header. Counts/outcome chips adapt (Keep/Sell for rules, Matched/No Match for tester) and the filters follow whichever table you pick.
- Drag & drop or Load button: drop `.sfr`, `.hsf`, or `.db` anywhere (overlay confirms) or click “Load RSL Helper Sellfile”. Both options behave the same — `.sfr` replaces your builder, `.hsf` layers on the optional base sellfile, and `.db` dumps go straight into the Rule Tester queue without touching the builder.
- Metasets: name groups of gear sets (e.g., Speed + Perception) and reuse them across rules.
- One-click Export: export an HSF file (the RSL Helper Sellfile) ready for RSL Helper.
- Logic Hub button (`Logic Hub`): open the dialog from the preview header to reach `Final Sell`, `Safeguards`, `Dungeon Drops`, and the Gear dialog (Logic Hub → Gear tab) from the same place. Load example gear, paste drops, or drag `%APPDATA%\\RslHelper\\Config`, then close the dialog and leave the preview toggle on whichever table you need — the tester queue stays visible without reopening.
- Safeguards tab: define combinations you never want to lose, and the scanner injects keep rules automatically whenever your recipes plus your current active Sell rules would sell every piece in that combination.

## How To Use

### Recipe File
- SFR (`.sfr`): your project file for this app. Think of it like a save file you can load/share. RSL Helper does not read SFR directly.
- HSF (`.hsf`): the RSL Helper Sellfile. Export from this app, then load it in RSL Helper.
- Saved filename defaults to `SellfileCreatorRecipes_YYYYMMDD_HHMM.sfr`.

### Recipe Builder
- Fill in the Recipe Builder and give your recipe a clear name.
- Click “Add as new recipe” to save it; then click the saved entry in the list below the builder to select it for editing and update it.
- Load/Save: Use “Load Recipes” and “Save Recipes” to reuse your custom rules. These actions save everything needed to rebuild what you see in the preview into a recipe file.
- Reset/Insert/Apply menus: Right-click Reset, Insert as recipe, or Apply as recipe to open the shared options menu. Save your current builder state as the default template, jump back to the factory defaults, enable Auto reset after Insert (clear the builder immediately after inserting a recipe), or enable Auto apply to selected recipe (push edits into the highlighted recipe automatically after ~400 ms of inactivity). Auto reset and Auto apply cannot be on at the same time—turning one on turns the other off—and both preferences persist between sessions.
- Note: Click “Add Note…” (or “Edit Note…”) to attach a note to your recipe file. The note is shown automatically after loading a recipe file that contains one. Use `<!-- recipes:1,0 -->` to drop chips for specific recipes (0 continues to the next one). Use `<!-- recipes-re:"speed" -->` to show every recipe whose name matches the case-insensitive pattern.
- Autosave restore: On launch, the dialog lists every autosaved section with its own checkbox. Restore only what you need — recipes (including the selected chip), metasets, Substat Target Values, Final Sell remainder, the pinned note, the filter panel (open state, chips, collapsed sections), and any Rule Tester imports. Leave a box unchecked to keep your current work untouched. Autosave also remembers which Final Sell toggles (Artifacts, Accessories, and level ranges) were enabled, so reopening Logic Hub mirrors exactly what you exported last time.

### Builder layout (top → bottom)
- Action & Enable: Tell the Sellfile what should happen when an item matches the recipe.
  - `Keep` marks matching gear as Keep so RSL Helper ignores it.
  - `Sell` marks matching gear as Sell so RSL Helper queues it for auto-sell.
- The Enabled toggle decides whether rows from this recipe are active when exported. Disabled recipes are shown struck through in the preview and have no effect in RSL Helper; enable "Omit disabled rules when exporting" from the export menu if you want to drop them entirely.
- Rank: Limit the rule to specific star ranks. Use `Any` when every rank should stay eligible.
- Levels: Choose the earliest and latest upgrade milestones the rule should cover. Milestones follow game levels: +0, +4, +8, +12, +16. Rows are emitted only inside this window.
- Rarity: `Auto` (recommended) picks the lowest rarity that still makes your picks possible at the selected levels.
  - No per-stat mins or global roll minimums? Auto keeps the rule broad so every rarity stays valid.
  - Asking for 1/2/3/4 starting substats? Auto guarantees the chosen rarity can spawn with that many (1→≥Uncommon, 2→≥Rare, 3→≥Epic, 4→≥Legendary).
  - Requiring specific roll counts? Auto chooses the lowest rarity that can reach that many rolls by +16, including Mythical for five rolls.
- `Auto ≥` chip (under Milestone Thresholds): raise the floor so Auto never drops below that tier and, with Late thresholds, adds bonus ≥ branches at +4/+8/+12.
    - Tap to cycle: Uncommon → Rare → Epic. For example, “Auto ≥ Rare” keeps Uncommon out of the rule.
    - The chip only turns on when Rarity is Auto and Milestone Thresholds are set to Late. Otherwise it shows a diagonal slash.
    - Example: Banner with SPD and ATK% where ATK% needs 2 rolls. Set Rarity = Auto, Milestone Thresholds = Late, Auto ≥ Epic. The builder keeps Epic rows for every milestone and adds ≥ Legendary branches at +8 and +12 so rarer gear stays eligible without relaxing the Epic timing.
  - Before +16, the builder uses whichever substat count the rarity can actually have at that milestone. At +16 it always enforces your requested count.
- Faction: Restrict accessory rules to a specific faction when you are targeting a single team. Rings, Amulets, and Banners obey this filter; armor pieces ignore it, so `Any` keeps armor safe.
- Slots: Focus the rule on certain gear pieces (Weapons, Boots, etc.) so off-slot drops do not match. Leave it empty to cover every slot.
- Sets & Metasets: Filter the rule to explicit gear sets or named Metasets so only those collections pass. Leaving it empty keeps every set eligible.
- Mainstat row: Require particular main stats.
  - Select multiple to accept any of them. Leaving it empty means any main stat passes.
  - Choosing several main stats generates one rule per main stat so each remains explicit in the export.
- Substats row: Tell the builder which substats matter.
  - Click to select (or click again to clear) a substat. Locked picks use the badge beside the label and always appear in the generated rows.
  - Use the lock badge (🔒) to require the stat. Right-click a selected substat to open quick actions for locking/unlocking and roll targets.
  - `Any` is a shortcut back to “no restrictions”. Picking specific substats automatically turns `Any` off.
  - The total substats per row is `max(required count, locked count)` capped at four, so locking a stat guarantees space for it.
- Flex toggle: When you have more optional picks than the Required count, Flex rotates those extras across permutations so every valid mix appears. Locked picks stay fixed, and the toggle disables itself when there’s nothing to rotate.
- Roll indicator: Each selected substat shows a round indicator for upgrade rolls.
  - Left-click raises expectations; Right-click lowers them.
- Starting from ★: Left switches to a green minimum (0→1→…→5) and Right switches to a red Roll Upper Limit (0→1→…→4).
- On a Roll Upper Limit, Left lowers the limit (1→0→★) while Right raises it (0→1→…→4→★).
- Green numbers show minimum rolls you insist on; red numbers enforce the upper limit above that value. Min and the Roll Upper Limit are mutually exclusive.
- Roll Targets (Base/+1…+5): Right-click a selected substat to open the Roll Targets grid. Base captures the +0 value, and each +N input tracks the value after that many extra rolls. Leave a cell blank to reuse your Substat Target Values, or click “Use global substat targets” to revert any overrides back to those values. The preview chips update immediately so you can confirm the numbers before exporting.
- Required substats: Choose how many of your selected substats must be present on the item for the rule to pass.
  - `Auto` keeps the count in sync with the number you selected (up to four).
  - Locked substats (🔒) always count toward the requirement, and warnings flag impossible combinations (for example, locking more than four stats).
- Min Required Rolls (global): Set the total number of rolls your selected or locked substats must share. `0` skips the aggregate check. Auto keeps the total aligned with your required substats when two or more are tracked, and caps it at what the current rarity can roll; single-stat recipes stay at zero. Early milestones list any splits that can still hit that target by +16.
- Locked Min Required Rolls (🔒) appears when at least one substat is locked. Click a number in the lock row to reserve that many rolls for the locked stats only; the rest of the builder keeps following the global minimum. If the lock equals or exceeds the highlighted global number, the global badge clears so the lock becomes the only aggregate floor. Unlocking the substat (or tapping Auto) clears both badges; picking a smaller global value re-lights the global badge alongside the lock so you can see which floor applies to which stats.
- Example: Lock SPD and CR%, set Min Required Rolls = 3, then set the 🔒 row to 2. The builder now needs 3 total rolls across every selected substat, at least 2 of which must land on the locked SPD/CR% picks. Lock = 3 automatically clears the global badge because both floors would be identical.
- Milestone Thresholds: Decide how per-stat minimums behave before +16 once you ask for roll minimums.
  - `Early` tracks the rolls you already have at each milestone.
  - `Late` only demands what must be present now so the +16 goal stays achievable.
  - The toggle matters only when any substat has Min > 0 or the global minimum is above 0.

### Levels & Rolls: Quick Guide
- Early thresholds: When you set per‑stat mins or an aggregate Min Required Rolls, thresholds rise until feasible and then remain fixed; once feasible, rows collapse to your Substat Target Values and stay fixed.
- Aggregate (Σ rolls): Min Required Rolls applies to the sum of rolls across your selected substats by the target level.
- Wildcards with Min Required (sum‑of‑rolls): With only starred substats (★) and Min Required > 0, Early shows just the minimal splits at each milestone (keeps lists small and stable). Late repeats the same minimal splits at the early milestones and again at +16.
- Mythical (5 rolls): Mythical can reach 5 rolls in a substat by +16 (vs 4 otherwise). When your Rarity selection includes Mythical, the generator accounts for its pre‑roll. With Rarity = Any, setting Min Required Rolls to 5 (or per‑stat mins summing to 5) is treated as Mythical‑capable and also accounts for a pre‑roll at +0.

### Substat Target Values
- Open via the “Substat Targets…” button in the top‑right of the builder — it launches the Substat Target Values dialog.
- Global: These values apply to every recipe, not just the one currently selected.
- The builder uses them to compute thresholds at each level range (0–3, 4–7, 8–11, 12–15, 16) and as the fallback in the Roll Targets grid.
- Use “Reset to defaults” inside the dialog to restore the recommended values.

### Metasets
- Click “Manage metasets…” in the Sets row to open the dialog.
- Add or rename metasets and choose which sets each one contains. The dialog uses the same search and view modes as the Sets picker.
- Starter metasets are included so you can begin right away. You can edit or remove them at any time.
- “Reset to defaults” (in the dialog) offers safe options when metasets are in use:
  - Delete and remove references, or
  - Replace each use with that metaset’s explicit sets, or
  - Replace references with another metaset.

### Final Sell
- Use the `Final Sell` toggle in the preview header to add catch-all Sell rules for items not matched by your Keep rules. The label never changes; an amber fill means it is active, and the neutral outline means it is off.
- Click the `Logic Hub` button next to the toggle to open the `Final Sell` tab and choose whether it covers Artifacts, Accessories, and which level ranges (0–3, 4–7, 8–11, 12–15, 16). The defaults cover 0–15 so fully leveled gear stays safe unless you turn `+16` on.
- Without Final Sell, items that do not match any rule are automatically kept by RSL Helper. Selling only happens when a Sell rule matches.
- When `Final Sell` is active, the generated Sell rules explicitly include all currently known sets. In the preview, the Sets column shows “All Currently Known” for these rules to reduce clutter; the exported file still lists every set explicitly.

### Safeguards
- Click `Logic Hub` in the preview header and switch to the `Safeguards` tab to mark the gear combinations you never want to lose. Turn on `Enable Safeguards` to let the scanner add keep rows (edits will also enable it automatically).
- Safeguard rules don’t ‘consume’ items—each rule evaluates the same candidate pool. If a piece matches multiple rules, it counts for all of them.
- Each keep rule lets you pick the slot, sets or metasets, ranks, rarities, main stats, and (for accessories) factions you care about. Leaving a picker empty means “any”.
- `Mode` decides how the rule is emitted: `Off` disables it, `Protect existing` injects keep rows for sold matches until the quota is met, and `Anticipate gaps` also emits placeholder keep rules for missing combinations so new drops stay protected until the DB refreshes.
- Substats are optional: pick one or more to only count items that actually have those substats. The match chip (`Any Substat` / `All Substats` / `Per Substat`) decides whether at least one, all, or each selected substat gets its own quota. Leave it empty to allow any substat.
- Selected substats are always ranked by the normalized substat formula (glyphs ignored); weight controls appear for `Any Substat` and `All Substats`, while `Per Substat` keeps equal weighting (ties at the cutoff stay protected).
- `≥ Required Count` is the promise you want the app to keep. Scope chips directly under each picker (everything except `Rank` and `Rarity`) decide how that quota is split: `Per slot`, `Per set`, `Per faction`, and `Per main stat` can be combined freely. Turning every chip off automatically falls back to the shared `Per rule` pool.
- The info tooltip behind `Required Count` shows the active scope split (`X per slot × per set × ...`) and a simple deficit line (`({missing} missing)`).
- The scanner only adds keep rows for matching items that would otherwise be sold, and only when the quota is not met. In `Anticipate gaps`, placeholder keep rules cover missing combinations.

#### Quota scopes at a glance
Stacking the scope chips changes who gets their own quota. Leave `Per rule` on to share one pool, then layer `Per slot`, `Per set`, `Per faction`, and `Per main stat` to enforce Slot × Set × Faction × Main stat mixes independently.

| Scope button | Quota behavior | When it shines |
| --- | --- | --- |
| `Per rule` | One shared pool for the entire rule. | Keep five SPD boots regardless of set. |
| `Per slot` | Duplicates the quota for each slot. | Keep two rings, two amulets, and two banners independently. |
| `Per set` | Duplicates the quota for each set/metaset in the safeguard. | Track two Stoneskin and two Protection drops separately. |
| `Per faction` | Duplicates the quota for each faction. | Guarantee three Merciless rings for every faction. |
| `Per main stat` | Duplicates the quota for each selected main stat. | Keep separate pools for ACC versus RES banners. |

#### Real-world examples
| Scenario | Filters | Required Count | Scope buttons | What the scanner guarantees |
| --- | --- | --- | --- | --- |
| Running out of SPD boots | Slot = Boots, Main Stat = SPD, Sets blank | `5` | `Per rule` | At least five SPD boots survive, no matter the set. |
| Mixing Savage + Lethal gloves | Slot = Gloves, Sets = Savage + Lethal, Main Stat = CDMG% | `3` | `Per rule` | Three high-damage gloves stay safe even if the set mix changes. |
| Merciless rings per faction | Slot = Ring, Set = Merciless, Faction blank | `3` | `Per faction` | Every faction keeps three of its own Merciless rings. |
| HP% rings per faction | Slot = Ring, Main Stat = HP%, Sets blank | `2` | `Per faction` | Two HP% rings per faction stay in inventory. |
| Core accessories per faction | Three rules (Ring, Amulet, Banner), Sets/Main blank | `5` | `Per faction` | Five Rings, Amulets, and Banners survive per faction. |
| Stoneskin + Protection accessories | Slot = Ring/Amulet/Banner, Sets = Stoneskin + Protection, Main blank | `2` | `Per set` + `Per faction` + `Per slot` | Each faction holds two Stoneskin and two Protection drops for each accessory slot. |
| Fastest SPD accessories | Slot = Ring/Amulet/Banner, Substats = SPD | `5` | `Per rule` | Keeps the top five SPD substat rolls across your accessories (ties included). |
| ACC banners that still roll SPD | Slot = Banner, Main Stat = ACC, Substats = SPD + ACC, Weights favor SPD | `3` | `Per faction` | Each faction keeps the best ACC banners where SPD rolls matter most. |

Tip: Import your `.db` or paste gear into the Gear dialog before opening Safeguards so the scanner sees real items. Click a safeguard rule to highlight matching gear; switch `Filter` to `Selection` to view only those matches.

### Dungeon Drops (Simulator)
Open Logic Hub and switch to **Dungeon Drops**. It simulates dungeon farming using your current Sellfile rules so you can see how much gear you would keep per set and upgrade level.

- Choose a dungeon and stage.
- Simulation mode:
  - `Level-up`: rolls stop as soon as the item would be sold, so results match real leveling.
  - `Snapshot`: rolls always go all the way to +16, even if the item would have been sold earlier.
- The table shows kept drops divided by all drops for that stage at +0 / +4 / +8 / +12 / +16.
- Click a cell for slot + main stat breakdowns, then open **Specific substat odds** for exact substat chances and run estimates.

Notes:
- Uses your current Keep/Sell rules, including Final Sell and Safeguards.
- Runs about 100,000 drops per stage and updates as it runs.
- Drop rates and rolls are simulated, so treat the numbers as estimates.

### Managing Recipes
- Saved recipes list: Each saved recipe appears as a small label below the builder. Use this list to select (left‑click), duplicate, reorder, or delete (deletions are confirmed). “Delete Recipes” removes all (with confirmation).
- Hover linking: Hovering a saved recipe highlights all rows from that recipe in the Sellfile Preview. Hovering a row in the Sellfile Preview highlights the corresponding saved recipe in the list.
- Click linking: Clicking a row in the Sellfile Preview selects its saved recipe (and loads it into the builder). Rows originating from the base `.hsf` do not change the current selection.
- Right‑click menus: On a saved recipe (Duplicate/Move/Copy/Delete) and on the saved recipes area (Copy All, Paste).
- Clipboard fallback: If clipboard access is blocked, a dialog opens with the content pre‑selected — press Ctrl/Cmd+C to copy, or paste into the Paste dialog.

### Sellfile Preview (Rules & Rule Tester)
- The preview header keeps the `Rules`/`Rule Tester` toggle, the “Logic Hub” button, and the “Load RSL Helper Sellfile” button together so you always know where to switch tables or open the Gear dialog (Logic Hub → Gear tab).
- `Rules` view (default): shows every rule that will be exported, including any optional base `.hsf` rows. The header counts stay on Keep vs Sell, the filter row keeps the Any/Only chips for Slot/Rank/Rarity/Level, and both Recipe buttons remain: Preview Recipes controls chip visibility, while the Recipe Filter button is a simple On/Off toggle that hides Sellfile rows outside your selected recipe chips (and keeps that filter staged for when you switch modes).
- `Rule Tester` view: flips the table to the imported gear list so you can scan imported or hand-built items without reopening Logic Hub. Counts/outcome chips switch to Matched vs No Match (and Keep vs Sell) based on first-match results, and the filter row keeps both Recipe buttons side by side: Preview Recipes still controls chip visibility, and the Recipe Filter button expands to a tri-state selector (`Off` → `First-Match` → `Any-Match`) so you can decide how those items respond while continuing to gate Sellfile rows when you jump back. Importing a `.db` automatically switches to this view, but you can jump back to Rules whenever you want.
- The “Load RSL Helper Sellfile” button behaves exactly like drag & drop: `.sfr` replaces the builder state, `.hsf` layers on the optional base Sellfile, and `.db` queue items into the Rule Tester preview (without touching recipes). The “Clear” button detaches the optional base `.hsf`.
- Use the palette icon to open Manage Colors for substat labels.
- In Rules view the table columns still include “Idx” and “Cfg” (empty for base file rows). In Rule Tester view the same space lists slot/set, item stats, and the first matching recipe badge so you can see what would happen to each artifact directly inside the preview.

### Sellfile Preview Controls
- Manage Colors: Click the palette icon above the table to customize text/background colors for substat labels. Use “Reset to defaults” in the dialog to restore recommended colors.
- Filters: Press `Ctrl+F` (`Cmd+F` on macOS) to open the panel and focus the Recipe search instantly. Right-click any section header (or `Ctrl`/`Cmd`+click its chevron) to collapse or expand every section at once. Preview Recipes hides saved-recipe chips that do not match the active filter so the preview stays readable. Recipe Filter controls which recipes are allowed in the table: it’s a simple On/Off toggle in Rules mode, and it cycles through `Off` → `First-Match` → `Any-Match` when the Rule Tester preview is active.
- Column menu: Right-click the table header to open controls:
  - Reset columns: Restore default columns and widths.
  - Auto-fit widths: Fit columns to the viewport.
  - Allow multi‑line rows: Toggle wrapping for Substats and others.
  - Show/Hide columns: Per‑column visibility checkboxes.
- Reorder columns: Drag a header left/right.
- Resize columns: Drag the right edge of a header.
- Click behavior: Clicking a table row selects the related saved recipe (no auto-scroll). Clicking a saved recipe scrolls the table to the first matching row.

### Rule Tester preview
- Click “Logic Hub” in the Sellfile Preview header to open the Gear dialog (Logic Hub → Gear tab). Create example gear or paste items (JSON/text). Items sync to the preview immediately, so closing the dialog does not clear your tester grid.
- Import your RSL Helper gear database by dropping `.db` files onto the app or by using the “Load RSL Helper Sellfile” button (same behavior). Those imports queue thousands of artifacts plus inbox items, switch the preview to the tester table, and keep the builder/export state untouched.
- Each tester item shows slot, set, level, main stat, substats (with glyphs and rolls), the source (inventory vs inbox), and chips for Keep/Sell + the first matching recipe/rule. Disabled rules never match, so “No match” entries represent gear the Sellfile would leave alone.
- The header counts update to show Matched vs No Match totals plus Keep/Sell breakdowns. Combine these totals with the tester filters (Keep/Sell outcome + Matched/No Match + Recipe `First-Match`/`Any-Match`) to focus on edge cases before exporting.
- Use the preview toggle to move between Rules and Rule Tester tables without reopening Logic Hub — great for comparing the generated rule rows against the gear that triggered them.

### Export
- Click “Export merged RSL Helper Sellfile” (or “Export RSL Helper Sellfile” when no base file is loaded).
- Use “Save Recipes” and “Load Recipes” in Add Rules to keep and reuse your work.
- Exported filename defaults to `Sellfile_YYYYMMDD_HHMM.hsf`.

## Examples

Examples below assume 6★ Substat Target Values (per roll unit): SPD=5, CR%=5, CDMG%=5.

**Early vs Late thresholds**
- **Early**: thresholds reflect rolls gained so far. For wildcard + Min Required, it lists the minimal splits at each milestone (stable list). Otherwise it enumerates selected-only progress until the +16 goal is feasible, then collapses to your per-stat targets (unless a global Σ minimum requires more).
- **Late**: demands only what must exist now so the +16 goal stays reachable. For wildcard + Min Required, it repeats the same minimal splits at the early milestones and again at +16. For per-stat targets, it emits the minimal lower bounds per level.

#### Builder scenarios at a glance

| Scenario | Setup | What the builder emits |
| --- | --- | --- |
| Early (2 substats) | SPD min = 2, CR% min = 1, Levels +0..+16 | `+0:` SPD ≥ 5, CR ≥ 5<br>`+4:` [10,5] and [5,10]<br>`+8:` [15,5], [10,10], [5,15]<br>`+12/+16:` [15,10] |
| Late (2 substats) | Same as above | `+0/+4:` [5,5]<br>`+8:` [10,5] or [5,10]<br>`+12:` [15,5] or [10,10]<br>`+16:` [15,10] |
| Early (3 substats) | SPD min = 2, CR% min = 1, CDMG% selected, Required = 3 | `+0:` [SPD,CR,CDMG] ≥ [5,5,5]<br>`+4:` single-roll splits (10/5/5 permutations)<br>`+8:` every two-roll permutation (upper limits respected)<br>`+12/+16:` [15,10,5] |
| Late (3 substats) | Same stats as above | `+0/+4:` [5,5,5]<br>`+8:` [10,5,5] or [5,10,5]<br>`+12:` [15,5,5] or [10,10,5]<br>`+16:` [15,10,5] |
| Lock one, require two | Substats SPD/HP/ATK; lock SPD (🔒); Required substats = 2 | Builder emits SPD+HP and SPD+ATK rows; HP+ATK is excluded because locked SPD must appear in every match. |
| Focus rolls on 3 stats, freeze the flex slot | Substats SPD/CR%/CDMG%/HP%/ATK%/DEF%; Required substats = 4; SPD/CR%/CDMG% get Min Roll = 1; HP%/ATK%/DEF% Roll Upper Limit = 0 | SPD/CR%/CDMG% always receive the rolls while the fourth stat (whichever of HP%/ATK%/DEF% appears) stays at base. Use Roll Upper Limits (Right-click from ★) whenever a stat must never gain rolls. |
| Early with a wildcard | Substats SPD (Min = 2) and ACC (★ wildcard); Required substats = Auto; Levels +0..+16 | Early milestones highlight any gear that can still reach SPD(2) by +16 (rows where SPD or ACC rolled). Once two SPD rolls are feasible, the SPD ≥ row appears. |
| Sum-of-rolls with wildcards | Substats SPD and ACC both set to ★; Required substats = 2; Min Required Rolls = 1 | **Early:** At +4/+8/+12/+16 the grid shows the two minimal splits (SPD ≥ 10 & ACC ≥ 9, plus SPD ≥ 5 & ACC ≥ 18).<br>**Late:** +0/+4/+8/+12 show baseline rows, +16 shows the same two splits. Higher Min Required targets cause Late to demand the necessary total earlier (e.g., with Min Required = 2, +12 displays the single-roll splits and +16 the double-roll splits). |

## Notes for contributors

- Translations: Release zips include localization templates under `i18n/` (e.g., `i18n/en-US.l10n.json`).
- Edit & test: Open the app and drag your edited `*.l10n.json` onto it to apply immediately for the current session (no install needed or possible).
- Submit fixes: Send the updated JSON via Discord message. Keep keys unchanged; missing keys fall back to English.
- Built-in languages: All shipped languages are compiled into the single HTML so the app works fully offline. Your fixes will be integrated into the next release.
- `Stream-Helper-DB-to-Creator.bat` launches the DB watcher and streams the default RSL Helper database into Sellfile Creator to make live recipe checks easier.

## Acknowledgements

Many thanks to **[STBL] Nasgor** for his invaluable contributions,  
to **[SP] Panda** for his sellfiles,  
to **KruYseN** for his gear cleanse videos,  
and of course thanks to **Farbstoff** for RSL Helper!

## Author
Made by [STBL] Nusi㊷  
Localization by [STBL] Nusi㊷

© Nusi㊷ - 2026
