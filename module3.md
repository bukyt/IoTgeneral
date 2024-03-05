## Agreement:

As students in this class, we agree to fulfill and present the results of a selection of the following tasks (we are picking at least 3 of the optional tasks):

- (M) Fill in the form [here](https://forms.gle/Pvaw8h5CDU1GrySaA) when picking up hardware (e.g., Laptop or Raspberry Pi).
  - (M) Set up an Access Point using an old laptop (completed in the classroom). For more advanced alternatives, consult with us. Options include using an OpenWrt router, Raspberry Pi, Atomic Pi, and ESP AP.

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
