Moving Platforms
---

It's common to have moving platforms:

For this, it's easier if we use an application to create a single-object platform (NOT something using the combined middle tile and end sprites).

It also needs to be its own object, as once we had teh moving behavior, it will apply to all the copies of that object...

![](images/combinedPlatform.png)

We like the desktop app [GIMP](https://www.gimp.org/).

But you can use [Piskel](https://www.piskelapp.com/p/create/sprite) or [PixilArt](https://www.pixilart.com/draw), which are web-based.

## Rectangular Movement 

Once we add this new Sprite to our project, we can add the two following Behaviors to it:

- **Platform**, in order to interact with character as a platform)
- **Rectangular Movement**, to make it move

![](images/movingPlatform.png)

Once you add this object to your scene you can experiment with the motion properties:

- You can make side-to-side movement by making the Vertical distance 0
- You can make it a vertial platform, like an elevator, by making the horizontal distance be 0
- You can adjust the distances and speeds to suit your game's needs

<video autoplay muted loop width=450 height="auto">
  <source src="images/movingPlatform.mp4" type="video/mp4">
</video>

## Irregular Platforms

You may have some ideas about other types of platforms (see-saws, rotators, toggle passthrough on/off, etc)

For instance, we wanted to have platforms that that fall off-screen and you have to jump off of it before it's too late!

There are many ways to do it, but one way for this is to toggle Physics types on the object.

First, create a new version of the Moving Platform (new Sprite, not just anothe rinstance of Moving Platform).

Then add the Behaviors:

- **Platform**: still need character to be able to stand on it
- **Physics Engine 2.0**: set object type to *Static* (leave the rest for now)

Place the object somewhere appropriate in your level.

Then add an event that changes the Physics type to *Dynamic* when your character collides with it:

![](images/fallingPlatform.png)


- *Static*: Non-moveable
- *Dynamic*: Moveable, including by gravity

You can change the Gravity scale to make it fall slower...

<video autoplay muted loop width=450 height="auto">
  <source src="images/fallingPlatform.mp4" type="video/mp4">
</video>

HINT: Make sure when you die to restart the scene or re-position and re-Static the object, so that it's reset when necessary.