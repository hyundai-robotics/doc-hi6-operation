# 2.3.1.4 Accuracy

It will determine the accuracy \(the degree of approach to the recorded position\) at which the robot passes through the step when progressing the target step. When the robot moves to the target step, if the error between the current position and the recorded position that occurs when the robot moves to the target step is less than a certain value, the robot will move to the next step. The value of the allowable error at this time is called accuracy.

A path that is newly created within the accuracy range \(0–7\) according to the accuracy is called a cornering path. In general, the higher the accuracy, the faster the cornering speed, which is advantageous in terms of moving time.



![Figure 18 Change of the Path P2 Because of Accuracy](../../../.gitbook/assets/image%20%2853%29.png)

Accuracy 0 has the highest accuracy, and Accuracy 7 has the greatest error. Accuracy will be applied in a way that it cannot be greater than 1/2 of the length of the shorter trajectory of both trajectories of the target step. In other words, you can apply the expression “Accuracy ≤ min \(P1-P2, P2-P3\) / 2” in the example above. In this expression, the TCP distance is used for explanation, but the same concept can be applied to the angle.

In the case of a robot, the value of the applicable accuracy level will be defined based on the tooltip distance and posture angle of the robot. When it comes to additional axes, the value in the case of the linear axis will be defined based on the length, and the value in the case of the rotation axis will be defined based on the angle. You can directly change the values in the \[Set up&gt; 3: Robot Parameter&gt; 6: Accuracy\] menu. For details on the value of the accuracy level, refer to “[7.4.6 Accuracy](../../../setting/robot-parameter/accuracy.md).”



The figure below shows how the cornering path is created according to the value of the accuracy level. If there is a general 6-axis articulated robot and an additional axis, the value of accuracy level can be set individually for TCP \(tooltip distance\), ORN \(position angle\), and AUX \(additional axis distance\). Because all the values of relevant accuracy levels should be satisfied, the cornering path will be created based on the smallest value among TCP, ORN, and AUX. The cornering path will be created in a constant curve, regardless of the speed variation, while satisfying the convex hull property. However, errors of several millimeters \(mm\) may occur at low speed and high speed because of servo delay.

![Figure 19 Creation of the Cornering Path According to the Value of Accuracy Level](../../../.gitbook/assets/image%20%2879%29.png)

{% hint style="info" %}
The mode of creating the cornering path according to the value of accuracy level will be applied to all types of interpolation in the same manner. In the case of P interpolation, the TCP distance accuracy will be applied, but errors may occur.
{% endhint %}

The cornering path will not exceed the convex polygon area because of the convex hull property, as shown below.

![Figure 20 All Points on the Cornering Path within the Convex Polygon Area](../../../.gitbook/assets/image%20%2887%29.png)

