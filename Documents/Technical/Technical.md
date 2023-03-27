
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
    - [2.2.1. Scene ](###2.2.1-scene)
    - [2.2.2. BluePrints ](###2.2.2-blueprints)
    - [2.2.3. Tools and Editor ](###2.2.3-tools-and-editor)
      - [2.2.3.1 Level Editor ](#####2.2.3.1-level-editor)
      - [2.2.3.2 Blueprint Editor ](#####2.2.3.2-blueprint-editor)
      - [2.2.3.3 Other Editors ](#####2.2.3.3-other-editors)
  - [2.3. 3rd Party Softwares/libraries ](##2.3-3rd-party-softwares/libraries)

- [3. Game Mechanics](#3-game-mechanics)
  - [3.1. Core Mechanics](##3.1-core-mechanics)
  // Needs details
  - [3.2. Character Physics](##3.2-character-physics)
  - [3.3. Level Settings ](##3.3-level-settings)
    - [3.3.1. Setting up a level ](###3.3.1-setting-up-a-level)
    - [3.3.2 Level Organization ](###3.3.2-level-organization)

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
This is a 2D side scroller action game where you play as a samuraï named Kazuo during feudal Japan's era. The player's objective is to cross a level where he must defend himself against enemies with his katana. 

This is a hardcore game where the player has only one life and will have to start all over again in case of a Game Over. In addition, he has a time limit of 10 minutes to reach the end of the game without getting killed.




# 2. Technologies used


## 2.1. Game Engine
The rendered product will be a game made with the Unreal Engine game engine.

It is a famous and free game engine developed by Epic Games. 

This amazing software enable creators across industries to deliver cutting-edge content, interactive experiences, and immersive virtual worlds. You can make any type of game such as platformers, FPS or side scrollers (2D or 3D). 

The latest updated version is 5.1, but our game is using the 4.27.2 version available on the Epic games launcher.

## 2.2. Development Tools

For this game, we have used the provided 2D Side Scroller template to build our level in Unreal Engine.
### 2.2.1 Scene

When we want to create a new project by opening Unreal Engine, the Project Browser propose us several categories depending on our works, like games, movies, architecture, product design and more.

After choosing to create a game template, the browser propose us different templates which serve as basic point depending on the kind of game we want (FPS, Virtual reality, etc...)

For this game, we have used the provided 2D Side Scroller template to build our level in Unreal Engine. It's using a 2D sprite as a character using texture base animation where the camera is positioned at the avatar's side.

In fact, it's the 2D paper version of another template, Side Scroller, more for using 3D characters.

Then, you just have to set the project settings (Blueprints or C++, quality, platform...), set a path location, and name your project before creating it.

### 2.2.2 BluePrints
Instead of using common scripting languages to program our game, like C++, we have decided to rely on blueprints when using Unreal Engine 4.

This system is extremely flexible and powerful, allowing designers to use virtually the full range of concepts and tools generally only available to programmers. 

Generally, Blueprints are visually scripted additions to our game. They allow us to create and modify complex gameplay elements by connecting Nodes, Events, Functions, and Variables with Wires. Indeed, they are used for various purposes (object construction, individual functions, and general gameplay events) that are specific to each instance of the Blueprint in order to control behavior and other features.

2 types of blueprints are commonly used:

-Level Blueprint: It's a specialized type of Blueprint that act as a level-wide global event graph. Each level in our project has its own Level Blueprint created by default that can be edited within the Unreal Editor, but cannot be created through the editor interface.

Furthemore, it's used to reference and manipulate Actors within the level, control cinematics using Matinee Actors, and manage things like level streaming, checkpoints, and other level-related systems. 

-Blueprints class:It's an asset allowing content creators to easily add functionality on top of existing gameplay classes. Created inside Unreal Editor, it defines a new class of Actor which can then be placed into maps as instances that have a specific behavior.

Most common Parent classes:
-Actor: object that can be placed or spawned in the world.
-Pawn: actor that can be "possessed" and receive input from a Controller.
-Character: pawn that includes the ability to walk, run, jump, and more.
-PlayerController: actor responsible for controlling a Pawn used by the player.
-Game Mode: defines the game being played, its rules, scoring, and other faces of the game type.

In fact, Blueprint Classes are great for making interactive assets such as doors, switches, collectible items, and more... And Level Blueprints can also interact with Blueprint classes.


### 2.2.3 Tools and Editor

When discovering Unreal Engine while ccreating a scene, there are several tools and editors to takine into account.

#### 2.2.3.1 Level Editor

By default, Unreal Engine 4 will open to this interface named the Level Editor:


It's the primary editor where we construct our gameplay levels.  Indeed, it provide us the core level creation functionality for Unreal Editor. Its purpose it to help is create, view, and modify levels, by mainly placing, transforming, and editing the properties of Actors.

Furthermore, it shows a level within a 3D environment (even in 2D) in which we place a series of objects and geometry to define the game world we want to conceive, shown in the world Outliner. There are also details about each objects, such has the Transform properties having numeric entry fields for the X, Y and Z axes. Indeed, we can modify their location, their rotation, and their scale.

It's also possible to change the perspective view of the scene.

Above the scene, a panel is displaying a group of commands, providing quick access to commonly used tools and operations.

#### 2.2.3.2 Blueprint Editor

Another important editor is the Blueprint editor: it's where we work and modify blueprints. It has different features:

- Viewport: it's the window where we can examine the object. Just like the level editor for scenes, we can change the perspective and see, as an example, how our character would look like.   
- Event Graph: it contains a node graph that uses events and function for calling  to perform actions in response to gameplay events related the Blueprint. Indeed, this is where we focus on the programming of our character's behavior depending on the player's input.

#### 2.2.3.3 Other Editors

And for our 2D Side Scrolling game, we also used these editors very often:

- Paper 2D Sprite Editor: it's a tool to set up and edit individual sprite assets. We can decide its dimension, its collision settings, and also the sprite its based from.



- Flipbook editor: for dealing with the sprite's animations, the editor uses flipbooks. Also referenced as 2D Paper flipbooks, it's an hand-drawn animation where a series of images are "flipped" through to produce motion. Indeed, flipbooks are a series of key frames, each of them containing a sprite to be displayed.


The flipbook editor allow us to create and/or preview 2D animations by using our sprite assets. Then, we tune or tweak the duration in which a sprite is displayed, but we can determine the overall playback speed of the Flipbook animation through the Frames Per Second option.

### Blueprints

## 2.3. 3rd Party Softwares/libraries
We are using several other softwares to help us with the project management:

- Google sheets: it's a spreadsheet program included in the web-based Google Docs Editor suite. It allow us to create and edit spreadsheets, allowing us to share data in Team such as KPIs or the test cases.

- Github: a famous code hosting platform for version control and collaboration. We use it to push progress on our game's scene and its related documentation.

- Visual Studio Code: a code editor used to write programs, but also to build and debugg modern web and cloud applications. However, we mostly use it to write our documentation in markdown format.

- ChatGPT: a chatbot prototype using Artificial Intelligence developped by OpenAI. We sometimes use it to ask diverse questions.

# 3. Game Mechanics

## 3.1. Core Mechanics
We play as Kazuo, the game's main protagonist, where we travel through a 2D scrolling level. 

Walking: the player move either on the right or on the left in order to progress. If he walk towards a wall, he will still have his walking animation without really moving.
Because it's a 2D Side Scroller, the character has limited directions: forward, backward, and jumping.

To program his different actions, we have to edit the 2DSideScrollerCharacter asset (the player's sprite) to set their behavior.

Jumping: the player can jump to reach a higher place, or jump above an enemy to avoid him. He can jump vertically, but he can also jump diagonally if he also move on the left/right during his jump animation.
Walking: 
- The player move either on the right or on the left in order to progress.
- We are using the Input Axis event named "MoveRight" to make the character move with the vectors coordinates X=1, Y=0 and Z=0. This event provides the current value of the MoveRight axis once per frame when the input is enabled for the containing vector. If the value is negative, the character will move to the left.
- If he walk towards a wall, he will still have his walking animation without really moving.

Attacking: the player takes his katana and swings it a front of him, extending his attack hitbox in order to touch his enemies. He has the possibility to attack several times to trigger different sword animations (and perhaps different hitboxes) and create combos.
Jumping: 
- The player can jump to reach a higher place, or jump above an enemy to avoid him. 
- The input action jump is used when the keys used for the jump are pressed or released. At this moment, a pending launch velocity of Z=800 will be set for the character. The velocity will be processed until the character reaches his falling state.
Indeed, a counter has been set for a limit of 2 jump. If the counter reaches its max, the character's velocity won't be launched anymore as long as he doesn't land back on the surface.
- He can jump vertically, but he can also jump diagonally if he also move on the left/right during his jump animation.

Attacking: 
- The player takes his katana and swings it a front of him, extending his attack hitbox in order to touch his enemies. 
- The input action Attack is used when the keys used for the jump are pressed or released. At this moment, a box collision for creating the hitbox attack is created.
It also possesses a counter indicating how much time the attack input has been pressed in a 0.3s delay. Depending on the counter number, a different attack animation will be displayed.
- He has the possibility to attack several times to trigger different sword animations (and perhaps different hitboxes) and create combos.

Dashing:
- While the player is moving, he can also dash to move faster. This mechanic is useful when the player want to progress at a faster rhythm, and in situations when the path is clear. 
- When we press the required button (Left Shift), a pending launch velocity of Z=100 (multiplicated by 800) is set for the player.
- He can also dash while jumping to make huge leaps.

Dashing: When the player is moving, he can also dash to move faster. This mechanic is useful when the player want to progress at a faster rhythm, and in situations when the path is clear. He can also jump while dashing before landing on the ground and continuing to run.

Crouch: The player can crouch, so he will have a kneeling animation. As a result, his hitbox's height will be reduced, and this could allow him to avoid projectiles sent by enemies.

## 3.2. Character Physics
In our game, we want to simulate our character's physics to make him feel like a strong samuraï.

For creating a "skeleton" for our character, we first need to create a blueprint with the class PaperCharacter, useful for 2D games.

When viewing the character in the viewports, we can have a preview on how the character will look in a 3D grid, behave if he is animated, and what would be his characteristics in the environment he is set in.

There is a capsule around the character called the Capsule component which contains several other components:
- The character sprite, which uses a pixellized picture representing Kazuo, and can itself contain a box for simulating the attack's hitbox.
- The CameraBoom (spring arm component), which creates a "camera" placed within a distance for the player. Used to "film" the sprite, it has a springarm in order to "pull" the camera if it collides with an obstacle.
- The capsule collision, which is used to simulate collision with other objects like obstacles or enemies. Its half height is 96 and his radius is 40.

Another component show the character's movement: it allows to hand the players different movement's physics.

-Walk: the character as a max ground speed of 600.0. He can step at a maximum height of 45 without jumpinh, and a ground friction of 3.0 to affect movement control when braking. Kazuo can also walk off ledges and maintain horizontal ground velocity.

-Jump: Kazuo has a jump velocity of 100, with a air control of 0.8 to allow the character's movement in the airs.

-Attack: Kazuo's sprite has a box collider which is its attack hitbox. It has a length of /// and a width of ///, and is activated when the player press the Attack input.

The first attack last /// frames and has a endlag of /// frames.
The second attack last /// frames and has a endlag of /// frames.
The third attack last /// frames and has a endlag of /// frames.

## 3.3. Level Settings

### 3.3.1 Setting up a level
The game contains 6 levels in total: 3 regular levels, and 3 boss levels.

A level is one of the basic assets, defined as a collection of actors (light, volumes, mesh instances...). It's referring to the scene we create for our game experience. In Unreal Engine, multiple levels can be loaded and unloaded into the World for creating a streaming experience.

When creating one, we are able to build a new world by integrating as many assets as we want, such as character sprites, tiles, decorations, and other optsions like the light direction.

By selecting the tool "Blueprints'" in the main Toolbar, we can access to the Open Level Blueprints. Shown in an event graph, they are used to set the number of enemies to kill to succeed the level, how much time the player must win, and other options.

A blueprint class is also used to allow the loading of the game and indicate the next level which will load once the first level is done. For now, we don't have to save our game due to our decision to make the player start over to the beginning if he dies.

### 3.3.2 Level Organization.

For the regular levels, the player has to move through a wide space, containing enemies and platforms.

To finish the level, the player doesn't only have to reach the end of the map, he also needs to kill every enemy present in place. If he succeeds, he will be instantly teleported in the next level.

All enemy will want to kill the player, so he will need to defend himself from them and travel towards the level by jumping on platforms. Moreoever, he will have to arrive to the end before time is out.

Regarding the boss levels: the player will face an enemy stronger than any common foes. The bosses have several HPs, and the player must find the right strategy to defeat him before he is killed or if he runs out of time. 

If he succeeds, the boss will drops a parchment that the player must pick up to finish the level. It will contain a random message about the Samuraï's code.

-FREE SAMURAI PIXEL ART SPRITE SHEETS (https://craftpix.net/freebies/free-samurai-pixel-art-sprite-sheets/)
The levels are organized in a way a regular level is followed by a boss level, that is itself followed by the next regular level.



# 4. Game Assets
Here are the list of game assets we used for the making of our game:

| Name  | Link   | Type of assets   | Picture   |
| ----------------- | :-------------------: |:-------------------: |:-------------------: |
| FREE SAMURAI PIXEL ART SPRITE SHEETS  | [Link](https://craftpix.net/freebies/free-samurai-pixel-art-sprite-sheets/)   | 2D Characters spritesheet   | <img src="./Images/Asset1.png" width="100" height="100" />   |
| FREE NINJA SPRITE SHEETS PIXEL ART  | [Link](https://craftpix.net/freebies/free-ninja-sprite-sheets-pixel-art/)   | 2D Characters spritesheet   | <img src="./Images/Asset2.png" width="100" height="100" />   |
| FREE GHOST PIXEL ART SPRITE SHEETS  | [Link](https://craftpix.net/freebies/free-ghost-pixel-art-sprite-sheets/?num=3&count=649&sq=sprites%20pixel&pos=0)   | 2D Characters spritesheet   | <img src="./Images/Asset3.png" width="100" height="100" />   |
| FREE GREEN ZONE TILESET PIXEL ART  | [Link](https://craftpix.net/freebies/free-green-zone-tileset-pixel-art/)   | Tileset and objects for 2D platformer   | <img src="./Images/Asset4.png" width="100" height="100" />   |
| FREE SWAMP GAME TILESET PIXEL ART  | [Link](https://craftpix.net/freebies/free-swamp-game-tileset-pixel-art/)   | Tileset and objects for 2D platformer   | <img src="./Images/Asset5.png" width="100" height="100" />   |
| FREE MARKET CARTOON 2D GAME TILESET  | [Link](https://craftpix.net/freebies/free-market-cartoon-2d-game-tileset/)   | Tileset and objects for 2D platformer   | <img src="./Images/Asset6.png" width="100" height="100" />   |
| FREE BUSH ASSETS PIXEL ART PACK  | [Link](https://craftpix.net/freebies/free-bush-assets-pixel-art-pack/)   | Objects for 2D platformer   | <img src="./Images/Asset7.png" width="100" height="100" />  |
| FREE ROCKS PIXEL ART ASSET PACK  | [Link](https://craftpix.net/freebies/free-rocks-pixel-art-asset-pack/?num=1&count=12&sq=rock&pos=2)   | Objects for 2D platformer   |<img src="./Images/Asset8.png" width="100" height="100" />   |
| Pixel Cave Background  | [Link](https://cutewallpaper.org/21/pixel-cave-background/view-page-21.html)   | Backgrounds for 2D platformer   | <img src="./Images/Asset9.png" width="100" height="100" />   |
| Campfire pixel art 32px  | [Link](https://itch.io/game-assets/tag-campfire)   | 2D Flame spritesheet   |<img src="./Images/Asset10.png" width="100" height="100" />   |




# 5. User Interface

## 5.1. Menus
The game opens on a main menu, showing the character artwork and 3 choices:
-Start Game: allows you to load the game before to start playing
-Options: lead you to another menu for changing sound, etc...
-Credits: lead you to a credits menu showing the name of those who worked on the project.
The game opens on a main menu, showing the game's title, the character artwork, and a Samuraï themed music is being played. 

With his mouse, the player has a menu of 3 different choices:
-Start Game: allows you to load the game before you start playing.
-Options: display a widget allowing you to activate/deactivate the menu music and the in-game music,change the screen resolution (640 x 480pp, 1280 x 720pp, full screen) and modify the control inputs.
-Quit: you can quit the game and close the application.

When you are playing the game but you decide to pause, the game stops, and you have 3 choices appearing in the middle of the screen:
-Resume: stop the pause and continue to play. 
-Options: similar to the one from the main menu.
-Menu: to quit your actual game, and return to the main menu.

## 5.2. Controls
The game is played on PC, so you use the keyboard keys to play the game.

Right Key: allows your character to move on the right.
Here are the default controls for playing the game:

- Right Key: allows your character to move on the right.

Left Key: allows your character to move on the left.
- Left Key: allows your character to move on the left.

Down Key: allows your character to crouch.
- Down Key: allows your character to crouch.

Space Key: allows your character to jump. If used in midair, he performs a double jump.
- Space Key: allows your character to jump. If used in midair, he performs a double jump.

Shift Key: used while your characer is moving, allows him to sadh in order to have a higher moving speed.
- Shift Key: used while your characer is moving, allows him to dash in order to have a higher moving speed.

Left Mouse Key: allows the player to swing his katana to attack a front of him. Clicked several times, he can create a combo attack.
- A Key: allows the player to swing his katana to attack a front of him. Clicked several times, he can create a combo attack.

It is also possible to customize the controls depending on the players' taste.

At the beginning of the level, the default controls are reminded to the player.
## 5.3. HUD Elements
To guide the player, there are 3 pieces of data displayed on screen during gameplay:

-The time: always located at 3/4 of the height of the screen in the middle, it gives the player information about the remaining time.
Either it acts as a warning timecode, telling the player how much he has left to complete the level before a game over occurs, either it just indicate how much time he must wait before going to the next level.

-The enemy counter: on the top-right corner, a number is constantly displayed in some levels. 
It represents the number of enemies the player must kill in order to complete the level. The number decreases by 1 each time an enemy is defeated, and if it hits 0, the player will teleport to the next level.

-Level results: it is located in the middle of the screen. However, it only appears in certain conditions depending on the player actions. Indeed, it displays "WIN" when he manages to finish a panel, or "GAME OVER" if he is defeated or has no time left.

# 6. Optimization

## 6.1. Performance
Unreal Engine provides us many features and possibility to build our game. However, the game's size became heavier the more we use countless assets, such as tiles which take a lot of place.
We also need to make the game's screen resolution appealing enough to make the player motivated to play Ronin's Revenge.

## 6.2. Memory Usage
Dealing with the memory used for creating our game will be important. Indeed, we want to avoid having issues when pushing the game's codes and files in github. So, the game's performance must remain almost untouched when transferring data in the main branch of our project.



# 7. Glossary

| word                                                                                                |                                                                                                    definition                                                                                                    |
| --------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| <img src="./Images/1200px-UE_Logo_Black_Centered.svg.png" width="30" height="30" /> <span id="Unreal Engine">Unreal Engine</span>                                                                     |   Real-Time 3D graphics game engine developed by epic Games              |
| <span id="Game Engine">Game Engine</span>                                                               |        Software framework primarily used for the development of video games.       |
| <img src="./Images/ISO_C++_Logo.svg.png" width="30" height="30" /><span id="C++">C++</span>               |                          C++ is a high-level and object-oriented programming language.                             |
| <span id="Blueprint">Blueprint</span>                  |                                                              Complete gameplay scripting system based on the concept of using a node-based interface for creating gameplay elements from within Unreal Editor.                                                               |
| <img src="./Images/ISO_C++_Logo.svg.png" width="30" height="30" /><span id="C++">C++</span>               |                          C++ is a high-level and object-oriented programming language.                             |
| <span id="Editor">Editor</span> | Software responsible for the definition and creation of all interactive architecture for a segment or level of a video game.   |
| <span id="Game Engine">Game Engine</span>                                                               |        Software framework primarily used for the development of video games.       |
| <span id="Game Over">Game Over</span> | Message displayed on the screen indicating the player's defeat or failure. |
| <span id="Hardcore">Hardcore</span> | Type of game that requires a high user input and time investment in order for users to be successful.  |
| <span id="HP">HP</span> | Meaning "Healing Points", determine the maximum of damage a character can take. |
| <span id="HUD">HUD</span> | Abbreviation meaning "Head Up Display", it's a set of information displayed on screen and informing the player about his character or his environment (score, remaining lives, etc...)  |
| <span id="Input">Input</span> | In video games, mean of interaction between the player and the game. Data is transmitted when the player act on the controller (keyboard, joysticks...).    |
| <span id="Lag">Lag</span> | Time delay between a player's input and the game's reaction.   |
| <span id="Level Design">Level Design</span>         |            Game design process involving the creation of video games levels.             |
| <span id="Mechanics">Mechanics</span> | In Game Design, rules and procedures guiding players through the game.  |
| <span id="Physics">Physics</span> | In video games, use of real life laws of physics to make a game more realistic and immersive.   |
| <span id="Samuraï">Samuraï</span> | In feudal Japan, he's a member of a powerful military castle.   |
| <span id="Side Scroller">Side Scroller</span> | Type of game viewed from a side-view camera angle where the screen follows the player.    |
| <span id="Sprite">Sprite</span> | Image (mostly pixelated) representing game assets like player characters, enemies, projectiles...   |
| <span id="Systems">Systems</span> | In Game Design, rules defining how the game react to player inputs.  |
| <span id="Hardcore">Hardcore</span> | Type of game that requires a high user input and time investment in order for users to be successful.  |
| <img src="./Images/1200px-UE_Logo_Black_Centered.svg.png" width="30" height="30" /> <span id="Unreal Engine">Unreal Engine</span>                                                                     |   Real-Time 3D graphics game engine developed by epic Games              |




