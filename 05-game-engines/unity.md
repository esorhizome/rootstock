# Unity

**One idea:** Unity pairs the industry's largest tutorial ecosystem with, currently, the most sign-in friction of the four engines — worth knowing both halves before a weekend is spent on it.

> **Previously** — [The engines overview](README.md): friction (accounts, cost, code style) is a first-class spec here. Unity's friction profile is distinctive, so this page is unusually specific about it.

## Verified facts (2026-08-20)

**Version, decoded:** two current lines exist on purpose. **Unity 6.5** (editor builds numbered 6000.5.x, released June 2026) is the newest "supported update" — the fresh-features line. **Unity 6.3 LTS** (6000.3.x, December 2025, supported into late 2027) is the Long-Term Support line — the steadier one that production teams and most tutorials target. A learner starting today does well on either; when in doubt, LTS is the calmer companion, and lessons written for one apply to the other almost everywhere at beginner level.

**Cost:** the Personal tier is free — no card — for individuals and small teams under **US$200,000** in yearly revenue/funding. The made-with-Unity splash screen became optional from Unity 6 onward. The once-notorious "runtime fee" (announced 2023) was fully cancelled in 2024 and remains cancelled; games ship with no per-install or revenue charges on the free tier.

**Accounts, honestly:** a **Unity ID is required** to activate the editor — even the free tier signs in through Unity Hub. The docs ([docs.unity3d.com](https://docs.unity3d.com/Manual/index.html)) read login-free, and Unity Learn courses are browsable logged-out, though progress-tracking invites sign-in per lesson. For readers who ration their friction budget, that's one mandatory account plus recurring nudges — the exact pattern [HOW-THIS-TEACHES](../HOW-THIS-TEACHES.md) tries to spare people, stated here so it's a known cost rather than an ambush.

**How logic is written:** C# — a capable, professional language, and a steeper first language than GDScript or event sheets. Unity's bundled visual-scripting package exists but sits in maintenance mode (no active development, uncertain future), so treat Unity as a *typed-code engine* when choosing; picking it for the visual scripting would be building on a quiet floor.

## Where the maths lives

`Vector2`/`Vector3` hold the [coordinate pairs](../01-maths/03-the-grid-under-everything.md); `Time.deltaTime` is dt (`transform.position += velocity * Time.deltaTime;` — [the most important line](../02-programming-maths/02-the-most-important-line.md), Unity spelling); `Mathf.Lerp` and `Vector2.Lerp` are [the workhorse](../02-programming-maths/03-lerp-the-quiet-workhorse.md) with a capital L. Branch 02 transfers wholesale.

## A gentle path in

1. **[Unity Learn — "Unity Essentials" pathway](https://learn.unity.com/pathway/unity-essentials)** — the official free beginner path (editor basics onward). Browsable logged-out; completion-tracking wants the ID you already made for the editor.
2. **[Code Monkey's free courses](https://unitycodemonkey.com/freecourses.php)** — complete, well-regarded free C#/Unity courses, video-first, no account.
3. **[The manual](https://docs.unity3d.com/Manual/index.html)** — reference, not bedtime reading; login-free.

All flagged in [the bibliography](../07-bibliography/game-engines.md).

---

**A fine place to stop.** Sibling pages: [godot.md](godot.md) · [unreal.md](unreal.md).

*Last tended: 2026-08-20 — versions and terms drift; re-verify before relying.*
