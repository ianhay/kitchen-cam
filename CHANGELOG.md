# Changelog

## 0.1.9 - 2026-11-21

- Added a **Lens** picker and **Zoom** control in the Controls tab (shown once the camera is running). The picker lists the camera devices the browser exposes for the current side (for example ultra wide, main, telephoto); the zoom slider and 0.5x / 1x / 2x / 5x buttons appear when the browser supports hardware zoom, and on many Android phones a zoom below 1x is the ultra-wide lens.
- The chosen lens is remembered on the device. Flip camera returns to the default lens for the other side, and if a remembered lens is no longer available the app falls back to the default camera. Zoom is kept when the resolution changes.
- If the phone or browser only offers one lens, the panel says so instead of showing an empty picker.

## 0.1.8 - 2026-11-21

- Added **Clear unstarred** in the Captures tab: deletes every photo that isn't starred and keeps the keepers (tap twice to confirm). It is disabled until at least one photo is starred.
- Removed the per-moment checkboxes from Settings. Every moment (smiling, taste testing, smelling, looking at each other, kissing, prep action) is always detected and recorded, and the pills, gallery filter and ZIP folders are unchanged.

## 0.1.7 - 2026-11-21

- The moment pills under the camera view are now a fixed size. They used to grow and wrap onto extra lines when "seen" or "captured" was appended to the label. State is shown by the dot and colour, and the words are kept for screen readers only.
- Pills are laid out on an even grid (two columns in portrait, three in landscape). The "Looking at each other" pill is labelled "Eye contact" so it fits; the toggle, filter and ZIP folder keep the full name. Any other long label is trimmed with an ellipsis instead of widening the pill.
- Fixed all pills briefly showing the orange "captured" state for the first 1.5 seconds after the page loads.

## 0.1.6 - 2026-11-21

- In the photo viewer, tap the left half of the screen to go to the previous photo and the right half for the next one. Faint arrows at the screen edges show the tap zones. Swiping, the buttons and the arrow keys still work.

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
