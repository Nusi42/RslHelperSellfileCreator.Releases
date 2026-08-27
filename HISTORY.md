Sellfile Creator Release History
DISCLAIMER: These release notes are AI generated and might contain incorrect statements.

## v1.0.44 — 2026-08-27
English:
- **Fixed: The Lategame preset's "Actually, just sell all weak Chaos Ore pieces?" option could also sell your Anomalous accessories** — the option matched on a shared behind-the-scenes flag instead of on the Chaos Ore rules themselves, and the Anomalous rule happened to carry that same flag. It now only ever touches the Chaos Ore rules it was built for.

Deutsch:
- **Behoben: Die Option „Ja, alle verkaufen” im Chaos-Erz-Bereich des Lategame-Presets konnte auch deine Anomalous-Accessoires verkaufen** — die Option griff auf eine intern geteilte Kennzeichnung zu statt auf die Chaos-Erz-Regeln selbst, und die Anomalous-Regel trug zufällig dieselbe Kennzeichnung. Sie betrifft jetzt ausschließlich die Chaos-Erz-Regeln, für die sie gedacht ist.

## v1.0.43 — 2026-08-23
English:
- **New: The recipe and safeguard builder column can now be split into two resizable sections** — drag the new handle between the rule form and its chip list to give either one more room. The split is remembered separately for recipes and safeguards, and double-clicking the handle resets it to the default size.
- **Fixed: RSL Helper running on a custom port could keep getting contacted on the old or default port after you launched it** — an earlier improvement that remembers your connection between sessions didn't pick up the port from the launch link; the app now reads it correctly, and a link without a port no longer overwrites the port you already had saved.
- **Fixed: The app could gradually use more and more memory during long play sessions, especially after using safeguard groups, eventually slowing things down or crashing** — a side effect of that feature kept reprocessing a growing snapshot of your gear on every update instead of reusing what it already had. Memory use now stays flat during extended sessions.

Deutsch:
- **Neu: Die Rezept- und Schutzregel-Builder-Spalte lässt sich jetzt in zwei größenveränderliche Bereiche aufteilen** — der neue Griff zwischen Regelformular und Chip-Liste lässt sich ziehen, um einem der beiden mehr Platz zu geben. Die Aufteilung wird getrennt für Rezepte und Schutzregeln gemerkt, ein Doppelklick auf den Griff setzt sie auf die Standardgröße zurück.
- **Behoben: RSL Helper auf einem abweichenden Port konnte nach dem Start weiterhin über den alten oder den Standard-Port angesprochen werden** — eine frühere Verbesserung, die sich die Verbindung zwischen den Sitzungen merkt, übernahm den Port aus dem Start-Link bisher nicht; die App liest ihn jetzt korrekt aus, und ein Link ohne Port überschreibt den bereits gespeicherten Port nicht mehr.
- **Behoben: Die App konnte bei langen Spielsitzungen nach und nach mehr Speicher verbrauchen, besonders nach der Nutzung von Schutzregel-Gruppen, was sie irgendwann verlangsamte oder abstürzen ließ** — ein Nebeneffekt dieser Funktion verarbeitete bei jeder Aktualisierung eine wachsende Momentaufnahme deiner Ausrüstung erneut, statt die bereits vorhandene weiterzuverwenden. Der Speicherverbrauch bleibt jetzt auch bei langen Sitzungen konstant.

## v1.0.42 — 2026-08-22
English:
- **New: Safeguard groups — several safeguards sharing one Required Count** — until now every safeguard counted on its own, so two rules that were really describing the same promise kept twice as much gear as you wanted: one wants 3 good rings, another wants 2, and you end up with 5.
- **New: Tags now have stable colours** — every tag gets its own colour derived from its text, the same on every recipe and safeguard chip, in the builder and in the tags popover, and legible in all three themes. Nothing to configure — same tag, same colour, everywhere.
- **Improved: Lategame preset's Utility safeguards now use grouping** — the Survivability, Damage, and Debuffer variants of the “Protect: Utility” rule now share one Required Count each instead of each keeping its own pieces separately, so you no longer end up protecting more utility gear than you meant to.
- **New: Recipe options for skipping safeguards or targeting reworked gear are now simple toggle buttons** — these used to be hidden as special tags typed into the free-form tag box; they're now dedicated flags shown as small icons on the recipe in the list and in its Keep/Sell badge. Recipes saved before this change keep working automatically.
- **Improved: Chaos Ore setup for each star rank uses a grid of gear-set checkboxes** — the Lategame preset's per-rank Chaos Ore questions now show one checkbox per gear set instead of a radio button plus separate fine-tune boxes, making it clearer which sets each rank targets. Default 5-star selections were also adjusted per account tier.
- **New: Simple mode can now limit which gear sets the “keep everything useful” and Chaos Ore “any set” rules cover**, instead of those rules always applying to every set.
- **Improved: The tag picker in the recipe and safeguard builders now suggests tags already used elsewhere** in your recipes and safeguards, so you don't have to remember or retype an existing tag's exact spelling.
- **Redesign: New gold-accented visual style across every theme** — panels, dividers, and dialog titles now carry a warm gold accent with subtle corner details. A new “Border style” option in Theme Settings switches back to the plain frame if you prefer it. Simple mode's note window can now open Theme Settings directly.
- **Fixed: Gear could get stuck showing under the wrong champion after moving it in-game** — the app only refreshed equipped gear when a champion itself changed, so moving gear directly between champions could leave it displayed on the one it had already left.
- **Improved: Gear Analytics now shows how many of your accessories are anomalous**, alongside the existing artifact and accessory totals.
- **Fixed: Anomalous gear was being scored as worthless in Gear Inspector and recipe ranking** — finishing up anomalous-stat support left these pieces with a rating of zero; they're now ranked normally like any other gear.
- **Fixed: Some safeguard rules that judge one substat at a time could rank pieces incorrectly** — a piece missing the actual substat being judged could still slip into the results, and changing an unrelated substat's weight could reshuffle which pieces qualified. Rankings now correctly require the piece to have the substat in question. Visual bug only.
- **Fixed: Turning certain setup options on or off while your note was open could close it unexpectedly** — flipping an account-mode override could switch to a recipe set with no matching note, silently closing the window; it now stays open as expected.

Deutsch:
- **Neu: Schutzregel-Gruppen — mehrere Schutzregeln teilen sich eine benötigte Anzahl** — bisher zählte jede Schutzregel für sich, sodass zwei Regeln, die eigentlich dasselbe Versprechen meinten, doppelt so viel Ausrüstung behielten wie gewollt: eine will 3 gute Ringe, eine andere 2, und am Ende behältst du 5.
- **Neu: Tags haben jetzt feste Farben** — jeder Tag bekommt aus seinem Text eine eigene Farbe, die auf jedem Rezept- und Schutzregel-Chip, im Editor und im Tag-Fenster gleich aussieht und in allen drei Designs lesbar bleibt. Nichts einzustellen — gleicher Tag, gleiche Farbe, überall.
- **Verbessert: Die Utility-Schutzregeln des Lategame-Presets nutzen jetzt Gruppierung** — die Varianten Survivability, Damage und Debuffer der Regel „Protect: Utility” teilen sich jetzt jeweils eine Benötigte Anzahl, statt jede für sich Teile zu behalten, sodass du nicht mehr mehr Utility-Ausrüstung schützt als beabsichtigt.
- **Neu: Die Rezept-Optionen zum Ausklammern aus Schutzregeln oder zum gezielten Ansprechen von überarbeiteter Ausrüstung sind jetzt einfache Schalter** — bisher steckten sie als spezielle Tags im freien Tag-Feld; jetzt sind es eigene Kennzeichnungen, die als kleine Symbole am Rezept in der Liste und in seinem Behalten/Verkaufen-Abzeichen erscheinen. Vorher gespeicherte Rezepte funktionieren automatisch weiter.
- **Verbessert: Die Chaos-Erz-Einrichtung je Sternerang nutzt jetzt ein Raster aus Set-Kontrollkästchen** — die Chaos-Erz-Fragen je Rang im Lategame-Preset zeigen jetzt ein Kästchen pro Ausrüstungsset statt eines Radio-Buttons mit separaten Feinabstimmungs-Kästchen, wodurch klarer wird, welche Sets jeder Rang anspricht. Die 5-Sterne-Standardauswahl wurde außerdem je Konto-Stufe angepasst.
- **Neu: Der Simple-Modus kann jetzt einschränken, welche Ausrüstungssets die Regeln „alles Nützliche behalten” und Chaos-Erz-„jedes Set” abdecken**, statt dass diese Regeln immer für jedes Set gelten.
- **Verbessert: Die Tag-Auswahl in Rezept- und Schutzregel-Builder schlägt jetzt bereits verwendete Tags vor** aus deinen Rezepten und Schutzregeln, sodass du dir die genaue Schreibweise eines vorhandenen Tags nicht merken oder erneut eintippen musst.
- **Redesign: Neuer goldakzentierter Look für alle Designs** — Panels, Trennlinien und Dialogtitel tragen jetzt einen warmen Goldakzent mit dezenten Eckdetails. Eine neue Option „Rahmenstil” in den Design-Einstellungen schaltet auf Wunsch zurück auf den schlichten Rahmen. Das Note-Fenster im Simple-Modus kann die Design-Einstellungen jetzt direkt öffnen.
- **Behoben: Ausrüstung konnte nach dem Verschieben im Spiel weiter beim falschen Champion angezeigt werden** — die App aktualisierte die ausgerüstete Ausrüstung bisher nur, wenn sich ein Champion selbst änderte, sodass direkt zwischen Champions verschobene Ausrüstung noch beim vorherigen Champion angezeigt werden konnte.
- **Verbessert: Gear Analytics zeigt jetzt, wie viele deiner Accessoires anomalous sind**, zusätzlich zu den bisherigen Artefakt- und Accessoire-Gesamtzahlen.
- **Behoben: Anomalous-Ausrüstung wurde im Gear Inspector und bei der Rezept-Rangfolge als wertlos bewertet** — beim Abschluss der Anomalous-Stat-Unterstützung erhielten diese Teile eine Bewertung von null; sie werden jetzt wie jede andere Ausrüstung normal eingestuft.
- **Behoben: Manche Schutzregeln, die Substats einzeln nacheinander bewerten, konnten Teile falsch einstufen** — ein Teil ohne den tatsächlich bewerteten Substat konnte trotzdem in die Ergebnisse rutschen, und das Ändern der Gewichtung eines unbeteiligten Substats konnte die Einstufung durcheinanderbringen. Die Rangfolge verlangt jetzt korrekt, dass das Teil den betreffenden Substat auch besitzt. Nur visueller Fehler.
- **Behoben: Das Ein- oder Ausschalten bestimmter Einrichtungsoptionen bei geöffnetem Note konnte dieses unerwartet schließen** — das Umschalten eines Konto-Modus-Overrides konnte auf ein Rezept-Set ohne passendes Note wechseln und das Fenster stillschweigend schließen; es bleibt jetzt wie erwartet geöffnet.

## v1.0.41 — 2026-08-12
English:
- **Fixed: Applying a saved filter preset could restore a different filter than the one you configured** — if the Rules panel and Gear Inspector filters weren't set to stay in sync, a preset could silently apply the other panel's leftover filter instead of the one you actually saved. Presets now always apply the filter of the panel you're using.
- **New: Your answers to a Note's recipe and safeguard setup questions now save with the sellfile itself** — previously they only lived in this browser, so opening the same file elsewhere, or after clearing browser data, reset those choices back to their defaults. "Copy All Recipes" now carries your answers along with the recipes and safeguards.
- **Improved: Substat lists in the recipe builder, safeguard builder, and filter panel are now split into two collapsible groups** — classic stats and anomalous stats — with the anomalous group collapsed by default to keep the list manageable.
- **Fixed: The Rolls flyout couldn't show all 19 substats for a piece** — the trailing anomalous rows were being cut off; the list now scrolls so every stat is visible.

Deutsch:
- **Behoben: Das Anwenden eines gespeicherten Filter-Presets konnte einen anderen Filter wiederherstellen als den gespeicherten** — waren die Filter von Regel-Panel und Gear Inspector nicht auf Synchronisierung eingestellt, konnte ein Preset stillschweigend den übriggebliebenen Filter des jeweils anderen Panels anwenden statt des tatsächlich gespeicherten. Presets wenden jetzt immer den Filter des gerade verwendeten Panels an.
- **Neu: Deine Antworten auf die Einrichtungsfragen eines Notes (Rezept- und Safeguard-Konfiguration) werden jetzt zusammen mit der Verkaufsdatei gespeichert** — bisher lebten sie nur in diesem Browser, sodass das Öffnen derselben Datei woanders oder nach dem Leeren der Browserdaten diese Auswahl auf die Standardwerte zurücksetzte. „Alle Rezepte kopieren" nimmt deine Antworten jetzt zusammen mit den Rezepten und Safeguards mit.
- **Verbessert: Substat-Listen im Rezept-Builder, Safeguard-Builder und Filter-Panel sind jetzt in zwei einklappbare Gruppen unterteilt** — klassische Stats und Anomalous-Stats — wobei die Anomalous-Gruppe standardmäßig eingeklappt ist, damit die Liste übersichtlich bleibt.
- **Behoben: Das Rolls-Flyout zeigte nicht alle 19 Substats eines Teils an** — die hinteren Anomalous-Zeilen wurden abgeschnitten; die Liste ist jetzt scrollbar, sodass alle Stats sichtbar sind.

## v1.0.40 — 2026-08-12
English:
- **Fixed: Recipes targeting the new anomalous accessory stats (PvE/PvP/Boss/Dungeon damage dealt/taken) never actually matched any gear** — a units mismatch inside Sellfile Creator's own rule matching, introduced together with anomalous accessory support, silently discarded every match. This only affected the matching logic inside the app itself — sell files you had already exported were correct and don't need to be redone.

Deutsch:
- **Behoben: Rezepte für die neuen Anomalous-Accessoire-Stats (PvE-/PvP-/Boss-/Dungeon-Schaden erlitten/verursacht) fanden nie passende Ausrüstung** — ein Einheiten-Mismatch im internen Regelabgleich von Sellfile Creator, der zusammen mit der Anomalous-Unterstützung eingeführt wurde, ließ jeden Treffer stillschweigend durchfallen. Betroffen war nur der Abgleich innerhalb der App selbst — bereits exportierte Verkaufsdateien waren korrekt und müssen nicht neu erzeugt werden.

## v1.0.39 — 2026-08-12
English:
- **New: Anomalous accessories are now fully supported** — rings, amulets, and banners that roll mode-specific damage stats (PvE, PvP, Boss, or Dungeon damage dealt/taken) can now be selected in recipes and safeguards, and rules built from them are correctly included in your exported sell file.
- **New: Precise decimal targets for anomalous stats** — since these stats roll in fine increments, their target values can now be set with 0.25% precision instead of being rounded to whole numbers.
- **New: A default "Anomalous" recipe was added to the built-in preset**, so accessories with these stats aren't accidentally sold while more detailed rules for them are still being worked out.
- **New: Gear carrying an anomalous stat is now visually marked** — its icon in Gear Inspector gets a dashed, double-ringed border so you can spot it at a glance.

Deutsch:
- **Neu: Anomalous-Accessoires werden jetzt vollständig unterstützt** — Rings, Amulets und Banners mit modusabhängigen Schadenswerten (PvE-, PvP-, Boss- oder Dungeon-Schaden erlitten/verursacht) können jetzt in Rezepten und Safeguards ausgewählt werden, und die daraus gebauten Regeln landen korrekt in der exportierten Verkaufsdatei.
- **Neu: Präzise Dezimal-Zielwerte für Anomalous-Stats** — da diese Stats in feinen Schritten würfeln, lassen sich ihre Zielwerte jetzt mit 0,25%-Genauigkeit statt nur in ganzen Zahlen festlegen.
- **Neu: Ein Standard-Rezept „Anomalous" wurde zum Preset hinzugefügt**, damit Accessoires mit diesen Stats nicht versehentlich verkauft werden, solange detailliertere Regeln dafür noch in Arbeit sind.
- **Neu: Ausrüstung mit einem Anomalous-Stat wird jetzt visuell markiert** — ihr Symbol im Gear Inspector erhält einen gestrichelten Doppelring-Rahmen, damit du sie auf einen Blick erkennst.

## v1.0.38 — 2026-07-16
English:
- **Improved: Safeguard scoring uses unscored substats to settle ties between otherwise-equal pieces** — when two artifacts weigh out the same on your priority stats, the remaining lines now tip the balance, giving more consistent rankings across all match modes.
- **Fixed: The app could become unresponsive or crash during long farm sessions or after frequently updating safeguard settings** — a gradual memory build-up that crept in alongside recent performance improvements is now kept in check.

Deutsch:
- **Verbessert: Safeguard-Bewertung nutzt unbewertete Substats zur Gleichstandsentscheidung** — wenn zwei Artefakte bei deinen priorisierten Stats gleich punkten, geben die übrigen Zeilen jetzt den Ausschlag, was zu konsistenteren Rangfolgen in allen Treffermodi führt.
- **Behoben: Die App konnte bei langen Farm-Sitzungen oder nach häufigen Änderungen an Safeguard-Einstellungen hängen bleiben oder abstürzen** — ein schrittweiser Speicheranstieg, der sich im Zuge jüngster Leistungsverbesserungen eingeschlichen hatte, wird jetzt in Schach gehalten.

## v1.0.37 — 2026-07-11
English:
- **Improved: Lategame preset safeguard rules expanded and reorganized** — grown to 133 rules (was 116), now arranged into labeled families — Speed, Debuffer, Damage, Crit Shield, Survivability, Utility, Accessories, Mercurial, and Faction Wars — with visual section dividers in the safeguard builder. Accessory and Mercurial sections are further divided by slot (Rings / Amulets / Banners). Rule names are standardized to 43 clear labels across all 133 entries (was 80 varied names).
- **Improved: Consistent rank and rarity handling across safeguards** — safeguard and recipe rules now apply rank and rarity uniformly, so Rare-rarity pieces are protected on the same footing as higher rarities instead of being excluded.
- **Fixed: When "Keep 5-star safeguards" is turned off, artifact rules now correctly clamp to 6-star** — only accessories (rings, amulets, banners) remain at 5-star; all artifact families (damage, debuffer, crit shield, survivability, speed set, and others) now behave as expected.
- **New: Midgame preset — damage CR% gauntlet recipe variants** — three new recipe options for damage CR% gauntlets, with roll-count defaults tuned for easier farming targets.
- **Fixed: Custom gear was silently lost on reload in simple/express mode** — manually entered gear pieces were disappearing when reopening the app. A new per-account "Restore custom gear on this device" toggle in the account manager lets you control this per device.
- **Fixed: Substat weight flyout was grouping results incorrectly** — gear is now bucketed correctly by slot, gear set, faction, and substat instead of being collapsed together.
- **Fixed: Apply button stayed disabled after changing rank or rarity in safeguard multi-edit** — you can now change these fields and immediately apply without needing an extra adjustment first.
- **Improved: Safeguard builder rule list — chip selection behavior** — left-clicking a chip now selects it as the only active rule (clearing others); shift-click range selection now anchors correctly and works when selecting upward in the list.

Deutsch:
- **Verbessert: Lategame-Preset-Safeguard-Regeln erweitert und neu organisiert** — auf 133 Regeln gewachsen (vorher 116), jetzt in beschriftete Familien unterteilt — Speed, Debuffer, Damage, Crit Shield, Survivability, Utility, Accessories, Mercurial und Faction Wars — mit visuellen Abschnittstrennern im Safeguard-Builder. Accessory- und Mercurial-Abschnitte sind weiter nach Slot unterteilt (Rings / Amulets / Banners). Regelnamen wurden auf 43 klare Bezeichnungen standardisiert (vorher 80 unterschiedliche Varianten).
- **Verbessert: Einheitliche Rang- und Seltenheitsbehandlung über Safeguards hinweg** — Safeguard- und Rezept-Regeln wenden Rang und Seltenheit jetzt einheitlich an, sodass Rare-Teile gleichrangig geschützt werden statt ausgenommen zu sein.
- **Behoben: Wenn „5-Sterne-Safeguards behalten" deaktiviert ist, begrenzen Artefakt-Regeln jetzt korrekt auf 6-Sterne** — nur Accessories (Rings, Amulets, Banners) bleiben bei 5-Stern; alle Artefakt-Familien (Damage, Debuffer, Crit Shield, Survivability, Speed Set und andere) verhalten sich jetzt wie erwartet.
- **Neu: Midgame-Preset — Damage-CR%-Gauntlet-Rezept-Varianten** — drei neue Rezeptoptionen für Damage-CR%-Gauntlets mit angepassten Würfelanzahl-Standards für leichtere Farming-Ziele.
- **Behoben: Eigene Ausrüstung verschwand beim Neuladen im Simple/Express-Modus** — manuell eingegebene Ausrüstungsteile gingen verloren, wenn die App erneut geöffnet wurde. Ein neuer Schalter „Eigene Ausrüstung auf diesem Gerät wiederherstellen" im Konto-Manager gibt dir geräteweise Kontrolle darüber.
- **Behoben: Das Substat-Gewichte-Flyout gruppierte Ergebnisse falsch** — Ausrüstung wird jetzt korrekt nach Slot, Ausrüstungsset, Fraktion und Substat getrennt, anstatt zusammengefasst zu werden.
- **Behoben: Der Anwenden-Knopf blieb nach dem Ändern von Rang oder Seltenheit im Safeguard-Multi-Edit deaktiviert** — du kannst diese Felder jetzt ändern und sofort anwenden, ohne eine zusätzliche Anpassung vornehmen zu müssen.
- **Verbessert: Chip-Auswahl in der Safeguard-Builder-Regelliste** — ein Linksklick auf einen Chip wählt ihn jetzt als einzige aktive Regel aus (hebt die Auswahl anderer auf); die Shift-Klick-Bereichsauswahl wird jetzt korrekt verankert und funktioniert auch beim Klicken nach oben in der Liste.

## v1.0.36 — 2026-07-07
English:
- **New: Clicking a row in the sell file preview now jumps to that rule in the builder** — recipe rows select the recipe and switch to Recipe Builder; safeguard rows select the safeguard and switch to Safeguard Builder; both scroll the rule into view.
- **Improved: Account switcher rows now have a dedicated auto-push toggle button** — clicking the icon on any account row turns automatic sell-file uploading on or off without opening a dialog. The account's accent color is now shown as a full person icon rather than a small colored square.
- **Improved: Hovering a sell file preview row now highlights the corresponding safeguard chip in the builder** — recipe chips were already highlighted on hover; safeguard chips now follow the same behavior.
- **Fixed: Override markers in the builder no longer float over section headers when a section is collapsed** — the "!" badge is now anchored to its control inside the section and disappears when that section is folded.
- **New: Safeguard "Weight by Rank" now has a tunable main-stat strength** — a factor control in the substat-weights flyout (open it with the tune button beside the chip, which now uses the same split-button layout as the Improvement-chance chip) lets you scale how heavily the main stat counts toward the rank score. The weight cap across all substat and main-stat controls has been raised to 9.9, and holding the +/– buttons down now accelerates through the range.
- **Updated: "Lategame" preset re-tuned for the new main-stat rank weight factor** — every "Weight by Rank" safeguard in the preset now sets an explicit `mainStatRankWeightFactor` of 4.5, so its rank scoring keeps the same relative main-stat influence it always had now that the factor is tunable rather than fixed. A handful of substat weights were also rebalanced alongside this.

Deutsch:
- **Neu: Ein Klick auf eine Zeile in der Verkaufsdatei-Vorschau springt direkt zur zugehörigen Regel im Builder** — Rezept-Zeilen wählen das Rezept aus und wechseln in den Rezept-Builder; Safeguard-Zeilen wählen den Safeguard aus und wechseln in den Safeguard-Builder; beide scrollen die Regel in den sichtbaren Bereich.
- **Verbessert: Konto-Wechsler-Zeilen haben jetzt einen eigenen Auto-Push-Schalter** — ein Klick auf das Symbol in einer Kontozeile schaltet den automatischen Upload der Verkaufsdatei ein oder aus, ohne einen Dialog zu öffnen. Die Akzentfarbe des Kontos wird jetzt als vollständiges Personen-Symbol dargestellt statt als kleines farbiges Quadrat.
- **Verbessert: Das Hovern über eine Zeile in der Verkaufsdatei-Vorschau hebt jetzt auch den zugehörigen Safeguard-Chip im Builder hervor** — Rezept-Chips wurden beim Hovern bereits hervorgehoben; Safeguard-Chips folgen jetzt demselben Verhalten.
- **Behoben: Override-Markierungen im Builder schweben nicht mehr über Abschnitts-Kopfzeilen, wenn ein Abschnitt eingeklappt ist** — das „!"-Abzeichen ist jetzt an sein Steuerelement innerhalb des Abschnitts gebunden und verschwindet, wenn der Abschnitt geschlossen wird.
- **Neu: Safeguard „Nach Rang gewichten" hat jetzt eine einstellbare Hauptstat-Stärke** — ein Faktor-Regler im Substat-Gewichte-Flyout (Tune-Taste neben dem Chip öffnen, der jetzt das gleiche Split-Button-Layout wie der Verbesserungschancen-Chip verwendet) lässt dich skalieren, wie stark der Hauptstat zum Rang-Score beiträgt. Die Gewichts-Obergrenze für alle Substat- und Hauptstat-Regler wurde auf 9,9 angehoben, und das Gedrückthalten der +/–-Knöpfe beschleunigt das Durchlaufen des Bereichs.
- **Aktualisiert: Preset „Lategame" an den neuen Hauptstat-Rang-Gewichtsfaktor angepasst** — jeder „Nach Rang gewichten"-Safeguard im Preset setzt jetzt einen expliziten `mainStatRankWeightFactor` von 4,5, damit die Rang-Bewertung denselben relativen Hauptstat-Einfluss behält wie zuvor, jetzt wo der Faktor einstellbar statt fix ist. Zusätzlich wurden einige Substat-Gewichte überarbeitet.

## v1.0.35 — 2026-07-05
English:
- **New: Multi-account support** — (NOT FINISHED YET) the app can now manage multiple game accounts, each with its own documents, builder settings, gear data, accent color, and auto-push preference. An account switcher in the header (and in simple mode) lets you create, rename, delete, and switch accounts. Existing users' data is automatically moved into a "Default" account on first launch.
- **New: Safeguard "Improve" mode** — a safeguard rule can now keep watching beyond its target piece count, continuing to protect new drops only as long as they still have a realistic chance of beating what you already own. The check runs at each upgrade step, so monitoring stops the moment further improvement becomes unlikely.
- **Improved: Rule evaluation now runs around 25% faster** on typical builds, with the largest rulesets seeing up to a 2× speedup.
- **Improved: Per-account auto-push** — each account independently controls whether its sell file uploads to RSL Helper automatically. Background accounts rebuild their sell file quietly whenever new gear data arrives. Failed background pushes no longer send pop-up toasts; instead a red "Push failed" line appears next to the account in the switcher until the next successful push.
- **Improved: Two browser tabs can now safely run the app with different accounts** — account changes made in one tab no longer conflict with or overwrite a second open tab.
- **Improved: Lategame preset — safeguard count cards now offer a four-step activation mode** — choose from None, Just what I own, Plus missing slots, or Plus likely upgrades when configuring how many pieces a safeguard should cover.
- **Fixed: The restore dialog now shows the Metasets row** when a restore snapshot references metasets that are not present in the current setup.
- **Fixed: Context menu hints you have already dismissed stay dismissed after an app update** — they were resetting to "unseen" on every new release.
- **Fixed: Tutorial recipe preview now shows the correct name for unnamed recipes** — they display their numbered badge rather than "Imported Base Rules."

