# easycat downloads

Cut. Transform. Meow. Local video trimming, compression and container conversion.
This repository distributes binaries and third-party source materials only. The easycat application source is available under the [MIT License](https://github.com/AmedeoSaadMichel/easycat/blob/main/LICENSE) at [AmedeoSaadMichel/easycat](https://github.com/AmedeoSaadMichel/easycat).

[Choose your operating system and view installation instructions →](DOWNLOADS.md)

## Install

- [macOS Apple Silicon DMG](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-macos-arm64-legal-preview.dmg) — macOS 15 or later; ad-hoc signed preview, not notarized.
- [macOS Intel DMG](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-macos-x86_64-legal-preview.dmg) — Intel x86_64, macOS 15 or later; ad-hoc signed preview, not notarized.
- [Windows x64 ZIP](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-windows-x64-legal-preview.zip) — extract the entire package and run easycat.exe; unsigned preview.
- [Linux x86_64 tar.gz](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-linux-x86_64-legal-preview.tar.gz) — glibc 2.35+, extract and run ./easycat.

On macOS, add the personal tap once:

```sh
brew tap AmedeoSaadMichel/easycat https://github.com/AmedeoSaadMichel/easycat-releases.git
brew trust --cask amedeosaadmichel/easycat/easycat
brew install --cask easycat
```

The trust command authorizes only the easycat cask, not every package or command in the tap. Recent Homebrew versions require explicit trust for non-official taps or their individual packages. See [Homebrew Tap Trust](https://docs.brew.sh/Tap-Trust).

An existing easycat tap pointing to the private development repository must be untapped and added again with the public URL. Homebrew does not remove macOS signature limitations; use normal Privacy & Security controls if macOS asks for approval.

## First launch on macOS

This preview has an ad-hoc signature and is not notarized with Apple. Installation can succeed while macOS still requires separate approval at first launch. This applies to both the DMG and Homebrew installations.

1. Open **easycat** from **Applications**.
2. If macOS blocks it because the developer cannot be verified or the app is not notarized, open **System Settings → Privacy & Security**.
3. Find the notice for **easycat**, click **Open Anyway**, then confirm the opening. Authenticate if macOS asks.

If the easycat notice is missing, try opening the app again, then return to Privacy & Security. Do not disable Gatekeeper system-wide. See [Apple's instructions](https://support.apple.com/en-us/102445).

For installation errors and warnings about unrelated taps, see [Homebrew installation troubleshooting](DOWNLOADS.md#homebrew-installation-troubleshooting).

## Third-party software and source

These packages contain FFmpeg under GPLv3-or-later, including GPL codec components. The easycat app runs FFmpeg as a separate executable. Third-party license rights remain intact.

- [MIT application source archive (Apple Silicon, Windows, Linux)](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-preview.6-source.tar.gz)
- [Intel application source archive](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-preview.6-intel-source.tar.gz)
- [Intel macOS dependency sources and native build metadata](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-macos-intel-third-party-source.tar.gz)
- [Intel checksums and verification](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/SHA256SUMS-INTEL)
- [macOS dependency source](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-macos-third-party-source.tar.gz)
- [Windows/Linux dependency source](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-portable-third-party-source.tar.gz)
- [Rust third-party crate source](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/rust-third-party-sources.tar.gz)
- [Checksums](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/SHA256SUMS)

Licenses and notices are included in each installer under Licenses/ThirdParty (inside easycat.app/Contents/Resources on macOS). Preserve the source archives beside each released binary indefinitely. The MIT-licensed application source is published separately in [easycat](https://github.com/AmedeoSaadMichel/easycat); the application source archive is attached to this release.

Native codec tests and the recorded source/license checks passed; see RELEASE-VERIFICATION.json for the original three packages and [INTEL-RELEASE-VERIFICATION.json](INTEL-RELEASE-VERIFICATION.json) for the Intel package and its preview limits. Downloads and corresponding third-party sources are available in the linked preview release.

## Update checks

Update checks were introduced in preview 4. In preview 6, easycat checks the public release policy at startup. The **Updates** button appears only when an update is available or the check failed; it stays hidden when current. An available update can be postponed; a build below the platform minimum requires an update after any running export finishes. Failed checks preserve offline use. Download buttons open the release page; installation is manual or through Homebrew.

The policy is in [updates.json](updates.json). The latest build and minimum supported build are both 6 on all four platforms. Preview 4 and 5 require an update after a successful check; any running export can finish before the update gate applies. Preview 3 and earlier have no checker: install preview 6 manually or through Homebrew to receive future notifications. Linux requires `/usr/bin/curl` for checks; if unavailable the app remains usable. No media or file paths are sent; GitHub receives normal request connection metadata.

The Intel [public download verification](INTEL-PUBLICATION-VERIFICATION.json) confirms anonymous access, matching checksums and preservation of the original release assets.
