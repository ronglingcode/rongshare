# VWAP Continuation Short

## Setup Summary

This is a short continuation pattern where:

- key level > VWAP > open/current price

The key level is usually a news level, after-hours low, prior daily level, or another higher-timeframe level that already failed before the open.

The idea is not to blindly short a stock just because it is below VWAP. The idea is:

- the stock already lost an important level
- VWAP is now acting as dynamic resistance
- trapped buyers or weak holders are likely to keep exiting
- the best short is usually a continuation entry after a small pop, pause, or failed reclaim below VWAP

## Core Idea

This pattern is best when the stock selection is already strongly bearish, and VWAP is confirming that the intraday auction agrees with the higher-timeframe thesis.

Examples:

- earnings miss with price already below after-hours low
- previous day had a large green candle and those buyers are now trapped
- stock gaps below prior support and cannot reclaim it

For high-confidence stock selection such as earnings plus trapped buyers, the expectation is often that the stock should move about `0.9 ATR` to `1.0 ATR` before making its first meaningful reversal, unless the setup fails first.

## Market Context

This pattern works best when:

- the stock is a `gap_down_and_go_down` or similar short-bias day
- premarket stayed below VWAP or lost VWAP before the open
- there is room below to the next real support
- the stock is not already too close to a major downside target at the moment of entry

## Key Reference Levels

Define these before entry:

1. main key level
   - news level
   - after-hours low
   - prior support
   - daily level
2. VWAP
3. high of day
4. last pop high before entry
5. opening range high
6. premarket low
7. next daily / premarket / CAM support targets
8. ATR value

## A+ Conditions

- Big room below current price after the key level already failed
- High-confidence stock selection such as earnings miss plus trapped buyers
- Premarket stayed below VWAP into the open
- VWAP was touched before entry and then rejected
- Another closer higher-timeframe level is aligned near price, so risk can be defined more tightly

## Lower-Quality Conditions

- Price is already too far below VWAP and too close to support, so reward is compressed
- There is no clear opening volume yet
- There is no nearby failed pop or failed reclaim to define risk
- Broad market is squeezing hard while the stock is not making new lows

## Entry Criteria

Use one of these entry ideas.

### 1. Red-to-red / low-of-day breakdown

- Short below large volume dots or below the opening low
- Best when the opening breakdown happens after real volume comes in

### 2. Small pop then next breakdown

- Open is near below a key level
- Price makes a small pop
- Short the next breakdown such as:
  - green-to-red under `60` seconds
  - ORB breakdown
  - pop back toward VWAP

### 3. Bounce toward VWAP then first new low

- Price moves toward VWAP
- It fails to reclaim
- Short the next local breakdown

### 4. Accelerated entry beyond reversal level

- The reversal level fails quickly
- Momentum expands
- Short the breakdown through the failure

### 5. VWAP reclaim failure

- Price closes above VWAP briefly
- The reclaim fails
- Short back below VWAP

## Entry Filters

If the stock is already far below the main key level, prefer continuation entries closer to VWAP or after a small pop. These can be:

- a temporary green candle in the first `60` seconds
- a break of high of day that is still below VWAP
- a green close that sets up first new low or ORB breakdown
- a touch of VWAP followed by:
  - new low
  - close back below VWAP

If price is near below the key level, an ORB breakdown is also acceptable when the second candle makes a mini pop. Use the ORB high or last pop high to define the tight stop.

## Pre-Entry Confirmation Modifier

The management rules are not fully static. Entry quality changes how much confidence you should have after entry.

### Plain Continuation Entry

This is a normal below-VWAP continuation short:

- price is below VWAP
- you short the breakdown
- but price did not first touch VWAP and fail there

This is still valid, but it deserves less management confidence than a confirmed VWAP rejection.

### Confirmed VWAP Retest Rejection Entry

This is a stronger version:

- after the open, price touches VWAP
- it cannot accept above VWAP
- it rolls back down
- you enter short on the next breakdown such as ORB breakdown or first new low

Definition:

- touching VWAP means price actually tags VWAP
- no buffer is allowed
- getting close to VWAP does **not** count as a confirmed VWAP test
- if price only gets near VWAP and rolls over, treat that as a normal continuation entry, not a confirmed VWAP retest rejection entry

This matters because your entry is no longer just "below VWAP." It is now:

- VWAP tested
- VWAP rejected
- continuation confirmed

For management, treat this as one confidence level stronger than a plain continuation entry.

Management consequences:

