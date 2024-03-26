## Module 4 Contract

**Student Names:** Kennar Kahju, Joonas Tiitson

**Agreement:**

As students in this class, we agree to present our skills in using and understanding publish/subscribe with a focus on MQTT, IoT testing (simulators), and integration with MQTT and Node-RED. We will demonstrate our capabilities in the following ways:

**Tasks (As a story):**

* MQTT
We are showing communication between devices in different rooms.
* Air conditioner
We have a microcontroller, which sends the air temperature value to the MQTT topic "airTemp", and another microcontroller as an "air conditioner" with a relay and LED light. It receives the temperature value from the MQTT topic and depending on the temperature received, it turns on/off the "air conditioner". For testing the device, we use an MQTT simulator written in Python. It generates the temperature values, like the first microcontroller, and sends it to the same topic.

* Discord bot
We want to see, what our home air temperature is when being away. For this we will design a Discord bot using Node-Red to respond to us on a command. After us writing /temperature in a channel, the bot responds with the latest info on the temperature value. This way we know how hot or cool our home is and react as needed. 


**Results:**
we don't know how to embed videos

MQTT communication:
[video link through Imgur](https://imgur.com/a/vEOeaY8)

Air conditioner showcase working through MQTT (turn-on temp is set at 24.6). Temperature rise is produced by us blowing on the sensor:
[video link through Imgur](https://imgur.com/a/BOB2v9F)

The following is the thermometer simulator, it publishes it's semi-random values to airTemp topic, it uses IOTknit
```
from iotknit import *
import random
import time

airTemperature=15

init("192.168.12.1")
i=0

led1 = publisher("airTemp")  
def button1Callback(msg):
      global airTemperature
      if random.random()*20>airTemperature:
            airTemperature=airTemperature+random.random()
      else:
            airTemperature=airTemperature-random.random()
      led1.publish(str(round(airTemperature,2)))

while(True):
      button1Callback("tere")
      time.sleep(5)
```
The nodeRed flow is pictured below  
![image](https://github.com/bukyt/IoTgeneral/assets/116277045/66499c17-a2c6-4f77-9846-34e1fbc502f5)



Discord bot responses:  
![image](https://github.com/bukyt/IoTgeneral/assets/68914924/0e71f8d7-c3f5-48a4-92b6-5368e1d85d32)
