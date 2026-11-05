# Grum · Orc – Warlock

**Status:** Draft (for review)

## 1. Identity
| Field | Value |
|---|---|
| Character name | Grum |
| Data ID | `SO_Hero_OrcWarlock` |
| Race (family) | Orc (Greenskin) |
| Class | Warlock |
| Initial role | Mage |
| Branch roles | Mage (all branches) |
| Tier | I |
| Recipe(s) | Basic |
| Basic rarity | Seasonal, hidden (GDD §4.2.2) |
| Soul | Yes: a reincarnated child's soul; keeps only its curiosity (Lore.md) |
| Codex flavor | "Great power, sworn in blood. Paid in donuts." |

## 2. Backstory
**Personality keywords:** polite, bookish, gentle giant, nervous about his own power.

Grum is the biggest homunculus in the guild and the quietest. He woke up, apologised for taking up so much space, and asked if there was anything to read. Nobody knows why a giant has a child's curiosity; his soul has been somewhere before, and kept only that. He spent his nights in the guild library, until an old hex book answered him back. Grum was too polite to refuse its offer. Now dark power flows through him, and every week a box of donuts disappears from the shelf where the book sleeps. His magic scares him, so he uses it carefully: "excuse me" before every hex, "sorry" after. He still reads bedtime stories to the younger homunculi, though Snick keeps stealing the bookmarks.

**The oath:** the dark being in the library's hex book (Lore.md) grants his dark energy. Its price: donuts, a lot of them. What else it wants is an open story hook.

## 3. Combat Profile
| Field | Value |
|---|---|
| Dominant principle | Sulfur |
| Attack type | Ranged |
| Damage type | Magic |
| Attack range | Long (7 tiles) |
| Base attack interval | 1.8 s |
| Move Speed | — (Long range: never needs to move) |
| Targeting | Largest group (middle row) → Front-most |
| Recommended row | Back |

## 4. Stats
| | Base (Lv. 1) | Growth / level |
|---|---|---|
| Salt | 16 | 1.8 |
| Mercury | 10 | 1.0 |
| Sulfur | 24 | 2.8 |

Budget: base 50 (46–54 ✔), growth 5.6 (5.0–6.0 ✔).

| Other base values | Value |
|---|---|
| Base HP | 200 |
| Base attack damage | 22 |
| Base DEF / RES | 2 / 2 |
| Base mana | 90 |

**Derived** (GDD §6.9 rates incl. Resonance, no gear):
| Stat | Lv. 1 | Lv. 30 |
|---|---|---|
| HP / HP regen | 520 / 1.6 per s | 1,564 / 6.8 per s |
| Mana / mana regen | 407 / 1.32 per s | 1,479 / 5.79 per s |
| Attack damage | 46 | 127 |
| DEF (reduction) | 3.5 (17%) | 7.8 (32%) |
| RES (reduction) | 6.0 (26%) | 19.4 (54%) |
| Attacks per second | 0.61 | 0.77 |

## 5. Skill Tree
Skill points: 1 per hero level. Every skill has 5 levels: core + one branch = 6 × 5 = 30 points, all spent at Lv. 30. Statuses: GDD §6.10.

**Core**
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| A1 | **Hex Bolt** | Start | 60 / 8 s | Current target | 90 / 140 / 190 / 240 / 290 magic damage |
| A2 | **Weakening Hex** | A1 Lv. 2 | 80 / 16 s | Current target | Weaken: the target deals −15 / 20 / 25 / 30 / 35% damage for 4 s |
| P0 | **Bookworm** (core passive) | Start | — | Self | +4 / 8 / 12 / 16 / 20% mana regen |

**Branch point:** after A2 Lv. 2. **3 branches**, permanent choice: three ways to use the dark being's gift. He stays a Mage.

**B1 · Soul Reaper** (role: Mage) — sustain battle-mage: the longer the fight lasts, the harder he is to kill. Overtime (GDD §6.12) halves his healing in the last 15 s; intended.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B1a | **Soul Tether** | Branch chosen | 90 / 16 s | Current target | Tether for 5 s: drains 20 / 30 / 40 / 50 / 60 magic damage per s and heals Grum for all of it; **steals 5 / 7.5 / 10 / 12.5 / 15% Evasion** (the target loses it, Grum gains it even with no Evasion of his own; 40% cap) |
| B1b | **Drain Life** | B1a Lv. 2 | 90 / 14 s | Current target | 80 / 125 / 170 / 215 / 260 magic damage; heals Grum for 50% of it |
| B1p | **Undying Hunger** | B1b Lv. 2 | — | Self | Every 3 s in battle: +1 / 1.5 / 2 / 2.5 / 3 DEF and RES, stacks up to 5 times (full at 15 s) |

