# UE_PlatformGame
Platform Game with Paragon assets

Play here: https://misakihime21.itch.io/path-of-the-guardian 

-------

WHAT IS DONE:

- created new level;
- the Shinbi character added;
- changed the view on camera boom and the character's movement;
- the basics obstacles added;
- health bar widget with changeble color;
- level transition;
- respawn and checkpoints;
- reset on R;
- effects
- main menu;
- end when every items collected (BP_Collectable);
- death count;
- sounds;
- assets;
- blocking volume added.

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

- Gideon's running - change AnimBP so he doesn't need Accelerating always;
- bug when jumps on the moving actors - character is thrown away from the Y0 route;
	partly fixed: from Movement Input disabled Get Control Rotation.
- interactive platforms without button;
- pause;
- UI booster timer;
- killing the enemy + UI of his health (maybe a bonus after killing?);
- color code for ledges when it's climbable;
- health sphere shouldn't be used when HP is full + UI - when you pick it up or when you can't;
- jump doesn't response well - sometimes it isn't working;
- platforms oninput and onstep broke;
- add reset button on the end;
- parent class for platforms and collectables;
- change environment to more realistic one, so it wouldn't be flying platforms, but the houses,
 walls, mountains and so on;
- 
 После приседания проигрывается анимация бега и не совсем понятно, чем опасна трава,

ANIMATION:
- the hanging animation: hands are too wide;
- the crouching animation: character looking in the wrong side;
- death animation;
- on-hit animation instead of LaunchCharacter (immune to a damage);
- animation for the environment damage (Branch False | immune to a damage);
- magic damage animation instead of collision hit.


#ue кто нибудь смог зареспавнить акторов после респавна самого игрока?
хочется, чтобы после смерти и возрождения враги и другие предметы тоже были на месте
На сколько помню, тем же spawn actor from class в логике респауна игрока можно добавить

