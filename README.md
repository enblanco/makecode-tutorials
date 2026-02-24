# MOT Intro Tutorial

## Introduction @unplugged

**Welcome to the game creation workshop!**

You have your Game Design Document ready. Now it's time to bring your idea to life!

In this tutorial you will learn how to:
- Create sprites
- Add movement
- Use effects

## Step One

Add a background color with the ``||scene:set background color||`` block.

```blocks
// @highlight
scene.setBackgroundColor(7)
```

## Step Two

Show a welcome message with ``||game:splash||``.

```blocks
scene.setBackgroundColor(7)
// @highlight
game.splash("My first game!")
```

## Step Three

Create a sprite with ``||variables:set mySprite to||``.

```blocks
scene.setBackgroundColor(7)
game.splash("My first game!")
// @highlight
let mySprite = sprites.create(img`
    . . . . . f f f f f . . . . . .
    . . . . f e e e e e f . . . . .
    . . . f d d d d d d e f . . . .
    . . f d f f d d f f d f f . . .
    . c d d d e e d d d d e d f . .
    . c d c d d d d c d d e f f . .
    . c d d c c c c d d d e f f f f
    . . c d d d d d d d e f f b d f
    . . . c d d d d e e f f f d d f
    . . . . f f f e e f e e e f f f
    . . . . f e e e e e e e f f f .
    . . . f e e e e e e f f f e f .
    . . f f e e e e f f f f f e f .
    . f b d f e e f b b f f f e f .
    . f d d f f f f d d b f f f f .
    . f f f f f f f f f f f f f . .
`, SpriteKind.Player)
```

## Step Four

Add movement with ``||controller:move mySprite with buttons||``.

```blocks
scene.setBackgroundColor(7)
game.splash("My first game!")
let mySprite = sprites.create(img`
    . . . . . f f f f f . . . . . .
    . . . . f e e e e e f . . . . .
    . . . f d d d d d d e f . . . .
    . . f d f f d d f f d f f . . .
    . c d d d e e d d d d e d f . .
    . c d c d d d d c d d e f f . .
    . c d d c c c c d d d e f f f f
    . . c d d d d d d d e f f b d f
    . . . c d d d d e e f f f d d f
    . . . . f f f e e f e e e f f f
    . . . . f e e e e e e e f f f .
    . . . f e e e e e e f f f e f .
    . . f f e e e e f f f f f e f .
    . f b d f e e f b b f f f e f .
    . f d d f f f f d d b f f f f .
    . f f f f f f f f f f f f f . .
`, SpriteKind.Player)
// @highlight
controller.moveSprite(mySprite)
```

## Conclusion @unplugged

**Congratulations!**

You completed your first tutorial. Now you know the basics of MakeCode Arcade!
