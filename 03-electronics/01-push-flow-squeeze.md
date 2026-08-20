# Push, flow, squeeze

**One idea:** Electricity in a circuit has exactly three main characters — push (volts), flow (amps), squeeze (ohms) — and one short law describes how they negotiate.

> **Previously** — [Letters standing in](../01-maths/04-letters-standing-in.md): a formula is a recipe with labeled boxes. This page introduces the three most-used boxes in all of electronics. No prior electronics is assumed — this *is* the beginning.

## The three characters

**Push — voltage — measured in volts (V).** How hard the electricity is being urged forward. A battery is a push-maker: a little coin cell pushes with 3 volts, a USB port with 5.

**Flow — current — measured in amps (A).** How much electricity is actually streaming past a point each second. Small crafts deal in *milliamps* (mA), thousandths of an amp: a sewn LED sips roughly 20 mA — that's `0.02` amps in its decimal outfit.

**Squeeze — resistance — measured in ohms (Ω).** How much the path fights the flow. A copper wire squeezes almost not at all; a resistor is a component built to squeeze by a precise, chosen amount.

A borrowed picture, offered honestly: water in a hose. Push is the water pressure, flow is how much water passes per second, squeeze is someone pinching the hose. More pressure, more flow; harder pinch, less flow. The picture is a loaner bicycle — genuinely useful for the first several kilometres, wobbly if ridden forever. Ride it as long as it helps and return it without guilt when it wobbles.

## The law that ties them

$$V = I \times R$$

*Push equals flow times squeeze.* This is **Ohm's law** — nearly two hundred years old, and the single most-used equation in practical electronics. (Why *I* for flow? An old French word choice, *intensité*. The letters are historical accidents; the meaning is the part that matters.)

The recipe runs in any direction, by unwrapping (the [labeled-boxes](../01-maths/04-letters-standing-in.md) move):

| Known | Wanted | Recipe | In words |
|---|---|---|---|
| flow, squeeze | push | `V = I × R` | push is flow times squeeze |
| push, squeeze | flow | `I = V ÷ R` | flow is push divided by squeeze |
| push, flow | squeeze | `R = V ÷ I` | squeeze is push divided by flow |

One law, three costumes. Working engineers do not memorize all three — they remember the relationship and unwrap on demand, or look it up. (Looking it up is the job.)

## Feel it once, in numbers

A 9-volt push through a 450-ohm squeeze: flow is `9 ÷ 450 = 0.02` amps — 20 mA, a comfortable LED sip. Double the push to 18 volts, flow doubles to 40 mA. Double the *squeeze* instead, flow halves to 10 mA. Push and flow rise together; squeeze and flow oppose each other. That opposition is the entire personality of the law, and it's why a resistor can *protect* something delicate — more squeeze, gentler flow.

In *FloralFight*, this is the equation the melee discipline resonates out of the boss's core, fragment by fragment: `V = I × R`, push equals flow times squeeze.

**Try it (optional, ~3 minutes, nothing to hand-write):** Open the [Falstad simulator](https://www.falstad.com/circuit/) — free, browser-based, no account. It loads with a working circuit already flowing (moving dots are the current). Click a resistor, nudge its value with the slider, and watch the dots slow as the squeeze rises. That is Ohm's law, live, negotiating in front of you.

---

**A fine place to stop.** Next, the three characters get their first real job: [First circuit on paper](02-first-circuit-on-paper.md), where one subtraction and one division keep an LED alive.

*Last tended: 2026-08-20*
