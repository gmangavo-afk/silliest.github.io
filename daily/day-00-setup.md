# Day 0 — Setup / Pre-Launch (2026-07-16)

## Challenge parameters
- **Goal:** Grow ~$100 into as much as possible over 30 market days.
- **Rule:** At least one real trade every day the U.S. market is open.
- **Account:** Robinhood "Agentic" cash account (••••6771) — the ONLY account this connector is authorized to trade (`agentic_allowed: true`). All other accounts on the login return `agentic_allowed: false` and are off-limits to this agent.
- **Instrument scope:** Cash account with no options level → **equities only** (no options, no margin).

## Hard risk rails (locked)
1. Minimum 1 real trade per market day. Never fabricate a trade or report a simulation as real.
2. Max 50% of account value in a single position unless overridden in writing for that day.
3. Always state the dollar downside before entering.
4. If a position is down hard, decide deliberately to cut or hold — no autopilot.

## Live account snapshot (2026-07-16)
Pulled via connector:
- Total value: **$0.00**
- Cash: **$0.00**
- Buying power: **$0.00**
- Equity positions: none
- Option positions: none

## Blocker to launch
The Agentic account (••••6771) is **empty**. The ~$100 stake must be deposited/transferred into this specific account before Day 1 can run. Funds sitting in the default margin account or any other account are NOT tradable by this connector.

## Next step
Once ••••6771 shows ~$100 in buying power, say **"run day 1"**. On Day 1 I will:
1. Confirm the U.S. market is open.
2. Pull the live account and set the true starting value.
3. Research the day's catalysts.
4. Write a thesis (ticker, entry, target, stop, size, $ downside).
5. Simulate/review the order, confirm affordable, then hand it to you to submit.
6. Verify the fill, update `positions.md`, append to `ledger.csv`, and write `daily/day-01.md`.
