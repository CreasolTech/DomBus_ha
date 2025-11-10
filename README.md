# Using Creasol DomBus modules with Home Assistant
DomBus modules can be supplied with two firmwares: please choose *Modbus firmware* if you intend to use it with Home Assistant.

In this repository, for each module a directory is created within the configuration files to use DomBus modules equipped with Modbus firmware with Home Assistant.

**It's recommended to use DomBus firmware + DomBusGateway software, that provides a DomBus 2 MQTT-AutoDiscovery interface. Please check https://github.com/CreasolTech/DomBusGateway**

Files are:
* **configuration.yaml** that includes **dombus1.yaml** with all entities for DomBus modules connected to the same bus, and some helpers.
* **dombus1.yaml** contains the configuration of Modbus #1 (you can have more buses, each for one serial port)
* **dombusXXXX.yaml** contains entities for specific DomBus modules connected to this bus

Any Modbus RTU bus can store up to 247 modules, but for large domotic networks with 20 or more modules, it's better to divide the network in more buses (one bus for each floor, for example): in this case it's possible to include in *configuration.yaml* the file *dombus2.yaml* for bus #2, and so on.
																																															  Please note that for each entity type there is a included file: in this way it's easier to enable/disable configuration file for each module ( EVSE module, relay modules, ... )

