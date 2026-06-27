# 7.4.8.1 基于模型的冲击检测

基于模型的冲击检测功能通过计算在机器人运动期间正常应生成的扭矩与实际测量的扭矩之间的差异来检测碰撞。可以调整灵敏度以控制对碰撞的响应，并且可以检测robot在低速移动时与外部物体接触的情况。


1. 触摸菜单 `[3: Robot parameter - 14: Impact Detection - 1: Model-Based Collision Detection] ([3: Robot parameter  - 14: Impact Detection  - 1: Model-Based Collision Detection])`。


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
      <td style="text-align:left">启用或禁用基于模型的碰撞检测功能。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">代表所有轴的默认灵敏度。较高的值增加碰撞检测灵敏度。
      (默认: 100, 最大: 200)  </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">启用或禁用低速碰撞检测功能。 </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">检测低速碰撞的设定时间。如果碰撞力施加的时间超过该参考时间，则被识别为碰撞。 </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">只有当连杆速度低于设定值时，碰撞才被视为低速碰撞。 </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">将设置重置为默认值。</td>
    </tr>
  </tbody>
</table>


![](../../../_assets/tp630/coldet/model_based_coldet_tab_axis.png)

{% hint style="info" %}
每个轴的设置选项卡仅在工程模式或更高模式下启用。
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
      <td style="text-align:left">相对于每个轴的碰撞检测阈值的比率（%）。较低的值导致更灵敏的响应。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">截止频率值，通常根据机器人的控制环境设置。如果任何轴设置为0，则禁用该轴的碰撞检测。（最大: 100） </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">将设置重置为默认值。</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
每个轴的最终灵敏度值与每个轴的灵敏度值成正比，与所有轴的整体默认灵敏度成反比。
{% endhint %}