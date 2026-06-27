# 7.4.8.2 设置每轴碰撞检测

碰撞检测功能监测每个机器人轴上发生的干扰扭矩和干扰扭矩的变化率。如果测量值超过配置的阈值，则视为错误。

* 如果干扰扭矩超过设置的阈值，将显示`[E0160 (Axis O) 检测到碰撞]`。
* 如果干扰扭矩速率超过设置的阈值，将显示`[E0161 (Axis O) 检测到冲击]`。

![](../../../_assets/tp630/coldet/collision_detection_of_axis.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">编号</th>
      <th style="text-align:left">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">启用或禁用每轴碰撞检测功能。即使启用，该功能在机器人停止或点焊枪施加压力时也不运行。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">设置在碰撞后是否保持灵敏度。当启用时，即使在检测到碰撞后，当前检测水平也会保持不变。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left"> 
        <p>[测量] 显示在碰撞检测命令（coldet level.id）处于激活状态期间发生的最大"干扰扭矩"。</p>
        <p>[阈值] 用户可以参考此值为每个级别配置"干扰扭矩"阈值。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p>[测量] 显示在碰撞检测命令（coldet level.id）处于激活状态期间发生的最大"干扰扭矩变化率"。</p>
        <p>[阈值] 用户可以参考此值为每个级别配置"干扰扭矩变化率"阈值。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">重新测量每个轴的干扰扭矩和干扰扭矩变化率的最大测量值。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">用于将每个轴配置的所有级别值重置为默认值。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left">用于添加额外的级别。可配置的最大级别数量为16。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c8.png" alt/>
      </td>
      <td style="text-align:left">用于删除最高级别。可以从第6级及以上开始删除。</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
碰撞检测测量值最多可显示2分钟。
{% endhint %}