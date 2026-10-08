# Android primary hosting

## Standalone app

Cineora Server 1.0.8 is now available in the owner's private source repository.
Install its private Setup APK and open it once. The bundled server starts
automatically, configuration requires no copy/paste, and Termux/root are not
needed. The APK supports ARM64, ARMv7, x86 and x86-64 on Android 8.0+.
Actual full app testing is on Samsung M20 / Android 13 / ARM64; ARMv7 native
tools have also run on that phone. Other devices and 16 KB environments need
their own testing. This is not a guarantee of support for every Android phone.

The compact dashboard shows server and public connector status, library size,
stream count, speed, data sent, conversion jobs, uptime, server/free RAM, heap used/budget,
storage, network, battery/power and library/IMDb update times. Settings and logs
are collapsed. Android may require initial notification and background-use
consent. Boot start defaults on; an intentional Stop stays stopped.

The private Setup APK includes authorized site configuration. It stays private
and is not published in this public Windows update channel. The Windows
installer and signed manifest are v1.2.19. The M20 receives a 1024 MB Node
old-space budget, up from its previous automatic limit of about 784 MB.
Other phones receive a budget based on physical RAM, with lower 32-bit and
low-memory limits. This is a heap ceiling, not a reservation of physical RAM.
New catalog content starts an IMDb metadata refresh automatically. Scores and
vote counts depend on availability in IMDb's official daily datasets.

Local hosting is automatic. The public connector stays paused while the PC
serves the site: stop the matching old PC connector before enabling the phone.
App installation alone does not prove public hosting with the PC powered off.
Keep Wi-Fi/media-network access and power available independently of the PC.
Charging remains under Android control; the unsupported 20% loop is removed.

Version 1.0.8 fixes Android tunnel DNS: native Android resolves Cloudflare's
two documented edge hostnames, instead of the connector querying an unavailable
Linux DNS resolver at `[::1]:53`. Addresses refresh on connector restart, and
a connection that remains unready for 90 seconds is restarted automatically.
The local server keeps running when public DNS is unavailable. TLS verification
and token-file authentication remain enabled.

The ordinary Windows EXE on a friend's PC supplies local hosting; it contains
no owner tunnel credential and does not automatically host this domain. Keep
one public application origin for standalone Watch Rooms.

## Previous Termux deployment

A Windows installer does not automatically turn a phone into a public server.
The phone needs both the Cineora application and an authorized Cloudflare
connector routing the public hostname to its own localhost:3000.

Use official Termux and Termux:Boot. Install Node.js LTS, FFmpeg, curl,
termux-services, termux-tools and cloudflared. Obtain the Cineora source from
your private backup and run its `scripts/install-termux-server.sh`. Transfer
the authorized tunnel credential into Termux private storage with file mode
600, then run `scripts/install-termux-tunnel.sh`. Credentials belong in private
runtime storage; they must not be included in a public download or pasted into
a command line.

Exempt Termux and Termux:Boot from battery optimization. Keep the phone supplied
with power and Internet from a router or mobile data independently of the PC.
The boot script supervises the app and connector using full service paths.
The phone's connection must also reach the configured ISP/BDIX media servers.
Cloudflare access alone does not make private media sources reachable over
another ISP or ordinary mobile data. Run the private source's
`node ~/cineora/scripts/check-android-host.js` to check app, connector and media
endpoints separately. It does not disclose private URLs or credentials, and
it does not substitute for a real playback or PC-off test.

When the phone is the sole public application server, disable every matching
PC connector, including a legacy Windows Cloudflared service if it belongs to
the same tunnel. Leave unrelated tunnels and Cloudflare WARP unchanged.
Standalone Watch Together rooms require one public application process, or
the shared control architecture, to avoid splitting room state between hosts.
Keep the phone connector paused during preparation if the PC still serves the
public site. The private Android guide includes persistent pause and enable
commands, and the updated boot script honors a paused connector.

Verify `localhost:3000/api/ready`, connector readiness on
`localhost:20241/ready`, and the public site with the PC application and all its
matching connectors stopped. Test actual playback; a connected tunnel alone
does not prove independence from the PC. Physical power-off and Android reboot
checks must be reported separately from service-stop tests.

The current private source also corrects HEVC capability detection and paused
seek recovery, reducing unnecessary conversions on the Android host. Deploy
its matching HTML and JavaScript client files together. The published Windows
installer is v1.2.19 and includes the shared player corrections.