Deutsch:
- **Neu: Mehrere Spielkonten** — (NOCH niCHT FERTIG) die App verwaltet jetzt mehrere Spielkonten, jedes mit eigenen Dokumenten, Builder-Einstellungen, Ausrüstungsdaten, Akzentfarbe und Auto-Push-Einstellung. Ein Konto-Wechsler in der Kopfzeile (und im Simple-Modus) ermöglicht das Erstellen, Umbenennen, Löschen und Wechseln von Konten. Bestehende Nutzerdaten werden beim ersten Start automatisch in ein „Standard"-Konto übertragen.
- **Neu: Safeguard-Modus „Improve"** — eine Safeguard-Regel kann jetzt auch nach Erreichen der Zielanzahl weiterhin neue Drops überwachen, solange diese noch eine realistische Chance haben, die vorhandene Ausrüstung zu übertreffen. Die Prüfung läuft auf jeder Aufwertungsstufe; die Überwachung endet, sobald eine weitere Verbesserung unwahrscheinlich ist.
- **Verbessert: Regelauswertung rund 25 % schneller** bei typischen Builds; sehr umfangreiche Regelwerke werden bis zu doppelt so schnell verarbeitet.
- **Verbessert: Auto-Push je Konto** — jedes Konto steuert unabhängig, ob seine Verkaufsdatei automatisch in RSL Helper hochgeladen wird. Inaktive Konten bauen ihre Verkaufsdatei still neu auf, sobald neue Ausrüstungsdaten eintreffen. Fehlgeschlagene Hintergrund-Pushes erzeugen keine Pop-up-Meldungen mehr; stattdessen erscheint eine rote „Push fehlgeschlagen"-Zeile neben dem Konto im Wechsler, bis der nächste erfolgreiche Push stattfindet.
- **Verbessert: Zwei Browser-Tabs können die App jetzt sicher mit verschiedenen Konten nutzen** — Kontoänderungen in einem Tab überschreiben oder verlieren keine Änderungen aus einem zweiten geöffneten Tab.
- **Verbessert: Lategame-Preset – Safeguard-Zählkarten haben jetzt einen vierstufigen Aktivierungsmodus** — wählbar zwischen Keine, Nur was ich besitze, Plus fehlende Slots und Plus wahrscheinliche Upgrades.
- **Behoben: Der Wiederherstellungsdialog zeigt jetzt die Metasets-Zeile** wenn ein Wiederherstellungsstand Metasets referenziert, die im aktuellen Dokument nicht vorhanden sind.
- **Behoben: Kontextmenü-Hinweise bleiben nach einem App-Update weggeklickt** — bisher wurden sie bei jedem neuen Release auf „ungesehen" zurückgesetzt.
- **Behoben: Tutorial-Rezept-Vorschau zeigt jetzt den korrekten Namen für unbenannte Rezepte** — sie zeigen ihr nummeriertes Abzeichen statt „Imported Base Rules".

## v1.0.34 — 2026-07-03
English:
- **Fixed: Duplicating a custom piece in Gear Inspector now gives each copy its own independent substats** — a side-effect of how duplicates were created meant all copies shared the same piece identity as their source, causing the weight flyout to show identical substat rows and tooltips regardless of which copy you hovered. Each duplicate is now fully independent.
- **Fixed: Picking an already-used substat in the custom gear editor now swaps the two rows instead of being blocked** — the dropdown previously hid already-used stats; it now keeps them visible and selecting one rearranges the two positions so both substats stay in place with their values intact.
- **Fixed: Renaming a safeguard now immediately updates the label shown on the Gear Inspector rank chip** — the chip was holding onto the old name until the inspector was next opened.
- **Fixed: Clearing a safeguard's name to empty now takes effect** — the change was silently ignored before, leaving the previous name in place.

Deutsch:
- **Behoben: Das Duplizieren eines eigenen Teils im Gear Inspector gibt jetzt jeder Kopie eigene, unabhängige Substats** — als Nebeneffekt der bisherigen Duplizierfunktion teilten alle Kopien dieselbe Teile-Identität wie ihr Ursprungsteil, sodass das Gewichts-Flyout unabhängig davon, welche Kopie man hoverte, immer dieselben Substat-Zeilen und Tooltips anzeigte. Jedes Duplikat ist jetzt vollständig unabhängig.
- **Behoben: Das Auswählen eines bereits verwendeten Substats im Editor für eigene Ausrüstung tauscht jetzt die beiden Zeilen, anstatt blockiert zu werden** — das Dropdown verbarg bisher bereits verwendete Stats; es zeigt sie jetzt und das Auswählen eines solchen tauscht die beiden Positionen, sodass beide Substats mit ihren Werten erhalten bleiben.
- **Behoben: Das Umbenennen eines Safeguards aktualisiert jetzt sofort die Bezeichnung am Rang-Chip im Gear Inspector** — der Chip zeigte bisher den alten Namen, bis der Inspector erneut geöffnet wurde.
- **Behoben: Das Leeren eines Safeguard-Namens wirkt jetzt sofort** — die Änderung wurde bisher still ignoriert und ließ den vorherigen Namen stehen.

## v1.0.33 — 2026-07-01
English:
- **Fixed: Picking a safeguard rule from the rank chip's right-click menu no longer leaves the chip gray or showing the wrong rank** — after selecting a rule, the chip now lights up and displays the rank for the rule you chose, rather than staying dimmed on a different rule with a better numerical rank.

Deutsch:
- **Behoben: Das Auswählen einer Schutzregel über das Rechtsklick-Menü des Rang-Chips lässt den Chip nicht mehr grau erscheinen oder einen falschen Rang anzeigen** — nach der Auswahl leuchtet der Chip jetzt auf und zeigt den Rang der gewählten Regel an, anstatt auf einer anderen Regel mit einem numerisch besseren Rang gedimmt zu bleiben.

## v1.0.32 — 2026-07-01
English:
- **Improved: Gear Inspector safeguard rank chip now shows all candidate rules in its tooltip** — the tooltip previously capped the list at four rules; it now shows every safeguard rule the piece qualifies for, with a scrollable list for longer cases.
- **New: Right-clicking a safeguard rank chip opens a rule picker** — when a piece qualifies for more than one safeguard rule, right-clicking its rank chip shows a menu with all candidate rules and their ranks; clicking any entry jumps directly to that rule.

Deutsch:
- **Verbessert: Der Schutzregel-Rang-Chip im Gear Inspector zeigt jetzt alle Kandidatenregeln im Tooltip** — der Tooltip war bisher auf vier Einträge begrenzt; er zeigt jetzt alle Schutzregeln, für die das Teil in Frage kommt, mit einer scrollbaren Liste bei vielen Einträgen.
- **Neu: Ein Rechtsklick auf den Schutzregel-Rang-Chip öffnet eine Regelauswahl** — wenn ein Teil für mehr als eine Schutzregel in Frage kommt, öffnet ein Rechtsklick auf den Rang-Chip ein Menü mit allen Kandidatenregeln und deren Rängen; ein Klick auf einen Eintrag springt direkt zu dieser Regel.

## v1.0.31 — 2026-06-28
English:
- **New: Lategame preset — Chaos Ore section** — a master question now covers all 14 Chaos Ore recipes with a single toggle; per-rarity conditions let you keep Ore of specific rarities.
- **New: Lategame preset note has collapsible "Optional" sections** — less essential topics can be collapsed to reduce the reading load on first view.
- **New: Preset name fields and save dialogs now suggest a name and include a dice button** — dialogs open ready to save with a pre-filled name; clicking the dice picks a random one.
- **New: Preset rows and flyouts warn when a saved answer is no longer available for the current note** — a badge appears on the preset row and affected flyout lines; questions removed from the note are gathered into a "Not available for this note" section so nothing is lost silently.
- **Improved: Autosave now restores with the current bundled preset rather than an older saved copy** — your overrides and per-session tuning are preserved; stale preset data no longer overwrites updated bundled content on launch.
- **Improved: Safeguard candidate list redesigned** — rank-protected and chance-protected pieces are now separated by a labeled amber divider; chance-protected items get a hollow icon; gear matching the active rule is flagged with a small amber indicator; all substats are shown per row (rule-selected first, then the rest at reduced opacity) rather than only the rule-selected ones.
- **Improved: Gear Inspector sort now correctly ranks 6★ artifacts above 5★ pieces with equal substats on glyphable stats** — the ordering now matches the keep/sell verdict.
- **Improved: Tooltip text simplified across several controls** — improvement-chance, safeguard rank, normalized sort, and related elements each have a shorter, clearer tooltip.
- **Improved: Lategame and beginner preset notes are now fully translated into German.**
- **Fixed: Preset labels in flyouts and rows now appear in your active UI language** — they were always shown in English regardless of the selected language.
- **Fixed: Several German UI labels that were previously untranslated now display correctly** — including "Gear Inspector Main Stat," "Analytics Chart Main Stat," and related strings.
- **Fixed: Missing translations filled in across Spanish, French, Italian, Portuguese, Russian, Turkish, and Ukrainian** — around 16–20 entries per locale; terminology is now consistent within each language.
- **Fixed: Clicking in the note preview pane no longer jumps your cursor to the end of the editor;** scroll sync between the editor and preview is improved for long notes.
- Slot names, help text, and analytics now use "artifact" in place of "armor."

Deutsch:
- **Neu: Lategame-Preset – Chaos-Erz-Bereich** — eine neue Hauptfrage deckt alle 14 Chaos-Erz-Rezepte mit einem einzigen Schalter ab; Seltenheitsbedingungen erlauben es, Erz bestimmter Seltenheitsstufen zu behalten.
- **Neu: Die Lategame-Preset-Notiz hat jetzt einklappbare „Optional"-Bereiche** — weniger wichtige Themen können weggeklappt werden, um den Einstieg übersichtlicher zu halten.
- **Neu: Preset-Namensfelder und Speicherdialoge schlagen jetzt einen Namen vor und enthalten einen Würfel-Button** — Dialoge öffnen sich mit einem vorausgefüllten Namen; ein Klick auf den Würfel wählt einen zufälligen Namen.
- **Neu: Preset-Zeilen und -Flyouts zeigen eine Warnung, wenn eine gespeicherte Antwort für die aktuelle Notiz nicht mehr verfügbar ist** — ein Abzeichen erscheint an der Preset-Zeile und den betroffenen Flyout-Zeilen; aus der Notiz entfernte Fragen werden in einem Bereich „Für diese Notiz nicht verfügbar" zusammengefasst.
- **Verbessert: Autospeicherung wird jetzt mit dem aktuellen gebündelten Preset wiederhergestellt statt mit einer älteren gespeicherten Kopie** — Overrides und Sitzungseinstellungen bleiben erhalten; veraltete Preset-Daten überschreiben beim Start keine aktuellen gebündelten Inhalte mehr.
- **Verbessert: Safeguard-Kandidatenliste neu gestaltet** — rang-geschützte und chance-geschützte Teile werden jetzt durch eine bernsteinfarbene Trennzeile mit Beschriftung getrennt; chance-geschützte Teile erhalten ein Kreiskontur-Icon; Gear, das zur aktiven Regel passt, wird mit einem kleinen bernsteinfarbenen Indikator markiert; alle Substats werden pro Zeile angezeigt (regelausgewählte zuerst, dann die übrigen in reduzierter Deckkraft).
- **Verbessert: Die Sortierung im Gear Inspector stuft 6★-Artefakte jetzt korrekt über 5★-Teile mit gleichen Substats bei glyphengeeigneten Stats ein** — die Reihenfolge entspricht nun dem Behalten/Verkaufen-Urteil.
- **Verbessert: Tooltip-Texte bei mehreren Steuerelementen vereinfacht** — Verbesserungschance, Safeguard-Rang, normalisierte Sortierung und verwandte Elemente haben jeweils kürzere, klarere Tooltips.
- **Verbessert: Lategame- und Anfänger-Preset-Notizen sind jetzt vollständig auf Deutsch übersetzt.**
- **Behoben: Preset-Labels in Flyouts und Zeilen werden jetzt in der aktiven Sprache der Benutzeroberfläche angezeigt** — sie wurden bisher immer auf Englisch dargestellt, unabhängig von der gewählten Sprache.
- **Behoben: Mehrere deutsche UI-Labels, die zuvor nicht übersetzt waren, werden jetzt korrekt angezeigt** — darunter „Gear Inspector Main Stat", „Analytics Chart Main Stat" und verwandte Texte.
- **Behoben: Fehlende Übersetzungen für Spanisch, Französisch, Italienisch, Portugiesisch, Russisch, Türkisch und Ukrainisch ergänzt** — je rund 16–20 fehlende Einträge pro Sprache; Terminologie ist jetzt innerhalb jeder Sprache einheitlich.
- **Behoben: Ein Klick in den Notiz-Vorschaubereich springt den Cursor nicht mehr ans Ende des Editors;** die Scroll-Synchronisation zwischen Editor und Vorschau ist für längere Notizen verbessert.
- Slot-Namen, Hilfetext und Analyse verwenden jetzt „Artefakt" anstelle von „Armor"; „Gear" wird in der deutschen Oberfläche konsistent als „Ausrüstung" bezeichnet.

## v1.0.30 — 2026-06-27
English:
- **Fixed: The "first match" chip in Gear Inspector could display an entirely wrong rule name for pieces already kept by a recipe** — for example, a Speed Weapon kept by a recipe would show a Banner safeguard ("Protect: Best SPD Banner") as its match chip instead of the correct rule. A side-effect of the evaluation shortcut that skips re-checking recipe-confirmed pieces when safeguards are active, which left a rule index pointing at the wrong position once safeguard rules were inserted ahead of the recipe list. The keep/sell verdict and the exported sell file were always correct; only the chip label, color, and jump target were wrong.

Deutsch:
- **Behoben: Der „First Match"-Chip im Gear Inspector konnte für Teile, die bereits durch ein Rezept behalten werden, eine völlig falsche Regelbezeichnung anzeigen** — zum Beispiel zeigte eine Geschwindigkeitswaffe, die durch ein Rezept behalten wird, als Match-Chip einen Banner-Safeguard („Protect: Best SPD Banner") anstelle der korrekten Regel. Ein Nebeneffekt der Auswertungsoptimierung, die das erneute Prüfen von rezeptbestätigten Teilen bei aktiven Safeguards überspringt: Ein Regelindex verwies auf die falsche Position, sobald Safeguard-Regeln vor der Rezeptliste eingefügt wurden. Das Behalten/Verkaufen-Urteil und die exportierte Verkaufsdatei waren immer korrekt; nur Bezeichnung, Farbe und Sprungziel des Chips waren falsch.

## v1.0.29 — 2026-06-25
English:
- **New: The Sellfile Preview now shows a labeled divider above each group of rules** — a slim header row appears before each recipe block, each safeguard block, the Final Sell block, and the imported-base block. Each divider shows the group's icon, name, and how many rules are in that group. Dividers cannot be selected or interacted with.
- **Fixed: The "first match" chip in Gear Inspector showed a recipe name for pieces matched by a safeguard rule** — the chip's label and index pointed to a recipe while its color, tooltip, and "open safeguard" link all pointed to a safeguard, making it appear inconsistent. A side-effect of how safeguard rules carry their originating recipe's identity internally, the chip now always shows the safeguard name, ordinal, and color when the match came from a safeguard.

Deutsch:
- **Neu: Die Verkaufsdatei-Vorschau zeigt jetzt eine beschriftete Trennzeile über jeder Regelgruppe** — vor jedem Rezept-Block, jedem Safeguard-Block, dem „Final Sell"-Block und dem importierten Basis-Block erscheint eine schmale Kopfzeile. Jede Trennzeile zeigt das Symbol der Gruppe, ihren Namen und wie viele Regeln sie enthält. Trennzeilen können nicht ausgewählt oder angeklickt werden.
- **Behoben: Der „First Match"-Chip im Gear Inspector zeigte einen Rezeptnamen für Teile, die durch eine Safeguard-Regel gematcht wurden** — Bezeichnung und Index des Chips zeigten auf ein Rezept, während Farbe, Tooltip und der „Safeguard öffnen"-Link auf einen Safeguard verwiesen, was den Chip widersprüchlich wirken ließ. Als Nebeneffekt davon, dass Safeguard-Regeln intern die Identität ihres Ursprungsrezepts tragen, zeigt der Chip jetzt immer den Safeguard-Namen, die Ordinalzahl und die Farbe, wenn der Match von einem Safeguard stammt.

## v1.0.28 — 2026-06-23
English:
- **Fixed: The simple view could show a blank screen on first launch inside RSL Helper's browser** — launching via RSL Helper with no previous session saved sometimes left the screen entirely black. A side-effect of earlier improvements that added browser storage handling caused two separate startup paths to fail silently in storage-restricted environments. Both are resolved; the simple view now opens reliably even without a prior save.

Deutsch:
- **Behoben: Die einfache Ansicht konnte beim ersten Start im RSL-Helper-Browser einen schwarzen Bildschirm zeigen** — wurde die App über RSL Helper ohne eine vorherige gespeicherte Sitzung gestartet, blieb der Bildschirm manchmal komplett schwarz. Ein Nebeneffekt früherer Verbesserungen an der Browser-Speicherbehandlung ließ zwei separate Startpfade in speicherbeschränkten Umgebungen lautlos fehlschlagen. Beide sind behoben; die einfaceh Ansicht öffnet sich jetzt zuverlässig, auch ohne vorherigen Speicherstand.

## v1.0.27 — 2026-06-22
English:
- **New: Rarity tier colors are now customizable** — each of the six rarity tiers has an editable color in the new "Color settings" flyout (previously "Manage Colors"). Rarity borders, gear-card frames, and chart fills use your chosen colors.
- **New: Rarity labels ("Mythical", "Epic", etc.) now appear colored throughout the app** — gear lists, filter chips, summaries, and tooltips all pick up the rarity color by default.
- **New: Stat and substat names are now colored in more places** — names appear tinted in dropdowns, filter panels, table cells, and rule summaries, not just in chips and the sell file preview.
- **New: Color scope can now be set independently for each color group** — Stats, Slots, and Rarity each have their own step selector in Color Settings: Off, Controls, Text, or Everything.
- **Lategame/Endgame preset: Dedicated Bomber safeguard rules added** — the preset now includes separate safeguard rules to protect gear used by Bomber-type champions.

Deutsch:
- **Neu: Farben der Seltenheitsstufen sind jetzt anpassbar** — jede der sechs Seltenheitsstufen hat eine eigene Farbe im neuen Bereich „Farbeinstellungen" (vorher „Farben verwalten"). Seltenheits-Rahmen, Gear-Karten-Ränder und Diagrammfüllungen verwenden deine gewählten Farben.
- **Neu: Seltenheits-Labels („Mythisch", „Episch" usw.) erscheinen jetzt farbig in der gesamten App** — Gear-Listen, Filterchips, Zusammenfassungen und Tooltips übernehmen die Seltenheitsfarbe standardmäßig.
- **Neu: Stat- und Substat-Namen werden jetzt an mehr Stellen eingefärbt** — Namen erscheinen getönt in Dropdowns, Filterpanels, Tabellenzellen und Regelzusammenfassungen, nicht nur in Chips und der Verkaufsdatei-Vorschau.
- **Neu: Farbbereich kann jetzt unabhängig für jede Farbgruppe eingestellt werden** — Stats, Slots und Seltenheit haben jeweils einen eigenen Stufenwähler in den Farbeinstellungen: Aus, Steuerungen, Text oder Alles.
- **Lategame/Endgame-Preset: Dedizierte Bomber-Safeguard-Regeln hinzugefügt** — das Preset enthält jetzt separate Safeguard-Regeln zum Schutz von Gear, das von Bomber-Champions verwendet wird.

## v1.0.26 — 2026-06-22
English:
- **Fixed: Switching to the full app from the simple view was forgotten every time the app restarted inside RSL Helper's built-in browser** — you now only need to switch once; the choice is remembered reliably across relaunches.
- **Fixed: Saved note settings (such as improvement-chance overrides) were silently lost when restoring a session inside RSL Helper's built-in browser** — they are now reapplied correctly after your previous SFC finishes loading.

Deutsch:
- **Behoben: Die Wahl, vom einfachen Modus zur vollständigen App zu wechseln, wurde bei jedem Neustart im eingebetteten Browser von RSL Helper vergessen** — der Wechsel muss jetzt nur einmal vorgenommen werden; die Einstellung wird zuverlässig über Neustarts hinweg behalten.
- **Behoben: Gespeicherte Notizeinstellungen (z. B. Verbesserungschance-Overrides) gingen beim Wiederherstellen einer Sitzung im eingebetteten Browser von RSL Helper still verloren** — sie werden jetzt korrekt angewendet, nachdem deine vorherige SFC vollständig geladen wurde.

## v1.0.25 — 2026-06-21
English:
- **Improved: Gear evaluation with safeguards active is now faster** — when safeguards are enabled, the app now skips re-checking gear that is already kept by your recipes, since those pieces cannot be affected by safeguard rules. Accounts with many safeguard rules and large gear collections will notice the biggest speedup. Results are unchanged.

Deutsch:
- **Verbessert: Gear-Auswertung mit aktiven Safeguards ist jetzt schneller** — bei aktiven Safeguards überspringt die App das erneute Prüfen von Gear, das bereits durch Rezepte behalten wird, da diese Teile nicht durch Safeguard-Regeln beeinflusst werden können. Konten mit vielen Safeguard-Regeln und großen Gear-Sammlungen werden die größte Verbesserung bemerken. Die Ergebnisse sind unverändert.

## v1.0.24 — 2026-06-21
English:
- **New: Gear slot icons now show a subtle color tint** — armor slots (Weapon, Helmet, Shield, Gauntlets, Chestplate, Boots) appear in pale gold; accessory slots (Ring, Amulet, Banner) appear in pale blue. The tints adapt to the active theme and can be customized or reset in Manage Colors. They follow the "Color stats & slots" toggle in display settings.
- **Fixed: Gear waiting in your RSL Helper inbox was not counted toward safeguard protection** — items delivered as in-game mail but not yet collected were quietly passed over, causing safeguard to generate extra placeholder keep rules until the gear appeared in a later sync.

Deutsch:
- **Neu: Gear-Slot-Icons zeigen jetzt eine subtile Farbtönung** — Rüstungs-Slots (Waffe, Helm, Schild, Handschuhe, Brustpanzer, Stiefel) erscheinen in hellem Gold; Accessoire-Slots (Ring, Amulett, Banner) in hellem Blau. Die Tönung passt sich dem aktiven Theme an und kann in „Farben verwalten" angepasst oder zurückgesetzt werden. Sie folgt dem Schalter „Stats & Slots einfärben" in den Anzeigeeinstellungen.
- **Behoben: Gear im RSL-Helper-Posteingang wurde nicht für den Safeguard-Schutz berücksichtigt** — Gegenstände, die als In-Game-Post eingegangen, aber noch nicht abgeholt wurden, wurden stillschweigend übergangen; dadurch erzeugte der Safeguard zusätzliche Platzhalter-Keep-Regeln, bis das Gear bei einer späteren Synchronisierung ankam.

## v1.0.23 — 2026-06-20
English:
- **New: Load SFC and Export/Push buttons now have a dropdown chevron (▾)** — clicking the chevron opens the preset and options menu; clicking the main button area directly opens the file picker or exports. On the first click each session, the Load SFC button opens the menu automatically to help you discover presets. The nudge to right-click is gone.
- **New: The unsaved-changes dot on the Save and Export/Push buttons now shows a "not saved since [time]" tooltip** — hover the dot to see at a glance how long ago you last saved or pushed.
- **New: Safeguard rank overlay cycle order changed to Off → Group → Safeguard → Both** — the Bucket rank step now comes before the overall Safeguard rank. The chip's color, number, and click target are now always consistent with each other and with the tooltip rows.
- **New: Safeguard rules now have a "Weight by Rank" toggle** — when enabled, higher-rank pieces get a scoring edge on their main stat, calibrated per slot and main stat, so a 6★ can edge out a same-mainstat 5★ with only slightly better substats.
- **Improved: Bundled preset files in the Load SFC menu are now named "Midgame / Lategame / Endgame Sample" and "Beginner Sample"** instead of the old names they previously showed.
- **Fixed: Clicking outside the note or pressing Escape no longer accidentally closes it when it is shown without a close button.**

Deutsch:
- **Neu: Lade-SFC- und Export/Push-Schaltflächen haben jetzt einen Dropdown-Pfeil (▾)** — ein Klick auf den Pfeil öffnet das Preset- und Optionsmenü; ein Klick auf den Hauptbereich öffnet direkt den Datei-Auswahldialog oder exportiert. Beim ersten Klick einer Sitzung öffnet die Lade-SFC-Schaltfläche automatisch das Menü, um Presets leichter zu entdecken. Der Hinweis auf Rechtsklick entfällt.
- **Neu: Der Punkt für ungespeicherte Änderungen an Speichern- und Export/Push-Schaltflächen zeigt jetzt ein Tooltip „Nicht gespeichert seit [Zeit]"** — beim Hovern siehst du auf einen Blick, wie lange es seit dem letzten Speichern oder Push her ist.
- **Neu: Der Zyklus des Safeguard-Rang-Overlays folgt jetzt der Reihenfolge Aus → Gruppe → Safeguard → Beides** — der Gruppen-Rang-Modus kommt jetzt vor dem Gesamt-Safeguard-Rang. Farbe, Zahl und Klickziel des Chips stimmen jetzt immer miteinander und mit den Tooltip-Zeilen überein.
- **Neu: Safeguard-Regeln haben jetzt einen Schalter „Nach Rang gewichten"** — ist er aktiviert, erhalten höherstufige Teile einen Scoring-Vorteil auf ihren Hauptstat, der je nach Slot und Hauptstat kalibriert ist, sodass ein 6★-Teil ein gleichnamiges 5★-Teil mit nur minimal besseren Substats verdrängen kann.
- **Verbessert: Gebündelte Preset-Dateien im Lade-SFC-Menü heißen jetzt „Midgame / Lategame / Endgame Sample" und „Beginner Sample"** statt der bisherigen alten Dateinamen.
- **Behoben: Ein Klick außerhalb der Notiz oder Drücken der Escape-Taste schließt sie nicht mehr versehentlich, wenn sie ohne Schließen-Schaltfläche angezeigt wird.**

