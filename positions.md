# Positions — 30-Day Trading Challenge

**Trading account:** Robinhood "Agentic" cash account (••••6771) — the only account this connector can trade.
**Account type:** Cash account, no options level → **equities only**.
**True starting stake:** $9.13 (funded 2026-07-16). _Challenge tracks % vs this $9.13, not $100 — the account only ever held ~$9._

_Last refreshed: 2026-07-17, ~11:46 AM ET (Day 2)_

## Account snapshot

| Field | Value |
|---|---|
| Total account value | **$9.10** |
| Cash / buying power | **$1.45** |
| Equity value | $7.65 |
| Cumulative return vs $9.13 | **-0.37%** |

## Open positions

| Ticker | Qty | Avg cost | Last mark | Mkt value | Unrealized | Thesis / plan |
|---|---|---|---|---|---|---|
| BTG (B2Gold) | 1 | $3.68 | $3.65 | $3.65 | -$0.03 | Gold safe-haven. ON NOTICE — miner lagging the metal (gold at record ~$3,983 but BTG down 2 sessions). Cut if it keeps diverging. Target ~$3.90, mental stop ~$3.50. |
| USO (US Oil Fund) | 0.03256 | $122.85 | $122.74 | $4.00 | -$0.00 | Oil momentum on Gulf/Iran tension (USO +3% intraday on a red equity day). Target +3-5%, mental stop ~-5% (~$116.7). |

## Positioning note
- **~84% of the account is one macro bet:** BTG (gold) + USO (oil) both rise on geopolitical escalation and fall on de-escalation. Held over the weekend of Jul 18-19 — weekend headline risk cuts both ways. Deliberate tilt given oil/gold are the only things bid on a risk-off tape.

## Automation
- Routine "30-Day Trading Challenge — Daily 9:30 ET" (`trig_01JohMT6u1ZBgFMqGgtYSAkq`), cron `30 13 * * 1-5`, self-bind, fully autonomous. **User authorized skipping order-approval prompts (2026-07-17)** — runs place trades directly within the risk rails, no confirmation pause.
- Verified working on Day 2: the self-bind resume kept the Robinhood connector (reconnected under a new server ID mid-run).

## Notes / mechanics
- **Cash account settlement:** proceeds from selling are unsettled and not immediately re-tradable same-day; rotate/hold overnight around this.
- **Regular-hours unlock:** fractional + dollar-based market orders work 9:30–16:00 ET (used for the $4 USO buy). After-hours is whole-share limit only.
