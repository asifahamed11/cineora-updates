# Cineora Android hosting

Cineora Server **1.0.20** bundles website/server **1.2.31**. The signed private Setup APK is supplied through the operator's private source repository. Update the existing package in place to retain settings and app data. Termux, rooting and manual credential entry are not required for this variant.

The APK includes ARM64, ARMv7, x86 and x86-64 runtimes for Android 8 or later. The installed release is verified on Samsung M20 / Android 13 / ARM64; this does not establish compatibility with every Android device.

The dashboard reports application server, public connector and library status, traffic, conversion jobs, memory, battery and metadata-update times. Keep Android's required notification/background permissions enabled for hosting.

Existing public connector settings are preserved during updates. Keep the operator's selected host configuration. A deliberately selected phone-only deployment should stop its matching PC connectors; a deployment using several authorized hosts needs consistent routing/shared state for Watch Rooms. Do not change unrelated tunnels or Cloudflare WARP.

Check the local application at `http://localhost:3000/api/ready` and the public site separately. A connected tunnel does not prove that upstream media is available. Test playback and large seeks; physical power-off and reboot checks are separate from service/readiness checks.

This release restores notification artwork, preserves known notification history across reloads and host changes, refreshes Updates when opened, and repairs popup timers, action/read-state races, browser Back and landscape tab clipping. Episode checks reserve a separate scan budget. Original-source availability still controls when new uploads can be discovered.
