# Animate the Player Character

## Bring your hero to life! @showdialog

Time to add the **player** — a boy sprite who walks around collecting food and coins! 🚶

In this tutorial you will create the sprite, enable movement, scale it up, and add a walking animation.

## Step 1: Create, move and position the player

Inside ``||loops:on start||``, create the player sprite using your **Boy-standing** asset with Kind **Player**.

Hook it up to the controller, set the starting position on the left, and lock it to screen edges:

```blocks
let mySprite = sprites.create(img`
    . . . . f f f f . . . . 
    . . f f e e e e f f . . 
    . f f e e e e e e f f . 
    f f f f 4 e e e f f f f 
    f f f 4 4 4 e e f f f f 
    f f f 4 4 4 4 e e f f f 
    f 4 e 4 4 4 4 4 4 e 4 f 
    f 4 4 f f 4 4 f f 4 4 f 
    f e 4 d d d d d d 4 e f 
    . f e d d b b d d e f . 
    . f f e 4 4 4 4 e f f . 
    e 4 f b 1 1 1 1 b f 4 e 
    4 d f 1 1 1 1 1 1 f d 4 
    4 4 f 6 6 6 6 6 6 f 4 4 
    . . . f f f f f f . . . 
    . . . f f . . f f . . . 
    `, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setPosition(20, 101)
mySprite.setStayInScreen(true)
```

## Step 2: Scale up the player

Add a **set scale** block from ``||sprites:Sprites||`` and set it to **2** — this makes the player twice as large and easy to see:

```blocks
mySprite.setScale(2, ScaleAnchor.Middle)
```

Press **Play** ▶️ — your character should now be bigger and walk around the screen!

~hint ScaleAnchor.Middle explained 💡
The sprite scales from its **center point** outward — so it grows evenly in all directions and stays in the same position!
hint~

## Step 3: Add the walking animation

Go to ``||animation:Animation||`` and drag out the **animate sprite** block. Click **+** to add 3 walking frames from My Assets. Set interval to **500ms** and loop to **true**:

```blocks
animation.runImageAnimation(
    mySprite,
    [img`
    . . . . f f f f . . . . 
    f 4 e 4 4 4 4 4 4 e 4 f 
    f 4 4 f f 4 4 f f 4 4 f 
    4 4 f 6 6 6 6 6 6 f 4 4 
    . . . f f f f f f . . . 
    `, img`
    . . . . f f f f . . . . 
    f 4 e 4 4 4 4 4 4 e 4 f 
    f e 4 d d d d d d 4 e f 
    4 4 f 6 6 6 6 6 6 f 4 4 
    . . . f f . . f f . . . 
    `, img`
    . . . . f f f f . . . . 
    f 4 e 4 4 4 4 4 4 e 4 f 
    f 4 4 f f 4 4 f f 4 4 f 
    4 4 f 6 6 6 6 6 6 f 4 4 
    . . . f f f f f f . . . 
    `],
    500,
    true
)
```

~hint Animation speed tip 💡
Try **200ms** for a faster walk or **800ms** for a slow shuffle. The last parameter **true** means the frames loop forever!
hint~

## Done! @showdialog

Your player is walking and animated! 🎉🚶

**Path 1 — Setting Up the Game World is COMPLETE!** 🎉

Head to **Path 2** to build the Sahur food-collecting scene! 🌙🍱