## v1.0.22 — 2026-06-20
English:
- **New: Builder and preview panels now appear side by side at most window sizes** — the layout no longer requires a wide screen to activate; zoom adjusts automatically to fit both the width and height of your browser window, so no space is wasted on the sides. At very small windows the layout stacks normally.
- **New: Side-by-side zoom can be configured in the display settings flyout** — a toggle turns the automatic side-by-side mode on or off, and a slider sets the minimum zoom level below which the layout switches back to stacked instead of shrinking further.
- **New: Safeguard candidate list can be focused on one bucket** — clicking a rank or improvement-chance chip in the Gear Inspector opens the safeguard flyout already narrowed to that piece's slot/set/faction group, so you can compare it directly against its competition. Ranks are recalculated relative to the focused bucket while focus is active.
- **New: Safeguard candidate list now shows an improvement-chance column** — the predicted improvement chance for each candidate appears alongside its score.

Deutsch:
- **Neu: Builder und Vorschau erscheinen jetzt bei den meisten Fenstergrößen nebeneinander** — das Layout benötigt keinen breiten Bildschirm mehr; der Zoom passt sich automatisch an Breite und Höhe des Browserfensters an, sodass kein Platz verschwendet wird. Bei sehr kleinen Fenstern wird das Layout normal gestapelt.
- **Neu: Nebeneinander-Zoom ist im Anzeigeeinstellungen-Flyout konfigurierbar** — ein Schalter aktiviert oder deaktiviert den automatischen Nebeneinander-Modus, und ein Schieberegler legt den Mindestzoom fest, unterhalb dessen das Layout statt weiter zu schrumpfen wieder gestapelt wird.
- **Neu: Safeguard-Kandidatenliste kann auf eine Gruppe gefokust werden** — ein Klick auf einen Rang- oder Verbesserungschance-Chip im Gear Inspector öffnet das Safeguard-Flyout bereits auf die Slot-/Set-/Fraktion-Gruppe des Teils eingeschränkt, sodass ein direkter Vergleich mit seiner Konkurrenz möglich ist. Ränge werden im Fokus-Modus relativ zur Gruppe neu berechnet.
- **Neu: Safeguard-Kandidatenliste zeigt jetzt eine Verbesserungschance-Spalte** — die vorhergesagte Verbesserungschance jedes Kandidaten erscheint neben seiner Bewertung.

## v1.0.21 — 2026-06-19
English:
- **New: "RSLH" theme option** — a third theme alongside Dark and Light.
- **New: Theme editor exposes additional color and font options** — you can now adjust the info color, primary, secondary, and disabled text colors, the UI and code font families, and the scrollbar thumb color directly from the theme popout.
- **New: Safeguard Rank overlay expanded to a four-mode cycle** — replaces the on/off toggle with four steps: Off, Rank (overall position among all safeguarded pieces), Bucket Rank (position within the piece's slot/set/faction group), and Rank + Group (both at once). Green = kept, red = would be sold.
- **New: Pieces ranked by unselected safeguard rules now show their rank in the overlay** — such chips appear faded with a dotted border and a tooltip identifying the source rule, so rank information is no longer hidden just because the rule is not in the active filter.
- **Midgame/Lategame/Endgame preset: SPD substat weight increased in safeguard rules** — gear with a Speed roll is now scored more aggressively when ranking borderline pieces under safeguard rules.

Deutsch:
- **Neu: Theme-Option „RSLH"** — ein drittes Theme neben Dunkel und Hell.
- **Neu: Theme-Editor bietet weitere Farb- und Schriftoptionen** — im Theme-Popout lassen sich jetzt Info-Farbe, primäre, sekundäre und deaktivierte Textfarbe, UI- und Code-Schriftfamilien sowie die Scrollbar-Daumenfarbe anpassen.
- **Neu: Safeguard-Rang-Overlay auf vier Modi erweitert** — der Ein/Aus-Schalter wird durch vier Schritte ersetzt: Aus, Rang (Gesamtposition aller safeguardeten Teile), Gruppen-Rang (Position innerhalb der Slot-/Set-/Fraktion-Gruppe des Teils) und Rang + Gruppe (beides gleichzeitig). Grün = behalten, rot = würde verkauft.
- **Neu: Teile, die durch nicht ausgewählte Safeguard-Regeln gerankt werden, zeigen jetzt ihren Rang im Overlay** — solche Chips erscheinen gedimmt mit gestricheltem Rand und einem Tooltip, der die Quellregel benennt; Ranginformationen gehen nicht mehr verloren, wenn die Regel nicht im aktiven Filter ist.
- **Midgame/Lategame/Endgame-Preset: SPD-Substat-Gewichtung in Safeguard-Regeln erhöht** — Gear mit Speed-Roll wird bei knapper Bewertung unter Safeguard-Regeln jetzt stärker priorisiert.

## v1.0.20 — 2026-06-16
English:
- **New: Improvement-chance override is now a continuous slider with named stops and an on/off toggle** — the improvement-chance question in notes uses a slider (range 0–90) with labeled marks (Soft 10 / Balanced 25 / Moderate 33 / Strict 50) and a Yes/No toggle, replacing the previous radio buttons; thresholds were recalibrated from real account data.
- **New: Gear Analytics now includes an Improvement Chance histogram** — a click-to-filter bar chart groups safeguarded gear by its predicted improvement chance in 10-point bands; clicking a bar cross-filters the rest of the Gear Analytics view to that range.
- **New: Selecting an account tier in the lategame note now automatically sets the improvement-chance sliders** — each tier applies its own values: Midgame sets artifacts to 25% and accessories to 50%; Lategame sets artifacts to 33% and accessories to 50%; Endgame sets both to 50%; Endgame+ sets both to 60%.
- **New: Saved override sets now have an overwrite button** — replaces the set's stored selections with the current choices without changing the set's name.
- **Fixed: The dungeon simulator in the note panel no longer restarts when RSL Helper sends routine background data updates** — routine gear-data pushes no longer interrupt or reset an active or completed simulation.
- **Fixed: Disabling all recipes or editing a recipe now immediately updates the sell file preview and Gear Inspector** — a caching problem (born of an earlier optimization to make rule evaluation as fast as possible) meant changes weren't reflected until something else triggered a rebuild.
- **Fixed: The "hide gear update message" preference now persists across page reloads** — the choice to dismiss the RSL Helper gear-update notification previously reset every time the page was reloaded.
- **Fixed: Slider values in saved override sets are now preserved correctly when saving and loading** — slider answers were previously lost on a save/load round-trip.
- **Fixed: Note editor preview scroll sync now works correctly in side-by-side mode when the browser is zoomed** — the editor and preview pane stay aligned at all zoom levels, including when scrolled to the very beginning of the document.
- **Midgame/Lategame/Endgame preset: slow debuffer safeguards can now opt out of the improvement-chance filter independently** — pieces needed for champions with carefully controlled Speed are tagged so the improvement-chance question can be disabled for that group without affecting other safeguards.
- **Midgame/Lategame/Endgame preset: Generic SPD recipe updated** — now targets Weapons, Helmets, Shields, and Banners with SPD as a required substat (≥3 rolls) **plus** at least 2 additional substats from CDMG%, CR%, ACC, RES, HP%, ATK%, DEF%.

Deutsch:
- **Neu: Override für Verbesserungschance ist jetzt ein Schieberegler mit benannten Stufen und Ein/Aus-Schalter** — die Verbesserungschance-Frage in Notizen verwendet einen Schieberegler (Bereich 0–90) mit beschrifteten Markierungen (Soft 10 / Balanced 25 / Moderate 33 / Strict 50) und einem Ja/Nein-Schalter anstelle der bisherigen Auswahloptionen; die Schwellenwerte wurden anhand echter Kontodaten neu kalibriert.
- **Neu: Gear Analytics zeigt jetzt ein Verbesserungschance-Histogramm** — ein klickbares Balkendiagramm gruppiert safeguarded Ausrüstung nach prognostizierter Verbesserungschance in 10-Punkte-Bereiche; ein Klick auf einen Balken filtert die übrigen Gear-Analytics-Ansichten auf diesen Bereich.
- **Neu: Die Auswahl einer Kontostufe in der Lategame-Notiz setzt jetzt automatisch die Verbesserungschance-Schieberegler** — jede Stufe verwendet eigene Werte: Mittelspiel setzt Artefakte auf 25% und Accessoires auf 50%; Lategame setzt Artefakte auf 33% und Accessoires auf 50%; Endgame setzt beide auf 50%; Endgame+ setzt beide auf 60%.
- **Neu: Gespeicherte Override-Sets haben jetzt eine Überschreiben-Schaltfläche** — ersetzt die gespeicherten Auswahlen durch die aktuellen Einstellungen, ohne den Namen des Sets zu ändern.
- **Behoben: Dungeon-Simulator im Notiz-Panel startet nicht mehr neu, wenn RSL Helper Hintergrund-Updates schickt** — routinemäßige Gear-Datenpushes unterbrechen oder setzen eine laufende oder abgeschlossene Simulation nicht mehr zurück.
- **Behoben: Das Deaktivieren aller Rezepte oder das Bearbeiten eines Rezepts aktualisiert jetzt sofort die Verkaufsdatei-Vorschau und den Gear Inspector** — ein Caching-Problem (das durch eine frühere Optimierung für schnellere Regelauswertung entstand) sorgte dafür, dass Änderungen erst sichtbar wurden, wenn etwas anderes einen Neuaufbau auslöste.
- **Behoben: Die Einstellung „Update-Meldung ausblenden" in der Gear-Datenbank bleibt nach Seiten-Reload erhalten** — die Auswahl, die RSL-Helper-Gear-Update-Benachrichtigung auszublenden, wurde zuvor bei jedem Seiten-Reload zurückgesetzt.
- **Behoben: Schieberegler-Werte in gespeicherten Override-Sets bleiben jetzt beim Speichern und Laden korrekt erhalten** — Schieberegler-Antworten gingen zuvor bei einem Speichern/Laden-Vorgang verloren.
- **Behoben: Die Vorschau-Scroll-Synchronisation im Notiz-Editor funktioniert jetzt korrekt im nebeneinander-Modus bei gezoomtem Browser** — Editor und Vorschau bleiben bei allen Zoomstufen ausgerichtet, auch ganz oben im Dokument.
- **Midgame/Lategame/Endgame-Preset: Slow-Debuffer-Safeguards können jetzt unabhängig vom Verbesserungschance-Filter ausgeschlossen werden** — Teile für Champions mit kontrollierter Geschwindigkeit sind getaggt, damit die Verbesserungschance-Frage für diese Gruppe deaktiviert werden kann, ohne andere Safeguards zu beeinflussen.
- **Midgame/Lategame/Endgame-Preset: Allgemeines SPD Rezept aktualisiert** — zielt jetzt auf Waffen, Helme, Schilde und Banner mit SPD als Pflicht-Substat (≥3 Rolls) **sowie** mindestens 2 weiteren Substats aus CDMG%, CR%, ACC, RES, HP%, ATK%, DEF%.

## v1.0.19 — 2026-06-14
English:
- **New: Dynamic override answer sets can now be saved, loaded, and deleted in the note dialog** — named sets capture all recipe and safeguard question selections and work in both view and edit mode; an info tooltip on each saved set lists every question and its selected answer. Existing SFC files saved with the previous format load correctly.
- **New: Dynamic override controls in the note editor now show an info tooltip (edit mode only)** — hovering a control reveals its DSL identifier, which constraints it forces, and a reconstructed preview of the DSL it changes; clicking the control jumps to its definition in the editor with a brief highlight.
- **Improved: Note editor scroll sync is now marker-anchored** — the editor and preview pane stay aligned even for tall option cards that previously caused the ratio-based sync to lose its position.
- **Fixed: Champion icons were blank on all gear pieces after connecting to RSL Helper** — the link between a gear piece and its equipped champion was not being applied because a guard incorrectly treated unequipped gear (champion ID 0) the same as already-linked gear.
- **Fixed: Fresh gear data from RSL Helper could be overwritten by a stale autosave restore** — gear that arrived while the Help/README screen was open before the restore prompt appeared was at risk of being replaced by the older draft; incoming endpoint gear is now always treated as authoritative.
- **Fixed: The "unsaved changes" badge appeared incorrectly when RSL Helper sent routine gear-database updates that did not change any sell decision** — the badge now only activates when at least one piece's outcome has actually changed.
- **Fixed: Editing safeguard substat-match or improvement-chance fields did not update the exported sell file** — the export could remain stale until an unrelated change triggered a full rebuild.
- **Fixed: Saving weight changes in the safeguard builder (without other edits) was silently ignored** — weight-only edits now save correctly and are recorded in the undo history.

Deutsch:
- **Neu: Override-Sets für Dynamic Overrides können jetzt im Notiz-Dialog gespeichert, geladen und gelöscht werden** — benannte Sets erfassen alle Rezept- und Safeguard-Fragenauswahlen und funktionieren in Ansichts- und Bearbeitungsmodus; ein Info-Tooltip auf jedem gespeicherten Set listet jede Frage und die gewählte Antwort auf. Bestehende SFC-Dateien im alten Format werden weiterhin korrekt geladen.
- **Neu: Override-Controls im Notiz-Editor zeigen jetzt ein Info-Tooltip (nur im Bearbeitungsmodus)** — beim Hovern erscheint der DSL-Bezeichner des Controls, welche Einschränkungen es erzwingt und eine rekonstruierte Vorschau des DSL-Blocks, den es verändert; ein Klick springt zur entsprechenden Zeile im Editor mit kurzem Highlight.
- **Behoben: Champion-Icons waren auf allen Gear-Teilen leer nach dem Verbinden mit RSL Helper** — die Verknüpfung zwischen einem Gear-Teil und dem ausgerüsteten Champion wurde nicht angewandt, da eine Prüfung nicht ausgerüstetes Gear (Champion-ID 0) fälschlicherweise wie bereits verknüpftes Gear behandelte.
- **Behoben: Frische Gear-Daten von RSL Helper konnten durch eine veraltete Autosave-Wiederherstellung überschrieben werden** — Gear, das während des Hilfe-/README-Bildschirms ankam, bevor der Wiederherstellungsdialog erschien, konnte durch den älteren Entwurf ersetzt werden; eingehende Endpoint-Daten gelten jetzt immer als autoritativ.
- **Behoben: Das „ungespeicherte Änderungen"-Badge erschien fälschlicherweise, wenn RSL Helper routinemäßige Gear-Datenbank-Updates sendete, die keine Verkaufsentscheidung änderten** — das Badge wird jetzt nur aktiviert, wenn sich das Ergebnis mindestens eines Teils tatsächlich geändert hat.
- **Behoben: Das Bearbeiten der Substat-Match- oder Verbesserungschance-Felder in Safeguard-Regeln aktualisierte die exportierte Verkaufsdatei nicht** — der Export konnte veraltet bleiben, bis eine unabhängige Änderung einen vollständigen Neuaufbau auslöste.
- **Behoben: Das Speichern von Gewichtsänderungen im Safeguard-Builder (ohne andere Bearbeitungen) wurde stillschweigend ignoriert** — reine Gewichtsänderungen werden jetzt korrekt gespeichert und in der Undo-Historie erfasst.

## v1.0.18 — 2026-06-08
English:
- **Fixed: Gear data from RSL Helper is no longer lost when it arrives while the restore dialog is open** — the app now re-requests a fresh snapshot from RSL Helper as soon as the restore dialog closes (whether you restore or dismiss it), so you do not need to manually reconnect to pick up changes that arrived during the prompt.
- **Fixed: Lategame preset "Mythical only" Chaos Ore option now actually restricts to Mythical pieces** — the option had the same effect as "≥ Legendary", keeping any 6★ piece that could reach 4× on a substat; it now correctly requires a 5× potential so only Mythical-rarity gear qualifies.
- **Lategame preset: the three Chaos Ore questions are now per-rarity checkboxes** — the bundled radio choices (≥Epic / ≥Legendary / level-cap / off) are replaced by independent Epic / Legendary / Mythical toggles, plus a separate "keep only already-rolled (level 12–16)" checkbox and the existing "Gauntlets, Chestplate, and Boots are ignored" checkbox as overall per-question modifiers.

Deutsch:
- **Behoben: Gear-Daten von RSL Helper gehen nicht mehr verloren, wenn sie während des Wiederherstellungsdialogs ankommen** — die App fordert nach dem Schließen des Wiederherstellungsdialogs (egal ob wiederhergestellt oder verworfen) automatisch einen frischen Snapshot von RSL Helper an, sodass kein manuelles Neuverbinden erforderlich ist.
- **Behoben: Die Option „Nur Mythical" beim Chaos-Erz im Lategame-Preset schränkt jetzt tatsächlich auf Mythical-Teile ein** — die Option hatte denselben Effekt wie „≥ Legendary" und behielt jedes 6★-Teil, das 4× auf einem Substat erreichen könnte; sie fordert jetzt korrekt ein 5×-Potenzial, sodass nur Mythical-Teile erfasst werden.
- **Lategame-Preset: die drei Chaos-Erz-Fragen sind jetzt Checkboxen pro Seltenheit** — die gebündelten Radio-Optionen (≥Epic / ≥Legendary / Level-Begrenzung / aus) werden durch unabhängige Schalter für Epic / Legendary / Mythical ersetzt, dazu eine separate Checkbox „Nur bereits gerollte Teile behalten (Level 12–16)" und die bestehende Checkbox „Handschuhe, Brustplatte und Stiefel werden ignoriert" als übergeordnete Modifikatoren je Frage.

## v1.0.17 — 2026-06-06
English:
- **New: Gear Diff — before/after comparison showing exactly what changed after editing rules** — a "Diff" toggle in the Gear Inspector header opens a side-by-side split view: the left (before) pane shows each group's verdict counts at the reference point, the right (after) pane shows what the current rules produce. A signed delta chip (±sold / ±kept / ±safeguarded) stays visible next to the Diff button even when the split view is closed, so you always know whether a meaningful difference exists. Selecting a piece in one pane highlights the same piece in the other. The reference can be pinned manually ("Set reference") or updated automatically whenever recipe or safeguard rules change; loading a sell file from disk also triggers a diff against whatever was loaded before.
- **New: Filter and sort presets can be pinned as one-click quick-toggle buttons in the header** — pinned presets appear as icon buttons to the left of the Filter/Sort buttons; one click applies the preset, a second click clears it. The built-in All Artifacts and All Accessories filters and the Newest and SPD sort presets are pinned by default (with hammer and crystal icons). Any preset can be assigned a glyph icon and toggled as pinned in the save dialog or preset menu.
- **Lategame preset: "Rely on 5★ gear" is now five separate per-category toggles** — the single 3-state radio is replaced with individual checkboxes for General gear, Limited-set artifacts, Accessories, Speed gear, and Safeguards, so you can keep 5★ protection for scarce categories while dropping it for others independently.
- **Lategame preset: new "Endgame+" account tier** — a fourth tier stricter than Endgame: keeps 5★ for safeguards only, uses Very Strict substat thresholds for artifacts and accessories, and sells all weak Chaos Ore without exception.
- **Lategame preset: SPD/CR/CDMG Gloves and Boots with a matching SPD/CR/CDMG substat now require 3 rolls instead of 2** — the stricter roll count reduces premature keeps on pieces where one strong substat masks an otherwise weak roll history.
- **Lategame preset: "Keep only already-rolled" Chaos Ore option now correctly applies the level 12–16 cap to 6★ Legendary pieces** — the restriction was previously only enforced on Epic pieces; Legendary 6★ pieces are now also capped when that option is selected.
- **Fixed: Gear Inspector recipe/tag name filter now searches all matching recipes, not just the winner** — the filter was only checking the primary match result, so pieces that qualified under a secondary recipe were incorrectly hidden when the filter was active.

Deutsch:
- **Neu: Gear Diff — Vorher-/Nachher-Vergleich, der genau zeigt, was sich nach Regeländerungen geändert hat** — ein „Diff"-Schalter im Gear-Inspector-Header öffnet eine geteilte Ansicht: der linke (Vorher-)Bereich zeigt die Ergebnis-Anzahl jeder Gruppe am Referenzpunkt, der rechte (Nachher-)Bereich zeigt die aktuellen Regeln. Ein vorzeichenbehafteter Delta-Chip (±verkauft / ±behalten / ±safeguard) bleibt neben der Diff-Schaltfläche sichtbar, auch wenn die geteilte Ansicht geschlossen ist. Auswählen eines Teils in einem Bereich markiert dasselbe Teil im anderen. Der Referenzpunkt kann manuell angepinnt oder bei jeder Regeländerung automatisch aktualisiert werden; das Laden einer SFC-Datei löst ebenfalls einen Diff zur vorherigen Ladung aus.
- **Neu: Filter- und Sortier-Presets können als Schnellumschalt-Schaltflächen im Header angepinnt werden** — angepinnte Presets erscheinen als Icon-Schaltflächen links neben den Filter/Sortier-Buttons; einmal klicken wendet das Preset an, nochmals klicken hebt es auf. Die eingebauten Filter „Alle Artefakte" und „Alle Accessoires" sowie die Sortierungen Neueste und SPD sind standardmäßig angepinnt (mit Hammer- und Kristall-Icons). Im Speicherdialog oder Preset-Menü lässt sich jedem Preset ein Glyph-Icon zuweisen und das Anpinnen umschalten.
- **Lategame-Preset: „5★-Ausrüstung beibehalten" jetzt als fünf separate Kategorie-Schalter** — der bisherige 3-Zustands-Radiobutton wird durch einzelne Checkboxen für Allgemeine Ausrüstung, Limited-Set-Artefakte, Accessoires, Speed-Ausrüstung und Safeguards ersetzt, sodass 5★-Schutz für knappe Kategorien unabhängig aktiviert oder deaktiviert werden kann.
- **Lategame-Preset: neue Kontostufe „Endgame+"** — eine vierte Stufe, strenger als Endgame: behält 5★ nur noch für Safeguards, verwendet Sehr strenge Substat-Schwellenwerte für Artefakte und Accessoires und verkauft alle schwachen Chaos-Erz-Teile ausnahmslos.
- **Lategame-Preset: SPD/CR/CDMG-Handschuhe und -Stiefel mit passendem SPD/CR/CDMG-Substat benötigen jetzt 3 statt 2 Rolls** — der strengere Schwellenwert verhindert das vorzeitige Behalten von Teilen, bei denen ein starker Substat eine sonst schwache Roll-Geschichte verdeckt.
- **Lategame-Preset: Option „Nur bereits gerollte Teile behalten" beim Chaos Erz wendet die Level-12–16-Begrenzung jetzt korrekt auch auf 6★-Legendary-Teile an** — die Einschränkung galt zuvor nur für Epic-Teile; Legendary-6★-Teile werden jetzt ebenfalls begrenzt, wenn diese Option ausgewählt ist.
- **Behoben: Der Rezept-/Tag-Namensfilter im Gear Inspector durchsucht jetzt alle passenden Rezepte, nicht nur das gewinnende** — der Filter prüfte nur das primäre Treffer-Ergebnis, sodass Teile, die über ein sekundäres Rezept qualifiziert waren, bei aktivem Filter fälschlicherweise ausgeblendet wurden.

## v1.0.16 — 2026-06-02
English:
- **New: Dungeon Simulator 5× boost for Fire Knight, Dragon, and Ice Golem** — the boost selector now includes a 5× drop-rate multiplier alongside 2× and 3×. Spider's Den and event dungeons are unaffected.
- **New: Safeguard override answers saved between sessions** — slider positions and selection choices in safeguard override questions now survive a page reload, matching the existing behavior for recipe overrides.
- **New: Gear Inspector group headers now stick and tuck cleanly while scrolling** — pinned section and subgroup labels stack in order as you scroll into nested groups, tuck behind their parent when a subgroup ends, and no longer lock up scrolling when a collapsed group's header was pinned.
- **Fixed: Renaming a metaset now updates all recipes and safeguard rules that reference it** — rules kept the old name after a rename and stopped matching correctly; they now follow the new name automatically.
- **Fixed: Clicking a chip in the Gear Inspector no longer accidentally selects the card** — match chips, other-match chips, the "+N" overflow chip, and the Final Sell label all correctly block the click from toggling card multi-selection.
- **Fixed: Safeguard builder no longer injects a fallback set when a metaset covers the slot** — rules that use a metaset but no individual sets no longer get Life or Swift Parry silently added to the sets list when you click a slot.
- **Fixed: Gear Analytics outcome chart now renders correctly in all themes** — a color format mismatch caused the outcome distribution donut to crash; it now uses the correct color values in all theme configurations.
- **Fixed: Gear piece lock state and last-used timestamps no longer reset on RSL Helper reconnect** — when RSL Helper sends a fresh gear snapshot, pieces that were locked or had a known last-used timestamp no longer lose that information.
- **Lategame preset: Mercurial accessories with a strong SPD substat now have dedicated protection** — a new safeguard rule keeps scarce Mercurial accessories with a top SPD roll from being sold prematurely; Mercurial safeguards are now organized as a metaset for easier maintenance.
- **Lategame preset: dedicated safeguards for high-Accuracy limited-debuffer gear** — new rules protect pieces worn by limited debuffers that require high Accuracy alongside controlled Speed.
- **Preset load buttons relabeled** — "Load Beginner Sample SFC" is now "Load Preset: Beginner" and "Load Midgame to Endgame Sample SFC" is now "Load Preset: Midgame to Endgame."

Deutsch:
- **Neu: Dungeon-Simulator 5×-Boost für Fire Knight, Drache und Ice Golem** — der Boost-Selektor bietet jetzt auch eine 5×-Drop-Rate-Option neben 2× und 3×. Spider's Den und Event-Dungeons sind nicht betroffen.
- **Neu: Safeguard-Override-Antworten werden zwischen Sitzungen gespeichert** — Schiebereglerstellungen und Auswahloptionen in Safeguard-Override-Fragen bleiben nach einem Seiten-Reload erhalten und verhalten sich jetzt wie die bereits vorhandene Persistenz für Recipe-Overrides.
- **Neu: Gear-Inspector-Gruppenüberschriften rasten sauber beim Scrollen ein** — angepinnte Abschnitts- und Untergruppen-Labels stapeln sich in der richtigen Reihenfolge beim Scrollen in verschachtelte Gruppen, schieben sich unter ihre übergeordnete Überschrift, wenn eine Untergruppe endet, und sperren nicht mehr die Scrollposition, wenn eine zusammengeklappte Gruppe angepinnt war.
- **Behoben: Umbenennen eines Metasets aktualisiert jetzt alle Rezepte und Schutzregeln, die darauf verweisen** — Regeln behielten nach einem Umbenennen den alten Namen und griffen nicht mehr korrekt; sie folgen jetzt automatisch dem neuen Namen.
- **Behoben: Ein Klick auf einen Chip im Gear Inspector wählt die Karte nicht mehr versehentlich aus** — Match-Chips, Andere-Match-Chips, der „+N"-Overflow-Chip und das Final-Sell-Label blockieren jetzt korrekt, dass der Klick die Mehrfachauswahl der Karte auslöst.
- **Behoben: Der Safeguard-Builder fügt keinen Fallback-Set mehr ein, wenn ein Metaset den Slot abdeckt** — Regeln mit Metasets, aber ohne einzelne Sets, erhalten beim Klick auf einen Slot nicht mehr stillschweigend Life oder Swift Parry hinzugefügt.
- **Behoben: Der Gear-Analytics-Outcome-Chart rendert jetzt korrekt in allen Designs** — ein Farbformat-Fehler ließ das Outcome-Donut-Diagramm abstürzen; es verwendet jetzt in allen Design-Konfigurationen die richtigen Farbwerte.
- **Behoben: Sperrstatus und Zuletzt-verwendet-Zeitstempel von Gear-Teilen werden bei RSL-Helper-Verbindungswiederherstellung nicht mehr zurückgesetzt** — wenn RSL Helper einen neuen Snapshot schickt, verlieren gesperrte oder mit bekannten Zeitstempeln versehene Teile diese Informationen nicht mehr.
- **Lategame-Preset: Mercurial-Accessoires mit starkem SPD-Substat erhalten dedizierten Schutz** — eine neue Schutzregel bewahrt seltene Mercurial-Accessoires mit hohem SPD-Roll vor vorzeitigem Verkauf; Mercurial-Schutzregeln sind jetzt als Metaset organisiert.
- **Lategame-Preset: dedizierte Schutzregeln für High-Accuracy-limitierte-Debuffer-Ausrüstung** — neue Regeln schützen Teile, die von limitierten Debuffern mit hoher Accuracy und kontrollierter Speed getragen werden.
- **Preset-Ladeknöpfe umbenannt** — „SFC-Beispieldatei laden (Anfänger)" heißt jetzt „Voreinstellung laden: Anfänger" und „SFC-Beispieldatei laden (Midgame bis Endgame)" heißt jetzt „Voreinstellung laden: Midgame bis Endgame".

## v1.0.15 — 2026-05-31
English:
- **Sample SFC: dedicated Mercurial accessory safeguards** — new rules protect the best Mercurial amulets (Debuffer HP/DEF with ACC; CDMG with ACC/RES; CDMG with full substat pool; HP/DEF Survivability), Mercurial rings by main stat, and Mercurial SPD-substat banners by faction and slot, so promising Mercurial accessories are no longer lost before they finish rolling.
- **Sample SFC: Merciless coverage extended to accessories** — added dedicated safeguards for the best Merciless CDMG amulets and Merciless SPD-substat banners by faction and slot, matching the protection already given to Merciless armor pieces.
- **Sample SFC: Endgame preset retuned for accessories** — accessories now need "Strict" (3) good substats instead of "Very Strict" (4), and the "accessories must roll desired stats early" question gains a new "Mostly" option (between "No" and "Yes") that only requires 5★ accessories and spider-set accessories to roll desired stats early; Endgame uses this new "Mostly" by default.
- **Sample SFC: "Strict" accessory substat preset is now actually stricter** — picking "Strict" in the "good substats per accessory" question now also bumps the minimum substat values for accessories (SPD from 1 → 2, other substats from 2 → 3), not just the required roll counts.

Deutsch:
- **Beispiel-SFC: dedizierte Schutzregeln für Mercurial-Accessoires** — neue Regeln schützen die besten Mercurial-Amulette (Debuffer HP/DEF mit ACC; CDMG mit ACC/RES; CDMG mit vollständigem Substat-Pool; HP/DEF Survivability), Mercurial-Ringe nach Hauptstat sowie Mercurial-Banner mit SPD-Substat pro Fraktion und Slot, sodass vielversprechende Mercurial-Accessoires nicht mehr verloren gehen, bevor sie fertig gerollt sind.
- **Beispiel-SFC: Merciless-Abdeckung auf Accessoires ausgeweitet** — neue dedizierte Schutzregeln für die besten Merciless-CDMG-Amulette und Merciless-Banner mit SPD-Substat pro Fraktion und Slot, analog zum Schutz, der bereits für Merciless-Rüstungsteile existiert.
- **Beispiel-SFC: Endgame-Preset bei Accessoires neu eingestellt** — Accessoires brauchen jetzt „Streng" (3) gute Substats statt „Sehr streng" (4), und die Frage „Accessoires müssen erwünschte Stats früh rollen" erhält eine neue Option „Größtenteils" (zwischen „Nein" und „Ja"), die nur 5★-Accessoires und Spider-Set-Accessoires zum frühen Rollen verpflichtet; Endgame nutzt diese neue Option „Größtenteils" standardmäßig.
- **Beispiel-SFC: „Streng"-Voreinstellung für Accessoire-Substats ist jetzt tatsächlich strenger** — die Auswahl „Streng" in der Frage „Gute Substats pro Accessoire" hebt jetzt zusätzlich die Mindestwerte für Substats auf Accessoires an (SPD von 1 → 2, andere Substats von 2 → 3), nicht nur die geforderten Roll-Zahlen.

## v1.0.14 — 2026-05-31
English:
- **New: Light mode** — a sun/moon toggle on the Help screen switches between dark and light themes instantly. A theme customization flyout lets you adjust accent color, selection color, background, border radius, and more; all choices are saved between sessions.
- **New: Note panel in side-by-side layout is now a floating, draggable panel** — drag it to snap to either screen edge and resize its width independently. Position and width are remembered between sessions.
- **New: Override DSL error diagnostics in the note editor** — unknown fields, bad selectors, and unterminated strings now appear as wavy red underlines in the note text, with a summary panel below the editor listing all issues and folding repeated messages.
- **New: Keyboard navigation for recipe and safeguard chip lists** — arrow keys move one item at a time; Page Up/Down jump by visible screen height; Home/End jump to the first or last item.
- **Metasets dialog redesigned** — recipe and safeguard usage split into separate fixed-width columns with persistent headers. Safeguard chips are now clickable to jump to the matching rule, matching how recipe chips already worked.
- **Gear Analytics: main stat bar is now a cross-filter** — clicking a main-stat slice filters all pie charts, KPIs, and the chip strip simultaneously, consistent with the other Analytics dimensions.
- **Sample SFC: dedicated "good substats per accessory" override** — a new question lets you tune accessory strictness (Rings, Amulets, Banners) independently from artifacts, with Very Relaxed / Relaxed / Strict / Very Strict choices.
- **Sample SFC: Chaos Ore options now offer a "Gauntlets, Chestplate, and Boots are ignored" checkbox** — limits weak-piece protection to slots that benefit most from safe mainstats (Weapon, Helmet, Shield, Ring, Amulet, Banner). On by default in Midgame/Lategame for all three Chaos Ore questions, and in Endgame for 6★ and All-Sets.
- **Sample SFC: Lategame preset now caps 5★ Chaos Ore protection to already-rolled gear at level 12–16** — previously Lategame kept any 5★ that *could* still hit 3× on a substat; it now only keeps pieces that have already done so.
- **Sample SFC: Endgame preset is stricter on accessories** — accessories now need one more good substat compared to the previous Endgame setting, and the "accessories must roll desired stats early" toggle is on by default.
- **Sample SFC: new Banner reference recipe for Midgame preset** — a 6★ HP/DEF banner template requiring three in SPD / HP% / DEF% is included as a starting point.
- **Sample SFC: Mercurial safeguards now run before the generic "catch unique sets" safeguards** — Mercurial pieces are evaluated by their dedicated rule first, so the catch-all no longer claims them before Mercurial-specific protection applies.
- **Sample SFC: removed two stale recipes** — an untagged duplicate "triple SPD banner" recipe (which bypassed the dynamic overrides) and the "Mythical-substat CDMG amulet" recipe (since players with mythical access can use 6★ instead, which is easier to obtain and has higher stat value).
- **Fixed: Gear Inspector scroll position now restores after RSL Helper reconnects** — the list no longer jumps to the top when the connection refreshes.
- **Fixed: Gear Inspector outcome counts in "Matched Active" context mode** — the scoped panel now counts only primary matches, excluding companion items.
- **Fixed: Dungeon Simulator tooltip no longer gets stuck on "Calculating..."** — restarting after the worker went idle now loads results correctly.
- **Fixed: Gear Inspector context menu relabeled to "Show Match Index"** (was "Show Recipe Index") — it now also correctly shows the safeguard rule ordinal for safeguard-only matched items.
- **Fixed: Meta-set selection in the safeguard builder is now disabled only when all member sets are outside the allowed pool** — previously it locked incorrectly when any single member was disallowed.
- **Fixed: Gear Sets Select quick-filter now includes no-set accessories** when no slot filter is active.
- **Fixed: Gear Analytics equipped rate was incorrectly pinned at 100%** — a comparison bug missed unequipped pieces.

Deutsch:
- **Neu: Hell-Modus** — Ein Sonne/Mond-Schalter auf dem Hilfe-Bildschirm wechselt sofort zwischen dunklem und hellem Design. Ein Design-Anpassungs-Flyout ermöglicht das Einstellen von Akzentfarbe, Auswahlfarbe, Hintergrund, Eckenradius und mehr; alle Einstellungen werden zwischen Sitzungen gespeichert.
- **Neu: Notizbereich im Side-by-Side-Layout ist jetzt ein schwebendes, verschiebbares Panel** — Ziehe es zum Einrasten an einen Bildschirmrand und passe die Breite unabhängig an. Position und Breite werden zwischen Sitzungen gespeichert.
- **Neu: Fehlerdiagnose für Override-DSL im Notiz-Editor** — Unbekannte Felder, fehlerhafte Selektoren und nicht geschlossene Zeichenketten erscheinen als wellenförmige rote Unterstreichungen im Notiztext, mit einer Zusammenfassung aller Probleme darunter, in der wiederholte Meldungen zusammengefasst werden.
- **Neu: Tastaturnavigation für Rezept- und Schutzregel-Chip-Listen** — Pfeiltasten bewegen sich um ein Element; Bild-auf/Bild-ab springt um eine Bildschirmhöhe; Pos1/Ende springt zum ersten oder letzten Element.
- **Metasets-Dialog neu gestaltet** — Rezept- und Schutzregel-Nutzung auf separate Spalten mit fester Breite und dauerhaften Überschriften aufgeteilt. Schutzregel-Chips sind jetzt anklickbar, um zur entsprechenden Regel zu springen – entsprechend dem Verhalten der Rezept-Chips.
- **Gear Analytics: Hauptstat-Balken ist jetzt ein Kreuzfilter** — ein Klick auf ein Hauptstat-Segment filtert alle Tortendiagramme, KPIs und den Chip-Streifen gleichzeitig, konsistent mit den anderen Analytics-Dimensionen.
- **Beispiel-SFC: dedizierter Override „Gute Substats pro Accessoire"** — eine neue Frage erlaubt es, die Strenge für Accessoires (Ringe, Amulette, Banner) unabhängig von Artefakten einzustellen, mit Auswahl „Sehr entspannt" / „Entspannt" / „Streng" / „Sehr streng".
- **Beispiel-SFC: Chaos-Erz-Optionen bieten jetzt eine Checkbox „Handschuhe, Brustplatte und Stiefel ignorieren"** — beschränkt den Schutz schwacher Teile auf die Slots, die sichere mainstats haben (Waffe, Helm, Schild, Ring, Amulett, Banner). Standardmäßig aktiv in Midgame/Lategame für alle drei Chaos-Erz-Fragen sowie in Endgame für 6★ und Alle-Sets.
- **Beispiel-SFC: Lategame-Preset begrenzt den 5★-Chaos-Erz-Schutz jetzt auf bereits gerollte Teile auf Level 12–16** — zuvor behielt Lategame jedes 5★, das auf einem Substat noch 3× erreichen *könnte*; jetzt werden nur Teile behalten, die das bereits geschafft haben.
- **Beispiel-SFC: Endgame-Preset ist strenger bei Accessoires** — Accessoires brauchen jetzt einen guten Substat mehr als bei der vorherigen Endgame-Einstellung, und der Schalter „Accessoires müssen erwünschte Stats früh rollen" ist standardmäßig aktiv.
- **Beispiel-SFC: neues Banner-Referenzrezept für das Midgame-Preset** — eine 6★-HP/DEF-Banner-Vorlage, die drei der Substats SPD / HP% / DEF% verlangt, ist als Ausgangspunkt enthalten.
- **Beispiel-SFC: Mercurial-Schutzregeln laufen jetzt vor den generischen „Unique-Sets einfangen"-Schutzregeln** — Mercurial-Teile werden zuerst von ihrer dedizierten Regel ausgewertet, sodass die Catch-All-Regel sie nicht mehr beansprucht, bevor der Mercurial-spezifische Schutz greift.
- **Beispiel-SFC: zwei veraltete Rezepte entfernt** — ein ungetaggtes Duplikat-Rezept für „Tripel-SPD-Banner" (das die dynamischen Overrides umging) sowie das Rezept für „Mythisch-Substat-CDMG-Amulette" (da Spieler mit Mythical-Zugang stattdessen 6★ verwenden können, was leichter zu erhalten ist und höhere Stat-Werte bietet).
- **Behoben: Scrollposition im Gear Inspector wird nach Wiederherstellen der RSL-Helper-Verbindung wiederhergestellt** — die Liste springt nicht mehr nach oben, wenn die Verbindung neu aufgebaut wird.
- **Behoben: Gear-Inspector-Ergebniszählung im „Matched Active"-Kontext-Modus** — die Scoped-Seite zählt jetzt nur noch primäre Treffer, ohne Begleiter-Items.
- **Behoben: Dungeon-Simulator-Tooltip bleibt nicht mehr bei „Berechne..." stecken** — ein Neustart nach dem Inaktiv-Werden des Workers lädt Ergebnisse jetzt korrekt.
- **Behoben: Gear-Inspector-Kontextmenü in „Show Match Index" umbenannt** (vorher „Show Recipe Index") — zeigt jetzt auch korrekt den Schutzregel-Index für nur durch Schutzregeln gematchte Items.
- **Behoben: Metaset-Auswahl im Schutzregel-Builder wird jetzt nur gesperrt, wenn alle Mitglieds-Sets außerhalb des erlaubten Pools sind** — zuvor wurde es fälschlicherweise gesperrt, wenn ein einzelnes Mitglied nicht erlaubt war.
- **Behoben: Gear-Sets-Select-Schnellfilter zeigt jetzt No-Set-Accessoires an**, wenn kein Slot-Filter aktiv ist.
- **Behoben: Gear Analytics zeigte fälschlicherweise 100 % für die Ausrüstungsrate** — ein Vergleichsfehler übersah nicht ausgerüstete Teile.

