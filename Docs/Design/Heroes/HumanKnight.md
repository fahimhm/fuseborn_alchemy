# Tobin · Human – Knight

**Status:** Numbers done (approved pilot)

## 1. Identity
| Field | Value |
|---|---|
| Character name | Tobin |
| Data ID | `SO_Hero_HumanKnight` |
| Race (family) | Human (Folk) |
| Class | Knight |
| Initial role | Tank |
| Branch roles | B1 Bludgeon: **Warrior** (off-role) · B2 Ultimate Protector: Tank · B3 Spellguard: Tank |
| Tier | I |
| Recipe(s) | Basic |
| Basic rarity | Seasonal, hidden (GDD §4.2.2) |
| Codex flavor | "He raised his shield before he learned his own name." |

## 2. Backstory
**Personality keywords:** anxious, loyal, clingy, quietly brave.

Tobin opened his eyes on a workbench, dizzy, with no past and no idea what he was supposed to be. The first thing he grabbed was a dented pot lid; the second was the guild master's sleeve. He decided right then that the guild was the only safe place in Alembria, and he swore an oath to protect it, mostly so it would never send him away. The pot lid became his shield. It blocks almost nothing, but he won't trade it for anything. His short sword is so dull it barely cuts bread. Tobin is always at the front of every fight, not because he is brave, but because whenever danger appears, he raises his shield first and forgets to step back. Somehow, that keeps working.

## 3. Combat Profile
| Field | Value |
|---|---|
| Dominant principle | Salt |
| Attack type | Melee |
| Damage type | Physical |
| Attack range | Melee (1 tile) |
| Base attack interval | 1.7 s |
| Move Speed | 300 |
| Targeting | Front-most → Same lane |
| Recommended row | Front |

## 4. Stats
| | Base (Lv. 1) | Growth / level |
|---|---|---|
| Salt | 24 | 3.0 |
| Mercury | 12 | 1.2 |
| Sulfur | 14 | 1.4 |

Budget: base 50 (46–54 ✔), growth 5.6 (5.0–6.0 ✔).

