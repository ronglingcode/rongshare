# Gap and Crap

## Key Characteristics

- Stock gaps up on news.
- Higher timeframe context suggests **profit taking** or **strong overhead supply**.
- Selling pressure is expected to appear **immediately or very early** in the session (first 30 minutes after the open).

## Stock Selection

Use the shared stock selection rules in [`tradebooks/shared/stock-selection.md`](shared/stock-selection.md).
For the daily tradebook decision process, use [`tradebooks/shared/tradebook-decision.md`](shared/tradebook-decision.md).


## Higher Timeframe Conditions (A+ Context)

At least one of the following should be true. More boxes checked = higher quality **Gap and Crap**.

### 1. Accumulated Too Much Profit

There is a lot of unrealized profit for buyers that is suddenly created by this gap. This makes it rational for those winning traders to sell right at the open.

- Prior day: **big trend day up** with no real reason to sell. Traders hold overnight and wake up with even more PnL.
- Prior weeks/months: **steady uptrend** with shallow or no pullbacks. ([example](https://www.notion.so/241d17cd21b380a78216ff7a759df4a5))
- **Earnings gap**: buyers positioned ahead of earnings are heavily rewarded on the open.
- Big gap:
  - Mag7: more than **1 ATR**
  - Others: more than **2 ATR**
  - These are just guidance. 1.9 ATR is not too different from 2 ATR. And if a stock opened with 1.5 ATR gap, and it went up for another 0.5 ATR after market open, that makes it 2 ATR above previous day close price and now it qualifies for 2 ATR gap up short.

### 2. Gap Near Range Top

- The gap **does not cleanly break out** of the main daily range.
- Instead, price opens **very close to the top edge** of the existing range. ([example](https://www.notion.so/2bfd17cd21b380df8cdfc95b4cf3f0bc))

### 3. Gap Into Heavy Supply Zone

- Stock gaps into a **heavy zone / supply area** created by:
  - **10+ days** of prior trading
  - A few days with elevated volume
- Open can be:
  - Inside the zone
  - Or just **below the bottom edge** of the zone
- ([example](https://www.notion.so/2dfd17cd21b3803bb8b2d212e8547932))

## Key Level Selection Priority
After the stock is considered for gap and crap with a given reason, we pick a level as key level. We can only short the stock when the price is below this key leve. It's ok to short it above vwap, it just only a subset of the entry methods are allowed above vwap. The premarket high is also considered a special threadshold. If short entry is above premarket high, use less risk.

The priority is start from higher timeframe to lower timeframe.

### P1: Level from Higher Timeframe Condition
For each category of the daily chart context, we have ways of choosing the key level.

- Accumulated Too Much Profit
  - This is not at any resistance on the daily chart, we use the news high as key level
  - for after hour news, use after hours high
  - for morning news, use premarket high
- Gap Near Range Top
  - Use the top edge of the range as key level
  - once price breakout of the range, we cannot short it any more
- Gap Into Heavy Supply Zone
  - we can either use the top edge of the zone, or use the news high level.

### P2: Previous News Level
There have been a previous news and that previous news created an extreme high/low price. That price hasn't been broken out yet. 

### P3: Intraday Level
- Default is the news levels. For after hour news, it's after hours high/low. For morning news, it's premarket high/low.
- R6 cam pivots. That's because it's the last cam pivot, beyond that, it opens for more room.

After consider all those above, we pick a final level as our key level. It's a bit discretionary of which one to use. We prefer to align more with the higher timeframe.


## News-to-Open Path
Avoid stocks that gapped up and already sold off to a major support level. And sometimes it bounced from there. Open at the middle between news high and news low will be choppy open.

## Entry Patterns
I only tracebook entry pattenrs now. 

### Entry Pattern Category 1: Short the Breakdown
Shorting the breakdown is only allowed when entry is below vwap.
* [Big Bid Clear, Bounce, Drop](./bookmap_patterns/big_bid_clear_bounce_drop.md)
* [Big Bid Clear, Asks Hold Below](./bookmap_patterns/big_bid_clear_asks_hold_below.md)

### Entry Pattern Category 2: Short the Pop Below VWAP
When price is below vwap, we can short the pop using the following 4 bookmap patterns.
* [Big Offer Clear, Fail Back Below, Breakdown Bid](./bookmap_patterns/big_offer_clear_fail_back_below_breakdown_bid.md)
* [Big Offer Clear, Fail Back Below, Breakdown Swing Low](./bookmap_patterns/big_offer_clear_fail_back_below_breakdown_swing_low.md)
* [Offer Reappear](./bookmap_patterns/offer_reappear.md)
* [Offer Step Down](./bookmap_patterns/offer_step_down.md)

### Entry Pattern Category 3: Short the Pop Above VWAP
When price is below vwap, we have short the pop only using the following 2 bookmap patterns of the previous 4 patterns
* [Offer Reappear](./bookmap_patterns/offer_reappear.md)
* [Offer Step Down](./bookmap_patterns/offer_step_down.md)

## Trade Management
Follow the [3-tier trade management](./shared/3-tier-live-trade-management.md)

### Core Tier
A common core targets are: premarket low or gap fill

Watch out for the following `Reversal / Invalidation Signal`
* higher timeframe new high
  * 9:40: 5-minute new high, 15-minute new high
* Vwap reclaim
  * if it tested vwap or crossed vwap before the entry, vwap hold can be a great condition to manage the trade
* 2 consecutive 1-minute candle close below a key level
  * if it tested the key level before the entry or break out a major key level after open, the hold of this level can be a great condition to manage the trade
* [Offer Reappear](./bookmap_patterns/offer_reappear.md) or [Offer Step Down](./bookmap_patterns/offer_step_down.md)
  * if there's a bid wall that has the larger size than our entry wall, this can be a great condition to manage the trade

### Runner Tier
A common runner targets are: 
  - key support on daily chart
  - premarket low or gap fill
  - core tareget to premarket low, then extend to gap fill


## Add
This section is not fully done. To keep things simple, only allow add when entry is below vwap.


## Power Gap and Crap

This is not a new setup. It is the exceptional-quality version of Gap and Crap.

Use this version when both are true:

- gap up is **4 ATR or more**
- premarket volume is **4 million shares or more**

When a stock qualifies as **Power Gap and Crap**, the expectation should be bigger than the normal Gap and Crap target map. The setup is more active than average and can keep moving well past the first obvious downside target.

Important:

- this changes the **target framework**, not the entry rules
- this does **not** give permission for looser entries

Target framework for **Power Gap and Crap**:
1. Allocation more partials for runner tier.
2. Besides the normal runner target, the ultimate runner target can be just hold for the entire day and close the trade just before market close.
3. Consider add back the core tier once the runner triggers and move stop tight
