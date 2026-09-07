# Changelog — mh_tools Astrophotography Weather Widget

All notable changes to the standalone Weather Widget. Format based on
[Keep a Changelog](https://keepachangelog.com/).
Licensed under **CC BY-NC-ND 4.0** — © 2026 Martin P. Heigan.

## [2.0.0] — 2026-09-06

Full rebuild on **Python 3.13 / PySide6 (Qt6)**, ported from PyQt6. This is the
same application that ships inside the mh_astro_tools Suite v2.0.0; the
standalone ZIP remains available for anyone who wants only the Widget.

### Added
- **Now also included in the mh_astro_tools Suite**, alongside the Exposure
  Calculator, UTC / GPS / Weather, 500 Rule Calculator, Night Vision Overlay and
  Scientific Calculator, all opened from a common Launcher. The application is
  identical in both; only the distribution differs.
- **User manual.** The v1 builds shipped without one. A standalone-specific
  manual is included in the ZIP and covers extraction, launching, verification
  and troubleshooting.
- Bundled `tzdata`, so local-time resolution is correct on Windows without any
  additional download.
- Signed `release_manifest.cat` and `SHA256SUMS.txt` in the distribution folder,
  so every file can be verified after extraction.

### Changed
- Ported from PyQt6 to **PySide6**, on the shared suite night-vision design.
- Settings moved to a per-user location under your Documents folder. Legacy
  locations are read as a fallback, so existing preferences migrate on first
  launch.
- Native WinRT geolocation is now optional, with IP-based lookup as the
  fallback when it is unavailable or declined.
- Distribution folder renamed to `mh_astro_weather_widget_v2_0_0` and the
  executable to `mh_astro_weather_widget_Win_x64_v2_0_0.exe`. There is no
  separate launcher EXE — the application starts directly.

### Removed
- **The full-screen black startup mask.** Startup now relies on the frameless
  window and a per-widget fade instead of covering the whole desktop. The
  night-vision benefit is retained without the side effects the full-screen
  mask caused with capture software and multi-monitor setups.

### Fixed
- A latent crash in the no-location branch (undefined `ts_str`).
- About-box copyright corrected to © 2026.

### Notes
- The units toggle introduced in v1.1.0.3 is retained: Metric (default) or
  Imperial (°F / inHg / mph).
- Upgrading from v1.x: delete the old extracted folder. The two versions use
  different folder and executable names, so they will not overwrite each other,
  and running both at once is not supported.

---

## [1.1.0.3]

- Added Metric / Imperial unit toggles (remembered preference; default Metric).
- Imperial uses US-style units: °F, inHg, mph.
- Settings layout refined (added an Options header).
- Retained full-screen startup black mask to prevent Windows launch flashes and
  preserve night vision.

## [1.1.0.0] — 2026-02-03

- Added Sunrise / Sunset display (offline, based on configured location).
- Added Moonrise / Moonset display (offline, based on configured location).
- Improved window drag reliability and kept the Arrow cursor (no pointing-hand
  cursor).

## [1.0.0.12] — 2026-02-03

- Fixed a refresh issue that could make the UI feel unresponsive (weather fetch
  now uses async Qt networking).
- Improved tray Show / Hide robustness (closes any popup or grab state before
  toggling visibility).
- Maintains the full-screen black night-vision shield startup behaviour.

## [1.0.0.8]

- First ZIP distribution using a launcher EXE.
- Added full-screen black startup shield to eliminate Windows launch flashes in
  the field.
- Close button quits; minimise hides to tray.
