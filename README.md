# Rotilio

**Production ready** Internet of Things (IoT) open source hardware and software platform

With WiFI and GPRS/3G/LTE connectivity, **Arduino compatible** FreeRTOS [Particle.io](http://particle.io) chip.

Fully loaded with common use **sensors and actuators**.

Multiple communication channels: **WiFI, USB serial, TTL serial, RS485 serial**.

Ready made firmware with Web and Mobile user interface for out-of-the box operation, **no coding** necessary to start.

**Secure** cloud communication for everyday operations and OTA firmware updates.

![Rotilio, piattaforma IoT hw e sw open source](./images/tm_rotilio.jpg "Rotilio")

## Technical datasheet v1.0


### Pin out

```
A0 		- Buzzer
A1 		- Photoresistor
A2 		- Trimmer
A3 		- Free
A4 		- MAX485
A5 		- MAX485
A6 		- Free
A7 		- Free
D0 		- I2C SDA (on board temperature, umidity, pressure sensors)
D1 		- I2C SCL (on board temperature, umidity, pressure sensors)
D2 		- P1, user button 1
D3 		- RELAIS RESET (bistable only OFF)
D4 		- RELAIS SET (monostable on/off - bistable ON)
D5 		- Switch
D6 		- P2, user button 2
D7 		- Free (on board blue led)
TXD		- SERIAL TTL TX
RXD		- SERIAL TTL RX
RS485A	- RS-485 Serial A
RS485B  - RS-485 Serial B
RST		- Reset
Vbat	- Backup battery (+3 V) for RTC clock in sleep mode
+5V		- +5V power supply
+3.3V	- +3.3V power supply
GND		- Ground
```
See [Pinout](https://github.com/techmakers/rotilio.cc/raw/master/hardware/ROTILIO_PINOUT.pdf)

### Input

```
Photoresistor 		- Resolution 12 bit (A1)
Trimmer 			- Resolution 12 bit (A2)
P1 					- Resolution 1 bit (D2)
P2 					- Resolution 1 bit (D6)
Switch 				- Resolution 1 bit (D5)
Temperature1		- Si7020 (I2C - D0&D1) - precision 0.1°C
Umidity 			- Si7020 (I2C - D0&D1) - precision 1%
Temperature2		- MS5673 (I2C - D0&D1) - precision 0.1°C
Pressure/Altitude	- MS5673 (I2C - D0&D1) - precision 1 mbar
```

### Ouput

```
Relais 		- Mono (D4) or bi-stable (D4&D3) 
Buzzer 		- Resolution 1 bit (A0)
RGB Led 	- Resolution 8 bit/color (Photon)
Blue Led	- Resolution 1 bit (D7)
```

### Communication

```
WiFI		- Broadcom BCM43362, 802.11b/g/n Wi-Fi, open, wep, wpa wpa2
or
CELLULAR 	- GPRS/3G/LTE Global data plan


RS485 		- MAX485 Chip (A4/A5)
SERIAL TTL 	- Serial TTL (RXD - TXD)
I2C			- (D0&D1)
Mini USB B	- RS-232 over USB
```

### CPU & Memory

```
CPU			- STM32F205 120Mhz ARM Cortex M3
Memory		- 1MB flash, 128KB RAM
```

### Power supply

```
+5V
+3.3V
Mini USB
80 mA, 160 microA in deep sleep mode (Photon only)
from 3 microA to 450 mA
```

### Firmware

```
Standard Arduino compatible
FreeRTOS based
OTA firmware update via cloud
HTTPs Restful Cloud API
Automatic application interface configuration
```

### User interface
See [https://rotilio.cc](https://rotilio.cc)

```
WEB and Mobile user interface
HTML5+CSS+JS with AngularJS, Twitter Bootstrap, ChartJs
PhoneGap ready
User authentication
Fully customizable
```

### Phisical dimension

```
70x70x20 mm
```

### About us

Rotilio is proudly crafted and developed in Genova by [Techmakers srl](http://techmakers.io), a startup for Internet connected industrial and consumer products.


### Open source MIT Licence

Copyright (c) 2015 Techmakers srl

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
