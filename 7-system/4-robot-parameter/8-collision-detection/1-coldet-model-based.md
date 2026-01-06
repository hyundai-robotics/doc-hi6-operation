# 7.4.8.1 Model-Based Impact Detection

The model-based impact detection function detects collisions by calculating the difference between the torque that should normally be generated during robot motion and the torque actually measured, based on the robot’s dynamic model.
Sensitivity can be adjusted to control responsiveness to collisions, and contact with external objects occurring while the robot is moving at low speed can also be detected.


1. Touch the menu \[3: Robot parameter &gt; 14: Impact Detection &gt; 1: Model-Based Collision Detection\].


![](../../../_assets/tp630/coldet/model_based_coldet_tab_general.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">Enables or disables the model-based collision detection function.</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">Represents the default sensitivity for all axes. A higher value increases collision detection sensitivity.
      (Default: 100, Maximum: 200)  </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">Enables or disables the low-speed collision detection function. </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">The setting time for detecting low-speed collisions. If a collision force is applied for longer than this reference time, it is recognized as a collision. </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">A collision is considered a low-speed collision only when the link speed is lower than the set value. </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">Resets the settings to their default values.</td>
    </tr>
  </tbody>
</table>


![](../../../_assets/tp630/coldet/model_based_coldet_tab_axis.png)

{% hint style="info" %}
The per-axis settings tab is enabled only in Engineering Mode or higher.
{% endhint %}

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">Ratio (%) relative to the collision detection threshold for each axis. Lower values result in more sensitive responses.</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">Cutoff frequency value, generally set according to the robot’s control environment. If any axis is set to 0, collision detection for that axis is disabled.(Maximum: 100) </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">Resets the settings to their default values.</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
The final sensitivity value for each axis is proportional to the per-axis sensitivity value and inversely proportional to the overall default sensitivity for all axes.
{% endhint %}
