# Materials List

## Printing

PETG or ABS is reccomended. The tensioning mechanisms and motor mount can warp over time if printed with PLA.

## Nuts/Bolts:

An exact list of required fasteners is coming in the future.


* 5x M5x30mm Bolts
* 3x M3x30mm Bolts
* 1x M3x15mm Bolt
* 5x M5 Nuts
* 4x M3 T-Nuts
* Assorted M3 bolts + nuts

https://s.click.aliexpress.com/e/_sIpZ55

## Frame:

The X-Axis runs along a V-Sot 2040 aluminum extrusion. The longer the extrusion, the more travel distance you will have.

The slider assembly takes approximatly 120mm off of the travel distance.

So a 500mm extrusion will give you approximately 380mm of travel.

https://s.click.aliexpress.com/e/_sMJLWJ



## Roller Carriage Wheels

3x V-Slot or T-Slot roller wheels are used for the X-Axis roller carriage.

For T-Slot rail,  3x Option B or similar roller wheels are used: https://s.click.aliexpress.com/e/_rJTbgF



## GT2 Belt
GT2 6mm belt is used.
The length of belt you will need for the X-Axis is double the length of the extrusion that you're using for the X-Axis plus 50mm.
So for a 500mm extrusion, you need 1050mm of belt to have enough.

The Y-Axis and Z-Axis use 250mm GT2 belt loops. The tensioning system will work with 250mm to 264mm long belt loops.

https://s.click.aliexpress.com/e/_rQ35Lp

https://s.click.aliexpress.com/e/_sOoTyx



## Bearings:

Bearings used are 608RS. 8mm inner diameter, 22mm outer diameter, 7mm thick.

Like these:

https://s.click.aliexpress.com/e/_s3uaUI


## Electronics:

An SKR 1.3 is used as the main controller.
TMC2130 drivers are used for the motors.
A 12864 LCD (RepRapDiscount Full Graphic Smart Controller) is used for a display, and local controls with SD functionality.

SKR 1.3 Mainboard with LCD controller and motor drivers:

https://s.click.aliexpress.com/e/_sN61d8

SKR 1.3 without LCD:

https://s.click.aliexpress.com/e/_sc29Y2


There are a LOT of alternatives for motion control. An SKR is chosen due to how versatile the board is and because it offers turn-key support for features like sensorless homing.

You can save a lot of money by opting for a different control board or creating your own controller setup. If you're the DIY type, you could create an amazing low cost control system using an ESP32. Or you use basically any 3D printer control board, or even an Arduino UNO.


## Motors
Nema 17 motors are used. One motor is needed for each axis. If you just want X and Y motion, you will only need two motors. 
You do not need very powerful motors for most use cases. 

If you expect to do vertical movements with a heavy DSLR, or rapid back and forth movements with high acceleration, invest in more powerful motors. For a USB camera, cellphone, action camera or PiCamera you can get away with pancake motors.

https://s.click.aliexpress.com/e/_sd4SLV









---------------------------------------------
----
----------------------------------------------
----
----------------------------------------------


# OpenSlider Legacy (Older Versions)
Arduino UNO + GRBL1.1 Shield for motion control.

This is the current control board setup used:
http://osoyoo.com/2017/04/07/arduino-uno-cnc-shield-v3-0-a4988/

I purchased mine through Aliexpress, though it is a widely available setup. You can find this Uno + CNC shield kit on most online retailers, like Amazon, eBay, etc.

There are many other boards available that will accomplish the same thing. The reason I chose the UNO + 4x A4988 setup is because it is extremely affordable, simple to use and it's widely available.

It is possible to also use other stepper drivers instead of the standard A4988. For example, you could upgrade to the TMC2130 for interpolated microstepping and quieter operation. If you are going to use audio from a device mounted directly to the slider, I suggest using TMC2130 drivers to reduce motor noise. I chose A4988 due to the incredibly low cost.

Three NEMA 17 stepper motors are used for motion control. Virtually any NEMA 17 motors will work, as long as they are not extremely low power, or extremely overpowered. I suggest NEMA motors rated to at least 20Ncm.

The software utilized is GRBL, and Universal GCode sender (UGS). GRBL is flashed to the Arduino, and UGS is used to send commands to the Arduino from a connected device.

## Software (Legacy)

GRBL: https://github.com/gnea/grbl/wiki
UGS: https://github.com/winder/Universal-G-Code-Sender

## Belts (Legacy)
The slider uses GT2 timing belts with 2mm pitch. You can use 6mm or 8mm width belts, whichever you prefer. The X-Axis requires one long piece of belt, and the other axis require 250mm continuous belts. You can make continuous belts by attaching the ends of a straight piece of belt cut to the right size, with an adhesive like CA glue.

## Electronics: (Legacy)
3x Nema 17 Stepper Motor
1x Arduino UNO + 4 Axis CNC Shield
4x A4988 Stepper Motor Driver
1x 12V 5A Power Supply