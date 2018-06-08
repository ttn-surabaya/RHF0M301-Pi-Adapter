# RisingHF RHF0M301 - Raspberry Pi Adapter

This is a simple adapter / backplane for RisingHF RHF0M301 LoRa Gateway and Raspberry Pi 2/3. 

More info about [**RHF0M301 LoRa Gateway**](http://www.risinghf.com/product/rhf0m301/?lang=en)<br>

## Configuration

The following pin configuration is used on this board (v1.1)

RHF0M301 pin    | Description   | RPi physical pin
----------------|---------------|-----------------
1,2             | Supply 5V     | 2
3,4,21,22,23    | GND           | 6
14              | Reset         | 22
16              | SPI CLK       | 23
15              | SPI MISO      | 21
18              | SPI MOSI      | 19
17              | SPI NSS       | 24

There is a jumper select pin to change the RHF0301 power source from either Rpi 5V or External 5V. You also could add GPS (UBlox Neo M6/M7/M8) on this board or just leave it empty.

## LoRa Packet Forwarder Installation

There are a couple of packet forwarder software libraries that you could use for this RPI - RHF0M301 LoRa Gateway for example:
* [**The Things Network Packet Forwarder**](https://github.com/TheThingsNetwork/packet_forwarder)<br>
* [**Official RisingHF Packet Forwarder**](https://github.com/risinghf/packet_forwarder)<br>
* [**Resin IO / TTN Packet Forwarder**](https://github.com/jpmeijers/ttn-resin-gateway-rpi)<br>

As you might notice, the RHF0M301 uses similar hardware as in other gateways such as IMST ic880a which is based on Semtech SX1301. The software is pretty much the same but usually they vary in pinout (i.e. Reset Pin).

If you wish to use this gateway for The Things Networks Environment, then I suggest you to follow the [**IMST ic880a Instruction at TTN Official Github page**](https://github.com/TheThingsNetwork/packet_forwarder/blob/master/docs/INSTALL_INSTRUCTIONS/IMST_RPI.md)<br>.
It will work straight away as the wiring configuration is identical.

## Revision History
* v1.0 Initial Design
* v1.1 Changed Reset Pin to Pin 22, added filter circuit on reset line, changed caps on 5V power line. 
