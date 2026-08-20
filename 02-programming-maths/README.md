# 02 · Programming maths

The maths that runs inside game code — the small set of ideas that move characters, arc arrows, glide cameras, and roll fair-feeling dice.

Examples are in **JavaScript**, because this project's prototypes are HTML/JS and GDevelop exports to HTML5. Every snippet comes with a plain-words twin, and none of them require having programmed before. The ideas transfer unchanged to every engine in [05-game-engines](../05-game-engines/) — only the spelling changes.

## Pages that exist

| # | Page | One idea |
|---|---|---|
| 01 | [Numbers inside a computer](01-numbers-inside-a-computer.md) | Computers store decimals as careful approximations, and pros plan around it rather than fight it. |
| 02 | [The most important line](02-the-most-important-line.md) | All movement is `position += velocity × dt` — repeated tiny addition. |
| 03 | [Lerp, the quiet workhorse](03-lerp-the-quiet-workhorse.md) | One three-input recipe handles fades, glides, blends, and regrowing petals. |
| 04 | [Randomness that feels fair](04-randomness-that-feels-fair.md) | True randomness feels unfair; games gently rig it, on purpose, in the player's favour. |

## Pages this branch is growing toward

- [ ] Angles and rotation — degrees, radians, and why engines prefer the odd one
- [ ] Aiming with trig — pointing a thorn-bow at a moving target
- [ ] Distance and collision — circles, boxes, and the Pythagorean check
- [ ] Vectors properly — adding arrows, scaling arrows, normalizing
- [ ] Easing beyond lerp — the shapes of graceful motion
- [ ] Noise — randomness with a memory (terrain, wobble, shimmer)
- [ ] Screen shake, knockback, and other spicy applications of small maths

## Pairs well with

[07-bibliography/programming-maths.md](../07-bibliography/programming-maths.md) — Red Blob Games and easings.net first; Freya Holmér's videos when vectors arrive.

## Returning after a while?

Read any page's **Previously** box. That's the whole ritual.

---

*Last tended: 2026-08-20*