## v1.0.13 — 2026-05-23
English:
- **New: Recipe overrides can now set absolute Roll Target thresholds per substat** — use `rolltarget.<stat>` in a `recipe-overrides` note block to replace the factory thresholds with your own values. Empty slots automatically fall back to the higher of the factory default and the last value you specified. A warning badge appears on the Roll Targets heading whenever a custom threshold is active.
- **New: Clearing tags that are in use by active dynamic overrides now asks for confirmation** — you can choose to apply the current override values before the tags are removed, so no adjustments are lost silently.
- **New: Gear Inspector bottom bar now has a single/multi-select mode toggle** — the toggle sits to the right of the Unselect All button, and your chosen mode is remembered between sessions.
- **New: Double-clicking a tag chip in the rule or safeguard builder copies its text to the clipboard.**
- **Sample SFC: accessory recipes/safeguards now use a dynamic override to make Roll Targets stricter** — accessory slots can require desired stat rolls to appear early (by level 8) and apply higher minimum flat-stat thresholds. Alternatively, you can rely mostly on safeguards to protect your best accessories.
- **Fixed: Tutorial step 10 now highlights the correct button in the Manage Metasets dialog** — export-step text formatting is also corrected in all supported languages.

Deutsch:
- **Neu: Recipe-Overrides können jetzt absolute Roll-Target-Schwellenwerte pro Substat setzen** — verwende `rolltarget.<stat>` in einem `recipe-overrides`-Notizblock, um die Standard-Schwellenwerte durch eigene Werte zu ersetzen. Leere Stellen fallen automatisch auf den höheren Wert aus Standard-Schwellenwert und zuletzt angegebenem Wert zurück. Ein Warnsymbol am Roll-Targets-Bereich zeigt an, wenn ein benutzerdefinierter Schwellenwert aktiv ist.
- **Neu: Das Löschen von Tags, die in aktiven dynamischen Overrides verwendet werden, fragt jetzt nach Bestätigung** — du kannst die Override-Werte übernehmen, bevor die Tags entfernt werden, sodass keine Anpassungen still verloren gehen.
- **Neu: Die untere Leiste des Gear Inspectors hat jetzt einen Einzel-/Mehrfachauswahl-Schalter** — der Schalter befindet sich rechts neben der Schaltfläche „Auswahl aufheben", und der gewählte Modus wird zwischen Sitzungen gespeichert.
- **Neu: Ein Doppelklick auf einen Tag-Chip im Regel- oder Schutzregel-Builder kopiert dessen Text in die Zwischenablage.**
- **Beispiel-SFC: Schmuckstück-Rezepte/Schutzregeln verwenden jetzt einen dynamischen Override, der die Roll Targets strenger macht** — für Schmuckstück-Slots können gewünschte Substat-Würfe bereits früh (bis Level 8) gefordert und höhere Mindest-Flatstat-Schwellen angewendet werden. Alternativ kannst du dich hauptsächlich auf Schutzregeln verlassen, um deine besten Schmuckstücke zu schützen.
- **Behoben: Schritt 10 des Tutorials hebt jetzt die richtige Schaltfläche im Metasets-Dialog hervor** — die Textformatierung des Export-Schritts ist zudem in allen unterstützten Sprachen korrigiert.

## v1.0.12 — 2026-05-22
English:
- **Fixed: deleting an empty, unused Metaset no longer causes it to reappear after closing the Manage Metasets dialog**

Deutsch:
- **Behoben: Ein geleertes, ungenutztes Metaset erscheint nach dem Schließen des Metasets-Dialogs nicht mehr erneut**

## v1.0.11 — 2026-05-22
English:
- **Fixed: "Ignore previous safeguards" now works correctly for safeguards that rank items by substats** — previously the toggle had no effect on the ranking path: the rule would re-protect the same top picks regardless of what earlier safeguards had already kept. Now, when the toggle is on, items already protected by an earlier active safeguard are removed from the matching pool before top-N selection, so the rule reaches deeper into the score ranking and protects distinct gear. Rules without substats continue to use the existing kept-count logic unchanged.
- **New: Note overrides can now reach across rule types in a single block** — a `recipe-overrides` note section can include `safeguard @name { ... }` blocks to override safeguard rules, and a `safeguard-overrides` note can include `recipe @name { ... }` blocks for recipes. Slider arithmetic using `$count` and `$value` works in both directions.
- **New: Note overrides can now change which ranks, rarities, and factions a safeguard rule applies to** — `rank`, `rarity`, and `faction` are now valid assignment fields in `safeguard-overrides` (and cross-domain `safeguard @...`) blocks, supporting both replace mode (bare values) and `+`/`-` mutate mode, matching the existing substat override pattern. The safeguard builder shows an override badge and displays the effective values in its selects when such an override is active.
- **Fixed: disabled safeguard rules no longer appear in the Gear Inspector's safeguard match filter** — rules with activation set to "Off" were leaking into the by-safeguard filter and rank overlays; they are now excluded, matching the behavior of disabled sell recipes.
- **Sample SFC: Mid-to-Endgame and Endgame presets now protect less Utility gear** — the Utility-set safeguard rules have been narrowed so fewer Utility pieces are kept when better alternatives exist.
- **Loading older save files: "Ignore previous safeguards" is reset to Off on substat-ranked rules** — since the flag had no effect on the ranking path in older versions, the app now resets it to Off on load to avoid silently activating the new behavior.

Deutsch:
- **Behoben: „Vorherige Schutzregeln ignorieren" funktioniert jetzt korrekt für Schutzregeln, die Items nach Substats ranken** — zuvor hatte der Schalter auf dem Ranking-Pfad keine Wirkung: Die Regel schützte erneut dieselben Top-Picks, unabhängig davon, was frühere Schutzregeln bereits behalten hatten. Wenn der Schalter aktiviert ist, werden Items, die von einer früheren aktiven Schutzregel bereits geschützt wurden, vor der Top-N-Auswahl aus dem Matching-Pool entfernt, sodass die Regel tiefer ins Ranking vordringt und andere Ausrüstung schützt. Regeln ohne Substats verwenden weiterhin die bisherige Kept-Count-Logik.
- **Neu: Dynamische Overrides können jetzt regeltypenübergreifend in einem einzelnen Block wirken** — ein `recipe-overrides`-Notizabschnitt kann `safeguard @Name { ... }`-Blöcke enthalten, um Schutzregeln zu überschreiben, und eine `safeguard-overrides`-Notiz kann `recipe @Name { ... }`-Blöcke für Rezepte enthalten. Schieberegler-Arithmetik mit `$count` und `$value` funktioniert in beiden Richtungen.
- **Neu: Dynamische Overrides können jetzt festlegen, welche Ränge, Seltenheiten und Fraktionen eine Schutzregel betrifft** — `rank`, `rarity` und `faction` sind jetzt gültige Zuweisungsfelder in `safeguard-overrides`- (und übergreifenden `safeguard @...`-) Blöcken, mit Unterstützung für Ersetzen-Modus (direkte Werte) und `+`/`-`-Mutier-Modus, analog zum bestehenden Substat-Override-Muster. Der Schutzregel-Builder zeigt ein Override-Badge und gibt die effektiven Werte in den Auswahlmenüs aus, wenn ein solcher Override aktiv ist.
- **Behoben: Deaktivierte Schutzregeln erscheinen nicht mehr im Safeguard-Match-Filter des Gear Inspectors** — Regeln mit Aktivierung „Aus" tauchten im Filter nach Schutzregel und in Rang-Overlays auf; sie werden jetzt ausgeblendet, entsprechend dem Verhalten deaktivierter Verkaufsrezepte.
- **Beispiel-SFC: Die Mid-to-Endgame- und Endgame-Presets schützen jetzt weniger Utility-Ausrüstung** — die Utility-Schutzregeln wurden enger gefasst, sodass weniger Utility-Teile behalten werden, wenn bessere Alternativen vorhanden sind.
- **Laden älterer Speicherdateien: „Vorherige Schutzregeln ignorieren" wird für substat-gerankte Regeln auf Aus zurückgesetzt** — da der Schalter beim Ranking-Pfad in früheren Versionen keine Wirkung hatte, setzt die App ihn beim Laden auf Aus, um neues Verhalten nicht stillschweigend zu aktivieren.

## v1.0.10 — 2026-05-18
English:
- **Gear Analytics: "Champion Equipment" section** — the former "Not Fully Equipped" section is renamed and expanded: a "Simulate sold" toggle highlights in red any equipped piece your active rules would sell; a "Show fully equipped" toggle includes champions with every slot already filled; sorting now defaults to in-game roster order (Empowerment › Blessing › Affinity › Star › Level); selecting an item in this list also highlights it in the Gear Inspector.
- **New: Simple Mode** — a streamlined view for RSL Helper integration, opened via the `?simple` URL parameter. It offers a preset toggle (Beginner / Endgame), a centered Auto-Push control with a connection status indicator, and a "Go Expert" button to switch to the full editor. Fully localized in all supported languages.
- **New: Color picker for rule and safeguard names** — names can now include a display color chosen through a proper color picker, replacing the old `[#RRGGBB]` text-embedded syntax.
- **Fixed: safeguard rules could evaluate gear incorrectly when substat totals were involved** — an internal type mismatch caused artifact substat total values to be missing from the evaluation input, which could cause keep/sell decisions to be wrong for rules that compare total substat values.
- **Fixed: rules with a faction set were incorrectly matching armor slots** — Helmet, Chest, and Leg pieces were being evaluated by rules that should only apply to accessories (Ring, Amulet, Banner). Keep/sell decisions for those pieces are now correct.
- **Fixed: safeguard rules with no substat filter now protect all matching items** — previously the app arbitrarily capped protection to a fixed count; now every item that qualifies is protected.
- **Fixed: safeguard weights live-rescoring popover now works correctly** — the live preview was producing wrong scores due to an initialization issue in the dedicated scoring worker; results now match actual rule evaluation.
- **Fixed: armor-slot and faction options are now mutually exclusive in the rule editor** — selecting a faction disables armor slot buttons, and vice versa, preventing invalid rule configurations.
- **Fixed: safeguard rule colors were missing from Gear Inspector labels, safeguard rank previews, and rule name tooltips** — color indicators now appear wherever a safeguard rule name is displayed.
- **Fixed: the cutoff divider in the safeguard weight adjustment popover would jump to the wrong row when the list was scrolled** — it now stays anchored to the position you set.
- **Fixed: safeguard keep-overrides were ignored when a sell rule had first-match priority** — items meeting safeguard conditions are now correctly kept even when a matching sell recipe is ordered first.

Deutsch:
- **Gear Analytics: Bereich „Champion Equipment"** — der frühere Bereich „Nicht vollständig ausgerüstet" wurde umbenannt und erweitert: ein „Verkauf simulieren"-Schalter markiert in Rot jedes ausgerüstete Teil, das deine aktiven Regeln verkaufen würden; ein „Vollständig ausgerüstete anzeigen"-Schalter schließt Champions mit allen besetzten Slots ein; die Sortierung folgt jetzt standardmäßig der In-Game-Reihenfolge (Empowerment › Blessing › Affinität › Sterne › Level); wählst du ein Item in dieser Liste aus, wird es auch im Gear Inspector hervorgehoben.
- **Neu: Simple Mode** — eine vereinfachte Ansicht für die RSL-Helper-Integration, die über den URL-Parameter `?simple` aufgerufen wird. Sie bietet einen Preset-Schalter (Anfänger / Endgame), ein zentrales Auto-Push-Element mit Verbindungsanzeige und einen „Experten-Modus"-Button zum Wechsel in die vollständige Bearbeitungsansicht. In allen unterstützten Sprachen verfügbar.
- **Neu: Farbauswahl für Regel- und Schutznamen** — Namen können jetzt eine Anzeigefarbe über einen Farbauswähler erhalten, anstatt die alte `[#RRGGBB]`-Schreibweise im Namen zu verwenden.
- **Behoben: Schutzregeln konnten Ausrüstung falsch bewerten, wenn Substat-Gesamtwerte relevant waren** — eine interne Typdiskrepanz ließ Artefakt-Substat-Gesamtwerte aus der Auswertungseingabe fehlen, was bei Regeln, die Gesamtwerte vergleichen, zu falschen Behalten/Verkaufen-Entscheidungen führen konnte.
- **Behoben: Regeln mit gesetzter Fraktion bewerteten fälschlicherweise Rüstungsslots** — Helm-, Brust- und Bein-Teile wurden von Regeln ausgewertet, die nur für Accessoires gelten sollten (Ring, Amulett, Banner). Behalten/Verkaufen-Entscheidungen für diese Teile sind jetzt korrekt.
- **Behoben: Schutzregeln ohne Substat-Filter schützen jetzt alle passenden Items** — bisher hat die App den Schutz willkürlich auf eine feste Anzahl begrenzt; jetzt wird jedes qualifizierende Item geschützt.
- **Behoben: Live-Neuberechnung im Schutzregel-Gewichte-Popover funktioniert jetzt korrekt** — die Live-Vorschau lieferte falsche Ergebnisse wegen eines Initialisierungsproblems im dedizierten Scoring-Worker; die Ergebnisse stimmen jetzt mit der tatsächlichen Regelauswertung überein.
- **Behoben: Rüstungsslot- und Fraktions-Optionen schließen sich im Regeleditor gegenseitig aus** — bei Auswahl einer Fraktion werden Rüstungsslot-Buttons deaktiviert und umgekehrt, um ungültige Regelkonfigurationen zu verhindern.
- **Behoben: Farbmarkierungen von Schutzregel-Namen fehlten im Gear Inspector, in Schutzregel-Rangvorschauen und in Regel-Tooltips** — Farbindikatoren werden jetzt überall angezeigt, wo ein Schutzregel-Name erscheint.
- **Behoben: Die Cutoff-Trennlinie im Schutzregel-Gewichte-Popover sprang beim Scrollen der Liste an die falsche Zeile** — sie bleibt jetzt an der gesetzten Position verankert.
- **Behoben: Schutzregel-Keep-Overrides wurden ignoriert, wenn eine Verkaufsregel im First-Match Vorrang hatte** — Items, die Schutzbedingungen erfüllen, werden jetzt korrekt behalten, auch wenn eine passende Verkaufsregel zuerst geordnet ist.

