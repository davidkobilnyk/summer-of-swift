# Bapit

## Description

Bapit is going to be a SpriteKit game written in Swift.  It's a take on the classic game where you must tap a ball to keep it up in the air for as long as possible.

## Project Location

https://github.com/hswolff/Bapit

## Team Members

- Harry Wolff [@hswolff](https://twitter.com/hswolff)

## Updates

(The dates below are the minimal dates suggested. Please feel free to update earlier & more often!)

### July 25

The project has begun!

I've created the initial game scaffold using Xcode's new Sprite Kit project layout.

Basic gameplay is functional.  You can tap only on the ball to cause it to move upwards in the scene.

We're also calculating where inside the ball you touched and using that when calculating the impulse vector to apply to the ball.

Also moving away from the .sks file and towards pure code implemenation of the game.

### August 10

This creates my first enum and struct.

The enum is for PhysicsBody category and collision bit mask, to allow
me to handle contacts between two physics bodies correctly.

The struct is to create a data type for storing the amount of taps
that someone correctly tapped the ball, and someone missed it in case
I'd want to use that information.

Also moved to instantiating each property in the initializer function init().

Also sped up the game to make it be a little more challenging.

Created the bottomBorder to know when the ball drops to the bottom.

Created scoreLabel to show the current score of the game.

Used the willSet observer to get notified when the TapCount struct is
modified so we can then update the scoreLabel correctly.

Add an extension to GameScene so we can become a contactDelegate
and handle all contact instances.

Abstract the setting up of the game kit view and initial scene
so it's the same no matter how the game is created.

Add ability to save the high score for that session of the game.

Still using observing functions to make for easy binding and updating
of the view.

Created GameOverScene to present once the ball hits the bottom of the screen.

Using SKTransition when presenting each scene for an added touch of life.

Added a 'tap to start label' so that the game only starts once the player
is ready.  I'm controlling this behavior by changing the dynamic property
of the ball's physicsBody.

**Sidenote**:  I'm really enjoying Swift's willSet/didSet property observer methods
on properties.  Really makes databinding really easy and lightweight to use.  Big
props to Apple for that.

### August 25

### September 10

### September 25
