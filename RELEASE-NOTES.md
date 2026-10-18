# easycat 0.1.0 preview 5

- Hides the Updates button when easycat is already current and while checking.
- Keeps Updates available when a newer build exists or a failed check can be retried.
- Preserves optional update notices, minimum-build enforcement and offline use when checks fail.
- Keeps development-only update simulations out of all distributed release executables.

The policy advances to latest build 5 with minimum build 4 after downloads are verified. Preview 4 users receive an optional update; no new mandatory upgrade is introduced. Preview 3 and earlier need a manual update because they predate the checker.

Homebrew: `brew update` followed by `brew upgrade --cask easycat`.

Native packages for macOS Apple Silicon, Windows x64 and Linux x86_64. App source remains private. Codec binaries, bundled libraries, third-party licenses and corresponding source archives are preserved from the verified preview 4 bundles.

Preview limits remain: macOS 15+, ad-hoc signed and not notarized; Windows x64 unsigned; Linux x86_64 glibc 2.35+ and an OpenGL-capable desktop. Linux update checks require /usr/bin/curl; missing clients preserve local use. No automatic installation, media uploads or telemetry.

See RELEASE-VERIFICATION.json for validation scope and SHA256SUMS for installer/source archive checksums.
