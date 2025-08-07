# FW.bin(Embedded)
      This was an embedded system CTF challenge. I was given a microcontroller and I had to extract the flag from its Flash memory. The flag was stored within the flash memory of an ATmega328P.
    1.I connected the device and used the following command "avrdude -p m328p -c arduino -p/dev/ttyUSB -b 115200 -U        flash:r:firmware.hex:i" to create firmware.hex file from device flash memory
    2.To make it easier and to analyze the contents of the firmware, I converted the intel hex file to raw binary using         "avr-objcopy -I ihex firmware.hex -O binary firmware.bin"
    3.Atlast I used "strings firmware.bin | grep -i flag" to get the flag and it was displayed {1_4m_7h3_fl46}
## TOOLS USED
    >avrdude
    >strings-command tools
    >grep-command tools
    >avr-objcopy
