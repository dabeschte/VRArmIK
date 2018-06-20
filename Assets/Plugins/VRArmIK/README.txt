VRArmIK animates your arms and shoulders in VR games.

HOW TO USE
1. Take a look at the demo scene and how it is setup
OR
2. Add the PoseManager-Prefab to your scene
3. Add the Avatar-Prefab to your scene with same position and rotation as the Main Camera (not as child!)
4. Press play and watch your arms move

HOW TO MODIFY
* If the shoulder is not at the correct position
    - You can change the parameters of the ShoulderPoser on the Shoulder GameObject of the Avatar (different offsets)
* If the elbow is not working correctly
    - Make sure that you scale the arms to be of the same lengths of your own
    - Change the ElbowSettings in the VRArmIK Monobehaviour of the arm Prefabs to optimize the elbow rotation  
        + Only do this if you know which pose the players will have while playing (e.g. in archery or a shooter, but not in yoga)
* Change the mesh of the arm
    - Either replace the meshes directly
    - If you have a full skeleton, you can take the joints from the sekeleton and place them as a child of the Shoulder GameObject
        + Add the new joints to the ArmTransform script of the Arm

For bugs, feature requests or if you want to contribute, please visit https://github.com/dabeschte/VRArmIK