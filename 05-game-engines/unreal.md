# Unreal Engine

**One idea:** Unreal carries the heaviest install and an account gate — and, in exchange, the one fully professional *visual* scripting system, where logic is a diagram you can read.

> **Previously** — [The engines overview](README.md): engines differ in friction, not in maths. Unreal's trade is distinctive: maximum weight, maximum visual-logic payoff.

## Verified facts (2026-08-20)

**Version:** 5.8.1 (the 5.8 line arrived June 2026, patched July). Epic has said 5.8 is the last planned major release of Unreal 5, with UE6's early access aimed at late 2027 — so 5.8.x should stay current unusually long.

**Cost, in plain words:** free to download and use, including commercially. Epic's cut begins only after a game earns **US$1,000,000 lifetime gross** — beyond that line, a **5% revenue share** applies (their standard terms; a day-and-date release on the Epic Games Store trims it to 3.5%, and sales made *through* that store are exempt entirely). For a solo builder, the practical reading: Unreal is free until a game has already succeeded beyond most games' wildest arcs, at which point sharing 5% will not be the day's biggest news.

**Accounts and weight, honestly:** an **Epic Games account is required** to install the engine (it arrives via the Epic launcher), and the install runs to *tens of gigabytes* — the heaviest first step of the four engines by far, worth scheduling rather than improvising. The documentation and official courses at [dev.epicgames.com](https://dev.epicgames.com/documentation/unreal-engine) read login-free.

**How logic is written:** **Blueprints** or C++. Blueprints deserve their sentence of respect: a node-graph language — boxes wired to boxes, *event → condition → action* — that is not a training-wheels mode but a first-class system that ships in commercial games. For a reader who thinks in diagrams, or for whom typing is the costly channel, Blueprints are the strongest professional argument in this branch. (C++ waits underneath for performance work, years from mattering to a beginner.) One aesthetic note this repo can't resist: a Blueprint graph makes formulas *visible* — a multiply node with two wires in and one out is `V = I × R` drawn as plumbing, which is nearly a rootstock lesson in itself.

## Where the maths lives

Vectors everywhere (the [coordinate pairs](../01-maths/03-the-grid-under-everything.md), in 3D dress); **Delta Seconds** is dt, handed to every tick event — [the most important line](../02-programming-maths/02-the-most-important-line.md) is two wired nodes; `Lerp` nodes are [the workhorse](../02-programming-maths/03-lerp-the-quiet-workhorse.md), searchable by name in the node menu. Branch 02 transfers; only the spelling becomes wiring.

## A gentle path in

1. **["Your First Hour in Unreal Engine"](https://dev.epicgames.com/documentation/unreal-engine/first-hour-in-unreal-engine)** — Epic's official guided first project; readable without an account (the engine itself needs the one you made to install).
2. **[Unreal Sensei on YouTube](https://www.youtube.com/@UnrealSensei)** — an actively maintained, beginner-first video course culture, Blueprints-forward, watchable logged-out.
3. **[The documentation](https://dev.epicgames.com/documentation/unreal-engine)** — for looking up nodes as needed; login-free.

All flagged in [the bibliography](../07-bibliography/game-engines.md).

---

**A fine place to stop.** Sibling pages: [godot.md](godot.md) · [unity.md](unity.md).

*Last tended: 2026-08-20 — versions and terms drift; re-verify before relying.*
