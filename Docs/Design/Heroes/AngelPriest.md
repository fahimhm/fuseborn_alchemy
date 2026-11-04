# Elsie · Angel – Priest

**Status:** Draft (rework in review). Needs 4 passive skills from the user: the core aura (Celestial Resilience) and one passive for each branch (The Seraph, The Archangel, The Fallen)

## 1. Identity
| Field | Value |
|---|---|
| Character name | Elsie |
| Data ID | `SO_Hero_AngelPriest` |
| Race (family) | Angel (Celestial) |
| Class | Priest |
| Role | Support |
| Tier | I |
| Recipe(s) | Basic |
| Basic rarity | Seasonal, hidden (GDD §4.2.2) |
| Codex flavor | "Has wings. Is afraid of heights. Heals anyway." |

## 2. Backstory
**Personality keywords:** gentle, worried, clumsy, warm.

Elsie woke up with a pair of white wings and immediately fell off the workbench. She has been afraid of heights ever since, which for an angel is a little awkward. She walks everywhere and flutters only when someone is hurt, and then she forgets to be scared. Elsie worries about everyone in the guild: she counts the homunculi before every battle and again after, and she knits bandages in her spare time even though her magic works better. Her healing light is warm and a little wobbly, like her flying. When the guild wins, she cries first and cheers second.

## 3. Combat Profile
| Field | Value |
|---|---|
| Main stat | MAG |
| Attack type | Ranged |
| Damage type | Magic |
| Attack range | Long |
| Base attack interval | 1.8 s |
| Move Speed | — (ranged, stays in her cell) |
| Targeting | Basic hits: Front-most → Random. Heals: lowest-HP ally |
| Recommended row | Back |

## 4. Stats
| | Base (Lv. 1) | Growth / level |
|---|---|---|
| STR | 12 | 1.2 |
| AGI | 12 | 1.2 |
| MAG | 26 | 3.2 |

Budget: base 50 (46–54 ✔), growth 5.6 (5.0–6.0 ✔).

| Other base values | Value |
|---|---|
| Base HP | 170 |
| Base attack damage | 20 |
| Base DEF / RES | 1 / 2 |
| Base mana | 100 |

**Derived** (GDD §6.9 rates, no gear):
| Stat | Lv. 1 | Lv. 30 |
|---|---|---|
| HP / HP regen | 410 / 1.2 per s | 1,106 / 4.7 per s |
| Mana / mana regen | 412 / 1.30 per s | 1,526 / 5.94 per s |
| Attack damage | 46 | 139 |
| DEF (reduction) | 2.8 (14%) | 8.0 (32%) |
| RES (reduction) | 5.9 (26%) | 19.8 (54%) |
| Attacks per second | 0.62 | 0.82 |

## 5. Skill Tree
Skill points: 1 per hero level. Every skill has 5 levels: core + one branch = 6 × 5 = 30 points, all spent at Lv. 30. Statuses: GDD §6.10.

**Core**
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| A1 | **Mend** | Start | 60 / 8 s | Lowest-HP ally | Heals 100 / 160 / 220 / 280 / 340 |
| A2 | **Feather Blessing** | A1 Lv. 2 | 90 / 16 s | 2 lowest-HP allies | Shield 80 / 130 / 180 / 230 / 280 for 4 s |
| P0 | **Worrier** (core passive) | Start | — | Allies | Her heals on allies below 30% HP are +4 / 8 / 12 / 16 / 20% stronger |

**Branch point:** after A2 Lv. 2. Permanent choice; she stays a Support.

**B1 · Radiance** — she learns her light can also push back.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B1a | **Smite** | Branch chosen | 90 / 14 s | Current target | 120 / 190 / 260 / 330 / 400 magic damage + Stun 0.5 / 0.75 / 1.0 / 1.25 / 1.5 s |
| B1b | **Halo Burst** | B1a Lv. 2 | 120 / 20 s | Front-most enemy row; all allies | 80 / 120 / 160 / 200 / 240 magic damage; heals all allies for 30% of the damage dealt |
| B1p | **Zeal** | B1b Lv. 2 | — | Self | +4 / 8 / 12 / 16 / 20% skill damage |

**B2 · Sanctuary** — she finds the courage to fly.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B2a | **Circle of Light** | Branch chosen | 130 / 22 s | All allies | Heals 30 / 45 / 60 / 75 / 90 per second for 5 s |
| B2b | **Second Wind** | B2a Lv. 2 | 150 / once per battle | First ally knocked out | Brings them back with 20 / 30 / 40 / 50 / 60% HP |
| B2p | **Grace** | B2b Lv. 2 | — | Self | +4 / 8 / 12 / 16 / 20% healing done |

**B3 · Purifier** — calm hands, clear minds.
| # | Skill | Unlock | Mana / CD | Target / area | Effect |
|---|---|---|---|---|---|
| B3a | **Cleanse** | Branch chosen | 70 / 12 s | 1 / 1 / 2 / 2 / 3 allies with a status | Removes all statuses and heals 50 / 80 / 110 / 140 / 170 |
| B3b | **Wing Gust** | B3a Lv. 2 | 100 / 18 s | Front-most enemy row | Knockback + Stagger; 50 / 80 / 110 / 140 / 170 magic damage |
| B3p | **Pure Heart** | B3b Lv. 2 | — | Allies in her lane | Status durations −4 / 8 / 12 / 16 / 20% (total cap −50%) |

**Scroll skill tags:** Support, Sustain, Magic.

## 6. Equipment
| Slot | Allowed |
|---|---|
| Weapon | Staff, Tome |
| Armor | Any piece |
| Accessory | Any |
| Default weapon | Staff |

## 7. Unique Trait
- Odds: Bronze 70% · Silver 25% · Gold 5%.
- Fitting trait tags: Support, Sustain, Magic ([TraitPool.md](../TraitPool.md)).

## 8. Illustrator Brief (draft)
| Field | Value |
|---|---|
| Silhouette & key shapes | Small and round; wings slightly too big and usually folded tight; a soft, lopsided halo |
| Palette (3–4 colors) | White, pale gold, sky blue, a knitted pink scarf |
| Race family base body | Celestial base body (shared with Half-Angel, Fairy scaled) |
| Weapon held | A short wooden staff with a bandage tied around the top |
| Card illustration | Kneeling beside a scuffed Tobin, healing light in her hands, eyes worried; wings tucked in |
| Battle views | Front ¾ and back ¾. Back view must read the wings clearly |
| Animations | Idle (wings twitching nervously), cast, Mend, Feather Blessing, hit, KO (sits down, dizzy), victory (happy cry, then cheer). Branches: B1 smite point; B2 hover with wings open (the only time she flies); B3 gentle touch + wing flap |
| Branch props | B1 halo burns brighter; B2 wings spread open; B3 a small bell on the staff |
| VFX per skill | Mend: warm sparkles; Feather Blessing: floating feathers forming a shield; Smite: golden beam; Halo Burst: ring of light; Circle of Light: glowing circle on the ground; Second Wind: rising feathers; Cleanse: soft chime glow; Wing Gust: feather wind |
| SFX / voice notes | Soft chimes; nervous "oh no, oh no" when allies are low; relieved giggle |
| References | TBD (moodboard) |
| Avoid | Anything that looks like an existing game's character |
