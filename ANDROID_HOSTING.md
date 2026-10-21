# Cineora Android hosting

Cineora Server **1.0.28** bundles website/server **1.2.39**. The signed private Setup APK is supplied through the operator's private source repository. Update the existing package in place to retain settings and app data. Termux, rooting and manual credential entry are not required for this variant.

The APK includes ARM64, ARMv7, x86 and x86-64 runtimes for Android 8 or later. The installed release is verified on Samsung M20 / Android 13 / ARM64; this does not establish compatibility with every Android device.

The dashboard reports application server, public connector and library status, traffic, conversion jobs, memory, battery and metadata-update times. Keep Android's required notification/background permissions enabled for hosting.

Existing public connector settings are preserved during updates. Keep the operator's selected host configuration. A deliberately selected phone-only deployment should stop its matching PC connectors; a deployment using several authorized hosts needs consistent routing/shared state for Watch Rooms. Do not change unrelated tunnels or Cloudflare WARP.

Check the local application at `http://localhost:3000/api/ready` and the public site separately. A connected tunnel does not prove that upstream media is available. Test playback and large seeks; physical power-off and reboot checks are separate from service/readiness checks.

This release keeps fullscreen in the current device orientation instead of forcing an Android rotation during entry. Normal device auto-rotation remains available. Watch Together refreshes after display changes and corrects small drift only when sufficient downloaded buffer remains. Thin or unavailable buffers do not trigger a display-only seek or stream restart. Existing room links, pinch zoom, Clear sounds and notification repairs remain included. Original-source availability still controls when new uploads can be discovered.

This release includes a 43,999-entry catalogue seed. Existing installations merge it while retaining current content IDs and newer metadata. Source discovery resumes through all organizational branches without turning grouping folders into content cards.

The library has six main sections and 23 collections. Satyajit Ray has its own collection; alphabet partitions combine under TV & Web Series. Legacy and normalized source IDs resolve across PC and Android so saved links and shared rooms remain compatible.

Filters follow the selected collection and its available metadata. Styled lists support keyboard and touch, with appropriate collection/field icons. Main titles omit technical tags while details retain metadata. Posters for off-screen cards and a closed notification panel load when needed, reducing initial image traffic. Stale software parent records cannot hide imported child cards after restart.

Mobile and desktop menus share section labels. Mobile shortcuts begin Home, Movies, Web Series and Anime. Instant search shows title suggestions before a full search. Notifications have the same six section filters, and More filters groups common choices with optional rating/download controls. Hidden hero/filter work is deferred. This release includes follow-redirects 1.16.1.

Search suggestions now show real poster thumbnails with a logo fallback. This release adds bounded smaller JPEG variants, catalogue revalidation caches, compressed content-hashed application styles, and loads the existing 3D hero engine only on Home. Search text is usable before artwork finishes. Original media-server and Internet latency can still affect playback.
