_**Home Automation Project Second Assignment**_

In the first part of our assignment, we discussed what is required for a home automation system in general. In the second part, we will elaborate on specifically what three home automation systems we mentioned below require and share their verilog codes.

Our _**first**_ home automation system provides a smart solution for enhancing safety by automatically shutting off the gas valve during an earthquake or fire. Such a system consists of essential components like integrated sensors, a control unit, and an automatic gas valve. The earthquake sensor measures the intensity of the tremor and sends a signal when it exceeds a predefined threshold; the fire sensor triggers an alarm upon detecting smoke or high temperatures. The control unit processes these signals from the sensors and ensures that the gas valve closes in case of an emergency. Setting up this system may require sensitive sensors, reliable and durable actuators, a secure network infrastructure for data transmission, and a backup power source.

_**The inputs:**_

Let x1 be the earthquake magnitude. If x1 is equal or greater than 4, x1  = 1; otherwise x1 =0.

Let x2 represent whether there is fire or not. If there is a fire, x2 = 1;  otherwise x2 =0.

_**The output:**_

Let y be the state of the gas valve. If the valve is open, y= 0;  otherwise y  = 1.


_**The truth table**_ created according to these values is below:

x1 | x2 | y
-- | -- | --
0  | 0  | 0
0  | 1  | 1
1  | 0  | 1
1  | 1  | 1


_**The table above represents the ‘or’ gate.**_

Our _**second**_ home automation system provides a mechanism to automatically turn off lights when no one is home, enhancing energy efficiency. This type of system includes components such as motion sensors, presence detection technology, and smart light control units. The motion sensors and presence detection system determine whether anyone is at home; if no one is present, the control unit turns off the lights.  If we were to keep track of these changes by giving them binary values, this system would look like this:

_**The input:**_

Let x state whether anyone is at home or not. If anyone is home, x = 1;  otherwise, x = 0.

_**The output:**_

Let y be the state of lights. If the lights are on, y =1, otherwise y =0.

The truth table created according to these values is below:

x | y
-- | --
0  | 1
1  | 0

_**The table above represents the ‘not’ gate.**_

Our _**third**_ home automation system’s purpose is to help people wake up to the perfect morning with the help of a system installed in their own bedroom. The user chooses a specific time according to their preferences to wake up while setting our system up.

If the illuminance outside is below 100 lux and is the right time, the system turns on the lights.

If the illuminance outside is above 100 lux and is the right time, the system opens the curtains.

If it is not the right time, the system does nothing, regardless of the illuminance.

The sensors we will use to make this system can be listed as such: smart switches for lights, motorized curtain rollers, a real time clock module to accurately keep track of time, and lastly a lux sensor to determine the illuminance outside. If we were to keep track of these changes by giving them binary values, this system would look like this:

_**The inputs:**_

Let x1 be the lux outside. If  x1 is less than 100 lux, x1 = 0; otherwise x1 = 1.

Let x2 be the time. If x2 is less than 11.30 am, x2 = 1; otherwise x2 = 0.

_**The outputs:**_

Let y1 be the state of curtains. If the curtains are opened, y1 = 1; otherwise y1 = 0.

Let y2 be the state of lights. If the lights are on, y2 = 1; otherwise y2 = 0.

Therefore, if we want to express its working principle in _**truth table**_, it will look like this:

x1 | x2 | y1
-- | -- | --
0  | 0  | 0
0  | 1  | 1
1  | 0  | 0
1  | 1  | 0

_**The truth table above can be represented as (not x1) and x2 in verilog description.**_

x1 | x2 | y2
-- | -- | --
0  | 0  | 0
0  | 1  | 0
1  | 0  | 0
1  | 1  | 1

_**The table above represents the ‘and’ gate.**_

Our _**fourth**_ home automation system is a plant irrigation system and it provides a smart solution for each plant that receives water on specific days based on its required watering frequency. The system consists of watering valves, a control unit, and a weekly irrigation schedule.Each plant is watered on specific days of the week. For example, Plant A is watered three times per week, while Plant B is watered twice per week. This ensures an ideal watering balance for each plant.It includes a control unit and the control unit initiates watering based on the day of the week, ensuring each plant is watered on its designated days.It includes watering valves When a plant’s watering day arrives, the control unit signals the appropriate valve to open, starting the irrigation process.

