# Contributing to PodsDx

Thanks for your interest in contributing! Here's how to get started.

## Getting Started

1. Fork the repo and clone your fork.
2. Run `flutter pub get` to install dependencies.
3. Run `flutter analyze` and `flutter test` before opening a PR — CI will check both.
4. Create a feature branch: `git checkout -b feature/your-feature-name`.

## Code Style

- Format with `dart format .` before committing.
- Keep BLE/protocol logic in `lib/ble/`, capacity math in `lib/capacity_estimator/`, and UI separate from both.
- Small, single-purpose files and commits are strongly preferred over large ones.

## Submitting Changes

1. Open a PR against `main` using the PR template.
2. Describe what changed and why — link any related issue.
3. Be responsive to review feedback; we aim to review PRs within a few days.

## Reporting Bugs / Requesting Features

Use the issue templates under "New Issue" — they'll prompt you for the info that helps us triage faster.

## Questions

Open a [Discussion](../../discussions) or an issue tagged `question`.
