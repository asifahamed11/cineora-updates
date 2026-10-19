# Cineora signed update channel

[Download Cineora 1.2.30 for Windows](https://github.com/asifahamed11/cineora-updates/releases/download/v1.2.30/Cineora-Standalone-Setup.exe).

This release restores notification posters, preserves known updates across reloads and host changes, refreshes the panel when opened, fixes action/read-state races and browser Back, and repairs popup expiry and phone landscape clipping. Episode checks retain a separate scan budget; corrupt history and equivalent file-size formatting no longer cause lost or false alerts.

Existing updater-enabled PCs verify the Ed25519 signature in `cineora-update.json` and the installer SHA-256 before applying an update. Existing app data and authorized public-hosting configuration are retained.

The public Windows installer contains no Cloudflare credential. Fresh trusted replicas use the private installer supplied separately by the website operator. Do not distribute private Setup builds publicly.

[Cineora Server 1.0.19 for Android](ANDROID_HOSTING.md) bundles the same website and server changes. Its signed private APK is available to the operator in the private source repository. Termux and root are not required.
