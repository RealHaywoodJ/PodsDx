# PodsDx

**Cross-platform AirPods battery health & capacity-degradation diagnostic tool.**

PodsDx reads real battery telemetry from AirPods (via the reverse-engineered Apple Accessory Protocol, AAP) and estimates true capacity degradation — not just charge percentage — to help users and repair shops make data-backed decisions about battery replacement.

## Why PodsDx?

Existing AirPods companion tools (LibrePods, OpenPods, capod, MagicPods) surface live battery *percentage*. None of them estimate actual *capacity degradation* over time, which is the number that actually matters when deciding whether a battery needs replacing. PodsDx fills that gap.

## Platforms

Built with [Flutter](https://flutter.dev) for a single codebase across:
- Windows
- macOS
- Linux
- iOS
- Android

## Status

🚧 Early scaffold — core BLE/AAP reading engine and capacity estimation logic in progress.

## How It Works (Planned)

1. **BLE Reader** — connects to AirPods over Bluetooth LE and polls AAP battery status fields (left bud, right bud, case).
2. **Capacity Estimator** — logs voltage/charge behavior across full discharge-charge cycles to estimate true capacity vs. rated mAh.
3. **Report Generator** — produces a shareable health report (PDF) suitable for customers or repair-shop documentation.

## License

MIT — see [LICENSE](LICENSE).

## Contributing

Contributions welcome. See [AGENTS.md](AGENTS.md) for project conventions if you're using an AI coding agent, and [docs/prd.md](docs/prd.md) for the full product spec.

## Credits

Built by SirSHAmun5on12. Protocol groundwork made possible by the prior reverse-engineering work of the [LibrePods](https://github.com/librepods-org/librepods) project.
