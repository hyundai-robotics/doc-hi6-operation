# 7.4.8.2 设置每个轴的碰撞检测

碰撞检测功能监控每个机器人轴上发生的干扰扭矩和干扰扭矩变化率。如果测量值超过配置的阈值，则视为错误。

* 如果干扰扭矩超过设定阈值，则显示`[E0160 (Axis O) 碰撞检测]`。
* 如果干扰扭矩变化率超过设定阈值，则显示`[E0161 (Axis O) 冲击检测]`。


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
      <td style="text-align:left">启用或禁用每个轴的碰撞检测功能。即使在启用状态下，当机器人停止或点焊枪施加压力时，该功能也不会工作。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">设置在碰撞后是否保持灵敏度。启用时，即使检测到碰撞，当前检测级别也会保持不变。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left"> 
        <p>[测量] 显示在碰撞检测命令（coldet level.id）活动期间发生的最大“干扰扭矩”。</p>
        <p>[阈值] 用户可以参考此值为每个级别配置“干扰扭矩”的阈值。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p>[测量] 显示在碰撞检测命令（coldet level.id）活动期间发生的最大“干扰扭矩变化率”。</p>
        <p>[阈值] 用户可以参考此值为每个级别配置“干扰扭矩变化率”的阈值。</p>
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
      <td style="text-align:left">用于将每个轴配置的所有级别值重置为其默认值。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left">用于添加额外的级别。可配置的最大级别数为16。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c8.png" alt/>
      </td>
      <td style="text-align:left">用于删除最高级别。删除可以从级别6及以上开始。</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
碰撞检测测量值最多显示2分钟。
{% endhint %}