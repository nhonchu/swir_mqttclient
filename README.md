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

 
