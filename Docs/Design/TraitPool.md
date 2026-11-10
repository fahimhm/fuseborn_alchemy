# Trait Pool — Fuseborn

> Source of truth for every rolled trait. Rules: GDD §4.6.4 (traits), §4.7 (gear), §4.8 (items), §6.9 (combat numbers and stat definitions). Lore: a homunculus's trait is its **innate trait**, a rare gift ([Lore.md](Lore.md)).

**Status:** Draft (start values, all tunable in ScriptableObjects)

## 1. Rules
| Rule | Value |
|---|---|
| **Who can roll** | **Homunculi, gear and accessories**, each with a **30% chance** of 1 trait when born (chest, starter pack or drop for basics; fusion for the rest). **Most cards have no trait, and that's intended.** Never: materials, potions, throwables, scrolls, charms, magic stones (they stack). **Gear with a fixed skill never rolls a trait** (GDD §4.7.6). Gear traits roll separately from the 0–5 stone slots |
| **Rarity** (if a trait rolls) | **Faint 65% · Bright 27% · Radiant 8% · Unique** (special, §2) |
| **Pool** | Each card rolls only from its own pool (Homunculus → §4, Gear → §5, Accessory → §6). Gear traits marked Weapon / Armor / Shield only roll on that kind of gear |
| **Block traits** | Only roll where Block works: on **Shield-family gear**, and on homunculi with a **built-in shield** (e.g. Tobin). Block does nothing on anyone else (GDD §6.9) |
| **Tags** | Rolls **ignore tags**: a misfit trait is worth trading to someone it fits (§3) |
| **Fusion** | Pure re-roll: ingredient traits never affect the result's roll. Fusing a card with a trait shows a **warning** naming it; Bright and up warn more strongly; **Unique** needs hold-to-confirm |
| **Tier** | Trait strength **does not scale with tier** (tier = recipe depth) |
| **Bad luck** | No pity, no re-roll item. Trading is the answer (GDD §4.9) |
| **Per homunculus in battle** | Up to 3 traits: its own + its gear's (weapon and/or armor) + its accessory's. Same stat from several sources adds up (Block stacks multiplicatively), then the caps in §7 apply |
| **Server** | All rolls happen on the server through a service (e.g. `ITraitRollService`), including the world-wide Unique registry; the client only shows the result |
| **Data** | One ScriptableObject per trait later: `SO_Trait_<Name>` |

## 2. Rarity Ladder
All traits are **passive**: none is an active skill, none needs a button or a battle slot.

| Rarity | Odds | Kind of effect | Strength guide |
|---|---|---|---|
| **Faint** | 65% | **Always on:** a plain stat bonus | ≈ **6 GP** (a Tier II gear; GDD §4.7.4 rates). About **10–15%** of Faint traits are harmless **jokes** (pure "cursed" comedy, marked 🃏) |
| **Bright** | 27% | **Conditional** (works only under a condition, e.g. below 30% HP) or **triggered** (fires when something happens, e.g. each basic hit). May be **ironic** | ≈ **10–12 GP**, conditional |
| **Radiant** | 8% | **Build-defining, rule-bending.** May be **ironic**: big upside, real downside | By judgment |
| **Unique** | special | **One in the whole game world** | About Radiant, but flashier |

**Irony and comedy:** pure jokes only at Faint. From Bright up, every downside comes with a real upside (*high risk, high reward*), so a lucky roll is never just a punishment.

**Unique traits (one and only)**
- Each Unique trait is a specific named trait that **only one card in the game** can hold at a time (one per server if regions ever split).
- It can drop (tiny chance, e.g. **0.1%** of trait rolls) only while **unowned**.
- It **returns to the pool** when its card is fused or destroyed, or when its owner has been inactive for about **6 months**, with a world announcement (e.g. *"The First Flame has been released."*).
- Shown with a special name, a **visual aura**, and a Codex entry naming the current owner. A badge of honor, not an automatic win.

## 3. Tags
Tags say what a trait is good for. Homunculus files list their **fitting tags**; the UI shows a "Good fit" badge when a rolled trait shares one. Tags **never change roll odds**.

