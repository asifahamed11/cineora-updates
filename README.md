# Cineora signed update channel

[Download Cineora 1.2.31 for Windows](https://github.com/asifahamed11/cineora-updates/releases/download/v1.2.31/Cineora-Standalone-Setup.exe).

Cineora now uses the selected Clear sound set for notifications, bookmarks and selections. Mute and volume persist; normal interface sounds stay silent during video playback. The sound studio is included at `/sound-preview.html`.

Watch Together supports one durable room authority across PC and Android, so switching public tunnel origins does not lose a room. All connected replicas must share the private authority configuration. Trusted Setup packages provision it; generic updates preserve it.

Existing updater-enabled PCs verify the Ed25519 signature in `cineora-update.json` and the installer SHA-256 before applying an update. Existing app data and authorized public-hosting configuration are retained.

The public Windows installer contains no deployment credentials. Fresh trusted replicas use the private installer supplied separately by the website operator. Do not distribute private Setup builds publicly.

[Cineora Server 1.0.20 for Android](ANDROID_HOSTING.md) bundles website/server 1.2.31. Its signed private APK is available to the operator in the private source repository. Termux and root are not required.
