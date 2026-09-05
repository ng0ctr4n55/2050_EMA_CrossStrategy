# Supply & Demand Zones — Video Summary + Calculation Research

**Video URL:** https://www.youtube.com/watch?v=e-QmGJU1XYc
**Video ID:** e-QmGJU1XYc
**Duration:** ~8.5 minutes
**Topic:** A 3-step price-action trading strategy: market structure + supply/demand zones + risk-to-reward filter

---

## Video Summary

The video teaches a 3-step, indicator-free trading formula the presenter claims is profitable over long-term backtests. The strategy combines market structure, supply/demand zones, and a strict risk-to-reward filter.

### Step 1 — Market Structure (trend identification)

- **Uptrend:** higher highs and higher lows. **Downtrend:** lower lows and lower highs.
- The presenter's key (non-standard) rule: **a low is only "valid" if the move that formed it broke the previous high**. If a pullback makes a low without breaking the prior high, it is *not* a valid low.
- Consequence: a chart can appear to "break a low" and look like a reversal, but if that low never broke the previous high, the uptrend is still intact — only longs are considered.
- The trend only flips to a downtrend when price breaks the **most recent valid low**. Conversely, when price breaks the previous high, the "valid low" transfers to the newer, higher low.
- The presenter stresses this is the most important step: get it wrong and the whole strategy fails.

### Step 2 — Supply and Demand Zones

- **Demand zones** (long setups) are found in uptrends; **supply zones** (short setups) in downtrends.
- Rationale: an area where price consolidated before a sharp impulse move is where many traders bought (or sold); when price retests that area, the same behavior is expected to repeat.
- **How to mark a zone:** find the consolidation (sideways area) immediately before the big impulse move, then draw a rectangle from the low to the high of the **candle right before the impulse**.
- **Execution:**
  - Uptrend: wait for price to re-enter the demand zone → enter long → stop loss just **below** the zone → take profit at the **recent high**.
  - Downtrend: wait for a retest of the supply zone → enter short → stop loss just **above** the zone → take profit at the **recent low**.
  - Only trade in the direction of the established trend (no counter-trend trades).

### Step 3 — Risk-to-Reward Filter

- Only take trades with **risk-to-reward above 2.5:1** (e.g., risking $100 to make $250).
- Even if a setup passes steps 1 and 2, it is skipped if the RR (based on the zone stop and the recent-high/low target) is below 2.5.
- The presenter claims this single filter substantially raises the strategy's profitability.

### Notes / Caveats

- The examples shown are cherry-picked winning walkthroughs; the claim of being "backtested 1000s of times and profitable every month" is asserted, not demonstrated with data in the video.
- Supply/demand zone boundaries ("previous candle before the impulse") are subjective, so results depend heavily on consistent application.
- The presenter's "valid low" rule is an unconventional definition of market structure — it differs from conventional swing-low definitions, which is the video's main distinguishing idea.

---

# Research: How to Calculate Supply & Demand Zones

Compiled from multiple sources (links at bottom). The video's "mark the candle before the impulse" is one simplified variant; the widely-used methodology is more quantified.

## 1. Core Concept

A zone is the **base** (tight consolidation) immediately before a strong **impulse move** away from it. The theory: institutional orders could not all be filled during the base, so unfilled orders remain resting there; when price returns, they react again. This is why zones are *areas* (rectangles), not lines like classic support/resistance, and why they are created by explosive moves rather than repeated touches.

## 2. The Four Zone Patterns

| Pattern | Structure | Zone Type |
|---------|-----------|-----------|
| **RBR** — Rally-Base-Rally | Up-move → base → up-move continues | Demand (continuation, uptrend) |
| **DBR** — Drop-Base-Rally | Down-move → base → reverses up | Demand (reversal, at bottom) |
| **DBD** — Drop-Base-Drop | Down-move → base → down-move continues | Supply (continuation, downtrend) |
| **RBD** — Rally-Base-Drop | Up-move → base → reverses down | Supply (reversal, at top) |