| Tag | Meaning | Usually suits (roles are labels, guidance only) |
|---|---|---|
| **Guard** | HP, DEF / RES, Block, shields, survival | Tank, Warrior |
| **Physical** | Better basic hits and physical damage | Warrior, Ranger, Assassin |
| **Magic** | Mana, skills, magic damage | Mage, Support |
| **Crit** | Crit chance or crit payoff | Assassin, Ranger |
| **Speed** | Attack Speed, Move Speed, Evasion | Assassin, Ranger |
| **Sustain** | Self-healing, Lifesteal, regen | Warrior, Tank |
| **Support** | Helps allies (heals, buffs, protection) | Support, Tank |
| **Control** | Applies or resists control (soft: Slow, Ensnare, Blind…; hard: Stun, Sleep, Freeze…) | Tank, Mage |
| **Universal** | Useful on any card | All |
| **Joke** 🃏 | Pure comedy, little or no effect | Nobody (trade it as a meme) |

## 4. Homunculus Traits (17)
The homunculus's innate trait: passive, always on, separate from the skill tree.

| ID | Trait | Rarity | Effect (start values) | Tags |
|---|---|---|---|---|
| HT01 | Thick Hide | Faint | +4% max HP | Guard |
| HT02 | Keen Eye | Faint | +3% Crit | Crit, Physical |
| HT03 | Light Step | Faint | +2.4% Evasion | Speed |
| HT04 | Steady Stance | Faint | **Built-in shield only:** +1.5% Block | Guard |
| HT05 | Quick Hands | Faint | +9 Attack Speed | Speed, Physical |
| HT06 | Deep Well | Faint | +8% max mana | Magic |
| HT07 | Blood Thirst | Faint | +2.4% Lifesteal | Sustain, Physical |
| HT08 | Gentle Touch | Faint | Healing received +10% | Support |
| HT16 | Butterfingers 🃏 | Faint | 5% of basic hits fumble and miss (with a little fumble animation) | Joke |
| HT09 | Last Stand | Bright | Below 30% HP: +6 DEF and +6 RES | Guard |
| HT10 | Staggering Blows | Bright | Basic hits have a 15% chance to **Stagger** the target for 1.5 s | Control, Physical |
| HT11 | Mana Spark | Bright | Each skill cast refunds 15% of its mana cost | Magic |
| HT12 | Shared Spoils | Bright | Heals the lowest-HP ally for 4% of damage this homunculus deals | Support, Sustain |
| HT13 | Battle Rhythm | Bright | Each basic hit gives +2 Attack Speed for 4 s, stacks up to 10 (+20) | Speed, Physical |
| HT17 | Lazy Genius | Bright | Attacks 20% slower, but every 4th basic hit deals ×2 damage | Physical |
| HT14 | Second Wind | Radiant | Once per battle, when knocked out, revives with 30% max HP, **but deals −30% damage** for the rest of the battle | Guard, Sustain |
| HT15 | Arcane Echo | Radiant | Damage and healing skills have a 15% chance to fire again at 50% power (no mana, no cooldown) | Magic, Support |
| HT18 | Glass Cannon | Radiant | +40% damage dealt, −30% max HP | Physical, Magic |

## 5. Gear Traits (14)
Rolled on 30% of new gear cards (never on gear with a fixed skill). **Slot** = which gear can roll it.

| ID | Trait | Rarity | Slot | Effect (start values) | Tags |
|---|---|---|---|---|---|
| GT01 | Honed | Faint | Weapon | +3% Crit | Crit, Physical |
| GT02 | Balanced | Faint | Weapon | +9 Attack Speed | Speed |
| GT03 | Reinforced | Faint | Armor | +1.8 DEF | Guard |
| GT04 | Warded | Faint | Armor | +1.8 RES | Guard, Magic |
| GT05 | Feathered | Faint | Armor | +15 Move Speed, +1.2% Evasion | Speed |
| GT06 | Attuned | Faint | Any | +3% Cooldown Reduction | Magic, Universal |
| GT13 | Squeaky 🃏 | Faint | Armor | Squeaks loudly every time the wearer is hit. No other effect | Joke |
| GT07 | Vampiric | Bright | Weapon | +4% Lifesteal; doubled while below 50% HP | Sustain, Physical |
| GT08 | Spiked | Bright | Armor | +10% Thorns | Guard |
| GT09 | Runed | Bright | Any | +6% Skill Power; +12% instead while above 70% mana | Magic, Support |
| GT10 | Stoneskin | Bright | **Shield** | +3% Block (multiplicative), +10% Control Resist | Guard, Control |
| GT11 | Gem-Hungry | Radiant | Any | Socketed Magic Stone bonuses on this gear +50% | Universal |
| GT12 | Executioner | Radiant | Weapon | Basic hits deal +25% damage to targets below 30% HP | Physical, Crit |
| GT14 | Rusty Edge | Radiant | Weapon | Basic hits apply Bleed (3 s), but the wearer's Crit Chance is halved | Physical |

