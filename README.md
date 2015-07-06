SWIR_MQTTClient
===============

This Arduino Library enables your Arduino-based system, equiped with Sierra Wirelss AirPrime HL series wireless module, to easily exchange data over MQTT with Sierra Wireless AirVantage server:
* Sending custom data such as sensor values or application data from Arduino to AirVantage
* Sending actuator commands or configuration data from AirVantage to Arduino

This library provides 3 functionalities:
1. Module management: setting SIM pin code, setting APN, making data call, etc…
2. MQTT Client: managing MQTT session with AirVantage, sending/receiving MQTT packets over AT commands.
MQTT packets are generated and handled by [Paho MQTTClient library](https://www.eclipse.org/downloads/download.php?file=/paho/arduino_1.0.0.zip) which implements MQTT protocol.
3. Log output facility: SWI_TRACE macro enables the Arduino app to output debug traces to a virtual serial port. This latter function is emulated on Arduino pins 12 & 13 (by default) and trace logs are visible with a serial monitor application bound to the TTL to serial USB port.

An sample sketch is provided as a Quick Start to publish data to and to receive data from AirVantage, without typing a single line of code.
This Quick Start sample Arduino sketch is intended to be used as a starting point to easily build AirVantage-MQTT-ready application.

Prerequisite
------------
1. Paho MQTTClient library, prebuild for Arduino
2. HL Shield + Antenna + Power adaptor + USB cable MiniB-A
3. AirPrime HL series Module
4. SIM card with data call plan
5. Arduino Mega2560 + USB cable type B-A
6. TTL to Serial USB cable (E.g. TTL-232R)
7. Have an account on AirVantage server : eu.airvantage.net

{{% collapse id="bom" text="Part references, for information" %}}
* [AirPrime HL series module](http://www.sierrawireless.com/productsandservices/airprime_wireless_modules/essential_modules/hl_series/)
* [Arduino Mega 2560](https://www.arduino.cc/en/Main/ArduinoBoardMega2560)
* HL Shield. Please contact Sierra Wireless sale representative
* [Antenna](http://fr.farnell.com/pulse-engineering/w1900/antenne-ext-penta-sma-artic/dp/1900068?ost=antenna+ex+penta+sma+artic)
* [Power adapter 12Vdc 1.5A](http://fr.rs-online.com/web/p/alimentations-enfichables/7212203/)
* [USB Hub](http://fr.rs-online.com/web/p/hubs-usb/7873404/)
* [TTL to Serial USB cable](http://fr.rs-online.com/web/p/kits-de-developpement-pour-interfaces/7676200/)
* [USB-A to USB-B cable](http://fr.rs-online.com/web/p/cordons-usb/7903931/)
* [USB-A to MiniUSB cable](http://fr.rs-online.com/web/p/cordons-usb/7903678/)
* [Passive Infra-Red (PIR) motion sensor](http://fr.rs-online.com/web/p/kits-de-developpement-pour-interfaces/7813024/)
* [LED](http://fr.rs-online.com/web/p/led/7088022/)
* [Wiring cables](http://www.miniinthebox.com/dupont-wire-female-to-female-cable-line-41p-41p-test-lines-connector-10cm-201211270080013_p480341.html)
{{% /collapse %}}

Library Installation
--------------------
* Launch Arduino IDE
* Import SWIR_MQTTClient library
    * In Arduino IDE, go to __Sketch__ menu, select __Include Library__, then __Add .ZIP Library...__
    * Select the SWIR_MQTTClient lib zip file (e.g. SWIR_MQTTClient V0.8.zip)
* Import Paho MQTTClient library
    * Download the prebuilt Arduino port of Paho MQTTClient [here](https://www.eclipse.org/downloads/download.php?file=/paho/arduino_1.0.0.zip)
    * In Arduino IDE, go to __Sketch__ menu, select __Include Library__, then __Add .ZIP Library...__
    * Select the Paho MQTTCleint zip file as downloaded in the previous step (e.g. arduino_1.0.0.zip)


Hardware Setup & Tutorial
----------------------------------
Please refer to this [tutorial](https://doc.airvantage.net/av/howto/hardware/samples/arduino-hl-mqtt/) for information on hardware setup and complete tutorial

 
