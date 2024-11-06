_**Home Automation Project Second Assignment**_

In the first part of our assignment, we discussed what is required for a home automation system in general. In the second part, we will elaborate on specifically what three home automation systems we mentioned below require and share their verilog codes.

Our _**first**_ home automation system provides a smart solution for enhancing safety by automatically shutting off the gas valve during an earthquake or fire. Such a system consists of essential components like integrated sensors, a control unit, and an automatic gas valve. The earthquake sensor measures the intensity of the tremor and sends a signal when it exceeds a predefined threshold; the fire sensor triggers an alarm upon detecting smoke or high temperatures. The control unit processes these signals from the sensors and ensures that the gas valve closes in case of an emergency. Setting up this system may require sensitive sensors, reliable and durable actuators, a secure network infrastructure for data transmission, and a backup power source.

_**The inputs:**_

Let x1 be the earthquake magnitude. If x1 is equal or greater than 4, x1  = 1; otherwise x1 =0.

Let x2 represent whether there is fire or not. If there is a fire, x2 = 1;  otherwise x2 =0.

__**The output:**_

Let y be the state of the gas valve. If the valve is open, y= 0;  otherwise y  = 1.


_**The truth table**_ created according to these values is below:

x1  |  x2 |  y1

0   | 0   |  0

0   | 1   |  1

1   |  0  |  0

1   |  1  |  0


_**The table above represents the ‘or’ gate.**_

Our _**second**_ home automation system provides a mechanism to automatically turn off lights when no one is home, enhancing energy efficiency. This type of system includes components such as motion sensors, presence detection technology, and smart light control units. The motion sensors and presence detection system determine whether anyone is at home; if no one is present, the control unit turns off the lights.  If we were to keep track of these changes by giving them binary values, this system would look like this:

_**The input:**_

Let x state whether anyone is at home or not. If anyone is home, x = 1;  otherwise, x = 0.

_**The output:**_

Let y be the state of lights. If the lights are on, y =1, otherwise y =0.

The truth table created according to these values is below:

x   |  y 

0   |  1

1   |  0

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

0  | 0  | 0

0  | 1  | 1

1  | 0  | 0

1  | 1  | 0

_**The truth table above can be represented as (not x1) and x2 in verilog description.**_

x1 | x2 | y2

0  | 0  | 0

0  | 1  | 0

1  | 0  | 0

1  | 1  | 1

_**The table above represents the ‘and’ gate.**_



