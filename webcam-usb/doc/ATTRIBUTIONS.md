# Attributions - webcam-usb

**Plugin author:** paxx12 (Extended Firmware overlay `60-app-camera`), packaged by Bespok3d

Moonraker camera configuration.

| Upstream project | Author | Licence | Needed at runtime | Code ships in this package |
| --- | --- | --- | --- | --- |
| Extended Firmware overlay `60-app-camera` | paxx12 | GPL-3.0 | no | yes |

The Moonraker config in this package is the USB WebRTC camera block from the Extended Firmware
overlay `60-app-camera` (paxx12), GPL-3.0, in that overlay's `03_usb_camera.cfg`, where it ships
commented out. Four of its five lines ship here unchanged; only the camera name differs, because
this plugin lets the user set it. Every revision of that config file is paxx12's. The overlay also
carries V4L2 camera controls contributed by @justinh-rahb, which this plugin does not ship.
