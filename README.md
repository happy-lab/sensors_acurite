# Publish AcuRite Weather Stations Sensor Data to MQTT
This service collects data from an One-Wire sensor network and publishes
them to a MQTT server.

## License
The majority of this program is copied from the AcuRite drive for the
[WeeWX](http://www.weewx.com) weather station.  It uses that software GPL3
[license](./LICENSE) so this program continues with that license.

## Implementation
All program are written in Python 3 and require that the
[Python MQTT package](https://pypi.python.org/pypi/paho-mqtt/1.1) be installed.
The program was developed and tested on **Arch Linux**
systems running on ARM processors and a Fedora 22 system.

## Installation
* Install and configure a MQTT server or use a public service.
* Install the MQTT Client
	* `pip install paho-mqtt`
* Copy the program to the desired directories or run `makepkg` and install with **pacman**.
* Modify the **sensor_acurite** configuation file and place in `/etc/sensor/sensor_acurite.conf`
* Enable the services:
	* `systemctl enable sensors_acurite`

## Things To Do
* Change running user to non-root.
* Support MQTT authentication
* Support secure MQTT connections
* Better documentation.
