# Build the Sahur Scene

## The Sahur Phase Begins! @showdialog

**Sahur** is the pre-dawn meal eaten before fasting during Ramadan. 🌙🍱

When the player walks into the Start Gate, the game switches to an outdoor Sahur scene.

In this tutorial you will swap the background, clean up intro sprites, and place 4 decorative trees.

## Step 1: Swap background and clean up

Go to your **on Player overlaps StartGate** block from Tutorial 2. Delete the splash placeholder.

Set the Sahur background image, destroy the intro sprites, and reset the score:

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.StartGate, function (sprite, otherSprite) {
    scene.setBackgroundImage(img`
        7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7
        7 7 7 7 7 7 7 7 7 7 7 7 7 7 7 7
        e e e e e e e e e e e e e e e e
        e e e e e e e e e e e e e e e e
    `)
    RamdhanKareem.destroy()
    StartText.destroy()
    info.setScore(0)
})
```

~hint Background image tip 💡
Click the image box → **My Assets** tab → select your **Sahur Background** image!
hint~

## Step 2: Place 2 trees on the left

Still inside the overlap block, add 2 green trees on the left side of the scene:

```blocks
    let tree1 = sprites.create(img`
        . . . 7 9 . . . 7 9 . . . . . .
        . . 9 9 9 9 9 . 7 9 9 . . . . .
        . 9 3 3 7 7 . 9 6 9 7 . . . . .
        . . . . 4 e e e e . . . . . . .
        . . . . 4 e e e c . . . . . . .
        . . . e 4 e e c e . . . . . . .
        . . . e e e e c e . . . . . . .
        `, SpriteKind.Trees)
    tree1.setPosition(30, 79)
    let tree2 = sprites.create(img`
        . . . 7 9 . . . 7 9 . . . . . .
        . . 9 9 9 9 9 . 7 9 9 . . . . .
        . . . . 4 e e e e . . . . . . .
        . . . . 4 e e e c . . . . . . .
        . . . e 4 e e c e . . . . . . .
        `, SpriteKind.Trees)
    tree2.setPosition(11, 100)
```

## Step 3: Place 2 trees on the right

Add 2 teal-toned trees on the right for depth and visual variety:

```blocks
    let tree3 = sprites.create(img`
        . . . 7 5 . . . 7 5 . . . . . .
        . . 5 5 5 5 5 . 7 5 5 . . . . .
        . . . . 4 e e e e . . . . . . .
        . . . . 4 e e e c . . . . . . .
        . . . e 4 e e c e . . . . . . .
        `, SpriteKind.Trees)
    tree3.setPosition(115, 69)
    let tree4 = sprites.create(img`
        . . . 7 5 . . . 7 5 . . . . . .
        . . 5 5 5 5 5 . 7 5 5 . . . . .
        . . . . 4 e e e e . . . . . . .
        . . . . 4 e e e c . . . . . . .
        `, SpriteKind.Trees)
    tree4.setPosition(134, 85)
```

Press **Play** ▶️ → walk into the gate → outdoor scene with 4 trees should appear! 🌳

## Done! @showdialog

The Sahur outdoor scene is ready! 🌳🌙

Next up — **spawning Sahur food** for the player to collect!
