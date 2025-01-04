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

### Credits

Firmware based on the excellent work of Gaurav Singh in the [PE1005_USB3_camera](https://github.com/circuitvalley/PE1005_USB3_camera).  
https://www.circuitvalley.com/2020/02/diy-usb-3-1080-full-hd-camera-PE1005-auto-focus-optical-zoom-cypress-fx3-usb.html

### Licensing

Cypress released their SDK examples licensed as  
`All Rights Reserved, UNPUBLISHED, LICENSED SOFTWARE, CONFIDENTIAL AND PROPRIETARY INFORMATION`.  
The `PE1005_USB3_camera` repo was licensed as GPLv3, this repo should also be held "in spirit" of GPLv3.
