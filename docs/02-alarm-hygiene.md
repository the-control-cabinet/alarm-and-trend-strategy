# 02 Alarm hygiene

[← Back to README](../README.md)

| Technique | Rule | Why |
|---|---|---|
| **On-delay** | Every analogue alarm needs a duration (e.g. pressure < 1.0 bar **for 10 min**) | Ignore transients |
| **Deadband / hysteresis** | Clear at a different value from the trip (e.g. trip < 1.0, clear > 1.1 bar) | Stop chattering |
| **Parent suppression** | If a board is offline, suppress its sensor alarms and raise **one** "board offline" alarm | Prevent floods |
| **Mode suppression** | E.g. no "cylinder cold" alarm while hot water is scheduled off | Context-aware |
| **Shelving** | A manual shelve with an **expiry** (max 24 h), logged | Silence known issues without losing them |
| **Nuisance review** | Monthly: the top 10 most frequent alarms, each fixed, retuned or justified | Alarm counts trend down |

**Lesson already learned:** Zigbee availability tracking generated false "offline" alarms and was replaced by event-based detection ([Zigbee repo](https://github.com/the-control-cabinet/zigbee-network-migration-z2m)), a real nuisance-alarm fix.
