# DoomAlef
Doom Alef is a prototype for a Retro-style first-person shooter game, implemented in Unreal Engine 5, reminiscent of the Doom-style gameplay. The game development is built upon the First Person template of Unreal Engine 5. The template generally comes with the first-person character controller and its weapon system. However, Doom Alef has its own weapon system, written from complete scratch and only uses the first-person character controller of the template. 

## Game objective
The game's objective is for the player to find three different keys of varying colors: red, orange, and blue. These keys are essential for unlocking doors throughout the game environment. The ultimate goal is to locate the final key (the blue key), which grants access to the last door and marks the player's victory. Each key corresponds to a different room, and obtaining them allows the player to progress through the game. Some keys may be found in locked rooms, requiring the player to discover a separate room key to proceed and obtain the desired key.

## Game AI
Along the way, the player will encounter various enemies with distinct abilities that must be eliminated. The enemy characters are created based on an 8-directional sprite system. They rotate toward the player character if they can either see him or hear him shooting and depending on the abilities it has attacked the player. If the enemy cannot see the player, it moves randomly within the environment. 
The first enemy type engages in melee attacks, charging toward the player to deliver hits, with the following behavior tree

![BPMeele](https://github.com/arashsheikhlar/DoomAlef/assets/53377712/e4452218-8df6-49fb-9faf-6dfa71d462ee)

The second enemy type possesses both melee and ranged attacks, using projectiles to shoot at the player, with the following behavior tree

![BPHybrid](https://github.com/arashsheikhlar/DoomAlef/assets/53377712/2a53a73a-f480-4d9f-93c7-506e45eaacb8)

Moving and attack animations are given to the enemies by using the engine's flipbook creation tools.

## Weapon system
The game offers five different weapons: pistol, shotgun, minigun, plasma rifle, and rocket launching weapon. The player must pick them up from different locations throughout the game.
The system involves the creation of master weapon blueprints, which contain essential information about a weapon's damage, ammo type, etc. Based on these master blueprints, various child weapons are generated.
The weapons utilize a line trace system, an invisible line projected from the weapon when fired. When the line hits something, damage is applied to the target. This is detailed in the "Fireweapon" function within the Base Weapon blueprint. The UE5's first-person character template includes default controls for looking, moving, and jumping. Additional shooting controls called "IA_Fire" are implemented to handle weapon firing.
Each weapon type is associated with a specific ammo type and has a maximum ammo capacity. Players can only fire weapons if they have enough ammo. The available ammo types are Bullet, Shell, Rocket, and Cell.

### Weapon bobbing system: 
when the player character is moving the weapon bobs both left&right and up&down. The weapon does not bob when the player is shooting.

### Weapon Swapping system: 
this allows the player to change the weapon to a desired one by pressing keys from 1 to 6, only the desired weapon is already picked up.


## Game features and interactable world objects
### Player Hud
shows the amount of weapons ammo and the player's health. The Hud gets updated with the damage, weapon firing, and ammo/health pickup.

### Explosive barrel
 there are explosive barrels that, when the player shoots them, can explode and significantly damage anyone who is near them.

### An acid pool
  there is an acid pool the player has to avoid not to fall into, as it damages the player.
### Shield
 other than the health kit, there is armor that the player can pick up.

### sprinting system
This enables the player character to move at a higher speed by pressing shift button.

### Sliding doors
 there are sliding doors within the game that grant access to different parts of the game world. Some of the doors need specific key cards to be unlocked.


## Gameplay mechanics
Classic Doom games incorporate a combination of distinct game mechanics. In this particular version, the following mechanics are featured,
Actions: Players have the ability to shoot enemies using a variety of weapons or resort to hand-to-hand combat when ammunition runs low. Each weapon has unique characteristics that offer different shooting experiences to the player.
Exploration: Essential items such as door keys, advanced weapons, health kits, and armor are cleverly concealed in various rooms throughout the game environment. This design encourages players to explore and navigate different sections of the environment in order to uncover secrets, earn rewards, and unlock new areas.
Movement: The first-person character is capable of walking and sprinting in four different directions in a 3D environment. Sprinting enables players to swiftly traverse empty or uneventful portions of the environment, allowing them to bypass mundane areas more quickly.

## How to install and contribute to the project
Go to https://www.unrealengine.com/en-US/download and download the Epic Games launcher. 
In the launcher, head over to the library tab and install the latest version of Unreal Engine 5.
Then, clone the repository into your computer and open the retrofpsgame.uproject, which is the main Unreal Engine project file.
### To add more features to the prototype-level map of the project, 
Go to the content folder as following 
...\DooAlef\Content\Levels
and Open levelPrototype.umap. This will run the prototype level where you can change the map.
### To Play the game on Windows
Download the following folder
https://drive.google.com/drive/folders/1id0ClVW_haBrm57rs09K12PtBpyYgU3L?usp=sharing
and open retrofpsgame.exe. This will take you to the game's main menu.


