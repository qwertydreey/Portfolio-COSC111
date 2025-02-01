Description

This project contains multiple Arduino-based LED lighting effects. The
first activity involves a simple LED blinking sequence, while the second
activity introduces a fading LED effect. Each LED sequence is controlled
using different Arduino programming techniques.

Code Explanation

LED Blinking Sequence

The code defines a constant lightSpeed set to 1000 milliseconds (1
second), which determines the delay between turning LEDs on and off. The
setup() function initializes the digital pins 12, 11, 10, 9, and 8 as
outputs. The loop() function:

Stores the LED pins in an array.

Turns each LED on sequentially with a delay of lightSpeed.

Turns each LED off sequentially with the same delay.

This creates a simple LED chasing effect.

LED Fading Effect

The second activity implements a fading LED effect. The code:

Defines an array ledPins\[\] for LED pins 3, 5, 6, 9, and 10.

Initializes the pins as outputs in the setup() function.

In the loop() function:

Fades each LED in by gradually increasing brightness.

Fades each LED out by decreasing brightness.

Adjusts brightness dynamically using fadeAmount to reverse direction
when reaching 0 or 255.

Uses a helper function fadeLED(int pin, bool fadeIn) to handle the
fading effect.

Setup Instructions

For Blinking Sequence:

1\. Connect each LED anode (+) to Arduino pins 12, 11, 10, 9, and 8.

2\. Connect the cathode (-) of each LED to a resistor (220Ω
recommended).

3\. Connect the other end of each resistor to the ground (GND) of the
Arduino.

4\. Upload the provided code to the Arduino board.

For Fading Effect:

1\. Connect each LED anode (+) to Arduino pins 3, 5, 6, 9, and 10.

2\. Connect the cathode (-) of each LED to a resistor (220Ω
recommended).

3 Connect the other end of each resistor to the ground (GND) of the
Arduino.

4\. Upload the provided fading effect code to the Arduino board.
