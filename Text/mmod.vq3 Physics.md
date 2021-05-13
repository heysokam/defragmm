************************************
**** It has been mentioned that the modes solution could be implemented through UI/UX design instead,  
**** with Tag filtering of the leaderboards, without requiring gamemode differentiation.  
**** I'll keep the modes mentions in this file only for reference.  
************************************
Tech Defrag gamemode (tag):  
Definition, Ruleset, Concepts and Reference Examples
************************************

This text explains the idea for a vq3-oriented trickjumps/tech mode, based around the code that Lumia is writing for mmod defrag.  
It has the same root physics of vq3, but with added technical mechanics that give mappers tools to also design around difficulty-of-completion value, and not only time-to-complete in isolation.  
Time-to-complete should be important too, just not the only core goal like in regular strafing/weapons defrag maps.  

Maps like this ruleset allows are already played in games like Defrag, Quake2, Enemy Territory, Reflex, Diabotical (video examples at the end).  
This mode aims to join the best pieces and core elements of those games together into one unique game.  

Custom mmod-defrag physics for the speed mode could be more cpm oriented (i.e. better turning and/or higher speed in general).  
But the vq3-oriented physics in this ruleset could also be used as an alternative to vq3 in the speed mmod-defrag mode.  

************************************
Potential names for the physics (needs revision):  
- Speed mmod-Defrag: Custom mmod-defrag ruleset, CPM oriented (pending definition).  
- Tech mmod-defrag: Custom mmod-defrag ruleset, VQ3 oriented (detailed in this text).  
- Classic df.cpm: Classic 1:1 defrag cpm physics.  
- Classic df.vq3: Classic 1:1 defrag vq3 physics.  
	(the word "vanilla" is already used to refer to vq3)  

************************************

Features:  
- Differential Strafing:  
	-- Based around vq3 vector control, mixed with cpm ad turning  
	-- No w-turning  
	-- Reduced AD turn rate.  
	-- Increased AD acceleration. Inferior to regular strafing, but stronger than cpm accel.  
	(cvar values for testing these are provided at the end)  

- vq3 ground acceleration values (for circlejumping, ?sliding?)  
- cpm sliding power values  

- No snapzones  
	-- Removal of W-turning makes snapzone-acceleration almost impossible to control / optimize.  
	-- Acceleration feels random/unstable without a way to control it.  
	-- Skillful strafing is more related to optimization of differential strafing angles.  

- Autojump:  
	-- Leaving jump pressed makes you -10% slower (maximum -10%, or else it becomes extremely punishing for new players)  
	-- You can still autojump most of the easy/medium maps  
	-- Additive jumps can be autojumped, but you reach -10% less height (?maybe -20%?)  
	-- (Difficulty in this should be left for mappers to design, as to not hinder new players that need to rely on   autojump in their early learning stages, because they are overwhelmed by the overall difficulty of the game)  

- General Triggers:  
	-- Overbounce  
	-- Slide  
	-- Surf (slide for ramps??)  
	-- Teleport  

- CPM specifics:  
	-- Teleport Jumps  
	-- Stairs jumps  
	-- Headbump double jumps  

- Q2+CPM ramps mix:  
	-- Sliding up the ramp if no input.  
	-- Jumping while in a ramp triggers the same loss of speed that cpm does, but gives the extra height from the cpm double jump.  
	-- Double jumping from a ramp has the same 400ms timer as a cpm double jump  
	-- (the goal of these is to join q2 and cpm ramp physics together)  

- Downramps: Regular vq3/q2/cpm behavior. Give horizontal speed boost.  
- Surf ramps: Keep vq3 behavior. If added, it should be with triggers.  

- Reducing player size mid air:  
	-- (allows you to fit through different areas/gaps that otherwise you would not be able to clear)(modified tech from ETjump)  
	-- Crouching:  
		--- Raises your legs, reducing your hitbox size  
		--- Doesn't change the highest level of your hitbox. No difference for ceiling avoidance. (-50% total player height maybe?)  
		--- Allows for higher & longer reach of jumps (how much?)  
	-- Proning:  
		--- Switches your width with your height (maybe by rotation of hitbox 90deg around the pitch axis? maybe different way?)  
		--- Reduces vertical player hitbox size, but increases the horizontal size  
		--- Lowers your hitbox (head), but doesn't change lower hitbox collision point (feet). (aka. doesn't help with higher jump reach)  
		--- For clearing narrow (height) gaps and avoiding hitting the ceiling  

- Ladders  
- Water movement  
	(both from q2)  

