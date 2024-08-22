# Rainbow 6: Siege Recon Drone using Arduino

***Disclaimer: I have used multiple sources to make this project; it is merely a how-to as this project seems to not be documented clearly.***

---

#### Credits

- For the drone's 3d printed body, I found [this repo](https://github.com/Jangberry/Drone-rainbow-six) by @Jangberry. The specific files used are gone into in detail in this repo below. 
- For the drone code, I adapted a script [I found on CircuitBest](https://circuitbest.com/how-to-make-bluetooth-controlled-car-using-arduino/) into a two-wheeled variant to fit this drone.
- I used the app "Arduino Car" on the Google Play Store to RC the drone using bluetooth.

---

#### Components needed

- Access to a 3D printer
- 300g-ish of Black PLA (or you could spray paint, but not recommended)
- A computer
- An android to control the drone
- An Arduino microcontroller (I recommend the nano for size and price)
- Two DC motors
- Two Mecanum wheels (coloured / sprayed black)
- L298N Motor Driver
- HC-05 Bluetooth PCB
- Jumper wires (M-M, M-F, F-F)
- Toggle switch
- 18650 2 Slot battery holder
- 18650 Rechargeable Batteries
- Superglue

---

#### Schematic
<img width="673" alt="image" src="https://github.com/user-attachments/assets/bcb118f8-95db-458b-b181-f3a3a1d9b6b4">

If that was a bit unclear, the connections are listed underneath anyway in the Wiring section:

---

#### Wiring
- L298N OUT1 to Motor 1 negative
- L298N OUT2 to Motor 1 positive
- L298N OUT3 to Motor 2 positive
- L298N OUT4 to Motor 2 negative
- Batteries positive to switch to L298N +12V
- Batteries negative to GND to L298N GND
- L298N GND to Arduino GND
- L298N +5V to Arduino Vin
- L298N IN1, 2, 3, 4 to Arduino Digital pins 11, 10, 9, 8 (Respectively)
- HC05 RX to Arduino TX
- HC05 TX to Arduino RX 
- HC05 VCC to Arduino 5V
- HC05 GND to Arduino GND


---

#### Instructions:

- Connect the circuit as shown in the Schematic/Wiring Section[s].
- Upload the code to the Arduino board. *Note: while you upload the code you **must** unplug all pins of the HC05 module. Replug after code is uploaded.*
- Verify sucess by opening the "Arduino Car" app and connecting to the HC05 via bluetooth. If help is needed, tutorials are avalible on youtube. The password will be ***1234***.
- After verifying the circuit works, turn it off with the master switch we installed earlier on the positive pole of the battery.
- 3D-Print the files in the 3DPrints section at a 60% size in Black PLA with a brim and with supports.
- Put the circuit in the 3D-Printed enlosure of the drone.
- Cut out a slot for the switch to go in.
- Adhesify the battery holder to a seperate half than the other Components, allowing easy access to recharge the batteries.
- Install the Mecanum wheels, which should have been [sprayed] black using superglue onto the DC Motor wheels.
- Superglue the two DC Motors onto the seperate flaps on the bottom part of the drone.
- Slot and superglue the leg to the corresponding slot.
- Now, put the circuit in the drone and close the enclosure. Magnets would work well to allow easy access to the drone batteries for recharging. 
- Turn on the switch and verify connectivity with the mobile phone. Drone should respond and move to the phone's commands.
- If the drone moves oppositely to the phone's commands, reverse the polarity of the motors and retry.

Success!
