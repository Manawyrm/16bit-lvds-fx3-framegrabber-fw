# Cypress FX3-based 16bit LVDS Framegrabber (Firmware repo)

![Framegrabber PCB with FX3 SuperSpeed Explorer Board](https://screenshot.tbspace.de/mbleyntaqgj.jpg)

### Overview

The 16bit-LVDS-FX3-Framegrabber is a Cypress FX3-based PCB, which can digitize a parallel 16bit digital video stream from a commercial image sensor.
It exposes a USB 3.0 UVC ("webcam") device to the operating system. 
The current state of the firmware/GPIF II configuration is fixed to 1024x1024px, 16bit dynamic range.

Due to limitations in USB UVC descriptor/color format support, this firmware reports itself to the OS as a YUYV/YUV2 device, in other words a 16bit per pixel color video signal.
This will create wrong color images when viewed on regular software (like VLC Media Player), the raw stream can be viewed & interpreted using Video4Linux, GStreamer, etc. though.

### Additional info 
[Hardware design files](https://github.com/Manawyrm/16bit-lvds-fx3-framegrabber)  

### Errata
None so far. Rev. A works well.
