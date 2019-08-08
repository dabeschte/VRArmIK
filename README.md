# VRArmIK
VRArmIK brings arms into VR without any additional tracking devices. 
Using head and hand positions, the shoulders and arms are estimated to create realistic arm movements.

[See the Video on Youtube](https://youtu.be/dHgH6Xsi3JQ)

# Features
* VR Tracking to Wrist and Neck estimations (currently only optimized for Oculus Touch)
* Estimates shoulder position and orientation 
  * 360° movement
  * crouching 
  * distinct shoulder rotations when stretching the arms to their limits
  * arm dislocation when the distance between shoulders and controllers is larger than the virtual arm
* Simple Arm IK Solver which connects shoulders with hand target positions
* Complex Elbow Angle calculations
  * many variable to optimize the IK for different use cases
  * prevents unrealistic hand rotations

# How To Use
1. Download package from [Unity Asset Store](http://u3d.as/1d07)
2. Add PoseManager and Avatar Prefab into your scene
3. Run

Take a look at the Demo scene to see a working demo.


# Tips & Tricks
* If the code does not compile, make sure that the Scripting Runtime is set to .NET 4.6 instead of 3.5. [Unity Manual](https://docs.unity3d.com/Manual/ScriptingRuntimeUpgrade.html)
* If shoulder is looking downwards: Unity handles different VR Systems differently. In Oculus, the tracking positions of hands and head are always relative to the base position used when calibrating the Oculus headset. In OpenVR/SteamVR, the positions are relative to the ground. <del>You might need to add an (negative) offset position to the "PoseManager" GameObject in order to compensate this. E.g. y=-1.8 should work on most platforms if you are 1.8m tall.</del>
<b>Update</b>: You need to set playerHeightHmd to -1.8f in the PoseManager. (thanks to 12DrewMileham13)
<b>Update 2</b>: I potentially fixed this issue in the branch "platform-fixes". Since I do not have the hardware to verify this, please send me a E-Mail if this branch solved your issues so I can merge it with the master-branch!

If you have any other questions, please open an issue in the [issue tracker](https://github.com/dabeschte/VRArmIK/issues).
