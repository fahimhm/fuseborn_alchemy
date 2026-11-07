# Roadmap

Each phase has an **exit criterion**. Don't move on until it's met.
The game is **online**, but we validate fun offline first, with code shaped so the server can be swapped in later.

## Phase 0 — Concept & GDD  🟡
- [x] Core concept, card categories, fusion rules
- [x] Card sources, upgrade systems
- [x] Resolve remaining GDD §13 questions (open: #30 hero roles proposed; tech/later items)
- [x] Basic card lists (15) + first ~20–30 recipes (Hero, Gear, Item trees in GDD §15)
- [x] Combat design (auto-battle) discussion (§6, numbers in §6.9)
- [ ] Per-hero content for 28 heroes from `Docs/Design/Heroes/_HeroTemplate.md` (pilot: Human – Knight done)
- [ ] Unique trait pool for Hero, Gear and Item
- [ ] Collect reference images in `References/Moodboard/`
- **Exit:** the fusion prototype can be built from the GDD alone.

## Phase 1 — Unity Project Setup  ⚪
- [ ] Choose & log Unity version and render pipeline (DecisionLog)
- [ ] Create project in `UnityProject/` via Unity Hub
- [ ] Create `Assets/_Project/` folder layout (see README)
- [ ] Set up Git + Git LFS; first commit
- **Exit:** empty scene runs; repo is committed.

## Phase 2 — Prototype 1: Fusion (offline)  ⚪
- [ ] Card data (ScriptableObjects / imported from a spreadsheet)
- [ ] Inventory UI + drag & drop fusion
- [ ] Recipe lookup, unique-skill roll, weapon-slot roll behind a `FusionService` interface (local implementation)
- [ ] Starter pack, Daily Chest, debug chest
- [ ] Codex; equip / socket / use potion
- [ ] Local save
- **Exit:** testers experiment for 10+ minutes, with no soft-lock.

## Phase 3 — Prototype 2: Auto-Battle (offline)  ⚪
- [ ] Party setup + PvE stage with auto-battle and manual skills
- [ ] XP for party heroes, card drops
- **Exit:** the fuse → equip → fight → drops loop feels rewarding.

## Phase 4 — Online Foundation  ⚪
- [ ] Pick backend (Technical Design + DecisionLog)
- [ ] Accounts, server-side inventory, server-side fusion and rolls
- [ ] Swap local services for online ones
- **Exit:** the same game, now server-authoritative.

## Phase 5 — Social: PvP, Trading, Mining  ⚪
- [ ] Async PvP + rewards
- [ ] Trading with in-game currency
- [ ] Mining mechanic
- **Exit:** a closed online playtest with real players.

## Phase 6 — Vertical Slice  ⚪
- [ ] Art from AssetList, audio pass, juice
- [ ] Build for target platform(s)

## Post-launch — Real-time PvP  🔮
- [ ] When enough players are online (GDD §6.14, §13 #40): real-time Best of Three PvP as a new mode next to the async ladder
- **Until then:** keep the battle simulation server-authoritative and fixed-step, and battle actions as commands (GDD §6.14)
