# Sellfile Creator for RSL Helper

Sellfile Creator eases building Sellfiles for RSL Helper — define gear filters by set, slot, main stat, substats, and more, preview matching results live, and export ready-to-use Sellfiles in seconds.

> This is an independent, fan‑made tool. Not affiliated with Plarium, Raid: Shadow Legends, or RSL Helper. Trademarks belong to their owners.

## Features

- **Recipe builder** — create named keep/sell recipes with filters for slot, set, rank,
  rarity, main stat, substats (with roll minimums and targets), faction, and level
  milestones. Build a reusable library and export it as an RSL Helper Sellfile (`.hsf`)
  in one click.
- **Sellfile preview** — preview the generated RSL Helper Sellfile in the Preview tab
  before exporting.
- **Metasets** — group gear sets (e.g. Speed + Perception) into named collections and
  reuse them across recipes and safeguards.
- **Gear Inspector** — connect to RSL Helper for live sync or load a `.db` file to preview
  which items each recipe matches and how many would be kept or sold.
- **Gear Diff** — turn on a before/after view to see exactly which gear pieces flip between
  *keep* and *sell* as you tune recipes or try the dynamic overrides. A chip shows the
  running totals; a side-by-side list shows every piece that changed.
- **Dungeon Simulator** — see keep-chance percentages for Fire Knight, Dragon, and Ice
  Golem across difficulty stages and upgrade levels to confirm the effect of your Sellfile
  when farming or leveling gear.
- **Safeguards** — define slot/set/stat combinations you never want to lose; the scanner
  automatically injects keep rules into the Sellfile whenever your setup would deplete a
  protected combination below its quota.
- **Gear Analytics** — analytics dashboard with KPI cards, crossfilter charts (slot, rank,
  rarity, source, level), a sets treemap, main stat bars, and a substat radar. Click any
  chart to filter all others; push the active filter straight into the Gear Inspector.
- **Final Sell** — one toggle adds catch-all sell rules for unmatched gear across
  configurable level ranges, so nothing slips through by accident.
- **Themes** — toggle between dark and light mode, customize colors and border radius
  with the built-in theme editor, or enable a color-blind-friendly palette.

## How To Use

### Recipe File
- SFC (`.sfc`): your project file for this app. Think of it like a save file you can load/share. RSL Helper does not read SFC directly.
- HSF (`.hsf`): the RSL Helper Sellfile. Export from this app, then load it in RSL Helper.
- Saved filename defaults to `SellfileCreatorRecipes_YYYYMMDD_HHMM.sfc`.

### Recipe Builder
- Fill in the Recipe Builder and give your recipe a clear name.
- Click “Add as new recipe” to save it; then click the saved entry in the list below the builder to select it for editing and update it.
- Load/Save: Use “Load Recipes” and “Save Recipes” to reuse your custom rules. These actions save everything needed to rebuild what you see in the preview into a recipe file.
  - Click the chevron (▾) next to **Load SFC File** for its menu: **Load from file…** opens the OS file picker as usual; **Load Preset: Beginner** or **Load Preset: Midgame to Endgame** loads one of the bundled presets after a confirmation prompt (your current setup will be replaced).