- while price stays below VWAP and below the pre-entry retest high, do not full-cover just because of a sub-VWAP pop
- the first warning signal usually means `trim / tighten`, not `full exit`
- for A+ names, lean more strongly toward the full minimum hold distance
- if price later squeezes, the pre-entry retest high becomes an important reference level

## Invalidation Criteria

There are 3 states: valid, warning, and failed.

### Valid State

- Price stays below VWAP
- Pullbacks remain weak
- The stock continues to make new lows or lower highs

### Warning State

The setup is still alive, but the clean continuation behavior is weakening.

Warning signals:

1. first `1-minute` close above VWAP
2. strong sub-VWAP squeeze that breaks the last pop high
3. two failed attempts to make a new low
4. three `1-minute` higher lows after entry with no new low
5. `1-minute` moving average golden cross after the opening breakdown
6. strong bid absorption at low of day / premarket low and downside stalls

What warning state means:

- no new short entries
- no adds
- tighten management
- consider trimming size

If the trade had a confirmed VWAP retest rejection before entry:

- a sub-VWAP pop is a weaker warning than usual
- as long as price stays below both VWAP and the pre-entry retest high, bias should still be to stay with the trade

### Failed State

The clean VWAP continuation short is over. Full cover is allowed.

Failed state signals:

1. chosen hard stop is hit
   - high of day
   - last pop high
   - anchor high
   - another pre-defined structural stop
2. two consecutive `1-minute` closes above VWAP
3. key level is reclaimed and held
4. price closes above VWAP, holds there, and then makes a new high from that reclaim

If this happens, the trade is no longer a clean VWAP continuation short. It may transition to another pattern, but this specific pattern is done.

## Risk and Stop Logic

Use one stop model before entry. Do not mix them after you are in the trade.

### Default Stop

- high of day

### Tight Stop

- high of the last pop before entry
- high of the anchor volume dot

### Wider Sizing Stop

If the main key level is still far above price, you can calculate shares using the key level as the theoretical risk level, but still execute with a tighter structural stop such as high of day. That means actual initial risk starts at less than `1R`.

## Trade Management

The goal is to make trade management mechanical enough to code while still preserving the real trading logic:

- hold while the continuation thesis is still valid
- reduce size when warning appears
- fully exit only when the trade has actually failed, or after enough favorable excursion and then clear deterioration
- manage A+ names more patiently than standard names
- manage confirmed VWAP-touch rejection entries more patiently than plain below-VWAP breakdowns

### 1. Required Inputs Before Entry

These fields should be defined before the bot starts managing the trade:

1. `entry_price`
2. `atr`
3. `stock_quality`
   - `A_PLUS`
   - `STANDARD`
   - `LOWER`
4. `entry_confirmation`
   - `PLAIN_CONTINUATION`
   - `VWAP_TOUCH_REJECTION`
5. `hard_stop_mode`
   - `HIGH_OF_DAY`
   - `LAST_POP_HIGH`
   - `ANCHOR_HIGH`
   - `CUSTOM`
6. `hard_stop_price`
7. `key_level_price`
   - can be null if not used in this trade
8. `entry_pop_high`
   - the most recent structural pop high used to define the breakdown
9. `pre_entry_retest_high`
   - required only for `VWAP_TOUCH_REJECTION`
10. `planned_targets`
   - ordered list of support / target prices below entry
   - can be empty

### 2. Derived Values

These values should be computed immediately after entry.

#### Minimum hold distance

This is the minimum favorable excursion expected before a discretionary full exit is normally allowed for non-failure reasons.

- `A_PLUS`: `0.9 * atr`
- `STANDARD`: `0.5 * atr`
- `LOWER`: `0.3 * atr`

#### Mini full-out distance

This is the minimum favorable excursion needed before a full reduced-profit exit is allowed just because momentum weakens.

- `mini_full_out_distance = 0.35 * atr`

#### Default partial distances when there is no target list

- `A_PLUS`: `0.35 ATR`, `0.6 ATR`, `0.9 ATR`
- `STANDARD`: `0.35 ATR`, `0.5 ATR`
- `LOWER`: `0.3 ATR`, `0.5 ATR`

#### Runtime values

These should update on every bar or event.

1. `lowest_price_since_entry`
2. `favorable_excursion = entry_price - lowest_price_since_entry`
3. `current_profit = entry_price - current_price`
4. `profit_giveback_pct = (favorable_excursion - current_profit) / favorable_excursion`
   - only when `favorable_excursion > 0`
5. `minimum_hold_reached = favorable_excursion >= minimum_hold_distance`
6. `mini_full_out_reached = favorable_excursion >= mini_full_out_distance`
7. `below_vwap = current_price < current_vwap`
8. `warning_sequence_active`
9. `warning_count_since_last_new_low`
10. `last_pop_high`
   - initialize with `entry_pop_high`
   - update only when a new valid bounce / pop structure forms

