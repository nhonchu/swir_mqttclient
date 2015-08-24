SWIR_MQTTClient
===============

This Library enables your __Arduino__-based or __STM32-Nucleo__-based Device, equiped with Sierra Wirelss AirPrime HL series wireless module, to easily exchange data over MQTT with Sierra Wireless AirVantage server:
* Sending custom data such as sensor values or application data from Device to AirVantage
* Sending actuator commands or configuration data from AirVantage to Device (Arduino or STM32-Nucleo)

This library provides 3 functionalities:

1. Module management: setting SIM pin code, setting APN, making data call, etc…
2. MQTT Client: managing MQTT session with AirVantage, sending/receiving MQTT packets over AT commands.
MQTT packets are generated and handled by [Paho MQTTClient library](https://www.eclipse.org/downloads/download.php?file=/paho/arduino_1.0.0.zip) which implements MQTT protocol.
3. Log output facility: SWI_TRACE macro enables the Device app to output debug traces to a virtual serial port. This latter function is emulated on Device pins 2 & 8 (by default) and trace logs are visible with a serial monitor application bound to the TTL to serial USB port.

An sample sketch is provided as a Quick Start to publish data to and to receive data from AirVantage, without typing a single line of code.
This Quick Start sample is intended to be used as a starting point to easily build AirVantage-MQTT-ready application.

Prerequisite
------------
1. Paho MQTTClient library, prebuild for Arduino
2. HL Shield + Antenna + Power adaptor + USB cable MiniB-A
3. AirPrime HL series Module
4. SIM card with data call plan
5.a Arduino Mega2560 + USB cable type B-A
       or
5.b STM32-Nucleo (tested on L053R8) + USB cable type B-A
6. TTL to Serial USB cable (E.g. TTL-232R)
7. Have an account on AirVantage server : eu.airvantage.net


Library Installation for Arduino
--------------------------------
* Launch Arduino IDE
* Import SWIR_MQTTClient library
    * In Arduino IDE, go to __Sketch__ menu, select __Include Library__, then __Add .ZIP Library...__
    * Select the SWIR_MQTTClient lib zip file (e.g. SWIR_MQTTClient V0.8.zip)
* Import Paho MQTTClient library
    * Download the prebuilt Arduino port of Paho MQTTClient [here](https://www.eclipse.org/downloads/download.php?file=/paho/arduino_1.0.0.zip)
    * In Arduino IDE, go to __Sketch__ menu, select __Include Library__, then __Add .ZIP Library...__
    * Select the Paho MQTTCleint zip file as downloaded in the previous step (e.g. arduino_1.0.0.zip)

Library Installation for mbed/STM32-Nucleo
--------------------------------
* Launch mbed IDE
* Import SWIR_MQTTClient library
    * In mbed IDE, select __Import__
    * In Upload tab, select the SWIR_MQTTClient lib zip file (e.g. SWIR_MQTTClient V0.91.zip)
* Import Paho MQTTClient library
	* In Upload tab, select the prebuilt Arduino port of Paho MQTTClient lib zip file [available here](https://www.eclipse.org/downloads/download.php?file=/paho/arduino_1.0.0.zip)
* Import __mbed__ C/C++ SDK from the Import/Libraries tab: Drag the lib package and drop it into your project
* SWIR_MQTTClient Library provides a Quick Start sample that is intended to be used as a starting point to easily build AirVantage-MQTT-ready application.
* This starting point application can publish data to and receive data from AirVantage... without typing a single line of code.<br>
However this sample app has been configured by default for Arduino platform, do the following to adjust it for Nucleo platform:
	* Go to the mbed IDE (web browser)
	* Select *swir_platform_def.h* file, disable TARGET_ARDUINO (//#define TARGET_ARDUINO) and enable TARGET_MBED (#define TARGET_MBED)
	* Right-click and Rename the provided sample arduino sketch HL-AV_QuickStart.ino (SWIR_MQTTClient/examples/HL_AV_QuickStart) to HL-AV_QuickStart.cpp
	* Right-click then Copy HL-AV_QuickStart.cpp file which is still greyed out due to precedent invalid *ino* file extension
	* Right-click on the top level program folder (e.g. Nucleo-AVHL) then select Paste, now the sample cpp file becomes valid.
	* Right-click on the greyed out HL-AV_QuickStart.cpp (in SWIR_MQTTClient/examples/HL_AV_QuickStart) then delete it

Hardware Setup & Tutorial
----------------------------------
For further information, please refer to :
* [Arduino tutorial](https://doc.airvantage.net/av/howto/hardware/samples/arduino-hl-mqtt/) for information on hardware setup and complete tutorial
* [STM32-Nucleo tutorial](https://doc.airvantage.net/av/howto/hardware/samples/nucleo-hl-mqtt/) for information on hardware setup and complete tutorial

 
