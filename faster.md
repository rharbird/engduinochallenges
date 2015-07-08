{% include "./header.md" %}

# Task 2.2: Faster and faster 
| Level| Points | Uses |
| ------ |:------:|------|
| Medium | 2 | LEDs |

## Mission

Make a single LED go around the board faster and faster.  

## You will need
* An Engduino.
* The ** ENGDUINO LIBRARIES: THE LEDS ** sheet.

## Method
1. Read the ** ENGDUINO LIBRARIES: THE LEDS ** sheet.
3. Open a new sketch.
4. Save the sketch with a new name: ```faster```.
5. First of all, make an LED run around the board by lighting up the LEDs in sequence with a delay in between.  
6. When you have that working, you need to gradually reduce the delay so that the LEDs move faster and faster. Start by creating a variable for the delay, let's call it ```myDelay```. You need to put this underneath the ```#include``` statements at the top of the sketch so that it looks like this:

	```
	#include <EngduinoLEDs.h>

	int myDelay = 1000;

	void setup() 
	{
		EngduinoLEDs.begin();
	}
	```

7. Now use your myDelay variable to set the delay like this:

	```
	delay(myDelay);
	```

8. To finish the challenge, you need to reduce the delay every time you go round the loop. To reduce the delay by 50 milliseconds, you should do this:

	```
	myDelay = myDelay - 50;
	```

9. For 2 bonus points, reset myDelay when it reaches zero.


Continue until you have completed the challenge.





Congratulations! Collect your points for this challenge.

<!---
{% include "./rae.md" %}
-->
