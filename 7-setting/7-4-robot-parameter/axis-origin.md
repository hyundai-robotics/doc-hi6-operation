# 7.4.2 Axis Origin

You can register the mechanical origin position of each axis.

1.	Touch the \[3: Robot Parameter &gt; 2: Axis Origin\] menu.

2.	Register the mechanical origin position of each axis.

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
        <p>Detailed information on the mechanical origin position of each axis. You
          can set the encoder and position of the axis.</p>
        <ul>
          <li>S-axis: You can change the S-axis origin depending on the installation
            situation of the robot and surrounding jig.</li>
          <li>R1-axis: You can change the origin of the R1- axis origin according to
            the tool attachment direction.</li>
          <li>H, V, R2, and B axes: Can be set automatically through the automatic calibration
            function</li>
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
          <li>[Apply One]: You can apply the selected origin position to the selected
            axis information.</li>
          <li>[Apply All]: You can apply the selected origin position to all axis information.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
* The axis origin setting affects the accuracy of the robot’s cartesian operation. Change it to the exact value as much as possible.
* 
  If the axis origin setting is changed, the position of the previously created program will be changed. Therefore, the axis origin setting must be executed only at the initial installation stage.

* 
  If the encoder offset setting is changed, the axis origin should be newly set. Therefore, the encoder offset setting must be completed before the setting of the axis origin.
{% endhint %}

{% hint style="info" %}
At the time of the shipping from the factory, the mechanical origin position of each axis is set at the standard value \(0X400000\).
{% endhint %}

