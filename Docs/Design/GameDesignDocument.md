# Game Design Document — Fuseborn (working title)

| | |
|---|---|
| **Version** | 0.33 (draft) |
| **Last updated** | 2026-11-03 |
| **Status** | Pre-production. Fusion, card categories, and upgrade systems defined; combat and mining outlined |
| **Engine** | Unity (tentative) |
| **Online** | ✅ Online game (server-authoritative) |

> **How to use this doc:** It's a *living* prototype GDD. Leave `TBD` where unsure and list it in §13 Open Questions. Keep answers short and concrete.

---

## 1. Core Concept

**Elevator pitch:**
> _An online card game where you fuse two cards to discover new heroes, weapons, and items. Fusion consumes the ingredients, results roll random unique skills and weapon slots, and your party fights monsters and other players in auto-battles where you choose when to fire each skill._

**World & Story:** ✅ In Alembria *(placeholder)*, alchemy is everything: any two things can **react** into something new. The first to discover a reaction is written into the **Great Codex** and gains wealth and fame. The player leads a new **alchemy guild** of **homunculi** (the heroes: living alchemical beings in the forms of the world's peoples), reacts junk into treasure, fights **Runoffs** (monsters born from failed reactions) and rival guilds for resources. Tone: hopeful, with weight (the player is the alchemist and carries the risk; souls return to nature in reactions). Full lore: [Lore.md](Lore.md).

**Terms:** ✅ **Hero**, **homunculus** and **homunculi** mean the same thing. Player-facing text (UI, card category, Codex, backstories) prefers *Homunculus*; code, data IDs and file names keep *Hero* (`SO_Hero_…`, `Docs/Design/Heroes/`, `HeroGrid.tsv`). Docs may use either; prose is switched to "homunculus" gradually as sections are touched.

**Genre:** Combination/discovery crafting + hero collection + auto-battler with manual skill activation
**Perspective / Camera:** UI-driven card board for fusion; **diagonal battle view** (party bottom-left, enemies top-right)
**Target platform(s):** TBD (mobile + PC fits the card UI and auto-battle best)
**Target audience:** Casual to mid-core collectors, theorycrafters, and traders
**Session length:** TBD (daily check-in of 5–15 min, plus longer optional sessions)
**Inspiration:**
- Combination-discovery genre (e.g. *Little Alchemy*): fuse two things to find a new one.
- Auto-battle with manual skill timing (e.g. *Cookie Run: Kingdom*): the party fights on its own, and the player chooses when to activate skills.
- All recipes, cards, characters, and content in this game are original.

**What makes it different (the hook):**
1. **Fusion consumes ingredients.** Every success is a trade-off.
2. **Results are usable and tradable game objects.** Heroes fight and level up, weapons get socketed, items are equipped or consumed.
3. **Multiple random layers:** hero unique skills (tier-based) and weapon slot counts (0–5). Two copies of the "same" card can differ a lot in value.
4. **Card presentation** for everything.

---

## 2. Design Pillars

1. **"What happens if…?"** Curiosity drives play. Experimenting is never punished (no match = no loss).
2. **Meaningful sacrifice.** Fusion costs cards, so the choice of what to fuse matters.
3. **My collection is one of a kind.** Levels, rolled skills, weapon slots, and sockets make every card personal and tradable.

**Player fantasy:** _"I'm an alchemist-summoner who discovers secret recipes, forges a one-of-a-kind army, and proves it in battle."_

---

## 3. Core Gameplay Loop

```
   ┌──────────────── Card sources ◄────────────────────────────────┐
   │   (Starter 30 · Daily Chest 8 · Monster drops · Mining · PvP) │
   ▼                                                               │
 Fuse 2 cards ──► New card (Codex) ──► Build party: equip, socket ──► Auto-battle
  (consumed)        random rolls          (weapon, armor, accessory)   PvE / PvP
                                                                        │
                                       Heroes in party gain XP ◄────────┘
                                       Drops + currency → fuse / trade
```

| Loop | Timescale | Description |
|---|---|---|
| **Moment-to-moment** | seconds | Fusion: drag a card onto another. Battle: tap skills at the right time. |
| **Short loop** | minutes | Open the chest → fuse → equip → clear a few stages |
| **Long loop** | days/weeks | Complete the Codex, chase Gold skills and 5-slot gear, climb PvP, trade |

**Win condition:** None overall (live game). Goals = Codex completion, stage progress, PvP rank.
**Lose condition:** Losing a battle only. No card loss (§5.2).

---

## 4. Mechanics

### 4.1 Card Categories (3)

| Category | Subtypes | Fusable with | Instance type |
|---|---|---|---|
| **Hero** | (Role-based, §4.6) | Hero | Unique instance (level, gear, skill) |
| **Gear** | **Weapon** (sword, bow, staff…) · **Armor** (mail, robe…), §4.7 | Gear | Unique instance (random slots + sockets) |
| **Item** | **Material** (junk basics and up, Tier I–III) · **Consumable** (Potion, Bomb, Scroll, Charm; only Potion & Bomb in battle) · **Accessory** (Ring, Necklace, Amulet, Crown) · **Magic Stone** | Item | Materials, consumables & Magic Stones **stack**; accessories are unique instances |

- ✅ **Fusion stays within one category.** Hero + Hero, Gear + Gear, Item + Item. A Gear + Gear fusion can produce a weapon **or** an armor (e.g. Sword + Iron Mail → Tower Shield).
- Cross-category interactions are **actions**, not fusion: *equip* (Hero ← Weapon/Armor/Accessory), *socket* (Gear ← Magic Stone), *use* (Hero ← Potion).
- An Item + Item fusion can produce **any Item subtype**. For example, two basic items might create a Ring.

### 4.2 Basic Cards & Starting Collection
- **Basic (Tier 1) card pool:** 5 per category = **15 basic card types** _(confirm, §13)_.
- ✅ **Starter pack:** each new player receives **30 random basic cards** (copies drawn from the basic pool). The category split can vary; it doesn't need to be 1:1:1.
- **Proposed safety rules for the starter pack** (so no player starts stuck):
  - At least **[party size] heroes**, so the player can field a full party.
  - At least **one fusable pair** (a valid recipe) per category.
- The starter pack uses the same rarity weights as the Daily Chest (§4.2.1), with the safety rules above applied on top.
- The basic list will be provided later. → §15 Content Lists.

#### 4.2.1 Basic Card Rarity ✅
Each **basic card type** has a **rarity** that controls how often it appears in chests and drops. Rarity is about **how hard a card is to obtain**. It's separate from **Tier** (how deep a card is in the recipe tree).

| Rarity class | Basic types per category (proposed) | Drop weight per card (proposed) |
|---|---|---|
| **Common** | 2 | 65% |
| **Uncommon** | 2 | 30% |
| **Rare** | 1 | 5% |

- Weights are per card in a chest, and tunable. Within a class, each type is equally likely.
- Rare basics are expected to become the **most-traded basic cards**.

#### 4.2.2 Seasonal Rarity Rotation ✅
- The game runs in **Seasons** (proposed: **4–6 weeks**). At each season start, the server **reshuffles which basic card types are Common / Uncommon / Rare**.
- **What's public vs. hidden:**
  - **Public:** the rarity *classes* and their odds (65 / 30 / 5). This keeps us compliant with app-store and regional loot-box rules that require disclosing odds.
  - **Hidden:** *which* card is in which class this season. The community figures it out (like recipes), and the market reacts.
- Because rarity changes, **the card frame does not show basic rarity** (§8).
- Why seasons, not weekly: a weekly change would crash card values too often. A player who traded hard for this week's Rare would feel cheated a few days later. A season gives the market time to settle and makes each reshuffle an event.
- ⚠️ **Recipe rule (updated):** since any basic can become Rare in some season, **every important result must have at least two recipes** (alternate paths). Then no single basic, if it turns Rare, can block progress.

#### 4.2.3 Rare Guarantee (pity)
- ✅ Every player is guaranteed **at least 1 Rare basic card per week.**
- Proposed delivery: a **7-day login streak chest** with 1 guaranteed Rare, plus a few random cards. It doubles as a weekly return reason.
- The guarantee is what makes the low 5% base rate fair. (At 10%, a player would almost always get a Rare from 56 chest cards a week anyway, so the guarantee would mean little.)

#### 4.2.4 Exchange: Duplicates → Chests ✅
Players trade unwanted basic cards to the system for a chest:

| Trade in | Get (proposed) |
|---|---|
| **10** basic cards | **Small Chest:** 3 random basics, improved odds (e.g. 50 / 40 / 10) |
| **25** basic cards | **Big Chest:** 8 random basics, at least 1 Uncommon, improved odds (e.g. 45 / 40 / 15) |

- Eligible: basic (Tier 1) cards only. Heroes at Lv. 1 with no gear, gear with no socketed stones.
- The Exchange **always returns fewer cards than it takes** (10 → 3, 25 → 8). It's a sink that turns quantity into a shot at rarity, and it can't be looped for profit.
- Possible limit: N exchanges per day, to control the economy (TBD).

### 4.3 Fusion Rules

| Rule | Definition |
|---|---|
| Input | Drag card A onto card B (2 cards; A+B = B+A) |
| **Match** | Both cards are **consumed** and the result is created. The recipe is recorded in the Codex. |
| **No match** | **Nothing happens.** No cards are lost. A short "no reaction" feedback plays. |
| Same + same | Allowed as a recipe |
| Determinism | The **result card type** is fixed per recipe. **Random rolls:** hero unique skill (§4.6.4) and gear slot count (§4.7.1). |
| Server authority | Recipe lookup and all random rolls happen **on the server** (§12). |

**Consumed hero / gear:**
- Equipped gear is **returned to the inventory** before a hero is fused.
- Socketed stones are **lost** when their weapon/armor is fused (detach first, which itself is risky, §4.7.2).
- ✅ **A fused hero result starts at Level 1.** The play pattern is "keep one, fuse the spare."
- A confirmation appears when fusing a leveled or equipped hero, or gear with 3+ slots.

### 4.4 Tiers
- Every card has a **Tier** (1 = basic). A result's tier ≥ the highest ingredient tier (formula TBD).
- ✅ **Hero tier = recipe depth, not power.** A hero's tier only maps where it sits in the fusion tree (what it is made from). A Tier I hero is **not weaker** than a Tier III hero: hero strength comes from the hero's own base stats, role and skills, and from how the player **levels and equips** it. Hero base stats are set per hero, never by tier.
- Why fuse heroes then: discovery and the Codex, new kits and roles (two homunculi with the same role bring different tools), targeting and active skills, a fresh unique-skill roll, and collection.
- Gear and Items: higher tiers **are** better quality (§15.7–15.8). Tier also drives card frame visuals and gear slot odds.

### 4.5 Codex & Recipe Discovery
- In-game Codex shows **every card that exists** as a silhouette "???" until discovered, with progress per category.
- Discovered entries show the recipe that made them.
- **Hints:** reveal one ingredient of an undiscovered recipe (cost: soft currency or a hint item, TBD).
- **Official recipe list policy:** ✅ **No official cheat sheet.** Show the full card list (silhouettes) in-game, and let the community research and share. See §5.4 for the reasoning and supporting features.

### 4.6 Hero

#### 4.6.1 Leveling
- ✅ Heroes gain XP **only when used in a party** in battle. Unused heroes stay at Level 1.
- ✅ **Level-up:** when XP passes the threshold, the hero levels up, its growth is **added to Salt / Mercury / Sulfur automatically**, and it gains **1 skill point** to spend in the skill tree (§4.6.4). Hero level only raises stats and gives points; it never unlocks skills directly.
- ✅ **Level cap: 30** for every hero, any tier. Built to be raised in later updates (cap stored as data, not hard-coded). XP curve: TBD.
- ✅ Each hero has its **own base stats and growth per level** (not set by tier), so a well-leveled basic can beat a Tier III hero.

#### 4.6.2 Stats ✅ (three principles)
Every homunculus is made of the three alchemical **principles** (Lore.md): **Salt** (body), **Mercury** (fluidity), **Sulfur** (fire and spirit). Each has its own **base value and growth per level** for all three, plus one **dominant principle**, **set by design per homunculus** (never by role). Principles give only flat stats through **universal rates** (same for every homunculus):

| Principle | Grants (start values, §6.9) |
|---|---|
| **Salt** | +20 HP, +0.1 HP regen/s per point |
| **Mercury** | +0.15 DEF, +1 Attack Speed per point |
| **Sulfur** | +12 mana, +0.05 mana regen/s, +0.15 RES per point |
| **Dominant principle** | **+1 attack damage** per point, and **Resonance:** that principle's own grants above are **+10%** |

- **Growth rules:**
  1. **Budget:** base Salt + Mercury + Sulfur = **46–54**, total growth = **5.0–6.0 / level**, for every homunculus (tier ≠ power).
  2. The **dominant principle has the highest growth**.
  3. The rest of the spread follows **lore and kit**. **The more roles its branches cover (§4.6.4), the flatter the spread**: single-role homunculi can be spiky, multi-role ones flatter, with branch passives filling the gap.
- **Percentage stats are never from principles:** Crit, Evasion and Block come from gear, items, skill-tree passives and unique traits.
- Full formulas: §6.9. Per-homunculus values: `Docs/Design/Heroes/`.

#### 4.6.3 Equipment Slots
✅ Each hero has 3 slots:

| Slot | Accepts |
|---|---|
| **Weapon** | Gear card of slot type Weapon (heroes come with a default basic weapon) |
| **Armor** | Gear card of slot type Armor: **one** piece, either Body, Helmet, Gloves or Boots (§4.7.3) |
| **Accessory** | ✅ **One slot:** Ring, Necklace, Amulet **or** Crown |

#### 4.6.4 Role, Trait & Unique Skill
- Each hero has an **initial role** (a label, §6.3), a **targeting priority** (§6.4), and trait(s).
- ✅ **Branching skill tree** (per hero, `Docs/Design/Heroes/`). Unlocks depend on **skill levels**, never on hero level:
  - **Skill points:** 1 per hero level (Lv. 1 starts with 1, so 30 at cap). The player spends them.
  - **Core:** **A1** (available from the start) → **A2** (unlocks at A1 skill Lv. 2), plus a **core passive** (on from the start; its levels cost points).
  - **Branch point:** set per hero, after A1 Lv. 2 or after A2 Lv. 2. **1 to 3 branches per hero (maximum 3, fixed for now)**; the count fits the hero's lore. With **2–3 branches**, spending the first point in one **locks it permanently** and closes the others. With **1 branch** there is no choice: it opens automatically at the branch point, with no permanent-choice warning. The branch stays on the card when traded.
  - **Each branch:** **Bx1** active (available once chosen) → **Bx2** active (at Bx1 Lv. 2) → **Bx passive** (at Bx2 Lv. 2).
  - **Skill levels:** **5 for every skill**, actives and passives. Values are **fixed per skill level**; each active costs **mana** and has a **cooldown**.
  - **Budget:** 6 skills (A1, A2, core passive + the branch's 2 actives and passive) × 5 levels = **30 points**, all on the hero's own skills, maxed exactly at Lv. 30. While leveling, the player chooses what to raise first.
  - **Scroll skills** cost no points: a Scroll teaches its skill at Lv. 1; using another copy of the **same Scroll** on that hero raises it by 1 level (max Lv. 5). Server-authoritative, like all inventory use.
  - ✅ **Each branch declares its role** (§6.3). A branch may keep the initial role or shift to another one, so the same homunculus can become e.g. a healer, a paladin or a tank-like build. Rules for designing branches:
    1. **Lore decides** which roles a homunculus can reach (an angel priest can tank; a goblin rogue never does).
    2. **At least one branch keeps the initial role**, so the label shown at discovery is always a valid path. A 1-branch homunculus stays in its initial role.
    3. **Specialists keep the core tool** (§6.3): an off-role branch takes the role's shape but only a weaker version of its core tool.
  - Body stays the same in every branch: dominant principle, base stats and growth, attack type and range never change; the branch changes skills and role.
  - In battle the hero brings **2 actives** (loadout, §6.5) from A1, A2, its branch actives and Scroll skills. Passives are always on.
  - Content per hero: 2 core actives + 1 core passive, plus 2 actives + 1 passive **per branch** (up to 9 actives + 3 passives with 3 branches). Fewer branches = less content and art. Branch skills should reuse the hero's animation set where possible; a branch may swap one signature prop so the build reads at a glance.
- ✅ The **rolled unique skill** (innate trait, Lore.md) below is **separate** from the tree: tree passives are the hero's identity, the unique roll is what makes each copy special.
- ✅ **Every hero rolls a unique skill (passive, always on), basics included.** A basic hero rolls when it is obtained (chest, starter pack, drop); a fused hero rolls when it is created. Basics are therefore worth keeping or trading, not only fusing. Weighted pool:

| Rarity | Example weight |
|---|---|
| Bronze | 70% |
| Silver | 25% |
| Gold | 5% |

- Same ingredients → possibly a different unique skill.
- ✅ **Pure re-roll:** ingredient skills have no effect on the result's roll. Fusing a hero with a good skill gives that skill up.
- ✅ **Skill strength does not scale with tier** (consistent with tier = recipe depth).
- ✅ Skill rarity uses **Bronze / Silver / Gold**, so it never gets confused with basic card rarity (Common / Uncommon / Rare).
- ✅ **No pity and no re-roll item.** Trading is the answer to bad luck.
- ✅ **Trait pool:** all hero, gear and accessory traits, with rarity, start values, tags and % stat caps, live in `Docs/Design/TraitPool.md`.

### 4.7 Gear (Weapon & Armor)
✅ **Weapon families** decide which heroes can equip a weapon. Each hero lists 1–3 allowed families; armor and accessories have no restriction (for now).

| Family | Gear cards |
|---|---|
| Sword | Sword, Greatsword, Runeblade |
| Dagger | Twin Daggers |
| Bow | Bow, Crossbow, Arcane Repeater |
| Staff | Staff, Elder Staff |
| Tome | Grimoire |
| Shield | Tower Shield |
| Instrument | Lute, War Drum |
✅ Weapons and armor are one category, **Gear**. Each Gear card has a **slot type** (Weapon or Armor) that decides which hero slot it fits. Lists in §15.7.

#### 4.7.1 Random Slots
- ✅ When a Gear card (weapon or armor) is created, it rolls **0–5 slots**. Proposed weights (tunable; higher tiers shift toward more slots):

| Slots | 0 | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|---|
| Tier 1 weight | 30% | 30% | 20% | 12% | 6% | 2% |

- ✅ **Gear trait:** separately from slots, a new Gear card has a **30% chance** to roll one trait (Bronze/Silver/Gold 70/25/5) from the gear pool in `TraitPool.md` §4. Fusing gear re-rolls it.

#### 4.7.2 Socketing Magic Stones (risk-based)
✅ **Magic Stones** (Item subtype) are attached to **Gear** slots (weapon or armor). Both attaching and detaching have a **success chance**.

| Action | ✅ Success | ❌ Fail ✅ decided |
|---|---|---|
| **Attach** stone | Stone is placed; gear is **upgraded** (stone bonus applied) | **Stone is destroyed**; gear is kept unchanged |
| **Detach** stone | Stone returns to the inventory; gear loses that bonus | **Stone is destroyed**; gear is kept (loses that bonus) |

**Proposed success rates** (tunable; each additional filled slot is harder):

| Filling slot # | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| Attach success | 100% | 90% | 75% | 60% | 40% |

- Detach success: proposed **70%** flat (or scales with stone tier).
- **"Destroy all" outcome (gear + stones lost):** proposed **not** in the base system. Possible later as an *opt-in* high-risk action (e.g. a "Volatile Stone" with bigger bonuses). See §13 #8.
- **Protection item:** an Item made through fusion (e.g. a "Ward Charm") that prevents loss on one failed attempt. It gives Item fusion an extra purpose.
- When a weapon/armor is **fused**, its socketed stones are **lost** (they're part of the gear), unless detached first. A confirmation warns the player.
- All attach/detach rolls happen **on the server**.

#### 4.7.3 Armor Pieces & Bonus Stats (proposed)
✅ Body armor, helmets, gloves and boots all share the hero's **one Armor slot**. Pieces differ by bonus focus: body armor for survival, the others for utility.

| Armor piece | Typical bonuses |
|---|---|
| Body | HP, DEF, Block, Thorns |
| Helmet | DEF, Cooldown Reduction, Control Resist |
| Gloves | ATK, Attack Speed, Crit Chance, Lifesteal |
| Boots | Move Speed, Evasion |

**Gear bonus stats** (on gear only, alongside hero Salt/Mercury/Sulfur): HP, DEF, ATK, Attack Speed, Move Speed, Crit Chance, Evasion, Block, Lifesteal, Cooldown Reduction, Skill Power, Thorns (reflects melee damage), Control Resist. These are the only sources of % stats besides passives and traits (§4.6.2). Values TBD.

### 4.8 Item

| Subtype | Use | Stackable | Notes |
|---|---|---|---|
| **Material** | Fusion ingredient only (Tier I–III: Stone, Seed, Log, Bone, Scrap Metal and what they make) | ✅ | Junk-like basics |
| **Potion** | Consumed on use (heal, mana refresh, buffs, special effects) | ✅ | Can be used in battle? TBD |
| **Bomb** | Consumed on use (battle effect) | ✅ | Effects TBD |
| **Scroll** | Used **outside battle**: teaches a hero a new active skill at Lv. 1; a duplicate of the same Scroll raises it 1 level (max 5; §4.6.4) | ✅ | Which skill, role limits: TBD |
| **Charm** | Consumed on use (e.g. Ward Charm protects a socketing attempt) | ✅ | Effects TBD |
| **Ring / Necklace / Amulet / Crown** | Accessory slot | ❌ | Stat bonus + trait (always rolls one, `TraitPool.md` §5) |
| **Magic Stone** | Socketed into Gear slots | ✅ | Upgrade effect per stone type |

✅ Item basics are junk materials. Usable items appear from Tier IV (Tier III + Tier I) and better ones at Tier V (Tier III + Tier II). Lists in §15.8.

### 4.9 Trading
- ✅ Player-to-player trading using **in-game currency** (design in a later phase).
- Gear slot count, unique-skill rarity, and level make each card's market value differ.

---

## 5. Progression & Economy

### 5.1 Card Sources

| Source | Role | Creates new cards? | Phase |
|---|---|---|---|
| **Starter pack**: 30 random basics | Onboarding | ✅ | Prototype 1 |
| **Daily Chest**: ✅ **8 fully random basic cards** (rarity-weighted) | Daily baseline, return reason, trading driver | ✅ | Prototype 1 |
| **7-day streak chest**: 1 guaranteed Rare (§4.2.3) | Weekly pity + return reason | ✅ | Prototype 1 |
| **Exchange** (duplicates → Small/Big Chest, §4.2.4) | Duplicate sink | ✅ (fewer than it takes) | Prototype 1 |
| **Monster drops** (auto-battle PvE) | **Main source** | ✅ | Prototype 2 |
| **Mining spot** | Basic card source, mechanic TBD (§7) | ✅ | Later |
| **PvP rewards** | Winner reward chest | ✅ (system-generated) | Later |
| **Trading** | Redistribution | ❌ Moves cards only | Later |

### 5.2 Rules
- **Daily Chest:** ✅ **8 fully random basic cards.** Any category mix and no fusable-pair guarantee (the starter pack already guarantees a working start). Each card is rolled by rarity weight (§4.2.1). An unlucky chest is meant to push players toward **trading**, even for basic cards.
- **PvP:** ⚠️ losers **don't lose cards**; winners get a system-generated reward. (Avoids rage-quits and alt-account abuse.)
- **Currencies:** ✅ Two currencies.
  - **Coins** (soft): earned from battles and selling cards; used for trading, hints and other sinks (TBD). Not called "Gold", which is a skill rarity.
  - **Gems** (premium): for convenience and cosmetics, never sold as direct power. Monetization details TBD.
- **Collection (inventory):** ✅ **Unlimited.** Cards **stack only when exactly identical** (same card, level, stats, skill, slots and sockets). In practice: materials, consumables, Magic Stones, and unleveled basics that rolled the same skill.
- **Battle loadout:** besides each hero's Weapon, Armor and Accessory slots, the party brings **2 shared consumable slots**. Each slot holds one stackable consumable type (§6.5).

### 5.3 Prototype 1 Plan
- Starter pack + Daily Chest + debug "Test Chest" (unlimited) for playtesting.
- Measure how many cards per session feel "enough", to tune chest size and drop rates.

### 5.4 Recipe Knowledge Strategy
**Decision: no official cheat sheet. Let the community share. Support discovery in-game.**
- Recipes are stored **only on the server**, so they can't be data-mined from the game client. The community must genuinely discover them.
- Expect most recipes to be public on fan wikis within weeks. That's fine: discovery is a **launch and new-content** experience. Long-term value must come from **random rolls, combat, and trading**.
- Supporting features:
  - Codex silhouettes + hints (§4.5)
  - **"First discoverer" credit**: the server records the first player to find each recipe. A great community hook.
  - **New recipes in content updates and limited-time events**, so discovery restarts regularly.
  - Optional later: an in-game recipe-sharing board.

---

## 6. Combat — Auto-Battle

✅ **Auto-battle with manual skill activation.** Heroes attack automatically with basic hits. The player selects a hero and taps one of its 2 skills when ready.

### 6.1 Camera & Battlefield
✅ **Diagonal view:** the player's party stands at the **bottom-left**, and opponents come from the **top-right**.

```
                                   ╱ enemies enter ↙
                         [E][E][E]
                      [E][E][E]          ← opponent grid
                   [E][E][E]

         [H][H][H]
      [H][H][H]                         ← player grid
   [H][H][H]
```

#### 6.1.1 Battle HUD ✅ (hybrid select-then-cast)
Each hero brings **2 active skills** (§6.5). The player **selects a hero, then taps one of its skills**.

**Mobile (landscape)**
```
 (H1)•                                   [E][E][E]
 (H2)                                 [E][E][E]
 (H3)••  ← selected (larger)
 (H4)•          [H][H][H]
 (H5)        [H][H][H]
          [ Skill A ][ Skill B ]              (P1)(P2)
```
**PC**
```
          [ Skill A ][ Skill B ]              (P1)(P2)
   [H1][H2][H3][H4][H5]   ← keys 1–5 select
```
- **Hero buttons (5, formation order):** mobile = vertical column of small circles on the left edge; PC = row under the skill bar, selected with keys **1–5**. The selected hero's button grows slightly.
- **Ready dots:** each hero button shows **one dot per ready skill** (0–2); the portrait ring shows HP. Ready skills are visible without selecting.
- **Skill bar:** shows the selected hero's 2 skills with cooldowns. PC keys **Q / W**.
- **Quick-cast:** tapping an **already selected** hero casts its first ready skill (Skill A first, then B).
- **Default selection:** first living hero at battle start; jumps to the next living hero when the selected one is knocked out.
- **Consumables:** **2 buttons in the bottom-right corner** (P1 / P2) on both platforms, with stack count and cooldown (§6.9). PC keys **E / R**.
- ⚠️ On mobile the left hero column must not cover the party at the bottom-left: shift the battle camera slightly right or keep the column narrow. Check in Prototype 2 (§13 #34).

- ⚠️ **Art implication:** in this view, the player's heroes are seen from a **back ¾ angle**, and enemies from a **front ¾ angle**. In PvP, the opponent's heroes are the same characters seen from the front, so **every hero needs both views** (two sprite/animation sets). Options:
  - 2D sprites with 2 facings (2× animation work per hero)
  - Low-poly 3D or 2D-skeletal (e.g. Spine) models, which can be shown from either side more cheaply
  - Decide in the Art Direction / Technical Design (§13 #20).

### 6.2 Party & Formation
- ✅ **Party size: 5 heroes.**
- ✅ **Board: 3 lanes × 8 rows.** Each side has a **3 × 3 formation** (back, middle, front row); **2 neutral middle rows** separate them. **Square tiles** (they keep lanes clean). The player places 5 heroes on their own 3 × 3 before battle; 4 tiles stay empty.

```
Enemy   row 8 back · 7 middle · 6 front
Middle  rows 5, 4
You     row 3 front · 2 middle · 1 back
```
- ✅ **Lanes matter:** rows decide who gets hit first; lanes are used by "Same lane" targeting and by lane skills (e.g. a pierce that hits a whole lane). A unit's lane and row are **where it currently stands**.

| Row | Intended roles | Rule (proposed) |
|---|---|---|
| **Front** | Tank, Warrior | Targeted first by most enemies |
| **Middle** | Warrior, Ranger, Assassin | Reached once the front row is down (or via targeting rules) |
| **Back** | Mage, Support, Ranger | Safest; reached by back-line targeting heroes |

- The formation is set before battle and saved per mode (PvE party, PvP defense party).
- Any role can be placed in any row. Placement is the player's strategy.
- ✅ **Tiles are for placement and range only.** In battle, homunculi **move freely** (continuous, not tile to tile).
- ✅ **Attack range in tile lengths**, set per homunculus (not by role):

| Range | Tiles | Reaches without moving |
|---|---|---|
| Melee | 1 | Must walk to the target |
| Short | 3 | From the front row: the enemy front row |
| Medium | 5 | From the back row: the enemy front row |
| Long | 7 | Anywhere; never needs to move |

- ✅ **Movement:** a homunculus moves only until its target is in range, then attacks. **Move Speed** (per homunculus + gear) decides how fast. Attack type (melee / ranged) is set per homunculus.
- ✅ **Crowding:** **allies never block allies** (they pass or slide around each other); only enemies block. Up to **4 melee attackers** can surround one target; extra ones **retarget** to the nearest other reachable enemy. Summons and back-row melee therefore always reach the fight.
- The simulation runs on the server in fixed steps, so every replay gives the same result.

### 6.3 Roles ✅ (labels)
A role is a **label for the job a build is tuned for**. It drives no mechanics by itself: dominant principle, attack type and range, DEF growth and targeting are set **per homunculus** (§4.6.2, §6.9). A homunculus has an **initial role** (shown on the card at discovery) and each branch declares its role (§4.6.4); after branching, the card shows the **branch role**. Two homunculi with the same role bring different tools.

Each role has a **core tool**. **Specialists** (initial role) are the best at it; **off-role branches** take the role's shape but only a weaker version of its core tool.

| Role | Job | Core tool (specialists keep the best of it) | Usual targeting (guideline only) |
|---|---|---|---|
| **Tank** | Survive in front, protect | **Protecting others:** Taunt, shields on allies, intercepting hits | Front-most enemy |
| **Warrior** | Melee damage, durable | **Sustained front-line damage** | Front-most enemy |
| **Ranger** | Ranged physical damage | **Reliable single-target damage from range** | Varies (e.g. Wren: same lane, back-most) |
| **Assassin** | Burst, dives the back line | **Reaching and deleting the back line** | Support or Mage first |
| **Mage** | Area / magic damage | **Area damage and control** | Largest group / middle row |
| **Support** | Heal, buff, cleanse | **Healing and buffing others** | Heals ally with lowest HP |

Example: Tobin (Tank specialist) keeps the team alive with Taunt and protection; an Elsie tank-like branch keeps *herself* alive with self-heal and a little healing, but protects others less.

### 6.4 Targeting Priority ✅
Each hero has its **own built-in targeting characteristic**. This is part of the hero's identity (e.g. Hero A always hits the front row; Hero B hunts supports).

- Each hero has a **primary priority** and a **fallback** (used when no valid primary target exists).
- Proposed targeting rules (pick from this list per hero):

| Rule | Picks |
|---|---|
| Front-most | Nearest enemy in the front-most occupied row |
| Same lane | Enemy in the same lane, front to back |
| Same lane, back-most | Furthest-back enemy in the same lane |
| Back-line | Enemy in the back-most occupied row (tie: nearest lane first) |
| Role: X | First enemy whose **current role** is X (branch role if branched, else initial role), otherwise fallback |
| Lowest HP | Enemy with the lowest current HP % |
| Highest ATK | Strongest enemy attacker |
| Random | Any living enemy |

- **Taunt** (any skill that applies it, usually Tanks) overrides targeting for its duration.
- Later: unique passives or accessories could modify targeting (e.g. "attacks the lowest-HP enemy instead").

### 6.5 Attacks & Skills
| Element | Rule |
|---|---|
| **Basic hit** | ✅ Automatic when no skill is used. Rate from base attack interval + Attack Speed (Mercury, gear). Damage = base damage + dominant principle (§6.9) |
| **Active skills** | ✅ **2 per hero in battle**, picked before battle from the hero's skill pool (leveling + Scrolls). Loadout saved per mode (PvE party, PvP defense). Cast via the hybrid HUD (§6.1.1) |
| **Skill readiness** | ✅ Each skill costs **mana** and has a **cooldown**. Heroes start with 50% mana; skills start 50% charged. Cooldown Reduction only from gear |
| **Unique skill** | ✅ **Passive**, always on (e.g. "heals allies 2% of damage dealt"). No extra button |
| **Auto-skill toggle** | PvE: optional, so grinding can be fully automatic. PvP: AI-controlled (§6.7) |
| **Consumables in battle** | ✅ **2 shared consumable slots** per party, shown as 2 buttons in the **bottom-right corner** (§6.1.1). **Potions and Bombs only** (Scrolls are used outside battle). Each slot holds one stackable consumable type (e.g. 5 × Minor Healing Potion). Per-slot cooldown and max uses per battle (to stop spam), and PvP AI use: TBD |

### 6.6 PvE — Monster Stages
- ✅ Monsters are **Runoffs**: failed or uncontrolled reactions that came alive (Lore.md). Their drops are recovered reagents.
- Stages are grouped into **chapters** following the guild's rise; chapter bosses are large Runoffs from famous failed reactions. Each stage = several **waves** entering from the top-right, ending with a **boss wave** on key stages.
- Rewards: **XP for party heroes**, **basic card drops** (main card source), Coins, chance of higher-tier cards on harder stages.
- Cleared stages can be replayed for grinding (optional later: "sweep" / skip for **3-star** stages, §6.12).
- **Win:** all waves defeated. **Lose:** all heroes knocked out, or the time limit runs out (**90 s per wave group**, with overtime in the last 15 s, §6.12). Wins are graded with **stars** (§6.12).
- Knocked-out heroes recover after battle. No permanent loss.

### 6.7 PvP — Asynchronous
- ✅ (proposed earlier) You fight another player's saved **defense party**. Both sides are shown in the same diagonal view: you at the bottom-left, the opponent at the top-right.
- The opponent's skills fire automatically by AI (e.g. when ready, or by simple rules: heal when an ally is under 50% HP).
- Your skills: manual, or auto if toggled.
- ✅ **Time limit 60 s**, overtime in the last 15 s. On timeout with both sides standing, **higher HP % wins** (§6.12).
- Rewards: **rank points scaled by stars** (§6.12) + a winner reward chest. A loss costs rank points; a draw gives a small change. **The loser loses no cards.**

### 6.8 Prototype 2 Scope (combat)
- 1 chapter, ~5 stages with waves + 1 boss
- 6 roles, targeting rules, basic hits, cooldown skills, passive unique skills
- 5-hero 3×3 formation editor
- XP gain + card drops
- PvP: out of scope (Phase 5)

### 6.9 Combat Numbers (proposed, all tunable in ScriptableObjects)
✅ **Damage types: Physical and Magic** (§13 #23). DEF reduces physical damage, **RES** reduces magic damage. No element chart; elements appear only as small Magic Stone effects (below).

**Per-hero data:** base Salt / Mercury / Sulfur, growth per level for each, dominant principle, initial role, base HP, base attack damage, base DEF / RES, DEF growth (per homunculus; 0 for most), base mana, base attack interval, attack range (melee / ranged), Move Speed. Never set by tier (§4.4).

**Attribute at level L** = base + growth × (L − 1).

| Derived stat | Formula (start values) |
|---|---|
| HP | base HP + Salt × 20 |
| HP regen | Salt × 0.1 /s |
| Mana | base mana + Sulfur × 12 |
| Mana regen | Sulfur × 0.05 /s |
| Attack damage | base damage + dominant principle × 1 |
| Resonance | the dominant principle's own grants (HP & HP regen / DEF & Attack Speed / mana, mana regen & RES) × 1.1 |
| DEF | base DEF + DEF growth × (L − 1) + Mercury × 0.15 + gear. DEF growth is **per homunculus** (e.g. Tobin: base DEF 6, +0.3 per level); most have none |
| RES | base RES + Sulfur × 0.15 + gear |
| Attack Speed | Mercury × 1 + gear (100 = normal) |
| Attacks per second | (100 + Attack Speed) / 100 / base attack interval |
| Crit / Evasion / Block | gear, items, passives, traits only. Crit = 150% damage |
| Move Speed | per hero + gear (everyone who needs to move, §6.2) |

**Damage reduction** = 0.06 × DEF / (1 + 0.06 × DEF) against physical; same formula with RES against magic. 10 DEF ≈ 37%, 20 DEF ≈ 55%, never immune.

**Basic hit** = attack damage × (1 − reduction) × crit × random 0.95–1.05. Damage type: physical for Tank, Warrior, Ranger, Assassin; magic for Mage, Support (per hero, can differ).

**Skills** = fixed value per skill level × (1 + Skill Power % from gear), then reduction by DEF or RES. Healing ignores reduction. Each skill costs mana and has a cooldown; **Cooldown Reduction comes from gear only**.

**Elemental effects (Magic Stones only):** a socketed stone may add a small rider, e.g. **Ember Stone → burn** (extra magic damage over 3 s). Other stone effects are designed with the Item effects.

**Consumable slots (§6.5):** proposed **15 s cooldown per slot** and **max 3 uses per slot per battle**. PvP AI uses them by simple rules (e.g. heal when an ally is under 40% HP).

**Battle timing:** basic hits on the attack timer; heroes start with **50% mana**; skills start with 50% of their cooldown charged; PvE time limit 90 s per wave group (§6.6).



### 6.10 Status Effects ✅
| Status | Effect |
|---|---|
| **Stun** | Can't act |
| **Taunt** | Must target the taunter |
| **Stagger** | Interrupts the current action and slows attacks by 30% for 2 s |
| **Confuse** | Attacks a random unit; may hit its own allies at 50% damage |
| **Burn** | Magic damage over time |
| **Shield** | Absorbs damage before HP |
| **Bleed** | Physical damage over time |
| **Weaken** | Deals less damage (%) |
| **Untargetable** | Can't be targeted by enemies |
| **Knockback** | Pushed back 1 tile length; also interrupts |
| **Ensnare** | Rooted: can't move (can't close distance to targets), can't evade (Evasion counts as 0, can't be or become Untargetable), and takes **physical** damage over time (reduced by DEF) |
| **Curse** | Magic damage over time. If the target dies while cursed, the Curse **jumps** to the nearest living enemy (neighbor cell first) with its remaining duration. Re-applying refreshes the duration; it does not stack |
| **Sleep** | Can't act (no attacks, skills or mana regen); **wakes on taking damage**. Skill-specific variants may say otherwise (e.g. Wren's curse) |

- Status duration reduction (Control Resist from gear, passives, traits) is **capped at −50%**. No full status immunity; only **knockback** immunity exists.

### 6.11 Summons ✅
Some skills summon **minions** onto the grid (first user: Grum's Demonology branch).

| Rule | Value |
|---|---|
| **Limit** | Up to **2 minions** per summoner. Summoning again with 2 alive replaces the oldest |
| **Placement** | An **empty cell on the summoner's side**: front-most empty cell in the summoner's lane first, otherwise the front-most empty cell anywhere. No empty cell → the skill is not cast and no mana is spent |
| **Stats** | **Fixed per skill level** (HP, attack damage, DEF / RES, attack interval, attack range). They do not scale with the summoner's stats, gear or traits |
| **Targetable** | Normal units for rows and targeting: a minion in front shields the units behind it. Statuses affect them as usual |
| **Lifetime** | The whole battle unless killed. They vanish at battle end and never get XP, drops or items, and never become cards |
| **Defeat** | Minions don't keep a battle alive: it is lost when all homunculi are down |
| **Server** | Spawns are server-authoritative, like every roll |
| **Art** | Each minion needs its own sprite set and animations (AssetList.md) |

### 6.12 Battle Result, Stars & Overtime ✅
| Rule | Value (start values) |
|---|---|
| **Time limit** | PvP **60 s**. PvE **90 s per wave group**; PvE timeout = **lose** |
| **Overtime "Unstable Reaction"** | Last **15 s** of each limit: all damage **+15% every 5 s** (max **+45%**); **healing and shields −50%**. UI shows the arena bubbling (Lore.md) |
| **HP %** | Party's current HP ÷ its starting max HP. Knocked-out homunculi count as 0; **minions don't count** |
| **Stars (win)** | ★★★ ≥ 60% HP · ★★ 30–59% · ★ < 30% |
| **PvP timeout** | Both sides standing → higher HP % wins, **★ at most**. Within 1% → **draw**, no stars |
| **Rewards** | PvP rank points scale with stars (exact values with the rank system). PvE stars count toward chapter rewards; 3★ unlocks sweep |
| **Why** | Fights normally end in ~25–45 s; HP % (not raw HP) keeps tank teams from winning timeouts; overtime and the ★ cap stop turtling |

---

## 7. Mining (outline)
A spot where players obtain basic cards. **Mechanic TBD.** Candidate approaches:

| Approach | Description | Effort |
|---|---|---|
| Idle expedition | Send spare heroes to a mine for X hours, then collect cards | Low |
| Farming-style plots | Place/plant, wait, harvest; plots can be upgraded | Medium |
| Mini-game | Short active mining game (tap/dig) for cards | Medium–High |

Planned to be discussed later.

---

## 8. Art Direction — Card-Based

**Card anatomy (draft):**
```
┌─────────────────────┐
│ [Tier ★★]   [Icon]  │  ← tier + category icon
│                     │
│     ARTWORK         │
│                     │
│ NAME          Lv. 5 │
│ Role / Subtype      │
│ Salt 12 Mercury 8 Sulfur 4  │  ← hero stats / item effect
│ ◆ ◆ ◇ ◇ ◇           │  ← weapon slots (filled / empty)
│ [Unique Skill]      │  ← highlighted by rarity
└─────────────────────┘
```
- **Frame color = category** (3 colors). **Stars = Tier.** Basic card rarity is **not** printed on cards, since it rotates each season (§4.2.2). Unique-skill rarity shows on the skill banner.
- Stackable items show a count badge (×3).
- Battle scene: diagonal view. Heroes need **back-¾ and front-¾** views (§6.1). Card art is used for cards and skill buttons; battle characters are separate assets.

## 9. Audio Direction
- Key SFX: card pick-up/drop, **fusion success**, **new discovery**, **no reaction**, **Gold skill reveal**, **5-slot gear reveal**, skill activation.
- Music: TBD.

---

## 10. Prototype Scope ⭐

**Prototype 1 — the question it must answer:**
> _"Is discovering recipes by fusing cards fun when fusion consumes the ingredients, and are the random rolls exciting?"_

| ✅ IN scope (Prototype 1: Fusion) | ❌ OUT of scope (later) |
|---|---|
| Card inventory UI with drag & drop | Auto-battle (Prototype 2) |
| Fusion: match → consume + create; no match → nothing | Real backend, accounts, PvP, trading (Prototype 3) |
| 3 categories, 15 basics, ~20–30 recipes | Mining |
| Starter pack (30) + Daily Chest (8) + streak chest + Exchange + debug chest | Monetization, seasonal rotation |
| Codex with ??? entries | Final art & audio |
| Unique skill roll + weapon slot roll | XP leveling (stub only) |
| Equip weapon/armor/accessory, socket stones, use potions | |
| **Server-shaped code** (fusion & rolls behind a "service" interface, local for now) | |

**Success criteria:**
- [ ] A new player understands "drag one card onto another" within 30 s
- [ ] Testers keep experimenting for 10+ minutes
- [ ] Testers react to discoveries, skill rolls, and slot rolls
- [ ] No soft-lock

---

## 11. UI / UX
| Screen | Contents |
|---|---|
| Main menu / Home | Daily Chest, Fusion, Party, Battle, Codex, (Market, Mine: later) |
| **Fusion board** | Card grid (filter: Hero / Gear / Item), drag & drop fusion |
| Card detail | Stats, gear, skills, slots, level |
| Hero equip | Weapon / Armor / Accessory slots, **skill tree** (spend skill points; branch choice shows a **permanent** warning) and **skill loadout** (pick 2 actives) |
| Gear socket | Gear slots + Magic Stone inventory |
| Codex | Discovered / ??? cards, recipes, progress, first discoverer |
| Result reveal | New card / skill rarity / slot count animation |
| Formation | 3×3 grid editor, place 5 heroes (PvE party / PvP defense) |
| Battle | Diagonal auto-battle view + hybrid HUD: 5 hero buttons, 2-skill bar, 2 consumable buttons (§6.1.1, Prototype 2) |

---

## 12. Online, Trading & Monetization Notes
- **Server-authoritative:** the server owns player inventories, recipes, random rolls, battle rewards, and trades. The client only sends requests ("fuse card #A with #B") and displays results. This prevents cheating and duplication, which is essential once trading exists.
- **Backend:** TBD in the Technical Design (candidates: Unity Gaming Services, PlayFab, Nakama, custom).
- **Gacha regulation:** if any random roll is ever tied to real money, publish odds and check loot-box laws per region.
- **Trading safeguards** (later): trade confirmation, possible trade cooldowns or level requirements to reduce bots and alt-account abuse.

---

## 13. Open Questions & Risks
| # | Question / Risk | Status |
|---|---|---|
| 1 | Basic card types per category | ✅ 5 per category (now 15 total with 3 categories). Confirm |
| 2 | Card sources | ✅ Starter 30, Daily Chest 8, drops, mining, PvP rewards; trading |
| 3 | Fused hero level | ✅ Resets to Lv. 1 |
| 4 | Cross-category fusion | ✅ Same category only |
| 5 | Categories | ✅ Hero, Gear, Item (v0.13: Weapon renamed Gear, holds weapons and armor) |
| 6 | Is Armor an Item subtype? | ✅ No longer: Armor is Gear (v0.13) |
| 7 | Accessory slot | ✅ One slot: Ring or Necklace |
| 8 | Magic Stones | ✅ Risk-based attach/detach; fail = stone destroyed, gear kept. Armor rolls slots too. Rates tuned in playtests |
| 9 | Starter pack guarantees (min. heroes, fusable pair)? | ✅ 30 cards: at least 5 heroes and 1 fusable pair per category |
| 10 | Party size | ✅ 5 heroes, 3×3 grid (grid size proposed) |
| 11 | Unique skill: from which tier? Pity? Re-roll? | ✅ All heroes incl. basics (rolled when obtained); pure re-roll on fusion; no pity, no re-roll item; no tier scaling |
| 12 | PvP: async or real-time? | ✅ Async (proposed, kept) |
| 13 | Potions usable during battle? | ✅ Yes: 2 shared slots, bottom-right; Potions & Bombs (§6.5) |
| 14 | Inventory limit, currencies | ✅ Collection unlimited, identical cards stack; 2 shared battle consumable slots; Coins (soft) + Gems (premium) |
| 15 | Mining mechanic | Later |
| 16 | Backend technology | Open (Technical Design) |
| 17 | Risk: online scope is much bigger than offline | Mitigate: offline Prototype 1 with server-shaped code |
| 18 | Risk: recipes go public fast | Mitigate: §5.4 (server-only recipes, events, first-discoverer) |
| 19 | Working title | ✅ **Fuseborn** (working title; check trademarks and store availability before any public release) |
| 20 | Battle character art: 2D sprites with 2 facings, 2D skeletal (Spine), or low-poly 3D? | Deferred: prototypes use greybox; decide after combat is proven fun |
| 21 | Grid size (3×3?) and whether lanes matter | ✅ 3×3, lanes matter |
| 22 | Battle stamina / energy limit for PvE? | ✅ No stamina. Pace with drop rates and daily-limited rewards (proposed: card drops on the first N clears per day, then XP and Coins only) |
| 23 | Elements or damage types (fire/water…) for counters? | ✅ Hybrid: Physical vs Magic (DEF/RES); elements only as Magic Stone effects (§6.9) |
| 24 | Basic card rarity split (2/2/1) and weights (65/30/5)? | ✅ Confirmed |
| 25 | Exchange | ✅ 10 → Small Chest, 25 → Big Chest (contents proposed); daily limit? |
| 28 | Seasonal rarity rotation | ✅ Per season (4–6 weeks, exact length TBD); odds public, card mapping hidden |
| 29 | Weekly Rare guarantee | ✅ 1 Rare / week; proposed via 7-day streak chest |
| 30 | Hero roles for the 22 heroes (§15) | Proposed; role balance to adjust |
| 31 | 5th Item basic (Armor moved to Gear) | ✅ Item basics are now 5 junk materials (§15.8) |
| 33 | Platform: PC or mobile? | Open. The battle HUD is designed for both (§6.1.1) |
| 34 | Mobile: left hero column vs party at the bottom-left | Check in Prototype 2 |
| 35 | World name (Alembria is a placeholder), guild base name, named rival guilds? | Open |
| 32 | Does Move Speed matter in battle (do heroes move, e.g. melee running to targets)? | ✅ Yes: melee heroes run to targets; ranged stay in place (§6.2) |
| 36 | When the level cap rises above 30, what do the extra skill points buy (capstone skill, Lv. 6, etc.)? | Open; decide with the cap raise (§4.6.4) |
| 37 | Should souled vs soulless homunculi (Lore.md) ever matter in battle or fusion (e.g. soulless immune to Sleep/Confuse)? | Open; lore only for now |
| 38 | Board & range: attack range per homunculus and whether every homunculus can move | ✅ 3 × 8 board, ranges in tiles, free movement, allies don't block (§6.2); results & overtime (§6.12). Tower/furnace objective parked: needs revive or deployment |
| 26 | Naming: card rarity and unique-skill rarity both use "Common/Rare". Use different labels to avoid confusion? | ✅ Skills use Bronze / Silver / Gold |
| 27 | Risk: many random layers (card rarity, skill roll, slot roll, socket chance) can feel like a slot machine | Mitigate: progress never depends only on luck; Exchange, trading, pity |

---

## 14. Change History
| Version | Date | Changes |
|---|---|---|
| 0.33 | 2026-11-05 | Board 3 × 8 (3 × 3 per side + 2 middle rows), square tiles for placement & range (Melee 1 / Short 3 / Medium 5 / Long 7), free movement, allies don't block, 4 melee per target + retarget; PvP 60 s, overtime, HP % tiebreak, stars (§6.12); §13 #38 closed |
| 0.32 | 2026-11-04 | Roles become labels with a core tool; initial role + branch roles (lore-limited, one branch keeps the initial role); STR/AGI/MAG → Salt/Mercury/Sulfur with a designer-set dominant principle and Resonance (+10%); growth rules; attack type and DEF growth per homunculus; Taunt not Tank-only; §13 #38 board & range |
| 0.31 | 2026-11-03 | Tone "hopeful, with weight" and souls (lore only, Lore.md; §13 #37); Terms: hero = homunculus; 1–3 branches per hero (max 3), 1-branch heroes open it automatically; budget unchanged; new targeting rule "Same lane, back-most" (§6.4); statuses Ensnare, Sleep and Curse (§6.10); Summons (§6.11) |
| 0.30 | 2026-11-03 | Every skill has 5 levels: 6 × 5 = 30 points, all on the hero's own skills; Scroll skills cost no points and level up with duplicate Scrolls; Tier I tables extended; §13 #36 |
| 0.29 | 2026-11-03 | Tank DEF rule (§6.9): Tanks get base DEF 6 + 0.3 DEF per level so they out-armor AGI heroes; Tobin updated |
| 0.28 | 2026-11-03 | Tier I hero drafts: Wren (Elf – Archer), Elsie (Angel – Priest), Snick (Goblin – Rogue), Grum (Orc – Warlock); statuses Bleed, Weaken, Untargetable, Knockback added; Tobin approved |
| 0.27 | 2026-11-03 | Branching skill tree: unlocks by skill level, core A1 → A2 + core passive, 3 permanent branches of 2 actives + 1 passive, 22-point kit; level-up gives growth + 1 skill point; status effects list (§6.10) with −50% duration cap |
| 0.26 | 2026-11-03 | Character-name rule (one name per hero type, card shows "Name · Race – Class"); Knight pilot reworked as Tobin (insecure homunculus, junk pot-lid shield) |
| 0.25 | 2026-11-03 | Trait pool (`TraitPool.md`): 15 hero, 12 gear, 12 accessory traits with Bronze/Silver/Gold, tags and % stat caps; gear has a 30% trait chance; accessories always roll one |
| 0.24 | 2026-11-03 | Dota-style attributes (main stat +1 damage, universal STR/AGI/MAG rates), mana + cooldown skills, Dota armor formula, % stats only from gear/items/passives/traits, skill tree (3 actives, 2 passives, skill points), weapon families, per-hero files in `Docs/Design/Heroes/` |
| 0.23 | 2026-11-03 | World & Story: alchemy world, Great Codex, player guild of homunculi, Runoff monsters, light-adventure tone (Lore.md) |
| 0.22 | 2026-11-02 | Heroes have a skill pool (leveling + Scrolls) and bring 2 skills into battle; hybrid select-then-cast HUD for PC and mobile; consumables bottom-right, Potion & Bomb only; Scrolls teach skills |
| 0.21 | 2026-11-02 | Combat numbers (§6.9): Physical/Magic damage with DEF/RES, derived stat formulas, damage formula, stone elemental riders, consumable slot limits |
| 0.20 | 2026-11-02 | 3×3 grid with lanes; no PvE stamina; hero level cap 30 (raisable) with per-hero growth |
| 0.19 | 2026-11-02 | Working title: Fuseborn |
| 0.18 | 2026-11-02 | Currencies Coins + Gems; unlimited collection with identical-card stacking; 2 shared consumable slots in battle |
| 0.17 | 2026-11-02 | Every hero rolls a unique skill, basics included (at chest open); pure re-roll on fusion; no pity; skill rarity Bronze/Silver/Gold; hero tier = recipe depth, not power; starter pack and basic rarity confirmed |
| 0.16 | 2026-11-02 | Melee heroes run to targets (Move Speed matters); consumables usable in battle via limited slots; battle art deferred; next focus: combat design |
| 0.15 | 2026-11-01 | Item tree: 5 junk basics (Stone, Seed, Log, Bone, Scrap Metal) → 12 Tier II → 13 Tier III materials → 10 Tier IV and 15 Tier V usable items; Item subtypes and accessory types expanded (§15.8) |
| 0.14 | 2026-11-01 | Armor pieces (Body/Helmet/Gloves/Boots) share the Armor slot; gear bonus stats; 11 Tier III Gear recipes from 55 pairs (§15.7) |
| 0.13 | 2026-11-01 | Weapon category renamed **Gear** (weapons + armor); Armor removed from Item; 5 Gear basics (3 weapons, 2 armor) and 11 Tier II Gear recipes, 4 no-match (§15.7) |
| 0.12 | 2026-10-31 | Merged with the hero sheet: kept 4 new and 4 re-raced Tier III heroes (renamed by the naming rules); 28 heroes; role balance 4/3/5/4/5/7 |
| 0.11 | 2026-10-31 | Hero naming rules; 14 Race–Class renames; 2 new Rangers (Wood Elf – Hunter, Dwarf – Gunner); Tier III alternate recipes; role balance 3/3/4/4/4/6; HeroPool.md |
| 0.10 | 2026-10-30 | Hero list: 5 Tier I, 11 Tier II, 6 Tier III; Race–Class naming; surprise-recipe philosophy; fixed role list |
| 0.9 | 2026-10-30 | Seasonal rarity rotation confirmed |
| 0.8 | 2026-10-29 | Seasonal rarity rotation (hidden mapping, public odds); weekly Rare guarantee; Exchange (10 → Small, 25 → Big Chest); alternate-recipe rule; base Rare rate 5% |
| 0.7 | 2026-10-29 | Daily Chest fully random (no pair guarantee); basic card rarity (Common/Uncommon/Rare) with drop weights; recipe-path rule; duplicate Exchange proposal |
| 0.6 | 2026-10-29 | Combat design: diagonal view, 5-hero 3×3 grid, 6 roles, per-hero targeting priority, bottom skill bar, per-hero cooldowns (MAG), passive unique skills, PvE waves, async PvP; stone failure rule decided |
| 0.5 | 2026-10-29 | Armor = Item subtype; one accessory slot (Ring or Necklace); risk-based Magic Stone attach/detach; party size 4–5 |
| 0.4 | 2026-10-29 | 3 categories (Hero/Weapon/Item); online game; starter pack 30; Daily Chest 8; recipe-sharing strategy; hero leveling via party, STR/AGI/MAG, 3 equipment slots; weapon 0–5 random slots + Magic Stones; auto-battle and mining outlines |
| 0.3 | 2026-10-29 | Resolved: basics per category, layered card sources, hero level reset, same-category fusion |
| 0.2 | 2026-10-29 | Defined core concept: card fusion, categories, consumption rule, tiers, unique-skill gacha, Codex, prototype scope |
| 0.1 | 2026-10-29 | Template created |

---

## 15. Content Lists
### 15.1 Hero Naming & Recipe Philosophy ✅
- Each hero is **Race – Class**, e.g. *Elf – Archer* (an elf whose main weapon is a bow, with longer attack range).
  - **Race:** free and diverse; mainly drives the look.
  - **Class:** free flavor name (Knight, Commander, Engineer…).
  - **Role:** a **label** from a fixed list: Tank, Warrior, Ranger, Assassin, Mage, Support (§6.3). Each hero has an initial role; branches may reach other roles (§4.6.4).
- ✅ **Recipes are intentionally surprising.** A result's race and class do **not** have to follow from the ingredients (Human + Human can give an Angel). Discovery comes from experimenting, hints, and community sharing, not from deduction.
- ✅ **Naming rules:**
  1. A class is **never a role word** (no "– Tank", "– Support"), and avoids near-role words (Healer, Buffer).
  2. **Each class name is used once** across the roster (no two "Knights").
  3. A compound race only when it's a known type (Dark Elf, Light Elf, Wood Elf, Half-Angel), not a mash-up (no "Goblin Zombie").
  4. ✅ **Character name:** each Race – Class has **one character name**, shown on the card as **"Name · Race – Class"** (e.g. *Tobin · Human – Knight*). All copies share it; the rolled trait makes each copy unique. Names are humble or fit the personality, and never copy a real person or an existing game's character.
- Race and class pools for future heroes: [HeroPool.md](HeroPool.md).
- **Initial-role balance (28 heroes):** Tank 4 · Warrior 3 · Ranger 5 · Assassin 4 · Mage 5 · Support 7.
- Source of truth: [Hero recipe sheet](https://docs.google.com/spreadsheets/d/1r2Nj3ZUcm3-e148e-pixrB-15U9P9bdaQpWJdFwOqZo/edit?gid=0#gid=0) (cross-section grid). This section mirrors it. Synced with the sheet in v0.12.

### 15.2 Heroes — Tier I (Basic)
| # | Hero | Role |
|---|---|---|
| H1 | Human – Knight | Tank |
| H2 | Elf – Archer | Ranger |
| H3 | Angel – Priest | Support |
| H4 | Goblin – Rogue | Assassin |
| H5 | Orc – Warlock | Mage |

Per-hero content (backstory, stats, skill tree, equipment, illustrator brief): `Docs/Design/Heroes/` (index in its README; pilot: Human – Knight).

### 15.3 Heroes — Tier II (Tier I + Tier I)
| + | Knight | Archer | Priest | Rogue | Warlock |
|---|---|---|---|---|---|
| **Knight** | Human – Commander | | | | |
| **Archer** | Human – Thief | Wood Elf – Hunter 🆕 | | | |
| **Priest** | Fairy – Druid | Light Elf – Bard | Angel – Crusader | | |
| **Rogue** | Goblin – Shieldbearer | Dark Elf – Nightblade | ✗ | Goblin – Saboteur | |
| **Warlock** | Human – Wizard | Oni – Berserker | ✗ | Dwarf – Gunner 🆕 | Hobgoblin – Brute |

| Result | Recipe | Role |
|---|---|---|
| Human – Commander | Knight + Knight | Support (leader buffs) |
| Human – Thief | Knight + Archer | Assassin |
| Wood Elf – Hunter 🆕 | Archer + Archer | Ranger |
| Fairy – Druid | Knight + Priest | Support |
| Light Elf – Bard | Archer + Priest | Support |
| Angel – Crusader | Priest + Priest | Warrior |
| Goblin – Shieldbearer | Knight + Rogue | Tank |
| Dark Elf – Nightblade | Archer + Rogue | Assassin |
| Goblin – Saboteur | Rogue + Rogue | Assassin (bombs, traps) |
| Human – Wizard | Knight + Warlock | Mage |
| Oni – Berserker | Archer + Warlock | Warrior |
| Dwarf – Gunner 🆕 | Rogue + Warlock | Ranger |
| Hobgoblin – Brute | Warlock + Warlock | Tank |

No match (✗): Priest + Rogue, Priest + Warlock. Two "no reaction" pairs are kept on purpose in Tier II.

### 15.4 Heroes — Tier III (Tier II + Tier I)
| Result | Recipe 1 | Recipe 2 | Role |
|---|---|---|---|
| Dwarf – Engineer | Human – Commander + Knight | Dwarf – Gunner + Knight | Ranger |
| Skeleton – Necromancer | Human – Thief + Warlock | Human – Wizard + Rogue | Mage |
| Wraith – Runecaster | Fairy – Druid + Rogue | _TBD_ | Mage |
| Troll – Marksman | Goblin – Shieldbearer + Archer | _TBD_ | Ranger |
| Half-Angel – Oracle | Human – Wizard + Priest | _TBD_ | Support |
| Dryad – Shaman | Light Elf – Bard + Priest | Fairy – Druid + Warlock | Support |
| Slime – Alchemist | Oni – Berserker + Rogue | Hobgoblin – Brute + Priest | Mage (poison, debuffs) |
| Wisp – Mender | Angel – Crusader + Archer | Fairy – Druid + Priest | Support |
| Minotaur – Brawler | Goblin – Saboteur + Warlock | Oni – Berserker + Knight | Warrior |
| Golem – Guardian | Hobgoblin – Brute + Knight | _TBD_ | Tank |

### 15.5 Notes & To-Do (heroes)
- ✅ Class names: role words and duplicates replaced (§15.6).
- ✅ Role balance (28 heroes): Tank 4 · Warrior 3 · Ranger 5 · Assassin 4 · Mage 5 · Support 7.
- Second recipe still needed for: Wraith – Runecaster, Troll – Marksman, Half-Angel – Oracle, Golem – Guardian.
- Tier II + Tier II combinations: not designed yet.
- Stats, default weapon, active skill, targeting per hero: TBD.

### 15.6 Revision Log
| Tier | Old | New | Role change | Reason |
|---|---|---|---|---|
| I | Goblin – Assassin | Goblin – Rogue | — | Class was a role word |
| II | Angel – Warrior | Angel – Crusader | — | Class was a role word |
| II | Goblin – Knight | Goblin – Shieldbearer | — | Duplicate of Human – Knight |
| II | Goblin – Thief | Goblin – Saboteur | — | Duplicate of Human – Thief |
| II | Dark Elf – Assassin | Dark Elf – Nightblade | — | Class was a role word |
| II | Fairy – Healer | Fairy – Druid | — | Near-role word |
| II | Light Elf – Buffer | Light Elf – Bard | — | Near-role word |
| II | Oni – Support | Oni – Berserker | Support → Warrior | Oni fits a brute; fewer Supports |
| II | Hobgoblin – Tank | Hobgoblin – Brute | — | Class was a role word |
| II | ✗ (Archer + Archer) | Wood Elf – Hunter | New, Ranger | More Rangers |
| II | ✗ (Assassin + Warlock) | Dwarf – Gunner | New, Ranger | More Rangers |
| III | Skeleton – Mage | Skeleton – Necromancer | — | Class was a role word |
| III | Elemental – Buffer | Elemental – Conduit | — | Near-role word |
| III | Goblin Zombie – Support | Zombie – Plague Doctor | Support → Mage | Compound race; fewer Supports |
| III | Wisp – Healer | Wisp – Mender | — | Near-role word |
| III | Beast – Warrior | Beastkin – Brawler | — | Vague race; class was a role word |
| III | — | Recipe 2 for all 6 heroes | — | Alternate-recipe rule |

**v0.12: merged with the sheet's newer Tier III heroes** (the sheet's races were kept; classes renamed by the naming rules)
| Recipe | Sheet name | v0.11 GDD name | Final name | Role |
|---|---|---|---|---|
| Commander + Knight | Dwarf – Engineer | Human – Engineer | **Dwarf – Engineer** | Ranger |
| Druid + Rogue | Wraith – Runecaster | — (new) | **Wraith – Runecaster** | Mage |
| Shieldbearer + Archer | Troll – Marksman | — (new) | **Troll – Marksman** | Ranger |
| Wizard + Priest | Half Angel – Support | — (new) | **Half-Angel – Oracle** | Support |
| Bard + Priest | Dryad – Buffer | Elemental – Conduit | **Dryad – Shaman** | Support |
| Berserker + Rogue | Slime – Support | Zombie – Plague Doctor | **Slime – Alchemist** | Mage |
| Saboteur + Warlock | Minotaur – Warrior | Beastkin – Brawler | **Minotaur – Brawler** | Warrior |
| Brute + Knight | Golem – Guardian | — (new) | **Golem – Guardian** | Tank |
| Archer + Warlock | Oni – Shaman | Oni – Berserker | **Oni – Berserker** | Warrior |

### 15.7 Gear (proposed, to be sorted)
**Tier I (basic): 3 weapons, 2 armor**
| # | Card | Slot | Leans to |
|---|---|---|---|
| 1 | Sword | Weapon | Salt |
| 2 | Bow | Weapon | Mercury |
| 3 | Staff | Weapon | Sulfur |
| 4 | Iron Mail | Armor | Salt, heavy |
| 5 | Cloth Robe | Armor | Sulfur, light |

**Tier II grid** (15 pairs: 11 results, 4 ✗). Source: `Docs/Design/Data/GearGrid.tsv`. Mirrored in the sheet's **Gear** tab.
| | Sword | Bow | Staff | Iron Mail | Cloth Robe |
|---|---|---|---|---|---|
| **Sword** | Greatsword | Twin Daggers | ✗ | Tower Shield | ✗ |
| **Bow** | | Crossbow | Lute | ✗ | Shadow Cloak |
| **Staff** | | | Grimoire | Rune Mail | Sage Robe |
| **Iron Mail** | | | | Plate Armor | Leather Armor |
| **Cloth Robe** | | | | | ✗ |

**Tier II results**
| Result | Recipe | Slot | Best role fit |
|---|---|---|---|
| Greatsword | Sword + Sword | Weapon | Warrior |
| Crossbow | Bow + Bow | Weapon | Ranger |
| Grimoire | Staff + Staff | Weapon | Mage |
| Twin Daggers | Sword + Bow | Weapon | Assassin |
| Tower Shield | Sword + Iron Mail | Weapon | Tank |
| Lute | Bow + Staff | Weapon | Support |
| Plate Armor | Iron Mail + Iron Mail | Armor | Tank |
| Shadow Cloak | Bow + Cloth Robe | Armor | Assassin / Mercury |
| Sage Robe | Staff + Cloth Robe | Armor | Mage / Sulfur |
| Rune Mail | Staff + Iron Mail | Armor | Sulfur + defense hybrid |
| Leather Armor | Iron Mail + Cloth Robe | Armor | Ranger / Mercury |

No match: Cloth Robe + Cloth Robe, Sword + Staff, Sword + Cloth Robe, Bow + Iron Mail.

**Tier III (Tier II + Tier I): 11 results from 55 pairs, 44 ✗.** Source: `Docs/Design/Data/GearGridTier3.tsv`.
| Result | Recipe | Slot · piece | Bonus focus | Role fit |
|---|---|---|---|---|
| Iron Gauntlets | Greatsword + Iron Mail | Armor · Gloves | Salt, ATK | Warrior |
| Arcane Repeater | Crossbow + Staff | Weapon | Attack Speed, Sulfur | Ranger |
| Wizard Hat | Grimoire + Cloth Robe | Armor · Helmet | Cooldown Reduction, Sulfur | Mage |
| Silent Boots | Twin Daggers + Cloth Robe | Armor · Boots | Move Speed, Evasion | Assassin |
| Knight Helm | Tower Shield + Sword | Armor · Helmet | DEF, Control Resist | Tank |
| War Drum | Lute + Iron Mail | Weapon | Team Attack Speed aura | Support |
| Thorn Plate | Plate Armor + Sword | Armor · Body | DEF, Thorns | Tank |
| Nightgrip Gloves | Shadow Cloak + Bow | Armor · Gloves | Crit Chance, Attack Speed | Assassin |
| Elder Staff | Sage Robe + Staff | Weapon | Skill Power, Sulfur | Mage / Support |
| Runeblade | Rune Mail + Iron Mail | Weapon | Salt + Sulfur hybrid | Warrior |
| Hunter's Boots | Leather Armor + Bow | Armor · Boots | Move Speed, Mercury | Ranger |

Mix: 4 weapons, 7 armor (1 body, 2 helmets, 2 gloves, 2 boots). Each Tier II card is used once.
To-do: exact stat values, second recipes for key results, Tier II + Tier II gear.

### 15.8 Items (proposed, to be sorted)
Junk materials climb two tiers before they become usable items. Effects of Tier IV–V items: TBD. Grids in `Docs/Design/Data/ItemGridT2.tsv` … `ItemGridT5.tsv`.

**Tier I (basic materials):** Stone · Seed · Log · Bone · Scrap Metal

**Tier II (Tier I + Tier I): 12 results, 3 ✗**
| Pair | Result |
|---|---|
| Stone + Stone | Flint |
| Seed + Seed | Sprout |
| Log + Log | Plank |
| Bone + Bone | Bone Dust |
| Scrap Metal + Scrap Metal | Rusty Nail |
| Stone + Seed | Moss |
| Stone + Bone | Chalk |
| Stone + Scrap Metal | Raw Ore |
| Seed + Log | Mushroom |
| Log + Bone | Glue |
| Log + Scrap Metal | Charcoal |
| Bone + Scrap Metal | Fishhook |

No match: Stone + Log, Seed + Bone, Seed + Scrap Metal.

**Tier III (Tier II + Tier I): 13 results from 16 recipes, 44 ✗**
| Result | Recipe 1 | Recipe 2 |
|---|---|---|
| Iron Ingot | Raw Ore + Log | Charcoal + Scrap Metal |
| Silver Nugget | Rusty Nail + Stone | Raw Ore + Bone |
| Healing Herb | Sprout + Seed | Moss + Seed |
| Crystal Shard | Flint + Stone | |
| Clay | Chalk + Stone | |
| Resin | Plank + Seed | |
| Rope | Moss + Log | |
| Glowcap | Mushroom + Bone | |
| Ash | Charcoal + Log | |
| Pearl | Fishhook + Bone | |
| Old Coin | Rusty Nail + Scrap Metal | |
| Ink | Bone Dust + Log | |
| Wax | Glue + Seed | |

**Tier IV (Tier III + Tier I): 10 usable items, 55 ✗**
| Result | Recipe | Type |
|---|---|---|
| Minor Healing Potion | Healing Herb + Stone | Potion |
| Mana Tonic | Glowcap + Seed | Potion |
| Smoke Bomb | Ash + Scrap Metal | Bomb |
| Spell Scroll | Ink + Log | Scroll |
| Ward Charm | Wax + Bone | Charm (socketing protection, §4.7.2) |
| Rough Magic Stone | Crystal Shard + Stone | Magic Stone |
| Iron Ring | Iron Ingot + Bone | Ring |
| Silver Necklace | Silver Nugget + Scrap Metal | Necklace |
| Pearl Amulet | Pearl + Seed | Amulet |
| Twig Crown | Rope + Log | Crown |

**Tier V (Tier III + Tier II): 15 better items, 141 ✗**
| Result | Recipe | Type |
|---|---|---|
| Greater Healing Potion | Healing Herb + Mushroom | Potion |
| Mana Elixir | Glowcap + Sprout | Potion |
| Soothing Salve | Wax + Moss | Potion |
| Fire Bomb | Ash + Charcoal | Bomb |
| Rune Scroll | Ink + Glue | Scroll |
| Guardian Charm | Rope + Chalk | Charm |
| Lucky Coin | Old Coin + Fishhook | Charm |
| Polished Magic Stone | Crystal Shard + Chalk | Magic Stone |
| Ember Stone | Crystal Shard + Charcoal | Magic Stone |
| Moonstone Ring | Silver Nugget + Flint | Ring |
| Pearl Necklace | Pearl + Fishhook | Necklace |
| Amber Pendant | Resin + Plank | Necklace |
| Ancestor Amulet | Clay + Bone Dust | Amulet |
| Iron Crown | Iron Ingot + Rusty Nail | Crown |
| Gilded Crown | Old Coin + Raw Ore | Crown |

Scrolls (Spell Scroll, Rune Scroll) teach heroes skills outside battle (§4.8). Every Tier II and Tier III card is used in Tier V. To-do: effects, second recipes for key Tier IV–V items, Tier II + Tier II items.

### Recipe Table
Hero recipes: see §15.3–15.4. Gear recipes: see §15.7. Item recipes: see §15.8.
