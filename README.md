# UE_PlatformGame
Platform Game with Paragon assets

Play here: https://misakihime21.itch.io/path-of-the-guardian 

"Iron chain" (https://skfb.ly/6VsTr) by DaBoRi is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).
-------

WHAT IS DONE:

LEVEL 
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
- on-step platform come back in case u fell;
- oninput platform rotation;
- door and key;

SOUNDS
- sound for attack;
- checkpoint sound;
- falling rocks sound;
- ui click sound;
- background music change;

COLLECTABLES
- heal sphere;
- double jump booster (can have only one at the time);
- collectables;
- key;

ANIMATION
- the crouching animation: character looking in the wrong side;
- death animation;
- animation for the environment damage (Branch False | immune to a damage);
- after crouching still there is running animation instead of idle.


UI 
- pause;
- UI for collectables;
- text ui modified;
- credits page;
- booster timer and key ui;
- death screen + new game.


END SCREEN
- death count;
- collectables;
- reset button;
- kills count;

BUG FIX
- the climbing bag is still there when the angle of a jump is weird (changed WALL NORMAL valuable so it isn't rotates with character that much);
- 
- boost UI isn't disappear when you take another boost too fast;
- bonus UI didn't dissapear after death\\reset;


-------

WHAT TO IMPROVE

+ respawn on the last checkpoint  BUTTON;
+ death after PainVolume - fadein isn't working;
+ death count - is going to null in BP SHinbi. transfer count to Gamemode. + prbbly has key there would be better;
+ respawn default point (from the start)
	RespawnLocation default set manually to a player start location;
+ interactive platforms without button;
+ platform changed to the rock mesh;
+ "You need the key" for the ending door;
+ fixed climbing after the falling plaftorms if u fall earlier;
+ door leads to ending;
+ non-static damage - it's gonna look better if the damage is within the certain range, like 20-30;
+ health sphere aren't used with full HP + UI;
+ new look for menu (pictures, etc.);
+ change quest item appearance and the name in the opening cutscene;
+ falling platforms bugfix;
+ attack fix - isn't able to attack while crouching\climbing\jumping; 
+ remove texts after gideon\shinbi texts;






ANIMATION:
- Gideon's running - change AnimBP so he doesn't need Accelerating always;
- the hanging animation: hands are too wide;
- on-hit animation (magic damage instead of collision hit) instead of LaunchCharacter (immune to a damage);


BUGS
- jumps aren't working properly  - maybe waiting for animation to stop; \\cant jump from running
- Shinbi's attack bug sometimes and doesn't reset
- bug when jumps on the moving actors - character is thrown away from the Y0 route;
	partly fixed: from Movement Input disabled Get Control Rotation. + added blocking volume
- on-step plaftorms are not coming back when you jump on plaftorm a few times in a row;
? Gideon turning when is attacked in the back?;
- after death\reset nodes may fail on trying to connect to the BP_Shinbi;




- sound settings;
- color code for ledges when it's climbable;
- parent class for platforms and collectables;

to respawn enemies and items after death  - use "spawn actor from class" in respawn logic

