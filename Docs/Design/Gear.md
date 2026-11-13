# Gear — Fuseborn

**Status:** Draft (Tier I–III approved; Tier IV for review). Rules: GDD §4.7 (budget §4.7.4, visuals §4.7.5, slots §4.7.1, stones §4.7.2, armor pieces §4.7.3). Traits: `TraitPool.md` §4. Lore: junk becomes treasure (Lore.md).

> ✅ **Knife** (Black Knife) and **Bomb** (Grenade) families now have cards (Tier IV, Early), so every branch of Snick has a weapon.

> ⏳ **Accuracy** (GDD §6.9) has no gear cards yet. Permanent Evasion is only ~5–6% today, so Accuracy gear would be worthless. Plan (GDD §13 #46): in **Tier V**, design stronger Evasion gear together with **one Accuracy glove and one Accuracy bow** as a counter-pair. Existing gloves and bows stay unchanged.

## How to read an entry
| Field | Meaning |
|---|---|
| Data ID | `SO_Gear_<Name>` |
| Slot · family / piece | Weapon (with its family: which homunculi can hold it, GDD §4.7), or Armor · Body / Helmet / Gloves / Boots |
| Tier · Band · GP | Tier (batch and recipe depth only), **power band**, and its Gear Point budget. The band sets the **level requirement** (GDD §4.7.4) |
| Recipe | Basic, or the fusion that makes it |
| Fits | Guidance only: which homunculi it suits |
| Stats | Fixed: every copy has them |
| Signature | Fixed special effect (Tier III optional, IV–V always); costs 25–30% of the budget |
| Skill | Fixed active skill (from the Early band, GDD §4.7.6); costs 30% of the budget. A card with a skill has **no** signature and **never** rolls a trait |
| Rolled extras | 30% chance of a gear trait (Faint / Bright / Radiant / Unique; not on skill cards); 0–5 stone slots. Not listed per card |
| Description | 2–3 sentences of flavor for the Codex and card details |
| Codex line | One short line on the card |
| Card art | What the illustrator draws on the card |
| Equipped look | Weapons: how it looks in the homunculus's hand. Armor: not shown (GDD §4.7.5) |
| Attack effect / Hit sound | Weapons: the basic-attack effect and sound. Armor: the sound when the wearer is hit |

---

## Tier I (basic)
All five are basics from chests and drops. **Starter band:** 3 GP, all in principles, no signature, no level requirement.

### Sword
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Sword` |
| Slot · Family | Weapon · Sword |
| Tier · Band · GP | I · Starter · 3 (no level requirement) |
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
| Tier · Band · GP | I · Starter · 3 (no level requirement) |
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
| Tier · Band · GP | I · Starter · 3 (no level requirement) |
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
| Tier · Band · GP | I · Starter · 3 (no level requirement) |
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
| Tier · Band · GP | I · Starter · 3 (no level requirement) |
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
11 cards from two basics (GDD §15.7). **Early band:** 6 GP, at least half in principles, plus 1 bonus stat; no signature; no level requirement. All 11 are plain for now; some may get a fixed skill later (GDD §4.7.6).

### Greatsword
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Greatsword` |
| Slot · Family | Weapon · Sword |
| Tier · Band · GP | II · Early · 6 (no level requirement) |
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
| Tier · Band · GP | II · Early · 6 (no level requirement) |
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
| Tier · Band · GP | II · Early · 6 (no level requirement) |
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
| Tier · Band · GP | II · Early · 6 (no level requirement) |
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
| Tier · Band · GP | II · Early · 6 (no level requirement) |
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
| Tier · Band · GP | II · Early · 6 (no level requirement) |
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
| Tier · Band · GP | II · Early · 6 (no level requirement) |
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
| Tier · Band · GP | II · Early · 6 (no level requirement) |
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
| Tier · Band · GP | II · Early · 6 (no level requirement) |
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
| Tier · Band · GP | II · Early · 6 (no level requirement) |
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
| Tier · Band · GP | II · Early · 6 (no level requirement) |
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

## Tier III
11 cards from a Tier II + a Tier I gear (GDD §15.7). Bands: **6 Early** (new helmets, gloves and boots: sideways choices next to body armor), **4 Mid** (weapon upgrades and heavy body armor, require Lv. 10), **1 Late** (War Drum, requires Lv. 20). Extras: **3 gear skills** (Iron Gauntlets, Silent Boots, Arcane Repeater: such cards never roll a trait), **3 signatures** (Runeblade, Thorn Plate, War Drum), 5 plain.

### Iron Gauntlets
| Field | Value |
|---|---|
| Data ID | `SO_Gear_IronGauntlets` |
| Slot · piece | Armor · Gloves |
| Tier · Band · GP | III · Early · 6 (no level requirement) |
| Recipe | Greatsword (II) + Iron Mail (I) |
| Fits | Salt front-liners (Warrior builds) |
| **Stats** | **+3 Salt, +1 ATK (4 GP after the skill)** |
| Signature | — |
| Skill | **Haymaker** (60 mana / 12 s): a heavy punch to the current target: 80 physical damage + **Knockback** 1 tile |

**Description:** The Greatsword's spare steel, folded around two chain-mail sleeves and riveted into heavy fists. They make every handshake a small threat.
**Codex line:** "Knock first, ask later."
**Card art:** A pair of chunky iron gauntlets with riveted knuckle plates and chain links at the wrists.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A dull metallic clank.
**Skill effect:** Haymaker: the fist glows briefly, a wide punch with a shockwave ring; the target slides back. SFX: a heavy thud.

### Wizard Hat
| Field | Value |
|---|---|
| Data ID | `SO_Gear_WizardHat` |
| Slot · piece | Armor · Helmet |
| Tier · Band · GP | III · Early · 6 (no level requirement) |
| Recipe | Grimoire (II) + Cloth Robe (I) |
| Fits | Sulfur casters |
| **Stats** | **+3 Sulfur, +1.5% Cooldown Reduction** |
| Signature | — |
| Skill | — |

**Description:** A Grimoire's loose pages stitched into the lining of a tall, stained workshop hat. Ideas come faster under it, mostly because the pages whisper them.
**Codex line:** "The point helps you think."
**Card art:** A tall, floppy pointed hat in faded blue, with paper scraps peeking out of the brim.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A soft papery rustle.

### Silent Boots
| Field | Value |
|---|---|
| Data ID | `SO_Gear_SilentBoots` |
| Slot · piece | Armor · Boots |
| Tier · Band · GP | III · Early · 6 (no level requirement) |
| Recipe | Twin Daggers (II) + Cloth Robe (I) |
| Fits | Mercury melee (Assassin builds) |
| **Stats** | **+3 Mercury, +5 Move Speed (4 GP after the skill)** |
| Signature | — |
| Skill | **Shadowstep** (40 mana / 14 s): blinks up to 2 tiles toward its target or away from danger, then +15% Evasion for 2 s |

**Description:** Soft cloth wrapped tight around the Twin Daggers' springy sinew, so every step lands and lifts without a sound. Their owners are always somewhere else.
**Codex line:** "Not a sound. Not a trace."
**Card art:** A pair of dark, wrapped cloth boots with thin sinew bindings up the calves.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** Almost no sound: a faint whisper of cloth.
**Skill effect:** Shadowstep: a puff of shadow where the wearer stood, a faint afterimage, then it reappears. SFX: a soft whoosh.

### Knight Helm
| Field | Value |
|---|---|
| Data ID | `SO_Gear_KnightHelm` |
| Slot · piece | Armor · Helmet |
| Tier · Band · GP | III · Early · 6 (no level requirement) |
| Recipe | Tower Shield (II) + Sword (I) |
| Fits | Tanks; Salt first |
| **Stats** | **+3 Salt, +3% Control Resist** |
| Signature | — |
| Skill | — |

**Description:** A corner cut from the Tower Shield's old door, hammered into a helm and crested with a cauldron-rim blade. Hard to shake, harder to knock over.
**Codex line:** "Keeps your head on straight."
**Card art:** A rounded helmet with a visor slit, an old keyhole still visible on one side, and a short metal crest.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A hollow wooden-metal bonk.

### Nightgrip Gloves
| Field | Value |
|---|---|
| Data ID | `SO_Gear_NightgripGloves` |
| Slot · piece | Armor · Gloves |
| Tier · Band · GP | III · Early · 6 (no level requirement) |
| Recipe | Shadow Cloak (II) + Bow (I) |
| Fits | Mercury attackers (crit builds) |
| **Stats** | **+3 Mercury, +1.5% Crit Chance** |
| Signature | — |
| Skill | — |

**Description:** Cut from the light-drinking Shadow Cloak and strung with broom-bow sinew at the fingers. The wearer's hand always seems to find the weak spot first.
**Codex line:** "They find the gap in the armor."
**Card art:** Thin black gloves with an oily sheen and sinew lines along each finger.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A soft leathery slap.

### Hunter's Boots
| Field | Value |
|---|---|
| Data ID | `SO_Gear_HuntersBoots` |
| Slot · piece | Armor · Boots |
| Tier · Band · GP | III · Early · 6 (no level requirement) |
| Recipe | Leather Armor (II) + Bow (I) |
| Fits | Mercury ranged and skirmishers |
| **Stats** | **+4 Mercury, +10 Move Speed** |
| Signature | — |
| Skill | — |

**Description:** Hardened leather boots with the broom-bow's springy limb set into the soles. They put a little bounce in every step, and a lot in every chase.
**Codex line:** "Always one step ahead."
**Card art:** Brown, laced leather boots with a curved wooden strip visible in each sole.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A leathery creak.

### Arcane Repeater
| Field | Value |
|---|---|
| Data ID | `SO_Gear_ArcaneRepeater` |
| Slot · Family | Weapon · Bow |
| Tier · Band · GP | III · Mid · 10 (requires Lv. 10) |
| Recipe | Crossbow (II) + Staff (I) |
| Fits | Mercury ranged (e.g. Wren) |
| **Stats** | **+4 Mercury, +3 ATK (7 GP after the skill)** |
| Signature | — |
| Skill | **Rapid Volley** (70 mana / 14 s): fires 3 quick bolts at the current target, 45 physical damage each |

**Description:** The Crossbow's angry spring, wound by the stirring rod's leftover magic so it re-cocks itself. It fires as fast as its holder can aim.
**Codex line:** "The spring winds itself now."
**Card art:** A sleek crossbow with a glowing copper coil and faint sparks along the rail.
**Equipped look:** Held at the hip with both hands; the coil glows and turns after every shot.
**Attack effect:** Fast bolt streaks with a faint violet spark trail; a sharp snap on impact. SFX: a quick clack and a magical whir. Rapid Volley: three bolts in a tight burst, the coil spinning hard.

### Elder Staff
| Field | Value |
|---|---|
| Data ID | `SO_Gear_ElderStaff` |
| Slot · Family | Weapon · Staff |
| Tier · Band · GP | III · Mid · 10 (requires Lv. 10) |
| Recipe | Sage Robe (II) + Staff (I) |
| Fits | Sulfur casters (e.g. Grum, Elsie) |
| **Stats** | **+6 Sulfur, +4% Skill Power** |
| Signature | — |
| Skill | — |

**Description:** A stirring rod wrapped in the Sage Robe's lesson-stained cloth until it grew heavy with knowledge. Older than the guild, the apprentices say, though it was made last spring.
**Codex line:** "Older than the guild. Wiser too."
**Card art:** A tall, gnarled staff wrapped in blue cloth strips, a small glowing crystal knot at the top.
**Equipped look:** Held upright in the main hand; the crystal knot glows softly while idle.
**Attack effect:** A brighter, steadier bolt than the Staff's (a blue-white orb with a cloth-ribbon trail); a soft burst on impact. SFX: a low hum and a chime.

### Runeblade
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Runeblade` |
| Slot · Family | Weapon · Sword |
| Tier · Band · GP | III · Mid · 10 (requires Lv. 10) |
| Recipe | Rune Mail (II) + Iron Mail (I) |
| Fits | Salt + Sulfur hybrids (Warrior builds that cast) |
| **Stats** | **+4 Salt, +3 Sulfur (7 GP after the signature)** |
| Signature | **Spellstrike:** after the wearer casts a skill, its next basic hit deals **+40 magic damage** |
| Skill | — |

**Description:** Rune Mail's humming rings melted and forged into a blade, with fresh iron to give it weight. The runes wake whenever its bearer casts, and the next swing carries the spell.
**Codex line:** "Steel that remembers the spell."
**Card art:** A straight sword with faintly glowing runes along the blade and a ring-wrapped hilt.
**Equipped look:** Held in the main hand; runes flicker along the blade, brightening after a skill.
**Attack effect:** A clean silver arc trail; runes flash on impact. Spellstrike: the next swing leaves a blue rune trail and a magic burst. SFX: a ring of steel; a chime on Spellstrike.

### Thorn Plate
| Field | Value |
|---|---|
| Data ID | `SO_Gear_ThornPlate` |
| Slot · piece | Armor · Body |
| Tier · Band · GP | III · Mid · 10 (requires Lv. 10) |
| Recipe | Plate Armor (II) + Sword (I) |
| Fits | Tanks; Salt first |
| **Stats** | **+4 Salt, +3% Thorns (7 GP after the signature)** |
| Signature | **Barbs:** melee attackers that hit the wearer get **Bleed 2 s** (20 per s), once per 5 s per attacker |
| Skill | — |

**Description:** Pot-bottom plates bristling with sword shards, welded point-out. Anyone who gets close enough to hit it learns to regret it.
**Codex line:** "Hug it. We dare you."
**Card art:** A heavy breastplate covered in short, jagged blade shards, like a metal hedgehog.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A clang with a sharp metallic scrape (Barbs: a small red spark on the attacker).

### War Drum
| Field | Value |
|---|---|
| Data ID | `SO_Gear_WarDrum` |
| Slot · Family | Weapon · Instrument |
| Tier · Band · GP | III · Late · 16 (requires Lv. 20) |
| Recipe | Lute (II) + Iron Mail (I) |
| Fits | Supports and front-row leaders |
| **Stats** | **+6 Sulfur, +6 Mercury (12 GP after the signature)** |
| Signature | **Marching Beat:** allies in the wearer's **row** get **+15 Attack Speed** (two War Drums on one row count once) |
| Skill | — |

**Description:** The Lute's body stretched with leather and ringed with iron, beaten until it boomed. When it plays, everyone nearby falls into step, even the ones who swear they can't dance.
**Codex line:** "Everyone marches to its beat."
**Card art:** A round iron-banded drum with a leather head and two knobbly drumsticks.
**Equipped look:** Hung at the hip and struck with a stick in the main hand.
**Attack effect:** Basic hit: a booming beat sends a ring-shaped sound wave to the target; a dull thump on impact. Marching Beat: small pulsing rings around allies in its row. SFX: a deep drum boom.

## Tier IV
22 cards: 12 from a Tier III + a Tier I gear, 8 from a Tier III + a Tier II, and 2 self pairs (a Tier III with itself). Bands: **6 Early, 9 Mid, 5 Late, 2 Peak**. Extras: **5 gear skills** (Viper Fangs, Battle Horn, Siren Harp, Shadowfang, Spellbrand; never roll a trait), **8 signatures** (Longbow, Siege Crossbow, Warblade, Fortress Plate, Castle Wall, and the named cards **Tarnhelm**, **Hagoromo of the Sky Kami**, **Balmung**), 9 plain. Every Tier III card has at least one use here; 8 of the 11 Tier II cards get a second use. The **Knife** (Black Knife) and **Bomb** (Grenade) families arrive here.

### Black Knife
| Field | Value |
|---|---|
| Data ID | `SO_Gear_BlackKnife` |
| Slot · Family | Weapon · Knife |
| Tier · Band · GP | IV · Early · 6 (no level requirement) |
| Recipe | Nightgrip Gloves (III) + Sword (I) |
| Fits | Snick's Trapmaster (Knife family); quick melee |
| **Stats** | **+3 Mercury, +3 ATK** |
| Signature | — |
| Skill | — |

**Description:** A cauldron-rim blade blackened in the Nightgrip Gloves' oily dye and bent into a hook at the tip. Made for cutting wire, setting snares and leaving before anyone notices.
**Codex line:** "Cuts the rope. Or the hand on it."
**Card art:** A short, hooked black knife with a coil of thin wire wrapped around the grip.
**Equipped look:** Held low in the main hand, hook forward; the wire coil glints on the grip.
**Attack effect:** A quick hooked slash leaving a thin dark trail; a small snag spark on impact. SFX: a sharp zip.

### Grenade
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Grenade` |
| Slot · Family | Weapon · Bomb |
| Tier · Band · GP | IV · Early · 6 (no level requirement) |
| Recipe | Iron Gauntlets (III) + Staff (I) |
| Fits | Snick's Goblin Sapper (Bomb family) |
| **Stats** | **+4 Mercury, +2 ATK. Bomb family property: **thrown, +1 range** (still melee for every other rule)** |
| Signature | — |
| Skill | — |

**Description:** An iron fist-casing from the Gauntlets, packed tight around the stirring rod's spark-soaked tip. Its owner always seems to have one more in a pocket.
**Codex line:** "Pull, count, throw. Mostly in that order."
**Card art:** A round, riveted iron grenade with a short sputtering fuse.
**Equipped look:** A grenade held ready in the main hand, fuse fizzing; a few more on a belt.
**Attack effect:** Basic hit: lobs a grenade from 2 tiles; a small smoky blast on impact. SFX: a fuse hiss and a pop-boom.

### Viper Fangs
| Field | Value |
|---|---|
| Data ID | `SO_Gear_ViperFangs` |
| Slot · Family | Weapon · Dagger |
| Tier · Band · GP | IV · Early · 6 (no level requirement) |
| Recipe | Silent Boots (III) + Sword (I) |
| Fits | Mercury melee (Assassin builds) |
| **Stats** | **+3 Mercury, +0.5% Crit (4 GP after the skill)** |
| Signature | — |
| Skill | **Venomous Strike** (50 mana / 12 s): the next basic hit deals +40 physical damage and **Bleed 3 s** (15 per s) that **ignores DEF** |

**Description:** Two thin blades forged from a split sword and grooved like snake fangs; the boots' soft wraps became their grips. A drop of something green always seems to be on the tip.
**Codex line:** "Two bites. One regret."
**Card art:** A pair of slim, curved daggers with green-tinted grooves along the blades.
**Equipped look:** One in each hand, reverse grip, a faint green drip at the tips.
**Attack effect:** Two fast slashes with a thin green trail. SFX: a double hiss.
**Skill / signature effect:** Venomous Strike: the blades glow green, the hit leaves a green splash and dripping venom ticks. SFX: a wet hiss.

### Swiftwind Boots
| Field | Value |
|---|---|
| Data ID | `SO_Gear_SwiftwindBoots` |
| Slot · piece | Armor · Boots |
| Tier · Band · GP | IV · Early · 6 (no level requirement) |
| Recipe | Hunter's Boots (III) + Cloth Robe (I) |
| Fits | Mercury skirmishers and ranged |
| **Stats** | **+3 Mercury, +15 Move Speed** |
| Signature | — |
| Skill | — |

**Description:** Hunter's Boots lined with the robe's light cloth, so loose and airy that wind runs through them. Wearers swear the breeze pushes them along.
**Codex line:** "The wind wears them too."
**Card art:** Light boots with fluttering cloth tails at the ankles and a faint swirl of wind around them.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A soft whoosh.

### Ranger's Hood
| Field | Value |
|---|---|
| Data ID | `SO_Gear_RangersHood` |
| Slot · piece | Armor · Helmet |
| Tier · Band · GP | IV · Early · 6 (no level requirement) |
| Recipe | Arcane Repeater (III) + Cloth Robe (I) |
| Fits | Mercury ranged (e.g. Wren) |
| **Stats** | **+3 Mercury, +4.5 Attack Speed** |
| Signature | — |
| Skill | — |

**Description:** A deep cloth hood with a spare copper coil from the Arcane Repeater sewn into the brim. It keeps the rain out and the aim steady.
**Codex line:** "See them first."
**Card art:** A dark green hood with a small copper coil glinting at the brim.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A muffled cloth thump.

### Phantom Cloak
| Field | Value |
|---|---|
| Data ID | `SO_Gear_PhantomCloak` |
| Slot · piece | Armor · Body |
| Tier · Band · GP | IV · Early · 6 (no level requirement) |
| Recipe | Silent Boots (III) + Shadow Cloak (II) |
| Fits | Mercury melee (evasion) |
| **Stats** | **+4 Mercury, +0.8% Evasion** |
| Signature | — |
| Skill | — |

**Description:** The Shadow Cloak, hemmed with the Silent Boots' soundless wraps. It doesn't just drink the light now; it forgets where its wearer was a moment ago.
**Codex line:** "Was it ever there?"
**Card art:** A long, ragged grey-black cloak whose edges fade into mist.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** Barely anything: a faint rustle.

### Bastion Shield
| Field | Value |
|---|---|
| Data ID | `SO_Gear_BastionShield` |
| Slot · Family | Weapon · Shield |
| Tier · Band · GP | IV · Mid · 10 (requires Lv. 10) |
| Recipe | Knight Helm (III) + Iron Mail (I) |
| Fits | Tanks (e.g. Tobin) |
| **Stats** | **+6 Salt, +1.2 DEF. Shield family: **Block 6%** (Mid)** |
| Signature | — |
| Skill | — |

**Description:** The Knight Helm's door-wood, widened with sheets of chain mail into a proper shield. Heavy, square and very stubborn.
**Codex line:** "Hold the line. It holds you."
**Card art:** A broad, square shield of dark wood banded with chain mail, a small helm crest on the boss.
**Equipped look:** Off-hand, replacing fixed hand props (Tobin's pot lid); the main hand shows the default weapon.
**Attack effect:** Basic hit: a hard shield shove with a dust puff. SFX: a heavy wooden thud.

### Tome of Ages
| Field | Value |
|---|---|
| Data ID | `SO_Gear_TomeOfAges` |
| Slot · Family | Weapon · Tome |
| Tier · Band · GP | IV · Mid · 10 (requires Lv. 10) |
| Recipe | Wizard Hat (III) + Staff (I) |
| Fits | Sulfur casters |
| **Stats** | **+6 Sulfur, +2% Cooldown Reduction** |
| Signature | — |
| Skill | — |

**Description:** The Wizard Hat's whispering pages bound around a stirring rod spine. It seems to hold more pages than it has room for, and some are from books not written yet.
**Codex line:** "Every page, a century."
**Card art:** A thick, ancient-looking tome with a wooden spine and loose pages fluttering out.
**Equipped look:** Held open in the off-hand, pages turning by themselves.
**Attack effect:** A swirling page-shaped bolt; the page bursts into glyphs on impact. SFX: a fast page flutter.

### Longbow
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Longbow` |
| Slot · Family | Weapon · Bow |
| Tier · Band · GP | IV · Mid · 10 (requires Lv. 10) |
| Recipe | Hunter's Boots (III) + Bow (I) |
| Fits | Mercury ranged (e.g. Wren) |
| **Stats** | **+4 Mercury, +3 ATK (7 GP after the signature)** |
| Signature | **Far Shot:** +15% damage to targets 5 or more tiles away |
| Skill | — |

**Description:** A tall bow strung with the Hunter's Boots' springy sole strips. It needs room to draw, and rewards patience with arrows that fly farther than anyone expects.
**Codex line:** "Distance is just a number."
**Card art:** A very tall wooden longbow taller than its owner, with leather-wrapped grip.
**Equipped look:** Held in the off-hand, nearly as tall as the wearer.
**Attack effect:** A long, thin arrow streak; on Far Shot hits, a small golden flash. SFX: a deep twang.

### Battle Horn
| Field | Value |
|---|---|
| Data ID | `SO_Gear_BattleHorn` |
| Slot · Family | Weapon · Instrument |
| Tier · Band · GP | IV · Mid · 10 (requires Lv. 10) |
| Recipe | War Drum (III) + Bow (I) |
| Fits | Supports and front-row leaders |
| **Stats** | **+4 Sulfur, +3 Mercury (7 GP after the skill)** |
| Signature | — |
| Skill | **Rallying Call** (70 mana / 16 s): allies in the wearer's row get +4 DEF for 4 s |

**Description:** The War Drum's iron band coiled into a horn and fitted with a bow-limb mouthpiece. One long blast and everyone nearby stands a little straighter.
**Codex line:** "One blast, and they stand taller."
**Card art:** A curved iron-banded horn with a wooden mouthpiece and a leather strap.
**Equipped look:** Hung on a strap; raised to the lips to play.
**Attack effect:** Basic hit: a short horn blast sends a cone-shaped sound wave to the target. SFX: a brassy toot.
**Skill / signature effect:** Rallying Call: a long blast; golden rings rise around allies in its row. SFX: a long, rising horn call.

### Berserker Gauntlets
| Field | Value |
|---|---|
| Data ID | `SO_Gear_BerserkerGauntlets` |
| Slot · piece | Armor · Gloves |
| Tier · Band · GP | IV · Mid · 10 (requires Lv. 10) |
| Recipe | Iron Gauntlets (III) + Greatsword (II) |
| Fits | Salt front-liners (Warrior builds) |
| **Stats** | **+5 Salt, +5 ATK** |
| Signature | — |
| Skill | — |

**Description:** Iron Gauntlets fused with the Greatsword's spare edge, so the knuckles are now blades. They always seem eager to punch something.
**Codex line:** "They want to punch something."
**Card art:** Huge iron gauntlets with short blade edges along the knuckles.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A loud iron clang.

### Sage's Circlet
| Field | Value |
|---|---|
| Data ID | `SO_Gear_SagesCirclet` |
| Slot · piece | Armor · Helmet |
| Tier · Band · GP | IV · Mid · 10 (requires Lv. 10) |
| Recipe | Wizard Hat (III) + Sage Robe (II) |
| Fits | Sulfur casters |
| **Stats** | **+5 Sulfur, +75 mana** |
| Signature | — |
| Skill | — |

**Description:** The Wizard Hat's brim and the Sage Robe's copper thread, woven into a thin circlet. Wearing it feels like a quiet room inside your head.
**Codex line:** "A ring of quiet thought."
**Card art:** A slim copper circlet with a small blue stone set in the front.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A light metallic ting.

### Siege Crossbow
| Field | Value |
|---|---|
| Data ID | `SO_Gear_SiegeCrossbow` |
| Slot · Family | Weapon · Bow |
| Tier · Band · GP | IV · Mid · 10 (requires Lv. 10) |
| Recipe | Arcane Repeater (III) + Crossbow (II) |
| Fits | Mercury ranged (heavy hitters) |
| **Stats** | **+3 Mercury, +4 ATK (7 GP after the signature)** |
| Signature | **Armor-Piercer:** basic hits ignore 20% of the target's DEF |
| Skill | — |

**Description:** Two crossbow springs stacked and wound by the Repeater's self-turning coil. It fires slowly, but every bolt goes through whatever it hits.
**Codex line:** "Knock, knock. Through the door."
**Card art:** A big, heavy crossbow with two stacked springs and a thick iron bolt loaded.
**Equipped look:** Braced at the hip with both hands; recoils hard after each shot.
**Attack effect:** A thick bolt streak; a punch-through burst of splinters on impact. SFX: a heavy clunk.

### Siren Harp
| Field | Value |
|---|---|
| Data ID | `SO_Gear_SirenHarp` |
| Slot · Family | Weapon · Instrument |
| Tier · Band · GP | IV · Mid · 10 (requires Lv. 10) |
| Recipe | War Drum (III) + Lute (II) |
| Fits | Sulfur supports (control) |
| **Stats** | **+5 Sulfur, +30 mana (7 GP after the skill)** |
| Signature | — |
| Skill | **Siren Song** (80 mana / 18 s): the target falls into **Sleep** for 1.5 s (wakes on damage) |

**Description:** The Lute's strings, restrung across the War Drum's iron ring into a small harp. Its notes are soft, sweet and dangerously relaxing.
**Codex line:** "Listen. Then sleep."
**Card art:** A small curved harp with an iron frame and glowing silver strings.
**Equipped look:** Held in the crook of the arm and plucked.
**Attack effect:** Basic hit: a ripple of soft note shapes drifts to the target. SFX: a gentle pluck.
**Skill / signature effect:** Siren Song: a slow, glowing melody wraps around the target; a sleepy "Zz" bubble. SFX: a soft lullaby phrase.

### Shadowfang
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Shadowfang` |
| Slot · Family | Weapon · Dagger |
| Tier · Band · GP | IV · Mid · 10 (requires Lv. 10) |
| Recipe | Nightgrip Gloves (III) + Twin Daggers (II) |
| Fits | Mercury melee (Assassin builds) |
| **Stats** | **+4 Mercury, +1.5% Crit (7 GP after the skill)** |
| Signature | — |
| Skill | **Garrote** (70 mana / 16 s): leaps onto the target's back: **Silence** 1.5 s and 25 physical damage per s for 3 s |

**Description:** The Twin Daggers, reforged as one long black fang with the Nightgrip's grip wound around it. Once it catches something, it doesn't let go.
**Codex line:** "It doesn't let go."
**Card art:** A long, curved black dagger shaped like a fang, with a wire loop at the pommel.
**Equipped look:** Held in reverse grip in the main hand; the wire loop dangles from the pommel.
**Attack effect:** A fast, dark crescent slash. SFX: a sharp snick.
**Skill / signature effect:** Garrote: the wearer leaps onto the target's back, a wire flashes around its neck; a silence icon pops above it. SFX: a whip-snap and a choke.

### Warblade
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Warblade` |
| Slot · Family | Weapon · Sword |
| Tier · Band · GP | IV · Late · 16 (requires Lv. 20) |
| Recipe | Iron Gauntlets (III) + Sword (I) |
| Fits | Salt front-liners (Warrior builds) |
| **Stats** | **+7 Salt, +5 ATK (12 GP after the signature)** |
| Signature | **Cleave:** basic hits deal 30% of their damage to enemies next to the target |
| Skill | — |

**Description:** A broad blade beaten from the Iron Gauntlets' fists around an old sword's core. Each swing carries far past where it should stop.
**Codex line:** "One swing, many problems solved."
**Card art:** A wide, heavy single-edged sword with a fist-shaped iron guard.
**Equipped look:** Held two-handed, resting on the shoulder while idle.
**Attack effect:** A wide sweeping arc that clips nearby enemies; sparks on each one. SFX: a deep whoosh and several clangs.

### Fortress Plate
| Field | Value |
|---|---|
| Data ID | `SO_Gear_FortressPlate` |
| Slot · piece | Armor · Body |
| Tier · Band · GP | IV · Late · 16 (requires Lv. 20) |
| Recipe | Thorn Plate (III) + Iron Mail (I) |
| Fits | Tanks; Salt first |
| **Stats** | **+7 Salt, +1.5 DEF (12 GP after the signature)** |
| Signature | **Immovable:** can't be Knocked Back; +10% Control Resist |
| Skill | — |

**Description:** Thorn Plate's barbs hammered flat and layered over chain mail until it looks like a small castle wall. Nothing moves its wearer unless the wearer wants to move.
**Codex line:** "Walls don't walk. Neither do you."
**Card art:** A massive, blocky breastplate like stacked castle stones, with flattened barbs between the plates.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A deep, solid clang like a struck wall.

### Castle Wall
| Field | Value |
|---|---|
| Data ID | `SO_Gear_CastleWall` |
| Slot · Family | Weapon · Shield |
| Tier · Band · GP | IV · Late · 16 (requires Lv. 20) |
| Recipe | Knight Helm (III) + Tower Shield (II) |
| Fits | Tanks (e.g. Tobin) |
| **Stats** | **+7 Salt, +1.5 DEF (12 GP after the signature). Shield family: **Block 8%** (Late)** |
| Signature | **Shelter:** allies behind the wearer in its lane take −10% damage |
| Skill | — |

**Description:** A Tower Shield rebuilt with the Knight Helm's crest and plates until it has battlements. Allies who stand behind it feel like they're inside a keep.
**Codex line:** "The castle comes with you."
**Card art:** A huge tower shield shaped like a castle wall section, with small battlements along the top edge.
**Equipped look:** Off-hand, replacing fixed hand props (Tobin's pot lid); the main hand shows the default weapon.
**Attack effect:** Basic hit: a heavy shield bash with stone-dust puff. SFX: a stony thump. Shelter: a faint wall-shaped shimmer behind the wearer in its lane.

### Spellbrand
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Spellbrand` |
| Slot · Family | Weapon · Sword |
| Tier · Band · GP | IV · Late · 16 (requires Lv. 20) |
| Recipe | Runeblade (III) + Grimoire (II) |
| Fits | Salt + Sulfur hybrids |
| **Stats** | **+5 Salt, +5 Sulfur, +1% Skill Power (11 GP after the skill)** |
| Signature | — |
| Skill | **Arcane Slash** (90 mana / 16 s): a magic slash along the target's lane: 140 magic damage to every enemy in it |

**Description:** The Runeblade, with a Grimoire's pages pressed into the steel. The spells are written along the edge now, and they read themselves aloud when it swings.
**Codex line:** "The spell has an edge."
**Card art:** A long sword with glowing script running along the blade and a book-clasp crossguard.
**Equipped look:** Held in the main hand; script glows along the edge.
**Attack effect:** A silver arc with floating glyphs. SFX: a ring of steel and a whispered word.
**Skill / signature effect:** Arcane Slash: a glowing blue crescent flies down the target's lane, leaving glyphs behind. SFX: a sharp magical whoosh.

### Tarnhelm
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Tarnhelm` |
| Slot · piece | Armor · Helmet |
| Tier · Band · GP | IV · Late · 16 (requires Lv. 20) |
| Recipe | Knight Helm (III) + Knight Helm (III) |
| Fits | Melee who want a gamble (front-liners, assassins) |
| **Stats** | **+5 Mercury, +4 Salt, +1% Crit (11 GP after the named signature)** |
| Signature | **Instant Travel** (named card): at battle start, the wearer teleports to a **random empty tile anywhere** (own side, middle rows or enemy side). If it lands on the **enemy side**, its first attack hits from behind for **+50% damage** |
| Skill | — |

**Description:** Two Knight Helms fused into one that no longer quite stays in one place. In the old saga it carried its wearer wherever it wished; here, it carries them wherever it likes.
**Codex line:** "Where will you wake up?"
**Card art:** A dark, sleek helm with a shimmering veil-like visor that seems to blur at the edges.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A hollow ring with a faint shimmer.
**Skill / signature effect:** Instant Travel: the wearer vanishes in a shimmer at battle start and reappears elsewhere; from behind, a bright strike flash. SFX: a soft warp and a sharp hit.

### Hagoromo of the Sky Kami
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Hagoromo` |
| Slot · piece | Armor · Body |
| Tier · Band · GP | IV · Peak · 24 (requires Lv. 25) |
| Recipe | Elder Staff (III) + Cloth Robe (I) |
| Fits | Sulfur casters and supports |
| **Stats** | **+9 Sulfur, +4 Mercury, +2% Cooldown Reduction (17 GP after the named signature)** |
| Signature | **Heavenly Robe** (named card): the wearer floats: **immune to Ensnare and ground zones**. Once per battle, when it drops below 30% HP, it becomes **Untargetable for 2 s** |
| Skill | — |

**Description:** From Japanese legend: the feathered robe of a celestial maiden, without which she cannot fly home to the sky. Woven here from an elder staff's light and a simple robe, it lifts its wearer a hand's width above the ground and never quite lets the earth hold them.
**Codex line:** "Lighter than the sky it came from."
**Card art:** A flowing white-and-pale-blue feathered robe with sleeves that drift as if underwater, faint light along the hems.
**Equipped look:** Not shown on the homunculus (GDD §4.7.5).
**Hit sound:** A soft feathery whisper.
**Skill / signature effect:** Heavenly Robe: feathers drift around the wearer's feet while it floats; at low HP it rises in a soft glow and turns translucent for 2 s. SFX: a gentle chime and a rush of wind.

### Balmung
| Field | Value |
|---|---|
| Data ID | `SO_Gear_Balmung` |
| Slot · Family | Weapon · Sword |
| Tier · Band · GP | IV · Peak · 24 (requires Lv. 25) |
| Recipe | Runeblade (III) + Runeblade (III) |
| Fits | Salt front-liners |
| **Stats** | **+9 Salt, +8 ATK (17 GP after the named signature)** |
| Signature | **Dragon-Slayer** (named card): +30% damage vs **Draconic** enemies (needs families as combat tags, GDD §13 #42) |
| Skill | — |

**Description:** From the Nibelungenlied: Siegfried's sword, the blade that slew the dragon Fafnir. Two Runeblades fused into one, its runes still remember the dragon's blood.
**Codex line:** "Forged for a hero. Hungry for dragons."
**Card art:** A long, gleaming broadsword with a gold hilt and a faint red rune glowing near the guard.
**Equipped look:** Held in the main hand; the red rune pulses softly.
**Attack effect:** A bright golden arc; a red rune flash on hits against Draconic enemies. SFX: a clear, ringing slash.

## Named cards (Late band and up)
Folklore weapons and armor discovered through fusion, each with a fixed signature (GDD §4.7.4). No rarity label in game: the name says it. One of each per party. Very high tiers may also give the homunculus a visible **aura** (GDD §4.7.5).

| Card | Slot | Where | Legend |
|---|---|---|---|
| **Balmung** | Weapon · Sword | Tier IV, Peak (Runeblade + Runeblade) | Nibelungenlied: Siegfried's dragon-slaying sword |
| **Tarnhelm** | Armor · Helmet | Tier IV, Late (Knight Helm + Knight Helm) | Nibelung saga: the helm of shape-shifting and instant travel |
| **Hagoromo of the Sky Kami** | Armor · Body | Tier IV, Peak (Elder Staff + Cloth Robe) | Japanese legend: the celestial maiden's feathered robe |

Balmung, Tarnhelm and Andvaranaut (`Items.md`) form a possible **Nibelung set**.
