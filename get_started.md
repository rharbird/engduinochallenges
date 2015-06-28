# Get Started

## Introduction
The Engduino is just a simple, small, computer that is capable of measuring quite a lot of interesting things about the real world and that has a bunch of LEDs that can be used to provide feedback to the user. This is a step-by-step guide to creating a very simple program and watching that run. 


## Overview of the Engduino board
For those who know about these things, the Engduino is, at heart, an Arduino (just a brand of simple computer). Your Engduino board comes pre-fitted with some sensors and LEDs so we can get straight into experimenting with programming the board without needing to do any construction beforehand.


| ![Front ](front.JPG) | ![Back](back.JPG)|
|-----|------|
| Top | Bottom |


Figure 1: The top and bottom of your Engduino
 

On the one side of your Engduino you have 16 LED lights that have adjustable brightness and can be set to various mixtures of the three primary colours (of light): Red, Green and Blue.
 

![](engduino.jpg)


Figure 2:  16 Red, Green, Blue LEDs on one side of the board


The LEDS are numbered 0 – 15 and their exact positions can be seen in ???. Also on this side of the board we have a thermistor which can be used to detect temperature and a light sensor. On the other side we have a battery holder where we can install a battery. 

## Your first app
For your first exercise you are going to write a program in your Arduino IDE and then upload it to your Engduino board. If this is a lab class, your Arduino IDE should be open for you already. If not, just double click on the blue Arduino icon on your computer. You should see a window like that shown below:



![](ide.png)

Now we’re going to write a program. Type the following into the white box. Try to type as accurately as you can. Notice that ```All``` is spelt with an upper case ```A``` and lower case ```ll```.

```
#include  <EngduinoLEDs.h>

void setup()
{
  EngduinoLEDs.begin();
}


void loop()
{
  EngduinoLEDs.setAll(GREEN);
}

```
Now let’s make it run…. make sure your Engduino is plugged in. Click on the upload button:


![](ide1.jpg)


This checks your code for some types of error, turns it into something that a machine can understand, and then uploads it to the Engduino board. If there are errors they will appear in the black section in red.

Voila – your first Engduino program.


## Looking a bit closer
Now let’s take a quick look at some interesting parts of the basic app code and see how we can customise, personalise or enhance it.

```#include  <EngduinoLEDs.h>```

This lets your program use the LEDs. If you wanted to use the button you would have change this to be ```#include <EngduinoButton.h>```, and if you wanted to use both, you would need to have both there. There is at least one ```#include``` for each of the sensors on the Engduino.

The next part of the program is:

```
void setup()
{
  EngduinoLEDs.begin();
}
```

This is a function. A function is similar to the ones you may have experienced in mathematics. It can take some value/s and returns another value after it executes. void is what the function returns (nothing in this case), then comes the function name (setup in this case) and then brackets that contain the values we pass to the function (none in this case, so the brackets are empty.) The curly brackets delimit our code, so in a file with many functions everything within the set of curly brackets just after our function name belongs to that function. Our function ```setup()``` has just one line ```EngduinoLEDs.begin();```

This line tells the EngduinoLEDs object to run the function begin(), which gets the LEDs started so we can play with them. The semi-colon at the end of the line is common to many programming languages and signals to the computer that is the end of one instruction. Don’t forget these when you start writing your own code . The setup function runs exactly once, when the program starts.
The next function:
```
void loop()
{
  EngduinoLEDs.setAll(GREEN);
}
```

is called ```loop()```. The loop function is run repeatedly – and it’s where we put most of the instructions we want our Engduino to perform. In this case, it’s just one thing: ```EngduinoLEDs.setAll(GREEN);```

This line tells the ```EngduinoLEDs``` object to execute the function ```setAll()```. We pass this function a value, namely what colour to make the LEDs (green in this case). It doesn’t return a value but simply does what you tell it, and switches the LEDs on.
This line will actually be executed over and over as fast as the Engduino can go  – but since it always does the same thing, you won’t see any change.

##Personalise your app

###Change the colour
The function ```setAll()``` can be given a number of different values including: RED, GREEN, and BLUE. Go ahead and delete the word GREEN inside the brackets and replace it with the colour of your choice all in capital letters. For example if you prefer red, your app will look like this.

```
#include  <EngduinoLEDs.h>

void setup()
{
  EngduinoLEDs.begin();
}


void loop()
{
  EngduinoLEDs.setAll(RED);
}
```
When you’ve done that, click the upload button, as before, to upload your code. The LEDs will now be lit according to the colour you choose. Well done!
##Blink
###Delay
The Engduino has a function built in called delay(). This function takes a number which tells the board to wait those number of milliseconds (remember a millisecond is one thousandth of a second) before executing the next instruction in your program. We are going to use this useful little function to make our Engduino blink.
Just below the line: ```EngduinoLEDs.setAll(RED);```

add the lines:
```
  delay(2000);
  EngduinoLEDs.setAll(OFF);
  delay(1000);
```
Don’t forget your semi-colons! Your code should now look something like this.  (With the colour you chose instead of RED if you chose something else.)
```
#include  <EngduinoLEDs.h>

void setup()
{
  EngduinoLEDs.begin();
}


void loop()
{
  EngduinoLEDs.setAll(RED);
  delay(2000);
  EngduinoLEDs.setAll(OFF);
  delay(1000);
}
```
Go ahead and program the Engduino with your code. You should see your Engduino now rhythmically blinking the LEDs in the colour that you chose (remember that the loop code is executed repeatedly).


PICCIE

Go ahead and experiment with the timings. Change the numbers inside the brackets of the delay functions in both the lines
```
  delay(2000);

  delay(1000);
```

to some number between 200 and 5000 or 0.2 seconds to 5 seconds - and see what happens. By playing around with combinations of numbers you can modify the sequence the blinking takes.
If we were to add the lines:
```
  EngduinoLEDs.setAll(YELLOW);
  delay(2000);
  EngduinoLEDs.setAll(OFF);
  delay(1000);
```
to the bottom so our code would look like this
```
void loop()
{
  EngduinoLEDs.setAll(RED);
  delay(2000);
  EngduinoLEDs.setAll(OFF);
  delay(1000);
  EngduinoLEDs.setAll(YELLOW);
  delay(2000);
  EngduinoLEDs.setAll(OFF);
  delay(1000);
}
```

What do you think would happen? Try it and find out… what happens if you change the timings now? What happens if you make them very small?

##What next?
There are many things we can do next. If you’re in a lab class, talk to one of the demonstrators, and they will give you another sheet that will tell you something about how you might make your code a bit more sophisticated, or how to work the button or one of the sensors. There’s no substitute for experience – try things, and if they don’t work, figure out why and fix them – there are many things you can do with the Engduino and the only rule is to be creative.

If you’re at home or school working through this, you can always visit the Engduino website and navigate to the worksheets.

If you’re a very advanced programmer, you can look at:
http://www.engduino.org/engduino_libraries_detailed/
And if you get stuck, by all means contact us on support@engduino.org.


