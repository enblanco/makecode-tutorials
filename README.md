# MOT - Intro to MakeCode Arcade

### @explicitHints true

## {Introduction @showdialog}

🎮 **Welcome to the game creation workshop!**

You've come a long way: you have your **Game Design Document** ready and now it's time to bring your idea to life.

In this tutorial you will learn:
- How the block editor works
- How to create your first sprite (character)
- How to make it move across the screen
- How to add effects and sounds

When you finish, you'll have the tools to start your own game!

## {Step 1}

**Let's explore the editor** 🔍

Look around you. In the center you have the **workspace** where you will connect code blocks.

On the left is the **toolbox** with all the pieces you can use.

~hint What are blocks? 🧩
---
Blocks are like LEGO pieces that fit together.
Each block does something specific (show text, move a character,
play a sound...). You don't need to write code!
hint~

➡️ Click **Next** when you're ready.

## {Step 2}

**Your first message** 💬

Let's make the game show a welcome message.

- :game: Click on the ``||game:splash " "||`` block that's already in your workspace.
- :keyboard: Type a message (for example: "My first game!")

```blocks
game.splash("My first game!")
```

## {Step 3}

**The background of your game** 🎨

A game needs a scene. Let's give it some color.

- :tree: Find the ``||scene:set background color to [ ]||`` block in the toolbox.
- :mouse pointer: Drag it and connect it **above** the splash block.
- :paint brush: Click the color square to choose your favorite.

```blocks
scene.setBackgroundColor(7)
game.splash("My first game!")
```

## {Step 4 @showdialog}

**Sprite time!** 🦸

In video games, a **sprite** is any image that appears on screen: your character, enemies, objects...

Think about the **protagonist** from your GDD. Now let's create it!

## {Step 5}

**Create your character** 🎭

- :paper plane: Find the ``||variables(sprites):set [mySprite] to sprite [ ] of kind [Player]||`` block
- :mouse pointer: Connect it at the end of your code
- :paint brush: Click the gray square to **draw** your sprite (or pick one from the **Gallery**)

~hint Design tip 💡
---
Start with a simple design: 8x8 or 16x16 pixels.
You can always improve it later!
hint~

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

## {Step 6}

**Make it move!** 🕹️

A still character is boring. Let's control it with the arrow keys.

- :game: Find the ``||controller:move [mySprite] with buttons||`` block
- :mouse pointer: Connect it at the end of your code

Test your game! Click on the **simulator** (game screen) and use the arrows to move your character.

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

## {Step 7}

**Special effects** ✨

Let's add an effect when you press the A button.

- :game: Drag the ``||controller:on [A] button pressed||`` block to an empty area of the workspace
- :paper plane: Inside, add ``||sprites:[mySprite] start [spray] effect||``
- :mouse pointer: Click on "spray" to choose another effect (try "confetti"!)

```blocks
let mySprite: Sprite = null
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.startEffect(effects.confetti, 500)
})
```

## {Step 8}

**🕹️ Let's play!**

Look at the simulator and test your creation:

1. Click on the simulator screen to focus it
2. Use the **arrows** to move your sprite
3. Press **A** (or space) to see the effect

~hint Not working? 🔧
---
Check that the blocks are properly connected.
The simulator updates automatically when you change the code.
hint~

## {Finale @showdialog}

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
