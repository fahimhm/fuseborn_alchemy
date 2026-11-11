# Ronan · Human – Commander

> Rules: GDD §4.6 (hero), §6 (combat), §6.9 (formulas). Lore: [Lore.md](../Lore.md). Big brother: [Tobin](HumanKnight.md).

**Status:** Draft (for review)

## 1. Identity
| Field | Value |
|---|---|
| Character name | **Ronan** |
| Data ID | `SO_Hero_HumanCommander` |
| Race (family) | Human |
| Class | Commander |
| Initial role | Support |
| Branch roles | B1 Vanguard Ironclad: **Tank** (off-role) · B2 Imperial Strategist: **Support** · B3 Executioner Warlord: **Warrior** (off-role) |
| Tier | II (recipe depth only, not power) |
| Recipe(s) | Human – Knight + Human – Knight (Tobin + Tobin) |
| Soul | Yes: the soul of a **young wolf**, a pack animal that leads and protects its family (Lore.md) |
| Codex flavor | "Never lost a game. Never left a brother behind." |

## 2. Backstory
**Personality keywords:** brilliant, brave, loyal, confident.

Ronan woke up where two Tobins used to stand, and the first thing he did was find the third Tobin and stand beside him. Nobody told him they were brothers; he simply knew. He is quicker than Tobin and braver too, yet he insists Tobin taught him everything (Tobin has no idea what). In the guild hall he has never lost a game of chess or go: apprentices line up to beat him and leave with a lesson instead. His soul came from a young wolf, a pack animal that watches over its family and moves as one with it. The Alchemist saw it at once and gave him what he wanted most: **command**. Ronan doesn't fight to obey. He fights so that nobody he leads, and least of all his big brother, gets left behind.

**Control:** the Alchemist controls Ronan through **trust and responsibility** (Lore.md): he is given command, and he refuses to let the guild or Tobin down.

## 3. Combat Profile
| Field | Value |
|---|---|
| Dominant principle | Salt |
| Attack type | Melee |
| Damage type | Physical |
| Attack range | Melee (1 tile) |
| Base attack interval | 1.5 s |
| Move Speed | 310 |
| Targeting | Same lane → Front-most |
| Recommended row | Front or Middle |

## 4. Stats
| | Base (Lv. 1) | Growth / level |
|---|---|---|
| Salt | 20 | 2.1 |
| Mercury | 16 | 1.8 |
| Sulfur | 14 | 1.6 |

Budget: base 50 (46–54 ✔), growth 5.5 (5.0–6.0 ✔). Salt has the highest growth; the spread is **flat** because his branches cover three roles (GDD §4.6.2).

| Other base values | Value |
|---|---|
| Base HP | 180 |
| Base attack damage | 24 |
| Base DEF / RES | 3 / 2 |
| DEF growth / level | 0.15 |
| Base mana | 90 |

**Derived** (GDD §6.9 rates incl. Resonance, no gear):
| Stat | Lv. 1 | Lv. 30 |
|---|---|---|
| HP / HP regen | 620 / 2.2 per s | 1,960 / 8.9 per s |
| Mana / mana regen | 258 / 0.70 per s | 815 / 3.02 per s |
| Attack damage | 44 | 105 |
| DEF (reduction) | 5.4 (24%) | 17.6 (51%) |
| RES (reduction) | 4.1 (20%) | 11.1 (40%) |
| Attacks per second | 0.77 | 1.12 |

## 5. Skill Tree
Skill points: 1 per hero level, spent on any open skill. Every skill has 5 levels; a skill's level can't exceed hero level ÷ 2, rounded up. Core skills are all open from Lv. 1; the branch opens at **hero Lv. 10** with all 3 of its skills open (GDD §4.6.4). Core + one branch = 6 × 5 = 30 points, all spent at Lv. 30.

**Core**
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| A1 | **Tactical Rally** | Lv. 1 | 80 / 16 s | Allies within 2 tiles (him included) | A crisp battle command: +6 / 9 / 12 / 15 / 18 Attack Speed and +2 / 3 / 4 / 5 / 6 DEF for 5 s |
| A2 | **Breakthrough Strike** | Lv. 1 | 70 / 12 s | Current target | 70 / 110 / 150 / 190 / 230 physical damage; **Stun** 1 / 1.1 / 1.25 / 1.4 / 1.5 s; **Knockback** 1 tile |
| P0 | **Lead by Example** (core passive) | Lv. 1 | — | Allies within 1 tile | Each of his basic hits gives them +2 / 2.5 / 3 / 3.5 / 4 mana |

