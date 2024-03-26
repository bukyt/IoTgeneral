## Module 4 Contract

**Student Names:** Kennar Kahju, Joonas Tiitson

**Agreement:**

As students in this class, we agree to present our skills in using and understanding publish/subscribe with a focus on MQTT, IoT testing (simulators), and integration with MQTT and Node-RED. We will demonstrate our capabilities in the following ways:

**Tasks (As a story):**

For MQTT, we are showing communication between devices in different rooms.
We plan to design a home device (air conditioner) as an LED (on/off light) on a microcontroller and temperature sensors. For testing the device we use a MQTT simulator. 
We will design a Discord bot using Node-Red to report us the temperature on command (through us writing in a channel) or do some other task.


**Results:**

MQTT communication:
[video link through Imgur](https://imgur.com/a/vEOeaY8)


Air conditioner showcase working through MQTT (turn-on temp is set at 24.6):
[video link through Imgur](https://imgur.com/a/BOB2v9F)

The rest is coming
The following is the thermometer simulator, it publishes it's semi-random values to airTemp topic, it uses IOTknit
```
from iotknit import *
import random
import time

airTemperature=15

#init("localhost")  # use a MQTT broker on localhost
init("192.168.12.1")
prefix("")  # all actors below are prefixed with /led
i=0

led1 = publisher("airTemp")  # create a Thingi interface that publishes to led/led1
def button1Callback(msg):
      global airTemperature
      if random.random()*20>airTemperature:
            airTemperature=airTemperature+random.random()
      else:
            airTemperature=airTemperature-random.random()
      led1.publish(str(round(airTemperature,2)))
      print(msg)


prefix("button")  # all sensors below are prefixed with /button

button1 = subscriber("button1")  # create a Thingi interface that can have 
                                 # subscribes only to button/button1
button1.subscribe_change(callback=button1Callback)
weather = subscriber("airTemp")

while(True):
      button1Callback("tere")
      time.sleep(5)
```
The nodeRed flow is pictured below  
![image](https://github.com/bukyt/IoTgeneral/assets/116277045/66499c17-a2c6-4f77-9846-34e1fbc502f5)
