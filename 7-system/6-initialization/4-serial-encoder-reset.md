# 7.6.4 串行编码器重置

串行编码器将编码器旋转速度信息存储在内部内存中。通过解决电机错误状态或重置编码器的零点，可以将编码器旋转速度清零。

1.	触摸`[5: Initialize - 4: Serial Encoder Reset] ([5: Initialize - 4: Serial Encoder Reset])`菜单。

2.	为每个轴设置编码器重置模式并检查状态，然后执行重置。

    ![](../../_assets/tp630/init-serialenco-reset_eng.png)

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
        <p>您可以为每个轴设置是否使用编码器重置功能，并为每个轴设置模式。</p>
        <ul>
          <li>[禁用]: 不执行串行编码器重置。</li>
          <li>[错误释放]: 您可以清除与电机编码器相关的错误，而不清除编码器旋转速度。</li>
          <li>[重置]: 通过解决与电机编码器相关的错误，然后重置编码器的零点，可以清除旋转速度。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[执行]: 您可以执行串行编码器重置。</li>
          <li>[全选]: 您可以一次选择所有轴。</li>
          <li>[全取消]: 您可以一次取消所有轴的选择。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
* 在执行机器人系统的初始设置时，您可以执行编码器重置，但绝不要在机器人正常操作时执行编码器重置。然而，如果发生通信错误等与编码器相关的错误或编码器电池丢失，您可以执行编码器重置。在这种情况下，请在机器人程序中检查实际位置，以便与现有机器人原点位置不发生差异。
* 如果控制器和编码器未供电，编码器的位置信息可能会丢失，可能会导致使用机器人作业程序时出现问题。为解决此问题，专用电池连接到串行编码器，使其能够在控制器的电源状态下记录位置信息。如果在编码器电池中发生电压错误，必须在控制器仍然通电的情况下更换电池，以防止丢失位置信息。
{% endhint %}