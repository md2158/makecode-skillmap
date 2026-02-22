# Custom Sprite Kinds

## Welcome to the Ramadan Game! @showdialog

Selamat datang! 🌙

In this tutorial you will add **custom Sprite Kinds** — labels that help the game tell different objects apart, like coins, food, trees, and gates.

## Step 1: Add your 5 custom kinds

Click on any **create sprite** block, open the **Kind** dropdown, scroll to the bottom and click **"Add a new kind..."**

Add these 5 kinds one by one:

```blocks
let a = sprites.create(img`
    . . . . . . . .
    . . . . . . . .
    `, SpriteKind.Decoration)
let b = sprites.create(img`
    . . . . . . . .
    . . . . . . . .
    `, SpriteKind.StartGate)
let c = sprites.create(img`
    . . . . . . . .
    . . . . . . . .
    `, SpriteKind.FinishSahur)
let d = sprites.create(img`
    . . . . . . . .
    . . . . . . . .
    `, SpriteKind.Trees)
let e = sprites.create(img`
    . . . . . . . .
    . . . . . . . .
    `, SpriteKind.Coin)
```

~hint The 5 kinds you need 💡
- **Decoration** — Ramadan Kareem banner
- **StartGate** — the banner the player walks into
- **FinishSahur** — the Next button when done
- **Trees** — decorative scene trees
- **Coin** — Pahala reward coins
hint~

## Step 2: Understand overlaps and kinds

Kinds are what make **overlap events** work. Drag out an **on sprite overlaps** block from ``||sprites:Sprites||`` — your 5 custom kinds now appear in both dropdowns!

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.StartGate, function (sprite, otherSprite) {
    game.splash("Gate touched!")
})
sprites.onOverlap(SpriteKind.Player, SpriteKind.Coin, function (sprite, otherSprite) {
    game.splash("Coin collected!")
})
```

~hint Why not use Food for everything? 💡
If coins and food were both **Food** kind, the game couldn't tell them apart! Separate kinds give each object its own identity so the right event fires every time.
hint~

## Step 3: Clean up and confirm

Delete the test sprites and overlap blocks — these were just to check everything works.

Click the Kind dropdown on any sprite block and confirm all 5 custom kinds appear in the list alongside the built-in ones. ✅

## Done! @showdialog

All 5 custom Sprite Kinds are ready! 🎉

Next up — building the **Intro Screen** with the Ramadan Kareem banner and Start Gate!
