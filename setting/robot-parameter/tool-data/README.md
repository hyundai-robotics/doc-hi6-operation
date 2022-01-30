# 7.4.1    Tool Data

You can set the distance and angle of the TCP based on the robot’s R1-axis flange and register the tool’s weight, center of gravity, and inertia. You can perform registration manually using the \[1: Tool data\] menu.

In another way, the tool length can be set using the automatic calibration function, and the tool’s weight, center of gravity, and inertia can be registered using the load estimation function.

In the case of interpolation operation such as linear or circular interpolation, the trajectory will be created based on the TCP, so the length and angle of the tool should be accurately set before the teaching.

The Hi6 controller performs control based on the dynamics of the robot. The robot can operate quickly and safely only when the weight, center, and inertia of the tool are correctly set. If the weight, center, and inertia values of the tool are incorrect or wrong, serious problems may occur in the performance and service life of the robot.

In particular, in the case of using the tool change function, all tool information related to tool change, not only the information about each tool, but also separate numbers assigned to disconnected tools, should be inputted for the use. Moreover, even during the handling operation, the attachment/detachment status of the workpiece should be assigned to each tool number for the use.

The length of the tool is the length in each direction in the flange coordinate system. \(Length in X-axis direction: Xt / Length in Y-axis direction: Yt / Length in Z-axis direction: Zt\)



![Figure 60 Flange Coordinate System for Each Robot Type](../../../.gitbook/assets/image%20%28213%29%20%282%29%20%282%29.png)

The angle of the tool is the posture conversion amount in each direction in the flange coordinate system. \(Angle in X-axis direction: Rx / Angle in Y-axis direction: Ry / Angle in Z-axis direction: Rz\)

![Figure 61 Tool Angle: Rotating Rx \(Left\) / Rotating Ry \(Middle\) / Rotating Rz \(Right\)](../../../.gitbook/assets/image%20%28211%29.png)

The length and angle of the tool will be set based on the flange coordinate system. The tool length can be set as the distance from the center of the flange coordinate system to the TCP.

The tool posture is a value acquired by performing rotation sequentially in the X, Y, and Z directions based on the tool flange coordinate system according to the tool angle set as above.

Rxyz = Rot\(z, Rz\)Rot\(y, Ry\)Rot\(x, Rx\)

* Rxyz: Tool posture rotation matrix based on the tool flange
* Rot\(z, Rz\): Rotation matrix that rotation occurs as much as Rz in the Z-axis direction of the flange coordinate system 
* Rot\(y, Ry\): Rotation matrix that rotation occurs as much as Ry in the Y-axis direction of the flange coordinate system
* Rot\(x, Rx\): Rotation matrix that rotation occurs as much as Rx in the X-axis direction of the flange coordinate system





