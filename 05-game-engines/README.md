# 05 · Game engines

An engine is three gifts in one download: a **loop** (the heartbeat that redraws the world and hands you `dt` — [branch 02's most important line](../02-programming-maths/02-the-most-important-line.md) runs inside it), an **editor** (where scenes are arranged visually), and an **exporter** (which turns the project into something playable on the web, a phone, a desktop).

The maths in [branch 02](../02-programming-maths/) is identical in every engine below — positions are coordinate pairs, movement multiplies by dt, lerp is lerp. Engines differ in *friction*: accounts, costs, download weight, and whether you type code or snap visual blocks. For this repo's readers, friction is a first-class spec, so it's tabled honestly below.

## The friction table

*Facts verified 2026-08-20 against official sources; engines move fast, so re-check before big decisions.*

| Engine | Current version | Cost, plainly | Account to use it? | How you "write" logic |
|---|---|---|---|---|
| [GDevelop](https://gdevelop.io/) | 5.6.x (rolling) | Engine free forever, open source (MIT). Optional paid cloud services. | **None** for the desktop app | Visual event sheets: *when this → do that*. No code required. |
| [Godot](godot.md) | 4.7.2 (2026-08-18) | Free forever, open source (MIT). No revenue conditions, ever. | **None**, anywhere in the pipeline | Typed code: GDScript (gentle, Python-like) or C#. |
| [Unreal](unreal.md) | 5.8.1 (2026-07) | Free; 5% revenue share only above the first US$1M lifetime gross (Epic-store sales exempt). | ⚠ Epic account to install | **Blueprints** (complete visual scripting) or C++. |
| [Unity](unity.md) | 6.5 current / 6.3 LTS | Personal tier free (under US$200k revenue/funding); splash screen optional; runtime fee cancelled. | ⚠ Unity ID to use the editor | C# code. (Bundled visual scripting exists but is in maintenance mode.) |

## An honest starting order for this repo's audience

**GDevelop** is the gentlest true on-ramp: no account, no code, and the event-sheet style ("when the mine is crossed → create explosion") reads like design notes. It is the engine the AIGR feasibility plan recommends, and its ceiling is higher than its reputation suggests. **Godot** is the gentlest *typed-code* home — zero accounts anywhere, small download, and GDScript reads closer to plain words than any other engine language. **Unreal** offers the one fully professional *visual* scripting system, Blueprints, at the price of an account and a heavyweight install. **Unity** currently carries the most friction for this audience — account-walled editor, C#-only in practice — while remaining an entirely reasonable place to end up (its tutorial ecosystem is vast).

No choice here is a marriage. The maths transfers; even most of the *design* transfers. Trying one for a weekend costs a weekend.

## Pages in this branch

- [godot.md](godot.md) — the no-account engine, verified facts + gentlest path in
- [unity.md](unity.md) — 6.5 vs 6.3 LTS explained, verified terms + path in
- [unreal.md](unreal.md) — Blueprints as visual logic, verified terms + path in
- GDevelop's fuller treatment lives in the AIGR project's own feasibility plan; its links are in [the bibliography](../07-bibliography/game-engines.md)

## Pairs well with

[07-bibliography/game-engines.md](../07-bibliography/game-engines.md) — every learning link below, gathered and flagged.

---

*Last tended: 2026-08-20*
