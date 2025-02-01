Description

This project is an Arduino-based LED blinking sequence that turns on and
off a set of LEDs in a loop. The LEDs are connected to digital pins 12,
11, 10, 9, and 8. The sequence turns each LED on with a delay, then
turns them off in the same order.

Code Explanation

The code defines a constant lightSpeed set to 1000 milliseconds (1
second), which determines the delay between turning LEDs on and off. The
setup() function initializes the digital pins 12, 11, 10, 9, and 8 as
outputs. The loop() function:

1\. Stores the LED pins in an array.

2\. Turns each LED on sequentially with a delay of lightSpeed.

3\. Turns each LED off sequentially with the same delay.

This creates a simple LED chasing effect.

Setup Instructions

Connect each LED anode (+) to Arduino pins 12, 11, 10, 9, and 8.

Connect the cathode (-) of each LED to a resistor (220Ω recommended).

Connect the other end of each resistor to the ground (GND) of the
Arduino.

Upload the provided code to the Arduino board.
