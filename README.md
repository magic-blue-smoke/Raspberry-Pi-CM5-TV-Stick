# Raspberry Pi CM5 TV Stick
Raspberry Pi CM5 that plugs directly to TV/monitor!

## Availability
Raspberry Pi CM5 TV Stick is available for purchase at [Makerfabs](https://www.makerfabs.com/raspberry-pi-cm5-tv-stick-lite.html)

Follow on X: [@magic__smoke](https://twitter.com/magic__smoke)

## Specs
- Compatible with Raspberry Pi CM5 Lite and eMMC variants
- HDMI plug
- Micro SD card connector
- USB-C connector for data/power
- Two USB3.0 USB-A connectors
- IR receiver
- User button
- Power button
- RPI_nBOOT button for CM5 eMMC programming
- Fan connector
- Power and Act LEDs
- Connector for Ambilight-like lightning with WS2812 or WS2801 LEDs (GND, GPIO18, GPIO10 and GPIO11)

## Description
### HDMI plug
The board has HDMI Type A plug and routed to CM5 HDMI0 port

### Micro SD card connector
Micro SD card connector accepts Micro SD card

**Important**: don't insert SD card if using CM5 with eMMC, as SD card and/or CM5 can be permanently damaged (eMMC and SD card connector are sharing same SoC pins)

### USB-C connector
USB-C connector is used to provide power to TV Stick. Consider using Raspberry Pi 5 power adapter or known good power supply for Raspberry Pi 5

USB-C connector also has CM5 USB2.0 data lines

### USB3.0 USB-A connectors
Raspberry Pi CM5 TV Stick has two USB3.0 ports. Power output has current limiting switch

### IR receiver
IR receiver is connected to CM5 GPIO17. 
To enable IR receiver following line has to added to `config.txt` file: `dtoverlay=gpio-ir,gpio_pin=17`

[This article](https://devkimchi.com/2020/08/12/turning-raspberry-pi-into-remote-controller/) describes further remote pairing/learning (omit parts describing IR TX and make sure to still use 'dtoverlay=gpio-ir,**gpio_pin=17**') 

### User button 
User button is connected to GPIO14. When used, has to be configured as active low, input pull-up

### nBOOT button
With USB2.0 routed to USB-C connector, board can be used:
- in "gadget mode" as USB Mass Storage Device, Ethernet Adapter, etc.
- to programm CM5 eMMC flash by entering USB boot mode. To boot CM5 through USB, the nBOOT button must be pressed at the time of connecting power