- Reset/Insert/Apply menus: Right-click Reset, Insert as recipe, or Apply as recipe to open the shared options menu. Save your current builder state as the default template, jump back to the factory defaults, enable Auto reset after Insert (clear the builder immediately after inserting a recipe), or enable Auto apply to selected recipe (push edits into the highlighted recipe automatically after ~400 ms of inactivity). Auto reset and Auto apply cannot be on at the same time—turning one on turns the other off—and both preferences persist between sessions.
- Note: Click “Add Note…” (or “Edit Note…”) to attach a note to your recipe file. The note is shown automatically after loading a recipe file that contains one. Use `<!-- recipes:1,0 -->` to drop chips for specific recipes (0 continues to the next one). Use `<!-- recipes-re:”speed” -->` to show every recipe whose name matches the case-insensitive pattern. Add `<!-- dungeon-simulator -->` to display a live keep-chance table for Fire Knight, Dragon, and Ice Golem across three difficulty stages (N20/N25/H10) and two boost modes, showing keep-rates at +0/+4/+8/+12/+16. Add `<!-- recipe-overrides [columns=N] -->` to embed interactive question cards (radio/checkbox groups) that override recipe export modes and settings at session time — stored recipes are never modified. Add `<!-- safeguard-overrides [columns=N] -->` to embed interactive slider and option cards that override safeguard rule properties (count, activation, substats, improvement chance, and more) at session time — stored safeguard rules are never modified. You do not need to type these blocks by hand: while editing the note, the pencil button on a question card (or the matching toolbar button for a new question) opens a visual editor that lets you build the questions, options, and effects with regular controls. When either marker type is present, the note footer adds a **Disable / Enable Dynamic Overrides** toggle and a **Reset Options to Defaults** button. Use **Save Current Selection…** (in the Dynamic Overrides menu) to store the current answers under a name — saved sets appear in the same menu so you can reload them in one click. Only the selections present in the current note are stored, and loading a saved set skips any questions that no longer exist.
- Autosave restore: On launch, the dialog lists every autosaved section with its own checkbox. Restore only what you need — recipes (including the selected chip), metasets, Substat Target Values, Final Sell remainder, the pinned note, the filter panel (open state, chips, collapsed sections), and any Gear Inspector imports. Leave a box unchecked to keep your current work untouched. Autosave also remembers which Final Sell toggles (Artifacts, Accessories, and level ranges) were enabled, so reopening the Tools dialog mirrors exactly what you exported last time.

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
- Faction: Restrict accessory rules to a specific faction when you are targeting a single team. Rings, Amulets, and Banners obey this filter; artifact pieces ignore it, so `Any` keeps artifacts safe.
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
- Open via the “Substat Targets…” button in the top‑right of the builder — it opens the **Substat Targets** tab in the Tools dialog.
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
- Click the `Tools` button next to the toggle to open the `Final Sell` tab and choose whether it covers Artifacts, Accessories, and which level ranges (0–3, 4–7, 8–11, 12–15, 16). The defaults cover 0–15 so fully leveled gear stays safe unless you turn `+16` on.
- Without Final Sell, items that do not match any rule are automatically kept by RSL Helper. Selling only happens when a Sell rule matches.
- When `Final Sell` is active, the generated Sell rules explicitly include all currently known sets. In the preview, the Sets column shows “All Currently Known” for these rules to reduce clutter; the exported file still lists every set explicitly.

