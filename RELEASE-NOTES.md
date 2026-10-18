# easycat 0.1.0 preview 4

- Background update checks at startup, plus a manual **Updates** button.
- Dismissible notices for newer builds and a per-platform minimum build policy.
- A required update applies after any running export finishes; playback and preset measurements then stop. Failed checks preserve offline use, including failed retries.
- Update notices preserve space for export controls at the minimum window size.
- The Buy Me a Coffee banner remains in the footer.

This is the first update-aware build. The policy will advertise latest build 4 and minimum build 4 after all downloads are verified. Older previews do not contain the checker and cannot receive notifications or be blocked retroactively. Update manually or with Homebrew once to enable future checks.

The app reads the public updates.json over HTTPS using the operating system curl client; Linux requires /usr/bin/curl. No videos, file paths, identifiers or usage events are submitted. Failed network checks leave local editing available. GitHub receives normal connection metadata. Downloads open in your browser; easycat does not install updates automatically.

Homebrew: run `brew update` and `brew upgrade --cask easycat`.

Native builds are provided for macOS Apple Silicon, Windows x64 and Linux x86_64. Application source remains private. Dependency versions and bundled codecs/libraries are unchanged; corresponding third-party sources and licenses accompany the packages.

Preview limits remain: macOS 15+, ad-hoc signed and not notarized; Windows x64 unsigned; Linux x86_64 glibc 2.35+ with an OpenGL-capable desktop. See RELEASE-VERIFICATION.json for validation scope and SHA256SUMS for the six installer/source archive hashes.
