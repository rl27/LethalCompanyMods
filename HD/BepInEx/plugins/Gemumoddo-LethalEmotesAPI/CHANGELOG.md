- Version 1.5.1: Updated some internal methods to be much more optimized. Should give a bit of a performance boost

- Version 1.5.0: Updated to use more accurate avatar for animations, consider using [the new ChadRig](https://github.com/Wet-Boys/LethalEmotesAPI/tree/main/ChadRigFolder) if you are animating your own emotes and you want more precision.

- Version 1.4.3: Enemy emote skeletons now get added a frame later to allow other mods to go first. Added BoneMapper.AttachItemHolderToTransform to allow easy locking of the held item position. Added a new import setting to prevent all movement during an emote.

- Version 1.4.2: Fixed a bug in realtion to advanced company not enjoying my emote bones existing. Made the deprecated importer sidestep duplicate emotes instead of straight up breaking when a duplicate is found

- Verison 1.4.1: Added emote skeleton for Peepers, added an option for the new import method to allow non-animating emotes

- Version 1.4.0: Added an emote skeleton for a few custom monsters

- Version 1.3.4: Fixed a weird 3-way bug with AdvancedCompany and More_Emotes when pulling out the portable terminal

- Version 1.3.3: Fixed local arms not being local enough when localTransforms is enabled on emotes.

- Version 1.3.2: Fixed syncing on emotes imported with the new system not working. Fixed oversight on MoreCompany cosmetic patches. Fixed when emotes get changed being a frame late

- Version 1.3.1: Removed debug commands, oops

- Version 1.3.0: Added new way to import emotes which allows more than one mod to have the same emote. This should address the issue where there are like 20 different emotes that are duplicated across multiple mods.

- Version 1.2.16: Fixed issue where we were breaking the bodycam mod

- Version 1.2.15: Upped LethalEmotesAPI priority in GameNetworkManager's Start but added a try catch block to attempt to sidestep some conflicts 

- Version 1.2.14: Fixed issue where I was destroying cosmetics when other mods still need them

- Version 1.2.13: Changed the third person camera to truly use the spectator camera's culling mask. This means it will only be able to see what you can see while spectating players (but it does mean if the spectator camera get's messed up, well... but this is better than the previous solution). Fixed issue when combing emotes from emotes api and toomanyemotes at the same time. The only conflict was when both played at the same time, so now emotes properly end when the other gets played to prevent this.

- Version 1.2.12: I suck

- Version 1.2.11: emergency fix oooooooooooooooooooooooooooooooooops

- Version 1.2.10: Hardened code on spawning to prevent conflicts with weird mod configurations

- Version 1.2.9: Fixed issue where I was locking the camera when I wasn't supposed to

- Verison 1.2.8: Fixed coil heads eating their own ass

- Version 1.2.7: Quick fix preventing spaghettification if your first emote has bones ignored from it's animation (literally no use case right now but just future proofing it)

- Version 1.2.6: Fixed audio sync issues, hopefully people will no longer be suffering randomly. Added useLocalTransforms to AnimationClipParams, this is primarily for if you are trying to do something like an upper body only animation where you  ignore the legs/pelvis

- Version 1.2.5: Fixed head not having proper mapping for emotes.

- Version 1.2.4: Fixed the first time any first person emote played, it would be camera locked.

- Version 1.2.3: Fixed being able to emoting during AC's terminal, fixed emote text not always showing up top

- Verison 1.2.2: Fixed a critical incompatibility issue I caused. Fixed first person arms not working when animating

- Version 1.2.1: Fixed the HealthbarAnimator from not spawning in the correct spot

- Version 1.2.0: Exposed the healthbar animator you can create and remove requests with HealthbarAnimator.StartHealthbarAnimateRequest() and HealthbarAnimator.FinishHealthbarAnimateRequest()

- Version 1.1.16: Fixed cosmetic issues with MoreCompany/AdvancedCompany

- Version 1.1.15: Made the VR mod a soft dependency purely to let it load first since the IL code injections conflict otherwise

- Version 1.1.14: Fixed respawning in latecompany causing emotes to t-pose on the floor

- Version 1.1.13: Fixed VRM t-posing

- Version 1.1.12: Fixed quite a few bugs

- Version 1.1.11: Added enemy skeletons, do with that as you will

- Version 1.1.10: Probably fixed issue with morecompany cosmetics not being removed

- Version 1.1.9: Fixed incompat with fov mod. Fixed morecompany cosmetics not showing up (fixed? added)

- Version 1.1.8: Probably really fixed third person with the mirror mod for real this time.

- Version 1.1.7: Fixed issue with third person breaking when using the mirror mod. Updated integration with LethalConfig

- Version 1.1.6: removed some unncesssary debug logs. Added displayName as an animation parameter, this name will overrite the name that displays in the top left of the screen when emoting.

- Version 1.1.5: Probably fixed issue where you can't emote after being revived by mods that allow that. Fixed overrideMoveSpeed not working at all

- Version 1.1.4: Updated ModelReplacementAPI dll reference so it don't break. Exposed each bonemapper's audiosource in code if you should ever need it. Fixed networkobject hash on the networker being bad

- Version 1.1.3: Fixed an issue with the third person camera's culling mask sometimes showing purple hitboxes. Fixed items not sticking to your hands when emoting

- Version 1.1.2: Fixed an error with third person settings causing camera locking when using the hotswap button.

- Version 1.1.1: Added LethalConfig as a dependency cause it just makes sense

- Version 1.1.0: Added third person camera options, emotes can decide on their default, but you can override this in the emote customization menu, if LCThirdperson is installed, emotesapi will NEVER enter third person camera to avoid conflicts. Change the lock settings when joining other emotes, if you are an emote creator and have emotes that lock players to other players, please consider assigning BoneMapper.currentlyLockedBoneMapper when locking players (if you notice and don't like it, you can revert it in the config). Fixed healthbar not resetting its color on death. Probably fixed hitting escape in the wheel customization menu pulling up the pause menu.

- Version 1.0.4: Fixed a critical error where we didn't patch the networking calls into the DLL, optimized BoneMapper position syncing a bit

- Version 1.0.3: Fixed the need to disable the base animator when emoting, this means we touch the base stuff even less so there should be truly no compat issues with other emote mods. Fixed a bit of teleporting when you use more than one root motion emotes at once.

- Version 1.0.2: Actually did the position lock fix, oops.

- Version 1.0.1: Fixed some issues with setting samples for audio syncing. Fixed an issue with teleports interacting weird with position locks. Made the emote preview in settings a bit less jank.

- Version 1.0.0: Initial Release
