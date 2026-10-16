# LESSON OB-08 — The Greeks Are Gauges (Delta, Theta, Gamma, Vega)

- **Part:** II — The Mechanics
- **Prerequisites:** OB-02 (Call = Up. Put = Down.), OB-03 (Contract Anatomy)
- **Next lesson:** OB-09 — Implied Volatility (the storm gauge gets its own lesson)
- **Visual page:** Options Playbook, "The Greeks Are Gauges"
- **Rule for every example in this pack:** hypothetical only. Never present an example as a trade suggestion.

## Concepts

### OB-08-01 — Four gauges, one dashboard
The Greeks are four readings that describe how an option's price will behave — before it behaves that way. You do not trade the gauges; you read them, the way a pilot reads instruments instead of guessing at the weather. Every contract on every chain carries all four, all the time.

### OB-08-02 — Delta = speed
Delta is how much the option's price moves for a $1 move in the stock. A call with delta 0.50 gains about 50 cents when the stock rises a dollar — $50 per contract. Calls run from 0 to +1; puts from −1 to 0; the deeper in the money, the faster the option travels (OB-07).

### OB-08-03 — Theta = melt
Theta is the value an option loses per day, all else equal — the daily rent on the extrinsic block (OB-06). A theta of −0.05 means roughly $5 per contract quietly evaporating every day the stock stands still. The melt runs on weekends too; the calendar does not pause for markets being closed.

### OB-08-04 — Gamma = acceleration
Gamma is how fast delta itself changes as the stock moves. High gamma means the speedometer is being rebuilt while you drive — small stock moves produce big swings in sensitivity. Gamma is highest for at-the-money options near expiry, which is why expiry week feels violent.

### OB-08-05 — Vega = storm gauge
Vega is the price change for a one-point move in implied volatility (OB-09). A vega of 0.12 means a 3-point rise in IV adds about 36 cents to the premium with the stock completely still. Bought options are long vega — they gain when the storm forecast worsens and bleed when it clears.

### OB-08-06 — The seat flips the sign (links OB-05)
The gauges sit on the contract; who benefits depends on which side of it you hold. Theta melts the buyer's asset and is the seller's income. Vega inflates the buyer's premium and threatens the seller's. Same numbers, opposite hopes — that is why buyer and seller are not playing the same game.

### OB-08-07 — Gauges are local readings, not promises
A Greek describes behavior at today's price, today's clock, today's storm reading. After a real move, the gauges themselves have changed. Professionals re-read the dashboard constantly; beginners take one reading at purchase and frame it.

## Worked examples (hypothetical)

### Example A — delta and theta on one position
You hold a 60 call on a stock trading at $60. Premium $3.20. Delta 0.52, theta −0.045.
- Stock rises $1 → the call gains about $0.52 per share: new value ≈ $3.72, worth about **+$52 per contract**
- Stock instead goes nowhere for 3 days → melt = 3 × $0.045 = $0.135 per share: about **−$13.50 per contract**, spent on standing still
- The two gauges fight: the stock must move faster than the melt, or the melt wins

### Example B — gamma and vega near expiry
Same 60 call, now close to expiry. Gamma 0.09, vega 0.11.
- Stock rises $1: delta climbs from 0.52 to about **0.61** (0.52 + 0.09). The *next* dollar of stock movement is worth roughly $0.61 to the option, not $0.52 — the contract is accelerating
- Implied volatility rises 3 points into an announcement, stock unmoved: premium gains about 3 × $0.11 = **$0.33 per share, +$33 per contract** — pure weather, no wind in the stock at all

## Common misconceptions

1. **"Delta is the probability the option expires in the money."** Traders use delta as a rough mental proxy, but delta is a sensitivity — a speed. Probabilities belong to models; the gauge on your chain measures movement, not destiny.
2. **"Theta only matters in the last week."** Theta runs every single day of an option's life. It is slower and quieter early — which is exactly how it takes money from people who aren't watching for it.
3. **"The Greeks are predictions I can set and forget."** They are measurements taken at one price and one moment. After the market moves, the readings have moved with it. A dashboard you read once is decoration.