## 3. Step-by-Step Calculation

### Step 1 — Find a qualifying impulse move

A move qualifies as an impulse only if it is measurably stronger than normal price action. Common quantified thresholds:

- **Size vs. average candle (ATR):** impulse candles should be at least **2–3× the average candle size / ATR** of that timeframe (e.g., a 100-pip impulse candle on a chart where average candles are 40 pips qualifies).
- **Number of candles:** typically **3+ consecutive large candles** in one direction, or one outsized displacement candle.
- **Candle anatomy:** full bodies with **small wicks** — algorithmic scanners use a **body-to-wick ratio** (commonly body ≥ ~2/3 of the candle, or body ≥ 2× total wicks). Long overlapping wicks = drift, not imbalance.
- **Departure ratio (distance rule):** price must travel at least **3× the height of the base** away from it before the zone counts (a $3-tall base needs a ≥$9 move). Some traders accept 2× as a minimum; 3×+ filters out noise.

### Step 2 — Identify the base

- The base is **1–5 candles** of consolidation immediately before the impulse (often just 1–3).
- Base candles have small ranges with overlapping bodies; the base can be a single candle.
- **Shorter time at the base = stronger zone.** Extended sideways consolidation means orders were filled gradually, leaving fewer unfilled orders — the zone is weaker.

### Step 3 — Draw the zone boundaries

Three common conventions (pick one and apply consistently):

1. **Full-base rectangle (most common):** rectangle from the **low to the high of the entire base** (all base candles), extended right until price returns. The video's method is the single-candle version of this (the candle right before the impulse).
2. **Body-to-wick (proximal/distal):** demand zone from the **lowest wick** of the base (distal line) to the **body edge** of the last base candle (proximal line); supply zone mirrored (highest wick to body edge). Tighter zones give better RR but more stop-outs.
3. **Wick-extreme method:** zone spans from the base extreme to the extreme wick of the first impulse candle — used when the impulse overshoots.

Terminology: the **proximal line** is the zone edge closest to current price (top of a demand zone / bottom of a supply zone — where entries go); the **distal line** is the far edge (where stops go).

### Step 4 — Track freshness

- **Fresh** = never revisited since formation → highest probability (most unfilled orders remain).
- **Tested once** = acceptable.
- **Tested 2–3+ times** = orders largely consumed → retire/delete the zone.
- Zones revisited quickly (within ~a week on daily/H4) tend to perform better than zones price takes weeks to return to.
- A zone that price **closes through** (body close beyond the distal line) is broken — remove it (some traders flip it into a "breaker"/inverted zone).

## 4. Zone Quality Score

Rate each zone across these factors before trading it:

| Factor | Strong | Weak |
|--------|--------|------|
| Departure strength | ≥3× base height, big full-bodied candles, small wicks | Small or slow drift away, long wicks |
| Base size | 1–3 candles, tight range | 5+ candles, wide range |
| Freshness | First return (untested) | 2+ previous tests |
| Speed of return | Price returns within days | Price takes weeks/months |
| Confluence | Aligns with HTF S/R, Fib (e.g. 61.8%), round number | Isolated level |

One source claims fresh daily/H4 zones with strong departures hold roughly **65–75%** of the time — this is an unsourced practitioner estimate, not a verified statistic.

## 5. Trade Calculation (entry / stop / target / RR)

