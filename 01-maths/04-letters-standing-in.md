# Letters standing in

**One idea:** A letter in maths is a labeled box with a number inside — and "solving" is nothing more than unwrapping the box one layer at a time.

> **Previously** — [Numbers you can trust](02-numbers-you-can-trust.md): subtracting steps leftward, dividing undoes multiplying, calculators always welcome. That's all this page leans on.

## The box

When algebra writes `x`, it is not hiding anything from you and it is not being clever. It is saying: *here is a box, labeled x, holding a number.* Sometimes the number inside isn't known yet. Sometimes it changes depending on the situation. The box lets us talk about it either way.

Formulas are recipes written with boxes. Ohm's law, `V = I × R` — *push equals flow times squeeze* — is the recipe "to find the push, take whatever is in the flow-box and multiply by whatever is in the squeeze-box." Fill the boxes, run the recipe: if the flow-box holds `2` and the squeeze-box holds `10`, the push is `20`. Filling boxes and running the recipe is most of what engineers actually do with equations, most days. It is arithmetic with labels — no mystery layer underneath.

## Unwrapping

Sometimes the situation is reversed: the *answer* is known and one box isn't. `2x + 3 = 11` says: *a mystery box was doubled, then 3 was added, and the result came out 11. What's in the box?*

Solving is unwrapping — undoing what was done, one layer at a time, outermost layer first, doing the same thing to both sides so the scales stay level:

```
2x + 3 = 11
2x     = 8        ← removed the "+3" wrapper (subtracted 3 from both sides)
 x     = 4        ← removed the "×2" wrapper (divided both sides by 2)
```

The box held `4`. Check it by re-wrapping: double 4 is 8, add 3 is 11. It holds.

Every unwrapping move is one of a few pairs of opposites: adding undoes subtracting, multiplying undoes dividing. The line `x = 4` isn't a different kind of statement from `2x + 3 = 11` — it's the *same fact*, undressed.

## Why letters and not words?

Purely for the writer's wrist. Physicists write "the push" hundreds of times a day; `V` is faster. But `V = I × R` and *"push equals flow times squeeze"* are the same sentence at two zoom levels, and you may live at whichever zoom level serves you. In this repo the plain-words twin always rides along. Out in the wild it often doesn't — which is a discourtesy of the wild, not a deficiency of yours. You are allowed to write the twin in yourself, or say it aloud over the symbols like a translation.

## One box, many wearings

The same box-letter can wear different numbers on different days — that's what makes formulas reusable. `V = I × R` worked for yesterday's LED and works for tomorrow's, because the boxes accept new contents each time. A formula is not a fact about particular numbers; it is a *shape* that many sets of numbers fit into. That shift — from numbers to shapes-that-hold-numbers — is the entire doorway into algebra, and you have now walked through it.

**Try it (optional, ~2 minutes, nothing to hand-write):** Unwrap `3x − 1 = 11` out loud, or in any typed note: what undoes the "−1"? What undoes the "×3"? (It unwraps to `x = 4` again — the boxes are reused here too.) A calculator for the arithmetic is entirely in keeping with house rules.

---

**A fine place to stop.** This branch's next pages are still growing (see [the map](README.md)). The boxes go to work immediately in [03-electronics](../03-electronics/02-first-circuit-on-paper.md), where unwrapping one recipe picks a real resistor for a real LED.

*Last tended: 2026-08-20*
