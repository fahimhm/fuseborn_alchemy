# Maeve · Fairy – Enchanter

> Rules: GDD §4.6 (hero), §6 (combat), §6.9 (formulas). Lore: [Lore.md](../Lore.md). Made from [Tobin](HumanKnight.md) + [Elsie](AngelPriest.md).

**Status:** Draft (for review)

## 1. Identity
| Field | Value |
|---|---|
| Character name | **Maeve** |
| Data ID | `SO_Hero_FairyEnchanter` |
| Race (family) | Fairy |
| Class | Enchanter (was Druid: "Fairy – Druid" said "nature" twice and clashed with Dryad – Shaman) |
| Initial role | Support |
| Branch roles | B1 Relic Sculptor: **Support** · B2 Spiteful Tarnisher: **Mage** (off-role) |
| Tier | II (recipe depth only, not power) |
| Recipe(s) | Human – Knight + Angel – Priest (Tobin + Elsie) |
| Soul | Yes: drawn from nature (the default, Lore.md); a little European folklore came with it |
| Codex flavor | "Loves your sword. Can't stand you." |

## 2. Backstory
**Personality keywords:** fast, vain, spiteful, possessive.

When the Alchemist tried a new combination, a small fairy popped out. She flew fast, faster than a fly, zipping all around the guild while the Alchemist ran after her. She stopped dead when she saw Tobin's and Ronan's shields, armor and accessories: "Oh, shiny!" That was enough. The Alchemist caught her and put her in a glass jar. Maeve hates mortals, but she loves shiny things. She hates it when shiny things get dirty, stained with blood when the wearer dies, and her hatred boils over when enemies wear things shinier than the guild's own. So she never buffs mortals. She enchants their items, gear and weapons instead.

**Control:** **captivity** (Lore.md). The Alchemist keeps her jar and lets her out only to fight. She stays anyway: the guild holds the shiniest hoard she has ever seen, and she can't stand the thought of it getting dirty without her.

## 3. Combat Profile
| Field | Value |
|---|---|
| Dominant principle | Mercury ("faster than a fly") |
| Attack type | Ranged |
| Damage type | Magic (fae-dust) |
| Attack range | Medium (5 tiles) |
| Base attack interval | 1.6 s |
| Move Speed | 340 (fastest so far) |
| Targeting | **Richest** (GDD §6.4) → Front-most |
| Recommended row | Back |

## 4. Stats
| | Base (Lv. 1) | Growth / level |
|---|---|---|
| Salt | 12 | 1.3 |
| Mercury | 22 | 2.5 |
| Sulfur | 16 | 1.8 |

Budget: base 50 (46–54 ✔), growth 5.6 (5.0–6.0 ✔). Mercury has the highest growth; the spread is moderately flat for two roles (GDD §4.6.2). She doesn't need Sulfur for mana: "Ooh, Shiny!" gives her up to +50% mana regen.

| Other base values | Value |
|---|---|
| Base HP | 150 |
| Base attack damage | 18 |
| Base DEF / RES | 0 / 3 |
| Base mana | 90 |

**Derived** (GDD §6.9 rates incl. Resonance, no gear):
| Stat | Lv. 1 | Lv. 30 |
|---|---|---|
| HP / HP regen | 390 / 1.2 per s | 1,144 / 5.0 per s |
| Mana / mana regen | 282 / 0.80 per s | 908 / 3.41 per s (before "Ooh, Shiny!") |
| Attack damage | 40 | 113 |
| DEF (reduction) | 3.6 (18%) | 15.6 (48%) |
| RES (reduction) | 5.4 (25%) | 13.2 (44%) |
| Attacks per second | 0.78 | 1.27 |

## 5. Skill Tree
Skill points: 1 per hero level, spent on any open skill. Every skill has 5 levels; a skill's level can't exceed hero level ÷ 2, rounded up. Core skills are all open from Lv. 1; the branch opens at **hero Lv. 10** with all 3 of its skills open (GDD §4.6.4). Core + one branch = 6 × 5 = 30 points, all spent at Lv. 30. Statuses: GDD §6.10.

