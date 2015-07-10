{% include "./header.md" %}

# Task 1.5: Random colours 
| Level| Points | Uses |
| ------ |:------:|------|
| Medium | 2 | LEDs |

## Mission

Set all the LEDs to a random colour, delay for one second then repeat with a different colour.

## You will need
* An Engduino.
* The ** ENGDUINO LIBRARIES: THE LEDS ** sheet.

## Method
1. Read the ** ENGDUINO LIBRARIES: THE LEDS ** sheet.
3. Open a new sketch.
4. Save the sketch with a new name: ```randomLEDs```.
5. You need to make all the LEDs light up in a randomly generated colour.  We know that you can mix  your own colours using values for red, green and blue.  You need to generate a random value for red, green and blue using the ```random``` function. The random function returns a random number in a range you specify like this:
	```
	int r =  random(0,16);
	int g =  random(0,16);
	int b =  random(0,16);

	```
	This code returns a random number for each of the variables r, g, b in the range that is one less than the second number in the brackets.

6. Make the LEDs light up with the colour.

Continue until you have completed the challenge.



Congratulations! Collect your points for this challenge.

<!---
{% include "./rae.md" %}
-->
