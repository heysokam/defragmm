# Thoughts on Crouchsliding  
_Why this mechanic turned the original Quake 4 into a cpm-style fast paced game,_   
_and how that fits into mmod_race physics_  

_This article became a bit longer than expected. Go to [Part2](https://github.com/heysokam/defragmm/blob/main/Text%20Files/Crouchsliding%20Thoughts%202.md) to read just the conclusion._
## Overview
Quake was originally made for multiplayer pvp.  
But the movement code/mechanics have sticked with us throughout the years.

Quake3 movement was "slow".  
It wasn't "pro" and skillful enough. And they removed all of the charm that QuakeWorld/Quake2 had with their ramp mechanics and AD turning.  

Or at least that's what some Quake fans thought back in the day.  
So they figured they could improve vq3 by adding back those mechanics, that were really good about previous Quake games, but that the developers were not implementing into their new games themselves.  
*(rampjumps, AD-turning, faster overall pace, etc)*  

That is, in my opinion, how the classic CPMA movement ruleset came into existence.  
Literally, a Frankenstein of previous mechanics that WORKED and were really FUN, but were forgotten by the original Quake devs.  
Marked as "unintended bugs" instead of "fun features".  
But properly tweaked and balanced together to make the fun to play movement style that now everybody knows.   
Making the end result not at all a Frankenstein, but a unique and distinct fun to play movement game.

This argument can be proven very simply by analyzing Quake Champions, and what the Quake devs are now doing with their movement, having learned from their previous mistakes:  
- Visor = Classic VQ3
- Anarky, Sorlag = CPMA
- Slash = Quake 4
- Nyx = warsow/titanfall wallkicks, +doublejumps midair

Thinking about it this way, there is NO DOUBT as to why Rapha is such a GOD with Visor.  
Or how Toxjq can be so impossible to stop with Slash.  
How could they not be!  

They are, quite literally, champions made for their unique strategies, movement and playstyle.  
These guys were top-tier gods when those games were at their peak back in the day, and they are still top-tier gods now with the same movement rulesets in QC.   

_I would argue that Vo0 or Rat would be just as good with Anarky/Sorlag if they weren't so strongly limited by the hardcoded speed cap, but that's a topic for another day._

## Improvement potential
Quake4 implemented crouchsliding to make duels faster (aka more pro/skilful) than Q3, but not impossibly fast like CPMA was proven to be.  

MMod doesn't have those duel requirements, so there is room for modification and improvement, since the game is fully oriented towards movement and that's all we need to worry about.

You could have three different types of cornering, with different drawbacks/benefits, and that would make the game more complex/interesting than only having one.  
That's irrelevant for a duel setting (or even redundant, since one of them can be proven superior in combat and outrule them all), but could be an essential thing for a movement oriented game like mmod.  

If we assume that "more unique/distinct movement options" equal "better movement game", then I think the addition of a well balanced crouchsliding mechanic can be highly beneficial to a CPM-influenced ruleset.

## Movement comparison: VanillaQ3 vs CPMA vs Quake4
Watch these duels, and keep these questions in mind:
- **How does Quake4 compare to Quake3?**   
   _(Acceleration mechanic, optimal gamestyle, positional play vs rushing)_
- **How does CPMA compare to VanillaQ3?**  
  _(slowing down for corners = slower game = positional play is more rewarded._  
   _not stopping at all = impossibly fast pace)_
- **What does CPMA have in common with Quake4?**  
  _(pay attention to stairjumps, rampjumps, cornering/turning, overall speed/pace of the game)_  

vq3: https://www.youtube.com/watch?v=tU6v8C1pw8Y  
cpm: https://www.youtube.com/watch?v=7dMGrop2zeQ  
q4: https://www.youtube.com/watch?v=KHCNWdKtUEc

Let's focus on their essential movement, which is what's important for us.  
VanillaQ3 is the slowest of the three, clearly. Everybody knows that.   
But... why? Think about it.

Ask yourself these questions:
- What makes you faster?
- What slows you down?  
- Who wins in a 100m running sprint race?
- Who wins in a Car Racing competition?
- And, more importantly: Who loses in those?

The simplest answer to all of them is in one word: -Acceleration-  
- No acceleration = No movement
- Negative acceleration (deceleration) = Slower overall speed/time
- Higher acceleration = Faster time  

What specifically affects that acceleration is what I'm trying to get to.  
_(We could talk about how the Q3 formulas for acceleration work, but I think that's a bit overkill for this. It can be explained with simpler words. Still, if you are into the mathy side of games, this is a decent enough explanation: https://www.youtube.com/watch?v=rTsXO6Zicls)_

### Essential movement factors
In essence, every movement competition (even real life physics) is based around two elements:
1. Cornering  (aka, shorter distance & how to decelerate less than others)
2. Speed (and with it, acceleration, because more accel = more speed)  

As you can see, both are actually related to acceleration.  
_(either positive or negative, respectively)_

So, how does each game handle these two factors?  
Considering that the optimal acceleration mechanic is more or less equal in all of them (diagonal strafing with A/D+W), lets look at how their unique cornering mechanics are similar/different to each other:
- VQ3:   
  Does not allow for vector redirection. Requires strategic bumping into things to navigate.
  - Only diagonal acceleration.  
  - Strongly limited turn-rate.  
  - Requires stopping down to walkspeed and then circlejumping...  
  - or bumping into walls or diagonal/rounded corners to redirect the speed vector to a better/shorter line.
- CPM:  
  Allows the player to redirect their current speed into a different direction, under very specific conditions:  
  - limited corner radius, dependent on Speed
  - limited acceleration
  - AD & W are well balanced against each other and distinct/unique
- Q4:  
  Allows the player to redirect their current speed into a different direction, under very specific conditions  
  - requires crouching
  - constant deceleration by friction (speed cost)
  - limited corner radius (same tool that AD uses to balance its power in cpm)

As you can see, both CPM and Q4, in essence, achieve the exact same thing (higher turn rate + vector redirection).  
BUT, what makes them similar is their **cornering style**, and not their acceleration style. That's why I would associate Q4 crouchsliding with AD turning, and not with VQ3. Even if Q4 had the same straight line acceleration style than VQ3.

Neither CPM nor Q4 give the player an infinite turn-rate, though.  
They have rules for when a higher turnrate can be achieved and how.  
Those situations are difficult to master and mechanically challenging in both games (AD-turning and W-turning for CPM, and Crouchsliding for Q4). And, in my opinion, this is what makes them interesting in their own unique ways.  

Although, if you think about it... they achieve the exact same outcome. Just in different ways.  
So, you could argue that they are not distinct, and one of them should be rejected.  
But this is where I saw something different, and asked for crouchsliding to be implemented.  
This is the reason why this text exists.  
Continue to [Part2](https://github.com/heysokam/defragmm/blob/main/Text%20Files/Crouchsliding%20Thoughts%202.md)
