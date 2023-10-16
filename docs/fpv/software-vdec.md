---
template: main.html
description: The vdec
---

![OpenIPC Logo](https://openipc.org/assets/openipc-logo-black.svg)


## The vdec


### vdec

Component for flashing OpenIPC Ground Station based on NVR with HI3536DV100/HI3536EV100 processors


### vdec-nvr-20231014

The latest stable version of vdec for NVR before switching to LVGL for OSD display.


### vdec-i386

The main intention of vdec-i386 is to test/debug the udp streams created from venc and majestic.

Currently it can gather the stream from one of the encoders and creates a generic rtp stream that can be viewed with gstreamer.

The usage for testing:

```
./vdec 5600 192.168.1.10 6000 
gst-launch-1.0 udpsrc port=6000 ! h265parse ! avdec_h265 ! autovideosink sync=false
```


### Files for download

- https://github.com/OpenIPC/silicon_research/releases/tag/latest