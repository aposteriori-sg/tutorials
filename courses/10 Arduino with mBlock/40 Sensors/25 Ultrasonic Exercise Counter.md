Challenge 3b - Exercise Counter
---

Now we can only detect push-up, but not count each one...

A single push-up consists of two actions:
- Going down
- Returning up

Our program should detect both of these, and count the pair as a single push-up.

First, you'll need a variable to keep count.

![](images/countvar.jpg)

Then let's change the code to light up after a set of 5 repetitions (reps):

![](images/ultrasoniccountcode.svg)

NOTE: After each set, you can click reset button to restart Arduino and the reset the count back to 0...

Now test this code:

- Does it work?
- If not, why?

It shouldn't work, it probably lights up green after only 1 push-up.  **Why?**

Once your lower your body and the condition of the distance is met, the variable is increased by one, and the loop runs again... before you have a chance to get back up...

So we need to somehow wait and hold the program until you finish each rep.

Try to use Wait and Wait Until blocks to get this to work (remember how we removed noise from the Tilt sensor program?):

![](images/waituntil.svg)

## *How else can you use the ultrasonic distance sensor in your Active Living solution design?*

Scroll down to see a more complete solution:

--

--

--

--

--

--

**Device**

![](images/ultrasonicfullexampledevice.png)


**Sprite**

![](images/ultrasonicfullexamplesprite.png)


If you can, check what the Ultrasonic Sensor returns when there's nothing in front of it for > 2.5 meters.  That's the max...

When no signal returns in time (too close or too far), the Ultrasonic distance block returns ZERO (0).

So, really any boolean test for short distance should look more like this:

![](images/ultrasonicavoidzero.png)

This way we avoid a false positive 0 zero reading...