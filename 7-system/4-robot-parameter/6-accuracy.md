# 7.4.6 精度

您可以设置精度级别的详细条件，这指的是当机器人执行目标步骤时通过该步骤的精度。

1. 触摸 `[3: Robot Parameter - 6: Accuracy] ([3: Robot Parameter - 6: Accuracy])` 菜单。

2. 为每个精度级别设置工具提示位置 \(TCP\) 和姿态。

    ![](../../_assets/tp630/robot-accuracy_eng.png)



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
        <p>每个级别的详细信息。您可以为每个精度级别设置工具提示位置
          (TCP) 和姿态。</p>
        <ul>
          <li>精度级别可以设置为 0 到 7 的值，精度级别将作为步骤语句参数之一被记录。</li>
          <li>精度级别 0&#x2013;6：为每个级别输入 TCP 距离和姿态，以及额外轴的距离和角度。
            <br />对于不支持线性或圆形插补的机器人，例如 LCD 机器人，将采用与额外轴相同的方法。</li>
          <li>精度级别 7：该值将自动计算并显示在控制器上，因此您无需直接输入值。
            <br />当应用精度级别 7 时，将创建一个满足步幅距离 1/2 条件的最大弯曲路径。精度级别 7 在需要使机器人尽可能平稳和快速移动时非常有效，例如 LDC 手进出时的动作。</li>
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
          <li>[重置所有]：您可以初始化所有精度级别的 TCP 距离和姿态。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 如果您根据对 “[2.3 步骤](../../2-operation/3-step/README.md)” 内容的理解接近精度级别，您可以更轻松地使用它。
* 在使用伺服枪或无均衡枪的焊接步骤中，控制器将自动执行限制，无论设置的精度级别如何。 
{% endhint %}