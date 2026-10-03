# Cineora signed update channel

This repository contains the signed stable update manifest and Windows installer releases for Cineora standalone.

## Latest release

[Cineora 1.2.14 installer](https://github.com/asifahamed11/cineora-updates/releases/download/v1.2.14/Cineora-Standalone-Setup.exe)

This release fixes HTTPS media playback recovery and fullscreen episode selection. It includes the earlier card, IMDb, collection design, hero animation, and automatic installer improvements.

Existing updater-enabled PCs fetch `cineora-update.json`, verify the Ed25519 signature and installer SHA-256, then install the update automatically. Existing authorized tunnel configuration is retained.

Public release assets do not contain Cloudflare credentials. New trusted replicas use the private installer supplied separately by the operator. No ZIP is required for end-user installation.