| Other base values | Value |
|---|---|
| Base HP | 200 |
| Base attack damage | 26 (the dull sword) |
| Base DEF / RES | 6 / 0 (Tobin's own DEF growth, GDD §6.9) |
| DEF growth / level | 0.3 |
| Base mana | 75 |

**Derived** (GDD §6.9 rates incl. Resonance, no gear):
| Stat | Lv. 1 | Lv. 30 |
|---|---|---|
| HP / HP regen | 728 / 2.6 per s | 2,642 / 12.2 per s |
| Mana / mana regen | 243 / 0.70 per s | 730 / 2.73 per s |
| Attack damage | 50 | 137 |
| DEF (reduction) | 7.8 (32%) | 21.7 (57%) |
| RES (reduction) | 2.1 (11%) | 8.2 (33%) |
| Attacks per second | 0.66 | 0.86 |

## 5. Skill Tree
Skill points: 1 per hero level, spent on any open skill. Every skill has 5 levels; a skill's level can't exceed hero level ÷ 2, rounded up. Core skills are all open from Lv. 1; the branch opens at **hero Lv. 10** with all 3 of its skills open (GDD §4.6.4). Core + one branch = 6 × 5 = 30 points, all spent at Lv. 30. Statuses: GDD §6.10.

**Core**
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| A1 | **Shield Bash** | Lv. 1 | 60 / 12 s | Current target | Hits with the pot lid: 60 / 100 / 140 / 180 / 220 physical damage, Stun 1.0 / 1.25 / 1.5 / 1.75 / 2.0 s |
| A2 | **Panicked Shout** | Lv. 1 | 80 / 18 s | Front-most enemy row | Yells in panic; enemies turn to him. Taunt 2 / 2.5 / 3 / 3.5 / 4 s; +4 / 6 / 8 / 10 / 12 DEF while it lasts |
| P0 | **Pot-Lid Guard** (core passive) | Lv. 1 | — | Self | 4 / 6 / 8 / 10 / 12% chance to block half a physical hit. At battle start he raises his shield first: Shield 60 / 80 / 100 / 120 / 140 for 3 s |

**Branch point:** hero Lv. 10. Each branch is how Tobin finds his courage. Permanent choice. B2 and B3 keep him a Tank; **B1 makes him a Warrior** (GDD §4.6.4). In every branch he keeps Panicked Shout's Taunt, so a Warrior Tobin still protects a little (a weaker version of the Tank core tool).

**B1 · Bludgeon** (role: **Warrior**) — his bravery piles up until he stops hiding behind the lid and starts swinging: high mobility, staggering enemies, heavy physical damage.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B1a | **Shield Charge** | Branch (Lv. 10) | 90 / 14 s | Enemy in his lane | Dashes in and slams: 80 / 130 / 180 / 230 / 280 physical damage + Stagger; +20% Move Speed for 4 s |
| B1b | **Shield Toss** | Branch (Lv. 10) | 110 / 18 s | 3 enemies (bounces) | Throws the lid: 70 / 110 / 150 / 190 / 230 physical damage each. Pot-Lid Guard is off until it returns (2 s) |
| B1p | **Heavy Lid** | Branch (Lv. 10) | — | Self | +1 / 1.25 / 1.5 / 1.75 / 2 attack damage per point of DEF; +4 / 8 / 12 / 16 / 20% Move Speed |

**B2 · Ultimate Protector** (role: Tank) — he gains confidence in defense.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B2a | **Wall** | Branch (Lv. 10) | 120 / 25 s | Allies in his lane + adjacent lanes | Plants the lid: a **shared shield** absorbs 150 / 240 / 330 / 420 / 510 damage in total for 6 s for every ally in those lanes; he can't move. **Redirection:** when it ends, 30% of the absorbed damage hits the front-most enemies |
| B2b | **Oath Leap** | Branch (Lv. 10) | 70 / 16 s | Lowest-HP ally | Leaps to them and takes all hits meant for them for 2 / 2.5 / 3 / 3.5 / 4 s |
| B2p | **Unshaken** | Branch (Lv. 10) | — | Self | Immune to knockback; status durations −10 / 20 / 30 / 40 / 50%; +4 / 5 / 6 / 7 / 8% block chance (stacks with Pot-Lid Guard, max 20%) |

**B3 · Spellguard** (role: Tank) — magic infuses the shield.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B3a | **Spell Mirror** | Branch (Lv. 10) | 100 / 20 s | Self | For 3 s, reflects the next 1 / 1 / 2 / 2 / 3 enemy magic skills that hit him back at the caster at 50 / 60 / 70 / 80 / 90% damage |
| B3b | **Lid Flash** | Branch (Lv. 10) | 110 / 22 s | Front-most enemy row; allies in his lane | Confuse 1.5 / 2 / 2.5 / 3 / 3.5 s; heals allies in his lane for 60 / 90 / 120 / 150 / 180 |
| B3p | **Rune-Etched Lid** | Branch (Lv. 10) | — | Self | Pot-Lid Guard can also block magic hits; +3 / 4 / 5 / 6 / 7 RES |

**Scroll skill tags:** Guard, Physical, Control.

## 6. Equipment
| Slot | Allowed |
|---|---|
| Weapon | Sword, Shield |
| Armor | Any piece |
| Accessory | Any |
| Default weapon | Sword (drawn dull) |

The pot-lid shield is part of Tobin (his look and P1), not a Gear card. If he equips a Tower Shield, his art swaps to it.

## 7. Unique Trait
- Odds: Bronze 70% · Silver 25% · Gold 5%.
- Fitting trait tags: Guard, Physical, Control ([TraitPool.md](../TraitPool.md)).

## 8. Illustrator Brief (draft)
| Field | Value |
|---|---|
| Silhouette & key shapes | Slightly hunched, peeking over an oversized round dented pot lid; helmet a size too big; the pot lid is the readable shape |
| Palette (3–4 colors) | Muted and mismatched: worn steel, faded guild blue, copper pot-lid brown, a patch of red cloth |
| Race family base body | Folk base body (shared with other Humans; Dwarf scaled) |
| Weapon held | Nicked, dull short sword held low (right); dented pot lid always raised (left) |
| Card illustration | Peeking over the pot lid in the guild workshop; the guild master's hand or silhouette just in frame behind him |
| Battle views | Front ¾ and back ¾. Back view must show the pot lid and the too-big helmet clearly |
| Animations | Idle (peeks over the shield), run (shield first), weak sword poke, Shield Bash, Panicked Shout (eyes shut, yelling), hit (ducks), KO (curls up behind the shield, not hurt), victory (relieved sigh, then looks back to the guild master). Branches: B1 charge + toss/catch; B2 plant (trembling) + leap; B3 mirror raise + flash |
| Branch props | Lid variant per branch: B1 thick, dented, iron-rimmed; B2 wide, battle-scarred; B3 etched with glowing runes. Posture grows more confident with each branch |
| VFX per skill | Shield Bash: dull "clong" flash + stars; Panicked Shout: wobbly shout ring; Shield Charge: dust trail; Shield Toss: spinning lid arc; Wall: blue barrier across lanes, then a burst; Oath Leap: jump arc; Spell Mirror: rune glint on the lid; Lid Flash: bright white flash |
| SFX / voice notes | Pot-lid clangs; nervous gulps; a squeaky battle cry on Panicked Shout |
| References | TBD (moodboard) |
| Avoid | Heroic or noble poses; anything that looks like an existing game's character |
