# Decision Log

Record notable decisions so future-you (and AI assistants) know *why*. Newest at the top.

| Date | Decision | Alternatives considered | Reason |
|---|---|---|---|
| 2026-11-03 | Wren: 2 branches, Leashed (precision/burst) and Unbound (AoE, evasion, Caged Fury: 3 rage → 5 s Berserk + lane Ensnare → curse Sleep 4→3 s, no rage gain while berserk or asleep); Trickster and Volley removed | 8 rage; rage from dodges too; keep 3 branches | Back row + evasion makes hits rare, so 3 rage keeps Berserk a real event; no rage during the cycle stops instant re-triggering |
| 2026-11-03 | Wren reworked: souled elf homunculus cursed by the guild master (player) to stop her returning to the forest; proud, restless, homesick, defiant | Comedic show-off archer | User's lore; the curse drives her two branches (obedient vs grudge) |
| 2026-11-03 | New statuses: Ensnare (can't move, can't evade, physical DoT) and Sleep (can't act, wakes on damage); curse variants may override in the skill text | Magic DoT for Ensnare; Sleep that never breaks | Physical scales with Wren and DEF counters it; general Sleep stays reusable while Wren's curse sleep can stay harsh |
| 2026-11-03 | New targeting rule "Same lane, back-most"; Wren uses it with Back-line fallback (tie: nearest lane) | Keep Lowest HP → Front-most; Lowest HP fallback | Fits her sniper identity and makes her lane placement a tactical choice |
| 2026-11-03 | 1–3 branches per hero (max 3, fixed for now); 1 branch opens automatically; 30-point budget unchanged | Exactly 3 for every hero | Branch count follows each homunculus's lore (Wren: 2 paths); simple heroes cost less content and art |
| 2026-11-03 | Hero = homunculus = homunculi (same thing). Player-facing prefers "Homunculus"; code, data IDs and files keep "Hero" | Full rename incl. files and IDs; keep "Hero" everywhere | Fits the lore without breaking links or data names |
| 2026-11-03 | Tone → "hopeful, with weight": player is guild master and alchemist and carries every risk; some homunculi draw a soul from nature, others are soulless; in a reaction, ingredient souls return to nature (nothing carries over). Lore only for now, may gain mechanics later | Light adventure, no grim costs; souls merge into the result; souls destroyed | Lets homunculi have will and unique lore (e.g. Wren's curse) without fusion becoming killing; avoids "which soul carries over" questions |
| 2026-11-03 | Every skill has 5 levels (6 × 5 = 30 points, all on the hero's own skills); Scroll skills cost no points and level up with duplicate Scrolls | 8 points for Scroll skills; a third branch "ultimate" active | Exact fit at the cap with no new skills or animations (an ultimate would add ~84 skills); gives duplicate Scrolls a use |
| 2026-11-03 | Heavy Lid lowered to +1 / 1.5 / 2 attack damage per DEF | Keep +3 / 4 / 5 | With the Tank DEF rule it would have added ~108 damage at Lv. 30; now ~43, close to before |
| 2026-11-03 | Tanks get base DEF 6 + 0.3 DEF growth per level (others 0) | Higher flat base DEF only; lower AGI → DEF rate | A flat base alone made Tanks twice as tough as everyone at Lv. 1; growth keeps Tobin ahead of AGI heroes at every level (32% vs 22% at Lv. 1, 57% vs 51–52% at Lv. 30) without changing the universal rates |
| 2026-11-03 | Tobin approved as the hero format; Tier I drafts Wren, Elsie, Snick, Grum written to the same budget (base 50, growth 5.6) | Ask for each concept first | Gives the user drafts to react to, as with Tobin |
| 2026-11-03 | Branching skill tree: unlocks by skill level; core A1 → A2 + core passive; 3 branches of 2 actives + 1 passive; branch choice permanent; role fixed | Hero-level unlocks; 3 actives + passive per branch; respec | Build identity per copy; ~12 skills per hero keeps content and art manageable |
| 2026-11-03 | Level-up = automatic attribute growth + 1 skill point; hero level never unlocks skills | Skill XP from use | Player decides which skills grow |
| 2026-11-03 | Status list (Stun, Taunt, Stagger, Confuse, Burn, Shield); duration reduction capped at −50%, only knockback immunity | Full status immunity | Full immunity would counter every control hero in PvP |
| 2026-11-03 | One character name per hero type, card shows "Name · Race – Class" | No names; player renames copies | Gives each hero a personality; copies stay distinct via traits |
| 2026-11-03 | Knight pilot = Tobin: insecure homunculus, no past, oath to the guild master; junk pot-lid shield is part of him (low block), dull sword | Noble knight | Ordinary basic that grows with the player; fits tier ≠ power and Lore.md |
| 2026-11-03 | Trait pool in `TraitPool.md`: separate Hero (15) / Gear (12) / Accessory (12) pools, 70/25/5 odds, tags as a fit hint only, gear 30% trait chance, accessories always, CDR & Skill Power only on gear traits, % caps (Crit 60, Evasion 40, Block 50, Lifesteal 30, CDR 40) | One master table; every gear rolls a trait; no caps | Each pool balances alone; trait gear stands out in trading; caps stop % stacking into near-immunity |
| 2026-11-03 | Dota-style attributes: per-hero base STR/AGI/MAG + growth, main stat +1 damage, universal rates (STR→HP/regen, AGI→DEF/attack speed, MAG→mana/regen/RES) | Per-hero or per-role rates | Readable, comparable heroes; identity from base stats and kit |
| 2026-11-03 | Skills cost mana + cooldown; values fixed per skill level; CDR from gear only | Cooldown only; stat-scaled skills | Easy to read and balance; MAG matters through mana |
| 2026-11-03 | Crit, Evasion, Block only from gear, items, passives, traits | On attributes | Avoids % stacking from leveling; gives gear identity |
| 2026-11-03 | Skill tree: 3 actives + 2 fixed passives, 1 skill point per level; rolled unique passive stays separate | Tree replaces roll | Hero identity (tree) plus per-copy surprise (roll) |
| 2026-11-03 | Weapon families gate weapons per hero; one file per hero in Docs/Design/Heroes/ with a power budget (base 46–54, growth 5.0–6.0) | Free equip; one big file | Clear builds; tier ≠ power stays fair |
| 2026-11-03 | World: alchemy reactions; Great Codex fame; player runs a guild of homunculi; monsters are Runoffs; light-adventure tone | Shattered Weave; Card Spirits; Forge of Echoes | User's own concept; explains fusion, discovery race, PvP and drops |
| 2026-11-02 | Heroes have a skill pool (leveling + Scrolls); 2 skills per hero in battle | 1 skill per hero | More build choice per hero, fits "strength from build" |
| 2026-11-02 | Hybrid select-then-cast HUD: hero buttons with ready dots, 2-skill bar, quick-cast on re-tap; consumables bottom-right | All 10 skills visible; plain select-then-cast | Clean screen that still shows every ready skill; works on PC and mobile |
| 2026-11-02 | Scrolls teach skills outside battle; battle consumables are Potion and Bomb | Scrolls as battle consumables | Scrolls become the skill source |
| 2026-11-02 | Damage model: Physical vs Magic (DEF/RES), elements only as Magic Stone riders | Element triangle; full elements | Easy to balance; strength from build, matching tier ≠ power |
| 2026-11-02 | Damage reduction 100/(100+DEF) curve; consumable slots 15 s CD, 3 uses (proposed) | Flat subtraction | Diminishing returns, never immune; stops potion spam |
| 2026-11-02 | 3×3 grid; lanes matter (Same-lane targeting, lane skills) | Rows only | More placement strategy |
| 2026-11-02 | No PvE stamina; pace via daily-limited drops | Energy system | Players can play freely; economy paced by rewards instead |
| 2026-11-02 | Hero level cap 30, raisable later; per-hero base stats and growth | Cap 50; account-level cap | Short enough to finish, room to grow with content |
| 2026-11-02 | Working title: **Fuseborn** | Twinforge; Card Crucible; Two Make One | Short, fits fusion, works as a logo; trademark check before release |
| 2026-11-02 | Currencies: Coins (soft) + Gems (premium, no direct power) | Soft only; trade token | Room for monetization later without pay-to-win |
| 2026-11-02 | Collection unlimited; cards stack only when exactly identical | Per-category caps; shared cap | Collection is the core joy; no storage pressure |
| 2026-11-02 | Battle: 2 shared consumable slots, each a stack of one type | 2–3 slots per hero | Simple loadout; keeps the skill bar readable |
| 2026-11-02 | Hero tier = recipe depth, not power; hero strength from base stats, leveling and gear | Higher tier = stronger | Basics stay competitive; build and leveling matter more than fusion depth |
| 2026-11-02 | Every hero rolls a unique skill, basics at chest open; fusion is a pure re-roll | Tier II+ only; inherited odds | Basics are valuable beyond ingredients; fusing a good skill is a real trade-off |
| 2026-11-02 | No pity and no re-roll item for unique skills | Pity counter; re-roll scroll | Trading answers bad luck |
| 2026-11-02 | Skill rarity labels Bronze/Silver/Gold; basic rarity 2/2/1 at 65/30/5 and starter guarantees confirmed | Shared Common/Rare labels | Avoid confusion with card rarity |
| 2026-11-02 | Next focus: combat design before Unity prototyping | Start Prototype 1; finish content first | User wants battle details settled first |
| 2026-11-02 | Melee heroes run to targets; ranged stay in their cell | Nobody moves; free movement | Gives Move Speed a purpose without full free movement |
| 2026-11-02 | Consumables usable in battle, limited slots (proposed 2–3) | Outside battle only; auto-used | Gives Items a combat role and a tactical choice |
| 2026-11-02 | Battle art approach deferred | Choose now | Prototypes are greybox; decide once combat is fun |
| 2026-11-01 | Item basics are junk materials (Stone, Seed, Log, Bone, Scrap Metal); usable items only from Tier IV (III + I) and Tier V (III + II) | Potion/Ring/Necklace/Stone as basics | Gives Item fusion a long crafting climb; usable items feel earned |
| 2026-11-01 | Accessory slot accepts Ring, Necklace, Amulet or Crown; consumables add Bomb, Scroll, Charm | Ring/Necklace only | More variety; effects decided later |
| 2026-11-01 | Helmet, Gloves, Boots and Body armor share the one Armor slot | New hero slots; Body + Extra slot | Simple to read and balance; pieces compete by bonus focus |
| 2026-11-01 | Gear bonus stats (HP, DEF, ATK, Attack/Move Speed, Crit, Dodge, CDR, Skill Power, Thorns, Control Resist), proposed | Only STR/AGI/MAG | Gives armor pieces distinct identities |
| 2026-11-01 | Gear Tier III: 11 results from 55 pairs, each Tier II used once (proposed) | More results | Keeps no-match surprises; even ingredient demand |
| 2026-11-01 | Weapon and Armor merged into one category, **Gear**; Armor leaves Item | Armor as its own category; Armor stays in Item | Weapon + armor fusions add variety; keeps 3 categories |
| 2026-11-01 | Gear Tier II: 5 basics (3 weapons, 2 armor), 11 results, 4 no-match (proposed, to be sorted) | All 15 pairs match | Mirrors hero grid; keeps "no reaction" surprises |
| 2026-10-31 | Merge hero sheet with GDD: GDD names for known heroes; sheet's newer Tier III heroes and races kept, classes renamed by the rules | Overwrite either side | Keeps the user's newer work; one consistent roster |
| 2026-10-31 | Slime – Alchemist is a Mage (sheet had Support) | Keep Support | Support would be 8/28 |
| 2026-10-31 | Hero naming rules: class never a role word, each class used once, no mash-up races | Free naming | Cards stay readable; class and role don't repeat each other |
| 2026-10-31 | Fill 2 Tier II no-match cells with Rangers (Wood Elf – Hunter, Dwarf – Gunner); keep 2 ✗ | Keep all 4 ✗ | Fixes Ranger shortage; still some "no reaction" pairs |
| 2026-10-31 | Oni → Berserker (Warrior), Zombie – Plague Doctor → Mage | Keep as Support | Support was 8/22; now 6/24 |
| 2026-10-31 | Every Tier III hero has 2 recipes | Single recipe | Alternate-recipe rule (seasonal rarity) |
| 2026-10-30 | Recipes are intentionally surprising (result race/class needn't follow ingredients) | Logical/guessable recipes | Diverse races, true surprise; discovery via hints & community |
| 2026-10-30 | Heroes = free Race + free Class name + fixed Role list | Free roles | Variety on the surface, manageable balance underneath |
| 2026-10-29 | Guarantee 1 Rare basic per week (proposed: 7-day streak chest) | No pity | Fair floor under a low 5% base rate |
| 2026-10-30 | ✅ Confirmed: seasonal (4–6 wk) rarity reshuffle; odds public, card mapping hidden | Weekly reshuffle; fixed rarity | Keeps market & community discovery alive without weekly value crashes; odds disclosure for compliance |
| 2026-10-29 | Every important result has 2+ recipes | Single recipe paths | Rotating rarity must never block progress |
| 2026-10-29 | Exchange: 10 basics → Small Chest, 25 → Big Chest | Gold-only exchange | Duplicate sink that always returns fewer cards than it takes |
| 2026-10-29 | Daily Chest is fully random (no fusable-pair guarantee) | Guarantee a pair | Starter pack already ensures a working start; unlucky chests drive trading |
| 2026-10-29 | Basic card types have rarity (Common/Uncommon/Rare) | Rarity only on rolls | Makes chests exciting and gives basics trade value |
| 2026-10-29 | Main recipe paths use Common/Uncommon basics; Rares unlock side branches | Rares required on main paths | Prevents luck-gated progression |
| 2026-10-29 | Party of 5 heroes in a grid formation (3×3 proposed) | 4 heroes | More team-building depth and hero demand |
| 2026-10-29 | Diagonal battle view: party bottom-left, enemies top-right | Side-view, single screen | Player's preferred look; gives depth to grid formation |
| 2026-10-29 | Per-hero targeting priority as hero identity | Uniform targeting | Makes heroes feel distinct; adds formation strategy |
| 2026-10-29 | Per-hero skill cooldowns, MAG lowers cooldown | Charge gauge, shared energy | Easy to read; gives MAG value |
| 2026-10-29 | Unique skills are passive | Second active, replace active | One button per hero; keeps the skill bar at 5 |
| 2026-10-29 | Magic Stone fail = stone destroyed, gear kept | Destroy all | Protects valuable tradable gear |
| 2026-10-29 | Armor is an Item subtype | Merge into Weapon/Equipment | Keeps 3 categories |
| 2026-10-29 | One accessory slot (Ring or Necklace) | Ring + Necklace slots | Simpler to read and balance |
| 2026-10-29 | Magic Stone attach/detach has a success chance; fail destroys the stone, gear kept (proposed) | Free removal; permanent; destroy-all | Adds tension and a stone sink without destroying valuable tradable gear |
| 2026-10-29 | 3 card categories: Hero, Weapon, Item (Item = potions, rings, necklaces, magic stones, armor?) | 4 categories | Simpler; richer Item recipe space |
| 2026-10-29 | Online, server-authoritative game | Offline/single-player | Trading & PvP need it; prevents cheating and duplication |
| 2026-10-29 | Validate fun offline first, with server-shaped service interfaces | Build backend first | Avoids big backend work before the fun is proven |
| 2026-10-29 | Starter pack 30 random basics; Daily Chest 8 cards | Daily Chest 5 | 5/day was too slow |
| 2026-10-29 | No official recipe cheat sheet; recipes server-only; community shares | Official recipe site | Keeps discovery genuine; community hook |
| 2026-10-29 | Heroes gain XP only when used in a party; stats STR/AGI/MAG | More stats | Simple, readable |
| 2026-10-29 | Hero slots: Weapon, Armor, Accessory | — | — |
| 2026-10-29 | Weapons roll 0–5 slots for Magic Stones | Fixed slots | Extra random layer, trading value |
| 2026-10-29 | Combat: auto-battle with manual skill activation | Turn-based, real-time | Fits mobile/idle play, keeps player agency |
| 2026-10-29 | 5 basic cards per category (20 total) | 5 total | Every category gets its own recipe tree |
| 2026-10-29 | Same-category fusion only; cross-category = equip/use | Cross-category recipes | Easier to learn and balance |
| 2026-10-29 | Fused hero result starts at Lv. 1 | Partial carry-over, min-level requirement | "Keep one, fuse the spare" duplicates pattern |
| 2026-10-29 | Layered card sources: Daily Chest (P1), monster drops (P2), mining/PvP rewards later; trading later | Single source | Chest alone is too slow; drops tie combat to fusion |
| 2026-10-29 | PvP losers don't lose cards; winners get a system reward | Loser's cards go to winner | Avoids rage-quits and alt-account abuse |
| 2026-10-29 | Core concept: 2-card fusion that consumes ingredients; no-match = nothing happens | Infinite ingredients (classic discovery) | Adds meaningful choice and ties into the hero/gear economy |
| 2026-10-29 | Card-based visuals instead of item icons | Freestanding item art | One template + artwork per card, holds stats, cheaper to produce |
| 2026-10-29 | Trading & combat out of Prototype 1 | Build everything at once | Validate that fusion is fun first |
| 2026-10-29 | Use Unity as engine (tentative) | Godot, Unreal | Initial preference; confirm in Phase 1 |
| 2026-10-29 | Keep raw art/audio outside Unity `Assets/` | Everything inside Assets | Faster imports, cleaner project |
| 2026-10-29 | Design-first: GDD before assets/code | Jump into prototyping | Avoid building features that get cut |
