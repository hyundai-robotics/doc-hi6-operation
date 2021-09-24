# 7.3.2.7 Output Signal Setting Information

#### Remote mode

With the mode switch of the teach pendant selected to remote \(![](../../../.gitbook/assets/sb-remote.png)\), the signal set in the input signal assign section should be inputted in the state of on in order to activate the remote state. This function is used to output the state to the outside. 



#### Manual \(Teach\) mode

This function is used to output the state to the outside that the operation mode of the controller is manual.



#### Auto \(Playback\) mode

This function is used to output the state to the outside that the operation mode of the controller is automatic.



#### Motor on 

When power is supplied to each motor by the input of the motor on signal and the driving is ready, this function is used to output the state to the outside.



#### Robot ready OK

When the current controller status satisfies all conditions set in the \[Set Up&gt; 2: Control Parameter&gt; 4: Robot Ready Condition\] menu, this function is used to output the state to the outside. 



#### Robot starting

When the robot is started by the step forward/backward operation in manual mode or by the input of the start signal in automatic mode, this function is used to output this state to the outside.



#### Robot moving

When the robot is moving, this function is used to output this state to the outside.



#### Robot stop \(Hold\)

When the robot is stopped, contrary to the output of the start signal, this function is used to output this state to the outside.



#### Emergency stop

When there is an input signal from the emergency stop button mounted on the front of the teach pendant or of the controller is inputted, this function is used to output the state to the outside.



#### Emergency stop \(External\)

This function is used to output to the outside the signal from an external emergency stop device connected to the system board. 



#### Low speed mode 

When the signal set for the low speed command in the input signal assign section is turned on or when the robot operates at a safe speed in manual mode, this function is used to output this state to the outside.



#### Program end 

When the end cycle is performed in the job program, this function is used to output this state to the outside.



#### Overall error

Errors occurring in the controller are divided into the errors caused by system errors and the errors caused by the user’s mistakes in operation. When an error occurs because of a system error, this function is used to output this state to the outside. The errors caused by system errors range from 1 to 999 and 2000 to 7999.



#### Operation error

Errors occurring in the controller are divided into the errors caused by system errors and the errors caused by the user’s mistakes in operation. When an error occurs because of the user’s mistakes in operation, this function is used to output this state to the outside. For information, the errors caused by system errors range from 1 to 999 and 2000 to 7999.



#### Warning

When a warning occurs in the controller, this function is used to output this state to the outside.



#### Collision sensor 

When the input of the collision sensor signal set in the input signal assign section is turned on and it is confirmed that a collision has occurred in the robot, this function is used to output this state to the outside.



#### Step set warning 

In automatic mode, it can be dangerous if the currently selected position of the cursor is different from the position in which the execution was performed previously. This function is used to output this state to the outside.



#### Interlock abnormal warning

When the waiting time in the wait statement of the job program exceeds the time set in the \[Interlock Abnormal Time\] option in the \[System&gt; 2: Control Parameter&gt; 1: Control Environment Setting\] menu, this function is used to output this state to the outside.

Error/Warning output bit, Error/Warning output selection and Error/Warning output strobe

For the error/warning output bit, error/warning output strobe, overall abnormality, operation error, and warning occurrence signals, refer to the following sequence.

![Figure 53 16Bit Output](../../../.gitbook/assets/image%20%28445%29.png)

#### External reset ack

When the external reset signal set in the input signal assign section is turned on, this function is used to output this state to the outside. This signal will be turned on for 200 ms and then turned off automatically.



#### Program echo bit 

When a program is selected by the program selection bit set in the input signal assign section, this function is used to output the selected program number to the outside. 



#### Program ack 

When the robot is started by an input of the external startup signal in remote mode, this function is used to output the state to the outside. The signal will be turned on for 200 ms and then turned off automatically.



#### Arc welding abnormal

When an error related to arc welding occurs, this function is used to output this status to the outside.



#### Arc deposition warning

When welding deposition occurs during arc welding, this function is used to output this state to the outside. This signal will be turned on for 200ms and then turned off automatically.



#### Robot lock state \(Valid=ON\)

This function is used to output to the outside the robot lock setting status in \[Condition Setting\].



#### Field bus abnormal, and field bus idle

When a fieldbus communication board such as CC-LINK and DeviceNet is used, this function is used to output the communication state to the outside.



#### Battery \(backup, encoder\) voltage drop

When there is a voltage drop in the backup battery to maintain the state of the SRAM installed on the main board or a voltage drop in the encoder battery to maintain the value of the encoder installed on each motor, this function is used to output to the outside.



#### Torque monitoring

This function is used to output to the outside the torque value that is applied to the six axes of the robot. The torque value that will be outputted to the outside is a % value in the multiplier of 1/2.



#### Grease injection alarm

This function is used to output to the outside the condition that requires grease injection.



#### Average load factor abnormality alarm 

This function is used to output to the outside the status regarding whether the robot has exceeded the average load factor during operation.





