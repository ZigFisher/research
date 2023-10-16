---
template: main.html
description: This is a blank template for the pages we create
---

![OpenIPC Logo](https://openipc.org/assets/openipc-logo-black.svg)

## Welcome to OpenIPC !

### vdec-i386

The main intention of vdec-i386 is to test/debug the udp streams created from venc and majestic.

Currently it can gather the stream from one of the encoders and creates a generic rtp stream that can be viewed with gstreamer.

The usage for testing:

```
./vdec 5600 192.168.1.10 6000 
gst-launch-1.0 udpsrc port=6000 ! h265parse ! avdec_h265 ! autovideosink sync=false
```
