# Elsie · Angel – Priest

**Status:** Numbers done (approved)

## 1. Identity
| Field | Value |
|---|---|
| Character name | Elsie |
| Data ID | `SO_Hero_AngelPriest` |
| Race (family) | Angel (Celestial) |
| Class | Priest |
| Initial role | Support |
| Branch roles | B1 The Seraph: Support · B2 The Archangel: **Warrior** (off-role) · B3 The Fallen: **Mage** (off-role) |
| Tier | I |
| Recipe(s) | Basic |
| Basic rarity | Seasonal, hidden (GDD §4.2.2) |
| Soul | Yes: a fresh soul drawn from the sky's light; she arrived in the workshop as a bright light (Lore.md) |
| Codex flavor | "Her wings never opened. Her halo never dims." |

## 2. Backstory
**Personality keywords:** obedient, sweet, childlike, cozy.

Elsie arrived as a bright light in the workshop. When it faded, a little girl sat on the workbench, a halo above her head and two small wings hanging limp and wilted. The first face she saw was the Alchemist's, and she decided at once that this was Father: the one who made her, the one she should obey. She does everything Father asks, right away, without a question. She is still a little girl, though. She picks flowers for the windowsill, ties ribbons on everything, and knits tiny scarves for anyone who stands still long enough, Tobin included. Her wings won't open, however hard she tries. Her halo is different: when someone gets hurt, it shines so bright that enemies can't see, and her friends feel their wounds close. She doesn't understand battles yet. Each one leaves something behind.

**Father:** Elsie sees the Alchemist (the player) as her creator and god, whoever the player is. Her soul has its own will (Lore.md); obeying is her choice, out of love. Contrast with Tobin, whom the Alchemist guides with a father's hand: Elsie gives blind faith to an Alchemist who is not always good, which is why the Fallen branch hits hardest. Her branches are what battle makes of her (§5).

## 3. Combat Profile
| Field | Value |
|---|---|
| Dominant principle | Sulfur |
| Attack type | Ranged |
| Damage type | Magic |
| Attack range | Long (7 tiles) |
| Base attack interval | 1.8 s |
| Move Speed | — (Long range: never needs to move; Descent moves her, B2) |
| Targeting | Basic hits: Front-most → Lowest HP. Heals: ally with the lowest HP % |
| Recommended row | Back (Archangel: starts in the back, Descent takes her to the front) |

## 4. Stats
Three branch roles, so a flatter spread than single-role homunculi (GDD §4.6.2); the Archangel's toughness comes from her core aura and branch passive.

| | Base (Lv. 1) | Growth / level |
|---|---|---|
| Salt | 16 | 1.8 |
| Mercury | 12 | 1.2 |
| Sulfur | 22 | 2.6 |

Budget: base 50 (46–54 ✔), growth 5.6 (5.0–6.0 ✔). Sulfur has the highest growth ✔.

| Other base values | Value |
|---|---|
| Base HP | 170 |
| Base attack damage | 20 |
| Base DEF / RES | 1 / 2 |
| Base mana | 100 |

**Derived** (GDD §6.9 rates incl. Resonance, no gear):
| Stat | Lv. 1 | Lv. 30 |
|---|---|---|
| HP / HP regen | 490 / 1.6 per s | 1,534 / 6.8 per s |
| Mana / mana regen | 390 / 1.21 per s | 1,386 / 5.36 per s |
| Attack damage | 42 | 117 |
| DEF (reduction) | 2.8 (14%) | 8.0 (32%) |
| RES (reduction) | 5.6 (25%) | 18.1 (52%) |
| Attacks per second | 0.62 | 0.82 |

## 5. Skill Tree
Skill points: 1 per hero level, spent on any open skill. Every skill has 5 levels; a skill's level can't exceed hero level ÷ 2, rounded up. Core skills are all open from Lv. 1; the branch opens at **hero Lv. 10** with all 3 of its skills open (GDD §4.6.4). Core + one branch = 6 × 5 = 30 points, all spent at Lv. 30. Statuses: GDD §6.10. Zones: GDD §6.13. Holy / Dark: GDD §6.9.

