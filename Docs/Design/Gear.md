# Gear — Fuseborn

**Status:** Draft (Tier I and II for review). Rules: GDD §4.7 (budget §4.7.4, visuals §4.7.5, slots §4.7.1, stones §4.7.2, armor pieces §4.7.3). Traits: `TraitPool.md` §4. Lore: junk becomes treasure (Lore.md).

> ⚠️ **Missing weapon families (GDD §13 #44):** **Knife** (Snick's Trapmaster) and **Bomb** (Snick's Goblin Sapper, melee) have **no cards yet**. Until they're created (Tier III or higher), those branches fight with their default weapon only. Plan: **Bomb family property: thrown, +1 range** (GDD §6.2), so the Sapper lobs from 2 tiles.

## How to read an entry
| Field | Meaning |
|---|---|
| Data ID | `SO_Gear_<Name>` |
| Slot · family / piece | Weapon (with its family: which homunculi can hold it, GDD §4.7), or Armor · Body / Helmet / Gloves / Boots |
| Tier · GP | Tier and its Gear Point budget (GDD §4.7.4) |
| Recipe | Basic, or the fusion that makes it |
| Fits | Guidance only: which homunculi it suits |
| Stats | Fixed: every copy has them |
| Signature | Fixed special effect (Tier III optional, IV–V always); costs 25–30% of the budget |
| Skill | Fixed active skill (from Tier II, GDD §4.7.6); costs 30% of the budget. A card with a skill has **no** signature and **never** rolls a trait |
| Rolled extras | 30% chance of a gear trait (Faint / Bright / Radiant / Unique; not on skill cards); 0–5 stone slots. Not listed per card |
| Description | 2–3 sentences of flavor for the Codex and card details |
| Codex line | One short line on the card |
| Card art | What the illustrator draws on the card |
| Equipped look | Weapons: how it looks in the homunculus's hand. Armor: not shown (GDD §4.7.5) |
| Attack effect / Hit sound | Weapons: the basic-attack effect and sound. Armor: the sound when the wearer is hit |

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
**Equipped look:** Held in the main hand, blade a little short for the hilt; the cauldron-ring pattern catches the light on swings.
**Attack effect:** Short grey arc trail; small orange sparks on impact. SFX: a dull clunk with a faint cauldron ring.

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
**Equipped look:** Held in the off-hand; a few bristles sway near the grip when she moves.
**Attack effect:** Thin arrow streak with a faint soap-bubble shimmer; a soft thud and a tiny bubble pop on impact. SFX: a springy twang.

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
**Equipped look:** Held upright in the main hand; a few sparks drift from the scorched tip while idle.
**Attack effect:** A small ember bolt flies from the tip; a pop of sparks on impact. SFX: fizz and crackle.

### Iron Mail
| Field | Value |
|---|---|
| Data ID | `SO_Gear_IronMail` |
| Slot · piece | Armor · Body |
| Tier · GP | I · 3 |
| Recipe | Basic |
| Fits | Front-line homunculi; Salt first |
| **Stats** | **+2 Salt, +1 Mercury (HP, and a little DEF)** |
| Signature | — |

**Description:** Rings cut from old copper coils and iron pot handles, riveted together by apprentices on a dare. Heavy, noisy, and surprisingly hard to get through.
**Codex line:** "You'll hear it coming. That's the point."
**Card art:** A mismatched chain shirt: grey iron rings mixed with reddish copper ones, a pot handle still recognizable at the shoulder.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A clank of pots and pans.

### Cloth Robe
| Field | Value |
|---|---|
| Data ID | `SO_Gear_ClothRobe` |
| Slot · piece | Armor · Body |
| Tier · GP | I · 3 |
| Recipe | Basic |
| Fits | Back-line casters; Sulfur first |
| **Stats** | **+2 Sulfur, +1 Mercury (mana and RES, a little DEF)** |
| Signature | — |

**Description:** A workshop robe stained by a hundred spills. The reagents soaked in so deep that the cloth seems to remember them, and it stays light enough to run in.
**Codex line:** "Rinse in cold water. Never near a flame."
**Card art:** A loose, ankle-length robe in faded cream, covered in colorful stain rings; a rolled-up sleeve and a scorched hem.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A soft cloth thump.

**Sanity check:** Sword on a Lv. 1 Tobin (Salt dominant, 24 Salt) gives about +66 HP, +0.3 HP regen and +3 attack damage: about +13% of his Salt, close to a Dota early item.

---

## Tier II
11 cards from two basics (GDD §15.7). Tier II: **6 GP**, at least half in principles, plus 1 bonus stat; no signature. All 11 are plain for now; some may get a fixed skill later (GDD §4.7.6).

### Greatsword
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Greatsword` |
| Slot · Family | Weapon · Sword |
| Tier · GP | II · 6 |
| Recipe | Sword + Sword |
| Fits | Salt front-liners (Warrior builds) |
| **Stats** | **+4 Salt, +2 ATK** |
| Signature | — |

**Description:** Two cauldron-rim swords hammered into one long blade, the seam still visible down the middle. It's slow to swing and very hard to stop once it's moving.
**Codex line:** "Two bad swords make one good one. Heavier, though."
**Card art:** A long, broad blade with a visible hammered seam down its center and a wide crossguard bent from a pot rim.
**Equipped look:** Held two-handed, or resting on the shoulder while idle; noticeably large next to small homunculi.
**Attack effect:** Wide, heavy grey arc; a burst of sparks and a small dust puff on impact. SFX: a deep whoosh and a heavy clang.

### Crossbow
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Crossbow` |
| Slot · Family | Weapon · Bow |
| Tier · GP | II · 6 |
| Recipe | Bow + Bow |
| Fits | Mercury ranged homunculi |
| **Stats** | **+4 Mercury, +2 ATK** |
| Signature | — |

**Description:** Two broom-handle bows bolted crosswise onto a stock, with a coiled spring from a broken workshop door doing the pulling. Every shot jolts the shooter.
**Codex line:** "Two broom handles, one very angry spring."
**Card art:** A chunky crossbow: two broom-handle limbs, a visible coiled spring, a short iron bolt loaded.
**Equipped look:** Held at the hip with both hands; the spring visibly recoils after each shot.
**Attack effect:** Fast, straight bolt streak (straighter and quicker than the Bow); a sharp snap on impact. SFX: a loud clack and spring boing.

### Grimoire
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Grimoire` |
| Slot · Family | Weapon · Tome |
| Tier · GP | II · 6 |
| Recipe | Staff + Staff |
| Fits | Sulfur casters |
| **Stats** | **+4 Sulfur, +2% Skill Power** |
| Signature | — |

**Description:** Two stirring rods' worth of soaked-in reagent notes, pressed into pages and bound with copper. The ink still moves when nobody is looking.
**Codex line:** "It reads you back."
**Card art:** A thick book bound with copper corners; faint glyphs crawling across the open pages.
**Equipped look:** Held open in the off-hand, pages fluttering; it floats a few centimeters above the palm when casting.
**Attack effect:** A small ink-purple glyph bolt; the glyph splashes like ink on impact. SFX: a quick page flip and a faint whisper.

### Twin Daggers
| Field | Value |
|---|---|
| Data ID | `SO_Gear_TwinDaggers` |
| Slot · Family | Weapon · Dagger |
| Tier · GP | II · 6 |
| Recipe | Sword + Bow |
| Fits | Mercury melee (Assassin builds) |
| **Stats** | **+3 Mercury, +1.5% Crit Chance** |
| Signature | — |

**Description:** A cauldron-rim sword split in two and sharpened twice, with the bow's springy sinew wound into the grips. Thrown or dropped, they seem to bounce back to the hand.
**Codex line:** "A sword split in half, sharpened twice."
**Card art:** Two short, matching blades crossed; sinew-wrapped grips with a little spring coil at each pommel.
**Equipped look:** One in each hand, held in reverse grip.
**Attack effect:** Two quick slashes forming an X trail; tiny paired sparks. SFX: a double snick.

### Tower Shield
| Field | Value |
|---|---|
| Data ID | `SO_Gear_TowerShield` |
| Slot · Family | Weapon · Shield |
| Tier · GP | II · 6 |
| Recipe | Sword + Iron Mail |
| Fits | Tanks (e.g. Tobin) |
| **Stats** | **+3 Salt, +0.9 DEF**. Shield family property: **+4% Block** (Tier II); the wearer counts as a shield bearer (GDD §6.9) |
| Signature | — |

**Description:** A workshop door, reinforced with the chain mail's rings and given a sword-hilt handle. It doesn't look like much until something tries to get through it.
**Codex line:** "A door with a handle. Hide behind it."
**Card art:** A tall rectangular shield that is clearly an old door: hinges, a keyhole, chain rings riveted across it.
**Equipped look:** Off-hand, replacing fixed hand props (Tobin's pot lid); the main hand shows the default weapon.
**Attack effect:** Basic hit is a shield shove: a short forward push with a dust puff. SFX: a heavy wooden thump.

### Lute
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Lute` |
| Slot · Family | Weapon · Instrument |
| Tier · GP | II · 6 |
| Recipe | Bow + Staff |
| Fits | Sulfur supports |
| **Stats** | **+4 Sulfur, +30 mana** |
| Signature | — |

**Description:** The stirring rod bent into a neck, the broom-bow's sinew restrung as strings. It plays in tune, mostly, and sparks a little on the high notes.
**Codex line:** "The bowstring still twangs when it's nervous."
**Card art:** A small round lute with a scorched wooden neck, sinew strings and a copper band near the head.
**Equipped look:** Held across the body and strummed; small sparks on the strings while playing.
**Attack effect:** A ripple of music-note shapes travels to the target; a soft chime on impact. SFX: a short twangy chord.

### Plate Armor
| Field | Value |
|---|---|
| Data ID | `SO_Gear_PlateArmor` |
| Slot · piece | Armor · Body |
| Tier · GP | II · 6 |
| Recipe | Iron Mail + Iron Mail |
| Fits | Tanks; Salt first |
| **Stats** | **+3 Salt, +0.9 DEF** |
| Signature | — |

**Description:** Two chain shirts melted down and beaten into plates: every pot in the guild kitchen gave its life for this. It's heavy, but it finally stopped clanking.
**Codex line:** "Twice the pots, half the noise."
**Card art:** A dented breastplate made of riveted pot bottoms; one still has a handle stub.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A deep gong-like clang.

### Shadow Cloak
| Field | Value |
|---|---|
| Data ID | `SO_Gear_ShadowCloak` |
| Slot · piece | Armor · Body |
| Tier · GP | II · 6 |
| Recipe | Bow + Cloth Robe |
| Fits | Mercury melee (evasion) |
| **Stats** | **+3 Mercury, +1.2% Evasion** |
| Signature | — |

**Description:** The workshop robe, soaked in the oily dye of the Runoff sinew until it drinks the light around it. Hard to see, harder to grab.
**Codex line:** "Dyed in a spill nobody could see."
**Card art:** A dark, hooded cloak whose edges fade into shadow; a faint oily sheen.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A soft rustle.

### Sage Robe
| Field | Value |
|---|---|
| Data ID | `SO_Gear_SageRobe` |
| Slot · piece | Armor · Body |
| Tier · GP | II · 6 |
| Recipe | Staff + Cloth Robe |
| Fits | Sulfur casters |
| **Stats** | **+4 Sulfur, +0.6 RES** |
| Signature | — |

**Description:** A robe stitched from cloth and the stirring rod's reagent-soaked wrappings. Every stain on it is a lesson someone learned the hard way.
**Codex line:** "Every stain is a lesson."
**Card art:** A long scholar's robe in deep blue, embroidered with stain-shaped patterns and copper thread.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A papery flutter.

### Rune Mail
| Field | Value |
|---|---|
| Data ID | `SO_Gear_RuneMail` |
| Slot · piece | Armor · Body |
| Tier · GP | II · 6 |
| Recipe | Staff + Iron Mail |
| Fits | Salt + Sulfur hybrids |
| **Stats** | **+2 Salt, +2 Sulfur, +0.6 DEF** |
| Signature | — |

**Description:** Chain mail whose rings were each dipped in the alembic before riveting. The rings hum when a spell comes close, as if they recognize it.
**Codex line:** "The rings hum when spells come near."
**Card art:** A chain shirt with faintly glowing runes etched into some of the rings.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A metallic clink with a faint humming chime.

### Leather Armor
| Field | Value |
|---|---|
| Data ID | `SO_Gear_LeatherArmor` |
| Slot · piece | Armor · Body |
| Tier · GP | II · 6 |
| Recipe | Iron Mail + Cloth Robe |
| Fits | Mercury ranged and skirmishers |
| **Stats** | **+4 Mercury, +10 Move Speed** |
| Signature | — |

**Description:** The robe's cloth layered and boiled hard, with a few chain rings kept at the shoulders. Lighter than mail, tougher than cloth, and it doesn't make a sound.
**Codex line:** "Lighter than mail, tougher than cloth."
**Card art:** A fitted brown jerkin of hardened layers with a few chain rings at the shoulders.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A leathery creak.

---

## Tier III (to do)
11 cards (GDD §15.7). Budget 10 GP; signature optional (War Drum's aura and Thorn Plate's thorns are likely candidates).

## Named cards (future, Tier IV+)
Folklore weapons and armor discovered through fusion, each with a fixed signature (GDD §4.7.4). No rarity label in game: the name says it. One of each per party. Very high tiers may also give the homunculus a visible **aura** (GDD §4.7.5). Recipes come when those tiers are designed.

| Card | Slot | Legend | Signature idea |
|---|---|---|---|
| **Balmung** | Weapon · Sword | Nibelungenlied: Siegfried's sword | *Dragon-Slayer:* +30% damage vs Draconic (needs families as combat tags, GDD §13 #42) |
| **Tarnhelm** | Armor · Helmet | Nibelung saga: the helm of invisibility, shape-shifting and instant travel | **To decide** (Stealth at battle start now belongs to the Ring of Gyges). Ideas: *shape-shift* (first 5 s, enemies treat the wearer as their lowest-priority target) or *instant travel* (once, at battle start, teleports to a tile chosen during placement). Part of a **Nibelung set** with Balmung and Andvaranaut (`Items.md`) |
