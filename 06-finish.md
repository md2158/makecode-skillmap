# Pahala Coins and Game Flow

## Earn your rewards and finish! @showdialog

**Pahala** means spiritual reward in Arabic and Indonesian. 🪙

In this final tutorial you will spawn 10 golden Pahala coins, handle coin collection, and wire up the final **FinishSahur** overlap to complete the full game loop!

## Step 1: Spawn 10 Pahala coins with a timed loop

Inside the **on Player overlaps StartGate** block (after the food loop), add a **repeat 10** loop.

Create a coin sprite at a random position and pause between each spawn:

```blocks
    for (let index = 0; index < 10; index++) {
        GetPahala = sprites.create(img`
            . . . . . . . . . . . . . . . . 
            . . . . . 4 4 4 4 4 . . . . . . 
            . . . 4 4 4 5 5 5 d 4 4 4 4 . . 
            . . 4 d 5 d 5 5 5 d d d 4 4 . . 
            . . 4 5 5 1 1 1 d d 5 5 5 4 . . 
            . 4 5 5 5 1 1 1 5 1 1 5 5 4 4 . 
            . 4 d d 1 1 5 5 5 1 1 5 5 d 4 . 
            . 2 5 5 5 d 1 1 1 5 1 1 5 5 2 . 
            . . 2 4 d d 5 5 5 5 d d 5 4 . . 
            . . . 2 2 4 d 5 5 d d 4 4 . . . 
            . . . . . 2 2 2 2 2 2 . . . . . 
            `, SpriteKind.Coin)
        GetPahala.setPosition(randint(0, 100), randint(0, 100))
        pause(500)
    }
```

## Step 2: Handle coin collection

Add a new **on Player overlaps Coin** block. Increase score, destroy the coin, and play the beep for early collects:

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Coin, function (sprite, otherSprite) {
    info.changeScoreBy(1)
    otherSprite.destroy()
    if (info.score() < 5) {
        music.play(
            music.createSoundEffect(
                WaveShape.Square,
                400,
                600,
                255,
                0,
                100,
                SoundExpressionEffect.None,
                InterpolationCurve.Linear
            ),
            music.PlaybackMode.UntilDone
        )
    }
    if (info.score() == 10) {
        NextButton = sprites.create(img`
            . . f f f f f f f f f f . .
            . f f 1 1 1 1 1 1 1 1 f f .
            . f 1 1 1 1 1 1 1 1 1 1 f .
            . f f 1 1 1 1 1 1 1 1 f f .
            . . f f f f f f f f f f . .
            `, SpriteKind.FinishSahur)
        NextButton.setScale(0.15, ScaleAnchor.Middle)
        NextButton.setPosition(144, 102)
    }
})
```

## Step 3: Wire up the Next button and win!

Add a final **on Player overlaps FinishSahur** block. This completes the game loop:

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.FinishSahur, function (sprite, otherSprite) {
    game.splash("Selamat Berpuasa! 🌙")
    game.splash("Ramadan Kareem! ✨")
    game.over(true)
})
```

Press **Play** ▶️ and run through the full game:
- ✅ Intro loads — dark sky, banner, gate
- ✅ Walk into gate — Sahur scene with trees
- ✅ Food and coins spawn one by one
- ✅ Collect them — score goes up, sound plays
- ✅ Score hits target — Next button appears
- ✅ Walk into Next button — **WIN!** 🎉

## Congratulations! @showdialog

You have completed the full **Ramadan Game Skillmap**! 🎉🌙

You learned how to:
- ✅ Create custom Sprite Kinds
- ✅ Build a multi-scene animated game
- ✅ Use overlap events to drive game flow
- ✅ Spawn collectibles with loops and timing
- ✅ Chain all phases into a complete game loop

**Ramadan Kareem! 🌙✨**