## Quiz bank (scenario style — ask one at a time; explain each answer in one line)

**Q1 · OB-08-02.** A call has delta 0.40. The stock jumps $2. Roughly what happens to the call's premium?
- a) It gains about $2.00 — options move dollar-for-dollar with the stock *(misconception: the default sensitivity imagined as one-to-one)*
- b) It gains about $0.80 per share — about $80 per contract ✔
- c) It gains $0.40 total for the whole contract *(misconception: the per-share reading treated as a per-contract total — the ×100 rule forgotten)*
- d) Nobody can say — the Greeks are decorative *(misconception: instruments dismissed because they are approximations)*
**Why:** Delta × the move = 0.40 × $2 = $0.80 per share. Per contract, multiply by 100: $80.

**Q2 · OB-08-03.** You own a call with theta −0.06. For five straight days the stock does absolutely nothing. Roughly where is your premium?
- a) Unchanged — nothing moved, so nothing changed *(misconception: price imagined to require a stock move in order to change)*
- b) Down about $0.06 in total *(misconception: a daily per-share figure read as a one-time per-contract fee)*
- c) Down about $0.30 per share — about $30 per contract ✔
**Why:** Theta accrues daily: 5 days × $0.06 = $0.30 per share, and per contract that is $30 spent on a stock that never moved.

**Q3 · OB-08-04.** Two calls on the same stock, both at the money: one expires in 60 days, one expires today. Which has the larger gamma — whose delta whips around most violently per dollar of stock movement?
- a) The 60-day call — more time means more sensitivity *(misconception: duration confused with acceleration)*
- b) The call expiring today ✔
- c) They are identical — gamma is a property of the strike alone *(misconception: the clock's role in gamma ignored)*
**Why:** Gamma concentrates at the money as expiry approaches. On the last day, a one-dollar move can take a call from hopeless to fully priced — that whipping is gamma.

**Q4 · OB-08-05.** You own a call with vega 0.14. A rumor sends implied volatility up 4 points while the stock price does not move at all. Your premium:
- a) Is unchanged — the stock didn't move *(misconception: the stock's price treated as the only input to the option's price)*
- b) Gains about $0.56 per share ✔
- c) Loses about $0.56 per share *(misconception: the vega sign flipped — rising IV hurts sellers of options, not owners)*
**Why:** Bought options are long vega: 4 points × 0.14 = $0.56 of premium created by weather alone (OB-09 is this gauge's whole lesson).

**Q5 · OB-08-06.** A buyer and a seller hold opposite sides of the same contract. Theta is −0.05. Who is the melt paying?
- a) Neither — theta is theoretical *(misconception: a measurement mistaken for an abstraction with no cash behind it)*
- b) The seller: the buyer's position loses about $5 per contract per day to time, and that decay is precisely the seller's edge ✔
- c) The broker, as a holding fee *(misconception: time decay mistaken for an account charge)*
**Why:** The gauge sits on the contract; the seat decides the sign of the benefit. Every dollar of extrinsic value the buyer melts is a dollar the seller no longer owes.

**Spaced repetition rule:** any question missed resurfaces on day 3 and again on day 7, re-asked with different numbers. Two clean passes in a row retire the question.

## Daily teaching protocol (for the buyer's AI)

- **Morning (with the briefing):** Teach the picture — a dashboard of four gauges: speed, melt, acceleration, storm. Then find ONE real example in today's market: open a live chain for a liquid stock, read all four numbers off one real contract, and say out loud what each gauge predicts for that contract today. Hypothetical only — a reading lesson, never a trade suggestion.
- **Evening:** Second angle — misconception #1 ("delta is a probability") — then run the quiz, one question at a time. Log misses by concept ID.
- **Close:** Preview tomorrow — OB-09, Implied Volatility: "one gauge deserves its own lesson. Tomorrow: why premiums inflate before the news — and collapse the moment it lands."
