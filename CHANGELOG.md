# Changelog

## 0.1.5 - 2026-11-21

- **Multi-select** in the Captures tab: tap **Select** (or long-press a photo), tap photos to toggle, then use Select all / None, Star or Unstar, and Delete (tap twice to confirm). Download ZIP and Share act on the selection when there is one.
- **Swipe** left or right in the photo viewer to move between photos (drag with a mouse works too). Previous and Next buttons and the arrow keys still work.
- **Star** keepers from the viewer (or in bulk from the selection). Stars show as a badge on thumbnails, are saved on the device, and there is a **Starred** filter, so Download ZIP and Share can export just the keepers. Clear all warns when starred photos are included.
- The viewer photo now scales to the available height, fixing overflow in landscape.

## 0.1.4 - 2026-11-21

- Controls are now in three tabs below the camera view: **Controls** (Start, Manual burst, Flip camera, Dim screen), **Settings** (burst size, sensitivity, resolution, moment toggles, tracking overlay) and **Captures** (gallery, filter, ZIP, share, clear). The Captures tab shows the photo count.
- Added a **Keep screen on** option (on by default). Turning it off releases the screen wake lock, including mid-session.

## 0.1.3 - 2026-11-21

- Removed the page header so the camera view sits at the top of the screen in landscape. The app name, version and status line moved to the top of the controls panel.

## 0.1.2 - 2026-11-21

- Added a **Kissing** moment (toggle, chip, gallery filter). Fires when two faces are detected with mouth-to-mouth distance under 0.45 of face width, or a puckered mouth within 0.3 of face width of the other person's cheek. 2 frames to trigger, 12 s cooldown, checked before the other moments. Thresholds are untuned first guesses.

## 0.1.1 - 2026-11-21

- First published release on GitHub Pages (https://ianhay.github.io/kitchen-cam/).
- Added README, MIT LICENSE, CHANGELOG and `.nojekyll`.
- No functional changes to the app; version bumped from 0.1.0 as a revision.

## 0.1.0

- Initial single-file version: on-device MediaPipe face and hand tracking, auto-capture bursts for smiling, taste testing, smelling, looking at each other and prep action; IndexedDB storage; ZIP and Web Share export.
