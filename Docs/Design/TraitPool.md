# Trait Pool — Fuseborn

> Source of truth for every rolled trait. Rules: GDD §4.6.4 (hero unique skill), §4.7 (gear), §4.8 (items), §6.9 (combat numbers). Lore: a hero's trait is its **innate trait** ([Lore.md](Lore.md)).

**Status:** Draft (start values, all tunable in ScriptableObjects)

## 1. Rules
| Rule | Value |
|---|---|
| **Who rolls** | **Hero:** always, 1 trait, when obtained (basics) or created by fusion. **Gear:** **30% chance** of 1 trait when created, rolled separately from the 0–5 stone slots (§4.7.1). **Accessory** (Ring, Necklace, Amulet, Crown): always, 1 trait, when created. Materials, Potions, Bombs, Scrolls, Charms and Magic Stones never roll a trait |
| **Rarity odds** | Bronze 70% · Silver 25% · Gold 5%, same for all three pools |
| **Pool** | Each card rolls only from its own pool (Hero → §3, Gear → §4, Accessory → §5). Gear traits marked Weapon or Armor only roll on that slot type |
| **Fusion** | Pure re-roll: ingredient traits never affect the result's roll (§4.6.4) |
| **Tier** | Trait strength **does not scale with tier** (tier = recipe depth) |
| **Bad luck** | No pity, no re-roll item. Trading is the answer (§4.9) |
| **Per hero in battle** | Up to 3 traits: own hero trait + weapon or armor trait(s) + accessory trait. Same stat from several sources adds up, then the caps in §6 apply |
| **Gear-only stats** | Cooldown Reduction and Skill Power only appear on **gear traits** (keeps §6.9: CDR and Skill Power come from gear) |
| **Server** | All rolls happen on the server through a service (e.g. `ITraitRollService`); the client only shows the result |
| **Data** | One ScriptableObject per trait later: `SO_Trait_<Name>` |

**Rarity guide**
| Rarity | Kind of effect |
|---|---|
| Bronze | Small flat or % stat, always on |
| Silver | Conditional or triggered effect |
| Gold | Build-defining effect, once-per-battle or rule-bending |

**Stat definitions used here** (proposed; §6.9 does not define them yet, see §7)
- **Crit:** chance for a basic hit to deal 150% damage (§6.9).
- **Evasion:** chance to fully dodge an enemy **basic hit** (not skills).
- **Block:** chance to take **50% less** damage from a physical basic hit.
- **Lifesteal:** heal for this % of **basic-hit** damage dealt (unless the trait says skills too).
- **Thorns:** reflect this % of **melee** damage taken back to the attacker as physical damage.
- **Control Resist:** shortens stuns, slows and other control on this hero by this %.

## 2. Tags
Tags say what a trait is good for. Hero files list their **fitting tags** (`Heroes/_HeroTemplate.md` §7); the UI shows a "Good fit" badge when a rolled trait shares a tag with the hero. Tags **do not change roll odds** (see §7).

| Tag | Meaning | Typical roles |
|---|---|---|
| **Guard** | HP, DEF/RES, Block, shields, survival | Tank, Warrior |
| **Physical** | Better basic hits and physical damage | Warrior, Ranger, Assassin |
| **Magic** | Mana, skills, magic damage | Mage, Support |
| **Crit** | Crit chance or crit payoff | Assassin, Ranger |
| **Speed** | Attack Speed, Move Speed, Evasion | Assassin, Ranger |
| **Sustain** | Self-healing, Lifesteal, regen | Warrior, Tank |
| **Support** | Helps allies (heals, buffs, protection) | Support, Tank |
| **Control** | Applies or resists stuns and slows | Tank, Mage |
| **Universal** | Useful on any hero | All |

## 3. Hero Traits (15: 8 Bronze, 5 Silver, 2 Gold)
The hero's innate trait, passive and always on, separate from the skill tree (§4.6.4).

| ID | Trait | Rarity | Effect (start values) | Tags |
|---|---|---|---|---|
| HT01 | Thick Hide | Bronze | +6% max HP | Guard |
| HT02 | Keen Eye | Bronze | +6% Crit | Crit, Physical |
| HT03 | Light Step | Bronze | +6% Evasion | Speed |
| HT04 | Steady Stance | Bronze | +8% Block | Guard |
| HT05 | Quick Hands | Bronze | +10 Attack Speed | Speed, Physical |
| HT06 | Deep Well | Bronze | +15% max mana | Magic |
| HT07 | Blood Thirst | Bronze | +5% Lifesteal | Sustain, Physical |
| HT08 | Gentle Touch | Bronze | Healing this hero gives +10% | Support |
| HT09 | Last Stand | Silver | Below 30% HP: +8 DEF and +8 RES | Guard |
| HT10 | Staggering Blows | Silver | Basic hits have a 10% chance to stun the target for 0.5 s | Control, Physical |
| HT11 | Mana Spark | Silver | Each skill cast refunds 15% of its mana cost | Magic |
| HT12 | Shared Spoils | Silver | Heals the lowest-HP ally for 4% of damage this hero deals | Support, Sustain |
| HT13 | Battle Rhythm | Silver | Each basic hit gives +3 Attack Speed for 4 s, stacks up to 10 (+30) | Speed, Physical |
| HT14 | Second Wind | Gold | Once per battle, when knocked out, revive with 30% max HP | Guard, Sustain |
| HT15 | Arcane Echo | Gold | Damage and healing skills have a 15% chance to fire again at 50% power (no mana, no cooldown) | Magic, Support |

