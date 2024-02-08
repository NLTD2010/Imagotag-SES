# Imagotag 2.6 BWR GL420 hacking

![image](https://github.com/NLTD2010/Imagotag-SES/assets/77970269/60861abd-a7d4-4000-b9e1-93f330c38c14)
> I have bought this from shopee, 2.6 price tag
## Chips used

- [CC2510 - MCU + Radio - 8051](../../raw/master/doc/cc2510.pdf)
- [NT3H2111 - NFC](../../raw/master/doc/NT3H2111_2211.pdf)
- [GDEW0213Z16 - 2.13" EPD display](../../raw/master/doc/GDEW026Z39.pdf)
- It uses [IL0373](../../raw/master/doc/IL0373.pdf) driver
- [TPS61071 - boost converter](../../raw/master/doc/tps61071.pdf) - used (only?) for white LED 
- [W25X10CL - Winbond 1Mbits NOR SPI flash](../../raw/master/doc/w25x10cl.pdf)

## CC2510 connections

### Port 0
- P0:0 - EPD power enable (active low via a P channel fet)
- P0:1 - EPD CS (SPI interface chip select)
- P0:2 - debug port
- P0:3 - EPD SDI (SPI interface serial data in)
- P0:4 - SDA to NFC chip
- P0:5 - EPD CLK (SPI interface clock)
- P0:6 - SCL to NFC chip
- P0:7 - *not connected*

### Port 1
- P1:0 - NFC VCC (seems to power NFC chip and SPI flash)
- P1:1 - NFC FD (field detection)
- P1:2 - EPD DC (data/command select for display)
- P1:3 - EPD BUSY (detect if display busy)
- P1:4 - SPI flash CS 
- P1:5 - SPI flash CLK
- P1:6 - SPI flash MOSI
- P1:7 - SPI flash MISO

### Port 2
- P2:0 - EPD Reset (display reset)
- P2:1 - debug data and white LED
- P2:2 - debug clock and LED boost chip enable (TPS61071)
##### nah, i'm still working on this stuff thing
