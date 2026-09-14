# Hi, I'm Evan (Yaxin Ge) 👋

**Game engineer based in Melbourne, with over seven years of commercial experience.** I develop gameplay features end to end, including their associated UI. On **_Light of Motiram_ at Tencent**, my work connected C++ gameplay systems, Lua interface logic and UMG widgets across building, multiplayer and automated production.

I focus on making complex game rules understandable and usable: coherent player flows, explicit data and lifecycle boundaries, reusable UI where it fits, and practical debugging and performance work.

`UE4/UE5` · `UMG` · `C++` · `GAS` · `Behavior Trees` · `Navmesh` · `Replication / Netcode` · `ECS / Mass` · `Rigid-body Physics` · `Unity` · `C#` · `Lua` · `TypeScript`

## Selected UI engineering case studies

These three case studies document **my past development and maintenance work on _Light of Motiram_**. Each connects the player experience to implementation, design decisions and observable outcomes.

The code walkthroughs preserve relevant interfaces and call relationships while omitting implementation details. Separately labelled reference models and tests were added for the portfolio; each repository includes its evidence scope and footage credits. The main reading path is in English, with a Chinese README available.

### 1. Building and interactable UI

[![Equipment-workbench UI showing weapon progression, product selection and material requirements.](https://raw.githubusercontent.com/seak123/building-ui-portfolio/main/media/screenshots/Equipment_Workbench.png)](https://github.com/seak123/building-ui-portfolio)

**From placing an object to using it:** building catalogue and contextual controls, equipment and crafting workbenches, storage interactions and item selectors.

- **My work:** initiated the building system and developed its gameplay and associated UI; developed and maintained constructed-object interactions across C++, Lua and UMG.
- **Key decisions:** specialised layouts for workbench progression, shared inventory presentation for storage, and common material-tracking guidance. Input and actions follow the current panel and building context.
- **Engineering focus:** UI composition, player recovery flows, interaction lifetime and storage refresh costs.

[Explore the case study →](https://github.com/seak123/building-ui-portfolio) · [Design decisions](https://github.com/seak123/building-ui-portfolio/blob/main/docs/DECISIONS.md) · [Code tour](https://github.com/seak123/building-ui-portfolio/blob/main/docs/CODE_TOUR.md)

### 2. Multiplayer and team UI

[![Team setup with member slots, leader identification and an invitation browser.](https://raw.githubusercontent.com/seak123/multiplayer-ui-portfolio/main/media/screenshots/Team_MainUI.png)](https://github.com/seak123/multiplayer-ui-portfolio)

**From finding teammates to playing together:** team setup, support invitations, compact team status and the in-game party HUD.

- **My work:** developed and maintained team and support UI integration, implemented the party HUD, and worked on state adaptation, refresh performance and ongoing data-freshness fixes.
- **Key decisions:** translate arena and PvE protocols into a common UI-facing model; separate hiding a panel from leaving a team; give roster structure, live combat values and player profiles different refresh responsibilities.
- **Engineering focus:** multiplayer state, asynchronous data, callback debugging and logic-layer UI performance.

[Explore the case study →](https://github.com/seak123/multiplayer-ui-portfolio) · [HUD performance](https://github.com/seak123/multiplayer-ui-portfolio/blob/main/docs/HUD_PERFORMANCE.md) · [Design decisions](https://github.com/seak123/multiplayer-ui-portfolio/blob/main/docs/DECISIONS.md)

### 3. Mechanical workers and world-space UI

[![Mechanical workers beside furnaces, with overhead feedback distinguishing movement from active work.](https://raw.githubusercontent.com/seak123/mechanical-workers-ui-portfolio/main/media/screenshots/world-work-phases.png)](https://github.com/seak123/mechanical-workers-ui-portfolio)

**From automated jobs to readable feedback:** production behaviour, overhead work status, item bubbles and data-driven content configuration.

- **My work:** developed and maintained production-to-behaviour integration, world-space feedback, job/payload consistency and the worker-configuration workflow.
- **Key decisions:** connect behaviour tasks and gameplay abilities to shared status mappings; separate the current activity from its item payload; keep job transitions and destination changes explicit.
- **Engineering focus:** gameplay-driven UI, behaviour trees and GAS, state lifecycle, and configuration linking Actor Blueprints, work abilities, text, imagery and animation.

[Explore the case study →](https://github.com/seak123/mechanical-workers-ui-portfolio) · [Configuration workflow](https://github.com/seak123/mechanical-workers-ui-portfolio/blob/main/docs/AUTHORING.md) · [Design decisions](https://github.com/seak123/mechanical-workers-ui-portfolio/blob/main/docs/DECISIONS.md)

---

## Gameplay architecture reference projects

Core gameplay systems I owned on **_Light of Motiram_** (Tencent) — an open-world multiplayer survival title in **Unreal Engine · C++**, where players build persistent homes, sail player-built watercraft, and automate production with creatures. The repositories below are **clean-room reference implementations** — architecture, design decisions, and technique, written for portfolio purposes with **no proprietary source**.

| System | Repository | Gameplay | Engineering |
|---|---|---|---|
| 🚢 **Watercraft physics & netcode** | [watercraft-physics](https://github.com/seak123/watercraft-physics) | Board and crew a player-built raft — paddle or raise the sail and catch the wind, steer by rudder, ride a trochoidal (Gerstner) wave field that shoals toward the coast. | Two buoyancy solutions behind one interface (sample-point vs submerged-volume with a true, self-moving center of buoyancy), frame-rate-independent fixed-substep physics, and sync of players walking on a *moving, rotating* platform via local-frame replication + prediction. |
| 🏗️ **Data-oriented building** | [data-oriented-building](https://github.com/seak123/data-oriented-building) | Build freely from pieces that snap by priority, must be structurally supported or they collapse, and run production lines on fuel / workload / product queues. | ECS / Mass-style entities + fragments instead of per-actor for **thousands** of persistent objects — instanced rendering, throttled delta replication with weak-net adaptation, capped on-demand actor pool, and support propagation solved by amortized iterative relaxation. |
| ⚙️ **Automation AI** | [automation-ai-productionline](https://github.com/seak123/automation-ai-productionline) | Assign creatures to stations and they run the line themselves — skill-typed jobs with headcounts, across 13 target kinds from Actors and foliage instances to purely virtual targets. | **GAS + behavior trees + navigation** behind clean seams, so one worker-AI drives any station by data alone; job-driven matching keeps multi-worker jobs staffed, with continuous and endless work modes. |

<sub>These are reference write-ups authored by me to document architecture and technique; they contain no proprietary or third-party code.</sub>

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
