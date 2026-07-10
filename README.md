# Mission Control 1.0

A box-inspired web controller for the littleBits Space Rover Inventor Kit.

## New design

- Uses the littleBits logo cropped from the user's photographed box.
- Purple, cream, green, orange, and blue palette inspired by the original packaging.
- Moon-style joystick surface and module-like arm control.
- Grouped Communications sound console:
  - Robot
  - Creatures
  - Funny
  - Effects
- Preserves the stable Bluetooth, drive, arm, auto-arm, sound finder, orientation, and calibration behavior from v8.
- Installable PWA assets included.

## Deploy

Upload all five files together:

- `index.html`
- `manifest.webmanifest`
- `sw.js`
- `icon-192.png`
- `icon-512.png`

Because a service worker caches the app, after deployment fully close and reopen Bluefy or clear the site's stored data if an older version appears.


## v1.2

- Remembers the selected w33 Control Hub after the first successful connection.
- On later launches, the Connect button first tries to reconnect to the previously permitted rover using `navigator.bluetooth.getDevices()`.
- Falls back to the filtered Bluetooth picker when automatic reconnect is unavailable or the saved rover is not found.
- Added **Forget saved rover** in Setup for classrooms or shared devices.
- Browser support varies; Bluefy may still require the chooser depending on its Web Bluetooth implementation.
