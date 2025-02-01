Description

This project includes an Arduino-based temperature and fire detection
system using a thermistor and an LED. The system reads the temperature
and, if it exceeds a specified threshold, the LED blinks as an alert.
The user can stop the blinking through the serial monitor.

Code Explanation Temperature Reading The code uses a thermistor
connected to analog pin A0 to measure temperature. The analog value from
the thermistor is converted into a resistance, and then the
Steinhart-Hart equation is used to calculate the temperature in Celsius.
This value is displayed in the Serial Monitor.

Analog Read: The analogRead(THERMISTOR_PIN) function reads the
thermistor value. Temperature Calculation: The thermistor\'s resistance
is calculated and used in the Steinhart-Hart equation to find the
temperature in Celsius. LED Blinking The LED connected to digital pin 12
blinks when the temperature exceeds the predefined threshold
(TEMP_THRESHOLD), which is set to 50°C. The LED blinks with a 100ms
delay when the temperature is above the threshold.

Threshold Check: If the temperature is greater than or equal to 50°C and
the stopBlinking flag is false, the LED blinks. Blinking Logic: The
digitalWrite(LED_PIN, HIGH) and digitalWrite(LED_PIN, LOW) control the
LED turning on and off, creating the blinking effect. Stop Command The
checkStopCommand() function listens for user input in the Serial
Monitor. If the user types \"stop\", the stopBlinking flag is set to
true, stopping the LED blinking.

Serial Monitor Input: The input from the Serial Monitor is read and
processed. If the input matches \"stop\", it halts the blinking
sequence.

Setup Instructions

Connect Thermistor:

1\. Connect the thermistor to analog pin A0 of the Arduino. 2. Connect
one end of the thermistor to the 5V pin and the other end to ground
through a 10kΩ resistor.

Connect LED:

1\. Connect the LED anode (+) to digital pin 12 on the Arduino. 2.
Connect the cathode (-) to a 220Ω resistor. 3. Connect the other end of
the resistor to ground (GND).

Upload Code:

1\. Upload the provided code to the Arduino board. 2. Open Serial
Monitor:

Open the Serial Monitor to view the real-time temperature readings. Type
\"stop\" in the Serial Monitor to stop the LED from blinking.
