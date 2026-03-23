# 9.2.2 姿态记录移动语句和姿态赋值语句

您可以编辑移动语句中的姿态变量值，包括姿态变量或姿态变量赋值语句。

1. 触摸记录为姿态变量的移动命令 \(移动语句\) 中的 `[property]` 按钮。然后，姿态变量设置屏幕将会出现。

2. 检查并修改当前姿态变量。

    ![](../../_assets/tp630/step-pose-global_eng.png)

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
        <p>当前姿态变量信息。您可以检查并设置名称、坐标值、坐标系统格式等。</p>
        <ul>
          <li><b>[名称]</b>: 当前姿态变量的名称</li>
          <li><b>坐标值</b>: 当前姿态变量的坐标值
            <ul>
              <li>使用光标键选择项目。</li>
              <li>在所需项目中输入值后，按 <b>`[ENTER]`</b> 键以反映更改。</li>
              <li>如果坐标系统格式设置为编码器，坐标值将不会更改。</li>
            </ul>
          </li>
          <li><b>[坐标系统]</b>: 表达当前姿态变量位置的坐标系统格式</li>
          <li><b>[配置]</b>: 描述机器人位置时，由于设备特性存在多种解决方案，因此机器人配置被指定为唯一描述配置。
            <ul>
              <li>此功能仅在坐标系统类型设置为基座或机器人时可用。</li>
              <li>有关机器人配置的详细信息，请参阅 “<a href="../../operation/step/step-pose-modify/">2.3.2 记录和改变一步位置</a><b>.</b> ”</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>`[确定]`: 您可以保存更改。</li>
          <li><b>[上一步]/[下一步]</b>: 您可以显示上一或下一步骤的信息。</li>
          <li><b>[原始值]</b>: 您可以显示当前步骤的原始隐藏姿态值。</li>
          <li><b>[当前机器人姿态]</b>: 您可以显示机器人当前所处的姿态值。</li>
          <li><b>[移动]</b>: 触摸按钮将使机器人移动到记录的步骤位置（Jog）。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

3. 触摸 `[确定]` 按钮。然后，更改将被保存到作业程序中，操作将结束。

* 如果您通过按 `[ESC]` 键结束操作，更改将不会被保存。