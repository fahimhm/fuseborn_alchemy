# Silas · Human – Thief

> Rules: GDD §4.6 (hero), §6 (combat), §6.9 (formulas). Lore: [Lore.md](../Lore.md). Made from [Tobin](HumanKnight.md) + [Wren](ElfArcher.md).

**Status:** Draft (for review)

## 1. Identity
| Field | Value |
|---|---|
| Character name | **Silas** |
| Data ID | `SO_Hero_HumanThief` |
| Race (family) | Human |
| Class | Thief |
| Initial role | Assassin |
| Branch roles | B1 Relic Highwayman: **Assassin** · B2 Spell Plunderer: **Support** (off-role) · B3 Shadow Mimic: **Mage** (off-role) |
| Tier | II (recipe depth only, not power) |
| Recipe(s) | Human – Knight + Elf – Archer (Tobin + Wren) |
| Soul | Yes: drawn from nature (the default, Lore.md); no particular animal |
| Codex flavor | "Left with nothing. Took everything." |

## 2. Backstory
**Personality keywords:** patient, sly, hungry, quietly proud.

The Alchemist thought Silas was a failure. He was born with a weak body, so weak that one of Tobin's slaps could knock him out: thin, and without a single hair anywhere. So Silas was ignored. No water, no food. But after a few days he made the Alchemist realize he shouldn't have been abandoned. First a little food went missing, then a big portion, then a minor potion, then a greater potion, then something bigger. The Alchemist finally understood: Silas has huge potential. He can steal anything, anywhere, anytime.

**Control:** a **trade** (Lore.md). Silas brings the Alchemist good loot, and every time he does, the Alchemist pays him with **good food**, the thing he wants most. A weak body never forgets hunger.

## 3. Combat Profile
| Field | Value |
|---|---|
| Dominant principle | Sulfur |
| Attack type | Melee |
| Damage type | Physical |
| Attack range | Melee (1 tile) |
| Base attack interval | 1.4 s |
| Move Speed | 320 |
| Targeting | **Richest** (GDD §6.4) → Lowest HP |
| Recommended row | Middle |

## 4. Stats
| | Base (Lv. 1) | Growth / level |
|---|---|---|
| Salt | 12 | 1.4 |
| Mercury | 18 | 2.0 |
| Sulfur | 20 | 2.2 |

Budget: base 50 (46–54 ✔), growth 5.6 (5.0–6.0 ✔). Sulfur has the highest growth; the spread is fairly flat because his branches cover three roles (GDD §4.6.2). Salt is the lowest in the roster so far: the weakest body.

| Other base values | Value |
|---|---|
| Base HP | 140 (lowest so far) |
| Base attack damage | 22 |
| Base DEF / RES | 0 / 2 |
| Base mana | 80 |

**Derived** (GDD §6.9 rates incl. Resonance, no gear):
| Stat | Lv. 1 | Lv. 30 |
|---|---|---|
| HP / HP regen | 380 / 1.2 per s | 1,192 / 5.3 per s |
| Mana / mana regen | 344 / 1.10 per s | 1,186 / 4.61 per s |
| Attack damage | 42 | 106 |
| DEF (reduction) | 2.7 (14%) | 11.4 (41%) |
| RES (reduction) | 5.3 (24%) | 15.8 (49%) |
| Attacks per second | 0.84 | 1.26 |

**Shape:** fragile against physical damage, tough against magic. Warriors and Rangers are his natural counter; the casters he robs struggle to kill him.

## 5. Skill Tree
Skill points: 1 per hero level, spent on any open skill. Every skill has 5 levels; a skill's level can't exceed hero level ÷ 2, rounded up. Core skills are all open from Lv. 1; the branch opens at **hero Lv. 10** with all 3 of its skills open (GDD §4.6.4). Core + one branch = 6 × 5 = 30 points, all spent at Lv. 30. Statuses: GDD §6.10.

**Stealing rules (all skills):**
- **Silas steals; he never just copies.** What he takes, the target loses for the same time.
- **No exclusions.** Anything can be stolen, including revives and Invulnerable; this is how he counters builds that rely on one effect.
- **Random and no refund.** Where a skill picks at random, it only picks among things that can be stolen. If there is nothing to steal, the skill does nothing (no refund): a target with no gear (PvP) or no passives (PvE) is his counter.
- **Runoffs** have no gear: anything that targets gear targets the Runoff's own body instead (GDD §6.6).
- **Copied skills** (Mirror Hijack, Echo Blade) cost no mana, keep their original damage type, use the **target's skill level** and **Silas's own stats**, and flip sides (damage hits his enemies, heals and buffs go to his allies). A stolen summon counts toward his max of 2 (GDD §6.11).
- **A stolen once-per-battle effect** (a revive, "survive a fatal hit") is used up if it triggers while Silas holds it; the owner loses it for the rest of the battle.

