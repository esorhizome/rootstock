# Lerp, the quiet workhorse

**One idea:** One tiny recipe — "start, end, and how-far-along" — powers fades, camera glides, color blends, and petals regrowing after a match.

> **Previously** — [The most important line](02-the-most-important-line.md): games run in heartbeats (frames), each `dt` seconds apart. [Numbers you can trust](../01-maths/02-numbers-you-can-trust.md): `0.75` and `75%` are the same creature. That creature stars in this page.

## The recipe

**Lerp** is short for *linear interpolation*, which is a formal name for something you already do by eye: finding the in-between. Halfway between 10 and 20 is 15. A quarter of the way is 12.5. Lerp is that, written as a recipe with three boxes:

```js
function lerp(start, end, t) {
  return start + (end - start) * t;
}
```

Plain-words twin: *"begin at the start, and walk t-of-the-way toward the end."* The box `t` holds a number from `0` to `1` meaning *how far along* — `0` is "still at the start," `1` is "arrived," `0.5` is "halfway." (That's a percent in its decimal outfit: `t = 0.25` is 25% of the way.)

```js
lerp(10, 20, 0.5)   // 15   — halfway
lerp(10, 20, 0.25)  // 12.5 — a quarter along
lerp(0, 255, 0.1)   // 25.5 — a dim tenth of full brightness
```

## Why one recipe carries so much

Because "in-between" is most of what motion and mood are made of:

**Fading** — lerp a sprite's opacity from `1` to `0` as `t` climbs, and it dissolves. In *FloralFight*, the "SWEPT!" banner easing in is a lerp on opacity and position.

**Camera glide** — lerp the camera from where it is toward the fighter each frame, and it follows with a soft, deliberate lag instead of a rigid stare.

**Color blends** — lerp the red, green, and blue channels separately and one color pours into another. A bruise-purple arena washing back to dawn tones after a match: three lerps.

**Petal regrowth** — when FLORA wins and her corolla refills petal by petal, each petal can lerp from scale `0` to scale `1`, slightly staggered. The stagger is the grace note; the lerp is the engine.

The pattern for animating any of these over, say, half a second: keep a small clock, feed it to `t`.

```js
t += dt / 0.5;                    // t crawls from 0 to 1 across 0.5 seconds
petal.scale = lerp(0, 1, Math.min(t, 1));
```

## Bending t: a preview of easing

Raw lerp moves at one steady rate, which reads as competent but slightly mechanical. The refinement is delightfully cheap: *bend t before feeding it in.* Feed `t * t` and motion starts gently, then commits. Feed `1 - (1 - t) * (1 - t)` and it arrives softly, like a settling leaf. These bends are called **easing functions**, and [easings.net](https://easings.net/) is a free, no-account gallery where every one of them is a small animation you can watch — worth a visit purely as a gallery of graceful motion.

One honest flag for later: code in the wild sometimes lerps *from the current position* toward a target every frame (`x = lerp(x, target, 0.1)`). It works and feels silky, but it behaves differently from the clock version — a detail with its own page someday. If you meet it before then, know it's a cousin, not a contradiction.

**Try it (optional, ~2 minutes, nothing to hand-write):** In a browser console (F12 → Console), paste the three-line `lerp` function above, press Enter, then try `lerp(10, 20, 0.75)`. Before pressing Enter, guess it aloud. (Three quarters of the way from 10 to 20 — the guess is probably already correct.)

---

**A fine place to stop.** Next: why honest dice feel dishonest, in [Randomness that feels fair](04-randomness-that-feels-fair.md).

*Last tended: 2026-08-20*
