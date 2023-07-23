# DoomAlef
Doom Alef is a prototype for a Retro-style first-person shooter game, implemented in Unreal Engine 5, reminiscent of the Doom-style gameplay. The game development is built upon the First Person template of Unreal Engine 5. The template generally comes with the first-person character controller and its weapon system. However, Doom Alef has its own weapon system, written from complete scratch and only uses the first-person character controller of the template. 

## Game objective:
The game's objective is for the first-person character to collect keys with different colors to unlock corresponding doors and ultimately complete the game by entering the last door.

## Game AI
Along the way, the player will encounter various enemies with distinct abilities that must be eliminated. The first enemy type engages in melee attacks, charging toward the player to deliver hits, with the following behavior tree
![BPMeele](https://github.com/arashsheikhlar/DoomAlef/assets/53377712/e4452218-8df6-49fb-9faf-6dfa71d462ee)

The second enemy type possesses both melee and ranged attacks, using projectiles to shoot at the player, with the following behavior tree
![BPHybrid](https://github.com/arashsheikhlar/DoomAlef/assets/53377712/2a53a73a-f480-4d9f-93c7-506e45eaacb8)

## Weapon system
The game offers five different weapons: pistol, shotgun, minigun, plasma rifle, and rocket launching weapon. The player must pick them up from different locations throughout the game.

