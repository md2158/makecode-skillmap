# Build the Intro Screen

## Let's set the opening scene! @showdialog

The intro screen is the first thing players see. 🌙

In this tutorial you will set the night sky background, add the Ramadan Kareem greeting banner, place the Start Gate, and wire up the overlap event.

## Step 1: Night sky background and greeting banner

Inside ``||loops:on start||``, set the background to **dark blue (color 13)**.

Then create the greeting banner sprite, set its Kind to **Decoration**, and shift it up near the top:

```blocks
scene.setBackgroundColor(13)
let RamdhanKareem = sprites.create(img`
    f f f f f f f f f f f f f f f f
    f 1 1 1 1 1 1 1 1 1 1 1 1 1 1 f
    f 1 d d d 1 1 1 d d 1 1 d 1 1 f
    f f f f f f f f f f f f f f f f
    `, SpriteKind.Decoration)
RamdhanKareem.y += -24
```

~hint How to pick the image? 💡
Click the grey image box → switch to **My Assets** tab → select your **Ramadan Greeting Text** image!
hint~

## Step 2: Add and position the Start Gate

Create the Start Gate sprite with Kind **StartGate**. Scale it down to 14% and place it center-right so the player walks toward it:

```blocks
let StartText = sprites.create(img`
    f f f f f f f f f f f f f f f f
    f 5 5 5 5 5 5 5 5 5 5 5 5 5 5 f
    f 5 1 1 1 1 1 1 1 1 1 1 1 1 5 f
    f f f f f f f f f f f f f f f f
    `, SpriteKind.StartGate)
StartText.setScale(0.14, ScaleAnchor.Middle)
StartText.setPosition(128, 100)
```

~hint Screen size tip 💡
MakeCode Arcade's screen is **160 × 120 pixels**. Position (128, 100) is right-center — perfect for the player to walk toward from the left!
hint~

## Step 3: Wire up the Start Gate overlap

Add an **on sprite overlaps** block. Set it to **Player** overlaps **StartGate**.

Add a splash placeholder — you will replace this with the real Sahur scene in Tutorial 4:

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.StartGate, function (sprite, otherSprite) {
    game.splash("Sahur dimulai!")
})
```

Press **Play** ▶️ — check dark background, banner near top, gate on the right!

## Done! @showdialog

The intro screen is complete! 🌙🏮

Next up — creating and animating your **player character**!
