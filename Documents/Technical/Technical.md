
# Ronin's Revenge Technical Specifications

<hr>

<br>
<p align="center"> Paul NOWAK</p>
<br>

<p align="center"> ALGOSUP, Group 3. All Rights Reserved. </p>

<hr>

<details>
<summary>Table of contents</summary>


- [Ronin's Revenge Technical Specifications](#Overview)

- [1. Presentation](#1-presentation)
  - [1.1. Overview](##1.1-overview)
  - [1.2. The game](##1.2-the-game)

- [2. Technologies used](#2-technologies-used)
  - [2.1. Game Engine](##2.1-game-engine)
  - [2.2. Development Tools ](##2.2-development-tools)
  - [2.3. 3rd Party Softwares/libraries ](##2.3-3rd-party-softwares/libraries)

- [3. Game Mechanics](#3-game-mechanics)
  - [3.1. Core Mechanics](##3.1-core-mechanics)
  // Needs details
  - [3.2. Character Physics](##3.2-character-physics)
  - [3.3. Level Settings ](##3.3-level-settings)

- [4. Game Assets](#4-game-assets)

- [5. User Interface](#5-user-interface)
  - [5.1. Menus](##5.1-menus)
  - [5.2. Controls](##5.2-controls)
  // Needs details
  - [5.3. HUD Elements](##5.3-hud-elements)

- [6. Optimization](#6-optimization)
  - [6.1. Performance](##6.1-performance)
  - [6.2. Memory Usage](##6.2-memory-usage)


- [7. Glossary](#7-glossary)


</details>

## Overview

The goal of this project gives us more freedom than the previous ones: we need to create a small but functional video game that is bug-free and polished. We could choose the technologies to proceed with the realization of the game.



## The game

The game in question is called Ronin's Revenge. 

This is a 2D side scroller action game where you play as a samurai named Kazuo during feudal Japan's era. The player's objective is to cross a level where he must defend himself against enemies with his katana. 

This is a hardcore game where the player has only one life and will have to start all over again in case of a Game Over. In addition, he has a time limit of 10 minutes to reach the end of the game without getting killed.

## Glossary

| word                                                                                                |                                                                                                    definition                                                                                                    |
| --------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| <img src="./Images/1200px-UE_Logo_Black_Centered.svg.png" width="30" height="30" /> <span id="Unreal Engine">Unreal Engine</span>                                                                     |   Real-Time 3D graphics game engine developed by epic Games              |
| <span id="Game Engine">Game Engine</span>                                                               |        Software framework primarily used for the development of video games.       |
| <img src="./Images/ISO_C++_Logo.svg.png" width="30" height="30" /><span id="C++">C++</span>               |                          C++ is a high-level and object-oriented programming language.                             |
| <span id="Blueprint">Blueprint</span>                  |                                                              Complete gameplay scripting system based on the concept of using a node-based interface for creating gameplay elements from within Unreal Editor.                                                               |
| <span id="Level Design">Level Design</span>         |            Game design process involving the creation of video games levels.             |
| <span id="Mechanics">Mechanics</span> | In Game Design, rules and procedures guiding players through the game.  |
| <span id="Systems">Systems</span> | In Game Design, rules defining how the game react to player inputs.  |
| <span id="Hardcore">Hardcore</span> | Type of game that requires a high user input and time investment in order for users to be successful.  |


# Product

## Software

The rendered product will be a game made with the Unreal Engine game engine.

### Unreal Engine
It is a famous and free game engine developed by Epic Games. 

This amazing software enable creators across industries to deliver cutting-edge content, interactive experiences, and immersive virtual worlds. You can make any type of game such as platformers, FPS or side scrollers (2D or 3D). 

The latest updated version is 5.1, but our game is using the 4.27.2 version available on the Epic games launcher.

### Scene

For this game, we have used the provided 2D Side Scroller template to build our level.

### Blueprints

### Assets used

-FREE SAMURAI PIXEL ART SPRITE SHEETS (https://craftpix.net/freebies/free-samurai-pixel-art-sprite-sheets/)



### Memory Management

The


## Assumptions

### Risks
-It's possible that we have some issues with the boss battles, as it involves several game elements (characters models, Higher Hp, fixed camera...)


### Constraints
-The computers we used (Windows11 Thinkbook and Macbook Air Ventura) might experience processor's problems for compiling Unreal Engine scenes. As a consequence, we may have difficulties to push our scenes in Github. 

## Security



