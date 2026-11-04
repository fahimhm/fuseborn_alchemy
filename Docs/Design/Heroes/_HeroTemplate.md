# [Name] · [Race – Class]

> Copy this file to `<RaceClass>.md` (e.g. `ElfArcher.md`). Rules: GDD §4.6 (hero), §6 (combat), §6.9 (formulas). Lore: [Lore.md](../Lore.md).

**Status:** Draft · Numbers done · Art-ready  ← keep one

## 1. Identity
| Field | Value |
|---|---|
| Character name | One per hero type, humble or fitting the personality (GDD §15.1 rule 4) |
| Data ID | `SO_Hero_RaceClass` |
| Race (family) | e.g. Elf (Elven) |
| Class | |
| Role | Tank / Warrior / Ranger / Assassin / Mage / Support |
| Tier | I / II / III (recipe depth only, not power) |
| Recipe(s) | Tier I: basic. Otherwise A + B (and C + D) |
| Basic rarity | Tier I only: seasonal, hidden (GDD §4.2.2) |
| Codex flavor | One line, ≤ 100 characters, shown on the card |

## 2. Backstory
**Personality keywords:** 3–4 words.

80–150 words. Heroes are **homunculi** (Lore.md): new beings in the form of a people of Alembria, each with its own personality. Write how this one woke up, what it loves, what it is like in the guild. Tone: hopeful, with weight (Lore.md); can vary per homunculus. Say whether it has a soul (drawn from nature) or is soulless.

## 3. Combat Profile
| Field | Value |
|---|---|
| Main stat | STR / AGI / MAG (+1 attack damage per point) |
| Attack type | Melee / Ranged |
| Damage type | Physical / Magic |
| Attack range | Melee / Short / Long |
| Base attack interval | seconds (1.7 = normal) |
| Move Speed | melee only |
| Targeting | Primary → Fallback (GDD §6.4) |
| Recommended row | Front / Middle / Back |

## 4. Stats
| | Base (Lv. 1) | Growth / level |
|---|---|---|
| STR | | |
| AGI | | |
| MAG | | |

| Other base values | Value |
|---|---|
| Base HP | |
| Base attack damage | |
| Base DEF / RES | |
| DEF growth / level | (Tanks: 0.3; others: —) |
| Base mana | |

**Derived** (universal rates, GDD §6.9; no gear):
| Stat | Lv. 1 | Lv. 30 |
|---|---|---|
| HP / HP regen | | |
| Mana / mana regen | | |
| Attack damage | | |
| DEF (reduction) | | |
| RES (reduction) | | |
| Attacks per second | | |

**Power-budget check:** base STR + AGI + MAG = **46–54**, total growth = **5.0–6.0 / level** for every hero. The role decides the split, not the total.

## 5. Skill Tree
Rules: GDD §4.6.4. Skill points: 1 per hero level (30 at cap). Unlocks depend on **skill levels**. Every skill has 5 levels: core + one branch = 6 × 5 = 30 points, all spent at Lv. 30. Scroll skills cost no points (duplicate Scrolls level them). In battle: 2 actives. Statuses: GDD §6.10.

**Core** (every skill 5 levels; passives: Lv. 5 = the intended max)
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| A1 | | Start | | | |
| A2 | | A1 Lv. 2 | | | |
| P0 | (core passive) | Start | — | | |

**Branch point:** after A1 Lv. 2 / after A2 Lv. 2 (pick one). **Branches: 1 / 2 / 3** (pick to fit the lore; delete unused branch tables). With 2–3, choosing a branch is **permanent**; with 1, it opens automatically. Role stays the same in every branch.

**B1 · [Branch name]** (style in one line)
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B1a | | Branch chosen | | | |
| B1b | | B1a Lv. 2 | | | |
| B1p | (passive) | B1b Lv. 2 | — | | |

**B2 · [Branch name]** and **B3 · [Branch name]**: same table.

**Scroll skill tags** (which Scroll skills it can learn): e.g. Guard, Physical.

## 6. Equipment
| Slot | Allowed |
|---|---|
| Weapon | 1–3 families (Sword, Dagger, Bow, Staff, Tome, Shield, Instrument; GDD §4.7) |
| Armor | Any piece |
| Accessory | Any |
| Default weapon | The basic weapon the hero starts with |

## 7. Unique Trait
- Odds: Bronze 70% · Silver 25% · Gold 5% (default; GDD §4.6.4).
- Fitting trait tags: 2–3 from [TraitPool.md](../TraitPool.md) §2 (Guard, Physical, Magic, Crit, Speed, Sustain, Support, Control). Tags only drive the "Good fit" badge, not the roll.

## 8. Illustrator Brief
Fill only when sections 1–7 are done.

| Field | Value |
|---|---|
| Silhouette & key shapes | |
| Palette (3–4 colors) | |
| Race family base body | Shared rig/body with: |
| Weapon held | |
| Card illustration | Framing, pose, background mood |
| Battle views | **Front ¾** (as an enemy / PvP) and **back ¾** (own party) |
| Animations | Idle, move (melee), basic attack, one cast per active (A1, A2 + 2 per branch; reuse where possible), hit, KO, victory |
| Branch props | Optional: one signature prop variant per branch so the build reads at a glance |
| VFX per skill | |
| SFX / voice notes | |
| References | |
| Avoid | Anything that looks like an existing game's character |

New art, VFX and audio needs go into `Docs/Production/AssetList.md`.
