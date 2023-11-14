# UE_PlatformGame
Platform Game with Paragon assets

Play here: https://misakihime21.itch.io/path-of-the-guardian 

"Iron chain" (https://skfb.ly/6VsTr) by DaBoRi is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).
-------

WHAT IS DONE:

- created new level;
- changed the view on camera boom and the character's movement;
- the basics obstacles added;
- health bar widget with changeble color;
- level transition;
- respawn and checkpoints;
- reset on R;
- effects
- main menu;
- end when every items collected (BP_Collectable);
- sounds;
- assets;
- blocking volume added.

SHINBI
- the Shinbi character added;
- attack;
- 

CROUCHING
- added new Input for Ctrl (crouching), E (interaction);
- UE4 animation from AnimStarterPack transfered via IK_Retargeter for Paragon Shinbi;
- added Crouching BlendSpase;
- added Animation BP for Shinbi.

CLIMBING
- retargeted animation for climbing;
- detecting walls and their height;
- implemented hanging from the ledge mechanic;
- Space is for Climbing Up, S or DOWN is to Drop down;
- new collision type for objects that you can climb.

ENEMY
- added Gideon;
- patroling works from one PatrolPoint to another (choose in the details of an actor);
- use NavMesh to show the area of action;
- attack animation;
- enemy health bar;
- enemy death;
- forced "IsAccelerating" for Gideon to make him run.

DAMAGE
- added Health and on-hit damage;
- character's immunity to a damage after hit; 
- character bouncing after being damaged;
- fadeout after death.

PLATFORM
- moving platforms (duration in sec);
- platforms activating by E button (float duration from 0 to 1);
- destroying platforms (could also be used as damaging platforms from above);
- door and key;

COLLECTABLES
- heal sphere;
- double jump booster (can have only one at the time);
- collectables;
- key;
- UI for collectables.

END SCREEN
- death count;
- collectables;
- reset button.


-------

WHAT TO IMPROVE

+ the climbing bag is still there when the angle of a jump is weird
	prbly needed to change WALL NORMAL valuable so it isn't rotates with character that much.
+ respawn on the last checkpoint  BUTTON;
+ death after PainVolume - fadein isn't working;
+ death count - is going to null in BP SHinbi. transfer count to Gamemode. + prbbly has key there would be better;
+ respawn default point (from the start)
	RespawnLocation default set manually to a player start location;
+ death screen + new game;
+ boost UI isn't disappear when you take another boost too fast;
+ bonus UI didn't dissapear after death\\reset;
+ interactive platforms without button;
+ platform changed to the rock mesh;
+ on-step platform come back in case u fell;
+ oninput platform rotation;
+ text ui modified;
+ booster and key ui improved;
+ "You need the key" for the ending door;
+ fixed climbing after the falling plaftorms if u fall earlier;
+ door leads to ending;
+ kills count;
+ non-static damage - it's gonna look better if the damage is within the certain range, like 20-30;
+ health sphere aren't used with full HP + UI;
+ new look for menu (pictures, etc.);
+ UI booster timer;
+ pause;
+ Gideon turning when is attacked in the back;


SOUNDS
- checkpoint sound;
- background music change;


BUGS
- jumps aren't working properly  - maybe waiting for animation to stop; \\cant jump from running
- Shinbi's attack bug sometimes and doesn't reset
- bug when jumps on the moving actors - character is thrown away from the Y0 route;
	partly fixed: from Movement Input disabled Get Control Rotation. + added blocking volume
- somehow falling platforms doesn't really falls;	




ANIMATION:
- Gideon's running - change AnimBP so he doesn't need Accelerating always;
- the hanging animation: hands are too wide;
- the crouching animation: character looking in the wrong side;
- death animation;
- on-hit animation instead of LaunchCharacter (immune to a damage);
- animation for the environment damage (Branch False | immune to a damage);
- magic damage animation instead of collision hit;
- after crouching still there is running animation instead of idle.



- color code for ledges when it's climbable;
- parent class for platforms and collectables;

to respawn enemies and items after death  - use "spawn actor from class" in respawn logic

