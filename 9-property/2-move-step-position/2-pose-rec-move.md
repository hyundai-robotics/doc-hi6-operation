# 9.2.2 位姿记录移动语句和位姿赋值语句

您可以在移动语句中编辑位姿变量值，包括位姿变量或位姿变量赋值语句。

1.	触摸记录为位姿变量的移动命令 \(移动语句\) 中的 `[property]` 按钮。然后，位姿变量设置屏幕将会出现。

2.	检查并修改当前位姿变量。

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
        <p>当前位姿变量信息。您可以查看并设置名称、坐标值、坐标系格式等。</p>
        <ul>
          <li><b>[名称]</b>: 当前位姿变量的名称</li>
          <li><b>坐标值</b>: 当前位姿变量的坐标值
            <ul>
              <li>使用光标键选择项目。</li>
              <li>在所需项目中输入值后，按下 <b>`[ENTER]`</b> 键以反映更改。</li>
              <li>如果坐标系格式设置为编码器，坐标值将不会改变。</li>
            </ul>
          </li>
          <li><b>[坐标系]</b>: 表示当前位姿变量位置的坐标系格式</li>
          <li><b>[配置]</b>: 当描述机器人位置时，由于设备特性存在多个解决方案，因此指定机器人配置以唯一描述配置。
            <ul>
              <li>此功能仅在坐标系类型设置为基座或机器人时可用。</li>
              <li>有关机器人配置的详细信息，请参见“<a href="../../operation/step/step-pose-modify/">2.3.2 记录和更改步骤位置</a><b>.</b> ”</li>
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
          <li><b>[上一个]/[下一个]</b>: 您可以显示上一个或下一个步骤的信息。</li>
          <li><b>[原始值]</b>: 您可以显示当前步骤的原始隐藏位姿值。</li>
          <li><b>[当前机器人位姿]</b>: 您可以显示机器人当前采取的位姿值。</li>
          <li><b>[移动]</b>: 触摸该按钮将使机器人移动到记录的步骤位置 (Jog)。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

3.	触摸 `[确定]` 按钮。然后，更改将保存在作业程序中，操作将结束。

* 如果您通过按 `[ESC]` 键结束操作，则更改不会被保存。