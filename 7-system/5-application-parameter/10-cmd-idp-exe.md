# 7.5.10 Command independent execution

This is a function that executes the corresponding statement separately from the work program when the set input signal turns from OFF to ON. <br>
The statement is executed using an unused subtask, and usually subtask 1 is used. <br>
For more information about multitasking, please refer to "[${cont_model} Controller Function Manual - Multitasking](https://hrbook-hrc.web.app/#/view/doc-multi-task/en/README)".


![](../../_assets/tp630/cmd-idp-exe.png)

  * Input signal: Set the signal input to the controller.
  * Command: 
    * Records statements to be executed when the input signal changes from OFF to ON. 
    * Generally, task start is used for gun search and tip dressing work of the stationary servo gun, and move is used for independent operation of the positioner. 
    * When using task start, subtask 1 is used to execute this command, so specify sub as 2 or more or set it to 0. (0=Auto assign)
  * Output signal under execution: 
    * It turns ON when execution of the statement begins and turns OFF when execution is complete. 
    * If the statement is not a move, it is meaningless because the execution time is very short.
  * Output signal after execution completed: 
    * It becomes OFF when execution of the corresponding statement begins and ON when execution is complete. 
    * If the statement is not a move, it is meaningless because the execution time is very short.

{% hint style="info" %}
* Execution is possible only with the motor ON in auto mode.
* When executing a move statement, the axis must be separated by a mechanism so that it is not used in the main task, or the axis control status must be disabled with axisctrl off.
{% endhint %}
