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
1. If the code does not compile, make sure that the Scripting Runtime is set to .NET 4.6 instead of 3.5. [Unity Manual](https://docs.unity3d.com/Manual/ScriptingRuntimeUpgrade.html)
2. If the shoulders are always (or never) facing downwards, try using Unity's "Camera OFfset" with tracking mode set to "Floor" and camera Y offset set to 0. If you do so, you also need to follow the next step:
3. If the avatar is a couple of meters below your head, try setting the "Vr System Offset Height" in the PoseManager to 0.

If you have any other questions, please open an issue in the [issue tracker](https://github.com/dabeschte/VRArmIK/issues).
