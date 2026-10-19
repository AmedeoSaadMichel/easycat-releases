# easycat 0.1.0 preview 6

- Publishes easycat as open source under the MIT License.
- Renames workspace folders, Rust packages and the CLI from easycut to easycat.
- Includes the application MIT license in all platform packages.
- Rebuilds and verifies native macOS Apple Silicon, Windows x64 and Linux x86_64 packages.

Application source: https://github.com/AmedeoSaadMichel/easycat/tree/v0.1.0-preview.6
The application source archive attached to this release matches the native application build commit.

The live policy now requires build 6 on all platforms (latest build 6, minimum build 6). Preview 4 and 5 must update after a successful check; an already-running export can finish before the update gate applies. The original verification report records the publication-time minimum of 4; the policy was raised afterward without changing release assets. Update notices preserve offline use if checks fail. Installation remains manual or through Homebrew.

Homebrew: `brew update` followed by `brew upgrade --cask easycat`.

Codec binaries, bundled libraries and existing third-party license files are preserved byte-for-byte from verified preview 5 bundles. The corresponding third-party source archives are included alongside the installers with unchanged checksums. Application MIT licensing does not replace third-party licenses.

Preview limits: macOS Apple Silicon, macOS 15+, ad-hoc signed and not notarized; Windows x64 unsigned, without manual interactive GUI certification; Linux x86_64 glibc 2.35+ and an OpenGL-capable desktop. Linux update checks require /usr/bin/curl; missing clients preserve local use. No automatic installation, media uploads or telemetry.

See RELEASE-VERIFICATION.json for the validation scope and SHA256SUMS for installer and source archive checksums.
