# Astrophotography Weather Widget — v2.0.0

A compact **night-vision-friendly** desktop widget for astrophotography field
use. It shows the observing-relevant weather at a glance, without opening a
browser, and lives in the system tray rather than the taskbar.

© 2026 Martin P. Heigan · [anti-matter-3d.com](https://anti-matter-3d.com) ·
licensed under 
[CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/)

## Also available in the Suite

This tool is now included in the **mh_astro_tools Suite v2.0.0**, alongside the
Exposure Calculator, UTC / GPS / Weather, 500 Rule Calculator, Night Vision
Overlay and Scientific Calculator, all opened from a common Launcher.

**The application is identical in both.** Only the distribution differs:


|        |Standalone ZIP                        |Suite installer                                    |
|--------|--------------------------------------|---------------------------------------------------|
|Contents|The Weather Widget alone              |All seven tools plus the Launcher                  |
|Install |Extract and run                       |Windows installer, Start Menu and Desktop shortcuts|
|Best for|Just this tool, or no installer wanted|The complete astrophotography toolset              |

Do not run both copies at once — they are the same application and will compete
for the same settings.

## Download


[mh_astro_weather_widget_v2_0_0.zip](https://github.com/MHeigan/mh_Astro_Weather_Widget/releases)
— GitHub releases

Also listed on the [Tools page](https://anti-matter-3d.com/tools/) at
anti-matter-3d.com, together with the full mh_astro_tools Suite installer.

## What it shows

- Temperature and dew point, with the temperature-to-dew-point spread
- Condensation-risk label derived from that spread — EXTREME / HIGH / MED / LOW
- Wind speed
- Barometric pressure with a trend arrow
- Sky condition (WMO weather text)
- **Units toggle** — Metric (default) or Imperial (°F / inHg / mph)

## What's new in v2.0.0

Full rebuild on **Python 3.13 / PySide6 (Qt6)**, ported from PyQt6, on the shared
suite night-vision design. The full-desktop black startup mask is gone —
startup now uses the frameless window and a per-widget fade. Settings moved to
a per-user location under your Documents folder, with legacy locations read as
a fallback so existing preferences migrate. Bundled `tzdata` for correct
local-time handling on Windows. A user manual is included for the first time.
See `CHANGELOG.md` for the full list.

## Installation

Extract the archive anywhere you can write to and run the executable. **No Python
or runtime is required** — everything is bundled.

1.  Right-click `mh_astro_weather_widget_v2_0_0.zip` → **Extract All…**
2.  **Keep the extracted folder structure intact** — the application loads its
    icons, Qt libraries and timezone data from subfolders beside the executable
3.  Double-click `mh_astro_weather_widget_Win_x64_v2_0_0.exe`

Upgrading from v1.x: delete the old extracted folder first. The two versions
use different folder and executable names, so they will not overwrite each
other.

To uninstall, delete the extracted folder. Nothing is added to the registry
except the optional run-at-startup entry, which is removed by clearing that
setting before you delete the folder.

## System requirements


|                |                                                                   |
|----------------|-------------------------------------------------------------------|
|Operating system|Windows 10 / 11, 64-bit                                            |
|Internet        |Required for weather data; astronomical values are computed offline|
|Runtime         |None — Python and all libraries are bundled                        |

## Documentation

`Astrophotography_Weather_Widget_User_Manual.pdf` is included in the archive and
covers installation, the HUD and tray, displayed fields and units, running at
startup, dew risk, and troubleshooting.

## Security

The executable is code-signed by Certum with SHA-256 Authenticode and an
RFC-3161 timestamp, and is submitted to Microsoft WDSI and VirusTotal before
release. The archive contains a signed `release_manifest.cat` and a `
SHA256SUMS.txt` covering every file, and the archive's own SHA-256 is published
with the release. Verify the Authenticode signature and the published SHA-256
if in doubt.

## Links

- Releases — <https://github.com/MHeigan/mh_Astro_Weather_Widget/releases>
- Tools & updates — <https://anti-matter-3d.com/tools/>
