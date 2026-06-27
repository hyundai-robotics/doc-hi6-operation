# 7.4.2 轴原点

您可以注册每个轴的机械原点位置。

1. 触摸 `[3: Robot Parameter - 2: Axis Origin] ([3: Robot Parameter  - 2: Axis Origin])` 菜单。

2. 注册每个轴的机械原点位置。

    ![](../../_assets/tp630/robot-origin_eng.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>每个轴机械原点位置的详细信息。您
          可以设置轴的编码器和位置。</p>
        <ul>
          <li>S轴：您可以根据机器人和周围夹具的安装情况更改S轴原点。</li>
          <li>R1轴：您可以根据工具安装方向更改R1轴原点。</li>
          <li>H、V、R2 和 B 轴：可以通过自动校准功能自动设置。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[确定]：您可以保存更改。</li>
          <li>[应用单个]：您可以将选定的原点位置应用于选定的轴信息。</li>
          <li>[应用所有]：您可以将选定的原点位置应用于所有轴信息。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
* 轴原点设置会影响机器人的笛卡尔操作精度。尽量将其更改为准确值。
* 
  如果更改轴原点设置，先前创建的程序的位置将会改变。因此，轴原点设置必须仅在初始安装阶段执行。

* 
  如果更改了编码器偏移设置，则应重新设置轴原点。因此，在设置轴原点之前，必须完成编码器偏移设置。
{% endhint %}

{% hint style="info" %}
在出厂时，每个轴的机械原点位置设置为标准值 \(0X400000\)。
{% endhint %}