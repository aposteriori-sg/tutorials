RGB Strip - Challenges
---

- (MODERATE) Add 5 more zeRGBas and make each control a different LED separately!
    - No need for the "for" loop to activate each LED
    - Just choose which Virtual Pin control which LED, and code 5 more BLYNK_WRITE functions for each

- (MODERATE) Add a button that makes the LEDs all blink several times
    - Need to create a new Virtual Pin VX button, and
    - Add a new BLYNK_WRITE(VX) function that clears and shows the LEDs

- (ADVANCED) Instead of zeRGBas use Sliders to control the RGB values more exactly:
    - One slider for Red, One for Green, One for Blue
    - Each controls a separate Virtual Pin
    - Each gets its own BLYNK_WRITE(Vx) function in which you need to redefine the current Color with the changes.
    - Might need to maintain 3 global variables for Red, Green, and Blue values so you can create the RGB with the correct current settings for the other 2 colors

- (ADVANCED) Add a button that starts some special effect:
    - Chase: same color but each LED turns on and off in order so it looks like the light is moving up the strip
    - Rainbow: Each LED a different color
    - Anything else you can think of!!!
