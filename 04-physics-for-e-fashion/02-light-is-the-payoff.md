# Light is the payoff

**One idea:** LEDs are one-way devices whose color sets their price in volts — and the difference between "a bulb is on" and "a garment is luminous" is one layer of diffusing physics.

> **Previously** — [First circuit on paper](../03-electronics/02-first-circuit-on-paper.md): an LED keeps some push for itself (a red one keeps ~2 volts), and the chaperone resistor is sized from the leftover. This page explains where that "keep" comes from and how to make the resulting light beautiful.

## One-way glass

An LED — *light-emitting diode* — passes flow in one direction only. Sewn in backwards, it doesn't break; it politely does nothing, which makes "LED in backwards" the single most common first-project hiccup in all of e-textiles, and the first thing to check when a circuit sulks. Every LED marks its directions: the longer leg (or the flat side of the rim, or a printed symbol on sewable modules) tells you which way the flow may enter. Ten seconds of checking; a whole afternoon of mystery avoided.

## Color has a price list

The light's color is set by the physics inside the LED — each color of light carries a different energy per particle (blue light is more energetic than red; that's a deep and lovely fact about the universe, not a manufacturing choice). The practical consequence: **each color keeps a different share of push.**

| Color | Typical keep (volts) |
|---|---|
| red | 1.8 – 2.2 |
| amber / yellow | 2.0 – 2.2 |
| green (classic) | 2.0 – 2.4 |
| blue, white, pink, UV | 2.7 – 3.4 |

Ballparks, honestly labeled — the datasheet of *your* LED states its own number, and reading it is the professional move. The chaperone arithmetic uses the real keep: on a 5-volt supply at 20 mA, a red LED leaves `5 − 2 = 3` volts of leftover (150 Ω), while a blue one leaves `5 − 3 = 2` (100 Ω). Same recipe, different grocery prices. One garment mixing colors sizes each chaperone separately — which is why kits ship assorted resistors, a fact that reads as clutter until this paragraph and as courtesy after it.

(A 3-volt coin cell and a blue LED's ~3-volt keep sit suspiciously close together — which is exactly why tiny coin-cell "throwie" crafts often run LEDs with no resistor at all: the cell is too weak to overfeed them. A workable shortcut for that one pairing; not a general license.)

## The diffusion secret

A bare LED is a *point* — a single glaring pixel, harsh to look at directly. Yet the projects that inspire this repo glow like living things. The difference is **diffusion**: putting translucent material between LED and eye so the light scatters — bounces through the material in thousands of directions — and the point becomes a *surface*.

Organza over an LED: a soft pool. An LED inside layered petals: the whole blossom breathes light. **Fiber optics** — FLORA's stem — are diffusion's elegant cousin: light poured in one end travels *inside* the strand, reflecting off the walls, and side-emitting fibers let it leak out gently along the whole length, turning a strand into a line of light. None of this costs extra flow. Diffusion spends no power; it spends *geometry*. The most beautiful watt in e-fashion is the one you scatter well.

One perceptual footnote worth its sentence: eyes judge brightness on a compressed curve — half the flow does **not** look half as bright, it looks only somewhat dimmer. So dimming an LED to stretch a battery (next page) costs less beauty than the arithmetic suggests. The universe is, on this point, on your side.

**Try it (optional, ~2 minutes, nothing to hand-write):** Turn on your phone's flashlight and look at it briefly — a harsh point. Lay a single tissue over it: a calm pool. You have now performed the core optical trick of every luminous garment ever sewn.

---

**A fine place to stop.** Light spends energy, and energy rides along in a pocket: [Battery budgets](03-battery-budgets.md).

*Last tended: 2026-08-20*
