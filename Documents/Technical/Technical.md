
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

# 1. Presentation
## 1.1. Overview

The goal of this project gives us more freedom than the previous ones: we need to create a small but functional video game that is bug-free and polished. We could choose the technologies to proceed with the realization of the game.



## 1.2. The game

The game in question is called Ronin's Revenge. 

This is a 2D side scroller action game where you play as a samurai named Kazuo during feudal Japan's era. The player's objective is to cross a level where he must defend himself against enemies with his katana. 

This is a hardcore game where the player has only one life and will have to start all over again in case of a Game Over. In addition, he has a time limit of 10 minutes to reach the end of the game without getting killed.




# 2. Technologies used


## 2.1. Game Engine
The rendered product will be a game made with the Unreal Engine game engine.

It is a famous and free game engine developed by Epic Games. 

This amazing software enable creators across industries to deliver cutting-edge content, interactive experiences, and immersive virtual worlds. You can make any type of game such as platformers, FPS or side scrollers (2D or 3D). 

The latest updated version is 5.1, but our game is using the 4.27.2 version available on the Epic games launcher.

## 2.2. Development Tools

For this game, we have used the provided 2D Side Scroller template to build our level.

### Blueprints

## 2.3. 3rd Party Softwares/libraries


# 3. Game Mechanics

## 3.1. Core Mechanics
We play as Kazuo, the game's main protagonist, where we travel through a 2D scrolling level. 

Walking: the player move either on the right or on the left in order to progress.

Jumping: the player can jump to reach a higher place, or jump above an enemy to avoid him. He can jump vertically, but he can also jump diagonally if he also move on the left/right during his jump animation.

## 3.2. Character Physics

## 3.3. Level Settings


# 4. Game Assets

-FREE SAMURAI PIXEL ART SPRITE SHEETS (https://craftpix.net/freebies/free-samurai-pixel-art-sprite-sheets/)





# 5. User Interface

## 5.1. Menus
The game opens on a main menu, showing the character artwork and 3 choices:
-Start Game: allows you to load the game before to start playing
-Options: lead you to another menu for changing sound, etc...
-Credits: lead you to a credits menu showing the name of those who worked on the project.
## 5.2. Controls
The game is played on PC, so you use the keyboard keys to play the game.

Right Key: allows your character to move on the right.

Left Key: allows your character to move on the left.

Down Key: allows your character to crouch.

Space Key: allows your character to jump. If used in midair, he performs a double jump.

Shift Key: used while your characer is moving, allows him to sadh in order to have a higher moving speed.

Left Mouse Key: allows the player to swing his katana to attack a front of him. Clicked several times, he can create a combo attack.

## 5.3. HUD Elements



# 6. Optimization

## 6.1. Performance

## 6.2. Memory Usage
Dealing with the memory used for creating our game will be important. Indeed, we want to avoid having issues when pushing the game's codes and files in github. So, the game's performance must remain almost untouched when transferring data in the main branch of our project.



# 7. Glossary

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



