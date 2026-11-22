# Changelog

## 0.1.11 - 2026-11-22

- **Kissing and Looking at each other re-worked.** Both previously needed precise facial landmarks (mouth on mouth, noses turned a set amount), which fail when two heads are close, turned or overlapping, so nothing was captured in a real session. They now work from where the two heads are:
  - **Kissing** fires when the two heads touch or overlap (centre-to-centre under 0.95 head heights, at about the same height). It also fires if the tracker loses one face just after the heads met, because the faces merge during a kiss. It needs about 0.4 s of this, up from 2 to 4 detection frames. Side-by-side heads that touch (shoulder to shoulder) will count too.
  - **Looking at each other** fires when the heads are within 3 head heights, at least one is turned toward the other, and neither is turned away. The old rule needed both to turn by a fixed amount.
  - Distances use head height, which holds up when a head turns to profile, instead of cheek-to-cheek width, which collapses.
- The camera overlay now draws a line between the two heads (solid when counted as together or looking, dashed when merely near), and the status line shows the head **gap** (in head heights) so thresholds can be tuned from real use. Face detection is slightly more forgiving (confidence thresholds 0.35).
- **Share to apps.** The Share button is now labelled **Share to apps**, and the photo viewer has a **Share** button beside Save, so a single photo can go straight to Google Photos or any other app in the share sheet. If the browser cannot share, it now says so instead of silently downloading. Save and Download ZIP are unchanged.
- **0.5x zoom button is now always shown** on a back camera. If the browser does not expose the ultra-wide, tapping it says so. A **Camera details** section lists the cameras and zoom range the browser reports. When several back cameras are listed, pick the ultra-wide in the Lens list and tap **Use this lens for 0.5×** to remember it.

## 0.1.10 - 2026-11-21

- Zoom now offers **0.5x** on phones whose browser reports a zoom range starting at 1x (for example the Pixel 8 Pro in Chrome). When the browser exposes the ultra-wide as its own camera, the 0.5x button switches to it, and 1x or higher switches back to the main camera. The ultra-wide is picked by name where the phone gives one, or assumed to be the only other back camera.
- The Controls tab now shows the zoom range the browser reports, and says when no ultra-wide lens is exposed, so a missing 0.5x can be diagnosed. All cameras are still listed under Lens for manual choice.

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
