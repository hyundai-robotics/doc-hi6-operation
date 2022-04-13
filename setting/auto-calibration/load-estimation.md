# 7.7.3 Load Estimation Function

Load estimation is a function that automatically calculates the physical properties \(mass, center position, inertia\) of the tool attached to the front end of the robot through a certain operation.

The manipulator information \(mass, center of mass, inertia of each link\) is registered in the controller. However, as a tool will be used after being attached to the front end of the robot when necessary, the tool information should be inputted. The information on the tool physical properties includes tool mass \(kg\), center position, and inertia that are necessary to safely use the robot.

If the CAD data contains the physical properties information of the tool, you can directly input the tool mass, center position, and inertia by touching the \[Set Up\] button &gt; \[3: Robot Parameter &gt; 1: Tool Data\] menu of the job program.

![](../../_assets/image%20%28491%29.png)



The tool data setting information is as follows.

![Figure 70 Tool Data](../../_assets/image%20%28505%29.png)

* \[Weight\]: The total weight \(kg\) of the tool installed at the front end of the robot
* \[Center\]: The distance \(mm\) in the x, y, z directions from the center of the robot flange face to the position of the center of gravity of the tool
* \[Inertia\]: The moment of inertia of the tool with respect to the tool coordinate \(kg/m2\). The moment of inertia will be determined by the mass distribution around the x, y, and z axes based on the center of gravity, and will increase as the load mass is distributed farther from the rotation axis.
* Tool data coordinate system: Inertia and center will be expressed as values with respect to the x-, y-, and z-axis directions.



However, in many cases, it is difficult to determine the physical properties of the tool such as mass, inertia, and center of gravity of the tool from CAD data. At this time, you can check the physical properties of the tool using the load estimation function in the robot controller.

![Figure 71 Load Estimation Function](../../_assets/image%20%28527%29.png)

1.	Touch the \[6: Auto Calibration &gt; 4: Load Estimation Function\] menu.

2.	After touching the \[Add. Weight on Each Axis\] button, input the information of the additional weight of each axis.

If the load estimation function is performed while there is additional weight, it will be determined that all the weight objects mounted onto the robot are at the front end. For accurate load estimation, the information on the additional weight of each axis should be inputted.

3.	After moving the robot to a safe area by moving the main axis of the robot, touch the \[Set pose\] button.

4.	After touching the \[Wrist Axis Operation Area\] button, designate the operation area of the wrist axis to be used in the load estimation operation. Load estimation can be performed in an operation area that there is no interference not only with nearby facilities but also with the manipulator.

If the \[Wrist Axis Operation Area\] button is not supported, skip this step, and perform the next step.

5.	Touch the \[Play check\] button. Then, while the robot is operating at a low speed, you can check for any interference with nearby facilities or the manipulator.

6.	After inputting the number of the tool mounted onto the robot, touch the \[Play Normal\] button. Then, load estimation will be performed, allowing the physical properties of the tool to be calculated.

7.	After checking the load estimation result, touch the \[End\] button. Then, the calculated physical properties of the tool will be registered in the tool number.

{% hint style="info" %}
* Additional weight is the overall weight of all devices that the user attaches to the robot, such as a welding dressing device and welding signal line relay box, except for the tool mounted at the front end of the robot.
* 
  The wrist axis operation area function will not be supported in some robots.

* It requires your attention that the load estimation function may not be executed depending on the setting values of the wrist axis operation area function.
* For details on the load estimation function, refer to the “Load Estimation Function Manual.”
{% endhint %}



