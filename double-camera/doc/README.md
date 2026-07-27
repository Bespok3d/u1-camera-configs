# Double Camera

Two views of the same print: the printer's built-in camera and a USB camera you plug in yourself.

## What it installs

| Plugin | What it does |
| --- | --- |
| Camera HW Accel | Encodes the video on the printer's video chip, so streaming barely touches the CPU |
| Built-in Camera | Shows the printer's built-in camera as a tile in Fluidd and Mainsail |
| USB Camera | Shows a camera you plug into the printer's USB port as a second tile |

All three install together with a single service restart.

## Before you install

Plug the USB camera in first. It needs to be a UVC camera (the kind that works on a computer with no
driver); almost every USB webcam is.

## After installing

Open Fluidd or Mainsail and both tiles are there. If the USB tile is blank, check the camera is
plugged in and reload the page. Each tile's name comes from its own plugin's settings, so you can
tell the two apart however you like.
