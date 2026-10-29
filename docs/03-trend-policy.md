# 03 Trend policy

[← Back to README](../README.md)

| Point class | Examples | Logging | Retention |
|---|---|---|---|
| Plant analogue | Flow/return temps, pressures, currents | On change with a deadband (0.2 °C, 0.02 bar, 0.05 A) + every 5 min | 10 days in HA; **long-term** in InfluxDB ⟨planned⟩ |
| Plant digital | Demands, boiler states, flame | On change | Same |
| Zone | Room temp, setpoint, heat demand | On change | Same |
| Energy and water | Meters, costs | Totals + statistics | Long-term statistics (permanent) |
| High-churn | BLE RSSI/distance, device lists | **Excluded** from the recorder | n/a |

**Rules:** no point is logged without a purpose; high-churn entities are excluded by glob; long-term storage is for M&V (before/after reports).
