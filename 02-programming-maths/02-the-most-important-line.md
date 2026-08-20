# The most important line

**One idea:** Every moving thing in every game moves by the same line of code — `position += velocity × dt` — which is nothing more than repeated tiny addition.

> **Previously** — [The grid under everything](../01-maths/03-the-grid-under-everything.md): a character *is* a pair of numbers `(x, y)`, and movement is arithmetic on that address. [Numbers inside a computer](01-numbers-inside-a-computer.md): positions live in floats. Now the arithmetic gets a heartbeat.

## The heartbeat

A game redraws the screen many times per second — commonly sixty. Each redraw is called a **frame**, and between one frame and the next a small slice of time passes. That slice is called **dt** ("delta time" — *delta* is maths-speak for "the change in"). At sixty frames per second, dt is about `0.016` seconds — a sixtieth.

Every frame, for every moving thing, the game runs one line:

```js
position.x += velocity.x * dt;
```

Plain-words twin: *"each heartbeat, nudge the across-address by the speed times the sliver of time that passed."*

That's it. An arrow crossing the screen, FLORA dashing, a drifting z above a swept opponent — each is this line, running sixty times a second. Movement in games is not one grand calculation; it is thousands of tiny additions, each too small to see, arriving so quickly they pour together into motion. (Film works the same way: still pictures, quickly.)

## Why the `× dt` matters

Suppose the line were only `position.x += 2` — two pixels per frame, no dt. On a sixty-frames-per-second machine the character crosses 120 pixels each second. On a fancier 120-frames machine, 240 pixels — *the same character moves twice as fast on a faster computer.* Players on different machines would experience different games.

Multiplying by dt repairs this gracefully. Write velocity in *pixels per second* (say, 120), and each frame contributes `120 × dt`. Small slices on fast machines, larger slices on slow ones — always adding up to 120 pixels for each real second, everywhere. This is called **frame-rate independence**, and the `× dt` habit is one of the first marks of well-kept game code.

Every engine hands you dt under a local name:

| Engine | dt is called |
|---|---|
| JavaScript (by hand) | you compute it from timestamps |
| GDevelop | `TimeDelta()` |
| Godot | `delta` (handed to `_process`) |
| Unity | `Time.deltaTime` |
| Unreal | `Delta Seconds` |

Same sliver, five spellings.

## Gravity, in one more line

Add a second line and arrows begin to arc:

```js
velocity.y += gravity * dt;   // each heartbeat, the downward speed grows a little
position.y += velocity.y * dt; // then the position moves by the current speed
```

Speed itself now changes a little every frame — that's *acceleration*, and it's precisely what `F = m·a` (*force equals mass times acceleration* — the archer discipline's equation in *FloralFight*) is about. Steady nudges to velocity, velocity nudging position: the arc of an arrow is two lines of repeated addition.

One whisper, no obligation attached: accumulating endless tiny changes into smooth motion is what **calculus** studies. If anyone ever asks whether you know what integration is, you may say, accurately: *"I know what it does — my games do it sixty times a second."*

**Try it (optional, ~2 minutes, nothing to hand-write):** Say the twin aloud: *"each heartbeat, nudge the position by speed times the sliver of time."* Then, if curiosity allows, watch any game character walk and try to see it — sixty nudges a second, pouring into a glide.

---

**A fine place to stop.** Next: what moves things that aren't travelling — fades, glides, regrowing petals — in [Lerp, the quiet workhorse](03-lerp-the-quiet-workhorse.md).

*Last tended: 2026-08-20*
