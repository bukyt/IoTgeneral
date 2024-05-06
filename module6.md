## Module 6

**Student Names:** Kennar Kahju, Joonas Tiitson

**Task we agreed to do:** Find the maximum amount of devices able to connect to a phone MQTT server


**Results of the task:**

We started by trying to install the IoTEmpower framework on a phone. This was simple, the install script is a one-line, but during installing we ran into missing packages which we had to install separately.  
![image](https://github.com/bukyt/IoTgeneral/assets/68914924/ac9eda42-d9ad-43c0-b502-34320e5ecbf1)  
Packages missing and installed via Termux packages: git, python3, npm. Everything was added with default settings.

After installing, the framework opened (almost) nicely:  
![image](https://github.com/bukyt/IoTgeneral/assets/68914924/04d7a0df-73af-4240-80bb-ed4f4b865ec1)  
One problem: ip command is locked behind root access on Android, so whenever it is needed, some scripts fail.

Trying the basic commands for MQTT broker and web interface Node-Red/Cloud commander showed that MQTT did not work out of the box, but Node-Red did after generating a password with `node-red admin hash-pw` to save in the settings file. `.node-red/settings.js`  
Cloud Commander has issues logging in, because we don't know any password in the Android environment.  
![image](https://github.com/bukyt/IoTgeneral/assets/68914924/d2ba0b01-522a-4974-be44-7e8cb0249042)  

The mqtt_starter command uses the "ip" shell command, and did not find a valid IP to host the broker on. To fix that, we got the phone's ip from ifconfig, and pasted it in the mosquitto configuration file `iot/.local/tmp/mosquitto/mosquitto.conf`:  
![image](https://github.com/bukyt/IoTgeneral/assets/68914924/14832ba1-d2f8-4ef2-90b8-c6f5041d31e5)  

Cloud Commander has its problems as well, even when separately starting the service using `cloudcmd --no-auth`. 
The service can not reach root folder, because of no root rights.  
![image](https://github.com/bukyt/IoTgeneral/assets/68914924/96defdbf-d4d3-48e4-a728-d2e7d769a7e6)  

We also created a new bash script to run the MQTT broker and other web services together (as Termux does not have multiple windows available):  
![image](https://github.com/bukyt/IoTgeneral/assets/68914924/ecb15ce7-d795-451f-9d1d-96e9e4dc3bec)  
Mosquitto is ran as a separate command, because mqtt_broker is broken and does not generate a valid IP to host on.



**Problems aside, what was the result?**
The nodes were flashed using the gateway device, because it was currently easier to do so. Everything else is done on the phone's hotspot.

We managed to flash 10 nodes and then faced a problem. When using the gateway as well (total 11), one node would not connect:  
![image](https://github.com/bukyt/IoTgeneral/assets/68914924/ada15703-ba95-470c-b230-1606633c0293)  
While the setting allows `32 devices`, only 10 were connected at a time, and more could not do:  
![image](https://github.com/bukyt/IoTgeneral/assets/68914924/fdd8f17c-1c09-4ef7-a67b-d609f39dd16e)  

So, with a gateway to control the devices, only 9 nodes can be connected at a time (at least on our phone).

To check this, we used the simple onboard LED to show it not working:  
* Flash every node to control LED via MQTT topic `node{number}/led/set`  
* Create a Node-Red flow to change the LED status
* Check the LEDs

The node-flow looks like this:  
![image](https://github.com/bukyt/IoTgeneral/assets/68914924/26ecdbb4-2138-4333-8046-28cf00870c10)


[Video of one LED not turning off](https://imgur.com/a/EN20pAP)


**Key points of result:**
* A phone can run the IoTEmpower framework (with modifications hopefully included in the releases)
* Our phone could run up to 10 nodes (or 9 nodes + separate control computer)
* We could run multiple services together, such as Node-Red and Mosquitto
* A phone is handy to bring around and to demonstrate solutions, with its own power supply (battery)
* 


