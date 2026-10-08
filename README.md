# Hi, I'm Evan (Yaxin Ge) 👋

**Game engineer based in Melbourne, with over seven years of commercial experience.** I develop gameplay features end to end, including their associated UI. On **_Light of Motiram_ at Tencent**, my work connected C++ gameplay systems, Lua interface logic and UMG widgets across building, watercraft, multiplayer and automated production.

I focus on making complex game rules understandable and usable: coherent player flows, explicit data and lifecycle boundaries, reusable UI where it fits, and practical debugging and performance work.

`UE4/UE5` · `UMG` · `C++` · `GAS` · `Behavior Trees` · `Navmesh` · `Replication / Netcode` · `ECS / Mass` · `Rigid-body Physics` · `Unity` · `C#` · `Lua` · `TypeScript`

## Selected gameplay and UI portfolio

Selected systems from my work on **_Light of Motiram_ at Tencent**, covering gameplay architecture, player-facing UI, multiplayer networking, content workflows and performance.

### 1. Building System — featured case study

[**Building System portfolio**](https://github.com/seak123/building-ui-portfolio)

An end-to-end building system: players select and preview pieces, build persistent homes, and use crafting, cooking and storage objects. My work covered the system architecture, placement rules and controls, associated UI, streaming-aware persistence, content-authoring workflows and optimisation.

The case follows its evolution from a **SpaceUnit / Pivot / Space** model to freer construction and **LiteMass integration**, explaining how rules, persistent data and runtime representation could change without replacing the whole interaction flow.

[System design](https://github.com/seak123/building-ui-portfolio/blob/main/docs/SYSTEM_DESIGN.md) · [Early spatial rules](https://github.com/seak123/building-ui-portfolio/blob/main/docs/SPATIAL_RULES.md) · [Lifecycles and LiteMass](https://github.com/seak123/building-ui-portfolio/blob/main/docs/LIFECYCLE_AND_SCALE.md)

### 2. Watercraft Physics and Multiplayer Sailing

[**Watercraft portfolio**](https://github.com/seak123/watercraft-physics) · Architecture reference implementation

Player-built watercraft with buoyancy, paddling, sails and steering. The technical focus is the separation of physics, controls and networking: alternative buoyancy models, fixed-substep integration, responsive input, and synchronising players walking on a moving and rotating boat.

### 3. Multiplayer and Team UI

[**Multiplayer UI portfolio**](https://github.com/seak123/multiplayer-ui-portfolio)

Team formation and matchmaking, support invitations and a contextual party HUD. The case covers a shared UI over different gameplay protocols, adapter lifecycles, asynchronous state, and choosing data-update strategies around player experience and performance cost.

### 4. Mechanical Workers and Automated Production

[**Mechanical workers portfolio**](https://github.com/seak123/mechanical-workers-ui-portfolio)

Configure creatures for production work and communicate their activity through world-space status, text and bubbles. The case connects behaviour-tree tasks, gameplay abilities, job data and UI presentation, with configuration workflows for worker behaviour and feedback.

### Supporting architecture references

- [**Data-oriented building**](https://github.com/seak123/data-oriented-building) — a separate, reduced reference implementation exploring entity data, instanced representation, replication and building operations. Start with the featured Building System case for the full development context.
- [**Automation AI production line**](https://github.com/seak123/automation-ai-productionline) — a reference implementation of worker/station coordination through data-driven jobs, behaviour trees, GAS and navigation.

The feature case studies include design decisions, screenshots and code walkthroughs with implementation details omitted. Repositories labelled as reference implementations contain separately authored, reduced examples rather than exported production systems.

---

## 🕹️ Indie prototypes & side projects

> 🗓️ **Project timeline** (newest → oldest). Dates are each project's inception, so the real chronology is clear regardless of GitHub's "last updated" sorting.

| Date | Project | Tech | What it is |
|---|---|---|---|
| **2025 · Dec** | ⭐ [hex-auto-battler](https://github.com/seak123/hex-auto-battler) | Unity + Lua | Hex-grid strategy auto-battler — deploy structures, strategize, auto-battle. **(current)** |
| 2025 · Sep | [AutoHeroDemo](https://github.com/seak123/AutoHeroDemo) | Unity + Lua | Auto-battler demo — deploy units and let them fight automatically. |
| 2021 · Jun | [CybeArtifact](https://github.com/seak123/CybeArtifact) | Unity C# + Lua | Card game framework: login → menu → battle flow with card UI. |
| 2021 · Apr | [TacticalDeck](https://github.com/seak123/TacticalDeck) | Lua | Turn-based card tactics — round state machine + replayable performer. |
| 2021 · Apr | [AutoForge](https://github.com/seak123/AutoForge) | Unity C# | Auto-battler: battle-order stream + node-based playback. |
| 2019 · Jan | ⭐ [WOFFEditor](https://github.com/seak123/WOFFEditor) | WPF C# | Node-based skill/trigger editor — author abilities as node graphs. |

<details>
<summary><b>Earlier projects (2018 – 2020)</b></summary>

| Date | Project | Tech | What it is |
|---|---|---|---|
| 2020 · Sep | [MagicTaleScript](https://github.com/seak123/MagicTaleScript) | TypeScript | WeChat mini-game on a hand-written TS engine framework. |
| 2020 · Sep | [MagicTale](https://github.com/seak123/MagicTale) | Cocos Creator | WeChat mini-game shooter (2D + 3D). |
| 2020 · Jul | [TeamFight](https://github.com/seak123/TeamFight) | Lua | Auto-battler with behavior-tree AI + spell/effect system. |
| 2020 · Jun | [IntelliFight](https://github.com/seak123/IntelliFight) | Unity + Lua | Auto-battler with a grid battlefield, summon & card systems. |
| 2018 · Oct | [CardCommander](https://github.com/seak123/CardCommander) | Unity + Lua | Lua-first card battler — thin C# host, 150+ Lua gameplay scripts. |
| 2018 · Mar | [Scripts](https://github.com/seak123/Scripts) | Unity C# | Entity-component battle core — composable units, data VOs, AI. |
| 2018 · Mar | [FreeBattle](https://github.com/seak123/FreeBattle) | Unity C# | Battle demo exploring dependency injection. |

</details>

### 🧭 A few threads across these projects
- **Auto-battler AI** — behavior trees, blackboards, and priority-based decision-making (TeamFight → IntelliFight → hex-auto-battler).
- **Data-driven abilities** — node-graph ability/skill systems and visual editors (WOFFEditor, hex-auto-battler).
- **Engine plumbing** — layered `GameBase / GameCore / GameLogic` architectures, C#↔Lua bridges (xLua), and a from-scratch TypeScript engine.

<sub>Some early ideas also exist as archived variants (e.g. `ArtField` → see `TeamFight`; `NewScripts` → see `CardCommander`).</sub>

---

## 📫 Get in touch

Currently **open to gameplay and UI engineering roles** — Melbourne, Australia (also open to remote).

- 📧 **Email** — [yaxinge.evan@gmail.com](mailto:yaxinge.evan@gmail.com)
- 💼 **LinkedIn** — [www.linkedin.com/in/gameryaxinge/](https://www.linkedin.com/in/gameryaxinge/)
- 📍 **Location** — Melbourne, AU

Happy to walk through the design decisions behind any of the systems above.
