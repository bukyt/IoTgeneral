# Module 2 Contract

**Student's Name(s):** Kennar Kahju, Joonas Tiitson

**Agreement:**

As students in this class, we agree to fulfill and present the results of a selection of the following tasks:

- (M) **What is in your kit?**
  - Get one Kit per pair from one of your friendly instructors.
  - Unpack and mark off all parts you find. While doing that also identify what the piece is good for and add potentially the wiring or bus system that it uses as an interface.
  - Create a table in Google Sheets and list all the parts. Link it in the shared pair-part of your portfolio.
  - Google some properties (speed, max length, number of cables needed, voltages, other notable properties) of the respective bus on the respective device - this is important for the next lecture.
  - Fill in the form when you receive the kit. [Form Link](https://forms.gle/BMuoYuQnnsd9DEEK8)

- (O) **Recompile from class:** Describe and sketch the general IoT architecture in detail. Mark, what is cloud, edge, etc., map to your own scenario/story.

- (O) **Compile information on the ESP ecosystem.** Basic Microcontrollers (ESP8266 and ESP32).
  - Google around and/or use your friendly AI.
  - ESP8266 video. [ESP8266 Video Link](https://youtu.be/wOEDaFRlhLo?si=ERGEnZ5NZ37XvrRa)
  - Wemos D1 Mini video. [Wemos D1 Mini Video Link](https://youtu.be/5WXPYWj-_a4?si=aN1WIzTkJIIBUl5E)
  - Why is this the “democratization of hardware”?

- (M) **Basic electronics prototyping (breadboard, jumper cables)** <- video [Video Link](https://youtu.be/yXirMBP3x4U?si=YiR1OVodxhQ-EjHL)
  - ”Hello breadboard” (leds and button - get power from Wemos D1 Mini plugged into usb power adapter from kit)
  - Create a RGB LED color mixer.

- (M) **Get to know Arduino IDE and the ESP8266 or ESP32.**
  - “Hello world”/Blink in C++ (led, compile for microcontroller with ArduinoIDE)
  - Blink video. [Blink Video Link](https://youtu.be/2nN_ZVyWLzg?si=EkluhBUelc4Rdhbg)
  - Variation(s) of blink with button.
  - Toggle Led with local button.
  - Meet the M5.
  - Take pictures and very brief notes for proof and documentation purpose.

(M) means Mandatory.

(O) means optional. We took 2 optional tasks and removed the other 2.

**Signature:** Confirm orally in lab with an instructor that you understand the content of this contract and are willing to put in the work for doing and presenting it. By uploading this markdown version to your repository you commit to the selections made in here.


# Tasks

1. We recieved kit number 9. Google Sheets link of our recieved parts: [here](https://docs.google.com/spreadsheets/d/1qb0uxTUjVfAXhcyMBwt0HGUkXmfpsmdn01q703IYodM/edit?usp=sharing)

2. Nodes are the end points of a IOT structure, such as lights, sensors and buttons. A gateway is a device that allows the items in a IOT network talk to other devices on some other network. It is also a edge device for the network. Devices in a network together form a cloud that can be accessed from the internet. In our example the phone is connected to the internet from which it can communicate with our home cloud
   ![Untitled](https://github.com/bukyt/IoTgeneral/assets/116277045/8d81ae8e-cd12-4c7b-8c85-2091deb48bc9)


3. esp32 is a series of low cost and power microcontrollers with wifi and dual mode bluetooth. They allow for low cost projects and exploring, are easy to program and connect with various external parts.  
ESP8266 - can use android or iot, attach a lot of stuff and sensors. Can connect to usb and power regulates easily. Cheap, as expensive as a coffee. Good to bridge gap of hardware and software.  
It is the democratization of hardware because it is cheap and modular, making it possible for anyone to get started with hardware. It is also cheap and is based on open source.

4. RGB Color mixer design - blue is always lit, but pressing a button shines either red or green into the mix and makes the color purple-ish or yellow-ish.
   ![Image](https://github.com/bukyt/IoTgeneral/assets/68914924/f5429e30-0d77-4986-b414-c7432e5ec3cd)

5. Blink was done according to the video instructions. (Pull-up) Button added to pin D1 to toggle between the external blinking LED.
   ![Image](https://github.com/bukyt/IoTgeneral/assets/68914924/8197da65-b253-42b5-a021-37500817382d)

[Videos of tasks 4&5](https://imgur.com/a/N7N7x5i)
