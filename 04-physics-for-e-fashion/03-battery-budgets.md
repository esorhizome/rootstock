# Battery budgets

**One idea:** One division — capacity over draw — estimates how long a garment will glow, which means wear-time can be *designed* instead of discovered mid-evening.

> **Previously** — [Power](../03-electronics/03-power-and-where-it-goes.md): flow times push is the spending rate. [Light is the payoff](02-light-is-the-payoff.md): each LED sips a chosen flow, ~10–20 mA. Now: how big is the pantry those sips come from?

## The pantry number

Batteries state their capacity in **milliamp-hours (mAh)**: how many milliamps a battery can supply, for how many hours, multiplied together. A 500 mAh battery can feed 500 mA for one hour — or 100 mA for five hours, or 50 mA for ten. Same pantry, different appetites.

So the estimate is one division:

$$\text{hours} \approx \text{capacity (mAh)} \div \text{draw (mA)}$$

*Glow-time is pantry over appetite.* A corsage of five LEDs at 15 mA each draws 75 mA; from a 500 mAh rechargeable pouch: `500 ÷ 75 ≈ 6.7` hours. An evening, comfortably, with encores.

## The honesty coefficient

Real batteries deliver a little less than the label under real conditions (cold air, aging cells, higher draws all tax the pantry). House habit: multiply the estimate by **0.8** and promise only that. `6.7 × 0.8 ≈ 5.3` hours — a promise the garment will keep. Engineers call this *margin*; socially it's the difference between "it lasted the whole show" and apologizing at intermission. Under-promising is a form of poise.

## Choosing the pantry itself

Three families cover nearly all e-fashion, each with a personality:

**Coin cells** (~220 mAh for the common CR2032) — weightless, sewable into anything, and *gentle by nature*: they can't push large flows even if asked, which makes them the safest possible first battery. Best for one to three LEDs. They are also non-rechargeable — fine for a brooch, wasteful for a jacket.

**AA/AAA packs** (~800–2500 mAh) — sturdy, cheap, replaceable at any corner shop mid-tour. Heavier; the weight wants a seam near the body's center (a physics point [the next page](04-seams-strain-and-motion.md) takes personally).

**LiPo pouches** (100–2500 mAh) — the wearable favourite: flat, light, rechargeable. They carry the dignity requirements from [the safety page](../03-electronics/04-safety-with-small-volts.md) — protected cells, proper chargers, no punctures — which are the entire price of their convenience.

## The three dials

When the estimate comes out short, the equation itself lists every remedy — that's the quiet gift of having one:

fewer or dimmer LEDs (smaller appetite; and the eye's compressed brightness-curve means dimmer costs less beauty than it saves power — [previous page](02-light-is-the-payoff.md)), a bigger pantry (heavier — physics charges for everything), or *cleverer spending*: LEDs that twinkle in patterns rather than burn steadily can cut average draw enormously, because an LED that's lit half the time draws half the average flow. Sparkle, it turns out, is not only prettier than steady glare — it is *cheaper*. Designers of luminous gowns lean on this constantly, and now the reason is yours.

**Try it (optional, ~2 minutes, nothing to hand-write):** Calculator: twelve LEDs at 10 mA each (`120` mA total) on a 1200 mAh pouch. Pantry over appetite: `1200 ÷ 120 = 10` hours; honesty coefficient: `× 0.8 = 8`. You've now specified a garment's evening from two numbers — before threading a single needle.

---

**A fine place to stop.** The budget survives the night; will the *stitching* survive the dancing? [Seams, strain, and motion](04-seams-strain-and-motion.md).

*Last tended: 2026-08-20*
