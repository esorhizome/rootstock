# The grid under everything

**One idea:** Two numbers can name any point on a flat surface — and this one trick is the floor that every game screen, graph, map, and embroidery pattern stands on.

> **Previously** — [Numbers you can trust](02-numbers-you-can-trust.md) put all numbers on one line: negatives leftward of zero, positives rightward. This page uses two of those lines at once. That's the only ingredient.

## A street address for points

Lay one number line flat (call it **x**, the across-line). Stand a second one upright (call it **y**, the up-line). Where they cross — where both read zero — is called the **origin**, the home square.

Now any point on the surface can be named with a pair of numbers, written `(x, y)`: *how far across, then how far up*. The point `(3, 2)` means "from home: three across, two up." That pair is a street address for a location that never had a name before. Address in, point found; point given, address readable. No ambiguity, ever, anywhere on the surface.

This idea — coordinates — is roughly four hundred years old and is quietly load-bearing for most of the modern world. Screens, GPS, graphs, architectural plans, cross-stitch charts: all of them are this page wearing different clothes.

## Your screen is one of these

Every pixel on the screen you're reading has an `(x, y)` address, and every game character is, at any instant, a pair of numbers. When *FloralFight*'s FLORA stands somewhere in the arena, the engine knows her as something like `(412, 250)` — four hundred twelve across, two hundred fifty down.

*Down?* Yes — one honest wrinkle. Most screens grow their y-numbers **downward**, because early screens drew from the top edge first, and conventions are loyal creatures. Maths class graphs grow y *upward*. Neither is wrong; they are two dialects of the same language, and every game programmer keeps a small mental sticky-note reading "screen-y goes down." You now have the same sticky-note, which puts you level with the professionals on this point.

## Movement, previewed

If a character stands at `(3, 2)` and walks one step rightward, the address becomes `(4, 2)`. Movement is *arithmetic on the address* — that's the entire secret, and the whole of [branch 02's most important line](../02-programming-maths/02-the-most-important-line.md) is this sentence with a clock attached.

And a whisper for later: the *straight-line distance* between two addresses can always be computed from the addresses alone. The recipe is called the Pythagorean theorem, it is two thousand years old, and it runs every "did the arrow reach the target?" check in every game. It gets its own page in time; nothing yet depends on it.

**Try it (optional, ~2 minutes, nothing to hand-write):** Open [Desmos](https://www.desmos.com/calculator) — free, no account, works in any browser. Type `(3, 2)` into the left panel and watch a point appear. Type a different pair. Drag the point around with your cursor and watch its address update live. That live-updating pair is what a game engine sees when a character moves.

---

**A fine place to stop.** Next: [Letters standing in](04-letters-standing-in.md) — what it means when a number's seat is held by an `x`.

*Last tended: 2026-08-20*
