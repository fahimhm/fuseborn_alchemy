# Wren · Elf – Archer

**Status:** Numbers done (approved)

## 1. Identity
| Field | Value |
|---|---|
| Character name | Wren |
| Data ID | `SO_Hero_ElfArcher` |
| Race (family) | Elf (Elven) |
| Class | Archer |
| Initial role | Ranger |
| Branch roles | Ranger (both branches) |
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
| Dominant principle | Mercury |
| Attack type | Ranged |
| Damage type | Physical |
| Attack range | Long (7 tiles) |
| Base attack interval | 1.6 s |
| Move Speed | — (Long range: never needs to move) |
| Targeting | Same lane, back-most → Back-line |
| Recommended row | Back |

## 4. Stats
| | Base (Lv. 1) | Growth / level |
|---|---|---|
| Salt | 14 | 1.4 |
| Mercury | 24 | 3.0 |
| Sulfur | 12 | 1.2 |

Budget: base 50 (46–54 ✔), growth 5.6 (5.0–6.0 ✔).

| Other base values | Value |
|---|---|
| Base HP | 180 |
| Base attack damage | 24 |
| Base DEF / RES | 1 / 0 |
| Base mana | 75 |

**Derived** (GDD §6.9 rates incl. Resonance, no gear):
| Stat | Lv. 1 | Lv. 30 |
|---|---|---|
| HP / HP regen | 460 / 1.4 per s | 1,272 / 5.5 per s |
| Mana / mana regen | 219 / 0.60 per s | 637 / 2.34 per s |
| Attack damage | 48 | 135 |
| DEF (reduction) | 5.0 (23%) | 19.3 (54%) |
| RES (reduction) | 1.8 (10%) | 7.0 (30%) |
| Attacks per second | 0.79 | 1.39 |

## 5. Skill Tree
Skill points: 1 per hero level, spent on any open skill. Every skill has 5 levels; a skill's level can't exceed hero level ÷ 2, rounded up. Core skills are all open from Lv. 1; the branch opens at **hero Lv. 10** with all 3 of its skills open (GDD §4.6.4). Core + one branch = 6 × 5 = 30 points, all spent at Lv. 30. Statuses: GDD §6.10.

**Core**
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| A1 | **Double Shot** | Lv. 1 | 50 / 8 s | Current target | Two arrows, 40 / 65 / 90 / 115 / 140 physical damage each |
| A2 | **Pinning Arrow** | Lv. 1 | 70 / 14 s | Current target | 70 / 110 / 150 / 190 / 230 physical damage + Stagger |
| P0 | **Forest Sense** (core passive) | Lv. 1 | — | Self | +3 / 5 / 7 / 9 / 11% Crit Chance |

**Branch point:** hero Lv. 10. **2 branches**, permanent choice: her two answers to the curse. She stays a Ranger.

**B1 · Leashed** — she obeys, careful never to wake the mark. Precision and burst.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B1a | **Aimed Shot** | Branch (Lv. 10) | 100 / 18 s | Current target | Aims for 1 s, then 200 / 300 / 400 / 500 / 600 physical damage |
| B1b | **Piercing Arrow** | Branch (Lv. 10) | 90 / 16 s | Her lane, all enemies | 90 / 140 / 190 / 240 / 290 physical damage to every enemy in her lane |
| B1p | **Fearful Focus** | Branch (Lv. 10) | — | Self | +4 / 8 / 12 / 16 / 20% damage to enemies below 50% HP |

**B2 · Unbound** — she still holds the grudge. Area control and evasion.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B2a | **Bramble Rain** | Branch (Lv. 10) | 120 / 22 s | Front 2 enemy rows | 3 waves of 20 / 30 / 45 / 55 / 70 physical damage (kept wide but light: a Ranger's area is weaker than a Mage's, GDD §6.3); the first wave applies **Ensnare** 1 / 1.25 / 1.5 / 1.75 / 2 s (15 / 20 / 25 / 30 / 35 damage per s) |
| B2b | **Wild Dance** | Branch (Lv. 10) | 80 / 20 s | Self | +15 / 20 / 25 / 30 / 35% Evasion for 4 s (Evasion cap 40% still applies) |
| B2p | **Caged Fury** | Branch (Lv. 10) | — | Self | **Rage:** +1 per hit taken (basic or skill). At **3 rage** she goes **Berserk** for 5 s: ×1.1 / 1.15 / 1.2 / 1.25 / 1.3 damage. On activation, roots burst through her lane: **Ensnare** on every enemy in it for 2 s (20 / 30 / 40 / 50 / 60 damage per s). When Berserk ends, the **curse** forces **Sleep** for 4 / 3.75 / 3.5 / 3.25 / 3 s: does **not** wake on damage and **ignores Control Resist**. Rage resets to 0; no rage is gained during Berserk or the curse Sleep |

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
| Animations | Idle (glances toward the horizon), shoot, Double Shot, Pinning Arrow, hit, KO, victory (lowers the bow, looks away). Branches: B1 slow aim; B2 vine-wrapped volley, Berserk (mark flares), curse Sleep (collapses, mark glowing) |
| Branch props | B1 a plain, well-kept bow; mark dimmed. B2 a bow wrapped in thorny vines; mark burning |
| VFX per skill | Double Shot: twin streaks; Pinning Arrow: impact pin; Aimed Shot: glint + long streak; Piercing Arrow: lane-long line; Bramble Rain: thorned arrow shower + roots; Wild Dance: leaf swirl; Caged Fury: mark flare, roots erupting down her lane, then a binding glow as she sleeps. UI: rage meter (3 pips) on her portrait, B2 only |
| SFX / voice notes | Bowstring twangs; a quiet exhale on crits; a sharp breath when the mark flares |
| References | TBD (moodboard) |
| Avoid | Anything that looks like an existing game's character |
