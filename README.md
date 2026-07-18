# DevFlow Factory — Update Feed

Public **Sparkle update feed** for the [DevFlow Factory](https://github.com/KlausFreiberufler/devflow-desktop) macOS app.

This repo holds **only** the auto-update artifacts:

- `appcast.xml` — the Sparkle feed (`SUFeedURL` points at the `raw` URL of this file on `main`).
- GitHub **Releases** — the signed `DevFlowFactory-<version>.zip` archives.

The **source code is private** and lives in `devflow-desktop`. Nothing here is source — releases are cut by `scripts/release-app.sh` in the source repo, which publishes the GitHub release and pushes `appcast.xml` here. Each archive is EdDSA-signed; the private key never leaves the macOS Keychain.
