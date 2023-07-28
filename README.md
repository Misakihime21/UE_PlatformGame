# UE_PlatformGame
Platform Game with Paragon assets

-------

WHAT IS DONE:

- created new level;
- the Shinbi character added;
- changed the view on camera boom and the character's movement;
- the basics obstacles added;
- health bar widget with changeble color.

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
- heal sphere.

-------

WHAT TO IMPROVE

+ the climbing bag is still there when the angle of a jump is weird
	prbly needed to change WALL NORMAL valuable so it isn't rotates with character that much.
- Gideon's running - change AnimBP so he doesn't need Accelerating always;
- bug when jumps on the enemy - character is thrown away from the Y0 route
- death screen + new game.

ANIMATION:
- the hanging animation: hands are too wide;
- the crouching animation: character looking in the wrong side;
- death animation;
- on-hit animation;
- magic damage animation instead of collision hit.