# First circuit on paper

**One idea:** One subtraction and one division — nothing more — pick the resistor that lets an LED glow for years instead of dying in a blink.

> **Previously** — [Push, flow, squeeze](01-push-flow-squeeze.md): volts push, amps flow, ohms squeeze, and `R = V ÷ I` (*squeeze is push divided by flow*) is Ohm's law unwrapped for finding a resistor. That one costume of the law is all this page uses.

## The cast

Three parts, joined in a loop:

**A battery** — the push-maker. Today's is a small 5-volt supply (a USB power bank, say).

**An LED** — the payoff: a light-emitting diode, the tiny lamp of all e-fashion. An LED has two fixed appetites, printed on its datasheet (the little spec sheet every component ships with — looking at it is standard practice, not remedial). First, it *keeps* some push for itself whenever it is on — a red LED keeps about 2 volts. Second, it wants a modest flow — about 20 mA (`0.02` A) for full comfortable brightness.

**A resistor** — the chaperone. Here is the LED's one character flaw: it has almost no squeeze of its own. Connected straight to the battery, the flow through it would spike enormously — and it burns out, sometimes instantly, occasionally with a tiny sad *pop*. The resistor stands in the loop to provide the squeeze the LED lacks. Nearly every LED you have ever seen glowing calmly had a chaperone in line with it.

## The arithmetic, slowly

The question: *how much squeeze?* Two steps.

**Step one — subtraction.** The LED keeps 2 volts of the battery's 5 for itself. Whatever remains lands on the resistor:

```
5 volts − 2 volts = 3 volts
```

*The resistor's share of the push is the battery's push minus the LED's keep.*

**Step two — division.** The resistor must turn its 3-volt share into a gentle 20 mA flow. Ohm's law, in its `R = V ÷ I` costume:

```
R = 3 ÷ 0.02 = 150 ohms
```

*Squeeze needed is the leftover push divided by the flow we want.* A 150-ohm resistor — a real, standard value sold everywhere for pennies — and the LED glows, comfortable, indefinitely.

The whole ceremony, as one recipe worth keeping:

$$R = (V_{battery} - V_{LED}) \div I$$

*Squeeze equals leftover push divided by desired flow.* This is, by a wide margin, the most-performed calculation in hobby electronics. Professionals type it into calculators. So will you; the calculator is house policy anyway.

## The forgiving direction

No exact match in the parts drawer? Round the squeeze **upward** — 220 ohms instead of 150. More squeeze means less flow means a slightly dimmer, cooler, longer-lived LED. Rounding *down* squeezes less and feeds more flow than the LED wants, which shortens its life. The graceful failure is always the dimmer one. (Often the dimmer version even looks better on fabric — full brightness can be glaring at close range.)

One forward note: the "2 volts" was for a red LED. Blue and white LEDs keep closer to 3, which changes step one's subtraction — the reason [the light page](../04-physics-for-e-fashion/02-light-is-the-payoff.md) exists.

**Try it (optional, ~3 minutes, nothing to hand-write):** With any calculator: a 3-volt coin cell, a red LED keeping 2 volts, a gentle 10 mA (`0.01` A) target — leftover push is `3 − 2 = 1` volt, so squeeze is `1 ÷ 0.01 = 100` ohms. You have now sized a real component for a real wearable circuit, which is not a metaphor: this exact sum is performed for every LED sewn onto every jacket in every tutorial in [the e-fashion bibliography](../07-bibliography/e-fashion.md).

---

**A fine place to stop.** Where does the energy the resistor absorbs *go*? [Power, and where it goes](03-power-and-where-it-goes.md) follows the trail.

*Last tended: 2026-08-20*
