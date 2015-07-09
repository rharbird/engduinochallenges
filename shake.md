{% include "./header.md" %}

# Task 3.5: Shake 

| Level| Points | Uses |
| ------ |:------:|------|
| Hard | 3 | LEDs, Accelerometer|

## Mission
Make the LEDs light up  when you shake the Engduino.  

Sometimes you want to do something when a sensor value is above or below a * threshold *. In this challenge you will turn some of the LEDs on when you shake the Engduino. First you need to calculate the overall acceleration when the board is still and then you need to see what happens when you shake the board. Use the information in the ** ACCELEROMETER ** sheet to work out how to do this.

## You will need
* An Engduino.
* The ** ENGDUINO LIBRARIES: THE LEDS ** sheet.
* The ** ENGDUINO LIBRARIES: ACCELEROMETER ** sheet.
* The ** ENGDUINO LIBRARIES: IF STATEMENTS ** sheet.

## Method
1. Read the ** ENGDUINO LIBRARIES: THE LEDS ** sheet,  the ** ACCELEROMETER ** sheet and the sheet about ** IF STATEMENTS **.
3. Open a new sketch.
4. Save the sketch with a new name: ```shake```.
5. Write some code to calculate the overall acceleration print it to the serial monitor. 
6. Open the serial monitor. Can you see the values being printed? 
7. Write down the value of the acceleration when the device is flat on the table.
8. Shake the Engduino. What is the accelerometer reading now?  Decide where you want your threshold to be.
9. Add some more code so that the LEDs light up when the accelerometer value reaches the threshold. You should use an ```if``` statement. 
12. Put in a short delay just before the end of the main loop and turn all the LEDs ```OFF```.



Congratulations! Collect your points for this challenge.

<!---
{% include "./rae.md" %}
-->
