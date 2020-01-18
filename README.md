# CamJam Edukit 1

The code contained within this repository is for use with the CamJam Edukit 1, created by the organisers of The Cambridge Raspberry Jam (http://camjam.me), an event for fans of the Raspberry Pi.

The worksheets are written for those using [BMC64](https://github.com/randyrossi/bmc64) running in C64 mode with the user port enabled.  The code should work in C128 mode without modifications.  They should also work in VIC20 and PET modes, however you will need to replace the locations of the user port and data direction register (DDR) in each program as follows:

Model | User Port | DDR
------|-----------|------
C64   | 56577     | 56579
C128  | 56577     | 56579
VIC20 | 37136     | 37138
PET   | 59471     | 59459

The kit costs only £5 including UK VAT, and is available from [The Pi Hut](http://thepihut.com/collections/camjam-edukit)