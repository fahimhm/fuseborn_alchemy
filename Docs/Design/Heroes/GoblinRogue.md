# Snick · Goblin – Rogue

**Status:** Numbers done (approved)

## 1. Identity
| Field | Value |
|---|---|
| Character name | Snick |
| Data ID | `SO_Hero_GoblinRogue` |
| Race (family) | Goblin (Greenskin) |
| Class | Rogue |
| Initial role | Assassin |
| Branch roles | B1 Shadow Assassin: Assassin · B2 Trapmaster: Assassin · B3 Goblin Sapper: **Mage** (off-role) |
| Tier | I |
| Recipe(s) | Basic |
| Basic rarity | Seasonal, hidden (GDD §4.2.2) |
| Soul | Yes: the soul of a forest hare (Lore.md) |
| Codex flavor | "The Alchemist wanted an obedient elf. He got the ears." |

## 2. Backstory
**Personality keywords:** wary, nimble, jumpy, quick-witted.

After Wren, the Alchemist wanted an elf that would obey, so he tried again. The reaction gave him the pointed ears and nothing else: a small, bald, green-skinned thing with thin bones and the soul of a forest hare. The Alchemist called him a failure and set out to fix him: another reaction, another test, another punishment for every flaw. Snick learned to run before he learned to speak. His body was made for it, quick and light, and within weeks nobody in the workshop could catch him. He started carrying a pocket of sand. When he's cornered, the sand goes in their eyes, and he's gone. He still flinches when the workshop door opens. On the battlefield, that flinch is the fastest thing alive.

**Link:** a failed attempt to make an obedient elf after Wren ([ElfArcher.md](ElfArcher.md)). The Alchemist controls him with harsh "fixing" (Lore.md).

## 3. Combat Profile
| Field | Value |
|---|---|
| Dominant principle | Mercury |
| Attack type | Melee |
| Damage type | Physical |
| Attack range | Melee (1 tile) |
| Base attack interval | 1.5 s |
| Move Speed | 330 |
| Targeting | Back-line → Lowest HP |
| Recommended row | Middle |

## 4. Stats
| | Base (Lv. 1) | Growth / level |
|---|---|---|
| Salt | 14 | 1.6 |
| Mercury | 26 | 3.0 |
| Sulfur | 10 | 1.0 |

Budget: base 50 (46–54 ✔), growth 5.6 (5.0–6.0 ✔).

| Other base values | Value |
|---|---|
| Base HP | 170 |
| Base attack damage | 26 |
| Base DEF / RES | 1 / 0 |
| Base mana | 60 |

**Derived** (GDD §6.9 rates incl. Resonance, no gear):
| Stat | Lv. 1 | Lv. 30 |
|---|---|---|
| HP / HP regen | 450 / 1.4 per s | 1,378 / 6.0 per s |
| Mana / mana regen | 180 / 0.50 per s | 528 / 1.95 per s |
| Attack damage | 52 | 139 |
| DEF (reduction) | 5.3 (24%) | 19.6 (54%) |
| RES (reduction) | 1.5 (8%) | 5.8 (26%) |
| Attacks per second | 0.86 | 1.50 |

## 5. Skill Tree
Skill points: 1 per hero level, spent on any open skill. Every skill has 5 levels; a skill's level can't exceed hero level ÷ 2, rounded up. Core skills are all open from Lv. 1; the branch opens at **hero Lv. 10** with all 3 of its skills open (GDD §4.6.4). Core + one branch = 6 × 5 = 30 points, all spent at Lv. 30. Statuses: GDD §6.10.

**Core** — rogue skills: blind and slip away. The dive to the back line comes from the Assassin branch (B1).
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| A1 | **Pocket Sand** | Lv. 1 | 50 / 12 s | Current target | Sand in the eyes: 30 / 45 / 60 / 75 / 90 physical damage + **Blind** 1.5 / 1.75 / 2 / 2.25 / 2.5 s |
| A2 | **Nimble Escape** | Lv. 1 | 40 / 14 s | Self | Instantly breaks all **soft control** on himself (GDD §6.10); +20 / 25 / 30 / 35 / 40% Move Speed for 3 s |
| P0 | **Opportunist** (core passive) | Lv. 1 | — | Self | +4 / 8 / 12 / 16 / 20% damage to enemies that are controlled, Blinded or taking damage over time |

**Branch point:** hero Lv. 10. **3 branches**, permanent choice: B1 Shadow Assassin and B2 Trapmaster keep him an Assassin; B3 Goblin Sapper makes him a Mage (off-role).

**B1 · Shadow Assassin** (role: Assassin) — the dive to the back line: vanish, reappear, strike.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B1a | **Backstab** | Branch (Lv. 10) | 70 / 12 s | Back-line enemy | Lunges behind them: 120 / 190 / 260 / 330 / 400 physical damage; **guaranteed crit if cast from Stealth** |
| B1b | **Shadow Stalker** | Branch (Lv. 10) | 60 / 16 s | Self | Instantly gains **Stealth** for 1.5 / 2 / 2.5 / 3 / 3.5 s, then reappears on a random tile next to an enemy in their back half |
| B1p | **Lethal Precision** | Branch (Lv. 10) | — | Self | +10 / 15 / 20 / 25 / 30% crit damage on hits made from Stealth |

