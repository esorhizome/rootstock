# Godot

**One idea:** Godot is the zero-account, zero-cost, genuinely-yours engine — its price is a willingness to type small amounts of a very gentle language.

> **Previously** — [The engines overview](README.md): an engine = loop + editor + exporter, and the maths transfers between all of them. This page is one engine, examined honestly.

## Verified facts (2026-08-20)

**Version:** 4.7.2 stable, released 2026-08-18 (the 4.7 line arrived June 2026). **Cost:** free, forever, open source under the MIT license — no revenue share at any income, no tiers, no seat fees; games made with it are entirely yours. **Accounts:** none to download (straight from [godotengine.org](https://godotengine.org/)), none to read the docs, none for the best learning resources. The entire pipeline, start to shipped game, can be walked without ever creating a login — unique among the big engines and a quietly big deal for low-friction learning. **Download weight:** refreshingly small (tens of MB, not tens of GB).

**How logic is written:** GDScript — Godot's own language, Python-like, designed to read gently:

```gdscript
func _process(delta):
    position.x += speed * delta
```

That's [branch 02's most important line](../02-programming-maths/02-the-most-important-line.md) wearing Godot's spelling — `delta` is dt, handed to you every heartbeat. C# is fully supported as an alternative. One honest note: Godot's built-in *visual* scripting was retired back in 4.0 — there is no official no-code path here. If typing code is a hard no, [GDevelop](README.md) keeps that door open instead; if typing *small, readable* code is merely daunting, GDScript is the gentlest version of that ask in the industry, and the resource below was built precisely for the daunted.

## Where the maths lives

Positions are `Vector2` — the [coordinate pairs](../01-maths/03-the-grid-under-everything.md), as a built-in type with arithmetic included. `lerp()` is a [built-in function](../02-programming-maths/03-lerp-the-quiet-workhorse.md). `delta` arrives in `_process(delta)`. `move_and_slide()` runs the velocity arithmetic *and* the collision checks in one call. Reading branch 02 first makes Godot's API feel like met-before friends.

## A gentle path in

1. **[Learn GDScript From Zero](https://school.gdquest.com/courses/learn_2d_gamedev_godot_4/learn_gdscript/learn_gdscript_app)** (GDQuest) — free, in-browser, no account, no install: interactive micro-lessons with instant feedback, assuming no programming history at all. Built by respected Godot educators; the single best on-ramp for this repo's readers.
2. **[Official docs, "Step by step"](https://docs.godotengine.org/en/stable/getting_started/step_by_step/index.html)** — the engine's own patient walkthrough of scenes, nodes, and signals. Public, no login.
3. **[Brackeys' Godot beginner video](https://www.youtube.com/watch?v=LOhfqjmasi0)** — one ~77-minute project built end to end, for those who prefer a single linear video to scattered pages. Watchable logged-out.

All three are flagged in [the bibliography](../07-bibliography/game-engines.md).

---

**A fine place to stop.** Sibling pages: [unity.md](unity.md) · [unreal.md](unreal.md).

*Last tended: 2026-08-20 — versions drift; re-verify before relying.*
