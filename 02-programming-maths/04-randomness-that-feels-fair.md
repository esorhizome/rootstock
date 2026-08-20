# Randomness that feels fair

**One idea:** Honest randomness produces streaks that feel rigged, so games quietly reshape it — and knowing the reshaping tricks is a designer's superpower, not a scandal.

> **Previously** — [Numbers inside a computer](01-numbers-inside-a-computer.md): floats live between the integers. This page begins with a float factory. No other page is required.

## The faucet

JavaScript's randomness faucet is:

```js
Math.random()   // a float from 0 up to (but never reaching) 1
```

Each call pours out a fresh number like `0.7284915…` — somewhere in `[0, 1)`, every region equally likely. Plain-words twin: *"a spinner that lands anywhere between zero and one, with no favourite spots."*

Everything else is plumbing on that faucet:

```js
Math.random() * 10;                       // a float from 0 up to 10
5 + Math.random() * 3;                    // a float from 5 up to 8
Math.floor(Math.random() * 6) + 1;        // a die: integer 1..6, each equally likely
```

That last line, read as words: *spin the spinner, stretch it across six lanes, chop off the decimals to get a lane number 0–5, then add 1 so the lanes read 1–6.* Every loot roll and critical hit in gaming history is a costume on this line.

## The uncomfortable truth about honest dice

Roll a fair die enough times and streaks *will* happen — five 6s in a row, or no 6 for thirty rolls. Not "might": will. Genuine randomness is far streakier than human intuition expects, because our pattern-hungry minds treat clusters as messages.

So a player who misses four "80% chance" hits in a row concludes — reasonably, wrongly — that the game is lying. The maths is innocent; the *feeling* is real. And games are in the feelings business.

## The gentle riggings

Game designers therefore reshape randomness toward how fairness *feels*. Three standard tools, all honorable:

**The shuffled bag.** Instead of rolling for each event, put every outcome in a bag, shuffle, and draw without replacement; refill when empty. Variety is now *guaranteed* — no outcome can flood or vanish. (Tetris has dealt pieces this way for years.)

**The pity timer.** Each miss quietly raises the next chance, so cruel streaks physically cannot run long. The player experiences "my luck held out eventually," which is exactly the story a kind game wants to tell.

**The fixed schedule wearing randomness's clothes.** Sometimes the graceful move is no dice at all. *FloralFight*'s prototype drops an equation fragment on every second landed hit — a plain, dependable rhythm. Players read steady rewards as fairness itself, and a learning game especially has no business gambling with someone's "understanding delayed" moments.

## Seeds: replayable luck

One more tool worth meeting early. A **seed** is a starting number fed to a random generator so it produces the *same* "random" sequence every time. Same seed, same world, same drops — which is how daily-challenge modes let every player face identical luck, and how a bug that "only happens sometimes" becomes catchable. (`Math.random()` itself doesn't accept a seed; small free libraries add it. What matters today is knowing the idea exists.)

**Try it (optional, ~2 minutes, nothing to hand-write):** In a browser console, type `Math.floor(Math.random() * 6) + 1` and press the up-arrow + Enter to reroll it ten times or so. Watch for a repeat — a streak — and notice the tiny *"hm, rigged?"* reflex in your own mind arriving even though you built the die yourself. That reflex is this entire page, felt firsthand.

---

**A fine place to stop.** This branch's remaining pages are on [the map](README.md). For a beautiful outside companion, [Red Blob Games on probability](https://www.redblobgames.com/) pairs well from the bibliography.

*Last tended: 2026-08-20*
