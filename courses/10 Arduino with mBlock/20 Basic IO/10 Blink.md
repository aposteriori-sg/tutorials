Blink
===

## Arduino Blink

The first program you learn to write for Arduino is usually Blink - it's the "Hello World" of the Arduino platform.  Blink code makes the internal LED (marked "L") on the Arduino blink on/off.

Let's start by understanding some of the pinout on the Arduino Uno board - refer to this image:

![](images/arduinopinoutright.jpg)

The 13 pinholes on the right starting from the bottom represent 13 digital input/output's.  That means each of those is connected to an internal pin that can either:

* Output a signal to toggle some external circuit
* Input a signal to read from some external device

We are going to look at some examples of such external circuits shortly, but for now, we just want to toggle the internal LED (marked "L") near the top right of the Arduino.

It just so happens that **this built-in LED is connected to digital I/O PIN 13** internally.

Therefore, when PIN 13 is turned *ON* the LED will turn on.

Similarly, when PIN 13 is turned *OFF* the LED will turn off.

* ON/OFF
* TRUE/FALSE
* HIGH/LOW 

These are just three different designations you can use to describe the state of these digital I/O pins.

![](images/blink.jpg)

## Sample Code for Toggling Pins

Our Blink program needs to toggle the state of PIN 13.

Let's look at the mBlock coding blocks for the Arduino Device.

![](images/pinblocks.jpg)

The first two start with *read...* - that means they assume the pin in question is an INPUT.  We want to treat PIN 13 as an OUTPUT.

*set digital pin (\_\_) output as [\_\_]* - that looks like a promising block.

Let's drag one onto our Workspace, change the Pin field to 13, and the High/Low dropdown to **High**.  

![](images/setoutputpin.svg)

If your Arduino is *Connected*, just click the block, and you should see the "L"-labelled LED is lit.  Clicking the block is causing mBlock to execute it and send the command to Arduino.

Duplicate or drag a second *set digital pin* block with the same PIN 13, but this time set to **Low**.  

Now click on this block and the LED should turn off.

Similarly, we can attach Events like *When Key Pressed* to create a manual light switch for our built-in LED:

![](images/simplecodeswitch.jpg)

NOTE: Greyed out blocks are usually meant for the other mode (Upload), so *"read pulse pin"* can only be used if we switch to *Upload Mode*.