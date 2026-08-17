# AGENTS.md

Guidance for AI coding agents (Claude Code, Copilot, Cursor, etc.) working in this repository.

## Project Overview

PodsDx is a Flutter app (Windows/macOS/Linux/iOS/Android) that reads AirPods battery telemetry over BLE using the reverse-engineered Apple Accessory Protocol (AAP), estimates real capacity degradation, and generates health reports.

## Tech Stack

- **Language/Framework:** Flutter (Dart), stable channel
- **BLE:** `flutter_blue_plus` package
- **PDF/report generation:** `pdf` + `printing` packages
- **State management:** keep simple (Provider or Riverpod) — avoid over-engineering early

## Code Conventions

- Follow standard `dart format` and `flutter analyze` output cleanly before committing.
- Keep BLE/AAP protocol parsing isolated in `lib/ble/` — do not mix UI code with protocol code.
- Keep capacity-estimation math isolated in `lib/capacity_estimator/`, unit-tested independently of BLE/UI layers.
- Prefer small, single-purpose files over large multi-responsibility files.

## Build & Test Commands

```
flutter pub get
flutter analyze
flutter test
flutter run
```

## Workflow for Agents

1. Propose a package/module structure before writing implementation code for any new feature.
2. Write the module, then run `flutter analyze` and `flutter test` before considering the task done.
3. Do not invent AAP protocol fields — reference `docs/prd.md` and the LibrePods project's public documentation for confirmed protocol behavior. Flag any assumption explicitly in code comments if a field's exact behavior wasn't found in a public reference.
4. Keep commits scoped to one module/feature at a time.

## Out of Scope (for now)

- No cloud backend / accounts — this is a local, offline-first tool.
- No monetization/licensing logic yet — MIT license applies to the whole repo until otherwise decided.