**Core** — the halo: heal, purify, and an aura that steadies the front line.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| A1 | **Minor Mending** | Lv. 1 | 60 / 8 s | Ally with the lowest HP % | Heals 100 / 160 / 220 / 280 / 340 |
| A2 | **Halo Pulse** | Lv. 1 | 90 / 16 s | Allies with harmful statuses; front-most enemy row | Her halo flares. Purifies 1 / 1 / 2 / 2 / 3 allies (most harmful statuses first): removes all their **harmful** statuses and heals them 40 / 60 / 80 / 100 / 120. **Blinds** the front-most enemy row for 1 / 1.25 / 1.5 / 1.75 / 2 s |
| P0 | **Celestial Resilience** (core passive, aura) | Lv. 1 | — | Allies standing in her side's front row or further forward, Elsie included | +2 / 3 / 4 / 5 / 6 DEF and RES |

**Branch point:** hero Lv. 10. **3 branches**, permanent choice: what battle makes of her. B1 keeps her a Support; B2 makes her a Warrior and B3 a Mage (off-role, weaker core tools than specialists, GDD §6.3).

**B1 · The Seraph** (role: Support; Angel of Renewal & Sanctuary) — her wings finally open, and they multiply as she grows.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B1a | **Seraphic Veil** | Branch (Lv. 10) | 120 / 24 s | Ally with the lowest HP % | Wraps them in giant ethereal wings: **Invulnerable** 1 / 1.25 / 1.5 / 1.75 / 2 s |
| B1b | **Heavenly Canopy** | Branch (Lv. 10) | 140 / 22 s | Zone: 1-tile radius around the lowest-HP ally's position | Starlight beam for 5 s: allies inside heal 40 / 60 / 80 / 100 / 120 per s and take −20 / 25 / 30 / 35 / 40% damage from **ranged** enemies (the burning shots are visual only, GDD §13 #39) |
| B1p | **Grace of the Six Wings** | Branch (Lv. 10) | — | Self; all allies' Shields | Her healing +4 / 8 / 12 / 16 / 20%. Every **Shield** status on her allies, from any source (e.g. Tobin's Pot-Lid Guard and Wall), +4 / 8 / 12 / 16 / 20%; no shield-maker in the party, no effect. Block chance isn't a Shield. Wings: 2 at Lv. 1, 4 at Lv. 3, 6 at Lv. 5 |

