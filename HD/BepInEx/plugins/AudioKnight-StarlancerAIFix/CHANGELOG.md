- 2.0.0
  - Added SandwormResetPatch and SpringManAnimPatch
    - Previous behavior: After attacking, sandworm would appear just below the surface and break its AI.
	- New behavior: Interior sandworms now relocate to a random inside node after they attack, thus preserving their AI.
  - Added SpringManAnimPatch
    - Previous behavior: Upon losing all targets (such as its target player entering the ship and there being no other targets available to it), a springman would begin sliding around without animating a walk cycle.
	- New behavior: Upon losing all targets, a springman will now correctly resume its walking animation.

- 1.2.0
  - Added JesterAIPatch, which fixes the jester enemy being unable to attack while outside.
    - Previous behavior: Jester would wind up, pop out, then immediately return to box.
    - New behavior: Jester winds up, pops out, then massacres anyone unfortunate enough to be outside.

- 1.1.1
  - Actually put the updated plugin in this time hahahahaaaaaaaaaa

- 1.1.0
  - Performance and accuracy optimization. (Big thanks to **RoboticPrism** and **IAmBatby** for helping to optimize the code! :3 )
    - Removed the "magic numbers" the initial release relied upon.

- 1.0.0  
  - Initial Release.