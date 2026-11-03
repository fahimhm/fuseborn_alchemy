# Fuseborn (working title)

A Unity game prototype. **Current phase: Pre-production (Game Design Document).**

> One-line pitch: In a world where anything can react with anything, lead an alchemy guild racing to discover new reactions. An online card game where you fuse two cards to discover new heroes, weapons, and items. Fusion consumes the ingredients, results roll random unique skills and weapon slots, and your party fights in auto-battles where you choose when to fire each skill.

---

## Project Status

| Phase | Status |
|---|---|
| 0. Concept & GDD | 🟡 In progress |
| 1. Unity project setup | ⚪ Not started |
| 2. Prototype 1: Fusion (offline) | ⚪ Not started |
| 3. Prototype 2: Auto-battle (offline) | ⚪ Not started |
| 4. Online foundation (backend) | ⚪ Not started |
| 5. PvP, trading, mining | ⚪ Not started |
| 6. Vertical slice (art/audio pass) | ⚪ Not started |

See [Docs/Production/Roadmap.md](Docs/Production/Roadmap.md) for details.

---

## Folder Structure

```
AI Project Game Prototype/
├── README.md                  ← You are here
├── CLAUDE.md                  ← Context & rules for AI assistants
├── .gitignore                 ← Unity + macOS ignores
├── .gitattributes             ← Git LFS rules for binary assets
│
├── Docs/
│   ├── Design/
│   │   └── GameDesignDocument.md   ← START HERE
│   ├── Technical/
│   │   └── TechnicalDesign.md      ← Filled after GDD is locked
│   └── Production/
│       ├── Roadmap.md              ← Milestones & tasks
│       ├── AssetList.md            ← Every art/audio asset to make
│       ├── DecisionLog.md          ← Why we chose X over Y
│       └── DevLog.md               ← Dated progress notes
│
├── ArtSource/                 ← Raw/editable art (.psd, .blend, .aseprite, .kra)
│   ├── Concepts/
│   ├── 2D/
│   ├── 3D/
│   └── UI/
├── AudioSource/               ← Raw audio projects & stems (.wav, DAW files)
│   ├── Music/
│   └── SFX/
├── References/                ← Moodboards, screenshots, inspiration (not shipped)
├── Tools/                     ← Helper scripts (batch export, build scripts)
├── Builds/                    ← Exported game builds (git-ignored)
│
└── UnityProject/              ← Created later by Unity Hub (not yet present)
    ├── Assets/_Project/        ← All our game content lives here
    ├── Packages/
    └── ProjectSettings/
```

### Why this layout
- **Source files stay outside Unity.** Unity imports everything inside `Assets/`, so large `.psd`/`.blend` working files live in `ArtSource/` and only exported files (`.png`, `.fbx`, `.wav`) go into Unity. Keeps the project fast and clean.
- **Unity project in its own subfolder.** Unity Hub wants to create a project in a new/empty folder; keeping it in `UnityProject/` lets docs and source assets sit alongside it in one repo.
- **`Assets/_Project/`** keeps our content separate from Asset Store / third-party packages (the underscore sorts it to the top).

### Planned Unity `Assets/_Project/` layout (created in Phase 1)
```
_Project/
├── Art/          (Sprites, Models, Materials, Animations, VFX)
├── Audio/        (Music, SFX)
├── Prefabs/
├── Scenes/       (Boot, MainMenu, Gameplay, Sandbox)
├── Scripts/      (Core, Player, Enemies, UI, Systems, Utilities)
├── ScriptableObjects/   (tunable game data: stats, levels, items)
├── UI/
└── Settings/     (URP/input/render settings)
```

---

## Tech Stack

| Item | Choice |
|---|---|
| Engine | Unity 6 (LTS) — _confirm version in DecisionLog_ |
| Render pipeline | URP — _TBD_ |
| Language | C# |
| Input | Unity Input System (new) |
| Online backend | TBD (UGS / PlayFab / Nakama / custom). Server-authoritative |
| Version control | Git + Git LFS |
| Target platform | _TBD (PC / Mobile / WebGL)_ |

---

## Getting Started (after Phase 1)
1. Install Unity Hub and the Unity version listed above.
2. Unity Hub → **Add project from disk** → select `UnityProject/`.
3. Open `Assets/_Project/Scenes/Boot.unity` and press Play.
