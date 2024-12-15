# 737-CDU
Replica 737 CDU for use with mobiflight. WORK IN PROGRESS

Repository for the files needed for building your own Boeind 737 CDU for use with mobiflight.
Designed to be as accurate as possible (without drawings) to the real thing.
**Early initial release, not yet complete.** Some of the buttons are need reworking, the PCB needs a rework to simplify it and add more mounting options.

Gerbers, BOM and placement files provided for ordering PCB from JLCPCB.
STLs provided for both (required) FDM and resin printing.

PCB has been tested working and has been coded in mobiflight; yet to be tested in SIM. The PCB was designed for redundancy and can be ordered preassmbled with some surface mount components, or can be ordered bare and fitted with through hold components. Provision is also made for powering arduino from 12V supply for isolation, but it's not required. LED backlighting can be controlled via arduino or powered directly from a PWM supply (just remove the MOSFET and solder the PWM leads to the LED+ve and LED-ve through holes).

Print FrontFrame.stl and Handle.stl on an FDM printer, all buttons to be printed in resin. Ensure there are no supports within the hollow buttons as they are designed to be backlit.

Due to design oversight, there is currently no way to mount the LCD driver board to the unit. For now you will need to create your own mount and affix it with adhesive.

Requires:<br>
72 6x6x7mm tactile switches with LEDs. There are 71 tactile buttons and the remaining one is canibalized for the LED, to simplify the backlight design process, a later release will remove this requirement by redicing the LED strings from 4 to 3 and using a properly selected resistor.<br>
3 white 6mm LEDs, 1 green 6mm LED and 1 Yellow 6mm LED<br>
1 4 pin male JST header with 2mm pitch. A 4 wire jumper of sufficient length to reach the LED driver board will also be needed. Optionally a 5.5mm female barrel jack connector can be installed and the board supplied from a second 12V (center positive) supply.

**CAUTION** The resistor on the power supply branch of LED backlight of 'Brightness Adjust Buttons' and 'Exec' need to be change to 180ohm because of you still use 1ohm resistor, the light may work overload with shorter lifetime.
