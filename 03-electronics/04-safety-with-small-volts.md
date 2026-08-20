# Safety with small volts

**One idea:** The low-voltage crafting territory — coin cells, AA packs, USB — is gentle to humans, and exactly three things in it deserve standing respect: shorts, lithium batteries, and wall power's border.

> **Previously** — [Push, flow, squeeze](01-push-flow-squeeze.md): more squeeze means less flow. [Power](03-power-and-where-it-goes.md): flow times push becomes heat somewhere. Both laws are about to explain every rule on this page — no rule here is arbitrary.

## The gentle territory

Everything this repo builds toward — sewn LEDs, glowing corsages, fiber-optic petals — runs on 3 to 5 volts. Touching both ends of such a supply with dry fingers is a non-event: skin's squeeze is enormous (many thousands of ohms), so the flow through you rounds to nothing. This is why e-textiles are taught to children and beginners worldwide: the medium itself is forgiving. You are not handling something that is out to get you.

Respect is owed in exactly three places.

## 1 · Shorts: the no-squeeze path

A **short circuit** is a loop where the push meets almost no squeeze — battery's two ends joined by bare wire, or by two conductive threads brushing where they shouldn't. Ohm's law does what it always does: `I = V ÷ R`, and with R near zero the flow spikes as high as the battery can feed. All of it becomes heat (`P = I × V`) in the wire and the battery — fast. Results range from a drained cell and a hot wire to, with strong batteries, burned fingers or scorched fabric.

The standing habits, each cheap: no bare crossings (conductive thread paths never touch each other); disconnect the battery while sewing or rearranging; and power any *first* test of a new circuit from something weak — a coin cell's worst temper is mild, which is exactly why tutorials adore it.

## 2 · Lithium batteries: dignified, not casual

LiPo (lithium polymer) pouches hold generous energy in a soft wrapper — wonderful for wearables, and the one component in this territory with a genuine temper. The respectful terms: never puncture, crease, or sew *through* one; charge only with a proper lithium charger, never improvised; stop using any pouch that puffs; and buy from real suppliers (the [bibliography's](../07-bibliography/e-fashion.md) shops, Adafruit and SparkFun, sell protected cells and matching chargers — "protected" means a tiny built-in guardian chip, worth its pennies).

Coin cells and AA/AAA packs carry no such temper. When a project's design lets you choose, choosing the milder battery is elegant engineering, not timidity.

## 3 · The border with wall power

Mains electricity — wall sockets, 110/230 volts — is a different territory with different physics: enough push to force meaningful flow through skin. The border crossing is a hard line, stated once and kindly: **nothing in this repo, and nothing sewn to a body, connects to a wall socket directly.** Wall power enters this hobby only pre-tamed — as the 5-volt output of a certified USB adapter or power bank, its taming done inside a sealed box by people licensed to tame it. On the craft side of that border, you inherit the gentleness. There is no project in e-fashion that needs to cross it raw, ever.

## Fabric's two extra notes

Cloth insulates heat in (a warm component under three layers stays warmer than on a bench — size resistors with margin, per the [power page](03-power-and-where-it-goes.md)), and bodies sweat while rain falls (water plus circuits = misbehaviour and corrosion, so power down when soaked; washing has its own future page in [branch 04](../04-physics-for-e-fashion/README.md)).

**Try it (optional, ~1 minute, nothing to hand-write):** Say the three respects aloud, once: *"No lazy loops. Lithium with dignity. The wall stays on its side."* That sentence is the branch's entire safety canon at current size.

---

**A fine place to stop.** The electronics so far assumed copper. [Branch 04](../04-physics-for-e-fashion/01-electricity-meets-fabric.md) replaces copper with thread — and the arithmetic gets pleasantly real.

*Last tended: 2026-08-20*
