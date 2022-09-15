# Home Assistant Add-on: Hewalex2MQTT

Hewalex devices are equipped with empty RS485 connectors. This is basically a serial port. This script uses a 'serial for url' connection.

You can buy a (cheap) wifi 2 rs485 or ethernet 2 rs485 device wich you attach to the rs485 port you want to interface with. And you need a piece of wire with 4 strands.
Heat pumps (PCWU) setup

Remove the plastic case and open up the "fuse box". In here you will find a free rs485 connector. Remove it and screw in a 4 strand wire. Connect the wire to the rs485wifi device. Make sure you connect them correctly. It is wise to measure ac and grnd to be sure!

In the controller, navigate to rs485 settings. Change baud rate to 38500, Actual address to 2 and Logic address to 2.

Setup the rs485-to-wifi device. Make sure baud settings match above settings. It is probably wise to assign static ip-address. Take note of this.
Solar pumps (ZPS) setup

Remove G-422 controller from the casing. Connect the RS485 port on the backside of the G-422 controller to the wifi controller.

## Add-on configuration:
All options from grott are available as options in this add-on. They need to follow the naming convention of the environment variables. Eg:  
```yaml
	gmode: proxy
	gnomqtt: False
	gmqttip: 127.0.0.1
	gmqttport: 5288
	gmqttauth: False
	gmqtttopic: energy/grott
	gmqttuser: user
	gmqttpassword: password

MQTT
Parameter 	Value
MQTT_ip 	192.168.1.2
MQTT_port 	1883
MQTT_authentication 	True
MQTT_user 	
MQTT_pass 	
MQTT_GatewayDevice_Topic 	HewaGate
```
