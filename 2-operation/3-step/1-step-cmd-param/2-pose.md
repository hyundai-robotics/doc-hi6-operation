# 2.3.1.2 位姿

位姿是记录位置的参数。如果您通过使用 `[Command]` 按钮输入移动，该运动命令，您应该在 tg \(target\) 参数中指定位姿表达。当使用 `[REC]` 键输入移动语句时，tg 参数不会出现。在触碰 `[REC]` 按钮的瞬间，机械手的位置信息和姿态将被记录，但它们不会在 JOB 编辑屏幕上显示，这就是它们被称为隐藏位姿的原因。

输入位姿的方法如下。

1. 声明一个位姿变量，po1。
   选择 [cmd.input > var_io > global or var] 菜单，然后输入 'po1'。
2. 使用 `[cur.pose]` 按钮将位姿变量初始化为位姿类型。
3. 执行声明和初始化命令，以便在每个命令前标记句点。
4. 在触碰 `[cmd.input]` 按钮后，选择 `[motion]` 然后输入语句。

    ![](../../../_assets/tp630/fbt-cmd-input-motion_eng.png)

5. 在触碰 `[property]` 按钮后，设置当前机器人位姿的属性，然后触碰 `[Apply]` 按钮。

    ![](../../../_assets/tp630/prg-step-pose_eng.png)

<br>

位姿变量和位移变量将以以下格式保存。

<table>
  <thead>
    <tr>
      <th style="text-align:center">位姿变量</th>
      <th style="text-align:center">位移变量</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center">(X, Y, Z, Rx, Ry, Rz, {坐标系}, {config.})</td>
      <td style="text-align:center">(X, Y, Z, Rx, Ry, Rz, {坐标系})</td>
    </tr>
    <tr>
      <td style="text-align:center">
        <p>{坐标系}:</p>
        <p>&quot;base&quot; = 基坐标系
          <br />&quot;robot&quot; = 机器人坐标系
          <br />&quot;user{n}&quot; = 用户坐标系 (n 指的是数字)
          <br
          />&quot;joint&quot; = 关节坐标系
          <br />&quot;encoder&quot;= 编码器</p>
      </td>
      <td style="text-align:center">
        <p>{坐标系}:</p>
        <p>&quot;base&quot; = 基坐标系
          <br />&quot;robot&quot; = 机器人坐标系
          <br />&quot;user{n}&quot; = 用户坐标系 (n 指的是数字)
          <br
          />&quot;joint&quot; = 关节坐标系</p>
      </td>
    </tr>
  </tbody>
</table>