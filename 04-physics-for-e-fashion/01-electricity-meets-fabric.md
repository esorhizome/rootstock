# Electricity meets fabric

**One idea:** Conductive thread is a resistor wearing a disguise — every stitched centimetre adds squeeze — and this is the exact moment the maths stops being theoretical.

> **Previously** — [Push, flow, squeeze](../03-electronics/01-push-flow-squeeze.md): ohms squeeze the flow. [First circuit on paper](../03-electronics/02-first-circuit-on-paper.md): an LED's chaperone resistor is sized by `R = leftover push ÷ desired flow`. On a workbench, the wires between parts squeezed roughly zero. That assumption is about to dissolve, beautifully.

## The disguise

**Conductive thread** — usually fine stainless steel or silver-coated fibre, sewable like ordinary thread — is what replaces wire in most e-textiles. It conducts honestly, but not effortlessly: where copper wire's squeeze rounds to zero, conductive thread typically squeezes somewhere in the range of **ten to a hundred ohms per metre**, depending on the thread. The spool's product page states its own number, and that number is not fine print — it is a load-bearing spec, the single most consequential figure in the garment.

Because here is what it means: *the path itself is a component.* Sew an LED half a metre from its battery using thread rated 30 Ω/m, and the round trip (out along one path, back along the other — a full metre) quietly inserts 30 ohms of squeeze into the loop. Nobody soldered a resistor there. The garment *is* one.

## What the hidden squeeze does

Recall the chaperone arithmetic: a 3-volt coin cell, a red LED keeping 2 volts, a desired gentle 10 mA gave `R = 1 ÷ 0.01 = 100` ohms of squeeze wanted. If the stitching already contributes 30, the loop now carries 130 — and the flow obeys Ohm's law, not our intentions: `I = 1 ÷ 130 ≈ 0.0077` — about 8 mA instead of 10. The LED dims noticeably.

Nothing broke. The physics counted stitches we forgot to count. Two graceful responses exist:

**Count the thread in.** Subtract the path's squeeze from the resistor you add: wanting 100 total and stitching 30 means adding only 70. One extra subtraction, and the garment behaves exactly as designed. This — a subtraction — is the difference between "e-textiles are unpredictable" and "mine do what I intend."

**Or shrink the path's share.** Shorter runs (place the battery near the payoff); doubled thread (two parallel paths halve the squeeze — a preview of the series-and-parallel page); or thicker/better thread for the power-carrying stretches. Real tutorials in the [bibliography](../07-bibliography/e-fashion.md) do all three, and now their reasons read as arithmetic instead of folklore.

## Why the pretty projects list this first

Nearly every serious e-textile guide opens with thread choice and run length before any aesthetics — which can look, from outside, like gatekeeping ceremony. It is the opposite: it is the two-minute calculation that decides whether twenty sewn LEDs shine evenly or fade sadly toward the hem (each successive LED sits behind more accumulated thread than the last — dimming down a strand is Ohm's law, drawn in light). The physics here isn't an obstacle before the beauty. It is the *mechanism* of the beauty.

**Try it (optional, ~2 minutes, nothing to hand-write):** Calculator: thread rated 20 Ω/m, an LED sewn 25 cm from the battery. Round trip is 0.5 m, so the path squeezes `20 × 0.5 = 10` ohms. Against last page's 100-ohm plan: add 90 instead. You have now compensated for a garment's hidden resistor — the exact skill the glossy projects run on.

---

**A fine place to stop.** The thing all this thread ultimately feeds: [Light is the payoff](02-light-is-the-payoff.md).

*Last tended: 2026-08-20*
