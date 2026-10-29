# 01 Alarm philosophy

[← Back to README](../README.md)

## Priorities
| Priority | Meaning | Examples | Route | Response |
|---|---|---|---|---|
| **P1 Life safety / property** | Act now | Fire/CO interface fault, water on floor, tundish discharge, burst flow | Critical phone alert (bypasses silent mode) + dashboard | Immediately |
| **P2 Plant fault** | Act today | Boiler pressure < 1.0 bar, cylinder inlet > 5.0 bar, boiler fault code, steady low flow 10 min | Phone push + dashboard | Same day |
| **P3 Degraded** | Act this week | Proxy offline > 10 min, supervisor heartbeat missed, sensor stale, battery low | Dashboard + daily digest | This week |
| **P4 Advisory** | Review | Pressure decay above baseline, rising overnight water use, boiler cycles above target | Weekly review | Monthly |

## Rules
- **Every alarm has an owner** (the repo or system it belongs to) and a **written response**.
- **Acknowledgement:** P1/P2 need acknowledging; unacknowledged P2 re-alerts after 2 h.
- **Escalation:** unacknowledged P1 escalates to a second person after 5 min ⟨decide⟩.
- **Return to normal** is logged, so every alarm has a start, an acknowledgement and an end.
