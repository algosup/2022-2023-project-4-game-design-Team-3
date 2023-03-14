
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

For this game, we have used the provided 2D Side Scroller template to build our level in Unreal Engine.

### Blueprints

## 2.3. 3rd Party Softwares/libraries


# 3. Game Mechanics

## 3.1. Core Mechanics
We play as Kazuo, the game's main protagonist, where we travel through a 2D scrolling level. 

Walking: the player move either on the right or on the left in order to progress. If he walk towards a wall, he will still have his walking animation without really moving.

Jumping: the player can jump to reach a higher place, or jump above an enemy to avoid him. He can jump vertically, but he can also jump diagonally if he also move on the left/right during his jump animation.

Attacking: the player takes his katana and swings it a front of him, extending his attack hitbox in order to touch his enemies. He has the possibility to attack several times to trigger different sword animations (and perhaps different hitboxes) and create combos.

Dashing: When the player is moving, he can also dash to move faster. This mechanic is useful when the player want to progress at a faster rhythm, and in situations when the path is clear. He can also jump while dashing before landing on the ground and continuing to run.

Crouch: The player can crouch, so he will have a kneeling animation. As a result, his hitbox's height will be reduced, and this could allow him to avoid projectiles sent by enemies.

## 3.2. Character Physics

## 3.3. Level Settings
The character move through a serie of levels, containing enemies and platforms.

To go to the next level, the player either has to kill every foes of the level or reach a certain point. Then, he will be instantly teleported at the next level.


# 4. Game Assets

-FREE SAMURAI PIXEL ART SPRITE SHEETS (https://craftpix.net/freebies/free-samurai-pixel-art-sprite-sheets/)


# 5. User Interface

## 5.1. Menus
The game opens on a main menu, showing the game's title, the character artwork, and a Samuraï themed music is being played. 

With his mouse, the player has a menu of 3 different choices:
-Start Game: allows you to load the game before you start playing.
-Options: lead you to another menu for changing sound, etc...
-Quit: you can quit the game and close the application.

On the top right corner, a blue square is indicating you the controls inputs:
-Arrows: Left, Right and Jump
-A,Z: Attack
-Esc (escape): pause.

When you are playing the game but you decide to pause, the game stops, and you have 3 choices appearing in the middle of the screen:
-Resume: stop the pause and continue to play. 
-Options: similar to the one from the main menu.
-Menu: to quit your actual game, and return to the main menu.
## 5.2. Controls
The game is played on PC, so you use the keyboard keys to play the game.

Right Key: allows your character to move on the right.

Left Key: allows your character to move on the left.

Down Key: allows your character to crouch.

Space Key: allows your character to jump. If used in midair, he performs a double jump.

Shift Key: used while your characer is moving, allows him to sadh in order to have a higher moving speed.

Left Mouse Key: allows the player to swing his katana to attack a front of him. Clicked several times, he can create a combo attack.

## 5.3. HUD Elements
To guide the player, there are 3 pieces of data displayed on screen during gameplay:

-The time: always located at 3/4 of the height of the screen in the middle, it gives the player information about the remaining time.
Either it acts as a warning timecode, telling the player how much he has left to complete the level before a game over occurs, either it just indicate how much time he must wait before going to the next level.

-The enemy counter: on the top-right corner, a number is constantly displayed in some levels. 
It represents the number of enemies the player must kill in order to complete the level. The number decreases by 1 each time an enemy is defeated, and if it hits 0, the player will teleport to the next level.

-Level results: it is located in the middle of the screen. However, it only appears in certain conditions depending on the player actions. Indeed, it displays "WIN" when he manages to finish a panel, or "GAME OVER" if he is defeated or has no time left.




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