[More information on DomBus modules with Home Assistant](https://www.creasol.it/HomeAssistant)

## DomBusEVSE EVSE module to make a Smart Wallbox EV Charging Station
Home Assistant configuration files for DomBusEVSE module used to make a DIY smart wallbox charging station
[![alt DomBusEVSE DIY wallbox home-made](https://images.creasol.it/creDomBusEVSE_dashboard1.png "Modulo EVSE per autocostruirsi una smart wallbox")](https://www.creasol.it/en/support/domotics-home-automation-and-diy/making-a-diy-homemade-wallbox-working-with-home-assistant)

In case that an energy meter to measure the grid power already exists, you don't need to install another energy meter: just use a simple automation to feed the current power from the grid (negative if power is exported to the grid) to the EVSE module, as shown in the following picture (check file *dombus/dombusevse/dombusevse_automations.yaml*)
![Automation example that feeds the grid power value to the EVSE: replace **evpower** with the name of your power entity](https://images.creasol.it/creDomBusEVSE_GridPowerAutomation.jpg "Automation example that feeds the grid power value to the EVSE: replace **evpower** with the name of your power entity")

**Want to build a home-made, full features, EV charging station? Discover our KITs!** \
 [KIT for single phase wallbox](https://store.creasol.it/EVSE1P) \
 [KIT for three phase wallbox](https://store.creasol.it/EVSE3P)



More information in the web pages:

* [DomBusEVSE page](https://www.creasol.it/EVSE)
* [DomBusEVSE with Home Assistant](https://www.creasol.it/en/support/domotics-home-automation-and-diy/making-a-diy-homemade-wallbox-working-with-home-assistant-to-charge-electric-vehicles)
* [Creasol store](https://store.creasol.it/en/18-ev-electric-vehicles)

### Youtube video showing DomBusEVSE working with Domoticz 
[![How DomBusEVSE works - Video using Domoticz, in this case](https://img.youtube.com/vi/m_n_A4lo9Gw/0.jpg)](https://youtu.be/m_n_A4lo9Gw)

### Home made wallbox using DomBusEVSE and Home Assistant
[![DomBusEVSE connections](https://images.creasol.it/creDomBusEVSE_wallbox_photo_ha.jpg "DIY wallbox using Creasol DomBusEVSE module with Home Assistant")](https://www.creasol.it/en/?view=article&option=com_content&id=160)

[![DomBusEVSE connections schematic](https://images.creasol.it/creDomBusEVSE_blockAll.webp "Home-made smart wallbox using Creasol DomBusEVSE module with HomeAssistant")](https://www.creasol.it/en/?view=article&option=com_content&id=160)

[![DomBusEVSE connections schematic for three-phase power supply](https://images.creasol.it/creDomBusEVSE_blockAll_3p.webp "Home-made smart wallbox using Creasol DomBusEVSE module with HomeAssistant, three-phase")](https://www.creasol.it/en/?view=article&option=com_content&id=160)

## DomBus36 
DomBus36 is a **high efficiency  module with 12 relay outputs**, grouped in 3 groups to have an easier wiring: each group share the same common, so you **don't need to make jumpers to connect the common wire (Line, Neutral, Ground or +12/24V) to all relays**.

Relays are protected from overvoltage and overcurrent, and module has a **very low power consumption: less than 15mW with all relays OFF, and less than 750mW when all 12 relays are ON**. Can you compare this power consumption with other modules in the market?

[![DomBus36 module with 12 relay outputs](https://images.creasol.it/creDomBus36.webp "12 relays module for HomeAssistant with very very low power consumption")](https://www.creasol.it/en/?view=article&option=com_content&id=166)

## DomBus37
DomBus37 is a **versatile module integrating inputs, AC inputs (to sense 230V presence) and relay outputs**.

In the application note below the simplest configuration with Home Assistant.
[![DomBus37 module with 12 inputs, 3 AC optoisolated inputs, 3 relay outputs](https://images.creasol.it/ha_creDomBus37_entities.webp "12 inputs, 3 AC optoisolated inputs, 3 relay outputs module for HomeAssistant")](https://www.creasol.it/en/?view=article&option=com_content&id=169)


## DomBus12
DomBus12 is a **compact and cost effective module with 9 I/Os**. Each I/O can be configured as button, switch, double-pushbutton (UP/DOWN pushbutton connected to a single port), counter, meter, NTC temperature sensor, distance sensor, buzzer, led, ...

Below an application example.

[![DomBus12 compact module with 9 configurable I/Os](https://images.creasol.it/an_creDomBus12_ha_garage_watering.webp "DomBus12 compact module for Home Assistant, with 9 configurable GPIO")](https://www.creasol.it/en/?view=article&option=com_content&id=153)








***

## Creasol DomBus modules

Below a list of modules, produced in Italy by Creasol, designed for high reliability and optimized for very very low power consumption.

[<img src="https://images.creasol.it/pdf2.png" alt="Video" style="vertical-align: middle;"> Download the PDF catalog!](https://www.creasol.it/catalog)


Our industrial and home automation modules are designed to be
* very low power &rArr; **10÷15mW with relays OFF**
* reliable &rArr; **no disconnections**
* wired network (bus) &rArr; **no radiofrequency interference, no battery to replace**

Modules are available in two versions:
1. with **DomBus proprietary protocol**, suitable for every type of DomBus modules, working with [Domoticz](https://www.domoticz.com) by using the Creasol DomBus plugin, and [Home Assistant](https://www.home-assistant.io), [OpenHAB](https://www.openhab.org), [Node-RED](https://nodered.org) ... by using the [DomBusGateway software, a DomBus 2 MQTT-AutoDiscovery interface](https://www.creasol.it/DomBusGateway)
2. with **Modbus standard protocol**, suitable for relays modules, EVSE and Dual Axis solar tracker, working with almost any building automation system supporting Modbus

What version is the best? DomBus version, because:

**Modbus** is a standard protocol Master/Slave: the controller must poll each module to get its status, so it's **not suitable to manage inputs and counters that change frequently**, but can be used to manage relay outputs or read inputs status every 2-5s

**DomBus** is a proprietary multi-master protocol where **each module is able to initiate the communication with the master** to notify, for example, an input change, with a short latency (<100ms) that permits to **manage alarm sensors in a reliable way**. Also, DomBus supports the so-called DCMD, **commands exchanged between modules as KNX does**, so it's possible to program simple automations that work between modules even if the domotic controller is OFF (for example, short pulse on button to toggle a light ON/OFF, 1s pulse to open the garage door, 2s pulse to turn OFF some lights, ...)


[Store website](https://store.creasol.it/domotics) - [Information website](https://www.creasol.it/domotics)

### Youtube video showing DomBus modules
[![Creasol DomBus modules video](https://images.creasol.it/intro01_video.png)](https://www.creasol.it/DomBusVideo)



### DomBusEVSE - EVSE module to build a Smart Wallbox / EV charging station
<a href="https://store.creasol.it/DomBusEVSE"><img src="https://images.creasol.it/creDomBusEVSE_plug_300.webp" alt="DomBusEVSE smart EVSE module to make a Smart Wallbox EV Charging station" style="float: left; margin-right: 2em;" align="left" /></a>
Complete solution to make a Smart EVSE, **charging the electric vehicle using only energy from renewable source (photovoltaic, wind, ...), or adding 25-50-75-100% of available power from the grid**.

* **Single-phase and three-phase**, up to 32A (8kW or 22kW)
* Needs external contactor, RCCB (protection) and EV cable
* Optional power meter to measure charging power, energy, voltage and power factor
* Optional power meter to measure the power usage from the grid (not needed if already exists)
* **Two max grid power thresholds** can be programmed: for example, in Italy who have 6kW contractual power can drain from the grid Max (6* 1.27)=7.6kW for max 90 minutes followed by (6* 1.1)=6.6kW for another 90 minutes: in this case **the EVSE module can drain ALL available power** when programmed to charge at 100% **minimizing the charge time and increasing the charging efficiency**.
* **Works without the domotic controller** (stand-alone mode), and **can also work in *managed mode*, with an automation in the home automation system setting the charging current**

<br clear="all"/>

### DomBusTH - Compact board to be placed on a blank cover, with temperature and humidity sensor and RGW LEDs
<a href="https://store.creasol.it/DomBusTH"><img src="https://images.creasol.it/creDomBusTH6_200.png" alt="DomBusTH domotic board with temperature and humidity sensor, 3 LEDs, 6 I/O" style="float: left; margin-right: 2em;" align="left" /></a>
Compact board, 32x17mm, to be installed on blank cover with a 4mm hole in the middle, to exchange air for the relative humidity sensor. It can be **installed in every room to monitor temperature and humidity, check alarm sensors, control blind motor UP/DOWN**, send notifications (using red and green leds) and activate **white led in case of power outage**.

Includes:
* temperature and relative humidity sensor
* red, green and white LEDs
* 4 I/Os configurable as analog or digital inputs, pushbuttons, counters (water, gas, S0 energy, ...), NTC temperature and ultrasonic distance sensors
* 2 ports are configured by default as open-drain output and can drive up to 200mA led strip (with dimming function) or can be connected to the external module DomRelay2 to control 2 relays; they can also be configured as analog/digital inputs, pushbuttons and distance sensors.
<br clear="all"/>

### DomBus12 - Compact domotic module with 9 I/Os
<a href="https://store.creasol.it/DomBus12"><img src="https://images.creasol.it/creDomBus12_400.webp" alt="DomBus12 domotic module with 9 I/O" style="float: left; margin-right: 2em;" align="left" /></a>
**Very compact, versatile and cost-effective module with 9 ports**. Each port can be configured by software as:
* analog/digital inputs
* pushbutton and UP/DOWN pushbutton
* counters (water, gas, S0 energy, ...)
* NTC temperature and ultrasonic distance sensors
* 2 ports are configured by default as open-drain output and can drive up to 200mA led strip (with dimming function) or can be connected to the external module DomRelay2 to control 2 relays.
<br clear="all"/>

### DomBus21 - Latching relays domotic module
<a href="https://store.creasol.it/DomBus21"><img src="https://images.creasol.it/creDomBus21_size_400.webp" alt="DomBus21 domotic module with 3 latching relays, 1 AC input and 4 low voltage inputs" style="float: left; margin-right: 2em; vertical-align: middle;" align="left" /></a>
Very compact domotic module providing:
* **3x latching relays SPST, max current 15A (3kW): no power consumption when relays are On or Off!**
* 1x 230V AC opto-isolated input to detect 230V and power outage, with **zero-detection to switch relays/loads minimizing in-rush current**
* 4x I/O lines, configurable as analog/digital inputs, temperature/distance sensor, counter, meter, ...
<br clear="all"/>

### DomBus23 - Domotic module with many functions
<a href="https://store.creasol.it/DomBus23"><img src="https://images.creasol.it/creDomBus23_400.webp" alt="DomBus23 domotic module with many functions" style="float: left; margin-right: 2em; vertical-align: middle;" align="left" /></a>
Versatile module designed to control **gate or garage door**.
* 2x relays SPST 5A
* 1x 10A 30V mosfet (led stripe dimming)
* 2x 0-10V analog output: each one can be configured as open-drain output to control external relay
* 2x I/O lines, configurable as analog/digital inputs, temperature/distance sensor, counter, ...
* 2x low voltage AC/DC opto-isolated inputs, 9-40V
* 1x 230V AC opto-isolated input
<br clear="all"/>

### DomBus31 - Domotic module with 8 relays
<a href="https://store.creasol.it/DomBus31"><img src="https://images.creasol.it/creDomBus31_400.webp" alt="DomBus31 domotic module with 8 relay outputs" style="float: left; margin-right: 2em; vertical-align: middle;" align="left" /></a>
DIN rail low profile module, with **8 relays and very low power consumption**:
* 6x relays SPST 5A
* 2x relays STDT 10A
* Only 15mW power consumption with all relays OFF
* Only 600mW power consumption with all 8 relays ON !!
<br clear="all"/>

### DomBus32 - Domotic module with 3 relays
<a href="https://store.creasol.it/DomBus32"><img src="https://images.creasol.it/creDomBus32_200.webp" alt="DomBus32 domotic module with 3 relay outputs" style="float: left; margin-right: 2em; vertical-align: middle;" align="left" /></a>
Versatile module with 230V inputs and outputs, and 5 low voltage I/Os.
* 3x relays SPST 5A
* 3x 115/230Vac optoisolated inputs
* Single common for relays and AC inputs
* 5x general purpose I/O, each one configurable as analog/digital inputs, pushbutton, counter, temperature and distance sensor.
<br clear="all"/>

### DomBus33 - Module to domotize a light system using step relays
<a href="https://store.creasol.it/DomBus33"><img src="https://images.creasol.it/creDomBus32_200.webp" alt="DomBus33 domotic module with 3 relay outputs that can control 3 lights" style="float: left; margin-right: 2em; vertical-align: middle;" align="left" /></a>
Module designed to **control 3 lights already existing and actually controlled by 230V pushbuttons and step-by-step relays**. In this way each light can be activated by existing pushbuttons, and by the domotic controller.
* 3x relays SPST 5A
* 3x 115/230Vac optoisolated inputs
* Single common for relays and AC inputs
* 5x general purpose I/O, each one configurable as analog/digital inputs, pushbutton, counter, temperature and distance sensor.

Each relay can toggle the existing step-relay, switching the light On/Off. The optoisolator monitors the light status. The 5 I/Os can be connected to pushbuttons to activate or deactivate one or all lights.
<br clear="all"/>

### DomBus36 - Domotic module with 12 relays
<a href="https://store.creasol.it/DomBus36"><img src="https://images.creasol.it/creDomBus36_400.webp" alt="DomBus36 domotic module with 12 relay outputs" style="float: left; margin-right: 2em; vertical-align: middle;" align="left" /></a>
DIN rail module, low profile, with **12 relays outputs and very low power consumption**.
* 12x relays SPST 5A
* Relays are grouped in 3 blocks, with a single common per block, for easier wiring
* Only 12mW power consumption with all relays OFF
* Only 750mW power consumption with all 12 relays ON !!
<br clear="all"/>

### DomBus37 - 12 inputs, 3 115/230Vac inputs, 3 relay outputs
<a href="https://store.creasol.it/DomBus37"><img src="https://images.creasol.it/creDomBus37_400.webp" alt="DomBus37 domotic module with 12 inputs, 3 AC inputs, 3 relay outputs" style="float: left; margin-right: 2em; vertical-align: middle;" align="left" /></a>
Module designed to **interface alarm sensors (magnetc contact sensors, PIRs, tampers): it's able to monitor mains power supply (power outage / blackout) and also have 3 relays outputs.**
* 12x low voltage inputs (analog/digital inputs, buttons, alarm sensors, **balanced double/triple biased alarm sensors**,  counters, meters, temperature and distance sensors, ...)
* 3x 115/230Vac optoisolated inputs
* 2x relays SPST 5A
* 1x relay SPST 10A
<br clear="all"/>

### DomBus38 - 12 inputs, 1 100-250Vac input, 6 relay outputs
<a href="https://store.creasol.it/DomBus38"><img src="https://images.creasol.it/creDomBus38_400.webp" alt="DomBus38 smart home module with 12 inputs, 1 AC input, 6 SPDT relay outputs + 2 SPDT relay outputs 10A" style="float: left; margin-right: 2em; vertical-align: middle;" align="left" /></a>
Module designed to **interface alarm sensors (magnetc contact sensors, PIRs, tampers), lights and appliances outputs, ...**
* 12x low voltage inputs (analog/digital inputs, buttons, alarm sensors, **balanced double/triple biased alarm sensors**, counters, meters, temperature and distance sensors, ...)
* 1x 115/230Vac optoisolated input to detect power outage and for zero-crossing detection (to switch relays minimizing the in-rush current)
* 4x relays SPDT 10A (with Normally Open and Normally Closed contacts)
* 2x relays SPST 10A (with only Normally Open contacts)
<br clear="all"/>

### DomBusTracker - Dual axis sun tracker controller working with Domoticz, Home Assistant, Node-RED, Modbus, ... and also working in standalone with no external controllers
<a href="https://store.creasol.it/DomBusTracker"><img src="https://images.creasol.it/creDomBusTracker_sun_400.webp" alt="DomBusTracker smart home module that controls 2 linear actuators in a solar tracking system" style="float: left; margin-right: 2em; vertical-align: middle;" align="left" /></a>
Module that **check a deep-hole sun sensor to detect the direction of maximal sun radiation, working also in case of cloudy weather.**
* Controls two external actuators/motors (linear or not) to move motors to reach the best tilt / elevation and azimuth position to optimize photovoltaic production.
* **Check current through the motors to detect internal limit switch** (useful for linear actuators) and find where the tracker reach the final/initial position.
* **Works autonomously** (stand-alone), without any home automation system controller, but **also can be connected to a home automation system using Domoticz, Home Assistant, NodeRED, OpenHAB,** and other systems by using the DomBusGateway software (that converts DomBus protocol to MQTT AutoDiscovery), or with other systems by using DomBusTracker with Modbus firmware.
* Wire connection (RS485) to the domotic controller for the best reliability.
<br clear="all"/>

### DomRelay2 - 2x relays board
<a href="https://store.creasol.it/DomRelay2"><img src="https://images.creasol.it/creDomRelay22_200.png" alt="Relay board with 2 relays, to be used with DomBus domotic modules" style="float: left; margin-right: 2em; vertical-align: middle;" align="left" /></a>
Simple module with 2 relays, to be used with DomBus modules (like <a href="https://store.creasol.it/DomBusTH">DomBusTH</a> and <a href="https://store.creasol.it/DomBus12">DomBus12</a>) or other electronic boards with open-collector or open-drain outputs
* **2x SPST relays 5A** (Normally Open contact)
* Overvoltage protection (for inductive loads, like motors)
* Overcurrent protection (for capacitive laods, like AC/DC power supply, LED bulbs, ...)
<br clear="all"/>

### DomESP1 / DomESP2 - Board with relays and more for ESP8266 NodeMCU WiFi module
<a href="https://store.creasol.it/DomESP1"><img src="https://images.creasol.it/creDomESP2_400.webp" alt="Relay board for ESP8266 NodeMCU module" style="float: left; margin-right: 2em; vertical-align: middle;" align="left" /></a>
**IoT board designed for NodeMCU v3 board using ESP8266 WiFi microcontroller**
* 9÷24V power supply input, with high efficiency DC/DC regulator with 5V output
* **4x SPST relays 5A with overvoltage protection** (varistor)
* **2x mosfet outputs** (max 30V, 10A) for LED dimming or other DC loads
* 1x I²C interface for sensors, extended I/Os and more)
* 1x OneWire interface (DS18B20 or other 1wire sensors/devices)
<br clear="all"/>

