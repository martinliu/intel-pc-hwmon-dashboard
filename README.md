# Intel PC Server Hardware Monitoring (node-exporter hwmon)

A Prometheus + Grafana dashboard for hardware sensors exposed by `lm-sensors` and `node-exporter`'s `hwmon` collector. The dashboard is designed to be reusable across Intel PC servers (and similar platforms) while keeping labels human-readable and actionable.

[简体中文 README](README.zh-CN.md)

## What this project contains

- `grafana-dashboard.json`: ready-to-import Grafana dashboard.
- `raw-data.md`: reference output of `sensors` and matching `node-exporter` metrics.
- `raw-data.txt`: raw capture used during development.

## Requirements

- Prometheus with `node-exporter`.
- `node-exporter` started with `--collector.hwmon`.
- `lm-sensors` installed and configured so `/sys/class/hwmon` exposes valid data.

## Quick start

1) Install and configure `lm-sensors` on the target host.
2) Run `node-exporter` with the `hwmon` collector enabled.
3) Import `grafana-dashboard.json` into Grafana.
4) Select a Prometheus datasource and choose `job` / `instance`.

## Dashboard overview

The dashboard is organized by rows:

- Overview (CPU temp, uptime, disk, memory, alarm status)
- CPU Thermal (package/core temps, thresholds, critical alarms)
- Motherboard / PCH (board sensors, ACPI zones)
- Fans & PWM (RPM, duty control)
- Voltages (rails and alarms)
- Alerts (active alarms with readable labels)

## Variables

- `DS_PROMETHEUS`: Prometheus datasource.
- `job`: Prometheus job label (supports `All`).
- `instance`: Prometheus instance label (supports `All`).

All panel queries use regex matching (`=~`) to keep compatibility with `All`.

## Compatibility notes

- Chip and sensor names differ across motherboards. This dashboard joins:
  - `node_hwmon_chip_names` for readable chip names.
  - `node_hwmon_sensor_label` for readable sensor labels.
- Some channels are unused or unmapped (e.g., `0.0°C` or `ALARM`). Use Grafana Transform filters to hide invalid series if needed.
- PWM and fan channels may not exist on all systems. Missing series are expected.

## Troubleshooting

- **No data in panels**: check that `node-exporter` exposes `node_hwmon_*` metrics and that `job`/`instance` values exist.
- **Unreadable labels**: verify `node_hwmon_sensor_label` and `node_hwmon_chip_names` are present in your Prometheus target.
- **Unexpected `ALARM`**: often indicates missing thresholds or unused channels. Validate in `sensors` output.

## Contributing

Contributions are welcome. Suggested areas:

- Improve compatibility across more Super I/O chips and platforms.
- Add better filtering or panel transformations for invalid channels.
- Provide screenshots and real-world validation notes.
- Extend documentation for setup on other distros.

Open a PR with your changes and include any relevant hardware details.

## Reference environment

- Intel NUC 6i
- Proxmox VE (PVE)
- `lm-sensors` + `node-exporter` `hwmon` collector