_**System inputs and outputs:**_

_**Inputs:**_

Day (day): The days of the week, represented by numbers 0 to 6 (from Monday to Sunday).

_**Outputs:**_

Watering Status (water): Set to 1 on the days each plant is watered, and 0 on other days.

The truth table created according to these values is below:

Day | Plant A | Plant B | Plant C | Plant D
----|---------|---------|---------|---------
000 |    1    |    0    |    1    |    0
001 |    0    |    1    |    0    |    0
010 |    1    |    0    |    0    |    1
011 |    0    |    0    |    1    |    0
100 |    1    |    1    |    0    |    0
101 |    0    |    0    |    0    |    0
110 |    0    |    0    |    0    |    0

Since we do not know the exact features of the card, we do not take into account the weight sensor and the amount of spilled water.


Our _**fifth**_ home automation system provides a secure door lock system. The system ensures that the door unlocks only when the correct authentication methods are followed, providing both high security and emergency flexibility. It uses facial recognition, password verification, and manual override to control the door output. Its working principle is stated as below.

The password consists of 4-bits. All the 4 digits need to be correct for the password to be correct.

If the password is correct and the face recognition is valid, the door unlocks. 

If either the password is incorrect or face recognition fails, the door will stay locked.

The manual override allows the door to be unlocked regardless of the authentication result. If the manual override is activated, the system will unlock the door.

The final output is determined by the XOR gate logic, ensuring that only one of the two conditions (keyless unlock or manual override) can unlock the door at any given time.

The _**sensors**_ used in this system are:

_**Password Input Sensors:**_
 
These are keypad sensors that allow the user to enter a 4-digit password. The keypad will detect each keypress and send the corresponding signal (binary value) to the system.

_**Face Recognition Sensor:**_

This can be an optical or infrared camera combined with facial recognition software or hardware.

_**Manual Override Switch:**_

This can be done by installing a key operated switch near the door lock. This switch should be wired to the manual override switch. When the key is turned, it should complete the circuit, sending a signal to the manual override input.

_**Inputs:**_

Let P0, P1, P2, P3 represent the 4 digits of the password and let password_ok be equal to 1 if and only if all the four digits are correct.

Let Face_recognition be equal to 1 if the face is successfully recognized; otherwise Face_recognition = 0.

Let manual_override switch be equal to 1 if the switch is successfully activated; otherwise, maual_override = 0.

_**Internal Signal:**_
 
Let keyless_unlock be equal to 1 only when both Face_recognition and password_ok conditions are fulfilled; otherwise, keyless_unlock = 0.

_**Outputs:**_

Let door_lock be equal to 1 when either keyless_unlock or manual_override conditions are met but not simultaneously; otherwise, door_luck = 0.


P0 | P1 | P2 | P3 | Password_ok
-- | -- | -- | -- | ------------
0 | 0 | 0 | 0 | 0
0 | 0 | 0 | 1 | 0
0 | 0 | 1 | 0 | 0
0 | 0 | 1 | 1 | 0
0 | 1 | 0 | 0 | 0
0 | 1 | 0 | 1 | 0
0 | 1 | 1 | 0 | 0
0 | 1 | 1 | 1 | 1
1 | 0 | 0 | 0 | 0
1 | 0 | 0 | 1 | 0
1 | 0 | 1 | 0 | 0
1 | 0 | 1 | 1 | 0
1 | 1 | 0 | 0 | 0
1 | 1 | 0 | 1 | 0
1 | 1 | 1 | 0 | 0 
1 | 1 | 1 | 1 | 1

_**The truth table above can be obtained through and gate.**_

Password_OK | Face_recognition | Keyless_unlock
-- | -- | --
0 | 0 | 0
0 | 1 | 0
1 | 0 | 0
1 | 1 | 1

_**The truth table above can be obtained through and gate.**_

Keyless_unlock | Manual Override | Door_output
-- | -- | --
0 | 0 | 0
0 | 1 | 1
1 | 0 | 1
1 | 1 | 0

_**The truth table above can be obtained through xor gate.**_
