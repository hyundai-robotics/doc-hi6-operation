# 7.2 User Environment

You can check and set various user conditions. 

1.	Touch the \[1: User Environment\] menu. Then, the user environment setting window will appear.

2.	After setting the user environment, touch the \[OK\] button.

![](../.gitbook/assets/image%20%28441%29.png)

* \[1: Pose Record Type\]: You can set the type of the position recording of the step to be recorded as a hidden pose.
  * 
    \[Base\]/\[Robot\]/\[Axis Angle\]: You can record the position of the step based on the base coordinate, robot, and axis angle values.

  * 
    \[U\]: You can record the position in the user coordinate system.
* 
  \[Confirm Delete  Command\] You can set whether to expose the deletion confirmation window when deleting a statement in manual mode.

* \[3: WAIT\(DI/WI\) release\]: While in the input signal wait or welding complete signal wait status, you can set whether to force the signal wait status to be deactivated using the &lt;shift+F3: Wait Deactivation &gt; keys.
* 
  \[4: Program Strobe Signal Use\]: When selecting an external program by receiving an external digital signal, you can set the time when the external program is to be selected.

  * 
    \[Disable\]: Makes it possible to select an external program by reading only the external program selection signal

  * 
    \[Enable\]: Makes it possible to select an external program by reading the external program selection signal at the time when the program strobe sognal is inputted

* 
  \[5: Ext. Update of Playback Prog.\]: You can set whether to allow the process of externally \(PC\) modifying the program that is being played back, and then to allow the process of downloading it to the controller \(With regard to the number of the program being played back, the downloaded program will be applied from the next cycle\).



{% hint style="warning" %}
If the program being played back is modified externally \(PC\) and downloaded to the controller, it could cause a failure of or abnormality with the product. Contact our customer support team to ask an expert or an engineer.
{% endhint %}

* \[6: Collision Sensor\]: You can set a method of stopping the robot when the collision sensor is operating.
  * 
    \[\(1\) Sensor\]: When the collision sensor is operating, this function will switch the robot into the emergency stop ready off \(motor off\) status or stop the robot \(operation ready on \(motor on\) status\).

  * 
    \[\(2\) Signal Logic\]: You can set the input signal logic of the collision sensor as positive logic or negative logic.



{% hint style="info" %}
* If you enter the \[Set up\] menu while the motor is turned off because of the operation of the collision sensor, the motor ON and jog operations can be performed. This function can be used to move the robot that suffered a collision.
* If the collision sensor operates while \[Sensor\] is set as stop, the robot can perform only jogging.
{% endhint %}

* \[7: cpo\( \) coordinate System\]: You can set the reference of the coordinate system of the pose that is to be acquired when the pose expression \(cpo\(\)\) that makes it possible to acquire the current robot pose in the job program is used.
* 
  \[8:cpo\( \) Selection\]: You can set the type of the current position value that is to be acquired when a pose expression \(cpo\(\)\) that makes it possible to acquire the current position of the robot based on the coordinate system \(U/Base/Joint\) designated in the job program. You can select the command value \(robot’s command value \(cmd\)\) or the current value \(robot’s current value \(cur\)\).

{% hint style="warning" %}
There may be an error between the robot’s current value and the robot’s command value because of servo delay. Set the type of the current position value according to the environment and purpose of the use.
{% endhint %}

* \[9: Manual Oper. for Stop Signal Input\]: You can set whether to enable jog operation when an external stop signal is inputted.

