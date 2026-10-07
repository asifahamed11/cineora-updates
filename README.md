# Cineora signed update channel

This repository contains the signed stable update manifest and Windows installer releases for Cineora standalone.

## Latest release

[Cineora 1.2.15 installer](https://github.com/asifahamed11/cineora-updates/releases/download/v1.2.15/Cineora-Standalone-Setup.exe)

This release fixes mobile search overlays, fractional seeking, timeline buffering, fullscreen performance, audio labels, media reference recovery and Live Together synchronization. Cards and episodes include IMDb vote counts with daily updates. Discovery adds year, genre, content type and minimum rating/vote filters; game/software downloads stay in the file gateway.

Existing updater-enabled PCs fetch `cineora-update.json`, verify the Ed25519 signature and installer SHA-256, then install the update automatically. Existing authorized tunnel configuration is retained.

Public release assets do not contain Cloudflare credentials. New trusted replicas use the private installer supplied separately by the operator. No ZIP is required for end-user installation.
