# USB Camera (Fluidd/Mainsail)

Registers an external USB camera as a camera in Fluidd and Mainsail, so it appears as a
tile without manual setup under Settings > Cameras.

## What it does

- Adds a Moonraker `[webcam]` entry for the USB camera's WebRTC stream and JPEG snapshots
  (`/webcam2/webrtc`, `/webcam2/snapshot.jpg`).
- Lets you pick the name shown in the UI.

## Configuration

- **Camera name in Fluidd/Mainsail** (default `USB`): for example `USB`, `External`,
  `Bed View`.

## Requires

- **Camera HW Accel**, which serves the stream (installed automatically). Make sure USB
  camera support is enabled there and a camera is plugged in.

## Notes

Snapmaker U1. This plugin only registers the camera entry; streaming comes from Camera HW
Accel.
