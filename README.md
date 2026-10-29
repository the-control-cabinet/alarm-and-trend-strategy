# Alarm and Trend Strategy: One Philosophy Across Every System (Living Document)

**A BMS-style alarm and trend philosophy applied across the whole portfolio: alarm priorities with defined responses, routing and escalation, shelving and suppression, a nuisance-alarm review, and a trend-logging policy (what is logged, how often, how long it's kept). Every other repo raises alarms or logs data; this one makes them consistent, and it's updated as each system goes live.**

[![YouTube](https://img.shields.io/badge/YouTube-The%20Control%20Cabinet-red?logo=youtube)](https://www.youtube.com/channel/UC5Cupmz7vlfcodpCX7k8iuQ)
[![Portfolio](https://img.shields.io/badge/Portfolio-the--control--cabinet-24292f?logo=github)](https://github.com/the-control-cabinet/the-control-cabinet)
![Domain](https://img.shields.io/badge/BMS-alarms%20%26%20trends-blue)
![Status](https://img.shields.io/badge/Status-Living%20document-yellow)

> **The short version:**
> - **Priorities P1-P4**, each with a defined response time and route (phone push, critical alert, dashboard, weekly review).
> - **An alarm register:** every alarm in the house, with its source, condition, delay, priority and owner repo.
> - **Hygiene rules:** delays on every analogue alarm, suppression when the parent system is down (no alarm floods), shelving with expiry, and a monthly nuisance-alarm review.
> - **Trend policy:** sample on change or by interval with deadbands, a retention tier per point class, and long-term storage for M&V.

**Portfolio position:** Management level · alarm and trend strategy (portfolio #6). Feeds from: [plant monitoring](https://github.com/the-control-cabinet/heating-plant-monitoring-esphome) · [leak detection](https://github.com/the-control-cabinet/layered-leak-detection) · [fire/CO interface](https://github.com/the-control-cabinet/aico-ei413-shelly-ha) · [supervisory layer](https://github.com/the-control-cabinet/ha-node-red-supervisory-layer) · [BLE network](https://github.com/the-control-cabinet/esp32-ble-presence-network) · [OpenTherm control](https://github.com/the-control-cabinet/opentherm-boiler-control-esphome)

---

## Documents

| Doc | Contents |
|---|---|
| [01 Alarm philosophy](docs/01-alarm-philosophy.md) | Priorities, responses, routing, escalation, acknowledgement |
| [02 Alarm hygiene](docs/02-alarm-hygiene.md) | Delays, deadbands, suppression, shelving, nuisance review |
| [03 Trend policy](docs/03-trend-policy.md) | What is logged, how often, how long, where |
| [04 Alarm register](docs/04-alarm-register.md) | Every alarm in the estate (living table) |

## Roadmap
- [ ] Alarm register populated from existing automations
- [ ] Priority routing implemented (critical alerts for P1)
- [ ] Parent suppression for every ESP board
- [ ] Monthly nuisance-alarm review started
- [ ] Long-term trend store (InfluxDB) for M&V

## Skills demonstrated (as built)
| Skill | Evidence |
|---|---|
| Alarm philosophy | P1-P4 priorities with responses and escalation |
| Alarm hygiene | Delays, deadbands, suppression, shelving, nuisance review |
| Trend policy | Point classes, deadbands, retention tiers |
| Estate-wide consistency | One register covering every repo |

📺 [The Control Cabinet on YouTube](https://www.youtube.com/channel/UC5Cupmz7vlfcodpCX7k8iuQ)

*Built and documented by James · part of [The Control Cabinet BMS portfolio](https://github.com/the-control-cabinet/the-control-cabinet). MIT Licence.*
