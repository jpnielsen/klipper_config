Klipper 3D configuration


This is a work in progress.





Klipper printer.cfg for modified ANET A8 Printer.

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

Stepper X: X (24V)
Stepper Y: Y (24V)
Stepper Z: Z (24V)
Stepper E: Z1 (24V)

Oprtical Endstop X-
Oprtical Endstop Y-
Oprtical Endstop Z-
Oprtical Endstop Z1-

Solid state relay for 220V 750W printbed heating element

3D touch probe

24V fan for extruder heatsink
24V fan for extruder part cooler

----------------------------
mcu board #2: ANET v1.7 
----------------------------
Stepper X: Extruder (12V)
12V fan for extruder stepper

----------------------------
Raspberry Pi 3B
----------------------------
ADXL345











