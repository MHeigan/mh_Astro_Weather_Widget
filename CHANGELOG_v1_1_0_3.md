# Changelog — mh_tools Astro Weather Widget

## v1.1.0.3
- Added Metric / Imperial unit toggles (remembered preference; default Metric).
- Imperial uses US-style units: °F, inHg, mph.
- Settings layout refined (added an Options header).
- Retained full-screen startup black mask to prevent Windows launch flashes and preserve night vision.

## v1.1.0.0 â€” 2026-02-03

- Added Sunrise/Sunset display (offline, based on configured location).
- Added Moonrise/Moonset display (offline, based on configured location).
- Improved window drag reliability and kept Arrow cursor (no pointing-hand cursor).

## v1.0.0.12 â€” 2026-02-03
- Fixed a refresh issue that could make the UI feel unresponsive (weather fetch now uses async Qt networking).
- Improved tray Show/Hide robustness (closes any popup/grab state before toggling visibility).
- Maintains the full-screen black â€œnight-vision shieldâ€ startup behaviour.

## v1.0.0.8
- First Zip distribution using a launcher EXE.
- Added full-screen black startup shield to eliminate Windows launch flashes in the field.
- Close button quits; minimize hides to tray.

