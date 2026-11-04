# Dev Log

Short dated entries: what was done, what was learned, what's next. Newest at the top.

---

## 2026-11-04 (2)
**Done:** GDD v0.32 on branch `main_rule_review`. Roles are labels with a core tool; branches declare their role (lore-limited, one keeps the initial role). STR/AGI/MAG renamed to Salt/Mercury/Sulfur with a designer-set dominant principle and Resonance (+10%); growth rules; DEF growth per homunculus. Principles added to Lore.md. All 5 homunculi updated and their derived stats recomputed (formula checked against all old values first).
**Learned:** Mercury Resonance raises Wren's and Snick's DEF to 54% at Lv. 30, closer to Tobin's 57%.
**Next:** Board & range design (§13 #38); Elsie's branch roles; check the Tank DEF gap.

## 2026-11-04
**Done:** Lore: reincarnated souls (temperament, never memories); the dark being in the library's hex book, paid in donuts. GDD: Curse status (§6.10), Summons (§6.11). Grum reworked: reincarnated child's soul, oath, 3 branches (Soul Reaper, Demonology, Corruptor).
**Next:** Elsie (Angel – Priest) and Snick (Goblin – Rogue) against the new tone; Tier II heroes.

## 2026-11-03 (7)
**Done:** GDD v0.31. Lore tone "hopeful, with weight": the player is the guild master and alchemist; some homunculi draw a soul from nature, which returns to nature in a reaction (lore only, §13 #37). Hero = homunculus. 1–3 branches per hero. Targeting "Same lane, back-most". Statuses Ensnare and Sleep. Wren reworked: cursed elf, 2 branches (Leashed / Unbound with Caged Fury rage).
**Learned:** A homunculus with a will changes the player's role: the alchemist is responsible for their homunculi, not just their owner.
**Next:** Review the other Tier I drafts (Elsie, Snick, Grum) against the new tone; Tier II heroes.

## 2026-11-03 (6)
**Done:** GDD v0.30: every skill has 5 levels, so all 30 skill points go to the hero's own skills. Actives got a Lv. 5 continuing their step; passives were re-spread so Lv. 5 = the old max. Scroll skills level up with duplicate Scrolls. Template and the 5 Tier I heroes updated; §13 #36 added (points after a cap raise).
**Next:** User review of the 4 Tier I drafts; then Tier II heroes.

## 2026-11-03 (5)
**Done:** Tank DEF fix (GDD v0.29): Tanks get base DEF 6 + 0.3 DEF per level. Tobin now has 32% physical reduction at Lv. 1 and 57% at Lv. 30, ahead of Wren (51%) and Snick (52%). Heavy Lid lowered to +1 / 1.5 / 2 attack damage per DEF to match.
**Next:** User review of the 4 Tier I drafts; then Tier II heroes.

## 2026-11-03 (4)
**Done:** Tobin approved. Drafted the other 4 Tier I heroes (Wren, Elsie, Snick, Grum) with core + 3 branches each; added Bleed, Weaken, Untargetable, Knockback to GDD §6.10 (v0.28).
**Learned:** Under the Dota rates AGI gives DEF, so AGI heroes end up with more DEF than Tobin (51% vs 35% at Lv. 30). Tanks likely need higher base DEF.
**Next:** User review of the 4 drafts; decide the Tank DEF fix; then Tier II heroes.

## 2026-11-03 (3)
**Done:** GDD v0.27: branching skill tree for all heroes, level-up gives growth + 1 skill point, status effects list. Template updated. Tobin now has core (Shield Bash, Panicked Shout, Pot-Lid Guard) + 3 branches: Bludgeon, Ultimate Protector, Spellguard.
**Next:** User review of Tobin's branches; then the other 4 Tier I heroes.

## 2026-11-03 (2)
**Done:** Knight pilot reworked as **Tobin** (backstory, Codex line, kit renames, lower block, dull sword, new illustrator brief). Character-name rule added (GDD v0.26, template, index).
**Next:** User review of Tobin; then the other 4 Tier I heroes.

## 2026-11-03 (2)
**Done:** GDD v0.25. New `Docs/Design/TraitPool.md`: 39 traits (Hero 15, Gear 12, Accessory 12) with rarity, start values and tags; % stat caps; gear 30% trait chance. Hero template §7 points to the tags.
**Next:** User review of the trait pool; confirm stat definitions (Block, Evasion, Lifesteal) in §6.9; fill fitting tags per hero.

## 2026-11-03
**Done:** GDD v0.24: Dota-style attribute model, mana + cooldown skills, armor formula, skill tree, weapon families. New `Docs/Design/Heroes/` with template, index (28 heroes) and pilot Human – Knight. Backstories build on the existing Lore.md (homunculi).
**Next:** Review the Knight pilot; then fill the other 27 heroes; trait pool for Hero/Gear/Item (separate task).

## 2026-11-03
**Done:** GDD v0.23. World & backstory: new `Docs/Design/Lore.md` (premise, glossary, system mapping), GDD §1 and §6.6 updated, README pitch.
**Next:** Per-hero content (stats, growth, skill pool, targeting) using the lore for flavor; world name.

## 2026-11-02 (3)
**Done:** GDD v0.22. Battle HUD revised (hybrid select-then-cast, PC + mobile), skill pool with 2-skill loadout, Scrolls teach skills, consumables bottom-right (Potion/Bomb).
**Next:** Per-hero content: base stats, growth, skill pool (3 level skills), targeting for 28 heroes.

## 2026-11-02 (2)
**Done:** Roadmap check: basic lists ticked. GDD v0.17 resolved §13 #9, #11, #24, #26 (unique skills on all heroes, pure re-roll, no pity, Bronze/Silver/Gold, hero tier ≠ power).
GDD v0.18: #14 resolved (Coins + Gems, unlimited collection with identical stacking, 2 battle consumable slots).
Working title chosen: **Fuseborn** (GDD v0.19, README).
GDD v0.20–0.21: combat questions #21–23 resolved; level cap 30 (raisable); combat numbers §6.9 (stat formulas, damage formula, consumable limits).
**Next:** Per-hero content (base stats, growth, active skill, targeting) for the 28 heroes; XP curve; then Phase 1 Unity setup.

## 2026-11-02
**Done:** GDD v0.16. Progress check: melee heroes run in (Move Speed matters), consumables usable in battle (limited slots), battle art deferred.
**Next:** Combat design: hero base stats & growth, damage formula, active skills and targeting per hero, consumable slots, PvE wave structure.

## 2026-11-01 (3)
**Done:** GDD v0.15. Item tree: 5 junk basics → 12 Tier II → 13 Tier III (3 with 2 recipes) → 10 Tier IV and 15 Tier V usable items (§15.8). Grids in `Docs/Design/Data/ItemGridT2–T5.tsv`, verified by script.
**Next:** User sorts Item list; item effects; Gear stat values; Move Speed question.

## 2026-11-01 (2)
**Done:** GDD v0.14. Armor pieces share the Armor slot, gear bonus stats, 11 Tier III Gear recipes (§15.7), grid in `Docs/Design/Data/GearGridTier3.tsv`.
Google Sheet Gear tab: Tier III grid added at A10:F22 (user's Tier II grid kept).
**Next:** User sorts Gear lists; stat values; 5th Item basic; Move Speed question.

## 2026-11-01
**Done:** GDD v0.13. Weapon renamed **Gear** (weapons + armor), Armor removed from Item. Proposed 5 Gear basics and 11 Tier II recipes (§15.7), grid in `Docs/Design/Data/GearGrid.tsv`. Google Sheet: new **Gear** tab (A2:F8, lower-triangle layout like Hero).
**Next:** User sorts the Gear list; 5th Item basic; gear traits/stats; hero second recipes.

## 2026-10-31 (2)
**Done:** GDD v0.12. Merged with the hero sheet: 28 heroes, role balance 4/3/5/4/5/7. HeroPool updated.
Google Sheet updated to match (Hero tab A3:S21), source grid in `Docs/Design/Data/HeroGrid.tsv`.
**Next:** Second recipes for Wraith, Troll, Half-Angel, Golem; Weapon & Item basic lists.

## 2026-10-31
**Done:** GDD v0.11. Revised 14 hero Race–Class names, added 2 Rangers, 2nd recipes for all Tier III, role balance 3/3/4/4/4/6. New `Docs/Design/HeroPool.md` (race/class pools, naming rules).
**Next:** Update the Google Sheet from GDD §15.6; Weapon & Item basic lists; hero stats/skills/targeting.

## 2026-10-30 (2)
**Done:** GDD v0.10. Added hero list from the recipe sheet (5 Tier I, 11 Tier II, 6 Tier III), roles proposed, recipe philosophy.
**Next:** Weapon & Item basic lists; hero stats/skills/targeting; alternate recipes.

## 2026-10-30
**Done:** GDD v0.9. Seasonal rarity rotation confirmed.
**Next:** Basic card lists (5 heroes, 5 weapons, 5 items) + first recipes.

## 2026-10-29 (8)
**Done:** GDD v0.8. Weekly Rare guarantee, seasonal rarity rotation, Exchange chests, alternate-recipe rule.
**Next:** Basic card lists (15) + first recipes (with 2+ paths to key results); battle art approach.

## 2026-10-29 (7)
**Done:** GDD v0.7. Daily Chest fully random; basic card rarity with weights; recipe-path rule; duplicate Exchange proposal.
**Next:** Battle art approach; basic card lists (15, with rarity) + first recipes.

## 2026-10-29 (6)
**Done:** GDD v0.6. Combat design (diagonal view, 5-hero grid, roles, targeting priorities, skill bar, cooldowns, passive uniques, PvE waves, async PvP). Stone failure rule decided.
**Learned:** The diagonal view means each hero needs back and front views, which is a major art-cost decision.
**Next:** Decide battle art approach; provide basic card lists (15) + first recipes; unique-skill tier/pity.

## 2026-10-29 (5)
**Done:** GDD v0.5. Armor as Item, single accessory slot, risk-based Magic Stone socketing (proposal), party size 4–5.
**Next:** Confirm stone failure severity; unique-skill rules; combat design (incl. party size 4 vs 5).

## 2026-10-29 (4)
**Done:** GDD v0.4. 3 categories, online game, starter 30 / chest 8, recipe-sharing strategy, hero leveling/stats/slots, weapon random slots + magic stones, auto-battle and mining outlines. Roadmap restructured (offline prototypes → online → social).
**Next:** Settle GDD §13 questions (armor, accessory slot, stones, party size, unique skill rules); basic card lists; combat design.

## 2026-10-29 (3)
**Done:** GDD v0.3. Resolved Q1–4 (basics per category, card sources, hero level reset, same-category fusion).
**Next:** Remaining §13 questions (upgrade method, unique-skill tier/pity, stats/roles); basic card lists; combat.

## 2026-10-29 (2)
**Done:** GDD v0.2: card fusion concept, 4 categories, consumption rule, tiers, unique-skill gacha, Codex, Prototype 1 scope.
**Next:** Resolve GDD §13 open questions (esp. base card source); provide basic card lists; then discuss combat.

## 2026-10-29
**Done:** Created project folder structure, README, CLAUDE.md, production docs, and GDD template.
**Learned:** —
**Next:** Fill GDD sections 1–4 (concept, pillars, core loop, mechanics).
