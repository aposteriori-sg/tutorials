Basic Movement Blocks
---

![](images/movementtab.jpg)

The following blocks are good to use for some basic sequential programs where you program the robot to drive in a particular path.

Use the blocks below to explore your robot's basic mobility with these driving tests:

### Beginner

1. Drive straight for 1 rotation
1. Drive back for 180 degrees
1. Drive straight for 1 second

### Intermediate 
1. Drive in circles for 5 seconds
1. Drive 2 rotations at %100 speed and float
1. Drive 2 rotations at %100 speed and hold position

### Advanced
1. Make a near-perfect Right turn 
1. Make a near-perfect Left turn

*Note the parameters you used for this.  It may come in handy in the future.*

## Move Forward/Backward for ...

![](images/movefwdback.jpg)

Use this block to go Forward or Backward only.
The block tries it best to move the two main motors connected at the same speed in the same direction.

![](images/movefwdchoices.jpg)

- For __ Rotations
    - The amount you enter is the number of times the motor shafts will rotate before coming to a stop.  

- For __ Degrees
    - Similar to Rotations, but with more accuracy, e.g:
    - 360 degrees = 1 rotation
    - 90 degrees = 1/4 of a rotation
    - 540 degrees = 1 and a half rotations
    - and so forth...

- For __ Seconds
    - Keep the motors running for the specified time

## Move with Steering for ...

![](images/movesteering.jpg)

This block let's you set the direction - so you can steer sideways, not just drive forward and backward.

Same options as above:
- For __ Rotations
- For __ Degrees
- For __ Seconds

## Set Movement Speed

![](images/setmovementspeed.jpg)

The default speed the above blocks are using is %50.  If you want to go faster you can set the Movement Speed higher.  Similarly, you can also set it lower to make the robot drive even slower.

## Set Movement Motors to Hold/Float at Stop

![](images/setstopoption.jpg)

Say you tell your robot to move Forward for 1 second.

When the 1 second is up, there are various behaviors that could take place:

- **Float**: The power to the motors is cut, but the motor shaft is allowed to rotate freely.  Some momentum will persist and the robot will advance a bit longer before coming to a full rest.

- **Hold Position**: The power to the motors is cut, and the motor shaft is held in place.  Some momentum will persist and the robot may jerk a bit, but the wheels should hold fast.

## Set Movement Motors

![](images/setmovementmotors.jpg)

Tell the Brick which 2 Motor ports to use for the Right & Left wheel motors.

The default is B & C, but EV3 Classroom is smart enough to detect the Movement Motors if you have only 2 large motors connected.

![](images/motordetection.png)

Make sure they are set correctly if the automatic detection is not working as expected.

## (Advanced) For Rotations/Degrees vs. For Seconds

Important: Try to make the robot bump into a wall using for **Rotations** vs. for **Seconds**.  Note the difference:

- For Rotations: program never stops.  The block waits until those number of rotations have completed before moving on to the next code block

- For Seconds: no matter what, the motors will shut off and the program will continue to the next line 

You can test this with 2 simple and similar programs as follows:

![](images/rotationsvsseconds.jpg)

In this case when bumping the wall, the motor shafts would not be able to rotate as many times as specified, and the EV3 should not show the end image (only eyes).

![](images/rotationsvsseconds2.jpg)

No matter what the motors and the wheels are doing, this should show a smile after 10 seconds had elapsed.