## v1.0.9 — 2026-05-11
English:
- **New: Two sample SFC presets in the “Load SFC File” right-click menu** — the menu now offers “Load Beginner Sample SFC” and “Load Mid-to-End Game Sample SFC”. Right-clicking the button still opens the menu; left-clicking opens your file picker as before.
- **Mid-to-Endgame sample SFC: dedicated Mercurial gear safeguards** — added Safeguards that specifically protect the best of your Mercurial pieces even when they are not yet stat-perfect, so promising Mercurial gear is not sold while you are still farming toward better rolls.
- **New: Two built-in filter presets “Scoped Sell – Artifacts” and “Scoped Sell – Accessories”** — selecting either preset filters results to sell-tagged items from both inventory and vault, scoped to the respective slot group.
- **New: Improvement Chance filter in the Gear Inspector** — a 0–100% range slider filters items by how likely they are to improve their safeguard standing after upgrading. A hide/show chip controls whether items with no safeguard coverage appear. Adjusting the range away from 0–100% automatically hides those uncovered items so the filter is immediately useful.
- **New: Gear Inspector shows a lock icon on items locked in RSL Helper** — any item you have locked inside RSL Helper now displays a padlock symbol in the Inspector, making it easy to see which pieces are protected there.
- **New: Label colors for filter and sort presets** — when saving a preset you can now pick a color for its label using a full gradient and hue slider; recently chosen colors are remembered between sessions.
- **New: Built-in filter and sort presets can be individually hidden** — an eye-icon toggle on each built-in preset lets you suppress ones you never use; the menu hides them unless you enable “show hidden”.
- **New: Safeguard multi-edit tag additions are reflected immediately** — adding tags via the multi-edit panel now updates the tag chip list right away, without waiting for Apply.
- **New: Dungeon Simulator starts automatically when you open the tab** — the simulation begins as soon as the Dungeon Simulator tab is opened and stops when you close it; no manual start required.
- **New: Scope and Unmatched filter buttons in the Gear Inspector now show a tooltip** explaining how both buttons interact, so the combined filtering behavior is easier to understand.
- **Fixed: +16 gear no longer shows a “100% improvement chance” badge** — fully-upgraded gear has no further upgrade to project, so this result was misleading and is now hidden. The 0% badge (gear currently losing a contested safeguard slot) is still shown.
- **Fixed: Improvement Chance sorting now places fully-upgraded (+16) gear at the bottom** — previously maxed gear sorted to the top of the results, making it harder to find items where the improvement chance is actually meaningful.
- **Fixed: Improvement Chance is now calculated independently per safeguard rule** — previously the best chance across all safeguard rules was combined into one global score; now each rule evaluates its own top-N threshold separately, giving more accurate guidance on which items are worth upgrading.
- **Fixed: tag-only changes in safeguard multi-edit now save correctly** — editing only tags through the multi-edit panel without changing other rule fields was silently discarded; those changes now persist as expected.
- **Fixed: items hidden by a filter or demoted in context mode after an RSL Helper data push are now properly deselected** — previously those items remained selected even though they were no longer visible.
- **Fixed: 0-star ascension filter had no effect** — setting the ascension filter to 0 stars now correctly includes 0-star items.
- **Fixed: RSL Helper data pushes with no new data are now processed much faster** — when RSL Helper sends identical data it already sent, the app skips redundant processing steps, reducing the delay by 200–500 ms per occurrence.
- **Fixed: “Connect to RSL Helper” in the Help dialog is now the same live toggle button as in the toolbar** — it previously used a stale link that reloaded the page, which had not worked since persistent-connection mode was introduced.

Deutsch:
- **Neu: Zwei Beispiel-SFC-Presets im Rechtsklick-Menü von „SFC-Datei laden”** — das Menü bietet jetzt „Anfänger-Beispiel-SFC laden” und „Mid-to-Endgame-Beispiel-SFC laden”. Rechtsklick öffnet weiterhin das Menü; Linksklick öffnet wie bisher den Dateiauswähler.
- **Mid-to-Endgame-Beispiel-SFC: spezielle Schutzregeln für Unstet (Mercurial)-Ausrüstung** — neue Schutzregeln schützen gezielt die besten deiner Unstet (Mercurial)-Teile, auch wenn sie noch nicht stat-perfekt sind, sodass vielversprechende Unstet (Mercurial)-Ausrüstung nicht verkauft wird, während du noch auf bessere Rolls farmst.
- **Neu: Zwei integrierte Filter-Presets „Scoped Sell – Artefakte” und „Scoped Sell – Accessoires”** — wähle eines dieser Presets, um Ergebnisse auf verkaufsmarkierte Items aus Inventar und Tresor einzugrenzen, gefiltert nach der jeweiligen Slot-Gruppe.
- **Neu: Verbesserungschance-Filter im Gear Inspector** — ein 0–100%-Schieberegler filtert Items danach, wie wahrscheinlich es ist, dass sie nach dem Aufrüsten ihren Schutzregel-Platz verbessern. Ein Ein-/Ausblend-Chip steuert, ob Items ohne Schutzregel-Daten angezeigt werden. Wenn du den Bereich von 0–100% veränderst, werden Items ohne Daten automatisch ausgeblendet.
- **Neu: Gear Inspector zeigt ein Schloss-Symbol bei in RSL Helper gesperrten Items** — Items, die du in RSL Helper als gesperrt markiert hast, werden im Inspector jetzt mit einem Vorhängeschloss-Symbol angezeigt.
- **Neu: Farb-Labels für Filter- und Sortier-Presets** — beim Speichern eines Presets kannst du jetzt mit einem Farbverlauf- und Farbton-Regler eine Farbe für den Label wählen; zuletzt verwendete Farben werden sitzungsübergreifend gespeichert.
- **Neu: Integrierte Filter- und Sortier-Presets können einzeln ausgeblendet werden** — ein Auge-Symbol-Schalter an jedem integrierten Preset lässt dich selten genutzte ausblenden; das Menü blendet sie aus, bis du „Ausgeblendete anzeigen” aktivierst.
- **Neu: Tag-Änderungen im Schutzregel-Mehrfach-Edit sind sofort sichtbar** — das Hinzufügen von Tags über das Mehrfach-Edit-Panel aktualisiert die Tag-Chip-Liste sofort, ohne vorher auf „Anwenden” klicken zu müssen.
- **Neu: Dungeon-Simulator startet automatisch beim Öffnen des Tabs** — die Simulation beginnt sofort, wenn der Dungeon-Simulator-Tab geöffnet wird, und stoppt beim Schließen; kein manueller Start erforderlich.
- **Neu: Scope- und Unmatched-Filterschaltflächen im Gear Inspector zeigen jetzt einen Tooltip**, der erklärt, wie beide Schaltflächen zusammenwirken – so ist das kombinierte Filterverhalten leichter zu verstehen.
- **Behoben: +16-Ausrüstung zeigt nicht mehr den irreführenden „100% Verbesserungschance”-Badge** — vollständig aufgerüstetes Gear hat keine weitere Aufwertung zum Projizieren, daher wird dieses Ergebnis jetzt ausgeblendet. Der 0%-Badge (wenn das Item gerade einen umkämpften Schutzregel-Slot verliert) bleibt sichtbar.
- **Behoben: Verbesserungschance-Sortierung platziert vollständig aufgerüstetes (+16) Gear jetzt ganz unten** — bisher sortierte maximal aufgerüstetes Gear an den Anfang der Ergebnisse, was es schwerer machte, Items mit wirklich relevanter Verbesserungschance zu finden.
- **Behoben: Verbesserungschance wird jetzt pro Schutzregel separat berechnet** — bisher wurde die beste Chance über alle Schutzregeln global zusammengefasst; jetzt wertet jede Regel ihren eigenen Top-N-Schwellwert unabhängig aus, was genauere Hinweise liefert, welche Items sich zu upgraden lohnen.
- **Behoben: Nur-Tag-Änderungen im Schutzregel-Mehrfach-Edit werden jetzt korrekt gespeichert** — Tag-Änderungen, die ohne weitere Regeländerungen über das Mehrfach-Edit-Panel vorgenommen wurden, wurden zuvor stillschweigend verworfen; sie werden jetzt zuverlässig gespeichert.
- **Behoben: Items, die nach einem RSL-Helper-Daten-Push durch einen Filter ausgeblendet oder im Kontext-Modus zurückgestuft werden, werden jetzt korrekt abgewählt** — bisher blieben diese Items ausgewählt, obwohl sie nicht mehr sichtbar waren.
- **Behoben: 0-Sterne-Aufstiegs-Filter hatte keine Wirkung** — der Filter auf 0 Sterne schließt jetzt korrekt 0-Sterne-Items ein.
- **Behoben: RSL-Helper-Daten-Pushes ohne neue Daten werden jetzt deutlich schneller verarbeitet** — wenn RSL Helper identische Daten erneut sendet, überspringt die App redundante Verarbeitungsschritte und reduziert die Verzögerung um 200–500 ms pro Vorgang.
- **Behoben: „Mit RSL Helper verbinden” im Hilfe-Dialog ist jetzt derselbe Live-Schalter wie in der Toolbar** — bisher verwendete er einen veralteten Link, der die Seite neu lud und seit Einführung des persistenten Verbindungsmodus nicht mehr funktionierte.

## v1.0.8 — 2026-05-09
English:
- **New: Right-click "Load SFC File" to instantly load the bundled sample configuration** — right-clicking the Load SFC File button now opens a quick menu with two options: "Load from file…" to pick your own `.sfc`, or "Load Sample SFC File" to load the bundled sample SFC file.
- **Note for new players after the tutorial** — When the tutorial (or the welcome dialog on first launch) is closed, the "Load SFC file" button briefly lights up to indicate the sample SFC file to new players.

Deutsch:
- **Neu: Mit einem Rechtsklick auf "SFC-Datei laden" können Sie sofort die mitgelieferte Beispielkonfiguration laden.** — Ein Rechtsklick auf die Schaltfläche "SFC-Datei laden" öffnet nun ein Schnellmenü mit zwei Optionen: "Aus Datei laden…", um Ihre eigene `.sfc`-Datei auszuwählen, oder "Beispiel-SFC-Datei laden", um die mitgelieferte Beispiel-SFC-Datei zu laden.
- **Hinweis für neue Spieler nach dem Tutorial** — Wenn das Tutorial (oder den Begrüßungsdialog beim ersten Start) geschlossen wird, leuchtet die Schaltfläche "SFC-Datei laden" kurz auf und weist neue Spieler auf die Beispiel-SFC-Datei hin.

## v1.0.7 — 2026-05-09
English:
- **New: "Must NOT have" substat constraint (¬)** — you can now tell a recipe that an item must be completely free of a specific substat (e.g. "no Speed"). Cycle the substat badge with left- or right-click until it shows the red ¬ symbol. Added a disabled reference recipe into the sample SFC file.
- **New: "Connect to RSL Helper" button is now a persistent toggle with auto-connect** — the button remembers your preference and automatically reconnects when you reload or reopen the app.
- **Fixed: Gear Inspector now correctly previews which items safeguard keep-rules protect** — some items were shown as "Sell" in the Inspector even though RSL Helper would keep them, because the app's preview was matching only the exact piece a safeguard keep-rule was generated for rather than all pieces that meet its conditions.

Deutsch:
- **Neu: Substat-Bedingung „Muss NICHT vorhanden sein" (¬)** — du kannst in einem Rezept jetzt festlegen, dass ein bestimmter Substat auf dem Item fehlen muss (z. B. „kein Speed"). Klicke das Substat-Badge so oft, bis das rote ¬-Symbol erscheint. Ein ausgeschaltetes Referenz-Rezept wurde der Beispiel SFC-Datei hinzugefügt.
- **Neu: „Mit RSL Helper verbinden"-Button ist jetzt ein dauerhafter Schalter mit Auto-Connect** — der Button merkt sich deine Wahl und verbindet sich beim nächsten App-Start automatisch.
- **Behoben: Gear Inspector zeigt jetzt korrekt, welche Items durch Schutzregel-Keep-Regeln behalten werden** — manche Items wurden als „Verkaufen" angezeigt, obwohl RSL Helper sie behalten hätte, weil die App-Vorschau zu eng nur das exakte Piece traf, für das eine Schutzregel-Keep-Regel generiert wurde, statt alle Pieces mit passenden Bedingungen.

## v1.0.6 — 2026-04-25
English:
- **Bundled recipe sample: broader accessory protection** — new safeguard rules cover Crit Damage amulets (both ACC/RES support-hybrid and HP/ATK/DEF pure-damage variants), HP/DEF Survivability amulets, a Debuffer amulet for HP/DEF mains with ACC, dedicated ATK and DEF banner builds, and per-main-stat ring matching (HP rings compete for HP%, ATK rings for ATK%, DEF rings for DEF%).
- **Bundled recipe sample: faction fallback tiers expanded and decoupled** — the per-faction backup rules for rings, amulets, and banners now keep the top 3 candidates per slot (was 1) and run independently of the stricter per-set guards above them, so your best faction accessories no longer get shut out of the fallback tier.
- **Bundled recipe sample: damage rules now favor SPD and Crit Rate more strongly** — speed and crit rate score higher on offense-oriented rules while defensive substats (RES, HP%, DEF%) score lower, so gear meant for damage is no longer over-ranked by tankiness.
- **Fixed: Per Slot / Per Set / Per Faction / Per Main Stat scope chips in the safeguard builder now disable when they have no effect** — if only one slot, set, faction, or main stat is selected in a safeguard rule, the corresponding scope chip is greyed out and its prefix label is hidden on summary chips, Gear Inspector tooltips, and Note scope chips, since splitting by a single-value dimension changes nothing.
- **Fixed: "Match at least N substats" threshold auto-reduces when you deselect substats** — removing substats until fewer remain than the required match count no longer leaves an impossible threshold. The threshold now automatically clamps down to the number of substats still selected.
- **Fixed: right-click hint in the sellfile preview no longer appears over resize handles or empty space** — hovering the column-resize grip or the empty area below the last rule row no longer triggers the right-click tooltip, which was confusing because right-clicking in those areas has no action.

Deutsch:
- **Mitgeliefertes Rezept-Beispiel: breitere Accessoire-Abdeckung** — neue Schutzregeln decken Crit-Damage-Amulette ab (sowohl ACC/RES-Support-Hybriden als auch reine HP/ATK/DEF-Damage-Varianten), HP/DEF-Survivability-Amulette, ein Debuffer-Amulett für HP/DEF-Hauptstats mit ACC, eigene ATK- und DEF-Banner-Builds sowie Ring-Zuordnung pro Hauptstat (HP-Ringe konkurrieren um HP%, ATK-Ringe um ATK%, DEF-Ringe um DEF%).
- **Mitgeliefertes Rezept-Beispiel: Fraktions-Fallback-Stufen erweitert und entkoppelt** — die Per-Fraktion-Backup-Regeln für Ringe, Amulette und Banner behalten jetzt die Top 3 Kandidaten pro Slot (zuvor 1) und werden unabhängig von den strengeren Set-Schutzregeln darüber ausgewertet, sodass deine besten Fraktions-Accessoires nicht mehr aus der Fallback-Stufe verdrängt werden.
- **Mitgeliefertes Rezept-Beispiel: Schadens-Regeln bevorzugen jetzt SPD und Crit Rate stärker** — Speed und Crit Rate werden auf Schadens-Regeln höher gewichtet, defensive Substats (RES, HP%, DEF%) niedriger, sodass Gear für Offense nicht mehr von Tankiness übergewichtet wird.
- **Behoben: „Pro Slot / Pro Set / Pro Fraktion / Pro Main-Stat"-Chips im Schutz-Builder werden deaktiviert, wenn sie keine Wirkung haben** — wenn nur ein Slot, ein Set, eine Fraktion oder ein Main-Stat in einer Schutzregel ausgewählt ist, wird der entsprechende Scope-Chip ausgegraut und sein Präfix-Label auf Summary-Chips, Gear-Inspector-Tooltips und Note-Scope-Chips ausgeblendet, da die Aufteilung einer einwertigen Dimension nichts ändert.
- **Behoben: „Mindestens N Substats treffen"-Schwellwert reduziert sich automatisch beim Entfernen von Substats** — wenn du Substats entfernst, bis weniger vorhanden sind als die geforderte Trefferzahl, bleibt kein unmöglicher Schwellwert mehr stehen. Der Wert klemmt sich jetzt automatisch auf die Anzahl der noch ausgewählten Substats.
- **Behoben: Rechtsklick-Hinweis in der Sellfile-Vorschau erscheint nicht mehr über Resize-Griffen oder leerem Bereich** — Hover über den Spalten-Resize-Griff oder den leeren Bereich unterhalb der letzten Regelzeile löst den Rechtsklick-Tooltip nicht mehr aus, der dort verwirrend war, weil Rechtsklick in diesen Bereichen keine Aktion hat.

## v1.0.5 — 2026-04-19
English:
- **Fixed: safeguard-overrides sliders using division arithmetic now update the sellfile correctly** — expressions like `count=$value/8` or `count=$value/16` in `<!-- safeguard-overrides -->` blocks were silently broken: the slider moved but the keep-count in the sellfile never changed, because the `/` character was not recognized as a separator in the override formula parser. Now division arithmetic in count expressions works as intended.
- **Fixed: tag-based selectors in safeguard-overrides now actually apply to the sell pipeline** — when you used `@tag=someName` to target specific safeguard rules by their tags, the chips in the panel looked correct but the background worker received rules with empty tag lists, so the selector never matched anything and the actual sell decisions were unchanged. Tags now flow through the full pipeline so `@tag=` selectors reliably reach the rules that matter.
- **Fixed: division expressions in the Note editor are no longer highlighted incorrectly** — text like `$value/16` in a safeguard-overrides block was visually miscolored in the note editor (the slash was mistaken for the start of a special pattern). The highlight is now correct; no functional change to sellfile output.

Deutsch:
- **Behoben: Schutzregel-Override-Schieberegler mit Divisionsarithmetik aktualisieren jetzt das Sellfile korrekt** — Ausdrücke wie `count=$value/8` oder `count=$value/16` in `<!-- safeguard-overrides -->`-Blöcken funktionierten bisher nicht: Der Schieberegler bewegte sich, aber die Behalten-Anzahl im Sellfile änderte sich nie, weil das `/`-Zeichen im Override-Formel-Parser nicht als Trennzeichen erkannt wurde. Divisionsarithmetik in Anzahl-Ausdrücken funktioniert jetzt wie vorgesehen.
- **Behoben: Tag-basierte Selektoren in safeguard-overrides werden jetzt tatsächlich auf die Sell-Pipeline angewendet** — wenn du `@tag=Name` verwendest, um bestimmte Schutzregeln über ihre Tags anzusprechen, sahen die Chips im Panel korrekt aus, aber der Hintergrund-Worker erhielt Regeln ohne Tags — der Selektor traf daher niemals etwas, und die eigentlichen Verkaufsentscheidungen blieben unverändert. Tags werden nun vollständig durch die Pipeline weitergegeben, sodass `@tag=`-Selektoren zuverlässig die richtigen Regeln treffen.
- **Behoben: Divisionsausdrücke im Notizeneditor werden nicht mehr falsch hervorgehoben** — Text wie `$value/16` in einem safeguard-overrides-Block wurde im Notizeneditor falsch eingefärbt (der Schrägstrich wurde als Beginn eines Sondermusters interpretiert). Die Hervorhebung ist jetzt korrekt; am Sellfile-Output ändert sich nichts.

## v1.0.4 — 2026-04-19
English:
- **Fixed: override controls in your Note no longer show stale results** — sliders, radio buttons, and checkboxes from `<!-- safeguard-overrides -->` and `<!-- recipe-overrides -->` blocks now immediately refresh the sellfile preview when you adjust them. Previously the controls appeared to respond but the preview kept showing the rules from before the change; an unrelated edit was needed to force a rebuild.

Deutsch:
- **Behoben: Override-Steuerelemente in der Notiz zeigen keine veralteten Ergebnisse mehr** — Schieberegler, Radio-Buttons und Checkboxen aus `<!-- safeguard-overrides -->`- und `<!-- recipe-overrides -->`-Blöcken aktualisieren die Sellfile-Vorschau jetzt sofort, wenn du sie veränderst. Zuvor reagierten die Steuerelemente scheinbar, aber die Vorschau zeigte weiterhin die Regeln von vor der Änderung — erst eine unzusammenhängende Bearbeitung erzwang eine Neuberechnung.

## v1.0.3 — 2026-04-19
English:
- **New: Safeguard Overrides in your Note** — add `<!-- safeguard-overrides ... -->` blocks to your Note to create interactive sliders, radio buttons, and checkboxes that tune safeguard rules on the fly, without touching the stored rules themselves. Tag your safeguard rules (just like recipe tags) and target them by tag; slider values feed directly into keep-count arithmetic (`count=$value/8` and similar). Session-only: changes revert when you reload — or use "Apply and Disable" to bake them in permanently.
- **Update-available notice** — the app now checks for newer releases on startup. When a newer version is found, a small animated notice appears in the header with a download link. Dismiss it and it won't reappear until an even newer version is published.
- **Tags visible on recipe chips** — recipe chips can now show their tags inline, matching safeguard chips. Toggle "Show tags in chip list" via the right-click context menu of the recipe chip panel.
- **Pause automatic Gear DB updates** — right-click the Gear DB history button and enable "Pause automatic update" to silently drop incoming RSL Helper endpoint data without disconnecting. A 5-second minimum gap is also now enforced between consecutive endpoint apply cycles to prevent rapid re-triggering.
- **Memory stability: app no longer grows unboundedly during long sessions** — the rule pipeline now reuses its memory after the first large run instead of repeatedly allocating fresh blocks that the browser couldn't reclaim. Combined with several smaller leak fixes, the memory footprint of long sessions with large gear databases and an active RSL Helper connection is dramatically more stable.
- **Fixed: gear-set picker menus were hard to scroll and could overflow** — set and metaset menus now show a visible scrollbar track; metaset names wrap to multiple lines instead of being cut off with "…" (which was also causing an unwanted horizontal scrollbar).

Deutsch:
- **Neu: Schutzregel-Overrides in deiner Notiz** — Mit `<!-- safeguard-overrides ... -->`-Blöcken in deiner Notiz kannst du jetzt interaktive Schieberegler, Radio-Buttons und Checkboxen erstellen, die Schutzregeln zur Laufzeit anpassen, ohne die gespeicherten Regeln direkt zu bearbeiten. Versehe deine Schutzregeln mit Tags (genau wie Rezept-Tags) und spreche sie per Tag an; Schieberegler-Werte fließen direkt in die Anzahl-Arithmetik ein (`count=$value/8` u. ä.). Nur für die Sitzung: Änderungen werden beim Neuladen verworfen — oder nutze „Anwenden und deaktivieren", um sie dauerhaft zu übernehmen.
- **Hinweis auf neue Version** — die App prüft beim Start, ob eine neuere Version verfügbar ist. Wenn ja, erscheint ein kleiner animierter Hinweis in der Kopfzeile mit einem Download-Link. Einmal weggeklickt, erscheint er erst wieder bei einer noch neueren Version.
- **Tags auf Rezept-Chips sichtbar** — Rezept-Chips können jetzt ihre Tags inline anzeigen, wie es Schutzregel-Chips bereits tun. Den Schalter findest du im Rechtsklick-Kontextmenü des Rezept-Chip-Panels unter „Tags in Chips anzeigen".
- **Automatische Gear-DB-Aktualisierung pausieren** — Rechtsklick auf den Gear-DB-Verlaufs-Button → „Automatische Aktualisierung pausieren", um eingehende RSL-Helper-Endpunkt-Daten stillschweigend zu verwerfen, ohne die Verbindung zu trennen. Außerdem wird jetzt ein Mindestabstand von 5 Sekunden zwischen aufeinanderfolgenden Endpunkt-Aktualisierungszyklen erzwungen.
- **Speicherstabilität: App wächst bei langen Sitzungen nicht mehr unbegrenzt** — die Regel-Pipeline verwendet ihren Speicher nach dem ersten großen Lauf wieder, anstatt wiederholt neue Blöcke zu belegen, die der Browser nicht zurückfordern konnte. Zusammen mit mehreren kleineren Leck-Fixes ist der Speicher-Fußabdruck langer Sitzungen mit großen Gear-Datenbanken und einer aktiven RSL-Helper-Verbindung deutlich stabiler.
- **Behoben: Gear-Set-Auswahlmenüs waren schwer zu scrollen und konnten überlaufen** — Set- und Metaset-Menüs haben jetzt eine sichtbare Scrollleistenspur; Metaset-Namen umbrechen auf mehrere Zeilen statt mit „…" abgeschnitten zu werden (was auch eine unerwünschte horizontale Scrollleiste verursachte).

