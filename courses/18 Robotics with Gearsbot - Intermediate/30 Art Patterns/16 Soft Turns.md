Soft Turns
---

Sometimes your robot will want to move less like a square, and more like a racing car!

For that, we need to learn how to make some soft turns, or move in arcs and circles.

## Arcs & Circles

You will need to play around with wheel speeds to get different turn angles.

![](images/right.jpg)

Then to make an arc, you just have to move some distance in that direction without completing a full circle...

![](images/softTurn.png)

Or you can try to figure out just how many rotations/desgrees it takes to complete one full circle, or more!

Use [this canvas](https://gears.aposteriori.com.sg/index.html?worldJSON=https%3A%2F%2Ffiles.aposteriori.com.sg%2Fget%2FtcygQfcnB4.json&robotJSON=https%3A%2F%2Ffiles.aposteriori.com.sg%2Fget%2F7r9K65arhz.json&filterBlocksJSON=https%3A%2F%2Ffiles.aposteriori.com.sg%2Fget%2Fq6jnF3GLcP.json).

## Move Steering

We can also use Move Steering block to abstract how sharp our turns are:

![](images/movesteering_fwd.jpg)

- <u>Direction</u>
  - **Positive (1 to 100)**: higher number means sharper turn to the **Right**
  - **Negative (-1 to -100)**: lower number means sharper turn to the **Left**

## Practice

Use [this canvas](https://gears.aposteriori.com.sg/index.html?worldJSON=https%3A%2F%2Ffiles.aposteriori.com.sg%2Fget%2FtcygQfcnB4.json&robotJSON=https%3A%2F%2Ffiles.aposteriori.com.sg%2Fget%2F7r9K65arhz.json&filterBlocksJSON=https%3A%2F%2Ffiles.aposteriori.com.sg%2Fget%2FoABKLFjrt4.json).
 
![](images/arc1.png)

- Test Direction values: 0, 30, 60, 100
    - For each Direction, figure out the number of rotations/degrees to complete a 90-degree turn (similar to turns we did in the Maze)
<br>
<br>
- Test Direction values: -25, -50, -75
    - For each Direction, figure out the number of rotations/degrees to complete a semi-circle

![](images/arc2.png)

## Circle Challenge

- Open **[this challenge](https://quirkycort.github.io/gears/public/index.html?worldJSON=https%3A%2F%2Ffiles.aposteriori.com.sg%2Fget%2FuEks4FnMpu.json&filterBlocksJSON=https%3A%2F%2Ffiles.aposteriori.com.sg%2Fget%2Fo22H2evjjT.json&worldScripts=world_challenges)**

- Try to play with the various speeds and distances to complete a perfect circle without bumping the tree or falling off!