**Her rules (all skills):**
- **She ignores units with 0 items.** Her skills and passives never affect a unit, ally or enemy, that has no gear card or accessory. The **default weapon** (visual only) doesn't count. Her **basic attacks** still hit gearless enemies (Richest → Front-most), grudgingly, so she is never idle.
- **Runoffs (PvE):** they have no gear (GDD §6.6), so their **passives count as their items**; their strongest passive is their "highest-band item". Small Runoffs with no passive are ignored: her PvE counter.
- **Shine:** each item gives shine by band: Starter / Early **1**, Mid **2**, Late **3**, Peak **4** (max 12 per unit). Locked, stolen or tarnished items stop shining.
- **Tie-breaks** when she picks an item or unit: higher band, then higher GP, then lowest HP %.
- **Item stats ×N** means the card's base stats and extras count ×N; its signature or gear-skill numbers don't change unless the skill says so.

**Core** — the jeweller's touch.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| A1 | **Gilded Polish** | Lv. 1 | 80 / 16 s | The allied item with the highest band | Item stats ×1.1 / 1.15 / 1.2 / 1.25 / 1.3 for 5 s; the item flashes: **Blind** 1 s on enemies within 1 tile of the wearer |
| A2 | **Tarnish Touch** | Lv. 1 | 70 / 14 s | The enemy holding the highest-band item within her range | **Tarnishes** that item (not the Curse status) for 2 / 2.5 / 3 / 3.5 / 4 s: its signature or gear skill is switched off (PvE: the Runoff's passive), and the wearer makes −25% attacks per second |
| P0 | **"Ooh, Shiny!"** (core passive) | Lv. 1 | — | Self | +1% mana regen per shine on her side (her own items included), cap +30 / 35 / 40 / 45 / 50%. Updates live |

**Branch point:** hero Lv. 10. **2 branches**, permanent choice: polish the guild's treasures, or punish the enemy's. B1 keeps her a Support; B2 makes her a **Mage** (off-role: damage below Mage specialists, GDD §6.3).

**B1 · Relic Sculptor** (role: Support) — turns the team's weapons and robes into hyper-charged artifacts, still ignoring the mortals holding them.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B1a | **Masterwork Ascension** | Branch (Lv. 10) | 120 / 24 s | The ally with the most shine | **All** its item stats ×1.3 / 1.35 / 1.4 / 1.45 / 1.5 for 6 s; **Peak** items also get that factor on their signature or gear-skill numbers. Stacks with Gilded Polish (up to ×1.95 on one item). Level requirements are ignored (the item is boosted, not changed) |
| B1b | **Puppeteer's String** | Branch (Lv. 10) | 100 / 22 s | The ally with a weapon card and the highest ATK (tie: higher weapon band) | Fae-threads on its weapon for 3 / 3.5 / 4 / 4.5 / 5 s: +20 / 25 / 30 / 35 / 40 Attack Speed and **+50% Accuracy**. ⚠ **Logged exception to §6.10:** the weapon keeps making basic hits on the current target (if in range) while the wearer is **Stunned, Asleep or Frozen**; the wearer still can't move or cast. **Disarm** stops it (it targets the weapon); **Taunt** and **Confuse** still apply. An ally with only the default weapon can't be chosen |
| B1p | **Hoarder's Pride** | Branch (Lv. 10) | — | Allies holding 3 items | A fae-shell around their gear blocks the **first** theft or disable on their items (Silas's Lockout and Vault Heist, Tarnish Touch, Searing Metal…), then breaks; it returns after 20 / 18 / 16 / 14 / 12 s, per ally. Also +8 / 11 / 14 / 17 / 20% shields received. The shell is part of the passive, not a status: it can't be stripped or stolen |

