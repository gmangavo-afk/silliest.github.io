# Positions — 30-Day Trading Challenge

**Trading account:** Robinhood "Agentic" cash account (••••6771) — the only account this connector can trade.
**Account type:** Cash account, no options level → **equities only**.
**True starting stake:** $9.13 (funded 2026-07-16). _Challenge tracks % vs this $9.13, not $100 — the account only ever held ~$9._

_Last refreshed: 2026-07-16, post-market (Day 1 close)_

## Account snapshot

| Field | Value |
|---|---|
| Total account value | **$9.10** |
| Cash / buying power | **$5.45** |
| Equity value | $3.65 |
| Cumulative return vs $9.13 | **-0.33%** |

## Open positions

| Ticker | Qty | Avg cost | Last mark | Mkt value | Unrealized | Thesis / plan |
|---|---|---|---|---|---|---|
| BTG (B2Gold) | 1 | $3.68 | $3.65 | $3.65 | -$0.03 | Gold safe-haven vs geopolitical risk-off. Target ~$3.90 (+6%), mental stop ~$3.50 (-5%). Managed manually — no auto-stop. |

## Automation (set up 2026-07-16)
- **Routine:** "30-Day Trading Challenge — Daily 9:30 ET" (`trig_01JohMT6u1ZBgFMqGgtYSAkq`), cron `30 13 * * 1-5` (13:30 UTC = 9:30 AM ET, Mon–Fri; first fire 2026-07-17 ~9:37 AM ET).
- **Mode:** self-bind (fires into the original session so it keeps the Robinhood + GitHub connectors). Fully autonomous — places real trades without per-trade confirmation, always respecting the hard risk rails (50% cap, dollar-downside stated, equities only).
- Holidays/weekends are self-checked by the run (cron covers Mon–Fri; the run skips U.S. market holidays and stops).
- Challenge auto-ends after 30 logged market days; the Routine deletes itself.

## Notes / mechanics
- **Cash account settlement:** proceeds from selling BTG won't be immediately re-tradable same-day (unsettled funds). To trade every market day I'll rotate/hold overnight and keep the $5.45 cash slice as dry powder.
- **After-hours constraint (recurring):** if a day's run happens after 4:00 PM ET, only whole-share limit orders execute, capped by price ≤ affordable buying power.
