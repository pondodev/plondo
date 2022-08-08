# bootloader

to flash the bootloader onto your atmega32a, you need to have some sort of in system programmer (ISP) such as a usbasp
programmer or an arduino. if you don't have one, they're pretty cheap online.
[this is the one that i use](https://core-electronics.com.au/usbasp-usbisp-3-3v-5v-avr-programmer.html), but any ISP
capable of programming AVR chips will do.

next, clone [my fork of usbasploader](https://github.com/pondodev/USBaspLoader) locally and make sure to change the
`PROGRAMMER` variable in `Makefile.inc` to be the programmer that you're using. then simply connect your ISP to your
computer and to the ISP header (J1) on the PCB and run `make fuse && make flash`.

once you're done here, move onto [flashing and testing your PCB](4-flashing.md)