## 6. Accessory Traits (13)
Rolled on 30% of new accessories (Ring, Necklace, Amulet, Crown); any accessory type can roll any of them. Named accessories also have the usual 30% chance on top of their signature.

| ID | Trait | Rarity | Effect (start values) | Tags |
|---|---|---|---|---|
| IT01 | Vital | Faint | +4% max HP | Guard |
| IT02 | Lucky | Faint | +3% Crit | Crit |
| IT03 | Nimble | Faint | +2.4% Evasion | Speed |
| IT04 | Focused | Faint | Starts battle with +10% mana (60% instead of 50%) | Magic |
| IT05 | Soothing | Faint | Regenerates 1% max HP every 5 s | Sustain |
| IT06 | Steadfast | Faint | +6% Control Resist | Control, Guard |
| IT13 | Itchy 🃏 | Faint | Scratches itself now and then (idle animation only). No other effect | Joke |
| IT07 | Rallying | Bright | Allies in the same lane get +5 DEF for the first 10 s of battle | Support, Guard |
| IT08 | Siphon | Bright | +4% Lifesteal, works on skill damage too | Sustain, Magic |
| IT09 | Arcane Veil | Bright | Battle start: a shield worth 10% max HP that only absorbs magic damage | Guard, Magic |
| IT10 | Hunter's Mark | Bright | Basic hits mark the target for 3 s; marked targets take +8% damage from all allies (does not stack) | Support, Physical |
| IT11 | Guardian Bond | Radiant | 20% of damage taken by the lowest-HP ally is redirected to this homunculus | Guard, Support |
| IT12 | Overflow | Radiant | Starts battle with 100% mana | Magic, Universal |

## 7. Caps (all sources combined)
Stored as tunable data. Gear, items, tree passives and traits all add up to these limits.

| Stat | Cap |
|---|---|
| Crit | 60% |
| Evasion | 40% |
| Block | **60%** (shield bearers only; stacks multiplicatively, GDD §6.9) |
| Lifesteal | 30% |
| Cooldown Reduction | 40% |
| Control Resist | 50% |

## 8. Unique Traits (one in the game world)
Starter ideas; the full list is designed later. Each exists on at most one card at a time (§2).

| Name | Pool | Effect idea |
|---|---|---|
| **All or Nothing** | Homunculus | **60% of basic hits miss**, but hits that land always crit and deal ×3 damage |
| **Heart of the First Flame** | Homunculus | All of its basic hits and skills carry the **Fire** tag; enemies it Burns burn 50% longer |

## 9. Open Questions
1. **Unique traits:** the full list, how many exist at launch, and their exact drop chance.
2. **Joke traits:** confirm the share (10–15% of Faint) after playtests; more jokes per pool.
3. **Accessory budgets** (8 / 12 GP) were set when accessories always rolled a trait; kept on purpose (a trait on an accessory is a lucky find).

## 10. Tag Coverage
| Tag | Homunculus | Gear | Accessory |
|---|---|---|---|
| Guard | HT01, HT04, HT09, HT14 | GT03, GT04, GT08, GT10 | IT01, IT06, IT07, IT09, IT11 |
| Physical | HT02, HT05, HT07, HT10, HT13, HT17, HT18 | GT01, GT07, GT12, GT14 | IT10 |
| Magic | HT06, HT11, HT15, HT18 | GT04, GT06, GT09 | IT04, IT08, IT09, IT12 |
| Crit | HT02 | GT01, GT12 | IT02 |
| Speed | HT03, HT05, HT13 | GT02, GT05 | IT03 |
| Sustain | HT07, HT12, HT14 | GT07 | IT05, IT08 |
| Support | HT08, HT12, HT15 | GT09 | IT07, IT10, IT11 |
| Control | HT10 | GT10 | IT06 |
| Universal | | GT06, GT11 | IT12 |
| Joke | HT16 | GT13 | IT13 |