- **Entry (aggressive):** limit order at the **proximal edge** — buy limit at the top of the demand zone, sell limit at the bottom of the supply zone. Best RR, but you get filled even if there's no reaction.
- **Entry (conservative):** wait for price to touch the zone and print a rejection candle (pin bar / engulfing) on your execution timeframe; enter after that candle closes. Slightly worse RR, higher selectivity.
- **Stop loss:** just beyond the **distal edge** (a few pips below the demand-zone low / above the supply-zone high).
- **Take profit:** the recent swing high/low (video's method) — better practice is the **next opposing zone** (e.g., long from demand with target at the nearest supply zone above), or a fixed multiple of risk.
- **RR filter:** require ≥ 2.5:1 (video) — many practitioners work with 3:1+.

**Worked example (EUR/USD daily, from research sources):** base consolidates 45 pips between 1.0710–1.0755 for three days, then rallies 180 pips → departure ratio 4:1 → valid demand zone. On retest at 1.0730: buy at 1.0725, stop 1.0700 (25 pips), target next supply at 1.0930 (205 pips) ≈ 8R.

## 6. Algorithmic Detection (for automation)

Scanners/indicators typically qualify a zone using:

- Departure candle **body-to-wick ratio** (imbalance check)
- Departure candle size **relative to ATR** (statistical outlier check)
- **Base width** (number of candles / range tightness)
- Departure distance ≥ **k × base height** (k usually 2–3)
- **Freshness counter** (number of subsequent touches; strength decays per touch)
- Zone strength score = departure speed + base size + freshness, often visualized (fresh zones solid, tested zones faded)

## 7. Common Mistakes

- Drawing zones after *every* consolidation — only mark bases followed by a genuine impulsive departure.
- Trading tested zones as if fresh; keeping dead zones on the chart.
- Making zones too wide (whole consolidation) instead of the tight base.
- Entering without checking RR first (zone can be valid but offer <2.5R to the nearest target).
- Ignoring trend — the video's rule (demand in uptrends, supply in downtrends) is the standard filter; DBR/RBD reversals are the exception at trend turns.

## Sources

- Dukascopy — Supply And Demand Zones: How to Use it in Forex Trading — https://www.dukascopy.com/swiss/english/marketwatch/articles/supply-and-demand-trading/
- JournalPlus glossary — Supply and Demand Zones (departure ratio, freshness, quality score) — https://journalplus.co/learn/glossary/supply-demand-zones
- AlgoMatrix — Fresh vs Tested Supply/Demand Zones (body-to-wick, ATR, base width) — https://algomatrix.trade/blog/fresh-vs-tested-supply-demand-zones
- Proptally — Supply & Demand Zones in Forex (2–3× ATR impulse, base 1–3 candles) — https://learn.proptally.app/forex-price-action-trading/supply-demand-zones-forex
- SignalPro — Supply and Demand Trading Guide (base 1–5 candles, draw base high-to-low) — https://signalpro.markets/supply-and-demand-trading
- EdgeLog — Supply and Demand Trading: A Practical Guide (4:1 worked example, next-zone targets) — https://edgelogtrading.com/blog/supply-demand-trading-strategy
- IC Markets — Supply and Demand: Identify Powerful Reversal Zones (RBR/DBR/DBD/RBD, duration rule) — https://ic.com/blog/how-to-identify-supply-and-demand/
- Complete Traders Edge — Supply and Demand Trading: The Complete Guide (quality factors, S/R vs S/D) — https://completetradersedge.com/supply-and-demand-trading-complete-guide
- NexusFi — Supply and Demand Zones in Futures Trading (order-flow mechanism, test-count depletion) — https://nexusfi.com/a/market-structure/supply-demand-zones-futures-trading
- Tradeciety — 6 Secret Tips For Supply And Demand Trading (DBR/DBD diagrams, freshness, amateur squeeze) — https://tradeciety.com/the-6-golden-rules-of-trading-supply-and-demand
- LitFX — Supply and Demand Trading Strategy (limit vs confirmation entries, trend filter) — https://litfx.app/learn/supply-and-demand-trading-strategy

---

## Full Video Transcript

*Auto-generated captions from YouTube.*

```
0:00 I have a 3 step formula that I've backtested 1000s of times
0:03 And every single month that I tested it, it was profitable in the long term.
0:07 No indicators, no patterns, just pure price action baby.
0:18 And by the end of this video, you too will know this strategy.
0:21 And will be able to take calculated trades just like this one and make insane amounts of money.
0:28 To jump right into it, the first step involves market structure.
0:31 Now, this is arguably one of the most important steps.
0:34 Because if you even slightly fk this part up. It will ruin the whole strategy.
0:38 *meme*
0:43 One of the very first things you learn as a trader is uptrends and downtrends. Its almost the sippy cup of trading.
0:48 A chart that makes higher highs and higher lows is an uptrend.
0:51 A chart that makes lower lows and lower highs is a downtrend.
0:54 Simple enough. Everybody know this. Now you may be thinking.
0:57 Why are we even going over this? I already know all of this.
0:59 Well, what if I told you, you're probably doing all of this completely wrong?
1:03 Let me explain. So going back to our example.
1:05 The chart does this, making higher highs and higher lows.
1:08 And as we already stated, its an uptrend. Okay..
1:13 But then something interesting happens. The chart starts heading downwards.
1:16 Which in the process, price makes this low, and breaks right through it.
1:20 And this exact point, is where I see the majority of traders make the mistake.
1:23 Since price broke this low, a lot of traders think we are now in a reversal and price is in a downtrend.
1:27 So they start looking for short trades because they now think price is going to head lower.
1:32 But what if I told you this chart is actually still fundamentally bullish.
1:38 *crowd gasp*
1:38 You see, sure price made this low.
1:40 But this low is actually not a low at all, or at least a valid one.
1:44 Why? Because price never broke the valid low which is right here.
1:47 *switch up*
1:47 You see, the only way you can get a valid low is by breaking the previous high.
1:48 If price did something like this, where price didn't break the previous high. This would not be a valid low.
1:49 I want to make this clear. In order for a low to be validated. It needs to break the previous high.
1:53 If you do not understand this part of the strategy. The strategy will not work.
2:02 So say if price does breaks this high, we now know this is the valid low. Okay good.
2:08 So now price is in an uptrend. Which means, we should only look for bullish trades.
2:12 The only time we should start looking for short trades is if price breaks this low.
2:16 It can do anything right here. It can go up, down, sideways.
2:19 Literally anything as long as it doesn't break this low. We are in an uptrend.
2:23 So if price did this. What are we in?
2:23 Well a lot of people would say downtrend, because we broke this low right here.
2:23 But like I said before, a low is only validated if it breaks the previous high.
2:23 Which this low did not break the previous high. So its not validated.
2:23 So we are still looking at our previous low. Which price hasn't broke, so we are still in an uptrend.
2:25 Now say if instead of doing this, price did end up breaking upwards.
2:28 Since price did break our previous high. Our new low will be transferred from this point, to this one.
2:32 I know it can be slightly confusing. But the main thing you have to remember
2:32 is the only way a low is validated is if it breaks the previous high.
2:32 If you remember that one simple rule, you will easily be able to identify if we are bullish trend or a bearish one.
2:34 So that's the first step. Identifying if we are in an uptrend or a downtrend. So whats next?
2:37 That would be step 2 in the formula.
2:37 Step 2 is identifying supply and demand in the markets.
2:41 Demand zones take place in uptrends. Supply zones take place in downtrends.
2:44 A good style of thinking is you want to buy from demand zones and sell from supply zones.
2:49 The reason why you want to buy from demand zones is this.
2:51 Here if we look closely. The market is going up.
2:54 Since we saw a large push from the beginning of this move.
2:56 It simply shows us that a lot people wanted to buy from this point onwards.
3:01 So we can assume, if price comes back down to this area.
3:04 Traders will have the same style of thinking and want to buy in this same area again.
3:11 A supply zone is the exact opposite.
3:14 Since we saw a large downwards move from this point on.
3:17 It shows us that a lot people want to sell at this area.
3:20 So if price ever retests this zone we can assume price will again move downwards from this point.
3:26 This supply and demand theory is the core of our strategy.
3:28 But we still have one more step in our 3 step formula.
3:32 But lets put all that we learned so far to the test on a real life chart example.
4:30 So looking at a real chart. We see price moved upwards
4:33 Came down, and then broke this previous high. Which means we have higher highs and higher lows.
4:38 Meaning we are in an uptrend.
4:41 Since we are in an uptrend. We only look for long trades.
4:41 WE DO NOT look for any sell positions.
4:45 As shorting in a uptrend is just silly. *meme*
4:48 Since this low broke the previous high, this is our valid low and price will only be in a downtrend if it breaks this point.
4:53 So now that we know we are in an uptrend, we want to look for demand zone opportunities.
4:57 We can find our demand zones by finding an area of consolidation or a point where price moved sideways before having a sharp move upwards.
5:02 As you can see from this chart we had some consolidation right here. The price shot straight upwards.
5:07 How I like to mark my demand zones is marking the candle right before the impulse move.
5:15 So grab your rectangle tool on the side.
5:19 Find the area of consolidation before the big move.
5:22 Then mark from the low to the high of the previous candle before the big move.
5:27 This is our area of demand.
5:27 Again, we are not even considering areas of supply because we are in an uptrend.
5:31 So we don't need to worry about that.
5:37 We wait for price to re-enter into this zone and this is where we would enter.
5:41 Set your stop loss right below the demand zone and set your take profit at the recent highs.
5:46 Boom we got an easy trade.
5:46 So that's an example of one winning trade.
5:51 But I want to show you just how accurate this strategy really is.
5:54 So lets break it down with a real chart example.
5:54 Here we get an uptrend, because price is making higher highs and higher lows.
5:59 As we can this low is what broke the previous high.
6:03 So, this is where price need to break in order to be in a downtrend.
6:05 Which is exactly what happens.
6:10 So now we are in a downtrend and we only look for areas of supply or short trades.
6:15 So we mark our areas of supply.
6:15 Price comes back up this area of supply. We enter.
6:20 Set our stop loss above the area of supply. And set our take profit at the recent lows.
6:25 Boom easy winning trade
6:25 But wait! we're not done
6:29 Price created another area of supply up here and we're still in a downtrend.
6:33 So we wait for price to come up to this supply. Enter.
6:36 Set our stop loss above the area of supply and target recent lows.
6:40 Another winning trade.
6:40 But again, we're still not done.
6:43 Price created another area of supply. Wait for price to come up to it.
6:47 Set stop loss above the area of supply. Set take profit at recent lows.
6:51 And again we got another winning trade.
6:51 But wait theres more
6:54 We got ANOTHER area of supply. Wait for price to come up here again.
6:58 Set you stop loss and take profit.
6:58 And we got another winning trade.
7:02 That's the power of this strategy.
7:02 Its extremely accurate for one.
7:05 And two, you are only trading in the direction of the trend.
7:08 Which raises the probability of you winning a trade by a lot.
7:11 So now that you know just how powerful this strategy really is.
7:15 Lets go to the third and final step on how to improve this strategy even more.
7:15 Our last step involves risk to reward.
7:19 Sometimes while using this strategy, you'll get a trade that checks all of the boxes.
7:23 But when you setup your stop loss and take profit. Its has a low risk to reward like in this example.
7:28 We only want to take trades if the risk to reward is above 2.5:1
7:32 Mean for every $250 we're getting back we're only risking $100.
7:37 So even if the chart follows both step 1 and 2.
7:43 But the risk to reward is under 2.5. We do not take this trade.
7:47 This one rule increases the profit rate of the strategy by a ton.
7:52 So for our final example we have price making higher highs and higher lows.
7:56 Meaning we are in an uptrend so we only mark our areas of demand.
7:59 Price consolidated right here before shooting upwards. So we mark this area.
8:04 We wait for to come to this area again. Enter.
8:08 Set our stop loss below the demand zone. Set our take profit at the recent high.
8:13 Last step is to check our risk to reward and make sure its over 2.5.
8:17 Which in this example its 3. So we're good to go there.
8:20 If its anything under 2.5, we do not take the trade.
8:23 Wait for price to play out and we get a beautiful winning trade.
8:27 Then we just repeat the process. Forever.
```