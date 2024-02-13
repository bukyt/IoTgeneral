# Module 1 Contract

**Student Name(s):** Kennar Kahju, Joonas Tiitson

**Agreement:**
As students in this class, we agree to fulfill and present the results of the following tasks:
1. We will present our team/pair and list the main characteristics of the other members.
2. The repository/portfolio will be set up, and there will be check-ins from all (small) team/pair members, as well as a first reflection per student.
3. We have compiled a small description of what IoT is that can be presented from our repository in a straightforward manner. We watched the [TIA video](https://www.youtube.com/watch?v=jJaWMWz6RpE&t=145s) and are taking notes from that.
4. We will have an initial but detailed (as an in-class example) story that is challenging and matters for us. It should tackle a problem that is IoT-related but also relevant to ourselves.
5. We will join and actively participate in the IoTempire Discord channel.

**Signature:**
Confirm orally in lab with an instructor that you understand the content of this contract and are willing to put in the work for doing and presenting it.



# Tasks

1. Joonas - hard-working, happy feller. Kennar - a tinkerer, I like doing many small projects at once and lose track of them
2. The repo is created and set up to be accessible by both members and lecturers.
3. The IoT description is located at the bottom of this document.
4. 
5. We have joined the Discord channel



# IoT description

* First solutions were machine to machine and too large solutions
* Fragmented ecosystems slow down the adoption of standards
* A lot of devices are limited to single standards and/or bad interoperability
* Security was/is less thought of with vulnerable devices such as cars
* Devices must be designed to last long (it is costly to regularly change batteries)
* There is no limit to device count, you can have multiple connections to devices
* People want an encapsulated solution that is easy to manage
* IoT should be all connected under a few standards, not every company having it's own standard
* It can be used to preemptively detect machine failures and maintenance needs using sensors measuring temperature, tolerances etc

Benefits of IoT:  
1. Everything is connected and can be centrally controlled
2. Convenient access to existing devices
3. Can streamline many difficult operations
4. Can use as many devices as needed for operation, there is no limit (50 billion devices mentioned in video)

Challenges of IoT:  
1. Some solutions are too broad for a specific issue
2. Set-up cost may be high and can be difficult due to different standards used
3. Some companies like to use their own proprietary protocol, rendering them inoperable with other companies products
4. Devices have low to no security implemented, it is crucial for some applications, such as smart cars

Some stand-out mentions:  
1. IoT devices and sensors can be used to detect machine failures and preemptively avoid high cost repairs
2. Some devices can last for years with a good battery and low power controller


# Initial story

I am used to running different servers on my desktop pc at home, which i don't always have the access to since it is not mobile.

I decided to embark on a DIY IoT project to address this issue. The goal is to design a system where a mobile app on my phone could communicate with a controller device, triggering a physical motor to press down the power button on my PC. This way, even if I was miles away, I could ensure my computer could be powered up any time I need to run things on it.

Components of the Solution:

    Mobile App:
    We will develop a user-friendly mobile application that would act as the remote control for the system. The app would allow me to check the status of my PC and send commands to the controller device.

    Controller Device:
    The controller device, a compact IoT-enabled microcontroller, will be the brain of the operation. It receives commands from the mobile app and controls the physical motor.

    Physical Motor:
    A small yet robust motor was connected to the controller device. Its purpose is to simulate the pressing down of the power button on the PC.

    IoT Connectivity:
    Both the mobile app and the controller device are equipped with Wi-Fi modules for seamless communication. This ensured that I could control my PC from anywhere with an internet connection.

The Remote startup device in action:

Since my friends want to play minecraft on a server but I am on holiday, I need to access my desktop remotely, which I use RDP for, but i first needed to start up my computer

Opening the mobile app, I connect to my home IoT network and accessed the controller device. With a simple tap on the app, I sent the command to the microcontroller, activating the physical motor. In a matter of seconds the motor pressed down the power button on my PC to start it up.

The day was saved as my friends could now enjoy playing minecraft on our server. The Remote Rescuer not only provided a practical solution to a common problem but also showcased the power of IoT in creating personalized and efficient solutions for everyday challenges.

In the end, IoT had proven a practical solution to my problem, that is applicable for many more cases of remote access.