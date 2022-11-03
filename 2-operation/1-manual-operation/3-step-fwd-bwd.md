﻿# 2.1.3 Step Forward/Backward

The step forward/backward is one of the methods of operating the robot in manual mode and refers to the act of playing back a recorded program. By manipulating the robot in the step forward/backward operation, you can check the recorded program path and mutual interlock relationship at a range of safe speed.

The execution unit for the step forward/backward operation can be checked and set from the \[run to\] button on the left side of the Hi6 teach pendant screen.

![](../../_assets/tp630/lbt-runto_eng.png)  

To set the execution unit for the step forward/backward operation, touch the \[run to\] button repeatedly until the desired option appears.

![](../../_assets/tp630/lbt-runto-sw_eng.png)

* **\[cmd\]:** Will execute the command line by line
* **\[Step\]:** Will execute step by step
* **\[End\]:** Will execute up to the end statement
****

<Br>

When the execution unit is set as 'Cmd' or 'Step', the robot will ignore the set accuracy area and reach the recorded step. If it is set as end, the robot will operate on the same path as the one for playing b/n automatic mode.

When you set the execution unit as 'Cmd' or 'Step' and perform the step forward/backward operation, the robot will operate on a path without cornering. For details on cornering, refer to "[2.3.1.4 Accuracy](../3-step/1-step-cmd-param/4-accuracy.md)".

![Figure 11 Playback Forward/Backward Path When cmd/step Setting is Performed](../../_assets/path-cmd-step-pback-fwd-bwd-en.png)

If you set the execution unit as end and then perform the step forward/backward operation, the path of the robot will change according to the stop position. In other words, if the robot stops at a place other than at cornering and then executes the forward operation, the robot will recover the original cornering path, but if the robot executes the backward operation, the robot will move to the recorded step, and at this time, the robot will stop at the recorded step and then move immediately to the previous step. When the robot stops at cornering, the robot will maintain its previous cornering path both when moving forward and when moving backward.

![Figure 12 Playback Forward/Backward Path When End Setting is Performed](../../_assets/path-end-pback-fwd-bwd-en.png)

When the robot stops at cornering and then executes the forward operation, the robot will operate on the original cornering path. Here, if the robot executes the backward operation and then, without reaching the previous step completely, executes the forward operation again, the robot may not be able to create the original cornering path in some cases. In other words, if the distance of the step becomes shorter than the original distance, making it impossible to meet the existing accuracy condition, a smaller cornering path than the original one will be created.

![Figure 13 Example of the Robot Path Change During Step Forward/Backward Operation](../../_assets/path-step-bwd-then-fwd-en.png)


You can set the maximum speed for the step forward/backward operation and set whether to execute functions as well. After touching the \[run to\] button on the left side of the Hi6 teach pendant screen, set the speed value and function execution option in the setting window.



![](../../_assets/tp630/cond-set-step-fwd-bwd-spd_eng.png)

* \[2: Step FWD/BWD maximum speed\]: Same as the value set for the speed in manual operation
* \[3: Function execution during step FWD\]: You can select the function execution option.
  * Off: The function will not be executed for the step forward/backward operation. Regardless of the conditions of the external I/O, you can check only the robot path. Be careful as the interlock with the external system will not work.
  * On: You can execute all functions. Should be used after the external interlock is completed.
  * I On: You can execute only the input wait function. It should be used when it is necessary to check the safety through the external interlock.