**Core** — a thief's hands: take a bit of everything.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| A1 | **Cutpurse Siphon** | Lv. 1 | 60 / 12 s | Current target | 30 / 45 / 60 / 75 / 90 physical damage; steals 7 / 9 / 11 / 13 / 15% of its **ATK and DEF** (flat amounts) for 6 s |
| A2 | **Arcane Plunder** | Lv. 1 | 50 / 14 s | Current target | Steals **1 random buff** (helpful status, incl. Invulnerable). Silas keeps it for its remaining time, max 3 / 3.75 / 4.5 / 5.25 / 6 s |
| P0 | **Pocket Theft** (core passive) | Lv. 1 | — | Self | Basic hits steal 2 / 3 / 4 / 5 / 6 mana. When a hit brings **the target** to 0 mana: +8 / 11 / 14 / 17 / 20 Attack Speed for 3 s (never triggers on targets with no mana) |

**Branch point:** hero Lv. 10. **3 branches**, permanent choice: three things to steal. B1 keeps him an Assassin; B2 makes him a **Support** and B3 a **Mage** (off-role: weaker versions of those roles' core tools than specialists, GDD §6.3).

**B1 · Relic Highwayman** (role: Assassin) — goes straight for the richest enemy and robs its gear. The gamble: both steals pick a card at random.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B1a | **Locksmith's Lockout** | Branch (Lv. 10) | 90 / 18 s | Richest enemy, anywhere | **Picks the lock:** a visible dash to a tile next to the Richest enemy (the Assassin's reach, no stealth), 60 / 95 / 130 / 165 / 200 physical damage, then **locks one random equipped gear card** for 4 / 4.5 / 5 / 5.5 / 6 s: the target loses that card's **base stats** (Salt / Mercury / Sulfur, ATK, HP, DEF, RES, mana, Attack Speed, Move Speed) and Silas gains them. Not the Disarm status: the target can still attack. **PvE:** takes 15% of the Runoff's base stats, capped at what one Late gear card gives (16 GP) |
| B1b | **Vault Heist** | Branch (Lv. 10) | 80 / 18 s | Current target | Steals **everything except base stats** from one random gear card for 5 / 5.75 / 6.5 / 7.25 / 8 s: Crit, Evasion, Block, Lifesteal, Thorns, CDR, Skill Power, Control Resist, Holy / Dark %, and its signature or gear skill (e.g. a DoT on hit). Only cards with something to steal can be picked. Stolen Block does nothing on Silas (not a shield bearer, GDD §6.9), but the target still loses it. **PvE:** steals one random Runoff passive |
| B1p | **Scavenger's Greed** | Branch (Lv. 10) | — | Self | Per item on his **current target** (gear cards in PvP, passives in PvE; max 3): +2 / 4 / 6 / 8 / 10 Attack Speed and +1 / 2 / 3 / 4 / 5% Lifesteal. Updates live; cards and passives he has stolen still count. The default weapon (visual only) doesn't count |

Lockout and Vault Heist roll separately: they may hit the same card or different ones.

**B2 · Spell Plunderer** (role: **Support**, off-role) — robs the enemy and shares the haul.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B2a | **Mass Siphon** | Branch (Lv. 10) | 110 / 20 s | Cone 2 tiles in front; then a zone 2 tiles around the cast spot (GDD §6.13) | Steals 4 / 5.5 / 7 / 8.5 / 10% of **ATK, RES and Attack Speed** (flat) from every enemy hit, for 6 s. The stolen amounts form **one pool, split evenly** between Silas and every ally inside the zone at the moment of the cast (alone, he keeps it all: he is weak and needs everything). The zone stays where it was cast. Anyone who leaves it loses their share, which is **not** passed to the others |
| B2b | **Cleanse and Convert** | Branch (Lv. 10) | 100 / 22 s | Current target; lowest-HP ally within 2 tiles of Silas (him included) | **Strips all buffs** from the target, Invulnerable included. Each of the first 3 becomes a **Shield** worth 4 / 5.5 / 7 / 8.5 / 10% of **the target's** max HP, all given to the lowest-HP ally for 6 s |
| B2p | **Osmosis** | Branch (Lv. 10) | — | Enemies within 3 tiles; lowest-mana-% ally within 3 tiles (him included) | When an enemy casts a skill: steals 2 / 2.75 / 3.5 / 4.25 / 5% of **its** max mana and gives it to the ally with the lowest mana %. Max once per second. Runoffs that never cast are its counter |

