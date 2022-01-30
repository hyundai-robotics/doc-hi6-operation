# 7.4.9.2 Inching Jog Operation

The inching function is a function that does not allow the movement to take place beyond the maximum moving distance per one push of the jog key. 

Even after reaching the inching distance, if you keep pressing the jog key and then release your hand, the robot will decelerate to the inching distance, and then stop.

![Figure 63 When Releasing the Key After Reaching the Inching Distance](../../../.gitbook/assets/image%20%28488%29.png)



If you release the jog key before reaching the inching distance, the robot will decelerate, starting from the time you release the jog key, and then stop. At this time, the mode will be the same as the general jog mode.

![Figure 64 When Releasing the Hand Before Reaching the Inching Distance](../../../.gitbook/assets/image%20%28473%29.png)

{% hint style="info" %}
In the joint coordinate system, the speed level 1 is fixed to a mode that the robot will move by 1 bit of the encoder.
{% endhint %}

