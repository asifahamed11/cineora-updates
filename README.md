# Cineora signed update channel

This repository contains the signed stable update manifest and Windows installer releases for Cineora standalone.

## Latest release

[Cineora 1.2.16 installer](https://github.com/asifahamed11/cineora-updates/releases/download/v1.2.16/Cineora-Standalone-Setup.exe)

This release puts IMDb counts in brackets beside each rating and integrates More filters into the library toolbar. A responsive filter dialog provides relevant options for movies, series, games, software and tutorials, with live result counts and saved selections. Header navigation no longer clips lowercase text. Existing playback, Live Together and daily IMDb refresh fixes are retained.

Existing updater-enabled PCs fetch `cineora-update.json`, verify the Ed25519 signature and installer SHA-256, then install the update automatically. Existing authorized tunnel configuration is retained.

Public release assets do not contain Cloudflare credentials. New trusted replicas use the private installer supplied separately by the operator. No ZIP is required for end-user installation.