## v1.0.2 — 2026-04-15
English:
- **Fixed: app crashes on Windows with large gear databases** — a bug in the internal WASM memory allocator (talc) could corrupt its own bookkeeping under specific heap fragmentation patterns, causing a hard crash (STATUS_ACCESS_VIOLATION) on Windows after loading ~8 000+ gear items and running several rule pipelines. The root cause is now patched at the allocator level; the app is stable across 100 consecutive pipeline runs in testing.
- **Fixed: autosaved gear database wiped when RSL Helper first connects** — after the app restored ~8 000 gear items from autosave, the very first push from the RSL Helper endpoint (which sends only inbox items initially) would replace the entire saved database with just those 300-or-so inbox pieces. Autosaved items are now retained until the endpoint sends a non-empty regular-artifacts payload.
- **Fixed: "Connect to RSL Helper" button did not work in Firefox when running as a local file** — Firefox returns the string `"null"` as the page origin for `file://` URLs, producing an invalid connect address. The connect URL is now constructed from the actual file path instead.
- **Fixed: right-clicking a safeguard chip to copy only copied that one chip even when multiple were selected** — when two or more safeguard chips were selected and you right-clicked one of them to copy, only the right-clicked rule was placed on the clipboard. All selected safeguard rules are now copied together as expected.
- **Shift-key hint shown in the file drag overlay** — when you drag a `.sfc` file over the app, the drop overlay now explains that holding Shift while dropping opens the selective import dialog (to merge recipes rather than replace your current file). Available in all languages.
- **Dungeon Simulator releases WASM memory after 30 seconds of inactivity** — the sim worker now terminates itself 30 seconds after a run completes. This frees the WASM linear memory so Windows can reclaim those pages, reducing the combined memory pressure that previously contributed to crashes when both the rule engine and Dungeon Simulator were active at the same time.
- **Compact group in Gear Inspector now scrolls into view automatically** — after clicking "Compact Current Group", the compacted group header smoothly scrolls into the visible area so you don't have to hunt for it.
- **"Save as…" is now always last in Gear Inspector preset menus** — in both the filter-button and sort-button preset menus, "Save as…" has moved from the top to the bottom of the list (shown in italics) so existing presets are easier to reach without accidentally clicking "Save as…".

Deutsch:
- **Behoben: App stürzte auf Windows mit großen Gear-Datenbanken ab** — ein Fehler im internen WASM-Speicher-Allokator (talc) konnte seine eigenen Verwaltungsstrukturen unter bestimmten Speicher-Fragmentierungsmustern korrumpieren und auf Windows nach dem Laden von ~8 000+ Ausrüstungsgegenständen und mehreren Regelberechnungen zum Absturz (STATUS_ACCESS_VIOLATION) führen. Die Grundursache ist jetzt im Allokator behoben; die App besteht 100 aufeinanderfolgende Pipeline-Durchläufe stabil.
- **Behoben: Autosave-Gear-Datenbank wurde beim ersten RSL-Helper-Connect überschrieben** — nachdem die App beim Start ~8 000 Ausrüstungsgegenstände aus dem Autosave wiederhergestellt hatte, ersetzte der allererste Push des RSL-Helper-Endpunkts (der zunächst nur Posteingangs-Items sendet) die gesamte gespeicherte Datenbank durch diese ~300 Einträge. Autosave-Items werden jetzt behalten, bis der Endpunkt eine nicht leere reguläre Artefakt-Liste liefert.
- **Behoben: „Mit RSL Helper verbinden"-Button funktionierte in Firefox beim Öffnen als lokale Datei nicht** — Firefox gibt für `file://`-URLs den String `"null"` als Seitenursprung zurück, was zu einer ungültigen Verbindungsadresse führte. Die Adresse wird jetzt korrekt aus dem tatsächlichen Dateipfad abgeleitet.
- **Behoben: Rechtsklick-Kopieren bei Schutzregel-Chips kopierte nur den rechts geklickten Chip** — wenn zwei oder mehr Schutzregel-Chips ausgewählt waren und man per Rechtsklick auf einen kopierte, wurde nur die rechts geklickte Regel in die Zwischenablage übernommen. Jetzt werden alle ausgewählten Regeln gemeinsam kopiert.
- **Shift-Taste-Hinweis im Datei-Drop-Overlay** — wenn du eine `.sfc`-Datei über die App ziehst, erklärt das Drop-Overlay jetzt, dass Shift gedrückt halten beim Ablegen den selektiven Import-Dialog öffnet (zum Zusammenführen statt Ersetzen). In allen Sprachen verfügbar.
- **Dungeon-Simulator gibt WASM-Speicher nach 30 Sekunden Inaktivität frei** — der Simulator-Worker beendet sich 30 Sekunden nach einem Lauf selbst. Das gibt den WASM-Linearspeicher frei, damit Windows die Seiten zurückerhalten kann; das reduziert den kombinierten Speicherdruck, der früher zu Abstürzen führte, wenn Regel-Engine und Dungeon-Simulator gleichzeitig aktiv waren.
- **„Aktuelle Gruppe komprimieren" scrollt im Gear Inspector jetzt automatisch in die Ansicht** — nach dem Klick auf „Aktuelle Gruppe komprimieren" scrollt der komprimierte Gruppen-Header jetzt sanft in den sichtbaren Bereich, sodass du nicht danach suchen musst.
- **„Speichern unter…" steht jetzt immer am Ende der Gear-Inspector-Preset-Menüs** — sowohl im Filter- als auch im Sortier-Preset-Menü ist „Speichern unter…" von der ersten Position an das Ende der Liste verschoben (kursiv dargestellt), damit vorhandene Presets leichter erreichbar sind, ohne aus Versehen „Speichern unter…" zu treffen.

## v1.0.1 — 2026-04-10
English:
- **Fixed: rule engine produced incorrect sell rules for Early-mode recipes with Potential strategy** — intermediate rules were too lenient, allowing gear to fall behind its required roll pace at upgrade milestones. Early mode now correctly requires proportional progress at each stage (+0/+4/+8/+12), so pieces that don't qualify are no longer kept by mistake. - Thanks to Krissam for reporting it!
- **Fixed: Late-mode wildcard substats could make required roll targets jointly infeasible** — when extra wildcard rolls absorbed the upgrade budget in late mode, some required stats became unreachable. A post-generation filter now rejects those distributions.
- **Fixed: Safeguard multi-edit "Apply" button stayed disabled when changing gear sets or metasets** — selecting multiple safeguard rules and editing their gear-set or metaset fields no longer keeps the Apply button stuck. The button label also now correctly reads "Apply to N Safeguards" (not "Apply to N Recipes").
- **Right-click the "Connect to RSL Helper" button to change the port** — if your RSL Helper listens on a port other than the default (8080), right-click the connect button and enter your port number. The setting is saved across sessions. A one-time hint overlay guides first-time users to the feature.
- **New champion portraits** — seven new champion icons added.

Deutsch:
- **Behoben: Regel-Engine erzeugte falsche Sell-Regeln für Early-Modus-Rezepte mit Potential-Strategie** — Zwischenregeln waren zu großzügig und erlaubten Gear, das beim Aufwerten unter dem erforderlichen Roll-Tempo lag. Early-Modus verlangt jetzt korrekt proportionalen Fortschritt bei jeder Stufe (+0/+4/+8/+12), sodass nicht qualifizierte Teile nicht mehr fälschlicherweise behalten werden. - Danke an Krissam für den Fehlerbericht!
- **Behoben: Late-Modus-Wildcard-Substats konnten erforderliche Roll-Ziele gemeinsam unerreichbar machen** — wenn Extra-Wildcards das Upgrade-Budget absorbierten, wurden manche Pflicht-Stats unerreichbar. Ein nachgelagerter Filter verwirft jetzt solche Verteilungen.
- **Behoben: Schutzregel-Mehrfachbearbeitung — „Anwenden"-Button blieb bei Set-/Metaset-Änderungen deaktiviert** — wenn mehrere Schutzregeln ausgewählt und ihr Gear-Set oder Metaset geändert wurde, blieb der Anwenden-Button gesperrt. Er funktioniert jetzt korrekt und zeigt auch die richtige Beschriftung „Auf N Schutzmaßnahmen anwenden" statt „Auf N Rezepte anwenden".
- **Rechtsklick auf „Mit RSL Helper verbinden" zum Ändern des Ports** — wenn dein RSL Helper auf einem anderen Port als dem Standard (8080) läuft, öffne per Rechtsklick auf den Connect-Button ein Eingabefeld und trage deinen Port ein. Die Einstellung wird sitzungsübergreifend gespeichert. Ein einmaliger Hinweis-Overlay führt neue Nutzer zu der Funktion.
- **Neue Champion-Porträts** — sieben neue Champion-Icons hinzugefügt.

## v1.0.0 — 2026-04-07
English:
- **Recipe files are now `.sfc`** (renamed from `.sfr`); existing `.sfr` files still load without any changes needed.
- **Side-by-side layout fills the full browser window**: builder and preview panels now stretch to the full viewport width instead of being capped — more room for your rules and gear cards on any screen size. The draggable splitter (previously only available in dev builds) is now enabled for everyone.
- **Gear Inspector card size modes**: choose **Large**, **Medium**, or **Small** cards; the column count adjusts automatically as you drag the splitter, so you always get as many columns as your panel width allows.
- **Safeguard "Improvement chance" is more accurate**: the probability that a piece still makes the cut after being fully leveled now accounts for **roll variance** (each roll can land low or high) and **glyph potential** (higher-rank gear benefits from stronger available glyphs). This reduces the number of false "100 % guaranteed" results you'd see with the old average-roll model.
- **Per-level improvement-chance thresholds + presets**: set a different threshold for each upgrade stage (+0 / +4 / +8 / +12) so freshly-dropped gear is held to a looser bar than near-max pieces. Four named presets make setup easy: **Lenient** (≥25 %), **Harsh** (≥65 %), **Graduated** (25 → 65 %), and **Soft** (3 → 50 %). The threshold *expands* the standard top-N keep-list rather than replacing it — your current best pieces are always protected first, and the threshold adds extra coverage on top.
- **Safeguard multi-select + symmetric By Match**: selecting several safeguard chips at once now makes **By Match: First** and **By Match: Any** work just like they do for recipes — First shows gear whose top-priority safeguard is one of the selected rules; Any shows all candidates for any selected rule.
- **Built-in Gear Inspector presets**: one-click **All Artifacts** and **All Accessories** filter presets, plus **Newest**, **Latest Used**, **Improvement Chance**, and **Safeguard Rank** sort presets are now available in the preset menus in all languages.
- **Gear Inspector Scope + Sources**: when **Scope** is active and you also filter by Source (e.g. Vault only), sources now act as a reference rather than a strict inclusion gate — sold-tagged items from that source are the primary sell candidates while companion pieces are drawn from your full collection for comparison.
- **Gear Analytics KPI row redesigned**: Artifacts and Accessories are shown as a combined count card; Equipped and Vault-locked are merged into one side-by-side card; 6★ + Legendary+ share a single wide card. All KPI cards fit in one row without wrapping.
- **Gear Analytics: amulet and banner slots respect ascension level** — champions not yet ascended to level 5 cannot equip an Amulet, and those below full ascension cannot equip a Banner; the Not Fully Equipped grid now correctly shows those slots as locked rather than missing.
- **Connect to RSL Helper button**: a new button in the app header (and a link in the Help dialog) lets you open the app pre-connected to a locally running RSL Helper instance in one click.
- **Final Sell defaults to Explicit Gear Sets** and now only emits rules for the active mode — no more `Use = false` rows cluttering the file for the inactive mode.
- **"No Gear-Set" is selectable again** in both recipe and safeguard builders when the slot scope includes accessories.

Deutsch:
- **Rezept-Dateien heißen jetzt `.sfc`** (umbenannt von `.sfr`); bestehende `.sfr`-Dateien laden weiterhin ohne Änderungen.
- **Side-by-Side-Layout füllt das gesamte Browserfenster**: Builder und Vorschau strecken sich jetzt auf die volle Viewport-Breite statt bei einem festen Maximum zu enden — mehr Platz für Regeln und Gear-Karten auf jedem Bildschirm. Der ziehbare Teiler (bisher nur in Entwickler-Builds) ist jetzt für alle aktiviert.
- **Gear-Inspector-Kartengrößen-Modi**: wähle **Groß**, **Mittel** oder **Klein**; die Spaltenanzahl passt sich beim Ziehen des Teilers automatisch an, damit stets so viele Spalten wie möglich in die Panel-Breite passen.
- **Schutzregel-Verbesserungschance präziser**: Die Wahrscheinlichkeit, dass ein Teil nach dem vollständigen Aufwerten noch unter die Top-N fällt, berücksichtigt jetzt **Würfelvarianz** (jeder Wurf kann niedrig oder hoch landen) und **Glyphenpotenzial** (höherrangiges Gear profitiert von stärkeren verfügbaren Glyphen). Das reduziert falsche „100 % garantiert"-Ergebnisse des alten Durchschnittswurf-Modells.
- **Verbesserungschance-Schwellwerte pro Aufwertstufe + Presets**: Der Schwellwert lässt sich jetzt für jede Aufwertstufe (+0 / +4 / +8 / +12) separat setzen — frisch gedroptes Gear darf einen lockereren Maßstab haben als fast fertig aufgewertete Teile. Vier Presets erleichtern die Einrichtung: **Locker** (≥25 %), **Streng** (≥65 %), **Abgestuft** (25 → 65 %) und **Sanft** (3 → 50 %). Der Schwellwert *erweitert* die Standard-Top-N-Schutzliste statt sie zu ersetzen — deine aktuell besten Teile bleiben immer zuerst geschützt.
- **Schutzregel-Mehrfachauswahl und symmetrisches By Match**: Mehrere Schutzregel-Chips gleichzeitig auswählen lässt **By Match: First** und **By Match: Any** genauso funktionieren wie bei Rezepten — First zeigt Gear, dessen höchstpriorisierte Schutzregel eine der gewählten ist; Any zeigt alle Kandidaten für jede gewählte Regel.
- **Integrierte Gear-Inspector-Presets**: Ein-Klick-Filter-Presets **Alle Artefakte** und **Alle Accessoires** sowie Sortier-Presets **Neuste**, **Zuletzt benutzt**, **Verbesserungschance** und **Schutzregel-Rang** sind jetzt in allen Sprachen im Preset-Menü verfügbar.
- **Gear-Inspector Scope mit Quellen**: Wenn **Scope** aktiv ist und ein Quellen-Filter gesetzt ist (z. B. nur Tresor), wirken Quellen jetzt als Referenz statt als Ausschluss — verkaufte Teile aus dieser Quelle sind die Primärkandidaten; Begleiter kommen aus der gesamten Sammlung zum Vergleich.
- **Gear-Analytics-KPI-Zeile neu gestaltet**: Artefakte und Accessoires werden als kombinierte Anzahlkarte gezeigt; Ausgerüstet und Tresor-gesperrt in einer Doppelkarte; 6★ + Legendary+ teilen sich eine breite Karte. Alle KPI-Karten passen in eine Zeile.
- **Gear Analytics: Amulett- und Banner-Slot respektieren Aufstiegslevel** — Champions unterhalb von Aufstiegsstufe 5 können kein Amulett tragen; nicht vollständig Aufgestiegene kein Banner. Das „Nicht vollständig ausgerüstet"-Grid zeigt diese Slots jetzt korrekt als gesperrt statt fehlend.
- **„Mit RSL Helper verbinden"-Button**: Ein neuer Button in der App-Kopfzeile (und ein Link im Hilfe-Dialog) öffnet die App per Klick verbunden mit einer lokal laufenden RSL-Helper-Instanz.
- **Final Sell verwendet standardmäßig Explizite Gear-Sets** und erzeugt nur noch Regeln für den aktiven Modus — keine `Use = false`-Zeilen mehr für den inaktiven Modus.
- **„Kein Gear-Set" ist wieder wählbar** in beiden Buildern, wenn der Slot-Bereich Accessoires umfasst.

