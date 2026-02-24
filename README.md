# MOT - Intro to MakeCode Arcade

### @explicitHints true

## {Introduction @unplugged}

**🎮 Welcome to the game creation workshop!**

You've come a long way: you have your **Game Design Document** ready and now it's time to bring your idea to life.

Complete this tutorial to find out how to:
- follow tutorial prompts
- find blocks in the toolbox
- build code in the workspace
- run your project on the built-in game screen

When you finish, you'll have the tools to start your own game!


## {step 1}

**⭐ Let's explore the editor ⭐**

You've just discovered the most important part of following a tutorial — **reading instructions**!

Look around you. In the center you have the **workspace** where you will connect code blocks.

On the left is the **toolbox** with all the pieces you can use.

~hint What are blocks? 🧩

---

Blocks are like LEGO pieces that fit together.
Each block does something specific (show text, move a character, play a sound...). 

You don't need to write code!

hint~

When you're ready to move to the next step, click **Next** to continue.


## {step 2}

**Your first message** 💬

Let's make the game show a welcome message.

- :mouse pointer: Click inside the ``||game(noclick):splash " "||`` block that's already in your workspace
and **change the sentence** to something more exciting.


#### ~ tutorialhint
```blocks
game.splash("My first game!")
```


## {step 3}

**The background of your game** 🎨

A game needs a scene. Let's give it some color.

- :tree: Find the ``||scene:set background color to [ ]||`` block in the toolbox.

- :mouse pointer: Drag it and connect it **above** the splash block.

- :paint brush: Click the empty square to set the background to your favorite color.


#### ~ tutorialhint
```blocks
scene.setBackgroundColor(7)
game.splash("My first game!")
```


## {Sprites @unplugged}

**Sprite time!** 🦸

In video games, a **sprite** is any image that appears on screen: your character, enemies, objects...

Think about the **protagonist** from your GDD. Now let's create it!


## {step 4}

**Create your character** 🎭

- :paper plane: Find the ``||variables(sprites):set [mySprite] to sprite [ ] of kind [Player]||`` block

- :mouse pointer: Connect it at the end of your code

- :paint brush: Click the empty box to **draw** your sprite or switch to the **Gallery** to pick one of ours.


~hint Design tip 💡

---

Start with a simple design: 8x8 or 16x16 pixels.
You can always improve it later!

hint~


#### ~ tutorialhint
```blocks
scene.setBackgroundColor(5)
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
```


## {step 5}

**Make it move!** 🕹️

A still character is boring. Let's control it with the arrow keys.

- :game: Find the ``||controller:move [mySprite] with buttons||`` block

- :mouse pointer: Connect it at the end of your code

Test your game! Click on the **game window** and use the arrows to move your character.


#### ~ tutorialhint
```blocks
scene.setBackgroundColor(5)
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
controller.moveSprite(mySprite)
```


## {step 6}

**Special effects** ✨

Let's add an effect when you press the A button.

- :game: Drag the ``||controller:on [A] button pressed||`` container block to an empty area of the workspace

- :paper plane: Inside, add ``||sprites:[mySprite] start [spray] effect||``

- :mouse pointer: Click on "spray" to choose another effect (try "confetti"!)


#### ~ tutorialhint
```blocks
let mySprite: Sprite = null
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.startEffect(effects.confetti, 500)
})
```


## {step 7}

**🕹️ Let's play!**

- :binoculars: Look at the game window and test your creation:

1. Click the **Ⓐ** button (or space bar) to clear your splash screen message
2. Use the **arrows** to move your sprite
3. Press **Ⓐ** over and over again to see your effects!

~hint Not working? 🔧

---

Check that the blocks are properly connected.
The simulator updates automatically when you change the code.

hint~


## {Finale @unplugged}

🎉 **Congratulations!** 🎉

You've completed your first creation in MakeCode Arcade.

**Now you know:**
- ✅ How to use the block editor
- ✅ How to create and draw sprites
- ✅ How to add movement with controls
- ✅ How to use visual effects

---

🚀 **Ready for your own game?**

Remember your GDD: you have the **game type**, the **protagonist**, the **mechanics**... It's time to make it real!


```template
game.splash("Welcome!")
```

```ghost
let mySprite: Sprite = null;
mySprite.startEffect(effects.spray)
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    scene.cameraShake(4, 500)
})
scene.setBackgroundColor(9)
controller.moveSprite(mySprite)
```
