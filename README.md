# LPC824_MAX30102

Status: work in progress.

A simple UART interface to MAX30102 SPO2 sensor mounted on a breakout board (part GY-MAX30102) using NXP LPC824 MCU. 

The Maxim MAX30102 sensor uses 1.8V for digital logic and 3.1 - 5.25V for LED drive. To use with 3.3V/5V MCUs or dev boards like Arduino, a linear regulator is needed for MAX30102 sensor supply rails and level convertors for I2C SDA/CLK lines.

## GY-MAX30102

Marked as "GY-MAX30100" on PCB. Cannot find schematic. PCB incorporates LDO and level converters. Can operate at 3.3V to 5V.
INT pin needs pull up resistor (either external or enabled within the MCU).

Breakout board components

* "662K" 3.3V LDO (presumably for LED driver)
* "65K5" 1.8V LDO  (for digital logic)
* "702" 60V N-channel enhancement mode MOSFET (as logic level convertor)

Using FET for level shifting:

AN97055 Bi-directional level shifter for I²C-bus and other systems.
https://cdn-shop.adafruit.com/datasheets/an97055.pdf

Datasheets:

http://www.mikrocontroller.net/attachment/193855/LM6206N3.pdf
http://www.s-manuals.com/pdf/datasheet/2/n/2n7002dw_panjit.pdf