**B3 · Shadow Mimic** (role: **Mage**, off-role) — steals the spell itself.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B3a | **Mirror Hijack** | Branch (Lv. 10) | 100 / 20 s | Enemy with the highest **current** mana | Marks it for **4 s**. If it casts an active skill during the mark: its cast is cancelled (its mana and cooldown are still spent), it is **Silenced** 1 / 1.25 / 1.5 / 1.75 / 2 s, and Silas casts the copy (stealing rules above). Any active can be stolen, gear skills included. No cast in 4 s: nothing happens, no refund |
| B3b | **Echo Blade** | Branch (Lv. 10) | 70 / 16 s | Current target | 50 / 80 / 110 / 140 / 170 physical damage and **records the last active skill the target used**. Echo Blade's button turns into that skill for **one use within 8 s**, then reverts and goes on cooldown (unused: it reverts with nothing). If the target hasn't cast yet: just the strike. Stays inside the 3-active loadout (GDD §6.5): no 4th slot |
| B3p | **Master of All Trades** | Branch (Lv. 10) | — | Self | After he casts a **stolen skill** (Mirror Hijack or Echo Blade copy; a buff from Arcane Plunder doesn't count): +6 / 8.25 / 10.5 / 12.75 / 15% Skill Power and +6 / 8.25 / 10.5 / 12.75 / 15% Crit for 6 s, and **his skills can crit** during that time. Doesn't stack: a new trigger refreshes it. Crit cap 60% applies |

Mirror Hijack denies (reactive, silences); Echo Blade lets him choose the moment (no denial).

**Note on async PvP:** the defense AI casts skills when they're ready (GDD §6.7), so Mirror Hijack lands more often there; the short 4 s mark keeps it from being a sure thing. In real-time PvP (GDD §6.14) a human can wait the mark out.

**Gear skill fit:** Physical, Speed, Magic (B3).

## 6. Equipment
| Slot | Allowed |
|---|---|
| Weapon | Dagger, Sword, Knife |
| Armor | Any piece |
| Accessory | Any |
| Default weapon | A bent kitchen knife he stole on his first night (visual only) |

## 7. Trait
- Chance: 30% when born; if it rolls: Faint 65% · Bright 27% · Radiant 8% · Unique (GDD §4.6.4).
- Built-in shield: no.
- Fitting trait tags: Physical, Speed, Magic ([TraitPool.md](../TraitPool.md)).

## 8. Illustrator Brief
| Field | Value |
|---|---|
| Silhouette & key shapes | **A walking pile of loot.** Thin and hairless underneath, but buried in mismatched stolen things, so his outline is a bundle of cloth and trinkets, not a bare thin body |
| Skin | **Fair to light brown** (human). Never green: that is Snick's. This is the main read between the two at card size |
| Stolen items (always on him) | Wren's red guild scarf, a strip of Tobin's faded guild-blue cloth, Grum's donut box worn as a satchel, rings on every finger, a potion bottle tucked behind his ear |
| Palette (3–4 colors) | Warm skin tone, patchwork browns, Wren's red scarf as the accent, glints of stolen gold |
| Race family base body | Shared rig/body with: Human (Tobin, Ronan), thinner build |
| Weapon held | A bent kitchen knife (default); equipped Daggers, Swords or Knives replace it |
| Card illustration | Sitting on a pile of stolen guild treasures, happily eating a fine meal the Alchemist just handed over; Grum in the background looking for his donut box |
| Battle views | **Front ¾** (as an enemy / PvP) and **back ¾** (own party) |
| Animations | Idle (counts his rings, checks his pockets), run (hunched, clutching the satchel), basic knife jab, Cutpurse Siphon (quick snatch at the target's belt), Arcane Plunder (plucks a glowing buff out of the air and pockets it), hit, KO (drops, loot spilling everywhere), victory (stuffs one more thing into the satchel). Branches: B1 dash and picklock twist; B2 cone grab, then tosses the haul to allies; B3 a mirror-flash, then casts the stolen spell with exaggerated imitation |
| Branch props | B1 a ring of lockpicks and a highwayman's mask; B2 an overflowing sack slung across his back; B3 a small cracked hand mirror at his belt |
| VFX per skill | Cutpurse Siphon: red and grey sparks pulled from the target to Silas; Arcane Plunder: a glowing buff icon flying into his pocket; Pocket Theft: tiny blue mana coins; Lockout: dash streak, then a **chain and padlock** on the weapon (or a padlock icon over the target for armor and accessories); Vault Heist: a vault-door flash; Greed: gold glints per item; Mass Siphon: a grabbing cone, then a golden zone ring; Cleanse and Convert: buffs melting into a shield bubble; Osmosis: thin mana threads; Mirror Hijack: a mirror sigil over the target, shattering on cast; Echo Blade: a ghostly copy of the skill's icon on his button; Master of All Trades: a short golden shimmer |
| SFX / voice notes | Jingling pockets, a lock click, a pleased little hum; "Mine now." |
| References | Classic street-thief archetype (patchwork, rings, satchel) |
| Avoid | Anything that looks like an existing game's character; stealth smoke and shadows (Snick's) |
