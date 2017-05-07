# Esp-radio for Adafruit Huzzah and VS1053 breakout board

This project is a small modification to the
[Esp-radio](https://github.com/Edzelf/Esp-radio) project so it works on
Adafruit Huzzah ESP8266 and Adafruit VS1053 breakout boards.

Not all features of the original project are supported.

* TFT display -- disabled via conditional USETFT
* buttons     -- disabled by adding conditional USEBUTTONS
* web UI      -- Works and eliminates the need for the display and buttons.

## Getting started

Read Esp-radio.pdf for the details on setting up the Arduino IDE. In
particular, be sure to install the ESP8266 Sketch Data Upload utility so you
can upload the radio.ini file. And be sure to install all the required
libraries. The TFT library is not used in this project so you can skip that
step.

## Hardware hookup

Adafruit VS1053        |ESP8266    |Audio jack |Description
-----------------------|-----------|-------|----------------------
VCC                    |V+ (5V USB)|       |
GND                    |GND        |       |
CLK                    |#14        |       |SPI clock
MISO                   |#12        |       |SPI MISO
MOSI                   |#13        |       |SPI MOSI
CS                     |#5         |       |SPI CS VS1053
RST                    |RST        |       |Reset
XDCS                   |#16        |       |Data/Command select
SDCS                   |#15        |       |SPI CS uSD card slot
DREQ                   |#4         |       |VS1053 interrupt
AGND                   |           |Center |
LOUT                   |           |Left   |Left audio channel
ROUT                   |           |Right  |Right audio channel

