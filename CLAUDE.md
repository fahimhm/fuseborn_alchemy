# CLAUDE.md — AI Assistant Context

This file gives AI assistants (Claude Code, etc.) the context and rules for this project. Keep it short and current.

## Project
- Unity game prototype, built step by step.
- **Current phase: Pre-production.** The Game Design Document is the source of truth: `Docs/Design/GameDesignDocument.md`.
- Do not create assets or write code for a feature until it is described in the GDD.
- **Online game, server-authoritative.** Fusion results, random rolls (skills, weapon slots), inventory changes, rewards, and trades must go through a service interface (e.g. `IFusionService`). Prototypes use a local implementation; never put game-authoritative logic directly in UI code.

## Workflow rules
1. **Design first.** If a request conflicts with or isn't covered by the GDD, point it out and propose a GDD update before implementing.
2. **Prototype mindset.** Prefer the simplest thing that proves the mechanic is fun. Greybox (primitive shapes) before final art.
3. **Log decisions.** Any notable choice (engine version, pipeline, architecture, scope cut) gets a line in `Docs/Production/DecisionLog.md`.
4. **Track assets.** New art/audio needs go into `Docs/Production/AssetList.md`.
5. **Update the DevLog** (`Docs/Production/DevLog.md`) at the end of meaningful work sessions.

## Folder conventions
- Raw/editable art → `ArtSource/`; raw audio → `AudioSource/`. Never put `.psd`/`.blend` working files inside Unity `Assets/`.
- Unity project lives in `UnityProject/`. Our content goes in `UnityProject/Assets/_Project/`.
- Third-party / Asset Store packages stay outside `_Project/`.

## Code conventions (Unity C#) — apply once coding starts
- One `MonoBehaviour` per file; file name = class name (PascalCase).
- Namespace: `Game.<Area>` (e.g. `Game.Player`, `Game.UI`).
- Private fields: `_camelCase`; expose to Inspector with `[SerializeField] private`, not public fields.
- Tunable numbers (speed, damage, timers) go in **ScriptableObjects**, not hard-coded.
- Use the new Input System.
- Keep scripts small and single-purpose; avoid "god" managers.

## Naming conventions for assets
- `Type_Name_Variant` — e.g. `SPR_Player_Idle`, `SFX_Jump_01`, `MAT_Ground_Grass`, `PFB_Enemy_Slime`.
- Common prefixes: `SPR` sprite, `TEX` texture, `MDL` model, `MAT` material, `ANM` animation, `PFB` prefab, `SFX`, `MUS` music, `UI`, `SO` ScriptableObject.
