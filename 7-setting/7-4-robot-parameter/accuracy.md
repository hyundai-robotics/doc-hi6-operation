# 7.4.6 Accuracy

You can set the detailed conditions of the accuracy level, which refers to the accuracy of passing through the step when the robot progresses the target step.

1.	Touch the \[3: Robot Parameter &gt; 6: Accuracy\] menu.

2.	Set the tooltip position \(TCP\) and posture for each accuracy level.

![](../../.gitbook/assets/image%20%28478%29.png)



<table>
  <thead>
    <tr>
      <th style="text-align:left">No.</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Detailed information for each level. You can set the tooltip position
          (TCP) and posture for each accuracy level.</p>
        <ul>
          <li>The accuracy level can be set to a value from 0 to 7, and the accuracy
            level will be recorded as one of the step statement parameters.</li>
          <li>Accuracy level 0&#x2013;6: Input the TCP distance and posture, as well
            as the distance and angle of the additional axis, for each level.
            <br />For the robots that do not support linear or circular interpolation, such
            as LCD robots, the same method as for additional axes will be applied.</li>
          <li>Accuracy level 7: The value will be automatically calculated and displayed
            in the controller, so you do not need to input the value directly.
            <br />When the accuracy level 7 is applied, the maximum cornering path that
            satisfies the condition of 1/2 of the step distance will be created. Accuracy
            level 7 is useful when it is required to make the robot move as smoothly
            and quickly as possible, such as the act of LDC hand entering and exiting.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: You can save the changes.</li>
          <li>[Reset All]: You can initialize the TCP distance and posture for all accuracy
            levels.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* If you approach the accuracy level based on your understanding of the contents of “2.3 Step,” you can use it more easily.
* In the welding step that uses a servo gun or an equalizerless gun, the controller will automatically perform restriction regardless of the set accuracy level. 


{% endhint %}



