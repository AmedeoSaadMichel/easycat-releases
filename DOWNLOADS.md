# Download easycat

**Cut. Transform. Meow.** Trim, compress and change video containers on your computer. No accounts, uploads or cloud processing.

Preview 6 publishes easycat under MIT, completes the workspace and CLI rename, and includes newly verified native packages.

## Choose your system

| System | Download | Requirements / status |
| --- | --- | --- |
| macOS · Apple Silicon | [Download DMG](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-macos-arm64-legal-preview.dmg) | macOS 15 or later · preview build |
| macOS · Intel | [Download Intel DMG](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-macos-x86_64-legal-preview.dmg) | Intel x86_64 · macOS 15 or later · natively tested preview |
| Windows · x64 | [Download portable ZIP](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-windows-x64-legal-preview.zip) | Windows 10/11 x64 · unsigned preview |
| Linux · x64 | [Download portable tar.gz](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-linux-x86_64-legal-preview.tar.gz) | glibc 2.35+ / Ubuntu 22.04+ · desktop with OpenGL |

[Release details and files](https://github.com/AmedeoSaadMichel/easycat-releases/releases/tag/v0.1.0-preview.6) · [SHA-256 checksum](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/SHA256SUMS) · [Intel SHA-256 checksums](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/SHA256SUMS-INTEL) · [Report a problem](https://github.com/AmedeoSaadMichel/easycat-releases/issues)

Packages are compiled and tested on native CI runners. Windows desktop interaction still needs hands-on validation; Linux startup/rendering is checked under Xvfb. Intel builds are compiled and tested on a native macOS Intel runner. Public downloads and corresponding third-party sources are hosted in a separate distribution repository; the application source is available under [MIT](https://github.com/AmedeoSaadMichel/easycat/blob/main/LICENSE) in [easycat](https://github.com/AmedeoSaadMichel/easycat).

## Install on macOS

1. Download and open the DMG.
2. Drag **easycat** into **Applications**.
3. Open easycat from Applications.

The package includes FFmpeg, ffprobe, ffplay and their required libraries. Homebrew and Rust are not required. Your original videos are never overwritten.

**Preview status:** this build has an ad-hoc signature and is not notarized with Apple. macOS may display a security warning. If you decide to open it, use the normal macOS Privacy & Security controls; do not disable Gatekeeper system-wide. Third-party source and license checks are complete for this preview; this is not a stable release.

### Install with Homebrew

On Apple Silicon or Intel with macOS 15 or later, add the public personal tap once, then install easycat:

```sh
brew tap AmedeoSaadMichel/easycat https://github.com/AmedeoSaadMichel/easycat-releases.git
brew trust --cask amedeosaadmichel/easycat/easycat
brew install --cask easycat
```

The trust command authorizes only the easycat cask, not every package or command in the tap. Recent Homebrew versions require explicit trust for non-official taps or their individual packages. See [Homebrew Tap Trust](https://docs.brew.sh/Tap-Trust).

This installs the same macOS preview and retains the signature limitations above. If you used the previous private tap, run `brew untap AmedeoSaadMichel/easycat` before adding the public tap.

### First launch on macOS (DMG and Homebrew)

This preview has an ad-hoc signature and is not notarized with Apple. Installation can succeed while macOS still requires separate approval at first launch. This applies to both the DMG and Homebrew installations.

1. Open **easycat** from **Applications**.
2. If macOS blocks it because the developer cannot be verified or the app is not notarized, open **System Settings → Privacy & Security**.
3. Find the notice for **easycat**, click **Open Anyway**, then confirm the opening. Authenticate if macOS asks.

If the easycat notice is missing, try opening the app again, then return to Privacy & Security. Do not disable Gatekeeper system-wide. See [Apple's instructions](https://support.apple.com/en-us/102445).

### Homebrew installation troubleshooting

- **No available formula with the name "easycat":** on a new machine, add the personal tap using the commands above. easycat is not listed in the official Homebrew catalog.
- **Unknown command: brew --cask:** use `brew install --cask easycat`; `--cask` belongs after `install`.
- **Refusing to load cask from untrusted tap:** run `brew trust --cask amedeosaadmichel/easycat/easycat`, then retry the installation.
- **Warnings about other taps**, such as `gromgit/fuse`, `oven-sh/bun` or `wickenico/wailbrew`, are unrelated to easycat. You do not need to trust those taps to install easycat.

The message `easycat was successfully installed!` confirms installation. macOS first-launch approval is a separate step.

## Install on Windows

1. Download the portable ZIP and extract the entire archive.
2. Open the extracted folder and run **easycat.exe**.
3. Keep **Helpers** beside the executable; it contains the FFmpeg tools and DLLs.

The pink cat icon is embedded in the executable. Rust, Homebrew and a separate FFmpeg installation are not required. This unsigned preview may trigger a Windows security warning. An OpenGL-capable graphics driver is required.

[Windows SHA-256 checksum](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/SHA256SUMS)

## Install on Linux

Extract the complete archive and run the launcher from the extracted directory:

```sh
tar -xzf easycat-0.1.0-linux-x86_64-legal-preview.tar.gz
cd easycat-0.1.0-linux-x86_64
./easycat
```

Keep **lib** and **Helpers** in place. Requires a Linux x86_64 desktop with glibc 2.35 or later (Ubuntu 22.04 or compatible), X11 or Wayland, an OpenGL-capable graphics driver and xdg-desktop-portal for file dialogs. FFmpeg, ffprobe and ffplay are included; Rust is not required.

[Linux SHA-256 checksum](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/SHA256SUMS)

Windows and Linux currently use software encoding. Hardware-accelerated export is implemented for macOS only. All packages are test previews; source/build provenance is included in each archive. See [recorded verification scope](RELEASE-VERIFICATION.json).

## What's included

- Lossless trimming and compatible container changes.
- Compression presets with automatic sample-based size estimates.
- Video preview, volume, fullscreen and a thumbnail trim timeline.
- An illustrated cosmic interface and the easycat mascot icon.

## Third-party software and source

The application source is available under the [MIT License](https://github.com/AmedeoSaadMichel/easycat/blob/main/LICENSE) at [AmedeoSaadMichel/easycat](https://github.com/AmedeoSaadMichel/easycat). FFmpeg and its bundled GPL components are distributed with their corresponding sources and build recipes in the [preview release](https://github.com/AmedeoSaadMichel/easycat-releases/releases/tag/v0.1.0-preview.6). Rust dependency source archives and license notices are provided there as well. Preserve these materials when redistributing the packages; third-party license rights remain intact.

## Update checks

Update checks were introduced in preview 4. In preview 6, easycat checks the public release policy at startup. The **Updates** button appears only when an update is available or the check failed; it stays hidden when current. An available update can be postponed; a build below the platform minimum requires an update after any running export finishes. Failed checks preserve offline use. Download buttons open the release page; installation is manual or through Homebrew.

The policy is in [updates.json](updates.json). The latest build and minimum supported build are both 6 on all four platforms. Preview 4 and 5 require an update after a successful check; any running export can finish before the update gate applies. Preview 3 and earlier have no checker: install preview 6 manually or through Homebrew to receive future notifications. Linux requires `/usr/bin/curl` for checks; if unavailable the app remains usable. No media or file paths are sent; GitHub receives normal request connection metadata.