**Branch point:** hero Lv. 10. **3 branches**, permanent choice: three ways to lead. B2 keeps him a Support; B1 makes him a **Tank** and B3 a **Warrior** (off-role: weaker versions of those roles' core tools than specialists like Tobin, GDD §6.3).

**B1 · Vanguard Ironclad** (role: **Tank**, off-role) — he holds the line himself.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B1a | **Phalanx Wall** | Branch (Lv. 10) | 120 / 24 s | Self + adjacent allies | Locks his shield into the ground for 4 s: can't move, **immune to control**, takes −30 / 35 / 40 / 45 / 50% damage, and takes 10 / 15 / 20 / 25 / 30% of the damage dealt to allies within 1 tile in their place |
| B1b | **Unyielding Taunt** | Branch (Lv. 10) | 90 / 20 s | Enemies within 2 tiles | Slams sword on shield: **Taunt** 1.5 / 1.75 / 2 / 2.25 / 2.5 s; gains a **Shield** worth 10 / 12.5 / 15 / 17.5 / 20% of his max HP |
| B1p | **Veteran's Will** | Branch (Lv. 10) | — | Self | Once per battle, when he drops below 30% HP: cleanses all harmful statuses; DEF and RES ×1.2 / 1.25 / 1.3 / 1.35 / 1.4 for the rest of the battle |

**B2 · Imperial Strategist** (role: **Support**) — high tactics: the board is his chessboard.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B2a | **Tactical Swap** | Branch (Lv. 10) | 90 / 22 s | Two allies | Swaps the positions of the ally with the highest ATK and the ally with the lowest HP %; both get +30 / 35 / 40 / 45 / 50 Move Speed and a **magic-only Shield** worth 6 / 8 / 10 / 12 / 14% of their max HP for 3 s |
| B2b | **Pincer Command** | Branch (Lv. 10) | 100 / 20 s | One enemy | Marks it as the objective for 5 s: allies' hits **ignore 10 / 12.5 / 15 / 17.5 / 20% of its DEF**; it takes +8 / 10 / 12 / 14 / 16% damage from all sources |
| B2p | **Supply Logistics** | Branch (Lv. 10) | — | Lowest-mana ally | Every 6 s: +20 / 25 / 30 / 35 / 40 mana and removes **Silence** and **Disarm** |

**B3 · Executioner Warlord** (role: **Warrior**, off-role) — turns the fight into momentum.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B3a | **Execute Cleave** | Branch (Lv. 10) | 100 / 14 s | Enemies within 1 tile | A sweeping strike: 90 / 130 / 170 / 210 / 250 physical damage, **×2 to targets below 30% HP**. A kill resets the cooldown (at most once every 10 s) |
| B3b | **Warlord's Roar** | Branch (Lv. 10) | 90 / 22 s | Allies within 2 tiles | +7 / 9 / 11 / 13 / 15% Crit and +6 / 7 / 8 / 9 / 10% Lifesteal for 4 s |
| B3p | **Momentum Surge** | Branch (Lv. 10) | — | Self | Each enemy death anywhere: +1.5 / 2 / 2.25 / 2.5 / 3% ATK and +2 / 2.5 / 3 / 3.5 / 4 Move Speed for the rest of the battle, **up to 10 stacks**. Summons give half a stack; Draupnir's illusions don't count |

**Gear skill fit:** Support, Guard, Physical.

## 6. Equipment
| Slot | Allowed |
|---|---|
| Weapon | Sword, Shield (a Shield-family weapon replaces his built-in shield, as with Tobin) |
| Armor | Any piece |
| Accessory | Any |
| Default weapon | A polished arming sword, with his built-in shield |

## 7. Trait
- Chance: 30% when born; if it rolls: Faint 65% · Bright 27% · Radiant 8% · Unique (GDD §4.6.4).
- Built-in shield: **yes** (a smaller, polished version of Tobin's pot lid): he can Block and can roll Block traits.
- Fitting trait tags: Support, Guard, Physical.

## 8. Illustrator Brief
| Field | Value |
|---|---|
| Silhouette & key shapes | Upright and confident, a little shorter than Tobin; short cape; a small, round, **polished shield** that echoes Tobin's pot lid (a wolf head embossed on it) |
| Palette (3–4 colors) | Navy blue, polished silver, wolf grey, a gold trim |
| Race family base body | Shared rig/body with: Human (Tobin) |
| Weapon held | A clean arming sword in the main hand; the polished round shield on the off arm |
| Card illustration | Leaning over a chess board in the guild hall, moving a knight piece with a small smile; Tobin peeking over his shoulder, confused but proud |
| Battle views | **Front ¾** (as an enemy / PvP) and **back ¾** (own party) |
| Animations | Idle (scans the battlefield, adjusts his cape), run (shield up, sword low), basic sword slash, Tactical Rally (points sword forward, shouting), Breakthrough Strike (shield-led charge into a slash), hit, KO (drops to one knee, reaching toward allies), victory (salutes, then nudges Tobin). Branches: B1 plants the shield and slams it; B2 points across the board and swaps allies; B3 wide cleave and a wolf-like roar |
| Branch props | B1 heavier pauldrons and a dented shield rim; B2 a command baton at his belt and a map case on his back; B3 a wolf-pelt cloak and red war paint |
| VFX per skill | Tactical Rally: golden command ring spreading 2 tiles; Breakthrough Strike: dust burst, stun stars, a push-back streak; Lead by Example: tiny blue mana sparks jumping to adjacent allies; Phalanx Wall: shield-shaped barrier and ground cracks; Unyielding Taunt: red shout ring + shield shimmer; Tactical Swap: two chess-piece-shaped flashes trading places; Pincer Command: a target sigil over the enemy; Supply Logistics: a small floating supply crate dropping on an ally; Execute Cleave: wide red arc; Warlord's Roar: a wolf-shaped sound wave; Momentum Surge: a growing red aura per stack |
| SFX / voice notes | Crisp, short commands ("Hold!", "Now!"); a shield clang; a wolf howl on Warlord's Roar |
| References | Classic young-commander archetype, chess motifs, wolf-pack symbolism |
| Avoid | Anything that looks like an existing game's character |
