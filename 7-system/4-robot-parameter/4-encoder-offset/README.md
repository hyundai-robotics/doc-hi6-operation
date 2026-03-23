# 7.4.4 编码器偏移

当前编码器位置可以设置为编码器原点位置 \(position 0X400000\)。您可以在机器人的每个轴的参考位置处确定编码器原点 \(每个轴附着刻度的位置\)。

1. 触摸 `[3: Robot Parameter - 4: Encoder Offset] ([3: Robot Parameter  - 4: Encoder Offset])` 菜单。

2. 通过调整每个轴的位置设置编码器偏移值。编码器偏移值将以十六进制数 \(a hexadecimal number\) 形式记录。

    ![](../../../_assets/tp630/robot-encoder-offset_eng.png)



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
      <td style="text-align:left">每个轴的编码器偏移值的详细信息。您可以设置已校准的编码器值、当前编码器值和轴的当前位置。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: 您可以保存更改。</li>
          <li>[Reset One]/[Reset All]: 您可以初始化所选或所有轴的编码器偏移值。</li>
          <li>[Calculate Correction Value]: 您可以校准所选轴的编码器偏移值。</li>
          <li>[Previous Correction Value]: 您可以检索在选定轴的校准之前存在的编码器偏移值。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
编码器偏移值在出厂时设置。只有在必要时，例如更换马达或编码器时，才应重置编码器偏移值。
{% endhint %}