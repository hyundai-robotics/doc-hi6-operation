# 7.7.4 Base Axis Calibration

Base axis calibration is a function to calibrate the installation direction of the axis.

It is almost impossible to install the base axis to exactly match one direction \(X, Y, or Z\) of the robot coordinate system. When you calculate the direction of the base axis in the controller using the base axis calibration function, you can improve the performance of the linear interpolation trajectory of the system including the base axis.

After the robot is installed on the base axis, this function makes it possible to perform position interpolation by finding the direction vector of any base axis on which the robot is installed.



![&#xADF8;&#xB9BC; 73 &#xBCA0;&#xC774;&#xC2A4; &#xCD95; &#xCE98;&#xB9AC;&#xBE0C;&#xB808;&#xC774;&#xC158;](../../../.gitbook/assets/image%20%28246%29.png)

일반적으로 베이스 축은 로봇을 작업 위치로 이동하는데 사용합니다. 특수한 경우, 로봇이 베이스 축으로 이동하면서 직선 궤적이 보장되어야 하는 경우에도 베이스 축을 사용할 수 있습니다.

* 2 대의 베이스 축 캘리브레이션 로봇이 작업물을 반송하는 경우\(멀티 로봇 향후 지원\)
* 베이스 축을 동작하며 보간 동작을 해야 하는 경우