## 4. Gear Traits (12: 6 Bronze, 4 Silver, 2 Gold)
Rolled on 30% of new Gear cards. **Slot** = which gear can roll it.

| ID | Trait | Rarity | Slot | Effect (start values) | Tags |
|---|---|---|---|---|---|
| GT01 | Honed | Bronze | Weapon | +5% Crit | Crit, Physical |
| GT02 | Balanced | Bronze | Weapon | +8 Attack Speed | Speed |
| GT03 | Reinforced | Bronze | Armor | +3 DEF | Guard |
| GT04 | Warded | Bronze | Armor | +3 RES | Guard, Magic |
| GT05 | Feathered | Bronze | Armor | +10% Move Speed, +3% Evasion | Speed |
| GT06 | Attuned | Bronze | Any | +5% Cooldown Reduction | Magic, Universal |
| GT07 | Vampiric | Silver | Weapon | +8% Lifesteal | Sustain, Physical |
| GT08 | Spiked | Silver | Armor | +15% Thorns | Guard |
| GT09 | Runed | Silver | Any | +8% Skill Power | Magic, Support |
| GT10 | Stoneskin | Silver | Armor | +10% Block, +15% Control Resist | Guard, Control |
| GT11 | Resonant | Gold | Any | Socketed Magic Stone bonuses on this gear +50% | Universal |
| GT12 | Executioner | Gold | Weapon | Basic hits deal +25% damage to targets below 30% HP | Physical, Crit |

## 5. Item / Accessory Traits (12: 6 Bronze, 4 Silver, 2 Gold)
Every Ring, Necklace, Amulet and Crown rolls one, next to its stat bonus (§4.8). Any accessory type can roll any trait.

| ID | Trait | Rarity | Effect (start values) | Tags |
|---|---|---|---|---|
| IT01 | Vital | Bronze | +5% max HP | Guard |
| IT02 | Lucky | Bronze | +4% Crit | Crit |
| IT03 | Nimble | Bronze | +4% Evasion | Speed |
| IT04 | Focused | Bronze | Start battle with +10% mana (60% instead of 50%) | Magic |
| IT05 | Soothing | Bronze | Regenerate 1% max HP every 5 s | Sustain |
| IT06 | Steadfast | Bronze | +15% Control Resist | Control, Guard |
| IT07 | Rallying | Silver | Allies in the same lane get +5 DEF for the first 10 s of battle | Support, Guard |
| IT08 | Siphon | Silver | +6% Lifesteal, works on skill damage too | Sustain, Magic |
| IT09 | Spellguard | Silver | Battle start: shield worth 15% max HP that only absorbs magic damage | Guard, Magic |
| IT10 | Hunter's Mark | Silver | Basic hits mark the target for 3 s; marked targets take +8% damage from all allies (does not stack) | Support, Physical |
| IT11 | Guardian Bond | Gold | 20% of damage taken by the lowest-HP ally is redirected to this hero | Guard, Support |
| IT12 | Overflow | Gold | Start battle with 100% mana | Magic, Universal |

## 6. Caps (all sources combined)
Stored as tunable data. Gear, items, tree passives and traits all add up to these limits.

| Stat | Cap |
|---|---|
| Crit | 60% |
| Evasion | 40% |
| Block | 50% |
| Lifesteal | 30% |
| Cooldown Reduction | 40% |

## 7. Open Questions
1. **Stat definitions** (§1): Block = 50% less physical basic-hit damage, Evasion = basic hits only, Lifesteal = basic hits only. Confirm and move into GDD §6.9.
2. **Tag weighting:** rolls ignore tags today (full trade value, real bad luck). Option later: small bonus weight toward fitting tags.
3. **Gear trait chance:** 30% flat for all tiers, or higher on Tier III gear like the slot weights (§4.7.1)?
4. **Fusing gear:** the gear trait is lost and the result re-rolls (same as heroes). A confirmation warns the player, like stones (§4.7.2).
5. **Role-based roll limits:** should a Support never roll Physical-only traits? Current answer: no, any hero can roll any hero trait.

## 8. Tag Coverage
| Tag | Hero | Gear | Accessory |
|---|---|---|---|
| Guard | HT01, HT04, HT09, HT14 | GT03, GT04, GT08, GT10 | IT01, IT06, IT07, IT09, IT11 |
| Physical | HT02, HT05, HT07, HT10, HT13 | GT01, GT07, GT12 | IT10 |
| Magic | HT06, HT11, HT15 | GT04, GT06, GT09 | IT04, IT08, IT09, IT12 |
| Crit | HT02 | GT01, GT12 | IT02 |
| Speed | HT03, HT05, HT13 | GT02, GT05 | IT03 |
| Sustain | HT07, HT12, HT14 | GT07 | IT05, IT08 |
| Support | HT08, HT12, HT15 | GT09 | IT07, IT10, IT11 |
| Control | HT10 | GT10 | IT06 |
| Universal | | GT06, GT11 | IT12 |
