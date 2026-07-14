# RogueFetch — Releases

Public distribution point for compiled **RogueFetch** releases, by [Rogue Gain](https://roguegain.com).

**Download, convert, and organize media.**

> **This repository contains release binaries and licence/source material only.**
> RogueFetch's application source code is **not** published here.

**→ [Get the latest release](https://github.com/Chaos-dwg/RogueFetch-Releases/releases/latest)**

---

## What RogueFetch is

RogueFetch is a Windows desktop utility from Rogue Gain that downloads, converts, and
organizes supported online media using a clear local interface. Paste a link, check
what it found, choose an output, and let the queue run — no command line, and no
separate FFmpeg install.

- **Audio:** MP3, WAV, FLAC, M4A, Opus, AAC — with selectable bitrate
- **Video:** MP4, MKV, WebM
- Metadata preview, download queue, live progress, history, and a native Save As for
  every download
- **FFmpeg is bundled** — it is never taken from your PATH

## Requirements

- **Windows 10 or 11 (64-bit)**
- **Python is not required.** FFmpeg ships with the application.

## Downloads

| | |
|---|---|
| **Installer** (recommended) | `RogueFetch-1.0.2-Setup.exe` — per-user install, no admin rights, Start Menu shortcut, clean uninstall |
| **Portable** | `RogueFetch-1.0.2-portable-win64.zip` — unzip anywhere and run `RogueFetch.exe` |
| **Checksums** | `RogueFetch-1.0.2-SHA256SUMS.txt` |

Upgrading from MediaGrabber? The installer removes the old installation for you, and
your settings and history are carried across on first run.

## Code signing

**These builds are unsigned.**

Windows SmartScreen may therefore warn you the first time you run the installer, and
some antivirus products flag PyInstaller-packaged applications. This is a consequence
of the build not carrying a code-signing certificate, not an indication that anything
is wrong with it.

Because the builds are unsigned, **verifying the checksum is the meaningful integrity
check.** Do it:

```powershell
Get-FileHash .\RogueFetch-1.0.2-Setup.exe -Algorithm SHA256
```

Compare the result against `RogueFetch-1.0.2-SHA256SUMS.txt`. If it does not match, do
not run the file.

## Bundled FFmpeg, and its source

RogueFetch bundles **FFmpeg** under the **LGPL v3**. It executes `ffmpeg.exe` as a
separate process and links no FFmpeg library into itself.

| | |
|---|---|
| Build | `ffmpeg-n7.1.5-2-g998de74adf-win64-lgpl-shared-7.1` |
| Upstream | FFmpeg `release/7.1`, commit [`998de74adf`](https://github.com/FFmpeg/FFmpeg/commit/998de74adf861c26df557e220996faa959419549) |
| Licence | LGPL-3.0-or-later — see [FFmpeg-LICENSE-LGPLv3.txt](FFmpeg-LICENSE-LGPLv3.txt) |
| Builder | [BtbN/FFmpeg-Builds](https://github.com/BtbN/FFmpeg-Builds), pinned to release tag `autobuild-2026-07-13-14-11` |
| Archive SHA-256 | `6e3fcd3c40e4f66806d5249fe784eaf3a789f1f2d4859662a2b8c05d8fd624fc` |

This is an **LGPL** build: configured *without* `--enable-gpl`, so the GPL-only
components (libx264, libx265, libxvid and others) are disabled. The FFmpeg libraries
ship as **separate DLLs**, so you can replace them with your own compatible build by
swapping the files in the `bin` folder — no relinking of RogueFetch is required.

**Corresponding source is published with every release** that ships these binaries:

- `ffmpeg-source-998de74adf.tar.gz` — the exact FFmpeg source
- `ffmpeg-build-scripts-BtbN-autobuild-2026-07-13-14-11.tar.gz` — the build scripts and configuration

Full details, including the exact `./configure` line, are in
[FFMPEG_BUILD_INFO.txt](FFMPEG_BUILD_INFO.txt).

## Licensing

RogueFetch is released under the **MIT License** — see [LICENSE](LICENSE).

Third-party components are listed in [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt).
The full FFmpeg LGPL v3 text is in [FFmpeg-LICENSE-LGPLv3.txt](FFmpeg-LICENSE-LGPLv3.txt),
and the bundled build's provenance and source information are in
[FFMPEG_BUILD_INFO.txt](FFMPEG_BUILD_INFO.txt). The same material ships inside both
packages.

## Release history

**v1.0.2 — Current release**

RogueFetch v1.0.2 updates the product identity and includes the current FFmpeg
distribution, licensing materials, source information, and checksums.

**Earlier releases — Superseded**

Earlier MediaGrabber-branded packages have been superseded. Use the current RogueFetch
release.

## Responsible use

RogueFetch is intended **only** for media you own, have permission to download, or are
otherwise legally authorized to save. You are responsible for complying with copyright
law and with the terms of the services you access.

RogueFetch does not bypass access controls and does not support DRM-protected streams.
Sign-in-required, region-locked, or bot-blocked content cannot be circumvented.

## Links

- **Product page:** <https://roguegain.com/products/roguefetch/>
- **Rogue Gain:** <https://roguegain.com>
- **Issues and support:** <https://roguegain.com/contact/>
