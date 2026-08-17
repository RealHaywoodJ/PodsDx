# PodsDx — Product Requirements (Draft)

## Problem

AirPods and their case use lithium batteries whose charge controllers drift out of calibration over time. Existing tools report live state-of-charge (%) but not actual capacity degradation, so users and repair shops have no data-backed way to decide if/when a battery needs replacing.

## Goal

Build a free, cross-platform tool that:
1. Reads real battery telemetry (left bud, right bud, case) via BLE/AAP.
2. Estimates true capacity vs. rated capacity by tracking behavior across full charge/discharge cycles.
3. Produces a clear, shareable report a user or repair shop can act on.

## Non-Goals (v1)

- Not a full AirPods feature-replication tool (that's what LibrePods/MagicPods already do).
- No cloud sync, accounts, or telemetry collection from users.
- No support for forcing/controlling charging behavior (not physically possible via software — see project research notes).

## Core Features (v1)

- BLE scan + pair to AirPods, read AAP battery fields periodically.
- Log battery readings locally (SQLite or flat file) across a full cycle.
- Compute capacity estimate from logged data.
- Generate a PDF report summarizing findings.

## Open Questions

- Exact AAP field offsets for case-battery vs. bud-battery reporting — validate against LibrePods' public protocol notes before implementing.
- Minimum viable cycle-logging duration needed for a stable capacity estimate.
- Report format/branding — keep neutral/professional for repair-shop use.
