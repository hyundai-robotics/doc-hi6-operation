# 6.3.2 热编辑

这是在播放仍在运行时编辑程序而不停止它的功能。

{% hint style="warning" %}
* 当您编辑并应用当前处于自动操作中或将要调用的程序时，将从下一个周期（执行程序结束后）开始应用，并用编辑过的程序回放机器人。请务必谨慎，因为错误的编辑可能会导致重大事故，例如机器人与夹具之间的碰撞。
{% endhint %}
<br><br>

### 输入

触摸面板上的 `[hot edit]` 按钮，当前程序的热编辑窗口将打开。

![](../../_assets/tp630/pane-hot-edit-0_eng.png)

<br>

### 可编辑的类型

尽管操作与手动模式相同，但以下功能无法使用。

1) `[REC]` 键（记录隐藏的姿态MOVE）：显示“在热编辑过程中不允许操作”的消息。
2) `[POS. MOD]` 键：显示“在热编辑过程中不允许操作”的消息。

    ![](../../_assets/tp630/pane-hot-edit-1_eng.png)

<br>

### 反映

如果您完成了程序编辑，请点击 ![](../../_assets/tp630/bt-menu.png) 导航显示条左侧的按钮以打开弹出菜单，并选择 [hotedit: request to apply]。

![](../../_assets/tp630/pane-hot-edit-apply2_eng.png)

<br>

实际的反映时间显示在以下表格中。

<u>V60.32-03 或更高版本：</u>
<table>
<thead>
  <tr>
    <th>状态</th>
    <th>程序</th>
    <th>请求后，反映时间</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="2">无论是 <br>不运行<br> 还是运行</td>
    <td>不运行程序<br>(不包含在调用栈中的作业)</td>
    <td>立即应用</td>
  </tr>
  <tr>
    <td>运行程序<br>(包含在调用栈中的作业)</td>
    <td>在周期结束时<br>或RESET 0</td>
  </tr>
</tbody>
</table>
<br>

<br>
<u>V60.32-02 或之前版本：</u>

<table>
<thead>
  <tr>
    <th>状态</th>
    <th>程序</th>
    <th>请求后，反映时间</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>不运行</td>
    <td>-</td>
    <td>立即应用</td>
  </tr>
  <tr>
    <td rowspan="2">运行</td>
    <td>不运行程序<br>(不包含在调用栈中的作业)</td>
    <td>立即应用</td>
  </tr>
  <tr>
    <td>运行程序<br>(包含在调用栈中的作业)</td>
    <td>在周期结束时</td>
  </tr>
</tbody>
</table>

<br>

### 标题栏显示

  当前状态符号显示在热编辑窗口标题栏的右侧。

  \'*' 符号表示教学程序已被修改，并与当前运行的程序不同。

  ![](../../_assets/tp630/pane-hot-edit-apply3.png)

  \'>' 符号表示在程序运行时已请求热编辑。

  ![](../../_assets/tp630/pane-hot-edit-apply4.png)

  ' '(空白) 符号表示请求尚未反映，或已反映，因此程序与运行的程序相同。

  ![](../../_assets/tp630/pane-hot-edit-apply5.png)

<Br>

### 不同程序选择

当您按下 `[SHIFT]` + `[PROG]` 键时，您可以选择不同的程序。您还可以创建一个新程序。