
Klipper printer.cfg for modified ANET A8 Printer.

This is a work in progress.



- Lerdge optical endstops on X,Y,Z and Z1
- Printed mounts for optical endstops of own design. Not ready for sharing.
- 220V 750W printbed heating element glued to underside of stock hotbed.
- FOTEK Solidstate relay for printbed heating element pwm power control.
- Thermal fuses 120C
- Spring steel PEI + magnetic sticker on heated printbed.
- Printed carriage. Thingiverse #######
- non-e3d Titan extruder 2.85 mm filament
- Nema 17 pancake stepper for extruder (12V).
- Adjustable DC-DC buck converter (24V to 12V) powers mcu board#2
- non-e3d Volcano hotend


----------------------------
mcu board #1: MKS Robin E3D
---------------------------

- Stepper X: X (24V)
- Stepper Y: Y (24V)
- Stepper Z: Z (24V)
- Stepper E: Z1 (24V)

- Optical Endstop X-
- Optical Endstop Y-
- Oprtical Endstop Z-
- Oprtical Endstop Z1-

- 24V fan for extruder heatsink
- 24V fan for extruder part cooler

----------------------------
mcu board #2: ANET v1.7 
----------------------------
- Stepper X: Extruder (12V)
- Bed: connects to SSR for 220V 750W printbed heating element
- HE: connects to MOSFET driver board for hotend heating element.
- Thermistor probe hotend
- Thermistor probe bed heater 


----------------------------
Flashing mcu board #1: Robin E3 (/dev/ttyUSB0) the cards end up having the same ID - so /dev/serial/by-path/ is used in "printer.cfg"
----------------------------

MKS Robin E3 boards. To use this config, the firmware should be compiled for the STM32F103.
When running "make menuconfig", enable "extra low-level configuration setup", select the 20KiB bootloader, and serial (on
USART1 PA10/PA9) communication.

Note that the "make flash" command does not work with MKS Robin
boards. After running "make", run the following command:
  ./scripts/update_mks_robin.py out/klipper.bin out/Robin_e3.bin
Copy the file out/Robin_e3.bin to an SD card and then restart the
printer with that SD card.

----------------------------
Flashing mcu board #2: ANET v1.7 
----------------------------

avrdude -p atmega1284p -c arduino -b 115200 -P /dev/ttyUSB1 -U out/klipper.elf.hex

avrdude: AVR device initialized and ready to accept instructions

Reading | ################################################## | 100% 0.00s

avrdude: Device signature = 0x1e9705 (probably m1284p)
avrdude: NOTE: "flash" memory has been specified, an erase cycle will be performed
         To disable this feature, specify the -D option.
avrdude: erasing chip
avrdude: reading input file "out/klipper.elf.hex"
avrdude: input file out/klipper.elf.hex auto detected as Intel Hex
avrdude: writing flash (27940 bytes):

Writing | ################################################## | 100% 3.56s

avrdude: 27940 bytes of flash written
avrdude: verifying flash memory against out/klipper.elf.hex:
avrdude: load data flash data from input file out/klipper.elf.hex:
avrdude: input file out/klipper.elf.hex auto detected as Intel Hex
avrdude: input file out/klipper.elf.hex contains 27940 bytes
avrdude: reading on-chip flash data:

Reading | ################################################## | 100% 3.04s

avrdude: verifying ...
avrdude: 27940 bytes of flash verified

avrdude: safemode: Fuses OK (E:00, H:00, L:00)

avrdude done.  Thank you.


----------------------------
Raspberry Pi 4
----------------------------












