# Power, and where it goes

**One idea:** Power — push times flow — measures how fast energy is being spent, and every spent bit becomes either the light you wanted or heat you must respect.

> **Previously** — [Push, flow, squeeze](01-push-flow-squeeze.md): volts push (V), amps flow (I). [First circuit on paper](02-first-circuit-on-paper.md): a resistor chaperones an LED by absorbing leftover push. This page asks what "absorbing" costs.

## The second law of the branch

$$P = I \times V$$

*Power equals flow times push*, measured in **watts (W)**. Where Ohm's law describes a negotiation, this one reads a meter: how much energy is being converted *per second*, right now. A phone charger works at roughly 5–20 watts; a kettle at 2000; a sewn LED at about `0.02 × 2 = 0.04` watts — forty milliwatts, a firefly's budget.

In *FloralFight*, this is the magic discipline's equation — the one the layered-lotus magician farms out of the boss's core. Fitting: magic orbs are energy visibly spent per second.

## Energy is never mislaid

A circuit spends energy in exactly the places the push gets used, and the spending always becomes *something* — mostly light where you wanted light, and heat everywhere else. The LED's 40 milliwatts become the glow (plus a little warmth). The chaperone resistor from last page converts its share — `0.02 A × 3 V = 0.06 W` — entirely into heat.

Sixty milliwatts of heat is nothing: the resistor barely notices. But the accounting habit matters, because it scales. Components carry **power ratings** — a common little resistor is rated ¼ watt — and the rating is a politeness threshold: run below it and the part stays cool and lives long; run above it and the part runs hot, ages fast, and eventually fails. The check is one multiplication: *is my `I × V` comfortably under the rating?* `0.06` under `0.25` — comfortably. Done. That two-second multiplication is the entire discipline of "will this get hot," and it is performed with a calculator by professionals everywhere.

## Warmth is information

A component that runs warm is *reporting* its spending rate to your fingertips. Slightly warm can be normal (power resistors expect it). But *hot* — uncomfortable to touch — means the arithmetic upstairs is being exceeded somewhere: too much flow, too small a rating, or a mistake in the loop. The prototype sim in *FloralFight* teaches exactly this instinct: slide the push to 9 volts against a small squeeze and it warns the LED would cook. The warning *is* `P = I × V`, wearing a costume.

On fabric this instinct graduates from good practice to necessity — cloth insulates, bodies notice warmth, and [branch 04](../04-physics-for-e-fashion/README.md) picks up the thread properly.

## The pocket summary

Two laws now, a matched pair:

| Law | Symbols | Plain twin | What it answers |
|---|---|---|---|
| Ohm's | `V = I × R` | push = flow × squeeze | how the three characters negotiate |
| Power | `P = I × V` | spending = flow × push | how fast energy converts, and into what |

Between them they cover a startling fraction of everyday electronics. Both fit on a sticky note. Professionals keep the sticky note; memorization is nobody's rent.

**Try it (optional, ~2 minutes, nothing to hand-write):** Calculator: a USB port pushes 5 volts into a string of LEDs drawing a combined 0.1 amps. `P = 0.1 × 5` — half a watt, spent as glow and warmth. Then the politeness check in reverse: a ¼-watt resistor asked to spend half a watt is over budget at a glance. You've now done thermal engineering.

---

**A fine place to stop.** The branch's gentle sentinel comes next: [Safety with small volts](04-safety-with-small-volts.md) — short, honest, and worth the five minutes before anything touches fabric.

*Last tended: 2026-08-20*
