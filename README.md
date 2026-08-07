# Hi, I'm Yaxin(Evan) 👋

**Gameplay programmer — Unreal Engine & C++ on a shipped commercial title, plus a long trail of Unity / Lua / custom-engine prototypes.** I build gameplay systems end to end — physics, netcode, data-oriented performance, and AI — and the tooling and workflows that let a whole team scale on them.

## 💼 Commercial / Shipped Work

Core systems I owned in a shipped commercial **open-world multiplayer** title (**Unreal Engine · C++**). The repositories below are **clean-room reference implementations** — architecture, design decisions, and technique, written for portfolio purposes with **no proprietary source**.

| System | Repository | What it is |
|---|---|---|
| 🚢 **Watercraft physics & netcode** | [watercraft-physics](https://github.com/seak123/watercraft-physics) | Player-built, physically-simulated boats — two buoyancy solutions (sample-point & submerged-volume + center of buoyancy), frame-rate-independent substep physics, and multiplayer sync of players standing on a *moving, rotating* platform. |
| 🏗️ **Data-oriented building** | [data-oriented-building](https://github.com/seak123/data-oriented-building) | ECS / Mass-style building system for **thousands** of persistent objects — entities + fragments instead of per-actor, instanced rendering, throttled delta replication, and an on-demand shared actor pool. |
| ⚙️ **Automation AI** | [automation-ai-productionline](https://github.com/seak123/automation-ai-productionline) | Creature-driven production line on **GAS + behavior trees + navigation**, with clean system seams so one worker-AI drives any station by data alone. |

<sub>These are reference write-ups authored by me to document architecture and technique; they contain no proprietary or third-party code.</sub>

---

## 🕹️ Indie prototypes & side projects

> 🗓️ **Project timeline** (newest → oldest). Dates are each project's inception, so the real chronology is clear regardless of GitHub's "last updated" sorting.

| Date | Project | Tech | What it is |
|---|---|---|---|
| **2026 · Aug** | ⭐ [hex-auto-battler](https://github.com/seak123/hex-auto-battler) | Unity + Lua | Hex-grid strategy auto-battler — deploy structures, strategize, auto-battle. **(current)** |
| 2025 · Dec | [AutoHeroDemo](https://github.com/seak123/AutoHeroDemo) | Unity + Lua | Auto-battler demo — deploy units and let them fight automatically. |
| 2021 · Jun | [CybeArtifact](https://github.com/seak123/CybeArtifact) | Unity C# + Lua | Card game framework: login → menu → battle flow with card UI. |
| 2021 · Apr | [TacticalDeck](https://github.com/seak123/TacticalDeck) | Lua | Turn-based card tactics — round state machine + replayable performer. |
| 2021 · Apr | [AutoForge](https://github.com/seak123/AutoForge) | Unity C# | Auto-battler: battle-order stream + node-based playback. |
| 2020 · Sep | [MagicTaleScript](https://github.com/seak123/MagicTaleScript) | TypeScript | WeChat mini-game on a hand-written TS engine framework. |
| 2020 · Sep | [MagicTale](https://github.com/seak123/MagicTale) | Cocos Creator | WeChat mini-game shooter (2D + 3D). |
| 2020 · Jul | [TeamFight](https://github.com/seak123/TeamFight) | Lua | Auto-battler with behavior-tree AI + spell/effect system. |
| 2020 · Jun | [IntelliFight](https://github.com/seak123/IntelliFight) | Unity + Lua | Auto-battler with a grid battlefield, summon & card systems. |
| 2019 · Jan | [WOFFEditor](https://github.com/seak123/WOFFEditor) | WPF C# | Node-based skill/trigger editor — author abilities as node graphs. |
| 2018 · Oct | [CardCommander](https://github.com/seak123/CardCommander) | Unity + Lua | Lua-first card battler — thin C# host, 150+ Lua gameplay scripts. |
| 2018 · Mar | [Scripts](https://github.com/seak123/Scripts) | Unity C# | Entity-component battle core — composable units, data VOs, AI. |
| 2018 · Mar | [FreeBattle](https://github.com/seak123/FreeBattle) | Unity C# | Battle demo exploring dependency injection. |

### 🧭 A few threads across these projects
- **Auto-battler AI** — behavior trees, blackboards, and priority-based decision-making (TeamFight → IntelliFight → hex-auto-battler).
- **Data-driven abilities** — node-graph ability/skill systems and visual editors (WOFFEditor, hex-auto-battler).
- **Engine plumbing** — layered `GameBase / GameCore / GameLogic` architectures, C#↔Lua bridges (xLua), and a from-scratch TypeScript engine.

<sub>Some early ideas also exist as archived variants (e.g. `ArtField` → see `TeamFight`; `NewScripts` → see `CardCommander`).</sub>
