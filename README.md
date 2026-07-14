# MediaGrabber — Releases

Public distribution point for compiled **MediaGrabber** releases, by [Rogue Gain](https://roguegain.com).

> **This repository contains release binaries only.**
> MediaGrabber's application source code is **not** published here.

**→ [Get the latest release](https://github.com/Chaos-dwg/MediaGrabber-Releases/releases/latest)**

---

## What MediaGrabber is

A Windows desktop application for authorized media retrieval and conversion. Paste a
link, check what it found, choose an output, and let the queue run — no command line,
and no separate FFmpeg install.

- **Audio:** MP3, WAV, FLAC, M4A, Opus, AAC — with selectable bitrate
- **Video:** MP4, MKV, WebM — up to 4K
- Metadata preview, download queue, live progress, history, and a native Save As for
  every download
- **FFmpeg is bundled** — it is never taken from your PATH

## Requirements

- **Windows 10 or 11 (64-bit)**
- **Python is not required.** FFmpeg ships with the application.

## Downloads

| | |
|---|---|
| **Installer** (recommended) | `MediaGrabber-1.0.0-Setup.exe` — per-user install, no admin rights, Start Menu shortcut, clean uninstall |
| **Portable** | `MediaGrabber-1.0.0-portable-win64.zip` — unzip anywhere and run `MediaGrabber.exe` |
| **Checksums** | `SHA256SUMS.txt` |

## Code signing

**These builds are unsigned.**

Windows SmartScreen may therefore warn you the first time you run the installer, and
some antivirus products flag PyInstaller-packaged applications. This is a consequence
of the build not carrying a code-signing certificate, not an indication that anything
is wrong with it.

Because the builds are unsigned, **verifying the checksum is the meaningful integrity
check.** Do it.

## Verify your download

Compare the hash of the file you downloaded against the value in `SHA256SUMS.txt`:

```powershell
Get-FileHash .\MediaGrabber-1.0.0-Setup.exe -Algorithm SHA256
```

If the hash does not match, do not run the file.

## Responsible use

MediaGrabber is intended **only** for media you own, have permission to download, or
are otherwise legally authorized to save. You are responsible for complying with
copyright law and with the terms of the services you access.

MediaGrabber does not bypass access controls and does not support DRM-protected
streams. Sign-in-required, region-locked, or bot-blocked content cannot be
circumvented.

## Licensing

MediaGrabber itself is MIT-licensed. The bundled FFmpeg is a GPL build.

## Links

- **Product page:** <https://roguegain.com/products/mediagrabber/>
- **Rogue Gain:** <https://roguegain.com>
- **Issues and support:** <https://roguegain.com/contact/>
