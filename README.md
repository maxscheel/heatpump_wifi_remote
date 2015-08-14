# heatpump_wifi_remote
# Controlling a (Fujitsu) heatpump from OpenHAB.
In the next few days I will add all files involved to run the show.

Personal log for this little project together with http://github.com/marcass

# Screenshots

# Communication Design
Changing heatpump status:
  * OpenHAB->[MQTT]->ESP8266->[SERIAL]->Nano->[IR]->Heatpump

Querying and reading temperature:
  * OpenHAB->[MQTT]->ESP8266->[SERIAL]->Nano->DS18B20->Nano->[SERIAL]->ESP8266->[MQTT]->OpenHAB

#Hardware:

- Linux box (hardkernels odroid U3 w/ Debian Jessie) running OpenHAB and Mosquitto (MQTT)
- Arduino Nano v3 Clone from Aliexpress
- ESP8266 WiFi module from Aliexpress
- Infrared (IR) LED
- 2N2222 Transistor
- Resistors 4k7, 47, 470, 10k, 220, ...
- DS18B20 Temperature sensor
- Reed switch
- Jumpers

#Eagle schematic and layout

#Software/Firmware
##Nano
 * library dependencies:
  ** Alex' heatpump IR
  ** OneWire 

##ESP8266 ESP01
* Flash nodemcu how-to
 
##OpenHAB
* Install openhab, install mosquitto, install rdd
* Add Sitemap
* Add Items
* Add Users
* Activate SSL
