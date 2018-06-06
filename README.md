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