### 3. Management Confidence Modifier

The management rules are not static. Entry quality changes how patient the management should be.

#### Plain continuation entry

- `entry_confirmation = PLAIN_CONTINUATION`
- Price was below VWAP and you shorted the breakdown
- Price did **not** first touch VWAP and reject there

Management bias:

- normal patience
- first warning can justify a small trim

#### Confirmed VWAP-touch rejection entry

- `entry_confirmation = VWAP_TOUCH_REJECTION`
- Price touched VWAP before entry
- It failed there
- You entered on the next breakdown

Management bias:

- higher patience
- while price stays below VWAP and below `pre_entry_retest_high`, the first warning should usually **not** trigger a full exit
- for A+ names, this should bias management more strongly toward the full minimum hold distance

### 4. State Machine

There are 3 states: `VALID`, `WARNING`, and `FAILED`.

#### VALID state

Conditions:

- price is below VWAP
- price has not hit hard stop
- the trade is still making new lows or holding lower-high structure

Default action:

- stay in the trade
- allow planned partials
- allow adds only if there is a fresh trigger and no active warning sequence

#### WARNING state

The trade is still alive, but the continuation is less clean.

Use these core mechanical warning signals for bot v1:

1. first `1-minute` close above VWAP
2. price trades above `last_pop_high` while still below VWAP
3. for `VWAP_TOUCH_REJECTION` entries, price trades above `pre_entry_retest_high` while still below VWAP
4. three consecutive `1-minute` higher lows with no fresh low since entry
5. after a meaningful move, `profit_giveback_pct >= 0.50` and there is still no fresh low

State behavior:

- no new adds
- tighten stop
- consider trim
- do not automatically full-cover

#### FAILED state

The VWAP continuation short is no longer valid as a continuation short.

Use these core mechanical failed signals for bot v1:

1. `current_price >= hard_stop_price`
2. two consecutive `1-minute` closes above VWAP
3. one `1-minute` close above VWAP, and then the next bar makes a higher high and does not close back below VWAP
4. if `key_level_price` is defined: two consecutive `1-minute` closes above key level after reclaim

Default action:

- full cover remaining position
- disable adds
- require a completely new entry trigger for any new short

### 5. Warning Reset Rule

The warning sequence resets only when both are true:

1. price makes a fresh low after the warning started
2. price is back below VWAP cleanly

If this reset happens:

- `warning_count_since_last_new_low = 0`
- management returns to `VALID`

### 6. Tightening Rule

When warning appears, tighten the active stop to the lowest of these valid short-stop references:

1. current active stop
2. warning candle high
3. last pop high
4. for `VWAP_TOUCH_REJECTION` entries, `pre_entry_retest_high`

Important:

- tightening can only move the stop closer, never farther
- once in warning state, no new adds are allowed until warning resets

### 7. Reduced-Loss Exit Rules

Reduced-loss exit means:

- short is covered at a price above entry
- trade did not hit the full hard stop

#### Full reduced-loss cover is allowed only when

1. trade enters `FAILED` state
2. there are 2 warning signals in sequence with no new low reset, and price still cannot make a fresh low
3. first close above VWAP is followed by higher high / higher low behavior instead of immediate rejection

#### Partial reduced-loss trim is allowed when

1. first warning appears before `mini_full_out_distance`
2. trade is still below VWAP, but behavior has become abnormal

Default trim size:

- `PLAIN_CONTINUATION`: trim `25%`
- `VWAP_TOUCH_REJECTION`: trim `0%` on first warning if still below VWAP and below `pre_entry_retest_high`
- `VWAP_TOUCH_REJECTION`: trim `25%` on second warning without reset

Hard rule:

- before `mini_full_out_distance`, do **not** fully cover just because price pops and feels uncomfortable
- before `minimum_hold_distance`, do **not** fully cover an `A_PLUS` trade unless it reaches `FAILED` state or repeated warning escalation

### 8. Reduced-Profit Exit Rules

Reduced-profit exit means:

- short is still green
- you are exiting because the move weakened before the ideal final target

#### Full reduced-profit cover is allowed only when

1. `mini_full_out_distance` has been reached, and then 2 warning signals appear without reset
2. a planned support target is hit, and price bounces aggressively from that target
3. `profit_giveback_pct >= 0.50` after a meaningful move, and there is still no fresh low
4. warning appears after a meaningful move, and the next push down fails to make a new low

