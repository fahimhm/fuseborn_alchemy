# Grum · Orc – Warlock

**Status:** Draft (for review)

## 1. Identity
| Field | Value |
|---|---|
| Character name | Grum |
| Data ID | `SO_Hero_OrcWarlock` |
| Race (family) | Orc (Greenskin) |
| Class | Warlock |
| Role | Mage |
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
| Main stat | MAG |
| Attack type | Ranged |
| Damage type | Magic |
| Attack range | Long |
| Base attack interval | 1.8 s |
| Move Speed | — (ranged, stays in his cell) |
| Targeting | Largest group (middle row) → Front-most |
| Recommended row | Back |

## 4. Stats
| | Base (Lv. 1) | Growth / level |
|---|---|---|
| STR | 16 | 1.8 |
| AGI | 10 | 1.0 |
| MAG | 24 | 2.8 |

Budget: base 50 (46–54 ✔), growth 5.6 (5.0–6.0 ✔).

| Other base values | Value |
|---|---|
| Base HP | 200 |
| Base attack damage | 22 |
| Base DEF / RES | 2 / 2 |
| Base mana | 90 |

**Derived** (GDD §6.9 rates, no gear):
| Stat | Lv. 1 | Lv. 30 |
|---|---|---|
| HP / HP regen | 520 / 1.6 per s | 1,564 / 6.8 per s |
| Mana / mana regen | 378 / 1.20 per s | 1,352 / 5.26 per s |
| Attack damage | 46 | 127 |
| DEF (reduction) | 3.5 (17%) | 7.8 (32%) |
| RES (reduction) | 5.6 (25%) | 17.8 (52%) |
| Attacks per second | 0.61 | 0.77 |

## 5. Skill Tree
Skill points: 1 per hero level. Every skill has 5 levels: core + one branch = 6 × 5 = 30 points, all spent at Lv. 30. Statuses: GDD §6.10.

**Core**
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| A1 | **Hex Bolt** | Start | 60 / 8 s | Current target | 90 / 140 / 190 / 240 / 290 magic damage |
| A2 | **Weakening Hex** | A1 Lv. 2 | 80 / 16 s | Current target | Weaken: the target deals −15 / 20 / 25 / 30 / 35% damage for 4 s |
| P0 | **Bookworm** (core passive) | Start | — | Self | +4 / 8 / 12 / 16 / 20% mana regen |

**Branch point:** after A2 Lv. 2. Permanent choice; he stays a Mage.

**B1 · Doom** — he stops holding back (and apologises more).
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B1a | **Shadow Burst** | Branch chosen | 130 / 20 s | Target cell + neighbors | 110 / 170 / 230 / 290 / 350 magic damage |
| B1b | **Soul Flame** | B1a Lv. 2 | 100 / 16 s | Middle enemy row | Burn 30 / 45 / 60 / 75 / 90 magic damage per second for 4 s |
| B1p | **Overcharge** | B1b Lv. 2 | — | Self | +4 / 8 / 12 / 16 / 20% skill damage; skills cost +10% mana |

**B2 · Hexer** — curses as a fine art.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B2a | **Mass Weaken** | Branch chosen | 120 / 22 s | Front-most enemy row | Weaken −10 / 15 / 20 / 25 / 30% damage for 4 s |
| B2b | **Hex Chain** | B2a Lv. 2 | 110 / 20 s | 3 enemies | Links them for 5 s: 20 / 25 / 30 / 35 / 40% of damage taken by one is also dealt to the others |
| B2p | **Lingering Curse** | B2b Lv. 2 | — | Self | His statuses last +20 / 25 / 30 / 35 / 40% longer |

**B3 · Blood Pact** — big body, big reserves.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B3a | **Drain Life** | Branch chosen | 90 / 14 s | Current target | 80 / 125 / 170 / 215 / 260 magic damage; heals Grum for 50% of it |
| B3b | **Shared Strength** | B3a Lv. 2 | 60 / 18 s | Ally with the lowest mana | Spends 10% of his HP to give them 40 / 60 / 80 / 100 / 120 mana |
| B3p | **Thick Hide** | B3b Lv. 2 | — | Self | +4 / 5 / 6 / 7 / 8 DEF and RES |

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
| Animations | Idle (reads, turns a page), cast, Hex Bolt, Weakening Hex, hit, KO (sits down heavily), victory (polite bow). Branches: B1 big two-handed cast; B2 drawn sigil + chain toss; B3 drain beam + hand-to-shoulder |
| Branch props | B1 the book glows and floats; B2 hex charms hang from the staff; B3 dark red veins on the robe |
| VFX per skill | Hex Bolt: green-purple orb; Weakening Hex: wilting sigil; Shadow Burst: dark bloom; Soul Flame: green flames; Mass Weaken: row of sigils; Hex Chain: glowing chain links; Drain Life: red beam; Shared Strength: blue sparkle transfer |
| SFX / voice notes | Deep, soft voice; "Excuse me." before casts, "Sorry!" after big hits |
| References | TBD (moodboard) |
| Avoid | Anything that looks like an existing game's character |
