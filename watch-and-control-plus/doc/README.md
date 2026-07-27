# Watch and Control Plus

Everything for watching and running the printer from somewhere else, plus a video of the finished
print.

## What it installs

| Plugin | What it does |
| --- | --- |
| Remote Screen | Mirrors the printer's touchscreen to your browser and sends your taps back |
| Camera HW Accel | Encodes the video on the printer's video chip, so streaming barely touches the CPU |
| Built-in Camera | Shows the printer's built-in camera as a tile in Fluidd and Mainsail |
| USB Camera | Shows a camera you plug into the printer's USB port as a second tile |
| Timelapse | Adds the Timelapse menu to Fluidd and Mainsail, so a print can be recorded as a video |

All five install together with a single service restart.

## Before you install

Plug the USB camera in first. It needs to be a UVC camera (the kind that works on a computer with no
driver); almost every USB webcam is.

## After installing

Both camera tiles and the screen tile are in Fluidd and Mainsail. The screen is also on its own page
at `http://<printer-ip>/screen/`, which installs as an app on a phone or tablet. A Timelapse menu
appears in Fluidd and Mainsail, where you turn recording on and find the finished videos.

Want less than this? "Watch and Control" is the same without the USB camera and the timelapse;
"Double Camera" is the two cameras on their own.
