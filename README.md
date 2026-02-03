# mh_astro_weather_widget (mh_Astro_Weather_Widget)

A small, night-vision friendly desktop weather widget for field use (astronomy / astrophotography).

## 🚀 Installation (ZIP Distribution)

This tool is distributed as a ZIP:

- **mh_Astro_Weather_Widget.zip**

### Steps

1. **Extract** the ZIP to a folder of your choice (important — do **not** run from inside the ZIP).
2. Launch the widget by double-clicking:

   - **mh_Astro_Weather_Widget_Launcher.exe**

### Folder layout (expected)

```
mh_Astro_Weather_Widget/
  mh_Astro_Weather_Widget_Launcher.exe
  mh_astro_weather_widget_Win_x64_v1.0.0.8/
    mh_astro_weather_widget_Win_x64_v1.0.0.8.exe
    (support files…)
  manuals/
    mh_astro_weather_widget_user_manual.pdf
    README.md
    README.txt
    License_Agreement.pdf
```

### Night-vision “blank screen” on launch (intentional)

You may briefly see a **full-screen black screen** at startup. This is intentional:
it blocks **Windows launch flashes** and helps preserve **night vision / dark adaptation** when used in the field.

## Quick Start

1. Double-click **mh_Astro_Weather_Widget_Launcher.exe**.
2. Click **Menu** → **Settings** and confirm **Auto-detect coordinates** is enabled (or enter coordinates manually).
3. Click **↻ Refresh** to pull weather data immediately.
4. Drag the widget by the **title bar** (not the buttons).
5. **Minimize (-)** hides to the **system tray**. **Close (x)** quits the widget.

## System Tray Menu

Right-click the tray icon for a small menu:
- Restore
- Refresh Now
- Quit

## File Locations / Config

The widget saves a JSON config next to the **widget executable** (inside the widget folder):

- `mh_astro_weather_widget_config.json`

Note: the launcher sits **one folder above** the widget EXE. The config stays with the widget so the widget remains self-contained.

## Troubleshooting

- **No weather data / wrong location**  
  Enable Windows Location Services or enter coordinates manually. If needed, enable **IP fallback** for approximate coordinates.

- **Black screen appears briefly on launch**  
  Expected behavior — it’s a night-vision preservation mask to prevent Windows launch flashes.

## Developer Notes (optional)

You can still run from source (for development):
- Python 3.8–3.12
- `pip install requests` (and any other project requirements you use)

## Change Log

- **v1.0.0.8**
  - ZIP distribution (**mh_Astro_Weather_Widget.zip**) with launcher + Nuitka onedir widget build.
  - Full-screen black startup mask to prevent Windows launch flashes and preserve night vision.
  - Position memory + night-mode tray popup menu.
  - Standard window behavior: **-** minimizes to tray, **x** quits.
