# Snick · Goblin – Rogue

**Status:** Draft (for review)

## 1. Identity
| Field | Value |
|---|---|
| Character name | Snick |
| Data ID | `SO_Hero_GoblinRogue` |
| Race (family) | Goblin (Greenskin) |
| Class | Rogue |
| Initial role | Assassin |
| Branch roles | Assassin (all branches) |
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
Skill points: 1 per hero level. Every skill has 5 levels: core + one branch = 6 × 5 = 30 points, all spent at Lv. 30. Statuses: GDD §6.10.

**Core**
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| A1 | **Backstab** | Start | 60 / 10 s | Back-line enemy | Dashes behind them: 90 / 140 / 190 / 240 / 290 physical damage |
| A2 | **Pocket Sand** | A1 Lv. 2 | 50 / 14 s | Current target | Confuse 1 / 1.5 / 2 / 2.5 / 3 s |
| P0 | **Sticky Fingers** (core passive) | Start | — | Self | Basic hits have a 4 / 8 / 12 / 16 / 20% chance to steal 10 mana from the target |

**Branch point:** after A1 Lv. 2 (A2 and the branch open at the same time). Permanent choice; he stays an Assassin.

**B1 · Cutthroat** — fast hands, faster finishes.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B1a | **Flurry** | Branch chosen | 80 / 12 s | Current target | 4 quick stabs, 30 / 45 / 60 / 75 / 90 physical damage each |
| B1b | **Finish Them** | B1a Lv. 2 | 90 / 16 s | Enemy below 30% HP (else lowest HP) | 150 / 250 / 350 / 450 / 550 physical damage |
| B1p | **Opportunist** | B1b Lv. 2 | — | Self | +3 / 5 / 7 / 9 / 11% Crit Chance |

**B2 · Shadow** — now you see him, now he has your wallet.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B2a | **Vanish** | Branch chosen | 70 / 18 s | Self | Untargetable for 1.5 / 2 / 2.5 / 3 / 3.5 s; his next hit deals +50% damage |
| B2b | **Junk Decoy** | B2a Lv. 2 | 60 / 20 s | His cell | Leaves a pile of junk that Taunts enemies for 2 / 2.5 / 3 / 3.5 / 4 s |
| B2p | **Slippery** | B2b Lv. 2 | — | Self | +8 / 10 / 12 / 14 / 16% Evasion |

**B3 · Dirty Fighter** — rusty, sneaky and proud of it.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B3a | **Rusty Shiv** | Branch chosen | 60 / 10 s | Current target | 40 / 60 / 80 / 100 / 120 physical damage + Bleed 20 / 30 / 40 / 50 / 60 per second for 4 s |
| B3b | **Gutter Bomb** | B3a Lv. 2 | 90 / 18 s | Back enemy row | 60 / 95 / 130 / 165 / 200 physical damage + Stagger |
| B3p | **Dirty Tricks** | B3b Lv. 2 | — | Self | +4 / 8 / 12 / 16 / 20% damage to enemies with any status |

**Scroll skill tags:** Physical, Crit, Speed.

## 6. Equipment
| Slot | Allowed |
|---|---|
| Weapon | Dagger, Sword |
| Armor | Any piece |
| Accessory | Any |
| Default weapon | Sword (worn as a "big knife") |

## 7. Unique Trait
- Odds: Bronze 70% · Silver 25% · Gold 5%.
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
| Animations | Idle (ears twitching, glancing over his shoulder), run (crouched), stab, Backstab (vanishing dash), Pocket Sand (throw), hit, KO (curls up small), victory (a quick, relieved breath; checks his pouch). Branches: B1 stab flurry; B2 fade out + junk pile drop; B3 shiv + bomb throw |
| Branch props | B1 a pair of polished daggers; B2 a hooded coat; B3 a bandolier of junk bombs |
| VFX per skill | Backstab: shadow streak; Pocket Sand: sand puff; Flurry: slash lines; Finish Them: big red slash; Vanish: smoke ring; Junk Decoy: junk pile pop; Rusty Shiv: dripping red ticks; Gutter Bomb: clattering blast |
| SFX / voice notes | Quick light footsteps; a sharp nervous laugh; a hiss of sand |
| References | TBD (moodboard) |
| Avoid | Anything that looks like an existing game's character |
