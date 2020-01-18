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

## Kit Contents

If you are unable to obtain the CamJam EduKit, then the following is a list of the kit contents:

* 400 point mini breadboard
* 1 x red LED
* 1 x yellow LED
* 1 x green LED
* 1 x push button
* 1 x buzzer
* 3 x 330Ω resistors
* 1 x 4.7kΩ resistor (not used by these worksheets)
* assortment of jumper wires (6 x M/F, 2 x M/M used by these worksheets)

## Preparation

Firstly, you will need to prepare an SD card with BMC64 by following [these instructions](https://accentual.com/bmc64/).

To enable the user port, you will need to add:

	gpio_outputs_enabled=true

to your `cmdline.txt` file.

Your Raspberry Pi will boot into C64 mode by default, which is what the worksheets assume.  You need to specify that you are using the Raspberry Pi GPIO pins for the user port by going into the settings menu (F12), selecting `Prefs` and then `GPIO Option` and use the right/left cursor keys until `#4 (Userport+Joy)` is selected.

## Saving Programs

In order to save your programs, first create a disk.  Go into the settings menu (F12), select `Drives` and `Create Empty Disk`. If you are unfamiliar with disk drive types, then select `D64` here and give your new disk a suitable name (such as `CamJam-EduKit1`).

Once you have a suitable disk, select `Drive 8` and `Attach Disk` and select the disk you created above.

To save a program as `1 HELLO WORLD`, use the following command:

	SAVE "1 HELLO WORLD",8

The `,8` is because you selected `Drive 8` when attaching the disk.

Always verify that you saved the program successfully using:

	VERIFY "1 HELLO WORLD",8

If you get a `VERIFY ERROR`, this might be because the program already exists on the disk.  If you want to replace it, then you need to add `@:` to the filename like this:

	SAVE "@:1 HELLO WORLD",8

## Worksheets

[CamJam EduKit1 on BMC64](https://github.com/markbush/EduKit1/blob/master/EduKit1.pdf)