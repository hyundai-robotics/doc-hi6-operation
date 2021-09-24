# 7.3.2.3 Input/Output Signal Setting Information

* \[Signal\]: The signal to apply the attribute to. The fb block signal can be designated by inputting the block number, decimal point, and signal number in sequence.

  For example, if you want to designate the signal 35 of the block fb1, you can set it by inputting 1.35.

* 
  \[Negative Logic\]: The positive logic and negative logic of the general input/output signal are as follows.

![](../../../.gitbook/assets/image%20%28447%29.png)

* \[Pulse Count\]: Pulse count. This is the count of pulses. If it is set to a value between 1 and 100, pulse output will occur, and if set to 0, a delayed output will occur.
* 
  \[Pulse On\]/\[Pulse Off\]: This is the On status time and Off status time of the output signal when pulse output or delayed output occurs.

  The example of the pulse output according to the pulse attribute value is as follows.

* 
  Pulse output: Count: 3. On status time: 1 second. Off status time: 0.2 seconds

![](../../../.gitbook/assets/image%20%28456%29.png)



* Delayed output: Count: 0. On status time: 1 second. Off status time: 0.5 seconds

![](../../../.gitbook/assets/image%20%28454%29.png)

* \[Name\]: Name of the general input/output signal



