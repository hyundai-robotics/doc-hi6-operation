# 6.3.8 程序预留执行

为了进行监视，需进行预设。您必须在`系统 - 2:控制参数 - 7:程序预留执行 (system - 2:Control parameter - 7:Program reservation execution)`页面上选择注册号为20EA或1EA。

![](../../_assets/tp630/ctrl-prog-reserve_eng.png)

在面板选择窗口中，触摸`[program reserve]`。然后，计划的程序执行窗口将出现。

当通过外部信号安排程序并按计划顺序执行时，您可以在计划程序列表中检查和更改状态。

![Figure 50 Program reserve](../../_assets/tp630/pane-prog-reserv_eng.png)

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
        <p>计划程序的列表。您可以安排1–20个程序。</p>
        <ul>
          <li>当在远程模式下执行的程序终止时，程序将根据计划顺序自动执行。</li>
          <li>当计划程序执行完成后，这些程序将从列表中删除。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[编辑]</b>: 您可以编辑计划程序的列表。</li>
          <li><b>[插入]</b>: 您可以将一个将在计划中执行的程序添加到计划程序列表中。</li>
          <li><b>[删除]</b>: 您可以从计划程序列表中删除一个已安排的程序。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>



{% hint style="info" %}
* 仅当应用功能中的传感器同步功能的同步状态设为输送机或压力时，`[Program reserve]`项目才会被激活。
* 如果`[system - 2: Control Parameter - 8: Program reserve] ([system  - 2: Control Parameter  - 8: Program reserve])`菜单中的`[Applied Register Count]`选项被设为禁用，则`[Program reserve]`项目将不会被激活。
* 有关计划程序执行的详细信息，请参阅"${cont_model}控制器计划程序执行功能手册"。
{% endhint %}