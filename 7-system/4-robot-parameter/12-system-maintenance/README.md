# 7.4.10 Reducer Lifespan Setting

If the reducer of the robot axis is replaced, the rated life of the reducer should be initialized.
The rate at which the rated life of the reducer is exhausted depends on the operating load conditions and speed. The higher the speed and the higher the load, the faster the life span decreases.
The reducer life data can be found in the system characteristics data. 
The monitoring menu displays the remaining rated life of the reducer and the expected life based on the latest robot operation pattern.

Rated life : Remaining life when continuously driven under rated load and rated speed conditions<br>
Expected life: Estimated remaining life based on recent actual driving conditions.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  Life expectancy may increase or decrease depending on the robot's recent motion patterns. 

Initialization of the reducer lifespan
1.    Touch the \[3: Robot parameter &gt; 12: System maintenance &gt; 2:Reducer Lifespan setting\] menu.

2.    Move the cursor to the position corresponding to the replaced reducer and touch the \[**Reset one**\] button.
If all reducers are replaced or the body is replaced with a new robot, touch the \[**Reset all**\] button. In the case of a reducer whose rated life is initialized, the date of initialization is recorded in the chaned date column.

![](../../../_assets/tp630/reducer_lifetime_setting.png)


Lifespan calculation cycle\[**min**\] : Renewal period of reducer lifespan. The minimum period is 10 minutes.

{% hint style="info" %}
The reducer rated and expected life are predicted reference values based on reducer life prediction model. The actual life of the reducer may vary from the expected model depending on the driving conditions.
{% endhint %}