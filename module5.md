## Module 5 Contract

**Student Names:** Kennar Kahju, Joonas Tiitson

**Agreement:**

As students in this class, we agree to present our skills in using and understanding IoTempower

**Tasks:**

* Talking about framework benefits: useful features, 
* We will show the basics of remote deployment, how to set it up with IoTEmpower and how to update devices over the air(OTA).
* We are designing a home security system with access control. It would feature:
    * RFID card access
    * a "main door"
    * sound signals for false entry
    * LED signal for having an open door
    * remote opening of the "door" using another microcontroller
    * ability to disable all opening of doors (security feature)
    * A dashboard featuring current lock status, ability to open door


## Results

Framework benefits: 
* There is less to be done from scratch, writing code is simplified by the use of simple modules
* Usually frameworks are more stable than self-built systems and can survive small code changes more easily
* Frameworks have the ability to quickly deploy changes, reducing time cost
* In the context of IoTEmpower, devices can be updated wirelessly, further reducing time cost and making updates faster
* Also, IoTEmpower allows setting up devices using only one line (everything else is included in the package)

Remote deployment:  
IoTEmpower has a simple interface to set up devices. First flash needs to be over USB, and after that every flash can be done over WiFi, reducing the need for wires.


### Security System: ###
Final functions:
* RFID card access
* Remote control button
* Sounds for allowed/denied entry
* Dashboard for opening lock remotely, viewing last time lock was opened and disabling card access

The security system can open the door in many ways:  
* Regular card access, using pre-configured cards  
* Using the M5 stick button, no card is needed  
* Using the Dashboard button  

The M5 Stick (remote control) has a LED light, that lights up whenever the "door" is open (and goes off if door closes).  
The screen is configured to show latest access info:  
* wrong cards show "Unknown entry detected"  
* right cards/m5 stick/dashboard button show "Authorized entry detected"  
* when door is opened, also show "Opened door"  

Dashboard has the function to disable all card access. Doing so, only the M5 stick and dashboard can access the system until turned on again. A good feature, if a high level access card has been lost :)  
At that time, using allowed cards shows "Switch is disabled" on the M5 display.  
The dashboard has the ability to see when the door was last opened, making it easier to spot hidden activity.

All nodes are configured using IoTEmpower's one line setup, all logic is through Node-Red.  
*Node-Red flow is not shown due to us forgetting to make a screenshot. Dashboard is seen from the video. Sorry :(*

The hardest part was configuring the nodes to work together. For some reason, the relay node kept resetting itself while turning the relay on/off a little too often. Fortunately, it did not happen on presenting the project, so we were lucky :)

[Video of all features (sound is available for buzzer)](https://imgur.com/a/eloPzSI)

Photo of final result:  
![IMG_20240416_132605](https://github.com/bukyt/IoTgeneral/assets/68914924/c63bcb2f-dedd-4911-8178-70490917d075)




