<div align="center">

# PodsDx

**Cross-platform AirPods battery health & capacity-degradation diagnostic tool.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![Made with Flutter](https://img.shields.io/badge/Made%20with-Flutter-02569B.svg?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](CONTRIBUTING.md)
[![Status](https://img.shields.io/badge/status-early%20scaffold-orange.svg?style=for-the-badge)]()

![Windows](https://img.shields.io/badge/Windows-0078D6?style=flat-square&logo=windows&logoColor=white)
![macOS](https://img.shields.io/badge/macOS-000000?style=flat-square&logo=apple&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![iOS](https://img.shields.io/badge/iOS-000000?style=flat-square&logo=ios&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=android&logoColor=white)

</div>

---

PodsDx reads real battery telemetry from AirPods (via the reverse-engineered Apple Accessory Protocol, AAP) and estimates true **capacity degradation** — not just charge percentage — to help users and repair shops make data-backed decisions about battery replacement.

## Table of Contents

- [Why PodsDx?](#why-podsdx)
- [Platforms](#platforms)
- [How It Works](#how-it-works-planned)
- [Status](#status)
- [Contributing](#contributing)
- [License](#license)
- [Star History](#star-history)

## Why PodsDx?

Existing AirPods companion tools (LibrePods, OpenPods, capod, MagicPods) surface live battery *percentage*. None of them estimate actual *capacity degradation* over time — the number that actually matters when deciding whether a battery needs replacing. PodsDx fills that gap.

## Platforms

Built with [Flutter](https://flutter.dev) for a single codebase across Windows, macOS, Linux, iOS, and Android.

## How It Works (Planned)

| Stage | Description |
|---|---|
| 🔍 **BLE Reader** | Connects to AirPods over Bluetooth LE and polls AAP battery status fields (left bud, right bud, case) |
| 📊 **Capacity Estimator** | Logs voltage/charge behavior across full discharge-charge cycles to estimate true capacity vs. rated mAh |
| 📄 **Report Generator** | Produces a shareable PDF health report for customers or repair-shop documentation |

## Status

🚧 **Early scaffold** — core BLE/AAP reading engine and capacity estimation logic in progress. See [docs/prd.md](docs/prd.md) for the full spec and roadmap.

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) and our [Code of Conduct](CODE_OF_CONDUCT.md) first. If you're using an AI coding agent, see [AGENTS.md](AGENTS.md) for project conventions.

## Support the Project

If PodsDx is useful to you, consider [sponsoring development](https://github.com/sponsors/RealHaywoodJ) — see the Sponsor button at the top of this repo.

## License

MIT — see [LICENSE](LICENSE).

## Credits

Built by **SirSHAmun5on12**. Protocol groundwork made possible by the prior reverse-engineering work of the [LibrePods](https://github.com/librepods-org/librepods) project.

## Star History

<a href="https://star-history.com/#RealHaywoodJ/PodsDx&Date">
  <img src="https://api.star-history.com/svg?repos=RealHaywoodJ/PodsDx&type=Date" alt="Star History Chart" width="600"/>
</a>
