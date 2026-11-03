# Technical Design Document

> ⏸ Fill this **after** the GDD core loop and prototype scope are locked. It translates design into Unity architecture.

## 1. Engine & Settings
- Unity version:
- Render pipeline: (URP / Built-in / HDRP)
- Target platform(s) & resolution:
- Target frame rate:

## 2. Scene Structure
| Scene | Purpose |
|---|---|
| Boot | Initialize services, load first scene |
| MainMenu | |
| Gameplay | |
| Sandbox | Testing ground for mechanics |

## 3. Architecture Overview
- Game state flow (Menu → Playing → Paused → GameOver):
- How systems communicate (direct refs / events / ScriptableObject channels):
- Save/load approach (if any):

## 4. Core Systems
| System | Responsibility | Key scripts | Data (ScriptableObjects) |
|---|---|---|---|
| Player | | | |
| Input | | | |
| Camera | | | |
| UI | | | |

## 5. Data & Tuning
List every tunable value from the GDD and where it lives.

## 6. Third-Party Packages
| Package | Purpose | Version |
|---|---|---|

## 7. Known Risks / Open Technical Questions
-
