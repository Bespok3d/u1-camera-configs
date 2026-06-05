# Remote Screen Tile (Fluidd/Mainsail)

Shows the Remote Screen mirror as a tile inside Fluidd and Mainsail, next to your cameras,
instead of opening it in a separate browser tab.

## What it does

- Adds a Moonraker `[webcam]` iframe entry that embeds the remote screen, sized for the
  U1's 480x320 display.

## Requires

- **Remote Screen**, which serves the mirror at `/screen/` (installed automatically).

## Notes

Snapmaker U1. This is a convenience tile only; the mirroring and touch input come from the
Remote Screen plugin.