**B2 · Spiteful Tarnisher** (role: **Mage**, off-role) — punishes enemies for daring to carry shiny things, turning their own gear into hazards.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B2a | **Searing Metal** | Branch (Lv. 10) | 110 / 20 s | The enemy with the most shine within her range | Superheats its gear for 5 s: **true damage** (GDD §6.9) every second, 6 / 9 / 12 / 15 / 18 **+ 1 / 1.5 / 2 / 2.5 / 3 per shine**; can't be Blocked (she enchants it from a distance). Its gear bonuses drop by 20 / 27.5 / 35 / 42.5 / 50% (HP and mana excluded). Lv. 5: 270 total on a full-Peak target, 180 on Mid gear |
| B2b | **Shatter Charm** | Branch (Lv. 10) | 120 / 22 s | The enemy with the highest ATK holding at least 1 item; everyone within 1 tile of it | A discordant fae-shriek overloads its **highest-band item**: 50 / 75 / 100 / 125 / 150 **magic** damage × band (Starter-Early 1 / Mid 1.25 / Late 1.5 / Peak 1.75) to the wearer and every enemy within 1 tile; the wearer is **Stunned** 1 / 1.1 / 1.25 / 1.4 / 1.5 s and the item is disabled for the same time. The item is not destroyed |
| B2p | **Envy's Toll** | Branch (Lv. 10) | — | Enemies within her range | When an enemy triggers a **signature or gear skill** (an on-hit proc, a shield trigger, a gear-skill cast; PvE: a Runoff passive), she blasts it with fae-fire: 3 / 3.75 / 4.5 / 5.25 / 6% of its max HP as **magic damage with the Fire tag** (ignites Oiled). Plain stats (Lifesteal, Crit, Evasion) don't trigger it. 6 s cooldown per enemy |

**Vs. Silas:** Silas **steals** gear; Maeve **enhances or spoils** it, and nobody gains from her spoiling. Hoarder's Pride is the answer to Silas, and Silas has to break it first.

**Gear skill fit:** Magic, Speed, Support.

## 6. Equipment
| Slot | Allowed |
|---|---|
| Weapon | Staff, Tome |
| Armor | Any piece |
| Accessory | Any (she adores them) |
| Default weapon | A sewing needle she uses as a wand (visual only) |

## 7. Trait
- Chance: 30% when born; if it rolls: Faint 65% · Bright 27% · Radiant 8% · Unique (GDD §4.6.4).
- Built-in shield: no.
- Fitting trait tags: Magic, Speed, Support ([TraitPool.md](../TraitPool.md)).

## 8. Illustrator Brief
| Field | Value |
|---|---|
| Silhouette & key shapes | Tiny (about a hand tall), quick, with sharp dragonfly-like wings; always trailing glitter; often shown next to (or inside) her **glass jar** |
| Palette (3–4 colors) | Silver and gold glints, pale lilac wings, polished-gem accents (sapphire, ruby); her own dress is plain, because all the shine goes on things |
| Race family base body | New: Fairy (small flying rig) |
| Weapon held | A sewing needle used as a wand (default); a Staff or Tome replaces it, comically big for her |
| Card illustration | Hugging Tobin's pot lid and polishing it with her sleeve, while ignoring Tobin entirely; the open jar behind her |
| Battle views | **Front ¾** (as an enemy / PvP) and **back ¾** (own party) |
| Animations | Idle (darting around, inspecting shiny things), fly, basic fae-dust flick, Gilded Polish (blows dust onto an item, which flashes), Tarnish Touch (flicks a grimy smudge at an enemy item), hit, KO (falls into her jar, which corks itself), victory (perches on the shiniest ally's weapon, not the ally). Branches: B1 conducting threads like a puppeteer; B2 a shriek with spiteful face, hands over her ears |
| Branch props | B1 a jeweller's loupe over one eye and a spool of glowing thread; B2 a blackened little crown of bent rings and soot on her wings |
| VFX per skill | Gilded Polish: gold beam, item gleam, white flash; Tarnish Touch: green-grey grime creeping over the item; "Ooh, Shiny!": sparkles drifting from allied items to her; Masterwork Ascension: the items glow and gain a gilded outline; Puppeteer's String: shining threads from her fingers to the weapon; Hoarder's Pride: a thin glass-like shell over gear, shattering when it blocks; Searing Metal: red-hot metal glow and heat haze; Shatter Charm: a sound-wave shriek, then the item bursts in shards (then reforms); Envy's Toll: a small burst of violet fae-fire |
| SFX / voice notes | Wing buzz, tiny bell-like chimes; "Oh, shiny!", "Don't touch it with your dirty hands." |
| References | European folklore fairies (small, capricious, love of treasure) |
| Avoid | Anything that looks like an existing game's or film's fairy; nature / leaf motifs (Dryad – Shaman's) |
