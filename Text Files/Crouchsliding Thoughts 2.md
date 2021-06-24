*This is a short conclusion to [Part1](https://github.com/heysokam/defragmm/blob/main/Text%20Files/Crouchsliding%20Thoughts%201.md). If you don't want to read the explanation of how/why this idea started, then just stay here.*
## My Crouchsliding vision
_and analysis of why crouchsliding can fit mmod_
### What is crouchsliding
#### 1. Cornering:
Like it was mentioned, crouchsliding can be seen as "just another turning mechanic, equal to the others and irrelevant".  
And this is true, but only if you think about what it DOES, and not what it COULD do.  
Which is: The potential for using it in corners of different radiuses than what AD or W can possibly achieve in CPM.   

Example:
- Sharp corner
- 180 degrees
- 64u radius
- 400u maximum width
- approached at +1500ups or more  

That's literally an impossible corner for AD or W without oversteering or bumping into the wall,  losing -at least- 200ups.  
_(see r7_tech for an example of this: https://youtu.be/WOwLF0MFRQ8?t=13)_

But, with the right cvar values for it, it can be made to require skilful control to execute a sharper turn than AD, at the cost of some speed.  

This way, the player would have to make a choice for their route strategy:  
1. Do I want to use AD for this turn?  
  Considering:  
  - Easier to execute (slightly)
  - Allows me to maintain all my speed (or increase it)
  - Increased overall distance/radius.  
  - Is that extra speed worth the increased overall distance?  
2. Or do I use crouchsliding:  
  Considering:  
  - Harder to execute  
  - Gives me the shortest overall distance.
  - Costs me some speed no matter what, but its effect can be minimized with my skilful control.   

This crouchsliding definition might conflict with AD's oversteering to slow down. But it doesn't with the optimal use of AD for full speed turns. And this use of AD for slowing down with oversteering doesn't consider the reduction of player height that occurs during crouchsliding.  

The reduction in player height during crouchsliding is an aspect of the mechanic that will open even more obstacle options for mappers, and some turns very unique to the mechanic (ie. same corner as before, but going under low beam or into a hole in the wall).

#### 2. Reduced player height:
Lowered player-collision height is only possible to execute in CPM/VQ3 by being submitted to the full effect of ground friction.
Height-based obstacles are possible, but their cost is extremely high. This cost makes them extremely difficult and punishing to implement in a map.

Crouchsliding allows the mapper to design those same obstacles mentioned, but without punishing the player so strongly.
It opens the option to design shortcuts/obstacles that cost just a bit of speed, instead of making the player lose it all no matter what they do.  

The skilful aspect of the mechanic also allows for this strategic choice:   
"Do I choose the faster, but harder to execute, path? Or do I take the longer/easier line?"  
Regular crouching would make that choice not possible, because the speed cost is just too high  
_(and it takes no skill to go under a crouching obstacle without sliding, so there is nothing to master/improve about it)_.

### Crouchsliding in vq3 influenced physics
_Why the added turning rate of CS doesn't belong in vq3 & mmod-Tech physics, but the reduced player height might._
Like it was mentioned before, what makes vq3 and cpm different is not their straight line acceleration mechanics, but their cornering styles.  

Adding the increased turnrate and vector redirection aspects of crouchsliding to VQ3 changes the physics into, essentially, a different version of CPM.
If we want to design a unique VQ3-influenced style, then maintaining that reduced turnrate as much as possible is essential to its design.

This is why I think regular crouchsliding doesn't fit phys_mmod_tech.  
But a different crouchsliding configuration could be useful, because it would allow for the reduced player height aspect of the mechanic, without turning the setting into "just cpm, but without AD".  
A simple `sv_crouchslide_accelerate 0` would achieve this effect perfectly.  
_(removes turning completely during crouchsliding, while keeping its reduced friction and height)_  
It is also simple to explain: "You cannot turn while crouching in mmod_tech, but you can crouchslide in both"

### Crouchsliding in mmod-Race physics.  
Crouchsliding can coexist with AD and W, without it being redundant and irrelevant.  
Making crouchsliding fit in a unique way with CPM-influenced physics is not an issue with the mechanic itself.
It is just a matter of balancing it properly, so that they don't overlap.

Starting point:
```
sv_crouchslide_accelerate 80;  
sv_crouchfriction 0.7;  
sv_crouchslide_threshold 700;  
```
