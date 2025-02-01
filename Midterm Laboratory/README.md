Description

This project contains multiple Arduino-based functionalities. The first
activity involves a simple LED blinking sequence, the second activity
introduces a fading LED effect, the third activity implements a fire
detection system using a thermistor and a photoresistor, the fourth
activity introduces a temperature monitoring system with a stop command,
the fifth activity implements a button press detection system, the sixth
activity introduces a serial-controlled LED system, and the seventh
activity implements an automatic/manual light intensity-based LED
control system.

Code Explanation

LED Blinking Sequence

The code defines a constant \`lightSpeed\` set to 1000 milliseconds (1
second), which determines the delay between turning LEDs on and off. The
\`setup()\` function initializes the digital pins 12, 11, 10, 9, and 8
as outputs. The \`loop()\` function:

1\. Stores the LED pins in an array. 2. Turns each LED on sequentially
with a delay of \`lightSpeed\`. 3. Turns each LED off sequentially with
the same delay.

This creates a simple LED chasing effect.

LED Fading Effect

The second activity implements a fading LED effect. The code:

1\. Defines an array \`ledPins\[\]\` for LED pins 3, 5, 6, 9, and 10. 2.
Initializes the pins as outputs in the \`setup()\` function. 3. In the
\`loop()\` function:  - Fades each LED in by gradually increasing
brightness.  - Fades each LED out by decreasing brightness.  - Adjusts
brightness dynamically using \`fadeAmount\` to reverse direction when
reaching 0 or 255. 4. Uses a helper function \`fadeLED(int pin, bool
fadeIn)\` to handle the fading effect.

Fire Detection System

The third activity uses a thermistor and a photoresistor to detect fire.
The code:

1\. Reads temperature using a thermistor and converts the analog value
to Celsius. 2. Reads brightness using a photoresistor. 3. Prints
temperature and brightness values to the Serial Monitor. 4. If both the
temperature exceeds \`TEMP_THRESHOLD\` (50°C) and brightness exceeds
\`BRIGHTNESS_THRESHOLD\` (220), the LED blinks to indicate a fire
warning. 5. Otherwise, the LED remains off.

Temperature Monitoring System with Stop Command

The fourth activity introduces a temperature monitoring system that
allows stopping the LED blinking via serial input. The code:

1\. Reads temperature using a thermistor and converts it to Celsius. 2.
Prints temperature readings to the Serial Monitor. 3. Checks for a stop
command (\`\"stop\"\`) from the Serial Monitor. 4. If the temperature
exceeds \`TEMP_THRESHOLD\` (50°C) and no stop command is issued, the LED
blinks rapidly. 5. If a stop command is received, the LED stops
blinking. 6. Prevents divide-by-zero errors by handling invalid
readings.

Button Press Detection System

The fifth activity implements a button press detection system. The code:

1\. Reads the state of a button connected to digital pin 12. 2. Uses the
built-in pull-up resistor to ensure accurate readings. 3. Prints
\`\"1\"\` when the button is pressed and \`\"0\"\` when it is not. 4.
Uses a delay to prevent excessive spamming of serial output.

Serial-Controlled LED System

The sixth activity introduces a serial-controlled LED system. The code:

1\. Reads serial input to turn an LED on or off. 2. If the user sends
\`\"1\"\`, the LED turns on and a confirmation message is printed. 3. If
the user sends \`\"0\"\`, the LED turns off and a confirmation message
is printed. 4. The LED is connected to pin 13, and serial communication
is used for control.

Automatic/Manual Light Intensity-Based LED Control System

The seventh activity implements an automatic and manual light
intensity-based LED control system. The code:

1\. Reads light intensity from a photoresistor connected to analog pin
A0. 2. Converts the sensor value into a percentage for better
readability. 3. Uses three LEDs (Green, Yellow, Red) connected to pins
11, 12, and 13 respectively. 4. Allows switching between automatic and
manual mode via Serial commands (\`\"MODE AUTO\"\` or \`\"MODE
MANUAL\"\`). 5. In manual mode, allows setting light intensity
thresholds (\`\"SET LOW \<value\>\"\` and \`\"SET HIGH \<value\>\"\`).
6. Adjusts LED output based on the light intensity percentage:  - Green
LED turns on when light intensity is below the low threshold.  - Yellow
LED turns on when light intensity is between the low and high threshold.
 - Red LED turns on when light intensity exceeds the high threshold. 7.
Prints real-time light intensity, mode status, and environment
conditions to the Serial Monitor.

Setup Instructions

1\. \*\*For Blinking Sequence:\*\*  - Connect each LED anode (+) to
Arduino pins 12, 11, 10, 9, and 8.  - Connect the cathode (-) of each
LED to a resistor (220Ω recommended).  - Connect the other end of each
resistor to the ground (GND) of the Arduino.  - Upload the provided code
to the Arduino board.

2\. \*\*For Fading Effect:\*\*  - Connect each LED anode (+) to Arduino
pins 3, 5, 6, 9, and 10.  - Connect the cathode (-) of each LED to a
resistor (220Ω recommended).  - Connect the other end of each resistor
to the ground (GND) of the Arduino.  - Upload the provided fading effect
code to the Arduino board.

3\. \*\*For Fire Detection System:\*\*  - Connect a thermistor to analog
pin A0.  - Connect a photoresistor to analog pin A2.  - Connect an LED
to digital pin 12.  - Upload the provided fire detection system code to
the Arduino board.  - Open the Serial Monitor to view real-time
temperature and brightness values.

4\. \*\*For Temperature Monitoring System with Stop Command:\*\*  -
Connect a thermistor to analog pin A0.  - Connect an LED to digital pin
12.  - Upload the provided temperature monitoring system code to the
Arduino board.  - Open the Serial Monitor to view temperature readings.
 - Type \`\"stop\"\` in the Serial Monitor to stop the LED blinking.

5\. \*\*For Button Press Detection System:\*\*  - Connect a button to
digital pin 12.  - Ensure one side of the button is connected to GND and
the other to pin 12.  - Upload the provided button press detection code
to the Arduino board.  - Open the Serial Monitor to view button press
states.

6\. \*\*For Serial-Controlled LED System:\*\*  - Connect an LED to
digital pin 13.  - Upload the provided serial-controlled LED code to the
Arduino board.  - Open the Serial Monitor and send \`\"1\"\` to turn the
LED on.  - Send \`\"0\"\` to turn the LED off.  - The Serial Monitor
will confirm the LED status.

7\. \*\*For Automatic/Manual Light Intensity-Based LED Control
System:\*\*  - Connect a photoresistor to analog pin A0.  - Connect LEDs
to digital pins 11, 12, and 13.  - Upload the provided light
intensity-based LED control code to the Arduino board.  - Open the
Serial Monitor to switch between automatic and manual modes and adjust
settings as needed.
