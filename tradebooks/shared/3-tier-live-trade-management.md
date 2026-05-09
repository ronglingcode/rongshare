# 3-Tier Live Trade Management

Shared rule: every trade is managed with 3 tiers.

Each tradebook must define its own:
- reversal / invalidation signals
- runner trigger condition
- runner target

## Before Entry

Define:
- scalp: x%
- core: y%
- runner: z%
- stop
- core main target
- runner trigger condition
- runner target
- reversal / invalidation signals

If these are not defined before entry, reduce size or skip.

## 1. Scalp

Purpose: emotion relief.

Rules:
- can exit anytime
- no strict signal required
- use this tier to reduce pressure, not the core

## 2. Core

Purpose: capture the tradebook thesis.

Default action: hold to the core main target.

Core exits only by:
- stop out
- limit fill at core main target, or slightly before it
- setup-specific reversal / invalidation signal

Actions to take if seeing reversal / invalidation signal
- trim more partials: not sure whether it will get worse, reduce some shares to allow more tolerance.
- fully exit: if seeing a very strong reversal signal.
- adjust stop: if we come to a condition that's going to make it or break it.

## 3. Runner

Purpose: capture extension after the core move.

Runner needs a tradebook-specific trigger condition that says the trade is starting to extend toward the runner target.

Examples:
- Gap and Crap runner may require breakdown below premarket low.
- Gap and Go runner may require holding above breakout level / VWAP after core target.

Runner exits if:
- runner trigger condition fails
- price cannot extend toward the runner target
- setup-specific reversal signal appears
- trailing structure breaks

Example:
If Gap and Crap runner target is 1 ATR below premarket low, but premarket low keeps holding, I can exit the runner instead of waiting for the ATR target.

## Simple Live Rule

Scalp is flexible.
Core follows stop / core target / reversal.
Runner follows trigger condition / runner target / reversal.
