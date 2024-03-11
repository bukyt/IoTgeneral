## Agreement:

As students in this class, we agree to fulfill and present the results of a selection of the following tasks (we are picking at least 3 of the optional tasks):

- (M) Fill in the form [here](https://forms.gle/Pvaw8h5CDU1GrySaA) when picking up hardware (e.g., Laptop or Raspberry Pi).
  - (M) Set up an Access Point using an old laptop (completed in the classroom).

- (O) Connect a button to an LED directly on the microcontroller. Adjust resistance, use PULLUP/PULLDOWN, and V.Divider as needed.
    - Learn about PULLUP/PULLDOWN resistors. 
    - What is the option INPUT_PULLUP?
- Connect a computer (browser or phone) to the microcontroller via Web request.
    - (M) Connect a computer (browser or phone) to the microcontroller's onboard LED via Web request.
    - (O) Enable WiFi and HTTP on the microcontroller to consume the web endpoint of another microcontroller. The button turns on the onboard LED on the other microcontroller.
    - (O) Connect a button to a Webhook, then use Webhook to curl to LED. (Integration step). 
        - What is the advantage of having a gateway in the middle?

- (M) Perform SSH key exchange so that every team member can log in without a password.
    - (M) Set up a central team git repository on the gateway with the option to pull. Implement a small stack to automate the pull via SSH from one of your laptops.

## Tasks:
1. We recieved the laptop and set up an access point in the classroom.

2. Pressing the button turns off the LED. Button is connected in a pull-up configuration.
   ![IMG_20240305_134500731 MP](https://github.com/bukyt/IoTgeneral/assets/68914924/f179a342-80da-45f8-8697-be2d0b375775)
   
![IMG_20240305_134502501 MP](https://github.com/bukyt/IoTgeneral/assets/68914924/605a5668-ed5a-4aa5-9e58-24d515c61c16)

3.1. We did the task, but no images. Can show in class. 
3.2. The LED is running the previous task program, and the button is blinking the LED when button is held down.
![IMG_20240305_134728173](https://github.com/bukyt/IoTgeneral/assets/68914924/ba27c9de-4361-4bca-995f-c64b1dbc740f)
![IMG_20240305_134731814 MP](https://github.com/bukyt/IoTgeneral/assets/68914924/7ccccc25-3033-47bb-9fa3-3a32a907c8ca)

3.3. ![Video shows it all](https://imgur.com/a/A5B6erD). Pressing the button turns on the LED until held. Let go, and the LED turns off.

4. SSH key exchange is done, can log in without a password.
4.1. Central repository is set up and one laptop has a script to pull via SSH. Can modify as needed.
