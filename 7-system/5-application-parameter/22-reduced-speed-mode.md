# 7.5.22 Reduced Speed Mode

When the input signal (di) changes from OFF to ON, the robot speed is reduced according to the set reduction ratio. <br>
In the move command, the robot speed is applied by combining the original speed value with the auto mode robot speed and the reduction ratio. <br>

![](../../_assets/tp630/reduced_spd_mode.png)

  * Input Signal: Sets the signal received by the controller.
  * Active: 
    * High : Reduction is applied when the signal is ON, and canceled when the signal is OFF.
    * Low : Reduction is applied when the signal is OFF, and canceled when the signal is ON.
  * Reduced Speed Rate:  
    * Determines the ratio by which the speed will be reduced.
    * When the reduced speed mode input signal is received, the robot speed is set to the auto mode robot speed multiplied by the reduced speed rate.

{% hint style="info" %}
* The reduction ratio is not applied in manual mode.
{% endhint %}

{% hint style="warning" %}
* Select the correct active condition that matches the state of the input signal.
* When an I/O signal is received during playback, the reduced speed mode will still be applied.
{% endhint %}

{% hint style="warning" %}
* Sélectionnez la condition d'activation correspondant à l'état du signal d'entrée.
* Si un signal d'E/S est reçu pendant l'exécution, le mode de vitesse réduite reste appliqué.
{% endhint %}