**B2 · Trapmaster** (role: Assassin) — traps set up his own kills (Templar Assassin style): he lays them, then strikes what they catch.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B2a | **Caltrops & Wire** | Branch (Lv. 10) | 80 / 18 s | Zone: a strip across all 3 lanes (placement rule below; GDD §6.13) | Field lasts 6 s: **Slow** 20 / 25 / 30 / 35 / 40%; Bleed 10 / 15 / 20 / 25 / 30 per second while an enemy moves inside it |
| B2b | **Snare Trap** | Branch (Lv. 10) | 70 / 16 s | 1 tile (placement rule below) | Invisible. The first enemy to step on it gets **Ensnare** 1.5 / 1.75 / 2 / 2.25 / 2.5 s and takes +10 / 15 / 20 / 25 / 30% damage from all sources while rooted. Max **1 active** (2 with Scavenger's Prep Lv. 3+). Lasts until triggered or 15 s. **Pre-placed** (GDD §6.2): the first Snare Trap is placed by the player before battle, free, and lasts until triggered |
| B2p | **Scavenger's Prep** | Branch (Lv. 10) | — | Self | Trap cooldowns −4 / 8 / 12 / 16 / 20%; from Lv. 3, a 2nd Snare Trap can be active |

**In-battle trap placement:** in the path of the nearest enemy moving toward his side; if none is moving, just in front of his own front row. Traps don't hit enemies that never move (Long range): that's their counter.

**B3 · Goblin Sapper** (role: **Mage**, off-role) — high risk, high reward (Techies style): trades stealth for volatile area explosions. Area damage stays below Mage specialists (GDD §6.3). Explosions are **physical with the Fire tag** (GDD §6.9): they ignite Oiled enemies, and backfire if Snick is Oiled.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B3a | **Black Powder Grenade** | Branch (Lv. 10) | 90 / 16 s | The target and every enemy within 1 tile | 60 / 95 / 130 / 165 / 200 physical damage + **Knockback** on everyone hit |
| B3b | **Kamikaze Dash** | Branch (Lv. 10) | 120 / 24 s | Front-most enemy; enemies within 1 tile of the blast | Straps on a lit fuse and charges: 100 / 150 / 200 / 250 / 300 physical damage. **Costs him 15% of his max HP; if his HP is at or below the cost, the blast knocks him out.** Afterwards he is thrown 2 tiles back toward his side. AI-controlled Snick (PvP defense) never casts it when it would knock him out |
| B3p | **Blast Shielding** | Branch (Lv. 10) | — | Self | Self-damage from his skills −10 / 20 / 30 / 40 / 50%; 2 / 4 / 6 / 8 / 10% of his explosive damage dealt becomes a shield on himself for 4 s |

**Gear skill fit:** Physical, Crit, Speed. (guidance for which gear skills suit it, GDD §4.7.6).

## 6. Equipment
| Slot | Allowed |
|---|---|
| Weapon | Core and B1 Shadow Assassin: Dagger, Sword. **B2 Trapmaster: Knife only. B3 Goblin Sapper: Bomb only** (still melee, 1 tile) |
| Armor | Any piece |
| Accessory | Any |
| Default weapon | Core / B1: Sword (worn as a "big knife"). B2: a hooked wire knife. B3: a fizzing clay bomb (visual only) |

⚠️ Knife and Bomb families have **no gear cards yet** (GDD §13 #44): until they exist, B2 and B3 fight with their default weapon only. Planned: Knife cards at Tier IV, Bomb cards at Tier V. Planned: Bomb weapons give **+1 range** (thrown), so the Sapper attacks from 2 tiles while staying melee (GDD §6.2).

## 7. Trait
- Chance: 30% when born; if it rolls: Faint 65% · Bright 27% · Radiant 8% · Unique (GDD §4.6.4).
- Fitting trait tags: Physical, Crit, Speed ([TraitPool.md](../TraitPool.md)).

## 8. Illustrator Brief (draft)
| Field | Value |
|---|---|
| Silhouette & key shapes | Small, thin and bald; pointed elf ears that twitch at every sound; crouched, ready to bolt |
| Palette (3–4 colors) | Moss green skin, worn grey-brown rags, a sand-colored pouch, faded workshop-issue straps |
| Race family base body | Greenskin base body (shared with Hobgoblin, Orc and Troll scaled) |
| Weapon held | A chipped short blade held backwards; a worn sand pouch at his hip |
| Card illustration | Mid-escape through a workshop doorway, a handful of sand flying behind him, ears flat |
| Battle views | Front ¾ and back ¾. Back view shows the sand pouch and ears |
| Animations | Idle (ears twitching, glancing over his shoulder), run (crouched), stab, Backstab (vanishing dash), Pocket Sand (throw), hit, KO (curls up small), victory (a quick, relieved breath; checks his pouch). Branches: B1 Backstab lunge, Shadow Stalker fade and reappear; B2 kneels to set a trap, scatters caltrops; B3 bomb throw, lit-fuse charge and blast-back tumble |
| Branch props | Never replace the equipped weapon (GDD §4.7.5). B1 a dark hood; his blade blackened (accent on any equipped weapon). B2 a coil of wire and a pouch of trap parts. B3 a bandolier of junk bombs |
| VFX per skill | Pocket Sand: sand puff; Nimble Escape: dust kick; Backstab: shadow streak; Shadow Stalker: fade + reappear shimmer; Caltrops & Wire: scattered spikes; Snare Trap: hidden glint, then snapping jaws; Black Powder Grenade: smoky fire blast; Kamikaze Dash: fuse sparks trail, big explosion |
| SFX / voice notes | Quick light footsteps; a sharp nervous laugh; a hiss of sand |
| References | TBD (moodboard) |
| Avoid | Anything that looks like an existing game's character |
