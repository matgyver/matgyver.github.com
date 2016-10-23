---
layout: page
title: StratuX Project
tagline: Aviation
category: aviation, stratux, projects
tags: [aviation, aircraft, stratux, raspberry pi, SDR]

bigimg:
  - "/aviation/stratux/img/power_boost.JPG" : "Adafruit PowerBoost 1000"
  - "/aviation/stratux/img/kerbos.jpg" : "OLED test with KerbOS"
  - "/aviation/stratux/img/hello.jpg" : "OLED test with Hello World!"
  - "/aviation/stratux/img/usb_power.JPG" : "Power measurements StratuX"

---
StratuX
=============

StratuX is project that allows a person to build a ADS-B receiver.  It should be noted that this is just a receiver, it has no transmit abilities at all.  This is the reason that this is a cheap way to receive ADS-B traffic and weather information into the cockpit.  

For more information about StratuX and see where the development of the software is, I highly recommend that you go to the [StratuX website](http://stratux.me/).  You can see the latest news and download the latest version of StratuX.

To build a StratuX reciever you will need at least the following items:

* Raspberry Pi 2 or 3
* WiFi dongle (not needed with the Pi 3)
* SDR that is compatabile with the RTL-SDR (RTL2832U)
* 8 GB or higher SD Card (should be Class 10)
* 5 VDC Power Supply (Can be battery pack, more on this later)

You can also add additional equipment that can provide some other functions as well.  This items are listed below.

* WAAS Enabled GPS
* IMU Unit (available on RY835AI GPS)
* Additional SDR reciever (for dual band operation)

We will talk about some of these features and their impact on the system later on.

Power consideration
-----
Power was one of the first things I wanted to look into and change with how many StratuX systems were doing.  Most systems was relaying on an external battery.  These are typically used to charge cell phones and tablets and provide 5 VDC and usually have a fairly large capacity (10,000 mAh or higher).  But there is a problem.  Let's talk about the USB specification for providing power.

The USB Specifications state that the voltage on USB shall be between 5 VDC plus or minus .25 VDC.  The Raspberry Pi follows this specification and must be supplied with a power source that matches it.  If it does not stay in that range, then the Raspberry Pi may "brownout" which may be poor performance or it may just reboot.  The problem with some battery packs though, is that under heavy load they may not maintain the correct voltage.  This is not usually a large problem for most charging applications which they are designed for.  But for the Raspberry Pi it can be bad.

There is also the issue of needing to carry an external battery pack with you.  It would be bettery if the battery was built into the case.

More to come later...