**B2 · Demonology** (role: Mage) — pacts with minions. Summon rules: GDD §6.11 (max 2 minions, shared by both skills).
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B2a | **Summon Imp** | Branch chosen | 100 / 20 s | Empty ally tile (GDD §6.11) | Ranged imp, **Medium range (5 tiles)**: HP 200 / 300 / 400 / 500 / 600; 20 / 30 / 40 / 50 / 60 magic damage every 1.5 s |
| B2b | **Summon Brute** | B2a Lv. 2 | 140 / 30 s | Empty ally tile (GDD §6.11) | Melee brute, **Melee (1 tile), Move Speed 280**: HP 400 / 600 / 800 / 1,000 / 1,200, DEF 6; 30 / 40 / 50 / 60 / 70 physical damage every 2 s; **Taunts** for 2 s when it appears |
| B2p | **Dark Command** | B2b Lv. 2 | — | His minions | +10 / 15 / 20 / 25 / 30% HP and damage |

**B3 · Corruptor** (role: Mage) — spreading curses (GDD §6.10 Curse: jumps on death).
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B3a | **Spreading Curse** | Branch chosen | 100 / 18 s | The target and every enemy within 1 tile of it | **Curse** 6 s, 20 / 27.5 / 35 / 42.5 / 50 magic damage per s |
| B3b | **Blight Wave** | B3a Lv. 2 | 110 / 20 s | Front-most enemy row | **Curse** 4 s, 15 / 20 / 25 / 30 / 35 magic damage per s |
| B3p | **Lingering Curse** | B3b Lv. 2 | — | Self | His Curses last +20 / 25 / 30 / 35 / 40% longer |

**Scroll skill tags:** Magic, Control, Sustain.

## 6. Equipment
| Slot | Allowed |
|---|---|
| Weapon | Staff, Tome |
| Armor | Any piece |
| Accessory | Any |
| Default weapon | Staff |

## 7. Unique Trait
- Odds: Bronze 70% · Silver 25% · Gold 5%.
- Fitting trait tags: Magic, Control, Sustain ([TraitPool.md](../TraitPool.md)).

## 8. Illustrator Brief (draft)
| Field | Value |
|---|---|
| Silhouette & key shapes | Huge, round-shouldered, slightly stooped; tiny reading glasses on a big face; a thick book chained to the belt |
| Palette (3–4 colors) | Olive skin, deep purple robe, bone-white trim, soft green magic glow |
| Race family base body | Greenskin base body (large scale, shared with Hobgoblin, Troll) |
| Weapon held | A gnarled staff with a cracked teapot hanging from it (the first thing he cursed) |
| Card illustration | Sitting on a crate reading the hex book, glasses slipping; a faintly glowing cursed teapot beside him |
| Battle views | Front ¾ and back ¾. Back view shows the chained book and robe |
| Animations | Idle (reads, turns a page), cast, Hex Bolt, Weakening Hex, hit, KO (sits down heavily), victory (polite bow). Branches: B1 tether pull + drain beam; B2 summoning gesture over a sigil; B3 two-handed spreading cast |
| Branch props | B1 dark red veins on the robe; B2 the hex book floats open beside him (a donut crumb on the page); B3 rotting purple pages drift around him |
| VFX per skill | Hex Bolt: green-purple orb; Weakening Hex: wilting sigil; Soul Tether: dark red chain between Grum and target; Drain Life: red beam; Undying Hunger: stacking dark aura; Summon Imp / Brute: summoning circle; Spreading Curse: purple rot blooming in a cross; Blight Wave: row-wide rot; Curse jump: purple wisp to the next enemy |
| SFX / voice notes | Deep, soft voice; "Excuse me." before casts, "Sorry!" after big hits |
| References | TBD (moodboard) |
| Avoid | Anything that looks like an existing game's character |
