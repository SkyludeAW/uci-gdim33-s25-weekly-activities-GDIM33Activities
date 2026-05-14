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

## W4
### Activity 1
My current dev has the basic turn based movement system and includes the attack action of two dummy characters. One dummy enemy exists, and does not have any AI right now, so the playtesting goal is mostly about identifying any potential bugs or suggestions on contents.

#### Playtesting Team:
Gong Chen, Ruichen Ma, Ziyue Yang

#### Playtest Notes
Right now, the camera teleports when moving from character to character between turns, and the playtesting team suggested it could be smoothened up a little. The character also teleports from tile to tiles, and also stutter during what is supposed to be a continuous movement, which should also be fixed. There are not enough content right now to provide exact feedbacks, but some idea about potential contents include a spreading, festering terrain tile. 

### Activity 2
1. Yes, as the logic structure of creating and activating the chain of dialogues is already established through C# code and visual scripting. The only things a writer would need to add are new ScriptableObject DialogueNodeW4s that contains the displayed text and possible player replies, which themselves links to their own subsequent DialogueNodeW4 and so on. Only data, not logic is modified here, so no code or graph need to change.

2. To create a large amount of dialogue options, especially when there are reused dialogue nodes with different options, such recursive-like method of extending the dialogue chain would be considerably inefficient. Creating a procedural, code-based list of nodes and possible replies allow the addition of custom dialogue chain logic and also eases/cleanly organize the existing dialogue lines and replies. 

3. The "Regenerate Nodes" button scans and updates if any new or custom classes are added, and creates their associated nodes, such as getters and setters of member variables, respectively. Unity's default visual scripting graph could possibly exclude any nodes associate to non-Unity-native classes or packages.

## W5
### Activity 1
1. Basic animation controllers and animation states for each character.
- Create the animation from the sprite sheets of each character
- Create animation states idle, movement, attack, etc. for each character
- Create triggers or variables in the animator and apply them to transitions in different animation states
- Create code-based triggers to alter the animation variables in the state machine system

2. Animation events incorporated into the animation that links up with other events such as initialization of projectiles or visual effects.
- Create animation events in attack trigger keyframes and start/end of animations for each character
- Create a custom animation listener class that acts according to the animation events
- Create a vfx/sfx system that uses the animation listener class to sync with the animation of characters

### Activity 2
I have not finished making the art assets for my game yet, so I used empty aniamtions as placeholders and created the animation states and the trigger variables first. I created the AnimatinListener class that contains multiple C# events such as AnimationBeggin, AttackTrigger, AnimationEnd, etc. I used a switch statement to take in an enum argument in the parameter of the method triggered when the animation event is reached to determine which specific event to trigger. This setup allows the game objects that has the AnimationListener class to react accordingly in their own unique ways when a specific keyframe is reached, such as spawning the bullet for a ranged attack. I could also make the C# events a mutable list that allows more flexibility in the amount of reactions to the keyframe of animations. However, I am still finishing up on my code-based state machine for my characters, and will add in my transition triggers for animations after I have completed the state machine.

## W6
### Activity 1
Link to Milestone: https://skyludeaw.itch.io/unbecoming
I slacked off this week and did not add new stuff to my game other than fixing a few minor bugs...

### Activity 2
1. Since color here is represented by a float, multiplying the RGB values results in a smaller value, which makes the overall color darker in the RGB color system. 

2. Multiplying two alpha value that are less than 1.0 results in a more translucent value, as opaqueness scales with the alpha value, with 1.0 as completely opaque and 0 as completely transparent.

3. The UV0 came from the first, default UV that is attached with the shiba model.

4. This is exciting as I had often seen those filters or layer modes in Photoshop without knowing how they exactly work. I can now create unique filters or visual effects.

## W7
### Devlog Questions
1. They came from the vertex's color in the mesh data of the applied objects.

2. The color on the edges came from an interpolation between the color of the vertices that composes the edge.

3. Without specific mapping via the 2d texture and UV, the color of each pixel may only be approxiamated with the vertex color on the mesh data. Though being less detailed, this may act as a fallback for when the texture goes missing, or a solution for machines with less powerful GPUs.

4. There is a small spot on the butt of the shiba that has a conspicuously different color when applying shaders that utilizes the vertex normals, which meant that specific vertex's normal might be wrong.

5. There can be some sort of debug shader that reacts extremely to things in the surrounding environment, such as light or some sort of hitbox. This allows quick visualization and validation of if any mechanism is being placed out of place and affecting this object with unintended effects. For example, there might be a field of vision collider from some enemy that somehow pierces through a wall that it is not supposed to, and debug shaders like this may alarm us developers immediately.

6. That specific vertex's normal data might be off, which affects the lighting calculation in the shader graph.

7. The additive blending mode adds the RGB values of the shader color to its background, which makes light areas of the shader appear lighter when rendered, while keeping black areas that have a RGB value of (0,0,0) transparent, unlike the multiply blending mode which makes the RGB value smaller and creates a darkening effect. This makes additive good for glowing, translucent VFXs like fire.