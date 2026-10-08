# Cineora signed update channel

This repository contains the signed stable update manifest and Windows installer releases for Cineora standalone.

## Latest release

[Cineora 1.2.19 installer](https://github.com/asifahamed11/cineora-updates/releases/download/v1.2.19/Cineora-Standalone-Setup.exe)

Fresh PCs install automatically without a public-tunnel credential. Existing authorized hosting is retained. Fullscreen close hides with the playback controls; timeline endpoints, elapsed/duration display, narrower desktop controls and episode download alignment are corrected. Playing episode badges use a clean muted style. New catalog content triggers an IMDb metadata refresh without waiting for the next day, including exact episode ratings and vote counts. IMDb publishes the underlying datasets daily; unavailable or ambiguous ratings remain empty.

Existing updater-enabled PCs fetch `cineora-update.json`, verify the Ed25519 signature and installer SHA-256, then install the update automatically. Existing authorized tunnel configuration is retained.

Public release assets do not contain Cloudflare credentials. New trusted replicas use the private installer supplied separately by the operator. No ZIP is required for end-user installation.

The final player keeps desktop controls on one line, removes Picture Size and Screenshot actions while retaining Theater, and gives long timestamps a compact layout on 320px phones. Inline video and fullscreen episode lists scroll normally; dedicated volume wheel controls remain available.

For phone hosting, [Cineora Server 1.0.8](ANDROID_HOSTING.md) adds an adaptive memory budget and live heap usage. It contains the same player and IMDb fixes, with automatic private setup without Termux or root. The APK is supplied privately. Version 1.0.8 fixes native Android tunnel DNS and reconnects stalled connections. Public hosting requires the phone connector enabled and matching PC connectors disabled. The standard Windows EXE supplies local hosting without the owner's private tunnel credential.
