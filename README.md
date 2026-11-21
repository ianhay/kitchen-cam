# Kitchen Cam

A single-file web app that runs in your phone browser and automatically captures short photo bursts of two people cooking together. It uses the camera with on-device face and hand tracking (MediaPipe) to spot the moments worth keeping.

**Version:** 0.1.9

## How to use

1. Open the Pages URL on your phone: https://ianhay.github.io/kitchen-cam/
2. Prop the phone up facing the kitchen.
3. Tap **Start** (Controls tab) and allow camera access. Settings and the Captures gallery are in the other tabs.
4. Pick a **Lens** (wide, ultra wide, telephoto) and a **Zoom** level in the Controls tab once the camera is running. Which lenses appear depends on what your phone and browser expose.
5. Cook. Bursts are captured automatically; **Manual burst** takes one on demand.
6. Review captures in the Captures tab: tap a photo to open it and swipe, or tap the left or right side of the screen, to browse, tap ★ to mark keepers, or use **Select** (or long-press) to pick several at once. Filter to **Starred**, then **Download ZIP** or **Share**.

The camera needs HTTPS, which is the only reason the page is hosted.

## Moments it captures

| Moment | What triggers it |
| --- | --- |
| Smiling | Any detected face with a clear smile |
| Taste testing | Fingertips near the mouth |
| Smelling | Fingertips near the nose, or an eyes-closed sniff |
| Looking at each other | Two faces turned toward one another |
| Kissing | Two faces with one mouth on the other's mouth, or puckered against the cheek |
| Prep action | Hands below face level moving briskly |

Detection thresholds are first guesses and not yet tuned. Burst size, sensitivity and resolution can be changed in the app.

## Privacy

All processing happens on your device. Nothing is uploaded: photos are stored in your browser's IndexedDB and leave the device only when you download or share them. There is no backend and no analytics.

On load the page fetches code and assets from public CDNs (MediaPipe and JSZip from jsDelivr, the MediaPipe model files from Google Cloud Storage, and fonts from Google Fonts). Those requests carry no camera data.

## Development

No build step. `index.html` is the whole app. The version lives in `APP_VERSION` in the script and in `<meta name="version">`; keep them in sync and see [CHANGELOG.md](CHANGELOG.md).

## License

[MIT](LICENSE)
