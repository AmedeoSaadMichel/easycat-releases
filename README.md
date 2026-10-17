# easycat downloads

Cut. Transform. Meow. Local video trimming, compression and container conversion.
This repository distributes binaries and third-party source materials only. The easycat application source and development history remain private.

## Install

- [macOS Apple Silicon DMG](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.2/easycat-0.1.0-macos-arm64-legal-preview.dmg) — macOS 15 or later; ad-hoc signed preview, not notarized.
- [Windows x64 ZIP](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.2/easycat-0.1.0-windows-x64-legal-preview.zip) — extract the entire package and run easycat.exe; unsigned preview.
- [Linux x86_64 tar.gz](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.2/easycat-0.1.0-linux-x86_64-legal-preview.tar.gz) — glibc 2.35+, extract and run ./easycat.

On macOS, add the personal tap once:

```sh
brew tap AmedeoSaadMichel/easycat https://github.com/AmedeoSaadMichel/easycat-releases.git
brew install --cask easycat
```

An existing easycat tap pointing to the private development repository must be untapped and added again with the public URL. Homebrew does not remove macOS signature limitations; use normal Privacy & Security controls if macOS asks for approval.

## Third-party software and source

These packages contain FFmpeg under GPLv3-or-later, including GPL codec components. The easycat app runs FFmpeg as a separate executable. Third-party license rights remain intact.

- [macOS dependency source](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.2/easycat-0.1.0-macos-third-party-source.tar.gz)
- [Windows/Linux dependency source](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.2/easycat-0.1.0-portable-third-party-source.tar.gz)
- [Rust third-party crate source](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.2/rust-third-party-sources.tar.gz)
- [Checksums](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.2/SHA256SUMS)

Licenses and notices are included in each installer under Licenses/ThirdParty (inside easycat.app/Contents/Resources on macOS). Preserve the source archives beside each released binary indefinitely. Publishing these materials does not publish easycat's application source.

Native codec tests and the recorded source/license checks passed; see RELEASE-VERIFICATION.json for their exact scope and preview limits. Downloads and corresponding third-party sources are available in the linked preview release.
