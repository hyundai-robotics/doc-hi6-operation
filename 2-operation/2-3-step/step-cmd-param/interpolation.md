# 2.3.1.1 Interpolation

Interpolation refers to the interpolated path between steps, and the interpolation method for the \[Step N\] determines the form of the path between \[Step N-1\] and \[Step N\].

* P-PTP \(Point-to-Point\) It is the fastest of the general interpolation modes as it interpolates the path between two steps based on individual axes, not the tooltip. Considering the characteristics of industrial robots that consist of rotation joints, the path of the tooltip is usually shaped in a C form.





![Figure 14 Example of the Tooltip Path in P-PTP Interpolation](../../../.gitbook/assets/image%20%2873%29.png)

* L-Linear interpolation It moves in a linear line between two steps in Cartesian space. It is used for a case in which a linear path is needed, such as an arc welding section. The movement will take place while the wrist posture changes automatically as follows.

![Figure 15 Example of L-Linear Interpolation](../../../.gitbook/assets/image%20%2848%29.png)

During the linear interpolation, under certain conditions, the robot cannot automatically change the wrist posture, and such a condition is called the singular posture.



{% hint style="info" %}
Singular postures in which the posture interpolation cannot be performed are as follows.

* If the B-axis is near the dead zone: For details on the dead zone setting, refer to “7.4.5 B-axis No-Use Area.”
* When the sign of the B-axis changes: When the sign of the B-axis angle switches \( - → + \) or \( + → - \)
* When the angle variation of the R2 and R1 axes exceeds 180 degrees
* When the center of the B-axis \(axis 5\) or the tooltip passes the center of rotation of the S-axis \(axis 1\): There may be an error in the trajectory as well as in the posture.
* When the angle variation of the S-axis exceeds 180 degrees
{% endhint %}

* C-Circular interpolation

  It moves in a circular path created between two steps. There should be three points to determine the circle, and the references for selecting them are as follows.



  * At the time of moving from \[Step n\] to \[Step n+1\], if the interpolation method of \[Step n+1\] is C-circular interpolation, it is required to refer to the next step \[Step n+2\].

  * If the interpolation method of \[Step n+2\] is C-circular interpolation, it is required to determine the circle based on \[Step n\], \[Step n+1\], and \[Step n+2\], and among them, movement should take place along the arc of the section of \[Step n\] - \[Step n+1\].

  * If the interpolation method of \[Step n+2\] is not a circular interpolation, it is required to refer to the previous step \[Step n-1\] and determine the circle based on \[Step n-1\], \[Step n\], and \[Step n+1\], and among them, movement should take place along the arc of the section of \[Step n\] - \[Step n+1\].



![Figure 16 Example 1 of C-Circular Interpolation](../../../.gitbook/assets/image%20%28338%29.png)

If you use the criteria of selecting three points required for determining the circle, you can create a program through the double registration of the same point, even in the case of a continuous arc.

In this way, by determining the interpolation method of the step in consideration of the path to move along and using the same point dual registration function, you can create a program as desired.

![Figure 17 Example 2 of C-Circular Interpolation](../../../.gitbook/assets/image%20%28302%29.png)

* Stationary tool interpolation

  This method will be used when the robot owns the workpiece and perform the work using an externally fixed tool. In this case, the interpolation will be performed based on the workpiece owned by the robot.

  For details on the types of interpolation for stationary tools, refer to “7.3.6.2 Stationary Tool Coordinate System.”





