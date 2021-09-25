# 7.6.2 Robot Type Selection

1.	Touch the \[5: Initialize &gt; 2: Robot Type Selection\] menu. Or touch the \[Mechanism\] button at the top right of the Hi6 teach pendant screen.

2.	Select a robot in the robot model selection window, and then touch the \[OK\] button.

![](../../.gitbook/assets/image%20%28494%29.png)



* You can scroll through the robot model list to check the model name, or you can input the model name to search.
* If you touch the robot usage button, only the robots belonging to the usage can be checked on the list.
* 
  If you select a new robot model, the machine parameter file \(hi6\_porj.json\) will be restored to the initial setting values, and various history files will also be initialized.

* 
  If you select a system that includes additional axes such as a travel axis or a servo gun, you should set the number of additional axes. If a system consists of only robot axes without additional axes, input 0. 



![](../../.gitbook/assets/image%20%28495%29.png)

{% hint style="warning" %}
* The manipulator and controller are shipped as one system. For this reason, the robot controller is equipped with a drive suitable for the drive capacity of the robot that is part of the system.
* When resetting the system by initializing it, you must check the model of the robot that was set to the initial setting values when shipped from the factory, and then set the correct model.


{% endhint %}

3.	After touching the \[Favorites\] button at the bottom right of the Hi6 teach pendant screen, input 314 in the input area of the favorites window, and then touch the \[OK\] button.

![](../../.gitbook/assets/image%20%28492%29.png)

{% hint style="warning" %}
* In Engineer Mode, the Engineer Mode icon \(![](../../.gitbook/assets/eng-mode%20%281%29.png)\) will blink on the status bar.
* Use caution as a serious problem may occur in the robot system if the setting is performed incorrectly.
{% endhint %}

4.	Touch the \[Set Up\] button &gt; \[3: Robot Parameter &gt; 4: Encoder Offset\] menu.

![](../../.gitbook/assets/image%20%28498%29.png)

5.	Perform encoder offset calibration. To turn on the motor, you should set the encoder offset temporarily even if the robot position is not the reference position.

![](../../.gitbook/assets/image%20%28489%29.png)

{% hint style="info" %}
* You should perform an encoder offset setting normally after moving the robot to the reference position.
* For the initial setting, you should perform the encoder offset setting even if the robot position is not the reference position. Otherwise, the motor will not be turned on, making it impossible to drive the robot.


{% endhint %}

6.	Turn off and on the power of the controller and then supply power to the motor.

7.	In manual mode, move the robot safely to the reference position at low speed and then perform the encoder offset calibration again by referring to steps 7–8.

* In the encoder offset setting item, the current encoder position will be set to 0X400000 \(hexadecimal\).
* When a motor is replaced because of failure, if the encoder offset setting is performed at the same location, the recorded program can be used identically.

8.	Press the &lt;Program&gt; key on the teach pendant, and select the program 9999 and then record one step. You can move the robot to the reference position easily. 

{% hint style="warning" %}
* To initialize the system, contact the customer support team and ask an expert.
* 
  For initialization of a collaborative root, refer to the collaborative robot safety functions manual.

* 
  When the system is initialized, all data and programs, including control parameter files and machine parameter files, will be deleted. If you back up your data before initializing the system, it can be restored and used when necessary.
{% endhint %}