#### Additional rule for A+ names

If `stock_quality = A_PLUS`:

- do not fully cover the whole trade before `minimum_hold_distance`
- exception:
  - `FAILED` state
  - repeated warning escalation with no reset
  - a planned major target is hit and price reacts strongly there

This is the rule that protects trades like NKE from shaking out too early.

### 9. Partial Profit Rules

Use planned targets first. ATR-only targets are fallback rules.

#### Target priority

1. daily support
2. premarket low
3. after-hours levels
4. CAM pivots
5. large Bookmap levels

#### If planned targets exist

Use this default scale-out logic:

1. first target hit: cover `25%`
2. second target hit: cover `25%`
3. third target hit: cover `25%`
4. keep last `25%` as runner until warning-based exit or failed state

#### If no planned targets exist

Use ATR fallback logic:

- `A_PLUS`
  - `25%` at `0.35 ATR`
  - `25%` at `0.6 ATR`
  - `25%` at `0.9 ATR`
  - last `25%` runner
- `STANDARD`
  - `33%` at `0.35 ATR`
  - `33%` at `0.5 ATR`
  - last `34%` runner
- `LOWER`
  - `50%` at `0.3 ATR`
  - `50%` at `0.5 ATR`

### 10. Add Rules

Adds are allowed only when all are true:

1. current state is `VALID`
2. price is below VWAP
3. warning sequence is not active
4. there is a fresh trigger

Allowed fresh triggers:

1. premarket low breakdown with room below
2. VWAP rejection and back below VWAP
3. weak bounce into broken level and next breakdown

Adds are not allowed when:

- state is `WARNING` or `FAILED`
- trade was just trimmed because of warning and has not reset
- price is only moving in your favor without a new trigger

### 11. Bot Evaluation Order

For implementation, evaluate management in this order on each bar:

1. update runtime values
2. update `lowest_price_since_entry`
3. check `FAILED` state first
   - if failed: full cover and stop
4. check whether warning reset happened
5. detect new warning signals
6. update `warning_count_since_last_new_low`
7. process partial profit targets
8. process reduced-loss trim rules
9. process reduced-profit full-exit rules
10. process add eligibility

### 12. Classification of Any Exit

Every exit should be labeled for review and for bot logging:

1. `HARD_STOP_FAILURE`
2. `FAILED_STATE_EXIT`
3. `REDUCED_LOSS_TRIM`
4. `REDUCED_LOSS_FULL_EXIT`
5. `PLANNED_PARTIAL`
6. `REDUCED_PROFIT_FULL_EXIT`
7. `RUNNER_EXIT`

That labeling matters because later review should separate:

- trade failed
- trade was trimmed because of warning
- trade worked but was exited early for reduced profit

## Exit Logic Summary

### Early full cover for reduced loss

Allowed only when:

- failed state
- repeated warning escalation with no fresh new low
- or first close above VWAP leads to higher-high continuation instead of immediate rejection

### Early full cover for reduced profit

Allowed when:

- mini full-out distance has been reached
- or the trade already reached the planned support target
- and warning / reversal behavior appears
- for `A_PLUS` names, avoid full reduced-profit exit before `minimum_hold_distance` unless warning escalation is repeated or a major target was already hit

### Stay in trend

If price is still below VWAP and still making lower highs / new lows, the trade is still valid. A pop below VWAP by itself is not enough reason to fully exit.

If VWAP was already tested and rejected before your entry, this rule becomes even stronger. In that case, a later sub-VWAP pop should usually be treated as pressure, not failure, unless it also breaks the pre-entry retest high or escalates into failed state.

## Common Failure Modes

- panic-covering below VWAP even though the invalidation has not happened
- FOMO re-entry at a worse price after covering
- mixing VWAP invalidation with high-of-day invalidation mid-trade
- taking full exits before the minimum hold distance on A+ stock selection
- adding during warning state

## Review Checklist

1. Was stock selection truly A+, standard, or lower quality?
2. What was the chosen hard stop before entry?
3. What was the minimum hold distance before entry?
4. Did the trade reach mini full-out distance?
5. Were exits reduced-loss or reduced-profit exits?
6. Did each exit happen because of:
   - warning
   - failed state
   - target hit
   - emotional discomfort
7. Did I cover because the setup changed, or because I felt pressure?
8. Did I re-enter without a fresh trigger?

## Notes

- This pattern file is mainly for trade management and entry refinement.
- The exact ATR thresholds should be reviewed against past trades and adjusted if needed.
- When this pattern is used inside a future `gap_down_and_go_down` tradebook, keep these management states consistent with that parent tradebook.
