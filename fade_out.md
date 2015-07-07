{% include "./header.md" %}

# Task: Fade out 
| Level| Maximum Points | Uses |
| ------ |:------:|------|
| Medium | 2 plus 2 bonus points | LEDs |

## Mission
Make the LEDs fade in and out.

## You will need
* An Engduino.
* The ** ENGDUINO LIBRARIES: THE LEDS ** sheet.

## Method
Set all the LEDs to any colour then delay for one second. Repeat but reduce the b.
1. Read the ** ENGDUINO LIBRARIES: THE LEDS ** sheet.
3. Open a new sketch.
4. Save the sketch with a new name: ```fade```.
5. Underneath the ```include``` statements at the top, you should create a variable to control the brightness like this:
	```
	int b =  15; // This is the brightness level.

	```
6. In the main loop, set the LEDs to any colour you like with the brightness level set to ```b```.
7. Subtract 1 from b like this:
	```b = b - 1;```
8. Add a delay of half a second. 
9. For an extra 2 points, reset ```b``` to 15 every time it reaches ```0```. Hint: use an ```if``` statement. 
10. Remember to ask one of the judges if you need help.


Continue until you have completed the challenge.



Congratulations! go and collect your points for this challenge.

<!---
{% include "./rae.md" %}
-->