### Safeguards
- Switch the builder to **Safeguards** mode using the toggle above the builder panel to mark the gear combinations you never want to lose. Turn on `Enable Safeguards` to let the scanner add keep rows (edits will also enable it automatically).
- Safeguard rules don’t ‘consume’ items—each rule evaluates the same candidate pool. If a piece matches multiple rules, it counts for all of them.
- Each keep rule lets you pick the slot, sets or metasets, ranks, rarities, main stats, and (for accessories) factions you care about. Leaving a picker empty means “any”.
- `Mode` decides what the safeguard does — the names match the buttons in the app: `Off` turns the rule off, `Protect` keeps only matching gear you already own (up to the required count), `Anticipate` also protects new drops while you own fewer matches than the required count, and `Improve` keeps watching after the count is met: a new drop stays protected only while the rule's improvement-chance setting says it can still beat your current gear (checked at each upgrade step); without an improvement-chance setting it works like `Anticipate`.
- Substats are optional: pick one or more to only count items that actually have those substats. The match chips set how many of the selected substats a piece must have — `≥1`–`≥4` (chips above the number you picked are greyed out) — or `Per Substat`, which applies the quota to each selected substat on its own. Leave the substats empty to allow any substat.
- Selected substats are ranked by their **current** substat value; weight controls appear in every min-count mode (`≥1`–`≥4`), while `Per Substat` keeps equal weighting (ties at the cutoff stay protected).
- `Weight by Rank` (the chip next to `Per main stat`) folds rank into the score itself instead of leaving it as an exact tie-break. The bonus is scaled by the **main stat**, and the exact size depends on the slot and main stat — a 5★ main stat scores roughly 81–89% of the same slot's 6★, a 4★ less again. The gap between adjacent ranks is small: enough to let a 6★ win a *near*-tie against a same-main-stat 5★ with only slightly better substats, but not enough to beat a real substat advantage. It uses the rank's +16 main stat, so leveling a piece never changes its score, and substat scores are untouched. Needs at least one substat selected; new rules have it on by default.
- `≥ Required Count` is the promise you want the app to keep. Scope chips directly under each picker (everything except `Rank` and `Rarity`) decide how that quota is split: `Per slot`, `Per set`, `Per faction`, and `Per main stat` can be combined freely. Turning every chip off automatically falls back to the shared `Per safeguard` pool.
- The info tooltip behind `Required Count` shows the active scope split (`X per slot × per set × ...`) and a simple deficit line (`({missing} missing)`).
- The scanner only adds keep rows for matching items that would otherwise be sold, and only when the required count is not met. With `Anticipate`, placeholder keep rules cover the matches you are still missing; with `Improve`, extra keep rules stay on after the count is met — but only for drops whose improvement chance still clears the rule's bar.
- **Ignore toggles** (chips next to the rule's enable switch) fine-tune what each rule counts:
  - `Ignore previous safeguards` — when the rule ranks candidates by substats, drops items that earlier safeguards already protected from its matching pool and picks the next top items instead. Useful when you stack a second SPD/CR rule after a generic one and want it to reach deeper into the score ranking rather than redundantly protect the same pieces. Rules without substats are unaffected. Default: off.
  - `Ignore equipped (Collection)` — excludes items currently equipped on collection champions from this rule's match count, so they do not satisfy the rule's quota. Default: off.
  - `Ignore equipped (Vault)` — same idea but for vault champions. Default: off.
- **`Improvement chance ≥ N%`** (optional talent scout): widens the safety net beyond the standard top-N. The scanner always keeps the top-N pieces by their **current** substat value first — those are never at risk. It then also protects any piece *outside* that top-N whose improvement chance meets the threshold. Think of it as: "hold on to the raw drops that have a good shot at being competitive once they're leveled."

  **What is improvement chance?** The app simulates all possible ways a piece could roll during upgrades to +16 — some rolls hit the substat you care about, some don't — and counts how often the piece ends up in your top N across all those futures. A piece with 68% improvement chance lands in the top N in roughly two out of three simulated upgrade paths.

  **Improvement chance is a *prediction*, not the rule that keeps your gear — they are two separate systems.** This trips people up, so it's worth being explicit:

  - The safeguard **always keeps the top-N pieces by their substat value *right now*** (see [Selected substats are ranked by their **current** value](#safeguards)). That current-value ranking is what actually protects a piece.
  - Improvement chance answers a *different* question: *"once everything is leveled to +16, will this piece still be one of my best?"* It scores **both the piece and its competitors at their projected +16 values**, then asks how often the piece lands in the top N.

  Because they ask different questions, the two can disagree — and that's expected, not a bug:

  - A piece can show **0% improvement chance and still be safeguarded.** It's one of your best *today* (so the current-value top-N keeps it), but the simulation expects rivals that are themselves still leveling to out-roll it by +16 (so its *future* top-N chance is ~0%). A single good roll that pushes a piece into your current top-N will safeguard it immediately — its improvement chance may stay 0% the whole time, because that number was never what protected it.
  - A piece can show a **high improvement chance and not be safeguarded yet.** It's a promising raw drop that isn't in your current top-N — it only gets kept if you turn on the threshold below.

  **Key rule: the threshold can only add to protection, never remove.** Your current top-N is always kept, regardless of their improvement chance score. A fully upgraded piece (+16) counts its locked current value directly — it cannot fall out of protection because it "ran out of upgrade potential."

  **Example — SPD banners, Required Count = 2, Per faction (rank-6 legendary):**

  | Banner | SPD | Level | Improvement chance | Standard | Threshold ≥ 50% | Threshold ≥ 25% |
  | --- | --- | --- | --- | --- | --- | --- |
  | A | 12 | +16 | 100% | ✔ top-2 | ✔ top-2 | ✔ top-2 |
  | B | 6 | +16 | 0% | ✔ top-2 | ✔ top-2 | ✔ top-2 |
  | C | 5 | +0 | 26% | ✗ sold | ✗ sold | ✔ threshold adds |

  Rank-6 banners roll SPD in increments of **5 or 6** per event, so the only realistic fresh values are **5** (minimum) or **6** (maximum). Banner A's SPD=12 means it received exactly one bonus SPD roll during upgrades (6 initial + 1 roll of 6). Banner B was fully leveled with no bonus SPD rolls — its score is locked at 6.

  Banner B scores 0% improvement chance: its fixed SPD=6 is expected to lose to any unleveled competitor whose future rolls could exceed it. Despite that, it stays protected because it is in the standard top-2 by **current** value. Improvement chance can never remove items from the top-N — only the threshold expansion logic uses it.

  Banner C (SPD=5, fresh) sits just outside the top-2 by current value. Its 26% improvement chance means it would end up in the top-2 in roughly 1 in 4 simulated upgrade paths. Setting threshold ≥ **25%** pulls it into protection; at threshold ≥ 50% it remains sold.

  If Banner C had started at **SPD=6** instead, its improvement chance rises to **68%** — a much stronger candidate. Threshold ≥ **65%** would protect it.

  **Rank-6 epic banners** only receive **3 SPD roll events** (versus 4 for legendary, because the +4 upgrade adds a brand-new substat rather than rolling an existing one). The resulting chances are nearly identical: SPD=6 fresh → **70%**, SPD=5 fresh → **26%**.

  **Suggested thresholds (rank-6 gear):**
  - **65%** — protects fresh max-roll drops (SPD=6, ~68–70% chance). Good default if you want promising drops to survive while leveling up.
  - **25%** — also protects min-roll drops (SPD=5, ~26% chance). Wider net; use this if inventory space is not a concern.
  - Avoid **100%**: it only ever matches fully-leveled pieces already held by the standard top-N, so it adds nothing beyond standard mode.

#### Quota scopes at a glance
Stacking the scope chips changes who gets their own quota. Leave `Per safeguard` on to share one pool, then layer `Per slot`, `Per set`, `Per faction`, and `Per main stat` to enforce Slot × Set × Faction × Main stat mixes independently.

| Scope button | Quota behavior | When it shines |
| --- | --- | --- |
| `Per safeguard` | One shared pool for the entire safeguard. | Keep five SPD boots regardless of set. |
| `Per slot` | Duplicates the quota for each slot. | Keep two rings, two amulets, and two banners independently. |
| `Per set` | Duplicates the quota for each set/metaset in the safeguard. | Track two Stoneskin and two Protection drops separately. |
| `Per faction` | Duplicates the quota for each faction. | Guarantee three Merciless rings for every faction. |
| `Per main stat` | Duplicates the quota for each selected main stat. | Keep separate pools for ACC versus RES banners. |

#### Real-world examples
| Scenario | Filters | Required Count | Scope buttons | What the scanner guarantees |
| --- | --- | --- | --- | --- |
| Running out of SPD boots | Slot = Boots, Main Stat = SPD, Sets blank | `5` | `Per safeguard` | At least five SPD boots survive, no matter the set. |
| Mixing Savage + Lethal gloves | Slot = Gloves, Sets = Savage + Lethal, Main Stat = CDMG% | `3` | `Per safeguard` | Three high-damage gloves stay safe even if the set mix changes. |
| Merciless rings per faction | Slot = Ring, Set = Merciless, Faction blank | `3` | `Per faction` | Every faction keeps three of its own Merciless rings. |
| HP% rings per faction | Slot = Ring, Main Stat = HP%, Sets blank | `2` | `Per faction` | Two HP% rings per faction stay in inventory. |
| Core accessories per faction | Three rules (Ring, Amulet, Banner), Sets/Main blank | `5` | `Per faction` | Five Rings, Amulets, and Banners survive per faction. |
| Stoneskin + Protection accessories | Slot = Ring/Amulet/Banner, Sets = Stoneskin + Protection, Main blank | `2` | `Per set` + `Per faction` + `Per slot` | Each faction holds two Stoneskin and two Protection drops for each accessory slot. |
| Fastest SPD accessories | Slot = Ring/Amulet/Banner, Substats = SPD | `5` | `Per safeguard` | Keeps the top five SPD substat rolls across your accessories (ties included). |
| ACC banners that still roll SPD | Slot = Banner, Main Stat = ACC, Substats = SPD + ACC, Weights favor SPD | `3` | `Per faction` | Each faction keeps the best ACC banners where SPD rolls matter most. |

Tip: Import your `.db` or paste gear into the Gear dialog before switching to Safeguards mode so the scanner sees real items. Click a safeguard rule to highlight matching gear; switch `Filter` to `Selection` to view only those matches.

### Dungeon Drops (Simulator)
Open `Tools` and switch to **Dungeon Drops**. It simulates dungeon farming using your current Sellfile rules so you can see how much gear you would keep per set and upgrade level.

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
- Recipes on/off toggle: The toggle in the builder header globally disables all recipes without deleting them, pausing the preview pipeline — useful to quickly check a safeguards-only export or confirm what Final Sell alone produces.

### Gear Analytics
Open `Tools` and switch to the **Gear Analytics** tab for an analytics overview of your imported gear.

**KPI cards (top row):** Eight percentage cards — **6★ Rate**, **Legendary+**, **Maxed (+16)**, **Equipped**, **Vault-Locked**, **Chaos'd**, **Glyphed**, **Ascended** — each with a tooltip.

**Crossfilter donuts:** Six charts — **Slots**, **Rank**, **Rarity**, **Result**, **Source**, **Level** — update each other as you click.
- Click a slice to add it as a filter for that dimension; every other chart instantly narrows to show only the matching gear. Each chart excludes its own dimension so it always shows its full range.
- Double-click a slice on the **Slots** donut to select an entire group at once: any artifact piece (Weapon, Helmet, Shield, Gauntlets, Chestplate, Boots) selects all six artifact slots; any accessory (Ring, Amulet, Banner) selects all three.
- **Slots** and **Source** donuts show category icons. The **Level** donut labels each arc with its level text.


**Sets treemap:** Displayed below the donuts. Each tile represents one gear set; tile area is proportional to item count. The tile background is split left-to-right into outcome color bands (Sell / Safeguarded / Keep / No Match). Click a tile to add that set as a crossfilter.

**Filter chips:** Active selections for each dimension appear as chips below the donuts; click the delete icon on a chip to remove just that filter. Main Stat selections also appear as chips. The **Clear filters** button resets all dimensions at once.

**Main Stats bar:** Shows how often each main stat appears across the filtered gear. Click a bar to drill down — the Substat Frequency chart updates to show only substats from gear with that main stat selected. Click the bar again to deselect.

**Improvement Chance:** How likely your gear is to improve, grouped in 10% steps. The number on the right is how many items fall in each group. Gear with no safeguard, and maxed +16 gear, are left out. Click a group to show only that gear.

**Substat Frequency radar:** Shows how often each substat appears across the filtered (and optionally main-stat-drilled) gear as a spider chart. Click an axis mark to select it as a co-occurrence pivot — the radar then narrows to gear containing all selected substats at once (up to 4 pivots). Active pivots appear as chips below the chart; click × to deselect one, or **Clear** to remove all.

**Slot × Main Stat heatmap:** Item count per slot (columns) × main stat (rows). Click a column header or any cell to filter by that slot.

**Champion Stats tab:** Substat totals summed across equipped pieces per champion. Filter by location (**All** / **Collection** / **Vault**), toggle **Fully Equipped** only, and include or exclude glyphs. Displays Min/Avg/Median/Max series.

**Champion Equipment:** Per-champion gear-slot coverage in two compact tables (**Collection** / **Vault**). Each row shows a 3×3 slot grid (filled = equipped, outline = empty, dashed = locked until ascension). Click a filled slot to select that piece — selection is shared with the Gear Inspector. Toggle **Simulate sold** to paint slots that would be sold red and count them as missing, or **Show fully equipped** to also list champions with every slot filled.

**Buttons:**
- **Copy Snapshot:** Renders the full analytics view as a PNG and copies it to the clipboard. Note: the Champion Equipment chart is not included in the snapshot.
- **Apply to Gear Inspector:** Pushes the active crossfilter into the Gear Inspector list filter (only visible when a filter is active).

### Sellfile Preview (Rules & Gear Inspector)
- The preview header keeps the `Rules`/`Gear Inspector` toggle, the `Tools` button, and the “Load RSL Helper Sellfile” button together so you always know where to switch tables or open the Gear dialog.
- `Rules` view (default): shows every rule that will be exported, including any optional base `.hsf` rows. The header counts stay on Keep vs Sell, the filter row keeps the Any/Only chips for Slot/Rank/Rarity/Level, and both Recipe buttons remain: Preview Recipes controls chip visibility, while the Recipe Filter button is a simple On/Off toggle that hides Sellfile rows outside your selected recipe chips (and keeps that filter staged for when you switch modes).
- `Gear Inspector` view: flips the table to the imported gear list so you can scan imported or hand-built items without reopening the Tools dialog. Counts/outcome chips switch to Keep / Sell / Scope / Unmatched based on first-match results, and the filter row keeps both Recipe buttons side by side: Preview Recipes still controls chip visibility, and the Recipe Filter button expands to a tri-state selector (`Off` → `First-Match` → `Any-Match`) so you can decide how those items respond while continuing to gate Sellfile rows when you jump back. Importing a `.db` automatically switches to this view, but you can jump back to Rules whenever you want.
- The “Load RSL Helper Sellfile” button behaves exactly like drag & drop: `.sfc` replaces the builder state, `.hsf` layers on the optional base Sellfile, and `.db` queue items into the Gear Inspector (without touching recipes). The “Clear” button detaches the optional base `.hsf`.
- Use the palette icon to open Manage Colors for substat labels.
- In Rules view the table columns still include “Idx” and “Recipe” (empty for base file rows). In Gear Inspector view the same space lists slot/set, item stats, and the first matching recipe badge so you can see what would happen to each artifact directly inside the preview.

### Sellfile Preview Controls
- Manage Colors: Click the palette icon above the table to customize text/background colors for substat labels. Use “Reset to defaults” in the dialog to restore recommended colors.
- Filters: Press `Ctrl+F` (`Cmd+F` on macOS) to open the panel and focus the Recipe search instantly. Right-click any section header (or `Ctrl`/`Cmd`+click its chevron) to collapse or expand every section at once. Preview Recipes hides saved-recipe chips that do not match the active filter so the preview stays readable. Recipe Filter controls which recipes are allowed in the table: it’s a simple On/Off toggle in Rules mode, and it cycles through `Off` → `First-Match` → `Any-Match` when the Gear Inspector is active.
- Column menu: Right-click the table header to open controls:
  - Reset columns: Restore default columns and widths.
  - Auto-fit widths: Fit columns to the viewport.
  - Allow multi‑line rows: Toggle wrapping for Substats and others.
  - Show/Hide columns: Per‑column visibility checkboxes.
- Reorder columns: Drag a header left/right.
- Resize columns: Drag the right edge of a header.
- Click behavior: Clicking a table row selects the related saved recipe (no auto-scroll). Clicking a saved recipe scrolls the table to the first matching row.

### Gear Inspector
- Click `Tools` in the Sellfile Preview header to open the Gear dialog. Create example gear. Items sync to the preview immediately, so closing the dialog does not clear your Gear Inspector grid.
- Connect to RSL Helper for live gear sync (the Connect button in the preview header), or import a `.db` file by dropping it onto the app or using the “Load RSL Helper Sellfile” button.- Each item in the Gear Inspector shows slot, set, level, main stat, substats (with glyphs and rolls), the source (inventory vs inbox), and chips for Keep/Sell + the first matching recipe/rule. Disabled rules never match, so “No match” entries represent gear the Sellfile would leave alone.
- The header counts show Keep / Sell / matched / unmatched totals. The four result-filter buttons — **Keep**, **Sell**, **Scope**, and **Unmatched** — work as independent toggles: activate any combination to narrow the list. **Scope** dims (but keeps visible) items that share the same set+slot as a piece your rules would sell, so you can compare a candidate against its competition in one view rather than hunting across two filter passes. When one or more **Sources** are also selected, those sources act as the reference set — only sell-tagged items from the selected sources become primaries, while companions are drawn from *all* sources, letting you see every copy of that gear piece regardless of where it sits. **Unmatched** shows gear no rule touches at all — useful for spotting gaps in your recipes. Combine these with the Recipe `First-Match`/`Any-Match` toggle to focus on edge cases before exporting.
- Use the preview toggle to move between Rules and Gear Inspector without reopening the Tools dialog — great for comparing the generated rule rows against the gear that triggered them.
- **Safeguard Rank overlay:** the grid menu has a **Safeguard Rank** button that cycles what each piece's rank chip shows (by current substat value, **#1** is the best; green = kept, red = would be sold). **Off** hides it; **Group** shows the rank within the piece's own group — the slot / set / faction / main-stat scope the rule keeps separately (e.g. **#2**); **Safeguard** shows the rank across the whole safeguard (e.g. **#7**); **Both** shows group then safeguard as **#2 · #7** (2nd in its group, 7th overall). The chip and tooltip are sorted by the displayed rank, the chip reflects the piece's best-ranked matching rule, and clicking it jumps to that rule. When safeguard rules are selected, the chip reflects those rules; a piece ranked only by a *different* rule still shows its best rank, slightly faded. Needs Safeguards enabled.

### Gear Diff (Before / After)
- The **Diff** button in the Gear Inspector header turns on a comparison that shows which gear pieces flip between **Keep** and **Sell** as you change things — handy when tuning recipes or trying the dynamic overrides in the Note dialog.
- A small chip next to the button shows the running change against your reference point: how many more (or fewer) pieces are now **Sold**, **Kept**, and protected by **Safeguards**.
- Left-click the **Diff** button to open a **side-by-side before/after** of the changed pieces (left = before, right = after) with synced scrolling. Click again to close.
- Right-click the button for options:
  - **Set reference** — freeze the current state as the “before” you compare against.
  - **Auto-track reference** (on by default) — keeps the “before” at your latest recipe/safeguard edit, so the diff always reflects your most recent change.
- Two things worth knowing:
  - Toggling **dynamic overrides** in the Note dialog **adds up** — clicking several overrides shows their combined effect, not just the last one.
  - Editing a recipe or safeguard in the builder moves the reference to that edit (while Auto-track is on). Turn Auto-track off (or use Set reference) to compare everything against one fixed point.
- Your normal Gear Inspector filters still apply: a piece shows if it matches the filter either before or after the change.

### Export
- Click “Export merged RSL Helper Sellfile” (or “Export RSL Helper Sellfile” when no base file is loaded).
- Use “Save Recipes” and “Load Recipes” in Add Rules to keep and reuse your work.
- Exported filename defaults to `Sellfile_YYYYMMDD_HHMM.hsf`.

### Accounts

Sellfile Creator can keep separate documents (recipes, safeguards, note, gear) for several game accounts. The account switcher sits in the top bar (and in the simple view's dialog): click it to switch accounts or create new ones, and use the gear icon next to an account to open the account manager. There you can rename an account, pick its accent color, enter the RSL Helper account id it belongs to, turn auto-push on or off per account, mark one account as the default for data that arrives without an account id, toggle whether received gear data is saved on this device at all, and delete an account together with all of its data. Hold Shift while picking an account in the switcher to merge the current document into it.

**How the transition works:**

- After updating, all your existing data simply lives in one account called "Default" — nothing changes for you.
- Account support is being rolled out in steps together with RSL Helper, so parts of it are not fully active yet.
- For now, RSL Helper doesn't yet tell Sellfile Creator which game account it is sending. That data goes to your active account — or to the account you flagged as "default for data without account id" in the manager.
- As soon as RSL Helper passes the account id when launching Sellfile Creator, your existing "Default" account is linked to that id automatically, so your data simply follows. A second game account then gets its own fresh Sellfile Creator account.
- Once RSL Helper also tags its data packets with the account id, everything routes automatically: data for another account never mixes into the one you are working on, and if that other account has auto-push enabled, its sellfile is rebuilt and sent back in the background.

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
to **[SP] Panda** for his Sellfiles,  
to **KruYseN** for his gear cleanse videos,  
and of course thanks to **Farbstoff** for RSL Helper!

## Author
Made by [STBL] Nusi㊷  
Localization by [STBL] Nusi㊷

© Nusi㊷ - 2026
