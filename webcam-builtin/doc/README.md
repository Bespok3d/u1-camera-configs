# Built-in Camera (Fluidd/Mainsail)

Registers the U1's built-in MIPI camera as a camera in Fluidd and Mainsail, so it shows up
as a tile without you adding it by hand under Settings > Cameras.

## What it does

- Adds a Moonraker `[webcam]` entry pointing at the built-in camera's WebRTC stream and
  snapshot URLs (`/webcam/webrtc`, `/webcam/snapshot.jpg`).
- Lets you pick the name shown in the UI.

## Configuration

- **Camera name in Fluidd/Mainsail** (default `Built-in`): whatever you want the tile
  called, for example `Built-in`, `Toolhead`, `Side`.

## Requires

- **Camera HW Accel**, which actually serves the stream. It is installed automatically as a
  dependency.

## Notes

Snapmaker U1. This plugin only registers the camera entry; the streaming itself comes from
Camera HW Accel.
