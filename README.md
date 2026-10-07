# Cineora signed update channel

This repository contains the signed stable update manifest and Windows installer releases for Cineora standalone.

## Latest release

[Cineora 1.2.17 installer](https://github.com/asifahamed11/cineora-updates/releases/download/v1.2.17/Cineora-Standalone-Setup.exe)

This release fixes overlapping episode/seek controls, pressed timeline-thumb alignment and persistent touch time previews. Portrait playback puts controls and resume prompts below the picture; landscape keeps episode actions in the transport row. Native fullscreen, its fallback and orientation changes restore controls correctly. Resume state and cancelled gestures preserve the intended playback position. Existing IMDb counts, filters, daily refresh and Live Together fixes are retained.

Existing updater-enabled PCs fetch `cineora-update.json`, verify the Ed25519 signature and installer SHA-256, then install the update automatically. Existing authorized tunnel configuration is retained.

Public release assets do not contain Cloudflare credentials. New trusted replicas use the private installer supplied separately by the operator. No ZIP is required for end-user installation.
