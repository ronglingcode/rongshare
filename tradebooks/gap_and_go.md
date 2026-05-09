# Gap and Go

## Overview

Gap and Go is a **long continuation setup** where a stock gaps up into favorable conditions with room to run higher, ideally with minimal early selling pressure so the move can continue after the open. We are following large players placing bullish trades, and the gap signals their positioning. If the setup holds, momentum funds may chase the breakout.

## Stock Selection

Use the shared stock selection rules in [`tradebooks/shared/stock-selection.md`](shared/stock-selection.md).
For the daily tradebook decision process, use [`tradebooks/shared/tradebook-decision.md`](shared/tradebook-decision.md). In summary, the main reasons for this tradebook being applicable can be one of:
1. The stock was doing consolidation and formed an obvious consolidation range before today's gap up.
2. There are large open space above such as all time high gap up.
3. It breakout a level from previous key event.

Here's the more detailed stock selection requirements for this gap and go tradebook.
### Uptrend from Higher Timeframe

On the daily chart, it needs to be one of the following cases:

1. Stock in an uptrend
2. Stock in a downtrend but recently has shown change of character from the bottom
   - Higher low base formed
3. The entire market was selling off, this stock is showing relative strength such as it will drop less or just consolidating.

Basically the daily chart needs to show large institutions have been buying this stock and that it is possible they will continue buying today.

### Consolidation Before the Gap

- Daily chart was doing consolidation or a minor pullback before today's gap
  - If it is already too extended to the upside, it becomes a Gap Give and Go setup
- Today's gap is above the consolidation range high or near its high

### Light Resistance Above

- No major resistance from current price
- Light zone above with minimal supply
- No heavy supply zones created by 10+ days or a deep downtrend

### Gap Path Matters
Pay attention to not only where the stock opens that creates the gap, also the entire path that it travelled since the news is released. We prefer to see the gap up has a smaller pullback like less 20%. If a stock gapped up 5 ATR and pulled back 4 ATR to open, although it's still 1 ATR gap up, maybe even near above a consolidation range on the daily chart, this is however not a good gap and go for long because it probably hit some major resistance at the 5 ATR gap and sellers already took control and took it down 4 ATR. That will be a more of bearish open dispite the gap up.

## Key Level Selection Priority
After the stock is considered for gap and go, we pick a level as key level. When price is above both the key and vwap, we look for long the breakouts that's above the key level and vwap. If price fall below key level, it's not allowed for long. If price fall below vwap, it's one case for gap give and go. 

There are multiple options for choose which level to be the key leve. Here's the order.

### P1: Level from Higher Timeframe
The first priority is to choose a level on the daily chart. 
- If there's a clean consolidation range on the daily chart, and the range has an obvious top edge, then that top edge is the level to use as key level.
- All time high is always a key level from the daily chart

### P2: Previous News Level
There have been a previous news and that previous news created an extreme high/low price. That price hasn't been broken out yet. 

### P3: Intraday Level
- Default is the news levels. For after hour news, it's after hours high/low. For morning news, it's premarket high/low.
- R6 cam pivots. That's because it's the last cam pivot, beyond that, it opens for more room.

For stocks with morning news, there are a few cases when using premarket high breakout is not a good idea, like it's probably too extended to long after premarket high breakout. If it actually ran to some supply zone on the daily chart during premarket and created such premarket high, then this premarket high is more likely to be entry for short sellers. For premarket high breakout to be a good long setup, it needs to have open space beyond premarket high.

## Entry Model: Bookmap Big Offer Wall Breakout
Given the key level we choose, we find the nearest large limit sell orders wall from the bookmap that's above the key level and vwap, and we trade the breakout of that wall. There are two ways for this breakout, they are documented in 
* [Big Offer Clear, Pullback, Go](./bookmap_patterns/big_offer_clear_pullback_go.md)
* [Big Offer Clear, Bids Hold Above](./bookmap_patterns/big_offer_clear_bids_hold_above.md)

### [Deprecated] Other candlesticks patterns
I used to trade candlesticks breakout pattern before I used bookmap, but I feel candlesticks patterns are very noisy and they don't demonstrate my core trading principle of following the large players. So right now in this gap and go tradebook, I don't want to include any candlesticks happens. Those candlesticks pattern can still occur with success, but they always comes with the bookmap patterns as well. So I can just trade the bookmap patterns. 

## Stop Loss

If stop loss is breached, momentum from that breakout is lost. This level breakout is not clean anymore. Once we lost the swing low of the bookmap wall breakout, there are only 2 conditions when we can take the next long:
#### 1. high of day breakout
Sometimes I set the stop loss to be too tight, it steal my stop and go back up. To avoid chop between my intial tight stop loss and high of day, we can only long the next gap and go breakout at the high of day breakout.

#### 2. transition to the [gap give and go](./gap_give_and_go.md) tradebook
If the stock didn't make a new high of day, it will probably go down to some support lower to find more buyers to make the next rally. This gap give and go can be ready after a retest to vwap or the key level. It has to touch the level or vwap. More details will be explained in the gap give and go tradebook.

