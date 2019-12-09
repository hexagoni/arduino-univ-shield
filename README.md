# Battery Powered Arduino Nano Pro Sensors & Nrf24L01+ Shield

## Why this shield was designed

The possibility of using a small battery-powered Arduino as a node for various home automation purposes is obvious and is already used in practice.
I have always seen the challenge of projects in the following points:
 - battery operation as long as possible
 - space-saving design
 - wireless communication => with battery operation mostly logical conclusion
 - provision of the necessary voltage for the desired sensors

Based on these points I have developed a universal shield for the Arduino Pro Mini, which fulfills all above desired specifications of the project hardware by the space-saving arrangement of the required components.

## What can the Shield do?

The Shield should be universally applicable for all battery operated Arduino Pro Mini with the wish to communicate with the gateway or other nodes via 2.4 Ghz (Nrf24L01+).
It offers the following features:
 - Improved resource utilization of the battery (3.3V) by using a more
   powerful step-up
 - Space-saving design: dimensions incl. Arduino with    soldered male
   pins: 18mm x 46mm x ~ 40mm (total height depends on use    and
   selected components)
 - Support of 5.0V sensors (optional)
 - Higher number of GND & VCC pins Battery level control by voltage
   divider and fixed voltage decrease by pin A0
 - Direct power supply stabilized by capacitor (recommended 47µF) for
   all current outputs and the Nrf24L01+


### Images

![Schematic](https://github.com/hexagoni/arduino-univ-shield/blob/master/Schematic/Schematic.png)
![PCB](https://github.com/hexagoni/arduino-univ-shield/blob/master/PCB/PCB.png)

## What do I have to consider when using the Shield?

The board is designed for a total load of 1 Ampere at 3.3V resp. 5.0V. If higher currents or voltages are required for sensors, a separate power supply must be installed.

Further it is necessary to remove the internal voltage regulator of the Arduinos. The better 3.3V StepUp does its job. Removing the unused LEDs saves additional power. (Here you can read more about the power saving measures: https://www.mysensors.org/build/battery)

## Which components should the board be equipped with?

In general, the board is labelled in detail and any components can be used as long as they meet the described specifications. Whether female or male pinheaders are used is individually selectable after own preference.

The following parts are needed resp. recommended:
 - Arduino Pro Mini (Aliexpress Link: https://www.aliexpress.com/item/32672852945.html)
 - 3.3V StepUp (Aliexpress Link: https://www.aliexpress.com/item/32825896409.html)
 - optional 5.0V Output =>5.0V StepUp (Aliexpress Link: https://www.aliexpress.com/item/32786144773.html)
 - Nrf24L01+ (Alixpress Link: https://www.aliexpress.com/item/32327366606.html)
 - Pinheader straight and 90 degrees (The StepUps arerecommend to solder
   with the 90 degrees pins
 - Resistors (470kΩ & 1MΩ)

## Notes on the placement sequence of the shield

The board is placed under the Arduino. Therefore you have to make sure that the pins needed by the shield are soldered from the Arduino to the bottom and the remaining pins are soldered from the top.

Before soldering the Nrf24L01+ you should consider if you need the additional 5.0V output. If this is not needed, the jumper pad below the Nrf24L01+ can be bridged and the 5.0V StepUp can be omitted. Then you have 6 pins with 3.3V output.  

## Recommended libraries

In general the board is universally applicable. Personally I like to use the library and methods of mysensors.org. Mysensors enables a simple integration of different sensors into a meshnetwork, which can communicate with different home automation software solutions via a gateway. I use a serial gateway and as server a RaspberryPi with FHEM (fhem.de).

Link list with further information: 
https://www.mysensors.org/
https://www.mysensors.org/build/battery
https://www.mysensors.org/build/connect_radio
https://www.mysensors.org/build/serial_gateway
https://fhem.de/
https://wiki.fhem.de/wiki/Quick-Start/en
https://fhem.de/commandref.html#MYSENSORS


If you have questions feel free to contact me:
ds@hexagoni.com
 
