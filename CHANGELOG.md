# Changelog

Format based on [Keep a Changelog](https://keepachangelog.com/). This file starts
from the F2000Alt work below — earlier releases aren't retroactively documented here.

## [3.5.2] - 2026-07-20

### Added

- Light bar mode select entity for F2000Alt (Off/Low/Medium/High/SOS), backed by
  the underlying library's `set_light_mode()`/`light`. Previously this control
  existed at the library level with no HA entity exposing it.

## [3.5.1] - 2026-07-20

### Added

- F2000Alt device model support (alternate-protocol 767 PowerHouse) — sensors and
  switches for AC Output, DC Output, and Power Saving Mode.

### Fixed

- The Power Saving Mode switch now reports real device state instead of being
  optimistic-only, using the status readback SolixBLEF2000 added for this.