## Trade Management
Follow the [3-tier trade management](./shared/3-tier-live-trade-management.md)
### Profit Targets
Common profit targets are in the order of
1. other levels from higher timeframe (daily chart)
2. levels from intraday charts: cam pivots, premarket high/low, previous day high/low, after hour high/low.
3. other big walls from bookmap

Use the above for setting core targets and runner targets. 

### Core Tier
Watch out for the following `Reversal / Invalidation Signal`
* higher timeframe new low
  * 9:40: 5-minute new low, 15-minute new low
* Vwap bounce fail
  * if it tested vwap before the entry, vwap hold can be a great condition to manage the trade
* 2 consecutive 1-minute candle close below a key level
  * if it tested the key level before the entry or break out a major key level after open, the hold of this level can be a great condition to manage the trade
* [Big Offer Wall Reappear](./bookmap_patterns/big_offer_wall_reappear.md) or [Sellers Step Down](./bookmap_patterns/sellers_step_down.md)
  * if there's a offer wall that has the larger size than our entry wall, this can be a great condition to manage the trade


### Runner Tier
Runner tier should first have its `Trigger Condition`. It's usually a major level for another breakout, it can also be the final target for the core tier, such as
* all time high
* high from a previous key event
* premarket high/after-hours high 

When price approaches core targets, it's ok to partial the core tire while holding the runner tier. If seeing strong signal of core targets holding, all out on both core and runner tier. If price easiy go beyond targets or made a mini consolidation and breakout, move the stop loss of the runner to the consolidation edge and hold it to the final runner target. 

## Add
This section is not fully done. To keep things simple, only allow add when add entry is above premarket high. If we started with a partial R risk, we can add into 1 R.

## Participation Thesis

Gap-and-Go is better understood as a **participation-dependent continuation strategy**, not just a one-minute breakout pattern.

When you buy a breakout at 9:32 AM, you are not trading the shape of the candle itself. You are participating in the continuation of **unfinished higher timeframe positioning**. In other words, you are stepping into a move that may have already begun days, or even weeks, earlier as larger institutions accumulate shares over time.

In a strong uptrend, when a stock is making higher highs or approaching all-time highs, capital is often still flowing into that name. Institutions may be building positions, momentum funds may be allocating, and systematic buyers may be scaling exposure. In this environment, an early-morning breakout is frequently not an isolated intraday event, but the next visible step in an ongoing parent order.

This is why Gap-and-Go setups tend to work best when a stock is:

- Trending above rising daily moving averages
- Breaking recent resistance or entering price discovery
- Near or above all-time highs
- Supported by an intact bullish narrative

In these conditions, pullbacks are more likely to be absorbed, VWAP often acts as support, and opening range breakouts can transition smoothly into continuation patterns such as five-minute bull flags. The breakout works not because of its visual appearance, but because **someone with size still needs to buy more**.

### When Participation Disappears

The same setup begins to fail when the participation regime changes.

Consider a stock that has already been trending down for several weeks, having lost key moving averages, broken prior support levels, and formed a series of lower highs. In many cases, the institutions that once drove the trend are no longer active buyers. Their participation has already occurred, and in some cases, distribution has already taken place.

What remains intraday is a different ecosystem, dominated by:

- Market makers
- Day traders
- Short-term swing traders
- Mean reversion algorithms

A breakout that occurs at 9:33 AM in this type of environment is no longer supported by institutional accumulation. Instead, it may represent a short-term liquidity event, a moment where local participants are trading against one another without meaningful directional intent from higher timeframe players.

Price may briefly push above the opening range, fill breakout orders, and then reverse once the immediate pool of aggressive buyers is exhausted. Without fresh capital flowing into the name, the move lacks follow-through and tends to mean revert toward VWAP.

To the discretionary trader, this often manifests as the stock "feeling dead" intraday. Volume may appear normal, but the quality of participation has changed:

- In an inflow phase, volume reflects accumulation
- In a post-distribution phase, volume reflects inventory rotation

The prints may look the same on a time-and-sales window, but their underlying intent is fundamentally different.

### Implications for Gap-and-Go Traders

The effectiveness of breakout-based strategies depends heavily on the presence of ongoing higher timeframe demand. Gap-and-Go works best when:

- Funds are still building positions
- Capital continues flowing into the stock
- The broader trend remains intact

It becomes less reliable when:

- Positioning has already been unwound
- Price is trading below declining moving averages
- The stock is inside prior value or beneath overhead supply

In these latter conditions, the opening auction becomes less about imbalance resolution and more about price discovery within a range. Continuation trades lose effectiveness, and setups that rely on identifying trapped participants, such as VWAP Bounce-Fail patterns, may offer a more reliable path to intraday profitability.

Understanding Gap-and-Go as a participation strategy, rather than a visual pattern, allows the trader to recognize when the setup is supported by active institutional demand, and when it is being applied in an environment that no longer supports its underlying premise.

## Live Execution Sheet

- Key level: `__________`
- Entry wall: `__________`
- Stop: `__________`
- Scalp target: `__________`
- Core target: `__________`
- Runner trigger condition: `__________`
- Size split: scalp `____%` / core `____%` / runner `____%`

