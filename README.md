# LDM2-LED Display Board
Adapter board to drive HDSP-C2x1 common anode seven segment displays.  
## Overview
This board can be mounted underneath a HSDP-C2x1 display to allow easy driving via MCU.  
It uses a TPIC6C595 power shift register to control the display.  
Resistor values are selected for a 10 - 13V LED supply.  
Depending on module color it might be necessary to increase R8 for even brightness on the decimal point.
## Pinout
All logic pins require a 5V high level. 
- LED Drive: Input for 10 - 13V LED driving voltage.
- Digital VCC: Input for 5V logic supply voltage.
- Data IN: Serial data input to shift register.
- Data OUT: Serial data output from shift register.
- Register CLK: Clock for output register. Use to apply changes to display after data input.
- Serial CLK: Shift register clock for serial data input.
- GND: Digital and LED ground connection.
- Register CLR: Clear contents of shift register (active low).
- Output ENA: Enable the output of the register (active low).
Output ENA can be used for PWM dimming.
## Other
Published under CERN-OHL-S license.