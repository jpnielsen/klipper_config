
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
Raspberry Pi 3B
----------------------------












