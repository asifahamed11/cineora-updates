# Cineora signed update channel

[Download Cineora 1.2.29 for Windows](https://github.com/asifahamed11/cineora-updates/releases/download/v1.2.29/Cineora-Standalone-Setup.exe).

This release keeps the open movie/episode and position after refresh, updates catalog cards without resetting loaded pages, refreshes games/software artwork, and provides compact working caption controls. Rating stars emphasize vote confidence; IMDb Top 250 matching and immediate notification entries are fixed.

Existing updater-enabled PCs verify the Ed25519 signature in `cineora-update.json` and the installer SHA-256 before applying an update. Existing app data and authorized public-hosting configuration are retained.

The public Windows installer contains no Cloudflare credential. Fresh trusted replicas use the private installer supplied separately by the website operator. Do not distribute private Setup builds publicly.

[Cineora Server 1.0.18 for Android](ANDROID_HOSTING.md) bundles the same website and server changes. Its signed private APK is available to the operator in the private source repository. Termux and root are not required.
