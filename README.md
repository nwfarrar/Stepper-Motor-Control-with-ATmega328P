# Stepper-Motor-Control-with-ATmega328P
A circuit that controls the position of a stepper motor to follow the setting of a potentiometer. Two LEDs will be used to indicate when the motor is moving in the forward or backward direction.

Parts needed:
ATmega328P minimal circuit components
10kΩ resistors (1)
220Ω or 330Ω resistors (4) 
Connector wires
Potentiometer
Small stepper motor (1) 
H-Bridge chip (1)
LEDs (2) – two different colors 
Multimeter
H-bridge chip

Code Descritpion:
Program your controller such that it uses the input from the potentiometer as a joystick to control the stepper motor. That is, the stepper motor must move to a position determined by the potentiometer reading.
- If the sensor reads a low value (less than 1⁄2 range, <2.5V), the motor will move
to a proportional negative angle (a reading of zero must correspond to
approximately -180 degrees);
- if the sensor reads a high value (greater than 1⁄2 range, >2.5V) the motor will
move to a proportional positive angle (a reading of 5V must correspond to
approximately +180 degrees);
- if the sensor reads mid-range, the motor will move to zero degrees of rotation.

Note that since you will not know what the absolute angle of the motor upon startup (that is, when the circuit is powered on), assume that the startup position is zero. This is fine for our lab, because the motor is not attached to anything. Make all of the movements relative to that angle. So if the potentiometer reading is, say, 3.0V at startup, the motor will immediately start moving forward to match the set point. You may use full wave stepping.
Note that the motor may not be able to keep up as you adjust the sensor signal, so a lag between the sensor reading and motor position is expected, and your code will “walk” the motor in individual steps until the motor position corresponds to the current sensor value. In the previous example, the motor will start moving to match the 3.0V potentiometer signal that it sees upon startup, but if you change the potentiometer setting while the motor is moving – for example, reduce the setting to 2.7 volts before it gets to 3V – then it will just go to the new set point. Placing a delay after a given step helps to visualize the motion.
Program the microcontroller such that the LEDs are on to indicate the direction of motor motion – that is, the direction of the last step taken – using one LED for forward motion and one for backward motion. When the motor has reached its set point (to within some tolerance) the LEDs must be off.

