# Gear — Fuseborn

**Status:** Draft (Tier I for review). Rules: GDD §4.7 (budget §4.7.4, slots §4.7.1, stones §4.7.2, armor pieces §4.7.3). Traits: `TraitPool.md` §4. Lore: junk becomes treasure (Lore.md).

## How to read an entry
| Field | Meaning |
|---|---|
| Data ID | `SO_Gear_<Name>` |
| Slot · piece | Weapon, or Armor · Body / Helmet / Gloves / Boots |
| Family | Weapons only: which homunculi can hold it (GDD §4.7) |
| Tier · GP | Tier and its Gear Point budget (GDD §4.7.4) |
| Recipe | Basic, or the fusion that makes it |
| Fits | Guidance only: which homunculi it suits |
| Stats | Fixed: every copy has them |
| Signature | Fixed special effect (Tier III optional, IV–V always); costs 25–30% of the budget |
| Rolled extras | 30% chance of a gear trait; 0–5 stone slots. Not listed per card |
| Description | 2–3 sentences of flavor for the Codex and card details |
| Codex line | One short line on the card |
| Card art | What the illustrator draws |

---

## Tier I (basic)
All five are basics from chests and drops. Tier I: **3 GP, all in principles**, no signature.

### Sword
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Sword` |
| Slot · Family | Weapon · Sword |
| Tier · GP | I · 3 |
| Recipe | Basic |
| Fits | Salt homunculi (e.g. Tobin) |
| **Stats** | **+3 Salt** |
| Signature | — |

**Description:** Hammered out of a cracked cauldron rim by a guild smith who swore it had always wanted to be a sword. It holds an edge better than it has any right to.
**Codex line:** "Once a cauldron. Now it cuts things. Mostly."
**Card art:** A plain short sword with a curved, slightly dented blade; a faint ring pattern from the old cauldron rim still shows along the flat.

### Bow
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Bow` |
| Slot · Family | Weapon · Bow |
| Tier · GP | I · 3 |
| Recipe | Basic |
| Fits | Mercury homunculi (e.g. Wren) |
| **Stats** | **+3 Mercury** |
| Signature | — |

**Description:** Bent from an old broom handle and strung with sinew from a Runoff that once tried to eat the guild's laundry. Light, quick and a little springy.
**Codex line:** "Still smells faintly of soap."
**Card art:** A simple wooden bow with a few broom bristles still tied near the grip; a pale, slightly glossy string.

### Staff
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Staff` |
| Slot · Family | Weapon · Staff |
| Tier · GP | I · 3 |
| Recipe | Basic |
| Fits | Sulfur homunculi (e.g. Grum, Elsie) |
| **Stats** | **+3 Sulfur** |
| Signature | — |

**Description:** A stirring rod from the guild's biggest alembic, soaked in so many reagents that it hums when held. Sparks gather at the tip when its bearer gets upset.
**Codex line:** "Stirred a thousand brews. Started a few fires."
**Card art:** A long, stained wooden rod with a scorched tip and a small copper band; tiny sparks around the end.

### Iron Mail
| Field | Value |
|---|---|
| Data ID | `SO_Gear_IronMail` |
| Slot · piece | Armor · Body |
| Tier · GP | I · 3 |
| Recipe | Basic |
| Fits | Front-line homunculi; Salt first |
| **Stats** | **+2 Salt, +1 Mercury** (HP, and a little DEF) |
| Signature | — |

**Description:** Rings cut from old copper coils and iron pot handles, riveted together by apprentices on a dare. Heavy, noisy, and surprisingly hard to get through.
**Codex line:** "You'll hear it coming. That's the point."
**Card art:** A mismatched chain shirt: grey iron rings mixed with reddish copper ones, a pot handle still recognizable at the shoulder.

### Cloth Robe
| Field | Value |
|---|---|
| Data ID | `SO_Gear_ClothRobe` |
| Slot · piece | Armor · Body |
| Tier · GP | I · 3 |
| Recipe | Basic |
| Fits | Back-line casters; Sulfur first |
| **Stats** | **+2 Sulfur, +1 Mercury** (mana and RES, a little DEF) |
| Signature | — |

**Description:** A workshop robe stained by a hundred spills. The reagents soaked in so deep that the cloth seems to remember them, and it stays light enough to run in.
**Codex line:** "Rinse in cold water. Never near a flame."
**Card art:** A loose, ankle-length robe in faded cream, covered in colorful stain rings; a rolled-up sleeve and a scorched hem.

**Sanity check:** Sword on a Lv. 1 Tobin (Salt dominant, 24 Salt) gives about +66 HP, +0.3 HP regen and +3 attack damage: about +13% of his Salt, close to a Dota early item.

---

## Tier II (to do)
11 cards (GDD §15.7). Budget 6 GP: at least half in principles, plus 1 bonus stat.

## Tier III (to do)
11 cards (GDD §15.7). Budget 10 GP; signature optional (War Drum's aura and Thorn Plate's thorns are likely candidates).

## Named legendaries (future, Tier IV–V)
Folklore weapons and armor discovered through fusion, each with a signature. Idea: **Balmung** (Nibelungenlied), signature *Dragon-Slayer*: +30% damage vs Draconic (needs families as combat tags, GDD §13 #42).