## v0.9.23 — 2026-03-29
English:
- New **Gear Analytics** tab in the **Tools** dialog: load your gear database and explore your full inventory through seven interactive charts — Slot, Rank, Rarity, Sets (treemap), Result, Source, and Level. Click any segment to instantly cross-filter all other charts; double-click a slot arc to select the whole Artefact or Accessory group at once. Eight KPI cards highlight key totals (6★, Legendary+, Maxed, Equipped, Vault-locked, Chaos'd, Glyphed, Ascended). "Insights you never knew you don't need." — N.
- Performance: rule evaluation is noticeably faster, especially in **Firefox** — large gear databases now evaluate in seconds rather than minutes.

Deutsch:
- Neuer **Ausrüstungsanalyse**-Tab im **Tools**-Dialog: Lade deine Gear-Datenbank und erkunde dein gesamtes Inventar über sieben interaktive Diagramme — Slot, Rang, Seltenheit, Sets (Treemap), Ergebnis, Quelle und Level. Ein Klick auf ein Segment filtert alle anderen Diagramme sofort; Doppelklick auf ein Slot-Segment wählt die gesamte Artefakt- oder Accessoire-Gruppe auf einmal. Acht KPI-Karten zeigen wichtige Kennzahlen (6★, Legendary+, Maximal aufgestuft, Ausgerüstet, Tresor-gesperrt, Zu Chaos-Erz, Glyphe angelegt, Aufgestiegen). "Insights you never knew you don't need." — N.
- Performance: Die Regelauswertung ist spürbar schneller, besonders in **Firefox** — große Gear-Datenbanken werden jetzt in Sekunden statt Minuten ausgewertet.

## v0.9.22 — 2026-03-25
English:
- Fixed: clicking the **upgrade-chance (%) chip** on a Gear Inspector card now correctly navigates to the matching safeguard rule — a serialization mismatch had prevented this while the rank chip already worked.
- Fixed: the **mythic substat red glow** was clipped and invisible in 4-column (compact) Gear Inspector mode; it now renders correctly in both compact and full-width layouts.
- Fixed: right-clicking the safeguard chip area when it is **empty** now opens a context menu (paste, select all, delete all), matching the behavior already present in the recipe builder.
- Fixed: **≤ Epic / ≤ Rare / ≤ Uncommon** (LTE) rarity settings now generate correct sell rules — they were silently using the wrong substat-presence schedule, causing those rules to produce no rows at all for any upgrade level.
- Fixed: Flex-mode recipes no longer include empty or under-qualified rows for LTE rarities at low upgrade stages (e.g. Common at +0/+4) where not enough substats are present yet.

Deutsch:
- Behoben: Ein Klick auf den **Verbesserungschance-(%)-Chip** einer Gear-Inspector-Karte navigiert jetzt korrekt zur passenden Schutzregel — ein Serialisierungsfehler hatte dies verhindert, während der Rang-Chip bereits funktionierte.
- Behoben: Der **mythische Substat-Rotrand** wurde im 4-Spalten-(Kompakt-)Modus des Gear Inspectors abgeschnitten und war unsichtbar; er wird jetzt in beiden Layouts korrekt dargestellt.
- Behoben: Rechtsklick auf die Schutzmassnahmen-Chip-Fläche, wenn diese **leer** ist, öffnet jetzt ein Kontextmenü (Einfügen, Alle auswählen, Alle löschen) — wie es im Rezept-Builder bereits der Fall war.
- Behoben: **≤ Epic / ≤ Rare / ≤ Uncommon** (LTE)-Seltenheitseinstellungen erzeugen jetzt korrekte Sell-Regeln — sie verwendeten stillschweigend den falschen Substat-Präsenz-Plan, was dazu führte, dass diese Regeln für jede Aufstufe keine Zeilen produzierten.
- Behoben: Flex-Modus-Rezepte enthalten für LTE-Seltenheiten bei niedrigen Aufstufen (z. B. Common bei +0/+4) keine leeren oder unzureichend qualifizierten Zeilen mehr.

## v0.9.21 — 2026-03-24
English:
- Fixed: importing an SFR file while a gear database (HSF) was already loaded no longer leaves stale gear rules visible in the sellfile — the previous database is cleared automatically on import.
- The Recipe Overrides DSL in Notes gains a `not` / `!` unary operator for exclusion logic in selectors: `not tag=ore`, `!rank=5`, or `rank>=4 && not tag=chaosore` all work without needing parentheses. Precedence follows natural reading order: `not` binds tightest, then `and`, then `or`.
- New `@lockedminrolls=N` selector term (also `>=` and `<=`): target recipes in your Note overrides based on the Locked Min Rolls floor specifically, separate from the overall Min Rolls setting.
- Used above changes to fix sellfiles - Midgame is now more forgiving on substat requirements, and Chaos Ore recipes remain untouched

Deutsch:
- Behoben: Das Importieren einer SFR-Datei, während bereits eine Gear-Datenbank (HSF) geladen war, lässt keine alten Gear-Regeln mehr in der Sellfile-Vorschau stehen — die vorherige Datenbank wird beim Import automatisch geleert.
- Das Recipe-Overrides-DSL in Notizen erhält einen unären `not`/`!`-Operator für Ausschlusslogik in Selektoren: `not tag=ore`, `!rank=5` oder `rank>=4 && not tag=chaosore` funktionieren ohne Klammern. Priorität: `not` bindet am stärksten, dann `and`, dann `or`.
- Neuer Selector-Term `@lockedminrolls=N` (auch `>=` und `<=`): Rezepte in deinen Notiz-Overrides gezielt nach dem Locked-Min-Rolls-Boden ansprechen, unabhängig vom allgemeinen Min-Rolls-Wert.
- Die oben genannten Änderungen wurden verwendet, um die Sellfiles zu verbessern. - Midgame ist nun weniger streng mit den Nebenattributanforderungen, und die Rezepte für Chaos-Erz bleiben unverändert.

## v0.9.20 — 2026-03-23
English:
- The "Rule Tester" is now called **Gear Inspector** throughout the app, all menus, tooltips, and every language; the "Logic Hub" button is now called **Tools**.
- Safeguards now have their own full-featured builder mode in the builder column: toggle between Recipe Builder and Safeguard Builder, edit rules with the same collapsible-section UI (rank, rarity, faction, main stats, substats, slots, sets), and drag-and-drop chips to reorder them.
- New **Beat Equipped ≥ N%** option on safeguard rules: a piece only qualifies if its weighted score beats at least 50 %, 75 %, or 100 % of your collection-equipped gear in the same slot, matched by the full rule filter (set, rank, rarity, main stat, faction) — no more easy floors from unrelated gear.
- **Scaffold from Recipe**: one click in the Safeguards panel bootstraps a new safeguard rule from any existing recipe, pre-filling slot, sets, rank, rarity, faction, and main stat.
- Builder sections (rank, rarity, faction, main stats, substats, slots, sets, level window, min rolls, min substats, milestones) are now individually collapsible; Ctrl+click or right-click the toggle to collapse or expand all at once.
- The Min Level / Max Level toggles are replaced by a **level range slider** that snaps directly to the +0 / +4 / +8 / +12 / +16 milestones.
- **Double-click any slot button** to select or deselect the entire Artefact group (6 slots) or Accessory group (3 slots) at once — works in the recipe builder, safeguard builder, and the Gear Inspector filter panel.
- The note editor now **syntax-highlights** the recipe-overrides and config-options DSL with colored tokens for keywords, strings, operators, and stat names. The DSL also gains three new assignment fields — `slots=`, `substats=`, `mainstats=` — to replace an entire list in one line.
- **Substat Targets** moved from a separate button into the Tools dialog as its own tab.
- A new **Recipes on/off toggle** in the builder header lets you globally disable all recipes without deleting them, and gate the preview pipeline accordingly.
- Safeguard chip summaries now show slot icons, colored stat names, set icons, Per Slot / Per Set / Per Faction / Per Main Stat prefix labels, and the required count inside the mode badge.
- Filter button labels renamed: "Preview Recipes" → **Narrow**, "Recipe Filter" → **Selection** (sellfile view) or **By Match** (Gear Inspector view).
- When viewing an imported HSF file, any recipe-index references that belong to a different SFR (not currently loaded) are shown in italics and are non-clickable, making it clear they cannot be edited here.
- The guided tutorial was fully overhauled — new Safeguard and Early/Late comparison steps, redesigned Flex and Metasets sections — and localized into all 9 non-English languages.
- The autosave/restore dialog now includes builder section collapse state in the View, Filter & Sort option; Gear Inspector sort preferences are no longer shown as a separate row.
- Rule building is faster: only the recipe you just edited is rebuilt; unchanged recipes are reused.
- Right-clicking **Reset** in the Safeguard Builder now offers **Save Local Settings as User Defaults** and **Reset to Factory Defaults**, matching the Recipe Builder's right-click menu.
- Fixed: loading a new SFR file now immediately syncs the Safeguard Builder panel instead of showing stale content from the previous session.
- Fixed: undo/redo no longer leaves the sellfile preview out of sync with the chip list after a selection change.
- Fixed: custom gear added manually in the Gear Inspector now correctly matches its generated safeguard rules.
- Fixed: duplicate recipes sharing identical settings now get the correct RecipeID in the rule cache instead of all appearing as Recipe #1.
- Fixed: Dungeon Drops run estimates no longer drift upward during simulation progress.
- Fixed: incompatible sets in the set selector are now shown disabled (greyed out) rather than hidden, matching recipe builder behavior.
- **Companion context mode** in the Gear Inspector result filter: the four buttons (Keep / Sell / Scope / Unmatched) now work as independent toggles. Activating **Scope** (formerly "Matched") dims items that share the same set+slot with any sold piece so you can compare candidates in context; **Unmatched** (formerly "No Match") shows gear that no rule touches at all.
- **Draggable splitter** between the builder and preview panels in side-by-side mode: grab the handle to resize both panes; double-click resets to 50/50; your preferred width is saved.
- **Safeguard multi-edit**: select multiple safeguard rules to edit their shared fields at once; mixed values show a hatched visual overlay; keyboard shortcuts (Ctrl+A, copy/paste) work across both recipe and safeguard chip lists.
- The **Action/Mode row** in both builders (Keep/Sell/mode in recipes; activation, count, and ignore chips in safeguards) is now a collapsible section; undo/redo buttons remain pinned in the header regardless.
- Clicking a **safeguard chip** in the sell-file preview now scrolls the table to the matching safeguard block; the **Selection** filter in the preview also works for safeguard rules.
- Add **`<!-- dungeon-simulator -->`** to your Note to display a live keep-chance table for Fire Knight, Dragon, and Ice Golem across three difficulty stages (N20/N25/H10) and two boost modes, showing keep-rates at +0/+4/+8/+12/+16.
- A new **Midgame** sell-file preset is now bundled alongside Lategame and Endgame.
- Shoutout to **Red Tuxedo** and **Red VII** who provided invaluable information to create the Midgame sellfile!
- The note DSL gains two more override fields: **`gearsets=`** swaps or mutates the gear-set list, and **`metasets=`** swaps or mutates a metaset reference — both support `+`/`-` prefixes to add or remove entries without replacing the whole list.
- The `wholeline` keyword in note cards is replaced by **`[columns=N]`** (e.g., `[columns=2]` makes a card twice as wide). Notes that used `wholeline` need to be updated to `columns=N`.
- A bare **`<br>`** tag between recipe-override comment blocks in a Note forces the next card onto a new row without rendering any visible element.
- Undo/Redo revisits are now **instant**: the app caches the last 10 computed pipeline states in memory, so stepping back to a state you already visited skips all recalculation.
- Gear Inspector cards and summary chips now **animate** on data changes: newly appeared cards slide in, keep/sell outcome flips pulse with a color flash, and summary chips pulse when their group first appears — filter-switch navigation no longer triggers spurious animations.
- The Gear DB update history now shows **change counts (added / removed / updated) as the primary headline** after the first import, with the running total as secondary, making it easier to spot what changed on each push.
- When a **push endpoint** is configured, right-clicking the Push button shows an "Export to file" option that always downloads the sell-file locally, bypassing the configured endpoint.
- **Safeguard improvement-chance** is now computed in the background worker instead of on the main thread — results appear faster and challengers are projected to +16 before ranking, giving a more realistic probability.
- The live-streaming watcher (RSL Helper integration) has been updated and requires a current version of RSL Helper; the legacy connection protocol is no longer supported.
- Fixed: safeguard **anticipate mode** now generates correct rank and rarity placeholder rules.
- Fixed: **pasting a multi-recipe clipboard** that contained no safeguard data no longer silently clears your existing safeguard rules.
- Fixed: changing the slot selection now **auto-removes any mainstat or substat** that is no longer valid for that slot, instead of leaving them stuck as selected-but-unclickable.
- Fixed: the preview header now correctly shows the filtered rule count (X of Y) when the **Selection** filter is the only active filter.
- Fixed: safeguard chip summaries no longer show "Per Faction" when the rule's slot selection contains no accessory slots.
- The sort-weight popover in the Safeguard Builder now includes a **Candidate Rank List**: a scrollable ranked list of all gear candidates for the active rule, showing slot, set, faction, substat names with roll counts, a weighted score, and a kept/sold badge. The list is windowed around the quota cutoff so borderline pieces are immediately visible. Hover any row to preview the item card; click to jump straight to that artifact in the Gear Inspector. Mythical substats are highlighted with a red glow matching the Gear Inspector card style.
- Gear Inspector cards gain a **Safeguard Rank chip** (center overlay): the item's rank among all candidates for the selected safeguard rule — green for kept, red for sold. Enable it with "Show Safeguard Rank" in the Gear Inspector grid context menu. A new **Sort by Safeguard Rank** option is also available so the most-at-risk pieces surface first.
- Fixed: the **By Match: First** filter in the Gear Inspector now correctly identifies which safeguard rule first claims each item rather than checking the quota bucket, which can differ when an earlier rule already keeps the piece.
- Fixed: clicking the **upgrade-chance overlay chip** on a Gear Inspector card now correctly navigates to the matching safeguard rule in the Safeguard Builder.

Deutsch:
- Der „Rule Tester" heißt jetzt überall **Gear Inspector** (alle Menüs, Tooltips und Sprachen); aus „Logic Hub" wird der **Tools**-Button.
- Schutzmassnahmen haben jetzt einen eigenen vollwertigen Builder-Modus in der Builder-Spalte: zwischen Rezept-Builder und Schutz-Builder umschalten, Regeln mit derselben klappbaren Benutzeroberfläche bearbeiten (Rang, Seltenheit, Fraktion, Main-Stats, Substats, Slots, Sets) und Chips per Drag-and-drop neu anordnen.
- Neue Option **Beat Equipped ≥ N%** für Schutzregeln: Ein Artefakt zählt nur dann als Kandidat, wenn sein gewichteter Substat-Score mindestens 50 %, 75 % oder 100 % der ausgerüsteten Sammlung im selben Slot schlägt – gefiltert nach dem vollständigen Regelfilter (Set, Rang, Seltenheit, Main-Stat, Fraktion).
- **Scaffold from Recipe**: Ein Klick im Schutz-Panel baut aus einem vorhandenen Rezept sofort eine neue Schutzregel vor (Slot, Sets, Rang, Seltenheit, Fraktion und Main-Stat werden übernommen).
- Builder-Sektionen (Rang, Seltenheit, Fraktion, Main-Stats, Substats, Slots, Sets, Levelbereich, Min. Rolls, Min. Substats, Meilensteine) lassen sich jetzt einzeln ein- und ausklappen; Strg+Klick oder Rechtsklick auf das Pfeil-Icon klappt alle auf einmal.
- Die Min-Level-/Max-Level-Schalter sind durch einen **Levelbereich-Slider** ersetzt, der direkt auf die Meilensteine +0 / +4 / +8 / +12 / +16 einrastet.
- **Doppelklick auf einen Slot-Button** wählt oder deaktiviert die gesamte Artefakt-Gruppe (6 Slots) oder Accessoire-Gruppe (3 Slots) auf einmal – funktioniert im Rezept-Builder, Schutz-Builder und im Gear-Inspector-Filter.
- Der Notizeneditor **hebt die Syntax des recipe-overrides- und config-options-DSL farbig hervor** (Schlüsselwörter, Strings, Operatoren, Stat-Namen). Das DSL erhält außerdem drei neue Zuweisungsfelder — `slots=`, `substats=`, `mainstats=` — um eine ganze Liste in einer Zeile zu ersetzen.
- **Substat-Ziele** ist jetzt ein eigener Tab im Tools-Dialog statt einem separaten Button.
- Ein neuer **Rezepte an/aus-Schalter** im Builder-Header deaktiviert global alle Rezepte (ohne sie zu löschen) und unterbricht die Vorschau-Pipeline entsprechend.
- Schutz-Chip-Zusammenfassungen zeigen jetzt Slot-Icons, farbige Stat-Namen, Set-Icons, Präfix-Label „Pro Slot / Pro Set / Pro Fraktion / Pro Main-Stat" sowie die Mindestanzahl im Modusbadge.
- Filter-Schaltflächen umbenannt: „Preview Recipes" → **Narrow**, „Recipe Filter" → **Selection** (Sellfile-Ansicht) oder **By Match** (Gear Inspector).
- Beim Betrachten einer importierten HSF-Datei werden Rezept-Index-Referenzen aus einer anderen SFR (die nicht geladen ist) kursiv und nicht anklickbar dargestellt.
- Das Tutorial wurde komplett überarbeitet – neue Schutz- und Early/Late-Vergleichsschritte, überarbeitete Flex- und Metaset-Sektionen – und in alle 9 nicht-englischen Sprachen übersetzt.
- Der Autosave/Wiederherstellen-Dialog enthält jetzt den Builder-Sektions-Klappstatus in der Option „Ansicht, Filter & Sort"; Gear-Inspector-Sortierung wird nicht mehr als eigene Zeile angeboten.
- Regelaufbau ist schneller: Nur das gerade bearbeitete Rezept wird neu berechnet; unveränderte Rezepte werden wiederverwendet.
- Behoben: Das Laden einer neuen SFR-Datei synchronisiert jetzt sofort den Schutz-Builder, statt veraltete Inhalte der letzten Sitzung anzuzeigen.
- Behoben: Undo/Redo lässt die Sellfile-Vorschau nicht mehr aus dem Takt geraten, nachdem sich die Auswahl geändert hat.
- Behoben: Manuell im Gear Inspector hinzugefügtes Custom-Gear trifft jetzt korrekt auf seine generierten Schutzregeln zu.
- Behoben: Doppelte Rezepte mit identischen Einstellungen erhalten jetzt die korrekte RecipeID im Regel-Cache, statt alle als Rezept #1 zu erscheinen.
- Behoben: Dungeon-Drops-Laufschätzungen driften während der Simulation nicht mehr nach oben.
- Behoben: Inkompatible Sets im Set-Selektor werden jetzt ausgegraut dargestellt statt versteckt.
- **Begleit-Kontext-Modus** im Gear-Inspector-Ergebnisfilter: Die vier Schaltflächen (Keep / Sell / Bereich / Unmatched) funktionieren jetzt als unabhängige Schalter. **Bereich** (früher „Treffer") blendet Items aus demselben Set+Slot wie ein Verkaufs-Item gedimmt ein, damit du Kandidaten direkt vergleichen kannst; **Unmatched** (früher „Kein Treffer") zeigt Gear, das von keiner Regel erfasst wird.
- **Ziehbarer Teiler** zwischen Builder- und Vorschau-Spalte im Side-by-Side-Modus: Teiler ziehen, um beide Bereiche zu skalieren; Doppelklick stellt 50/50 wieder her; die gewählte Breite wird gespeichert.
- **Mehrfachbearbeitung für Schutzregeln**: Mehrere Schutzregeln auswählen und gemeinsame Felder auf einmal bearbeiten; gemischte Werte werden mit einem Schraffur-Overlay angezeigt; Tastaturkürzel (Strg+A, Kopieren/Einfügen) gelten für Rezept- und Schutzregel-Chips gleichermaßen.
- Die **Aktions-/Modus-Zeile** in beiden Buildern (Keep/Sell/Modus im Rezept-Builder; Aktivierung, Anzahl und Ignorieren-Chips im Schutz-Builder) ist jetzt eine klappbare Sektion; Undo/Redo-Schaltflächen bleiben im Header sichtbar.
- Ein Klick auf einen **Schutzregel-Chip** in der Vorschau scrollt die Sellfile-Tabelle zum passenden Schutzregel-Block; der **Selection**-Filter in der Vorschau wirkt jetzt auch für Schutzregeln.
- **`<!-- dungeon-simulator -->`** in deiner Notiz zeigt eine Live-Keep-Chance-Tabelle für Feuerritter, Drachen und Eisgolem auf drei Schwierigkeitsstufen (N20/N25/H10) und zwei Boost-Modi, mit Keep-Raten bei +0/+4/+8/+12/+16.
- Ein neues **Midgame**-Sellfile-Preset ist jetzt neben Lategame und Endgame enthalten.
- Ein herzliches Danke an **Red Tuxedo** und **Red VII** die mir unersätzliche Information zum Erstellen des Midgame Sellfiles gegeben haben!
- Das Notiz-DSL erhält zwei weitere Override-Felder: **`gearsets=`** tauscht oder mutiert die Gear-Set-Liste, **`metasets=`** tauscht oder mutiert einen Metaset-Verweis – beide unterstützen `+`/`-`-Präfixe zum Hinzufügen oder Entfernen ohne die ganze Liste zu ersetzen.
- Das Schlüsselwort `wholeline` in Notizkarten ist durch **`[columns=N]`** ersetzt (z. B. `[columns=2]` macht eine Karte doppelt so breit). Notizen, die `wholeline` verwenden, müssen auf `columns=N` aktualisiert werden.
- Ein einfaches **`<br>`**-Tag zwischen Rezept-Override-Kommentarblöcken in einer Notiz zwingt die nächste Karte auf eine neue Zeile, ohne ein sichtbares Element zu rendern.
- Undo/Redo-Revisiten sind jetzt **sofort**: Die App speichert die letzten 10 berechneten Pipeline-Zustände im Speicher – ein Schritt zurück zu einem bereits besuchten Zustand überspringt alle Berechnungen.
- Gear-Inspector-Karten und Zusammenfassungs-Chips **animieren** jetzt bei Datenänderungen: Neue Karten gleiten ein, Keep/Sell-Ergebniswechsel blitzen mit einem Farb-Pulse auf, Chips pulsen beim ersten Erscheinen ihrer Gruppe – Filterwechsel lösen keine Animations-Flut mehr aus.
- Die Gear-DB-Update-Historie zeigt nach dem Erstimport **Änderungszahlen (hinzugefügt / entfernt / aktualisiert) als Hauptüberschrift**, die Gesamtzahl rückt in die zweite Zeile.
- Wenn ein **Push-Endpunkt** konfiguriert ist, bietet das Rechtsklick-Menü am Push-Button eine „Als Datei exportieren"-Option, die das Sellfile lokal herunterlädt statt es zum Endpunkt zu senden.
- Die **Schutzregel-Verbesserungschance** wird jetzt im Hintergrund-Worker berechnet statt im Haupt-Thread – Ergebnisse erscheinen schneller und Konkurrenten werden vor dem Ranking auf +16 hochgerechnet, was eine realistischere Wahrscheinlichkeit ergibt.
- Der Live-Streaming-Watcher (RSL-Helper-Integration) wurde aktualisiert und benötigt eine aktuelle Version von RSL Helper; das ältere Verbindungsprotokoll wird nicht mehr unterstützt.
- Behoben: Der **Antizipationsmodus** von Schutzregeln erzeugt jetzt korrekte Rang- und Seltenheits-Platzhalterregeln.
- Behoben: **Einfügen eines Mehrfach-Rezept-Clipboards** ohne Schutzdaten löscht deine bestehenden Schutzregeln nicht mehr stillschweigend.
- Behoben: Ein Slot-Wechsel **entfernt jetzt automatisch** alle Mainstats oder Substats, die für den neuen Slot ungültig sind, statt sie als ausgewählt-aber-nicht-anklickbar hängen zu lassen.
- Behoben: Die Vorschau-Kopfzeile zeigt jetzt korrekt die gefilterte Regelanzahl (X von Y) an, wenn der **Selection**-Filter als einziger aktiv ist.
- Behoben: Schutzregel-Chip-Zusammenfassungen zeigen nicht mehr „Pro Fraktion" an, wenn die Slot-Auswahl der Regel keine Accessoire-Slots enthält.
- Das Gewichtungs-Popover im Schutz-Builder enthält jetzt eine **Kandidaten-Rangliste**: eine scrollbare sortierte Liste aller Gear-Kandidaten für die aktive Schutzregel, mit Slot, Set, Fraktion, Substat-Namen und Roll-Anzahl, einem gewichteten Score und einem Kept/Sold-Badge. Die Liste ist rund um den Quota-Cutoff fensteriert, damit Grenzfälle sofort sichtbar sind. Hover über eine Zeile zeigt eine Vorschaukarte; ein Klick springt direkt zu diesem Item im Gear Inspector. Mythische Substats sind mit einem roten Leuchten hervorgehoben.
- Gear-Inspector-Karten erhalten einen **Schutzregel-Rang-Chip** (mittleres Overlay): zeigt den Rang des Items unter den Kandidaten der ausgewählten Schutzregel — grün für behalten, rot für verkauft. Aktivieren über „Schutzregel-Rang anzeigen" im Gear-Inspector-Kontextmenü. Außerdem lässt sich jetzt nach **Schutzregel-Rang sortieren**, damit gefährdete Items zuerst erscheinen.
- Behoben: Der **By Match: First**-Filter im Gear Inspector ermittelt jetzt korrekt, welche Schutzregel ein Item zuerst beansprucht, statt den Schutz-Bucket zu prüfen (der sich unterscheiden kann, wenn eine frühere Regel das Item bereits behält).
- Behoben: Ein Klick auf den **Verbesserungschance-Overlay-Chip** auf einer Gear-Inspector-Karte springt jetzt korrekt zur passenden Schutzregel im Schutz-Builder.

## v0.9.19 — 2026-02-22
English:
- Rule Tester and Safeguards got major polish: better card layout in compact grids, clearer mythic highlighting, keep/sell outcome background emphasis, unified summary chips, and safeguards-specific visibility defaults.
- Tester ordering allow to sort by `Newest`.
- Updated Recipes and Sellfiles to allow more control over gear to be ored.
- Updated Recipes files with extended Safeguards for your account: We want to ensure that your likely best 16 or 32 items per artifact slot are not sold.

Deutsch:
- Rule Tester und Schutzmassnahmen wurden stark aufpoliert: besseres Kartenlayout in kompakten Grids, klarere Mythisch-Hervorhebung, Keep/Sell-Hintergrundmarkierung, vereinheitlichte Summary-Chips und safeguards-spezifische Sichtbarkeits-Defaults.
- Im Tester ist kann man jetzt nache `Neuste` sortieren.
- Rezepte and Sellfiles aktualisiert: Mehr Kontrolle über Gear das man erzen möchte.
- Die Rezepte-Datei wurde um besondere Schutzmaßnahmen für euren Account erweitert: Wir versuchen sicher zu stellen, dass eure besten 16 oder 32 Artefakte pro Slot nicht verkauft werden.

## v0.9.18 — 2026-02-20
English:
- Updated for updated Swift Parry and Deflection.
- Bundled sample sellfiles were refreshed so Swift Parry and Deflection are now handled out of the box in the Lategame and Endgame presets.

Deutsch:
- Für das aktualisierte Swift Parry and Deflection aktualisiert.
- Die mitgelieferten Beispiel-Sellfiles wurden aktualisiert: Swift Parry und Deflection sind jetzt in den Lategame- und Endgame-Presets direkt abgedeckt.

## v0.9.17 — 2026-02-20
English:
- *Rule Tester now shows a safeguard improvement-chance overlay with tooltip details*, and you can sort by Improvement Chance to surface gear with the best upgrade outlook first.
- The app now consistently uses `Recipes` and `Safeguards` in the UI, docs, and shipped examples, and recipe files are now `.sfr` by default.
- Safeguards got major control upgrades: new ignore toggles let you skip already-protected items or equipped items (collection/vault).

Deutsch:
- Die App nutzt jetzt durchgaengig `Rezepte` und `Schutzmassnahmen` in UI, Doku und Beispielen, und Rezept-Dateien sind standardmaessig `.sfr`.
- *Im Rule Tester gibt es jetzt ein Overlay fuer die Verbesserungschance mit Tooltip-Details*, und du kannst nach Verbesserungschance sortieren, um Gear mit der besten Upgrade-Perspektive zuerst zu sehen.
- Schutzmassnahmen haben neue Steuerungen: Mit Ignore-Toggles kannst du bereits geschuetzte oder ausgeruestete Items (Sammlung/Hoehle) ausklammern.

## v0.9.16 — 2026-02-10
English:
- Dungeon Drops adds a refresh button so you can rerun every dungeon without changing inputs.
- Collapsed Dungeon Drops rows can rotate the summary level (+0/+4/+8/+12/+16) forward or backward.
- Dungeon Drops percentages now use dynamic precision based on the run count, and the generic substat-odds tooltip is wider so tiny percentages stay readable.
- Min Required Rolls = 0 now truly means "no roll requirements": Auto with no roll mins resolves to Any, and manual zero suppresses roll-based thresholds so rules stay at base values.
- Champion portraits were updated, including new icons.

Deutsch:
- Dungeon Drops hat jetzt einen Refresh-Button, damit du alle Dungeons neu simulierst ohne die Eingaben zu aendern.
- Eingeklappte Dungeon-Drops-Zeilen lassen sich zwischen +0/+4/+8/+12/+16 vorwaerts oder rueckwaerts durchschalten.
- Dungeon-Drops-Prozente nutzen jetzt dynamische Dezimalstellen basierend auf der Run-Anzahl, und das generische Substat-Odds-Tooltip ist breiter damit winzige Prozentwerte lesbar bleiben.
- Min Required Rolls = 0 bedeutet jetzt wirklich "keine Roll-Anforderungen": Auto ohne Roll-Mins bleibt bei Any, und manuelles 0 unterdrueckt rollbasierte Schwellwerte damit Regeln auf Basiswerten bleiben.
- Champion-Portraets wurden aktualisiert, inklusive neuer Icons.

## v0.9.15 — 2026-02-09
English:
- Logic Hub adds a `Dungeon Drops` simulator: pick dungeon, stage, and mode (Snapshot vs Level-up) to estimate how many drops your current Sellfile keeps, with event dungeon support, boosted set weights, and a +16 summary view.
- Dungeon Drops tooltips go deeper: hover for slot/main breakdowns and generic substat odds (1-4 specific substats), and the simulator now reuses results so only the dungeons you change rerun while others keep running.
- Keep Uniques matching is more flexible: Any/All/Per Substat matching with weights (Any/All), selections are filtered by slot/main, and Anticipate mode now covers empty scope groups so gaps still get protected.
- Keep Uniques QoL: accessory `No Gear-Set` is handled consistently (Spider icon, only when accessories are in scope), rule order is stable in UI/exports, and the tab adds rule action menus plus readable clipboard copy/paste.
- Gear DB update history is clearer: toasts/history now show compact diff previews with add/remove/update counts and timestamps, and you can hide the update toast from the history menu.
- Builder guardrails improved: impossible substats are pruned by slot/main and configs with no valid substats emit no rules; gear DB imports now aggregate substat totals correctly.

Deutsch:
- Logic Hub hat jetzt einen `Dungeon Drops`-Simulator: Dungeon, Stufe und Modus (Snapshot vs Aufwertung) waehlen, um zu sehen, wie viele Drops dein aktuelles Sellfile behaelt, inkl. Event-Dungeon, Boosted-Set-Gewichte und +16-Zusammenfassung.
- Dungeon-Drops-Tooltips gehen tiefer: Hover zeigt Slot/Main-Breakdown und generische Substat-Chancen (1-4 konkrete Substats), und der Simulator nutzt Ergebnisse wieder, sodass nur geaenderte Dungeons neu laufen waehrend die anderen weiterlaufen.
- Keep Uniques Matching ist flexibler: Beliebig/Alle/Pro Substat mit Gewichten (Beliebig/Alle), Auswahl wird nach Slot/Main gefiltert, und der Anticipate-Modus deckt jetzt auch leere Scope-Gruppen ab, damit Luecken geschuetzt bleiben.
- Keep Uniques QoL: Zubehoer `No Gear-Set` wird konsistent behandelt (Spider-Icon, nur wenn Zubehoer im Scope ist), Regel-Reihenfolge ist in UI/Export stabil, plus Aktionsmenue und lesbares Clipboard Copy/Paste.
- Gear-DB-Update-Historie ist klarer: Toasts/History zeigen kompakte Diff-Previews mit Add/Remove/Update-Zahlen und Zeitstempel, und das Update-Toast laesst sich im History-Menue ausblenden.
- Builder-Guardrails verbessert: Unmoegliche Substats werden nach Slot/Main entfernt und Configs ohne gueltige Substats erzeugen keine Regeln; Gear-DB-Importe fassen Substat-Totale jetzt korrekt zusammen.

## v0.9.14 — 2026-01-26
English:
- Auto-apply now flushes before you move or reorder configs, so edits stay with the config you just moved.
- The Rule Tester header (and the Note dialog) now shows a keep/sell/keep-unique summary chip with totals; with filters active it shows filtered/total counts.
- Rule Tester grouping controls are more granular: toggle set/slot/faction grouping for artifacts vs accessories, and optionally hide headers for a flat list.
- Rule Tester matching is faster, especially with Keep Uniques enabled.
- The Rule Tester grid now defaults to 4 columns.

Deutsch:
- Auto-Apply speichert Aenderungen jetzt vor dem Verschieben/Sortieren, damit die Edits beim verschobenen Config bleiben.
- Im Rule Tester zeigt der Header (und der Notiz-Dialog) jetzt eine Keep/Sell/Keep-Uniques-Zusammenfassung mit Gesamtzahlen; bei Filtern stehen gefiltert/gesamt dabei.
- Die Rule-Tester-Gruppierung ist feiner: Set/Slot/Fraktion lassen sich getrennt fuer Artefakte und Accessoires toggeln, plus optional "keine Header" fuer eine flache Liste.
- Die Rule-Tester-Auswertung ist schneller, besonders mit Keep Uniques.
- Das Rule-Tester-Grid startet jetzt standardmaessig mit 4 Spalten.

## v0.9.13 — 2026-01-20
English:
- Rule Tester cards can now show an optional "Add Config" action that builds Keep/Sell configs from the selected item and jumps you to the new config.
- Keep Unique coverage is more reliable: configs tagged `ignore_keep_unique` no longer count toward uniqueness checks, and tester labels stay in sync after renaming rules.
- Live RSL Helper DB streaming is more dependable and faster for big databases, plus the push status now includes a received timestamp.
- Push endpoints now require `ws://` or `wss://` URLs.
- The config-name filter hint now calls out tag and regex matching.

Deutsch:
- Rule-Tester-Karten koennen jetzt optional eine Aktion "Konfig hinzufuegen" anzeigen, die aus dem Item Keep/Sell-Konfigs baut und direkt zur neuen Konfig springt.
- Keep Unique ist verlaesslicher: mit `ignore_keep_unique` getaggte Konfigs zaehlen nicht mehr fuer die Unique-Abdeckung, und Tester-Labels bleiben nach Umbenennungen aktuell.
- Live-Streaming der RSL-Helper-Datenbank ist robuster und schneller bei grossen Datenbanken; der Push-Status zeigt jetzt den Empfangszeitpunkt.
- Push-Endpunkte akzeptieren jetzt nur noch `ws://`- oder `wss://`-URLs.
- Der Filter-Hinweis beim Konfig-Namen nennt jetzt Tag- und Regex-Suche.

## v0.9.12 — 2026-01-10
English:
- The Argonites faction is now available in builder faction menus, filters, and gear database imports.

Deutsch:
- Die Fraktion der Argoniten ist jetzt in Builder-Menues, Filtern und Gear-DB-Importen verfuegbar.

## v0.9.11 — 2026-01-04
English:
- Notes can now host Config Options questions that apply tag-driven overrides at runtime—toggle tagged configs and adjust rank/rarity/level windows — without editing the stored configs.
- Config tags are now first-class in the builder: tags live beside Export Mode and the name filter also matches tag tokens.
- Rule Tester sorting adds grouping modes (set+faction, accessories-by-faction, split artifacts/accessories, or flat) with a global substat sort when grouping is custom, and mythic bonus highlights are clearer.

Deutsch:
- Notizen koennen jetzt Config-Options-Fragen enthalten, die Tags zur Laufzeit auswerten: getaggte Configs werden ein/aus geschaltet und Rank/Rarity/Level werden temporaer ueberschrieben, ohne die gespeicherten Configs zu aendern.
- Config-Tags sind jetzt fest im Builder verankert: Tags sitzen neben dem Exportmodus, und der Namensfilter findet auch Tag-Tokens.
- Die Rule-Tester-Sortierung hat neue Gruppierungen (Set+Fraktion, Accessoires nach Fraktion, Split Artefakte/Accessoires oder flach) mit globaler Substat-Sortierung bei Sondergruppen, und Mythisch-Boni sind deutlicher hervorgehoben.

## v0.9.10 — 2025-12-15
English:
- The standalone Gear window is gone: use the header `Logic Hub` button and switch to the `Gear` tab to import your RSL Helper `.db`, add manual test items, and reset the Gear list without leaving the dialog.
- Rule Tester sorting is much stronger: sort by Last Used and/or substat priorities, flip direction per key, and use Normalized mode (with weights) to compare mixed stats; the restore prompt can now bring back your saved sort setup.
- Tester cards can show normalized “rating” overlays: enable overlay presets, reuse your sort weights, and toggle whether glyphs count so scores match what you expect.
- Preview filters get new power tools: right-click a substat to mark “must NOT have”, use per-section Clear buttons to reset just one area, and save/load named filter presets; broken localStorage no longer crashes the filter panel.
- New gear set coverage: the Mercurial set (1–9 pieces) is now recognized and also included in the **Lategame** sellfile.
- Keep Uniques rules are easier to manage.

Deutsch:
- Das separate Ausrüstungsfenster ist weg: Nutze den Header-Button `Logic Hub` und den Tab `Ausrüstung`, um deine RSL-Helper-`.db` zu importieren, manuelle Test-Items anzulegen und die Ausrüstungsliste im Dialog zurückzusetzen.
- Die Sortierung im Regel-Tester ist deutlich besser: Sortiere nach „Zuletzt benutzt“ und/oder Substat-Prioritäten, drehe die Richtung pro Schlüssel um und nutze den Normalized-Modus (mit Gewichten), um gemischte Stats fair zu vergleichen; im Restore-Dialog lässt sich die Sortierung jetzt mit wiederherstellen.
- Tester-Karten können Normalized-„Ratings“ als Overlay anzeigen: Presets aktivieren, Sort-Gewichte wiederverwenden und umschalten, ob Glyphen zählen, damit die Scores zu deiner Erwartung passen.
- Die Vorschau-Filter haben neue Werkzeuge: Rechtsklick auf einen Substat setzt „darf NICHT haben“, pro Abschnitt gibt es Clear-Buttons zum Teil-Reset, und du kannst Filter-Presets speichern/laden; kaputtes localStorage bringt das Filterpanel nicht mehr zum Absturz.
- Neue Set-Abdeckung: Das Mercurial-Set (1–9 Teile) ist jetzt enthalten und natürlich auch im **Lategame** sellfile referenziert.
- Keep-Uniques-Regeln sind leichter zu benutzen.

## v0.9.9 — 2025-12-07
English:
- Load your full RSL Helper gear database straight into the new Rule Tester view, then watch every config decide Keep or Sell before you export the Sellfile.
- The Rule Tester grid groups items by set and faction, shows champion portraits, offers keep/sell chips that jump back to the builder, and gains context menus plus search hotkeys so scanning huge inventories stays friendly.
- Unique or at-risk items are spotlighted: the grid collapses to the truly unique groups, adds a clear All/Selection toggle, and paints a green Keep Uniques chip so you instantly know why a piece is protected.
- Keep Unique protection now lives inside a dedicated Keep-Unique tab in the Logic Hub dialog, letting you define slot/set/rank/rarity/main/faction combos, see how many copies you own, highlight the matching tester cards, and merge the rules into exports with one switch.

Deutsch:
- Du kannst jetzt deine komplette RSL-Helper-Gear-Datenbank direkt im neuen Rule-Tester-View laden und sehen, welche Config jedes Item behalten oder verkaufen würde, bevor du das Sellfile exportierst.
- Das Rule-Tester-Grid gruppiert Items nach Set und Fraktion, zeigt Champion-Porträts, bringt Keep/Sell-Chips zurück in den Builder und liefert Kontextmenüs plus Such-Hotkeys, damit große Inventare übersichtlich bleiben.
- Einzigartige oder gefährdete Items werden hervorgehoben: Das Grid klappt auf die wirklich einzigartigen Gruppen ein, hat einen klaren All/Selection-Schalter und zeigt einen grünen „Keep Uniques“-Chip, damit du sofort weißt, warum ein Teil geschützt ist.
- Keep-Unique-Schutz lebt jetzt in einem eigenen Tab im Final-Sell-Dialog – hier definierst du Slot/Set/Rang/Seltenheit/Main/Fraktion-Kombos, siehst sofort, wie viele Kopien du besitzt, markierst die entsprechenden Tester-Karten und übernimmst die Regeln per Schalter in jeden Export.

## v0.9.8 — 2025-11-03
English:
- Multi-edit stays inline: select several configs to see mixed placeholders, total rule counts, and an `Apply to N configs` button; chip menus add Select All / Copy All options and the header counter shows how many configs are filtered or selected. Roll Target overrides now patch across every selected config, and the old Draft visibility is renamed to Export Mode → Separator so dividers are clearer.
- Substat controls got their own right-click menu: lock badges toggle independently, the menu edits min/max rolls without leaving the builder, and the new Roll Targets grid lets you enter Base/+1…+5 totals with spinner controls, show override summaries on the chips, and clear back to the global targets; multi-edit keeps mixed cues visible while you sync overrides.
- Undo/Redo describe the next change and expose a history timeline on right-click, so you can jump back to a named snapshot or clear the stack with confidence.
- Builder feedback tightens up: the rule-count chip turns red when a config would export zero rules, every context menu has a close button, and the Sellfile preview flashes a scroll-range overlay after fast scrolls so you always know where you are in long tables.
- Save and Export buttons display a dirty badge when the HSFC or sellfile has unsaved changes, preview/export layouts stay balanced when filters hide rows, and narrow screens auto-zoom to keep the builder and preview side by side. Rule builds are cached so large projects stay responsive, and flex exports keep every valid combination instead of dropping ring rows.
- Updated the Auto + Late tutorial copy across German, Spanish, French, Portuguese, Russian, Turkish, Ukrainian, and other catalogs so every language matches the new lock/context menu flow.
- Mythical gear with locked totals behaves correctly: Minimum Required Rolls count the Mythical pre-roll against your locked stats, so unlocked substats stay at baseline until they have to roll and the config still emits rules.
- Export menu can skip disabled configs: right-click `Export RSL Helper Sellfile`, toggle `Omit disabled rules when exporting`, and `Use = false` rows stay out of downloads and push streams; the choice persists across sessions in every language.

Deutsch:
- Mehrfachbearbeitung bleibt im Builder: Wähle mehrere Konfigurationen, siehst Misch-Platzhalter, Gesamtregelanzahl und eine Schaltfläche „Auf N Konfigs anwenden“; Chip-Menüs bieten „Alle auswählen“/„Alle kopieren“ und der Zähler zeigt, wie viele Konfigs ausgewählt oder ausgeblendet sind. Roll-Richtwerte landen jetzt per Multi-Edit auf allen markierten Konfigs, und die alte Sichtbarkeit „Draft“ heißt nun Exportmodus → „Separator“, damit Trenner direkt auffallen.
- Substat-Controls haben jetzt ein eigenes Rechtsklick-Menü: Sperr-Icons lassen sich separat schalten, das Menü ändert Min-/Max-Rolls direkt im Builder, und das neue Roll-Richtwerte-Raster nimmt Basis- sowie +1…+5-Werte mit Spinner-Steuerung auf, zeigt Übersichten auf den Chips und springt bei Bedarf zurück auf die globalen Vorgaben; Mehrfachbearbeitung hält gemischte Zustände sichtbar, während du Überschreibungen synchronisierst.
- Undo/Redo beschreiben jetzt die nächste Änderung und ein Rechtsklick öffnet eine Verlaufsliste, in der du zu benannten Snapshots springen oder den Stapel gezielt leeren kannst.
- Rückmeldungen im Builder wurden geschärft: Der Regelzähler färbt sich rot, sobald eine Konfiguration keine Regeln mehr erzeugt, jedes Kontextmenü bringt jetzt eine Schließen-Schaltfläche mit und die Sellfile-Vorschau blendet nach schnellen Scrolls kurz eine Bereichsanzeige ein, damit du dich in langen Tabellen orientieren kannst.
- Die Schaltflächen zum Speichern und Exportieren zeigen einen Hinweis, wenn HSFC oder Sellfile ungesicherte Änderungen haben; Vorschau und Export bleiben trotz Filterung gleich hoch und auf schmalen Monitoren zoomt die App automatisch, um Builder und Vorschau nebeneinander zu halten. Die Regel-Erstellung wird zwischengespeichert, damit große Projekte reaktionsschnell bleiben, und Flex-Exporte behalten jede gültige Kombination statt Ring-Zeilen zu streichen.
- Die Auto-+Spät-Anleitung wurde für Deutsch, Spanisch, Französisch, Portugiesisch, Russisch, Türkisch, Ukrainisch und weitere Kataloge aktualisiert, damit jede Sprache den neuen Lock-/Kontextmenü-Ablauf abdeckt.
- Mythische Werte bei Locks bleiben stabil: Mindestwürfe zählen den Vorabwurf jetzt auf die gesperrten Stats, dadurch bleiben freie Substats unberührt, bis sie wirklich rollen müssen, und die Konfiguration erzeugt weiterhin Regeln.
- Export-Menü kann deaktivierte Regeln auslassen: Rechtsklick auf `RSL-Helper-Sellfile exportieren`, `Deaktivierte Regeln beim Export auslassen` aktivieren – dann landen `Use = false`-Zeilen weder im Download noch beim Push, und die Auswahl bleibt sprachübergreifend gespeichert.

## v0.9.7 — 2025-10-06
## English
- Config chips gained a Draft mode (produces no rules) so you can drop labeled separators; duplicates are flagged, chips can be limited to whatever the preview filter keeps, and the bundled sample HSFC/HSF were refreshed to use the new structure.
- Notes can display config chips or metasets by adding `<!-- recipes:... -->` / `<!-- recipes-re:"..." -->`; the editor adds insert buttons so shared projects stay self-explanatory.
- Builder clean-up: removed the `Any` buttons from Slots/Mainstats/Substats in favour of clear icons, matching how other pickers work; reset buttons now say `Reset Config`.
- Logic Hub keeps the same controls but the wording and inline hints now explain what turning it on does and why all sets are listed explicitly; the preview badge highlights when the export hover suggests enabling it.
- Visual pass: slot art now uses the RSL Helper icons, faction icons show up on chips, filters, and in the Rule Tester, and localisation strings were updated in every shipped language.
- Rule Tester and filters: you can filter by config name, pull incoming gear in from the db watcher, see faction icons alongside set icons, and the optional export push endpoint can send the `.hsf` straight to a receiver when configured.

## Deutsch
- Config-Chips haben jetzt einen Draft-Modus (erzeugt keine Regeln), damit sich beschriftete Trenner anlegen lassen; Duplikate werden markiert, Chips können auf die Regeln aus der Vorschau gefiltert werden, und die beigelegten Beispiel-HSFC/HSF sind entsprechend aktualisiert.
- Notizen können Config-Chips oder Metaset-Listen anzeigen (`<!-- recipes:... -->` bzw. `<!-- recipes-re:"..." -->`); der Editor bringt Einfüge-Schaltflächen mit, damit geteilte Projekte den Kontext gleich mitliefern.
- Builder-Aufräumarbeiten: Die `Any`-Schaltflächen bei Slots/Mainstats/Substats sind zugunsten von Löschen-Icons verschwunden und entsprechen jetzt den anderen Auswahlfeldern; die Reset-Schaltfläche heißt nun `Reset Config`.
- Final-Sell-Dialog: gleiche Steuerung, aber mit klareren Texten und Hinweisen darauf, warum alle Sets explizit gelistet werden; das Badge in der Vorschau hebt sich beim Export-Hover hervor, wenn Final Sell deaktiviert ist.
- Optischer Durchgang: Slot-Grafiken stammen jetzt aus RSL Helper, Fraktions-Icons tauchen auf Chips, in Filtern und im Rule Tester auf, und alle Sprachen wurden textlich angepasst.
- Rule Tester und Filter: Filter nach Config-Namen, Übernahme von Tester-Items aus dem Beispiel-Server, Fraktions- und Set-Icons nebeneinander sowie eine optionale Export-Push-Funktion, die die `.hsf` bei konfiguriertem Ziel direkt verschickt.

## v0.9.6 — 2025-09-29
English:
- Auto Rarity now picks the first rarity that can spawn your required substat count. Flex only turns on when optional stats or roll targets need permutations, and Late keeps Rare paths visible even when the first roll lands on an optional stat. Exports keep every viable combo without duplicate rows.
- Rule Tester opens with six curated sample items and stays fast thanks to virtualized rows. A Reset button and builder links on match chips make it easy to see which rule keeps or sells each scenario.
- Builder guidance improved: the cheat sheet highlights Auto ≥ and Flex setups with badges, and the tutorial scrolls the preview to spotlight Late milestones. The Help dialog keeps the language picker in view and adds Italian plus Brazilian Portuguese translations.

Deutsch:
- Auto-Rarität wählt jetzt die erste Seltenheit, die deine geforderte Substat-Anzahl tragen kann. Flex springt nur an, wenn optionale Stats oder Rollziele Permutationen erzwingen, und Spät-Zweige bleiben sichtbar, selbst wenn ein seltener Drop seinen ersten Roll auf einen Optionalen setzt. Exportierte Regeln behalten dadurch jede gültige Kombination ohne Dubletten.
- Der Rule Tester startet mit sechs kuratierten Beispiel-Gegenständen und bleibt dank virtualisierten Zeilen flott. Ein Zurücksetzen-Dialog und Builder-Links auf den Treffer-Chips zeigen dir schnell, welche Regel behält oder verkauft.
- Bessere Hilfen im Builder: Das Cheat Sheet erklärt Auto ≥ und Flex mit Badges, und das Tutorial scrollt die Vorschau automatisch zu den Spät-Meilensteinen. Der Hilfe-Dialog zeigt den Sprachschalter prominent an und liefert neue Übersetzungen für Italienisch sowie brasilianisches Portugiesisch mit.

## v0.9.4 — 2025-09-22
English:
- Builder defaults to Auto rarity: it picks the lowest rarity that can start with your required substats or reach the roll totals, Auto ≥ keeps higher floors when you need them, and the new Locked toggle lets min-roll sums consider only the stats you locked.
- Config chips grew up: multi-select lets you duplicate, move, or delete several configs at once, duplicate chips get flagged, auto-reset after insert is optional, and badges now show slot icons with hollow roll rings.
- Sellfile Preview adds filters for sets, rank, rarity, and faction alongside color-blind palettes and smoother hover/scroll so big tables stay readable.
- Rule Tester dialog debuts under Preview → Rule Tester, letting you paste items, adjust rolls per level, and see which rule keeps or sells them; scenarios autosave between visits.
- A guided tutorial with breadcrumbs walks through basic and advanced configs, resets the sandbox when it ends, and lives behind the Help button.
- Configs now save as `.hsfc`, and copy/paste carries the metasets a single config needs so sharing snippets just works.

Deutsch:
- Der Builder nutzt jetzt standardmäßig Seltenheit Auto: Die App wählt die niedrigste Seltenheit, die deine Pflicht-Substats oder Roll-Summen tragen kann; per Auto ≥ hältst du Rare/Epic-Böden fest, und ein neuer Locked-Schalter lässt Mindestwürfe nur für gesperrte Stats zählen.
- Config-Kacheln sind flexibler: Multiselect dupliziert, verschiebt oder löscht mehrere Einträge auf einmal, Dubletten werden markiert, Auto-Reset nach dem Einfügen ist optional, und Badges zeigen Slot-Icons plus hohle Roll-Ringe.
- Die Sellfile-Vorschau bietet jetzt Filter für Sets, Rang, Seltenheit und Fraktion sowie farbenblinde Paletten und glatteres Scrollen, damit große Tabellen lesbar bleiben.
- Der neue Rule Tester unter Vorschau → Rule Tester erlaubt, Items einzutragen, Roll-Stände je Stufe anzupassen und sofort zu sehen, welche Regel sie behält oder verkauft; Szenarien bleiben per Autosave erhalten.
- Ein geführtes Tutorial mit Breadcrumbs führt Schritt für Schritt durch einfache und komplexe Konfigurationen und setzt die App danach wieder zurück; starte es über Hilfe.
- Configs werden als `.hsfc` gespeichert, und Copy/Paste bringt die dazugehörigen Metasets gleich mit – so lassen sich Einzel-Konfigs leichter teilen.

## v0.9.2 — 2025-09-08
English:
- Final Sell now writes Sell rules that list every known set and offers clearer gear/level toggles, so new RSL sets never slip through.
- Builder adds a `Min Required Rolls` aggregate control and deterministic Mythical handling, keeping Potential rows and roll math consistent no matter the click order.
- Set pickers gain search plus icon, Game, or A–Z views that persist across the builder and metaset dialog, helping you find sets faster.
- Metaset management supports replace-on-delete and reset flows, auto-names new groups, and keeps builder/config references in sync to avoid orphaned metasets.
- Config saves (`.hsfr`) can now include a Markdown Note that reloads automatically; drag & drop works anywhere with a global overlay and copy/paste preserves the note.

Deutsch:
- Final Sell schreibt jetzt Sell-Regeln mit allen bekannten Sets und bietet klarere Gear-/Level-Optionen, damit neue Raid-Sets nicht versehentlich durchrutschen.
- Der Builder hat den Schalter `Min Required Rolls` (Auto/1–5) und behandelt Mythical deterministisch, sodass Potential-Zeilen und Roll-Mathematik unabhängig von der Klick-Reihenfolge stimmen.
- Die Set-Auswahl bietet Suche sowie Icon-, Game- und A–Z-Ansichten, merkt sich deine Wahl und der Metaset-Dialog nutzt denselben Blick, damit du Sets schneller findest.
- Metaset-Verwaltung erlaubt Löschen mit Ersetzen-Optionen oder Reset auf Default, vergibt neue Namen automatisch und aktualisiert Builder/Configs sauber.
- HSFR-Saves können jetzt eine Markdown-Notiz enthalten, die beim Laden sofort erscheint; Drag & Drop funktioniert überall mit Overlay und Copy/Paste übernimmt die Notiz.

## v0.8.5 — 2025-08-29
English:
- Roll badges now split Min and Max: click sets 1–5 required rolls (green) and Shift+click caps 0–5 allowed rolls (red); Max = 0 forbids that substat and generated rules respect both limits.
- Rarity "Any" no longer assumes a Mythical pre-roll by default—the builder only adds the fifth roll when your thresholds demand it and hides combinations that can never reach the mins.
- Substat selectors stay put and preview their badge on hover, so locks and roll states are visible before you click.

Deutsch:
- Roll-Badges trennen jetzt Minimum und Maximum: Klick setzt 1–5 Pflichtwürfe (grün) und Shift+Klick begrenzt 0–5 zulässige Würfe (rot); Max = 0 sperrt den Substat und die Regeln beachten beide Grenzen.
- Seltenheit "Beliebig" geht nicht mehr automatisch von einem mythischen Vorab-Wurf aus – der Builder ergänzt den fünften Wurf nur, wenn deine Schwellen ihn brauchen, und blendet unerreichbare Kombinationen aus.
- Die Substat-Auswahl bleibt stabil und zeigt das Badge beim Hover vorab, sodass du Locks und Roll-Zustände vor dem Klick siehst.

## v0.8.0 — 2025-08-27
English:
- Config chips now have right-click controls: duplicate, move to the top/bottom, copy a single config, or use the chip area menu to copy the entire HSFR or paste into an empty list. Manual copy/paste dialogs appear automatically when the browser blocks clipboard access.
- Copy All and Save now include version, metasets, minima, and the All (Explicit) toggle, and loading normalizes older exports while keeping wildcard roll targets and roll limits inside 0–5 so HSFRs round-trip safely.
- Default substat chip colors were retuned to a brighter, higher-contrast palette that lines up with Raid’s stat colors and stays readable in the dark theme.

Deutsch:
- Konfig-Chips bieten jetzt per Rechtsklick Duplizieren, ganz nach oben/unten verschieben und Einzelkopie; der Chipbereich hat ein Menü für „Alles kopieren (.hsfr)“ oder Einfügen, auch wenn noch keine Regeln existieren. Fallback-Dialoge springen ein, sobald der Browser den Clipboard-Zugriff sperrt.
- „Alles kopieren“ und Speichern schreiben Version, Metasets, Minima sowie den All-(Explicit)-Schalter mit, und beim Laden werden alte Exporte normalisiert, behalten aber Wildcard-Rollziele und Roll-Grenzen zwischen 0 und 5, sodass HSFR-Dateien zuverlässig zurückkehren.
- Die Standardfarben der Substat-Chips wurden auf eine hellere, kontrastreichere Palette umgestellt, die zu den Raid-Statfarben passt und im Dark-Theme besser lesbar ist.

## v0.7.5 — 2025-08-27
English:
- Roll Strategy now includes an Auto mode (and is the default) that switches between Strict and Potential as soon as you add numeric roll badges, so you no longer have to retoggle once items get circled.
- The builder cleans up config chips and summaries: the help icon lives next to Roll Strategy, and list entries hide "Any" rank/rarity and the old Required/Potential flags so you only see the filters you set.
- Mythical gear counts its level-0 pre-roll in both Strict and Potential math, letting SPD(5) and similar badges evaluate correctly and matching the Count Rolls switch (From vs All).
- Potential preview rows stay deduplicated after a target becomes feasible, so each strict row appears once even when progress rows remain.
- Added the default metaset "Accessoires - Special" to quickly target the unique accessory set IDs without hand-picking each one.

Deutsch:
- Die Roll-Strategie hat jetzt einen Auto-Modus (Standard), der zwischen Streng und Potenzial wechselt, sobald du numerische Roll-Badges setzt – manuelles Umstellen entfällt.
- Der Builder räumt die Konfig-Kacheln auf: Das Hilfe-Icon sitzt direkt am Roll-Strategie-Label, und in der Liste verschwinden "Beliebig"-Rank/Rarity sowie die alten Required/Potential-Kürzel.
- Mythische Ausrüstung zählt den Vorab-Roll auf Stufe 0 nun korrekt in Streng- und Potenzial-Berechnungen, sodass SPD(5) und Co. passend zum Count-Rolls-Schalter geprüft werden.
- Potenzial-Vorschauen enthalten keine doppelten Zeilen mehr, wenn ein Ziel erreicht ist – die strenge Zeile erscheint nur einmal neben den Fortschrittsreihen.
- Neu dabei ist das Standard-Metaset "Accessoires - Special", damit du die speziellen Zubehör-Sets ohne Einzelwahl aktivieren kannst.

## v0.7.1 — 2025-08-26
English:
- Builder now loads curated metaset presets for speed, nuker, so you can slot popular set bundles without building them from scratch.

Deutsch:
- Der Builder bringt jetzt kuratierte Metaset-Vorlagen für Speed-, Nuker-, Support- und Tank-Setups mit, damit du beliebte Set-Bündel ohne Eigenbau nutzen kannst.

## v0.7.0 — 2025-08-26
English:
- `Evaluate From` adds an `Any` option (automatically sets Roll Strategy to Off) so you can demand substats at every level; level headings now show 0–3, 4–7, etc., and exports drop the level gate when you pick Any.
- Potential strategy keeps the strict row plus any catch-up rows once badge targets are feasible and lets leftover rolls land on untargeted substats, so promising items stay eligible until they can finish at 16.
- Roll badges now respond to right-click by stepping backward through ★/0–5, making it faster to undo overshoots while adjusting minimum rolls.
- A new info popover beside Roll Strategy walks through Count Rolls, Evaluate From, Strategy, and Required with an example so you can see how the controls interact at a glance.
- Merged Preview uses wider columns, larger fonts, and synchronized heights on ultra-wide layouts, making large exports easier to scan.

Deutsch:
- `Evaluate From` bietet jetzt die Auswahl „Any“ (stellt Roll Strategy automatisch auf Off), damit du Substats auf jedem Level verlangen kannst; Levelanzeigen zeigen 0–3, 4–7 usw., und der Export verzichtet dabei auf eine Level-Grenze.
- Die Strategie „Potential“ behält nach erreichbarer Badge-Zielsetzung die strikte Zeile plus alle nachholbaren Fortschrittszeilen bei und lässt Restwürfe auf ungezielte Substats fallen, sodass aussichtsreiche Items bis Level 16 erhalten bleiben.
- Roll-Badges lassen sich per Rechtsklick rückwärts durch ★/0–5 schalten, wodurch sich Fehleingaben beim Einstellen der Mindestwürfe schneller korrigieren lassen.
- Ein neues Info-Popup neben Roll Strategy erklärt Count Rolls, Evaluate From, Strategy und Required samt Beispiel, damit du das Zusammenspiel der Regler sofort siehst.
- Die Merged Preview nutzt breitere Spalten, größere Schrift und gleicht auf sehr breiten Monitoren die Höhe mit dem Builder ab, sodass große Exporte besser lesbar sind.

## v0.6.1 — 2025-08-25
English:
- Builder progress now autosaves: configs, metasets, minima, and the “All (Explicit)” toggle are stored locally with an integrity check, the app offers to restore them on launch, and your color or column tweaks stick between visits.
- Substat roll badges picked up a star wildcard and sturdier minimum logic, so Strict/Potential enforce “at least N rolls” as soon as that level is feasible and single-stat keeps like SPD≥1 behave the way you expect.
- The merged preview table gained a Manage Colors dialog, persistent column menu (auto-fit widths, wrap toggle), and virtualization with a “Showing X–Y of Z” readout so giant sell files stay readable and fast.
- On wide monitors the builder and preview panes sit side-by-side with matched heights, and each section keeps its helper copy inline, trimming wasted space.

Deutsch:
- Der Builder speichert deine Sitzung jetzt automatisch lokal (Konfigs, Metasets, Minima und der Schalter „All (Explicit)“) und bietet beim Start eine Wiederherstellung an; Farb- und Tabelleneinstellungen bleiben ebenfalls erhalten.
- Substat-Badges haben ein Stern-Wildcard und eine robustere Mindestlogik bekommen, sodass Streng/Potenzial „mindestens N Würfe“ ab dem ersten möglichen Level durchsetzen und Einzel-Checks wie SPD≥1 verlässlich greifen.
- Die Merged Preview erhielt einen „Manage Colors…“-Dialog, ein dauerhaftes Spaltenmenü (Auto-Fit, Zeilenumbruch) und Virtualisierung samt „X–Y von Z“-Anzeige, wodurch auch große Sellfiles lesbar und schnell bleiben.
- Auf breiten Monitoren stehen Builder und Vorschau jetzt nebeneinander mit abgestimmter Höhe, und die Abschnittstitel führen ihre Hilfetexte inline, sodass weniger Platz verloren geht.

## v0.5.0 — 2025-08-25
English:
- Create Keep/Sell configs with auto rarity math, milestone windows, slot/faction/set filters, multi-main picks, and per-substat roll controls (locks, min/upper limits, wildcard targets) so the export mirrors Raid's upgrade rules.
- Reuse named metasets for gear sets — search, icons, context menus, conflict resolution, and default groups keep builder picks and saved configs in sync.
- Preview everything before export: merged Sellfile table with color-coded chips, duplicate warnings, filters, and a Rule Tester; Final Sell remainder modes cover the items your Keep configs skip.
- Quality-of-life everywhere: drag & drop HSF/HSFC and localization files, autosave + restore, config notes, copy/paste sharing, tutorial & help overlays, customizable substat colors, and one-click deduped exports.

Deutsch:
- Erstelle Keep/Sell-Konfigs mit automatischer Seltenheitsberechnung, Meilenstein-Fenstern, Slot-/Fraktions-/Set-Filtern, Multi-Hauptattributen und Substat-Rollkontrollen (Sperren, Mindest-/Obergrenzen, Wildcards), damit der Export die Aufwertungsregeln von Raid exakt widerspiegelt.
- Gruppiere Sets als benannte Metasets – Suche, Icons, Kontextmenüs, Konfliktauflösungen und Standardgruppen halten Builder-Auswahl und gespeicherte Konfigs synchron.
- Vorschau vor dem Export: Zusammengeführte Sellfile-Tabelle mit farbcodierten Chips, Duplikat-Warnungen, Filtern und Rule Tester; Final-Sell-Restmodi fangen alles ab, was deine Keep-Konfigs offenlassen.
- Komfortfunktionen überall: Drag & Drop für HSF/HSFC und Lokalisierungen, Autosave + Wiederherstellung, Config-Notizen, Copy/Paste-Sharing, Tutorial- und Hilfe-Overlays, anpassbare Substat-Farben und ein Klick für deduplizierte Exporte.
