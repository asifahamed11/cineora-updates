# Cineora signed update channel

[Download Cineora 1.2.41 for Windows](https://github.com/asifahamed11/cineora-updates/releases/download/v1.2.41/Cineora-Standalone-Setup.exe).

The library seed contains 43,999 entries. Source discovery follows all year/language/alphabet groups, awards, wrestling branches and software collections. Bounded scans resume their queue; historical backfill stays quiet in notifications. Metadata and artwork load on demand. Video courses have a lesson browser.

Fullscreen keeps the current phone orientation and follows the device's rotation setting. It avoids forced landscape rotation during entry. Watch Together refreshes after display changes and can correct small drift when sufficient downloaded buffer remains. Thin or unavailable buffers do not trigger a display-only seek or stream restart.

Room invitations now join directly from a shared link. Share room link uses native sharing where available; Copy link and manual copying remain available. Browser-blocked autoplay has a Tap to watch action. Mobile fullscreen video supports 1x–4x pinch zoom and panning while controls keep their size.

Cineora uses the selected Clear sound set for notifications, bookmarks and selections. Audio can unlock again on the next touch after Android suspends it. Mute and volume persist; normal interface sounds stay silent during video playback. The sound studio is included at `/sound-preview.html`.

Watch Together supports one durable room authority across PC and Android, so switching public tunnel origins does not lose a room. All connected replicas must share the private authority configuration. Trusted Setup packages provision it; generic updates preserve it.

Existing updater-enabled PCs verify the Ed25519 signature in `cineora-update.json` and the installer SHA-256 before applying an update. Existing app data and authorized public-hosting configuration are retained.

The public Windows installer contains no deployment credentials. Fresh trusted replicas use the private installer supplied separately by the website operator. Do not distribute private Setup builds publicly.

[Cineora Server 1.0.30 for Android](ANDROID_HOSTING.md) bundles website/server 1.2.41. Its signed private APK is available to the operator in the private source repository. Termux and root are not required.

The library has six main sections and 23 collections. Satyajit Ray has its own collection; alphabet partitions combine under TV & Web Series. Legacy and normalized source IDs resolve across PC and Android so saved links and shared rooms remain compatible.

Filters follow the selected collection and its available metadata. Styled lists support keyboard and touch, with appropriate collection/field icons. Main titles omit technical tags while details retain metadata. Posters for off-screen cards and a closed notification panel load when needed, reducing initial image traffic. Stale software parent records cannot hide imported child cards after restart.

Mobile and desktop menus share section labels. Mobile shortcuts begin Home, Movies, Web Series and Anime. Instant search shows title suggestions before a full search. Notifications have the same six section filters, and More filters groups common choices with optional rating/download controls. Hidden hero/filter work is deferred. This release includes follow-redirects 1.16.1.

Search suggestions now show real poster thumbnails with a logo fallback. This release adds bounded smaller JPEG variants, catalogue revalidation caches, compressed content-hashed application styles, and loads the existing 3D hero engine only on Home. Search text is usable before artwork finishes. Original media-server and Internet latency can still affect playback.

Version 1.2.40 reduces startup overhead with one preloaded application script bundle, a smaller lossless UI logo, common icon font subsets with full-font fallback, and earlier catalogue requests. Restored collection views avoid Home-only work; Home avoids an invisible all-content request and duplicate rail rendering. Layout, colours and existing room/player behavior are retained.

Version 1.2.41 bounds artwork discovery and downloads, separates network and encoder capacity, and prevents a slow source from occupying every worker. Existing cached images remain visible during refresh; smaller card variants can reuse a cached image without contacting the source. Visible cards take priority, distant images stay deferred, and transient failures have limited recovery attempts. Unavailable original artwork can still require a logo fallback; a faster failure is not a successful photo delivery.