- Additive jumps:  
	-- Q2 based. The more vertical speed you have, the higher the next jump is. (each jump adds X v.ups to your v.speed? revise q2 code)  
	-- (includes ladder+water jumps by making each one's vertical speed the base for the additive jump calculation)  

- Stances (names/fantasy should be revised):  
	-- (based around q2 fps manipulation)  
	-- (needs a clear HUD indicator of which one is active)  
	-- Each stance gives you a boost/increase in one type of movement, but reduces the others.  
		--- Balancing:  
			---- +10% / -10% / -5%  
			---- higher numbers = too important / mandatory / punishing  
			---- If higher numbers: Lower skilled players will be too punished/gimped for not being able to manage everything properly  
			---- If lower numbers: Higher skilled players will still be rewarded for their skill by being able to clear the highest difficulty challenges designed by good mappers that can design around the mechanic.  
	-- Types:  
		--- Balanced/Neutral: Suboptimal in everything (lets say -+0% to all), but allows you to not worry about optimization (overwhelming area/zone or just new to the game)  
		--- Sliding stance: Augments sliding power (including both ramps and slide triggers). Reduces Height and Control power  
		--- Height stance: Augments vertical speed acceleration. Reduces Speed and Control power.  
			---- (including additive jumps and cpm-based ramp jumps. shouldn't affect catapult/push triggers)  
		--- Speed stance: Augments/optimizes horizontal acceleration. Reduces Height and Sliding power  
		--- Control stance: (greatly?) Reduced acceleration in all directions (included sliding, additive jumps, etc). Augments air/ground control power.  
			---- Goal of control stance: Fine control, torture-esque maps, avoiding obstacles (improved breaking+handling), tiny platforms.  

- Maps for tech mode:  
	-- Based around technical jumps that require more precision and control than just miliseconds optimization.  
	-- You should still be able/encouraged to fight for a better time. Mix of both.  
	-- Examples:  
		--- https://www.youtube.com/watch?v=dDHPiNrsy5c  
		--- https://www.youtube.com/watch?v=9lOlPq_Ys3U  
		--- https://www.youtube.com/watch?v=zZNuooB_S_8  
		--- https://www.youtube.com/watch?v=q9txEQqDViQ  
		--- Technical strafing, but not 100% trickjumping (tech). Although technical, should be considered speed defrag maps.  
			---- https://www.youtube.com/watch?v=_6syNv5xfxo  
			---- https://www.youtube.com/watch?v=rmOz4U_I17E  


************************************
Gocnak:  
- What should the base mode here have  
- Documentation around the tech  
- Examples  
- A mode is pretty self contained with its identity and features.  

************************************
Cvar values:  
- You can copy&paste everything AFTER the three asterisk rows into a FILENAME.cfg file (I always use phys_sokam.cfg)  
- Place the file inside the momentum cfg folder ("GAMEFOLDER/momentum/cfg" where GAMEFOLDER is the root of your mmod installation folder)  
- Open console, and execute "exec FILENAME", where FILENAME is the name you set (in my case, "exec phys_sokam")  
- The game needs to be launched with the "-mapping" command added to the launching shortcut, or these variables wont work.  
************************************
************************************
************************************

////////  
//// vq3 good parts  
////////  
sv_differentialstrafing 1		// (default 0) enables strafing differently depending on the wishdir angle to the velocity.  
// Strafing with halfbeat is a really nice feeling you can normally only have in vq3.  
// Mixing AD turning with Halfbeat is really unique, and I think it should be the core of mmod physics settings, which cannot be enjoyed in any other game   
//  
sv_cpm_accelmult 1				// (default 1.5) the factor to multiply ground acceleration by in CPM  
// Having the slower start of vq3 is one of the ways the physics could be controlled, which also helps maintaining the vq3 core feel of the game.  
// Another value to be considered for ground accel might be 0.85 or 0.9 (0.75 seems too slow). This would make vq3 circlejump heavy maps ported from defrag much more difficult to clear. Might not be a good thing, just to compensate for differential. But should be reconsidered to balance slide surfaces speed increases in relation to overall acceleration speeds. Slide power might be able to be balanced programatically in other ways (i.e. unique sliding cvars)  

////////  
//// cpm good parts  
////////  
sv_cpm_physics 1					// enables CPMA physics. dj, ramp jump, tele jumps  
//  
// W turning:  
// Makes the game more accessible to new players. But it also dumbs down the skill requirement of some maps.  
// Does not work well with differential, because it removes the need to control your directional vector at all, removing a core vq3 element/mechanic with it.  
sv_differential_aircontrol 0		// (default 1) enables aircontrol when using differential strafing. activated when wishdir is less than the minimum q3 strafe angle.  
//  
// AD turning  
sv_airstrafeaccelerate 3			// (default 6.7) acceleration when strafing with A/D (CPM only)  
sv_maxairstrafespeed 60				// (default 30) max speed when strafing with A/D (CPM only  
// Half the amount of control of CPM, but double the acceleration.  
// Keeps the vq3 gameplay feel from being erased from the game just because of adding AD turning.  
// Higher acceleration helps with not feeling punished for having to AD-turn a lot in turn heavy maps.  
// But the acceleration is still lower than regular/halfbeat straight strafing.  
// So you still need to optimize your directional vector and route to get a better time.  


////////  
//// Common to both  
////////  
//// Snap Zones  
sv_snapvelocity 0				// enables rounding velocity to ints every frame (default 1 from defrag)  
// Maybe yes with snaphud. Needs testing both to compare.  
//  
//// Autojump  
sv_autojump 1					// enables auto-jumping (default defrag 0)  
sv_scalecmd_fix 1				// fixes slowdown on jump input if enabled (default defrag 0)  
//////// Autojump, plus removing slowdown on jump (currently -50%, not configurable, so it is disabled for now)  
////////  
////////  
//////// Other mechanics will be added here when they are implemented.  