**B2 · The Archangel** (role: **Warrior**, off-role; paladin) — she folds her wings away and takes up holy swords for Father. Descent takes her to the front, where she stays.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B2a | **Descent** | Branch (Lv. 10) | 110 / 18 s | Current target and every enemy within 1 tile | Leaps high and crashes down like a meteor next to the target: 120 / 190 / 260 / 330 / 400 **Holy** damage; the shockwave knocks them down: **Stun** 0.5 / 0.6 / 0.7 / 0.8 / 1.0 s. She **stays where she lands** and keeps fighting with basic attacks (her range covers everything; she doesn't walk back) |
| B2b | **Blade of Justice** | Branch (Lv. 10) | 130 / 24 s | All allies | Floating holy swords for 6 s: after each ally's basic attack, a sword strikes the same target for 15 / 22 / 30 / 37 / 45 physical damage |
| B2p | **Righteous Vengeance** | Branch (Lv. 10) | — | Self | Stores 10 / 15 / 20 / 25 / 30% of the damage she takes (after reduction). Her next basic attack triggers a separate **Holy smite** for the stored amount, then the store resets. Store cap: 25% of her max HP. The basic attack itself stays plain Magic |

**B3 · The Fallen** (role: **Mage**, off-role) — battle after battle leaves marks she can no longer hold in. Her wings tear and turn to obsidian; her halo dims; she grows darker. Lore only: the branch is chosen like any other.
| # | Skill | Unlock | Mana / CD | Target / area | Effect (Lv. 1 / 2 / 3 / 4 / 5) |
|---|---|---|---|---|---|
| B3a | **Abyssal Tether** | Branch (Lv. 10) | 100 / 16 s | Current target; ally with the lowest HP % | Links her life force to the enemy for 5 s: 20 / 30 / 40 / 50 / 60 **Dark** damage per s; all damage dealt becomes dark grace that heals the ally with the lowest HP % (re-checked each second), never Elsie herself. Hard control on Elsie breaks the tether (GDD §6.10) |
| B3b | **Condemnation** | Branch (Lv. 10) | 140 / 24 s | Zone: 1-tile radius around the current target's position | Absolute darkness for 4 s: enemies inside are **Blinded** and **Silenced** (pulsed, GDD §6.13) and take 20 / 30 / 40 / 50 / 60 **Dark** (decay) damage per s |
| B3p | **Malice Aura** | Branch (Lv. 10) | — | Enemies inside her zones or linked by her tether | RES −10 / 15 / 20 / 25 / 30% and +5 / 10 / 15 / 20 / 25% damage taken from damage over time |

**Scroll skill tags:** Support, Sustain, Control.

## 6. Equipment
| Slot | Allowed |
|---|---|
| Weapon | Staff, Tome |
| Armor | Any piece |
| Accessory | Any |
| Default weapon | Staff |

## 7. Unique Trait
- Odds: Bronze 70% · Silver 25% · Gold 5%.
- Fitting trait tags: Support, Sustain, Control ([TraitPool.md](../TraitPool.md)).

## 8. Illustrator Brief (draft)
| Field | Value |
|---|---|
| Silhouette & key shapes | A small girl; a round halo, slightly too big and bright; two small wings that droop like wilted petals |
| Palette (3–4 colors) | White, pale gold, soft pink, a touch of flower green |
| Race family base body | Celestial base body, child scale (shared with Half-Angel; Fairy scaled) |
| Weapon held | A short wooden staff with a knitted flower and a ribbon tied on top |
| Card illustration | Sitting on the workbench in a fading glow, knitting a tiny scarf, halo bright, wings drooping; looking up as if at Father |
| Battle views | Front ¾ and back ¾. Back view must read the wings (or their absence in B2) clearly |
| Animations | Idle (halo flickers, wings droop, fiddles with yarn), cast, Minor Mending, Halo Pulse (halo flares), hit, KO (sits down, sniffling), victory (hugs her staff, looks back at Father). Branches: B1 wings open, hover cast; B2 leap + meteor landing, floating swords, fighting stance at the front; B3 darker idle (stands still, head low), tether pull, darkness cast |
| Branch props | B1 wings spread open, 2 → 4 → 6 with Grace of the Six Wings level; B2 wings hidden under a knitted cloak, halo sharpened into a ring of light; B3 tattered obsidian wings, cracked and dimmed halo, the flower on her staff wilted black |
| VFX per skill | Minor Mending: warm sparkles; Halo Pulse: bright flash ring (blinding white on enemies); Celestial Resilience: faint gold glow on front-row allies; Seraphic Veil: giant ghostly wings closing around the ally; Heavenly Canopy: starlight beam over a circle, shots burning up inside; Descent: meteor trail + shockwave ring; Blade of Justice: floating swords following each ally's hit; Righteous Vengeance: halo charging, golden smite; Abyssal Tether: black chain with dark-gold motes flowing to the healed ally; Condemnation: a circle of total darkness; Malice Aura: purple haze on affected enemies |
| SFX / voice notes | Small, sweet voice; "Yes, Father!" on command; humming while idle. B3: quieter, flatter voice |
| References | TBD (moodboard) |
| Avoid | Anything that looks like an existing game's character |
