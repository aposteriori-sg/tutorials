Using Real Electronics
---

Now that we have learned the basic ideas behind IoT technology, it's time to take our understanding into the real world, where things get a bit more complex, but way more fun!

**Things will not always work!**

That's ok - part of engineering and being a technologist is learning to find the source of a problem, and figuring out how to solve it with materials you have.

First, let's get acquainted with our board.
We've chosen one of the more ubiquitous and easily-available development kits on the market: Espressif's ESP32.

It's got:

- WiFi 
- Bluetooth
- Buttons
- LEDs
- USB connection for easy programming
- multi-us GPIO pins
- Built-in I2C & SPI support

In short - it can connect to and control a lot of electronics!

![](images/esp32pinout.png)

## Connect

First, let's make sure we can connect and program this micro-controller.

Use the short USB wire to connect the ESP32 to your laptop.  You should see a small LED light up.  That indicates the controller is connected to power.

## Arduino & Hello World/Blink

First, find the Arduino app on your laptop and bring it up:
![](images/arduino.jpg)


Arduino is an open-sourced platform for programming micro-controllers.  We need to make sure it's setup to control your ESP32.

### Board Manager

First, open the **Prefences**:

![](images/pref.png)

And add the following to the Board Manager URLs list (copy and paste):

http://dl.espressif.com/dl/package_esp32_index.json

Click **OK** to close the Preferences.

Now navigate to **Tools->Board->Board Manager**.

Type "esp32" in the search box and install the ESP32 library:

![](images/installesp32.png)

Then follow the below image to pick the correct Board, NodeMCU 32-S:

![](images/pickesp32s.png)

### Choose Speed & COM Port

Make sure that a COM port is selected - it may already populate when you connect the board to the laptop:

![](images/comport.png)

If there's more than one choice, you may need to experiment to see which one is the correct one.

As for **Upload Speed**, leave it on whatever the default is.

### Test Program

Before we do anything IoT, let's write a simple test program we can use to see that we can easily change the behavior of our board.

We will just blink the built-in user-controlled LED.

You can copy this code into the Arduino Sketch area:

    int LED_BUILTIN = 2;
    void setup() {
      pinMode (LED_BUILTIN, OUTPUT);
    }

    void loop() {
      digitalWrite(LED_BUILTIN, HIGH);
      delay(1000);
      digitalWrite(LED_BUILTIN, LOW);
      delay(1000);
    }

Next, compile the program to make sure you followed the above instructions properly:

![](images/compile.jpg)

It will ask you to save the file if you haven't yet.  You can call it whatever you want...

If there are no errors, proceed.
If there are errors, see if you can fix them on your own, and if not, call an instructor to help you.

Finally, it's time to upload the program:

![](images/upload.jpg)

**IMPORTANT NOTE - BOOT MODE**

Every time you Upload a program to the ESP32, you have to click and hold the small Boot button next to the mini-USB connector.

![](images/boot.jpg)

*The buttons may be labelled differently on your board, but it should be the same side as shown here.*

This puts the board into programming mode.

Hold the button until the Arduino log says it passed the connection part:

    Connecting........___   <----
    Chip is ESP32-D0WDQ6 (revision 1)
    
    ...
    <bunch of other logs>
    ...
    
    Leaving...
    Hard resetting via RTS pin...


After that you should start seeing a new LED light blinking on your board.

You can mess around with the **delay()** times to make the LED flash longer or more frequently, just to get comfortable with the programming environment.