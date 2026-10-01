# Getting started with OrangePic

## 1. Prepare your PhotoPrism server

OrangePic connects over HTTPS and HTTP as well. Before you add your server in the app:

1. Make sure your PhotoPrism instance is reachable at an https:// address, for example https://photos.example.com
2. Check that you can open the address and log in from Safari on the same device first.

## 2. Add your server in the app

1. Open OrangePic and tap [Add server / Login: use the exact button name].
2. Enter the server URL, for example `https://photos.example.com` (include the port if you use one, such as `:2342` behind HTTPS).
3. Enter your PhotoPrism username and password.
4. Your library loads. The app keeps you signed in using a session token.

## 3. Tips for common setups

**Reverse proxy (Nginx, Traefik, Caddy)**
- Forward the standard headers and allow WebSocket upgrade.
- Set `PHOTOPRISM_SITE_URL` to your public HTTPS address.
- Do not set upload size limits that are too small if you use photo upload.

**Access from outside your home network**
- Use a domain name

**Apple TV and Apple Watch**
- Apple TV: sign in on the TV with the same server URL.
- Apple Watch: choose photos on iPhone and they sync to the watch.

## 4. Troubleshooting

| Problem | What to check |
|---|---|
| "Cannot connect" | Is the URL http:// and reachable from your phone's network? |
| Certificate error | Use a certificate from a trusted authority, not a self-signed one |
| Login fails | Try the same username and password in Safari. Check whether two-factor/app passwords are in use [confirm] |
| Photos do not load outside home | Check your reverse proxy and firewall |
| Widget shows old photos | Open the app once, then wait for the widget to refresh |
| AutoSync does not upload | Allow Photos access (All Photos) and Background App Refresh in iOS Settings |

Still stuck? Open a [Discussion](https://github.com/mover81/OrangePic-Feedback/discussions) or a bug report and include your app version, device, iOS version and PhotoPrism version. Do not post your password or private URLs.
