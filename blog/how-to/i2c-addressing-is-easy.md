# I2C addressing is easy<br>_Reading data sheets is hard_

## What's the problem?

Almost every project I've worked on which has an I2C peripheral has had problems with I2C addressing.
I2C addressing is easy.
There are 7 bits in the address.
The address for the device you are talking to is hard-coded.
The address is stated in the data sheet or user manual.

Okay, there is a bit more to it than that.
- 10 bit addresses
  - There are some devices with 10 bit addressing. I have not met one in the field yet.
- SW configured
  - An MCU with an I2C target block may have a SW configured device addres.
- OTP (one time programmable) or NVMEM (non-volatile) configurable address
  - Devices like the  have software settable device address.
  - Microchip ATECC608B
- HW address select pins
  - some devices have several address select lines.
  - The TI TCA9548ALow-Voltage8-Channel I2CSwitchWithReset has A0-A2, three select lines, so the address can be any from 0x70 through 0x77

Every board I have touched has had either an I2C peripheral, some of the ones I have encountered include

- IMU
- image sensor
- EEPROM
- flash
- custom logic in CPLD or FPGA
- LED controller
- PMIC
- CAC (crypto authentication chip)

As I say, it's never easy, someone on the team always goofs up somewhere on a new board.

## So why do we get problems?

Taking the simplest 7 bit addresses, without any HW selectable address bits, not SW changeable, we still hit two fundamental problems.

1. Description - How the address is specified
1. Usage - How the software expects the address.


## Description on the schematic

There is no obligation for the board designer to annotate the schematic with the I2C address of a device placed on the board.
When the designer does include this detail it may not be in an intuitive location.
It might be 
- adjacent to the peripheral
- tabulated on the same page as the peripheral
- tabulated on the interconnects page
- tabulated on first or last page
- rely on data sheet

The designer will use one of two formats for an I2C address

- 7 bit address
- 8 bit combined address + read write

Whatever is on the schematic may be at the mercy of a drop in replacement that is pin compatible, but not address compatible.


## Description in the data sheet

This is where things get really fun.
Just looking at several vendor data sheets we can see that the address is not always obvious.

### Bosch



### 

