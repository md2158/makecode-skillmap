# ramadan-game

- name: Ramadan Game - MakeCode Arcade Skillmap
- description: Build a Ramadan-themed arcade game step by step! Learn to create a walking character, animated scenes, collectible items, and a full game flow — all inspired by the spirit of Ramadan.
- infoUrl: https://github.com/md2158/makecode-skillmap
- backgroundurl: https://raw.githubusercontent.com/md2158/makecode-skillmap/main/img/background.png
- bannerurl: https://raw.githubusercontent.com/md2158/makecode-skillmap/main/img/banner.png
- primarycolor: #2EA9B0
- secondarycolor: #F9A825
- tertiarycolor: #1B5E20
- highlightcolor: #FAED28

## path-setup

- name: Path 1 - Setting Up the Game World
- description: Build the game foundation with sprite kinds, the intro screen, and your animated player character.
- completionUrl: https://github.com/md2158/makecode-skillmap

### activity-spritekinds

- name: Custom Sprite Kinds
- type: tutorial
- description: Add 5 custom Sprite Kinds so the game can tell different objects apart.
- tags: sprites, setup
- url: github:md2158/makecode-skillmap/01-spritekinds
- imageUrl: https://raw.githubusercontent.com/microsoft/pxt-skillmap-sample/main/img/space.png

### activity-intro

- name: Build the Intro Screen
- type: tutorial
- description: Set the night sky background, add the Ramadan Kareem banner, and wire up the Start Gate.
- tags: sprites, scenes
- url: github:md2158/makecode-skillmap/02-intro
- imageUrl: https://raw.githubusercontent.com/microsoft/pxt-skillmap-sample/main/img/space.png

### activity-player

- name: Animate the Player
- type: tutorial
- description: Create the boy sprite, enable controller movement, scale it up, and add a walking animation.
- tags: animation, player
- url: github:md2158/makecode-skillmap/03-player
- imageUrl: https://raw.githubusercontent.com/microsoft/pxt-skillmap-sample/main/img/space.png

## path-gameplay

- name: Path 2 - Game Phases and Collectibles
- description: Build the Sahur food phase, Pahala coins, and complete the full game loop.
- completionUrl: https://github.com/md2158/makecode-skillmap

### activity-sahur

- name: Build the Sahur Scene
- type: tutorial
- description: Swap in the outdoor background, destroy intro sprites, reset score, and place 4 decorative trees.
- tags: scenes, environment
- url: github:md2158/makecode-skillmap/04-sahur
- imageUrl: https://raw.githubusercontent.com/microsoft/pxt-skillmap-sample/main/img/space.png

### activity-food

- name: Collect Sahur Foods
- type: tutorial
- description: Spawn 15 food sprites with a timed loop, handle collection, play sounds, and unlock the Next button.
- tags: collectibles, score
- url: github:md2158/makecode-skillmap/05-food
- imageUrl: https://raw.githubusercontent.com/microsoft/pxt-skillmap-sample/main/img/space.png

### activity-finish

- name: Pahala Coins and Game Flow
- type: tutorial
- description: Spawn 10 Pahala coins, wire up the FinishSahur overlap, and complete the full game loop.
- tags: coins, game-flow
- url: github:md2158/makecode-skillmap/06-finish
- imageUrl: https://raw.githubusercontent.com/microsoft/pxt-skillmap-sample/main/img/space.png
