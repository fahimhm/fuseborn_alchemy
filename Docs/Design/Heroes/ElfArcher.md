# Wren · Elf – Archer

**Status:** Draft (for review)

## 1. Identity
| Field | Value |
|---|---|
| Character name | Wren |
| Data ID | `SO_Hero_ElfArcher` |
| Race (family) | Elf (Elven) |
| Class | Archer |
| Role | Ranger |
| Tier | I |
| Recipe(s) | Basic |
| Basic rarity | Seasonal, hidden (GDD §4.2.2) |
| Soul | Yes: an elf soul drawn from the forest (Lore.md) |
| Codex flavor | "Her soul remembers a forest she has never seen. The mark on her brow remembers who she belongs to." |

## 2. Backstory
**Personality keywords:** proud, restless, homesick, defiant.

Wren woke with leaves in her memory. She had never seen a forest, yet she knew its smell, its paths, the sound of its wind. Within a day she tried to leave. The guild master stopped her the only way an alchemist could: a binding mark burned into her brow. The harder she pulls toward the forest, the tighter it holds. Fury doesn't break it. She has tried. Now she draws her bow for the guild, and every arrow hits. Some days she shoots calmly, careful not to wake the mark. Other days she shoots like she's aiming past every enemy, at someone standing behind her. She hasn't stopped listening for the wind.

**The curse:** placed by the guild master (the player). The stronger her urge to return to the forest, the stronger it binds; even berserk she cannot break it. Her branches are her two answers to it (§5).

## 3. Combat Profile
| Field | Value |
|---|---|
| Main stat | AGI |
| Attack type | Ranged |
| Damage type | Physical |
| Attack range | Long |
| Base attack interval | 1.6 s |
| Move Speed | — (ranged, stays in her cell) |
| Targeting | Same lane, back-most → Back-line |
| Recommended row | Back |

## 4. Stats
| | Base (Lv. 1) | Growth / level |
|---|---|---|
| STR | 14 | 1.4 |
| AGI | 24 | 3.0 |
| MAG | 12 | 1.2 |

Budget: base 50 (46–54 ✔), growth 5.6 (5.0–6.0 ✔).

| Other base values | Value |
|---|---|
| Base HP | 180 |
| Base attack damage | 24 |
| Base DEF / RES | 1 / 0 |
| Base mana | 75 |

**Derived** (GDD §6.9 rates, no gear):
| Stat | Lv. 1 | Lv. 30 |
|---|---|---|
| HP / HP regen | 460 / 1.4 per s | 1,272 / 5.5 per s |
| Mana / mana regen | 219 / 0.60 per s | 637 / 2.34 per s |
| Attack damage | 48 | 135 |
| DEF (reduction) | 4.6 (22%) | 17.6 (51%) |
| RES (reduction) | 1.8 (10%) | 7.0 (30%) |
| Attacks per second | 0.77 | 1.32 |

## 5. Skill Tree
Skill points: 1 per hero level. Every skill has 5 levels: core + one branch = 6 × 5 = 30 points, all spent at Lv. 30. Statuses: GDD §6.10.

**Core**
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| A1 | **Double Shot** | Start | 50 / 8 s | Current target | Two arrows, 40 / 65 / 90 / 115 / 140 physical damage each |
| A2 | **Pinning Arrow** | A1 Lv. 2 | 70 / 14 s | Current target | 70 / 110 / 150 / 190 / 230 physical damage + Stagger |
| P0 | **Show-Off** (core passive) | Start | — | Self | +3 / 5 / 7 / 9 / 11% Crit Chance; after each crit she twirls (cosmetic) |

**Branch point:** after A1 Lv. 2 (A2 and the branch open at the same time). Permanent choice; she stays a Ranger.

**B1 · Sharpshooter** — she stops showing off and starts aiming.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B1a | **Aimed Shot** | Branch chosen | 100 / 18 s | Lowest-HP enemy | Aims for 1 s, then 200 / 300 / 400 / 500 / 600 physical damage |
| B1b | **Piercing Arrow** | B1a Lv. 2 | 90 / 16 s | One lane, all enemies | 90 / 140 / 190 / 240 / 290 physical damage to every enemy in the lane |
| B1p | **Eagle Eye** | B1b Lv. 2 | — | Self | +4 / 8 / 12 / 16 / 20% damage to enemies below 50% HP |

**B2 · Volley** — more arrows, more applause.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B2a | **Arrow Rain** | Branch chosen | 120 / 22 s | Front 2 enemy rows | 3 waves of 50 / 80 / 110 / 140 / 170 physical damage |
| B2b | **Scatter Shot** | B2a Lv. 2 | 90 / 16 s | Front-most enemy row | 60 / 95 / 130 / 165 / 200 physical damage + Stagger |
| B2p | **Quick Draw** | B2b Lv. 2 | — | Self | +4 / 8 / 12 / 16 / 20 Attack Speed |

**B3 · Trickster** — the elf who wins by being annoying.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B3a | **Smoke Arrow** | Branch chosen | 90 / 18 s | 1 enemy cell + neighbors | Confuse 1.5 / 2 / 2.5 / 3 / 3.5 s |
| B3b | **Decoy Arrow** | B3a Lv. 2 | 80 / 20 s | Empty cell in front of allies | A painted target that Taunts enemies for 2 / 2.5 / 3 / 3.5 / 4 s |
| B3p | **Light Feet** | B3b Lv. 2 | — | Self | +8 / 10 / 12 / 14 / 16% Evasion |

**Scroll skill tags:** Physical, Crit, Speed.

## 6. Equipment
| Slot | Allowed |
|---|---|
| Weapon | Bow |
| Armor | Any piece |
| Accessory | Any |
| Default weapon | Bow |

## 7. Unique Trait
- Odds: Bronze 70% · Silver 25% · Gold 5%.
- Fitting trait tags: Physical, Crit, Speed ([TraitPool.md](../TraitPool.md)).

## 8. Illustrator Brief (draft)
| Field | Value |
|---|---|
| Silhouette & key shapes | Tall and slim; long ponytail and pointed ears; a bow taller than she should carry; chin up, eyes often toward the horizon; **curse mark on her brow** |
| Palette (3–4 colors) | Forest green, cream, gold trim, a red guild-issued scarf she resents; the curse mark glows faintly (flares in Berserk) |
| Race family base body | Elven base body (shared with Light, Dark and Wood Elf) |
| Weapon held | Longbow; quiver with mismatched arrows (some fletched with workshop junk) |
| Card illustration | Drawing her bow at a workshop window, leaves drifting in from outside; the mark on her brow faintly glowing |
| Battle views | Front ¾ and back ¾. Back view shows the quiver and ponytail |
| Animations | Idle (glances toward the horizon), shoot, Double Shot, Pinning Arrow, hit, KO, victory (lowers the bow, looks away). Branches: B1 slow aim; B2 sky volley; B3 smoke shot + decoy toss |
| Branch props | B1 a simple tuned bow; B2 a quiver overflowing with arrows; B3 a bow tied with ribbons and a smoke pouch |
| VFX per skill | Double Shot: twin streaks; Pinning Arrow: impact pin; Aimed Shot: glint + long streak; Piercing Arrow: lane-long line; Arrow Rain: arrow shower; Scatter Shot: fan; Smoke Arrow: purple puff; Decoy Arrow: painted target pop-up |
| SFX / voice notes | Bowstring twangs; a quiet exhale on crits; a sharp breath when the mark flares |
| References | TBD (moodboard) |
| Avoid | Anything that looks like an existing game's character |
