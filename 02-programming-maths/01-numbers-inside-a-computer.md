# Numbers inside a computer

**One idea:** Computers store decimal numbers as very careful approximations, so professionals compare them with a tolerance instead of demanding exactness — and now you will too.

> **Previously** — [Numbers you can trust](../01-maths/02-numbers-you-can-trust.md) showed that `1/3` stays exact while `0.3333…` has to trail off somewhere. Computers live with a version of that same trailing-off. No code experience is assumed on this page.

## Two kinds of number

Game code mostly holds numbers in two containers.

**Integers** — whole numbers: `0`, `7`, `−3`, `412`. Counting things. A score, a number of petals, a number of collected equation fragments. Integers are stored *exactly*; an integer never drifts.

**Floats** (floating-point numbers) — numbers with a decimal point: `0.5`, `3.14159`, `−0.02`. Positions, speeds, volumes, time. Floats are stored as *approximations* — extremely good ones, accurate to roughly fifteen meaningful digits, but approximations all the same.

## The famous surprise

Open any browser, press F12, click "Console," and type:

```js
0.1 + 0.2
```

The computer answers:

```
0.30000000000000004
```

Not `0.3`. This is not a bug, not your machine misbehaving, and not a trick question — every mainstream computer on Earth gives this answer. In plain words: *computers store numbers in base two, and one-tenth cannot be written exactly in base two, the same way one-third cannot be written exactly in our base ten.* So the machine stores the nearest number it can represent, and two tiny roundings peek out at the end.

Fifteen digits of accuracy is astonishingly good — a float describing the distance to the Moon would be off by less than a hair's width. The surprise is only that the error *exists*, not that it's large.

## The professional habit

The habit that follows: **never ask floats "are you exactly equal?"** — ask "are you close enough?"

```js
// Fragile — can fail because of the crumbs:
if (opacity === 0.3) { ... }

// House style — compare with a tolerance:
if (Math.abs(opacity - 0.3) < 0.0001) { ... }
```

The plain-words twin: *"is the distance between these two numbers smaller than a dust speck?"* The dust speck (often called an *epsilon*) is chosen to be far smaller than anything a player could perceive and far larger than float crumbs. This one habit dissolves an entire category of mysterious bugs before they're born.

## Where each container belongs

Count things a player would notice being wrong — score, currency, petals remaining, fragments collected — in **integers**, where exactness is guaranteed. Let positions, speeds, and times be **floats** and never demand exactness of them: a character standing at `x = 100.00000000000001` is standing at 100 for every purpose a game has. The crumbs are harmless until someone writes `===`, and nobody here will.

**Try it (optional, ~2 minutes, nothing to hand-write):** In that same browser console, type `0.1 + 0.2` and see the famous answer with your own eyes. Then type `Math.abs(0.1 + 0.2 - 0.3) < 0.0001` and watch the computer say `true` — the dust-speck comparison, agreeing that close-enough is enough.

---

**A fine place to stop.** Next, floats get their signature job: [The most important line](02-the-most-important-line.md).

*Last tended: 2026-08-20*
