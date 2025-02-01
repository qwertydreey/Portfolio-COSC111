Description

This project contains multiple Arduino-based functionalities. The first activity involves a simple LED blinking sequence, the second activity introduces a fading LED effect, the third activity implements a fire detection system using a thermistor and a photoresistor, the fourth activity introduces a temperature monitoring system with a stop command, the fifth activity implements a button press detection system, the sixth activity introduces a serial-controlled LED system, the seventh activity implements an automatic/manual light intensity-based LED control system, and the eighth activity introduces a button-triggered serial message system.


Code Explanation

LED Blinking Sequence

The code defines a constant `lightSpeed` set to 1000 milliseconds (1 second), which determines the delay between turning LEDs on and off. The `setup()` function initializes the digital pins 12, 11, 10, 9, and 8 as outputs. The `loop()` function:

1. Stores the LED pins in an array.
1. Turns each LED on sequentially with a delay of `lightSpeed`.
1. Turns each LED off sequentially with the same delay.

This creates a simple LED chasing effect.


LED Fading Effect

The second activity implements a fading LED effect. The code:

1. Defines an array `ledPins[]` for LED pins 3, 5, 6, 9, and 10.
1. Initializes the pins as outputs in the `setup()` function.
1. In the `loop()` function:
- Fades each LED in by gradually increasing brightness.
- Fades each LED out by decreasing brightness.
- Adjusts brightness dynamically using `fadeAmount` to reverse direction when reaching 0 or 255.

4\. Uses a helper function `fadeLED(int pin, bool fadeIn)` to handle the fading effect.


Fire Detection System

The third activity uses a thermistor and a photoresistor to detect fire. The code:

1. Reads temperature using a thermistor and converts the analog value to Celsius.
1. Reads brightness using a photoresistor.
1. Prints temperature and brightness values to the Serial Monitor.
1. If both the temperature exceeds `TEMP\_THRESHOLD` (50°C) and brightness exceeds `BRIGHTNESS\_THRESHOLD` (220), the LED blinks to indicate a fire warning.
1. Otherwise, the LED remains off.


Temperature Monitoring System with Stop Command

The fourth activity introduces a temperature monitoring system that allows stopping the LED blinking via serial input. The code:

1. Reads temperature using a thermistor and converts it to Celsius.
1. Prints temperature readings to the Serial Monitor.
1. Checks for a stop command (`"stop"`) from the Serial Monitor.
1. If the temperature exceeds `TEMP\_THRESHOLD` (50°C) and no stop command is issued, the LED blinks rapidly.
1. If a stop command is received, the LED stops blinking.
1. Prevents divide-by-zero errors by handling invalid readings.


Button Press Detection System

The fifth activity implements a button press detection system. The code:

1. Reads the state of a button connected to digital pin 12.
1. Uses the built-in pull-up resistor to ensure accurate readings.
1. Prints `"1"` when the button is pressed and `"0"` when it is not.
1. Uses a delay to prevent excessive spamming of serial output.


Serial-Controlled LED System

The sixth activity introduces a serial-controlled LED system. The code:

1. Reads serial input to turn an LED on or off.
1. If the user sends `"1"`, the LED turns on and a confirmation message is printed.
1. If the user sends `"0"`, the LED turns off and a confirmation message is printed.
1. The LED is connected to pin 13, and serial communication is used for control.


Automatic/Manual Light Intensity-Based LED Control System

The seventh activity implements an automatic and manual light intensity-based LED control system. The code:

1. Reads light intensity from a photoresistor connected to analog pin A0.
1. Converts the sensor value into a percentage for better readability.
1. Uses three LEDs (Green, Yellow, Red) connected to pins 11, 12, and 13 respectively.
1. Allows switching between automatic and manual mode via Serial commands (`"MODE AUTO"` or `"MODE MANUAL"`).
1. In manual mode, allows setting light intensity thresholds (`"SET LOW <value>"` and `"SET HIGH <value>"`).
1. Adjusts LED output based on the light intensity percentage.


Button-Triggered Serial Message System

The eighth activity introduces a button-triggered serial message system. The code:

1. Reads the state of a button connected to digital pin 12.
1. Uses the internal pull-up resistor to ensure accurate readings.
1. Sends `"group1\_on"` when the button is pressed and `"group1\_off"` when the button is released.
1. Uses a delay to control the frequency of message sending and avoid excessive output.


Setup Instructions

(Add setup instructions for the new activity here, following the format of previous sections)
