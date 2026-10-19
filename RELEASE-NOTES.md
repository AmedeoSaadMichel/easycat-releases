# easycat 0.1.0 preview 6

- Publishes easycat as open source under the MIT License.
- Renames workspace folders, Rust packages and the CLI from easycut to easycat.
- Includes the application MIT license in all platform packages.
- Rebuilds and verifies native macOS Apple Silicon, Windows x64 and Linux x86_64 packages.

Application source: https://github.com/AmedeoSaadMichel/easycat/tree/v0.1.0-preview.6
The original application source archive matches the Apple Silicon, Windows and Linux build commit. The Intel application source archive matches its separate source tag below.

The live policy now requires build 6 on all platforms (latest build 6, minimum build 6). Preview 4 and 5 must update after a successful check; an already-running export can finish before the update gate applies. The original verification report records the publication-time minimum of 4; the policy was raised afterward without changing release assets. Update notices preserve offline use if checks fail. Installation remains manual or through Homebrew.

Homebrew: `brew update` followed by `brew upgrade --cask easycat`.

The original Apple Silicon, Windows and Linux codec binaries, bundled libraries and third-party license files are preserved byte-for-byte from verified preview 5 bundles. The corresponding third-party source archives are included alongside the installers with unchanged checksums. Application MIT licensing does not replace third-party licenses.

Preview limits: macOS Apple Silicon and Intel, macOS 15+, ad-hoc signed and not notarized; Windows x64 unsigned, without manual interactive GUI certification; Linux x86_64 glibc 2.35+ and an OpenGL-capable desktop. Linux update checks require /usr/bin/curl; missing clients preserve local use. No automatic installation, media uploads or telemetry.

See RELEASE-VERIFICATION.json for the validation scope and SHA256SUMS for installer and source archive checksums.


## Intel macOS package

The native x86_64 DMG is now available for macOS 15 or later, build 6. Native format/lint checks, all 67 Rust tests and 15 Python checks passed. Packaged H.264, HEVC (including 10-bit), VP9 and AV1 encode/decode tests, lossless remux, thumbnails, audio playback, CLI exports, GUI startup, strict signatures and DMG integrity checks passed. All 14 bundled Homebrew components match the reviewed source inventory. The package is ad-hoc signed and is not notarized.

- [Intel DMG](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-macos-x86_64-legal-preview.dmg)
- [Exact Intel application source](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-preview.6-intel-source.tar.gz), matching [v0.1.0-preview.6-intel](https://github.com/AmedeoSaadMichel/easycat/tree/v0.1.0-preview.6-intel)
- [Intel dependency sources and native build metadata](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/easycat-0.1.0-macos-intel-third-party-source.tar.gz)
- [Intel verification report](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/INTEL-RELEASE-VERIFICATION.json) and [Intel checksums](https://github.com/AmedeoSaadMichel/easycat-releases/releases/download/v0.1.0-preview.6/SHA256SUMS-INTEL)

These five Intel assets supplement preview 6. The original nine release files and their checksums remain unchanged. The latest and minimum supported build are 6 for all four platforms.
