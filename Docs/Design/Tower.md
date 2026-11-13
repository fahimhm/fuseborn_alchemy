# The Athanor — Fuseborn PvE

**Status:** Draft, first idea (2026-11-13). Rules: GDD §6.6 (PvE), §6.12 (time, stars), §6.13 (zones), §4.1 (fusion). Lore: [Lore.md](Lore.md).

## 1. What it is
The **Athanor** is a giant alchemical furnace shaped like a tower (in real alchemy, the athanor is the alchemist's tower-furnace). An ancient Alchemist built it for the **Great Work**; the reaction went wrong and **never stopped burning**.
- **It is the source of Runoffs.** Failed reactions keep forming inside; some leak out into the world.
- **Why the guild climbs:** every floor holds recovered reagents (cards) and treasure (Coins); higher floors hold richer ones. Rival Alchemists climb too: it's a race. The top may hold the finished Great Work (an open hook, no decision yet).
- **The Athanor grows.** The reaction keeps building new floors upward; each season a newly risen part opens (§7).
- **Every floor is an experiment** left running: its own environment, a journal-page backstory, and sometimes a riddle.

## 2. Structure
- ✅ **The tower is the whole PvE.** It replaces the earlier chapters (GDD §6.6).
- ✅ **One floor = one Gate** (one alchemical process), with its own environment modifier and story.
- ✅ **Each floor has about 10 rooms** (stages with waves). Rooms open one after another; the **last room is the boss room**.
- ✅ **Season 1:** 12 floors (Ripley's Twelve Gates) × ~10 rooms = **~120 stages**.
- ✅ **Acts:** the four stages of the Great Work group the floors 3 by 3 for mood and colors: **Nigredo** (black) floors 1–3, **Albedo** (white) 4–6, **Citrinitas** (yellow) 7–9, **Rubedo** (red) 10–12. A creative grouping, not strict alchemical history.
- ✅ Cleared rooms and floors stay **replayable** for farming (3★ sweep, GDD §6.12). No stamina (GDD §13 #22).
- ✅ **No walking: a stage map** (like Cookie Run: Kingdom's adventure map). Two levels:
  - **Tower view:** the Athanor drawn vertically, floors stacked upward; each floor band shows its Gate name, act color, stars, and a lock with its Gate Seal requirements. Tap a floor to enter.
  - **Floor view:** the floor's environment as background, **~10 dots joined by a path**, ending at the **boss room**; stars (0–3) under each dot; tap a dot to see its waves, the party and **Start**. The boss dot shows an **empty altar** until the summon condition is met. The floor modifier is shown as an icon in the corner.
  - ✅ **Main path plus optional side dots:** the main path is not the only route; side branches hold optional content: a **journal page** (story, riddle hints), an **elite** fight (better drop table), a **treasure** dot (one-time Coins or a Rare). Players who only climb can ignore them.
- ⏸ **Banked: a labyrinth** floor or section (which floor and details TBD).
- **Content cost:** zones share a tileset; floors vary through modifiers; milestone floors and boss rooms get hand-made story and riddles.

## 3. Unlocking floors: the boss room
- ✅ **Always:** beat the previous floor's boss to reach the next floor.
- ✅ **The boss appears only when the floor's summon condition is met.** Until then the boss room is empty, the battle can't start, and the next floor stays closed. **Condition types stay open:** new riddle types can be added anytime; a floor holds a list of conditions.
- ✅ **Condition type 1: the altar.** The boss room holds an **altar** (the Athanor's furnace). The player **recreates the failed reaction** that made the boss by combining cards (2 for now; more later). Same as normal fusion (GDD §4.1): a wrong combination does nothing and **no cards are lost**. The recipe can be **property-based** (e.g. "a Sulfur-dominant homunculus + a Fire material"), so several answers can work. The floor's journal pages hint at it.
  - ✅ Cards are **consumed on the first summon only**; after that the altar remembers, so replays and farming are free.
  - Boss summons get their own Codex section, separate from card recipes.
- ✅ **Gate Seals** (other condition types), approved examples: a **Codex milestone** (e.g. 10 recipes discovered); **bring a homunculus** with a given dominant principle (e.g. Sulfur); **earn N★** on the floors below. More will be added when ideas come.
- ✅ Requirements are **shown from the start** so players can plan.

## 4. Rewards
- ✅ **Targeted drops are the farming mechanic.** Each floor (and each Runoff, §5) has its own drop table, so players farm where the ingredients they need drop.
- ✅ Higher floors: **more basics** and **better Rare odds**.
- ✅ **Higher-tier cards already in the player's Codex** can drop, at a **lower rate**. Saves fusion cost; never skips a discovery.
- ✅ **First clear of each floor:** an **exceptional** reward plus status.
- ✅ **Leaderboard per floor:** stars first, then **clear time** as tiebreaker. Each **season** (4–6 weeks, in step with the basic-card rotation, GDD §4.2.2), the **top 3** of each floor get an exceptional reward.
- ✅ **Exceptional** = the one deliberate rule bend: it **can be a card the player hasn't discovered yet**, at a low chance. It arrives as **"seen, recipe unknown"** in the Codex: owning the card doesn't reveal its recipe, so fusing it is still a discovery.
- Coins, journal pages (Codex), recipe hints (GDD §4.1) and titles / frames: rewards to use around these (amounts TBD).

## 5. Runoffs
- ✅ **Every Runoff has a "recipe":** the 2 reagents that failed to react (e.g. *Ash Slime = Goblin – Rogue + Rust*).
- ✅ **Its drops are its reagents** (targeted farming); the Codex shows a Runoff's reagents once it's defeated.
- ✅ **Its look and kit come from its reagents** (an Orc inside makes it bulky; Fire Oil makes it burn).
- ✅ **Its stats use the homunculus model** (GDD §6.9: principles, a role, derived stats), scaled by **size**: small, elite, boss, with **0–1 / 1–2 / 2–3 passives** (GDD §6.6).
- ✅ **Runoffs have no gear**; gear effects hit their body (GDD §6.6).
- ✅ A floor boss is a famous failed reaction: its reagents connect to the altar recipe (when that condition is used).

## 6. Season 1: the Twelve Gates
Source: George Ripley, *The Compound of Alchemy* (1471), public domain; Ripley's original order. Each Gate is one floor with one **modifier** that affects **both sides**. Numbers are placeholders for playtesting.

| Floor | Act | Gate (process) | Environment | Modifier |
|---|---|---|---|---|
| 1 | Nigredo | **Calcination** (burning to ash) | Extreme heat | Every 8 s, every unit gets a short **Burn** |
| 2 | Nigredo | **Solution** (dissolving) | Flooded | The 2 middle rows are water: **Slow** while crossing |
| 3 | Nigredo | **Separation** | Cracked floor | Lanes walled off: units **can't change lane** (dashes and blinks still can) |
| 4 | Albedo | **Conjunction** (joining) | Chained pairs | Units in the same lane **share 20% of damage** taken |
| 5 | Albedo | **Putrefaction** (rot) | Swamp of decay | **Healing −30%**; poison puddles appear (zones, GDD §6.13) |
| 6 | Albedo | **Congelation** (freezing) | Extreme cold | **Move Speed −20%**; Freeze lasts longer |
| 7 | Citrinitas | **Cibation** (feeding) | A hungry floor | Runoffs **grow +5% stats every 10 s** |
| 8 | Citrinitas | **Sublimation** (rising vapor) | Wind, floating ground | **Knockback +1 tile**; some tiles vanish and come back |
| 9 | Citrinitas | **Fermentation** | Bubbling vats | **All statuses last 50% longer** |
| 10 | Rubedo | **Exaltation** | Blinding light | **All damage +20%** |
| 11 | Rubedo | **Multiplication** | Mirrors | Small Runoffs **split into 2** weaker copies when killed |
| 12 | Rubedo | **Projection** (final transmutation) | Everything at once | The modifier **rotates through earlier Gates every 15 s** |

- ✅ **Wards** (an ancient Alchemist's traps: pre-placed traps and zones, GDD §6.2, §6.13) are a **separate modifier** any floor can carry on top of its Gate (e.g. floor 3 = Separation + Wards).

## 7. Expansion: the Athanor grows
- ✅ Each season adds floors from **another public-domain alchemical text**. Floor numbers continue (13, 14…).
- Candidate sources:

| Source | Year | Floors | Flavor |
|---|---|---|---|
| Twelve Gates (Ripley) | 1471 | 12 | Processes (Season 1) |
| Seven planetary metals | classical | 7 | Lead / Saturn → Gold / Sun |
| Paracelsus's elementals | 1500s | 4 | Gnomes, undines, sylphs, salamanders |
| Twelve Keys of Basil Valentine | 1599 | 12 | Symbolic keys: riddle floors |
| Mutus Liber ("the Silent Book") | 1677 | 15 | Pictures, no words: riddles |
| Splendor Solis | 1582 | 22 | Illustrated plates: art direction |
| Atalanta Fugiens (Maier) | 1617 | 50 | Emblems with music: long endgame climb |

- ✅ **Data, not code:** each floor is one data asset (number, source text, environment modifier, Runoff waves, drop table, journal page, summon conditions). Nothing depends on "12".
- **Risk:** content added only on top reaches veterans only. Later option: **side wings** that open at mid floors.

## 8. Banked
- **Mining** (GDD §7): banked until a good mechanic appears. Discussed and not chosen: an idle expedition (like Cookie Run: Kingdom's Hot Air Balloon) from "landings" every 10 floors, sending spare homunculi. Targeted drops cover farming for now.

## 9. Open
- More summon condition types and Gate Seals (user-led).
- Per-floor story, journal pages, riddles; boss list; Runoff roster per floor.
- Reward amounts; exceptional reward chances; leaderboard details (ties on time).
- Side wings; what's at the top.
- The labyrinth (banked, §2).
