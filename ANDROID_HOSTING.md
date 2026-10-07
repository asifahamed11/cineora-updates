# Android primary hosting

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
