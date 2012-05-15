CatNip - LPC1343 Developement board
======

This is a derivative work of microbuilder’s LPC1343 Reference Design http://www.microbuilder.eu/projects/LPC1343ReferenceDesign/

The design is aimed at creating a platform that enables to create USB enabled devices quickly and efficiently. The board is optimised for creating devices which will be contained within a case. 

The main differences from microbuilder’s design:
 - USB connection header is added in order to facilitate adding an external case - mounted USB connector that is placed far away from the board
 - RESET pin is in a breakout in order to allow putting a reset button on the device case.
 - power is connected via screw terminals
 - eeprom in SO8 package is used as it’s more common
 - separate power header is added to export regulated and incomming voltages to daughter boards
 - most of 3.3V and GND connections removed from breakout as it encourages ground loops, GND connections are left near communication pins (SPI, I2C, RXTX) for easier prototyping, 3.3V connection is left near ADC inputs as it’s handy to limit ADC input to 3.3V by adding a diode
 - All UART pins except RX and TX are reclaimed (who uses UART anyway?:)
 - More ADC pins added
 - LED pin is added to header
 - JTAG connector removed and it’s pins reclaimed for GPIO/ADC
