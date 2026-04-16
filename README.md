# GDIM 33 In-Class Activities
## W1
### Activity 1
#### Inspiration Board Link:
https://docs.google.com/drawings/d/19N4TGcwLQ5mR7HmwdiY5fCTBPbsWcZhjpol8QFy02LI/edit?usp=sharing

#### 1. 
I have a specific interest into roguelike games with some aspects of supernatural horror. Games with a setting in liminal spaces are also my favorites since they establish an oppressive and uneasy atmosphere.

#### 2.
We both like roguelike, lovecraftian games, preferrably 2D games with a good, suspenseful storyline. 

#### 3.
Our LA love RPG games such as Undertale and Deltarune but ended up creating a 3D action puzzle game. Mine is quite different as I prefer a non-linear gameplay loop. 

### Activity 2
#### Pitch Breakdown Link:
https://docs.google.com/drawings/d/1Vwa2GCTFOWZ9fGL_lilL8FELztcmid0OwFhaSD9LxCY/edit?usp=sharing

I plan to make a 2D combat roguelike SLG/SRPG, where the goal is to traverse through a grid map into the sxit per level. Player control multiple characters, and they act in turns. Getting all surviving characters into exit clears the level.

The level map is a grid (most likely rectangular) that contains obstacles that block movement, treasure/power-ups in different spots, enemies scattered in different areas, areas that bring different buffs/debuffs (e.g. Snow terrain that lowers agility), etc.

Character attributes may include the following:
Hitpoints, defence, attack, range, agility, mana, unique skills, etc.; enemy characters also have an alert radius that determines how close player's characters may approach them until they come in combat. 

Each turn, a character will choose between:
Traverse some distance through the map (distance determined via agility), attacking an enemy (must be in-range, damage determined by self's attack and target's defence), using a skill (consumes mana or other resources), etc. 

After they finish the action, their turn will end and the next character in sequence begins their turn. It is possible that to add mechanisms that allow multiple actions per turn per character in future development. Each enemy will have a unique ai. 

The aesthetic of the game would probably be something lovecraftian.

## W2
N/A (there is no devlog for week 2)

## W3
### Activity 1
#### New Pitch Breakdown Link:
https://drive.google.com/file/d/11DBX-YsytkqCEoSsYu8VwVuhDdAKxQEf/view?usp=sharing

### Activity 2
#### 1.
This allows other objects in the scene to access the click npc event when adding new logic that requires interaction with this event.

#### 2.
The Debug.Log() node allows immediate notification when an event is triggerered or a certain node on the logic chain is reached in the console.

#### 3.
For my vertical slice in particular, the set cursor lock state is not relevant. My game is a top-down 2D game that requires the player to click on the GUI to input commands, in which I do not want the cursor to be locked.

#### 4.
My vertical slice would use the concept of game states. My game is a turn-based SRPG, where in each turn, there would be a preparation state for the player to input their commands, and an action state to execute and display the results of the commands.

