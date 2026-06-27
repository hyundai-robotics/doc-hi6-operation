# 2.6 事件日志

存储从过去到当前时间点发生的事件日志，例如错误、警告、通知、开始/停止操作、操作、I/O 值变化和机器人语言执行。（存储的最大记录数根据类型而异。）<br>
您可以查看每个日志的类型、消息、发生时间、发生时的程序/步骤/功能编号及相关辅助信息。这些信息可以作为分析问题原因及应对问题的线索。

请触摸功能按钮栏上的 `[Log]` 按钮。然后，日志窗口将出现。

![](../_assets/tp630/log/11_fb_log.PNG)

您可以查看事件日志。请触摸右侧的向上箭头图标。

![](../_assets/tp630/log/21_log.PNG)

日志的过滤选项和辅助信息如下所示；

![](../_assets/tp630/log/31_log.PNG)
![](../_assets/tp630/log/44_di.PNG)

{% hint style="info" %}
辅助信息的显示从 V60.30-01 开始支持。
{% endhint %}

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
        <img src="../_assets/c1.png"/>
      </td>
      <td style="text-align:left">
        辅助信息：错误或警告发生时系统的状态也被记录，您可以在辅助信息窗口中查看。通过点击顶部的选项卡，您可以选择并查看所需的辅助信息。活动输入/输出信号值以黄色背景显示，分配的用户 I/O 以粗体显示。
        <ul>  
          <li>姿态 : 机器人，附加轴值。(单位：mm 或 deg.)</li>
          <li>S/In : 系统输入值。仅记录前 8 字节。(si0~63)</li>
          <li>S/Out : 系统输出值。仅记录前 8 字节。(so0~63)</li>
          <li>D/In : 用户输入值。仅记录 fb0 的前 32 字节。</li>(fb0.dib0~31)
          <li>D/Out : 用户输出值。仅记录 fb0 的前 32 字节。</li>(fb0.dob0~31)
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png"/>
      </td>
      <td style="text-align:left">
        您可以使用过滤按钮仅显示所需类型的日志。当过滤按钮开启时，对应的类型将显示，关闭时将隐藏。
        <ul>
          <li>[全部]：同时开启或关闭所有过滤按钮。</li>
          <li>[+E]/[+W]：查看错误或警告日志。</li>
          <li>[+N]：查看通知（Notice）日志。</li>
          <li>[+ST]：查看机器人启动（START）和停止（STOP）日志。</li>
          <li>[+P]：查看定期记录的状态日志。</li>
          <li>[+OP]：查看用户操作日志。</li>
          <li>[+IO]：查看输入/输出信号变化日志。</li>
          <li>[+H]：查看作业程序执行日志。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c3.png"/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[
            <img src="../_assets/bt-menu.png"/>]: 您可以打开弹出菜单。
            <ul>
              <li>另存为日志文件：事件首先存储在内存缓冲区中，当缓冲区满时，它们会自动保存到文件中。通过选择此菜单，缓冲区中仍然存在的任何日志将立即保存到文件。</li>
              <li>清除日志文件：您可以清除内存缓冲区中的日志并删除所有日志文件。（删除的文件无法恢复。）</li>
            </ul>
          </li>
          <li>[
            <img src="../_assets/bt-lock.png"/>]: 此功能锁定屏幕上新事件的显示。即使被锁定，新事件仍将继续记录；只有屏幕刷新被阻止。当日志屏幕不断更新并阻碍视野时，此功能可能会很有用。您可以再次按锁定按钮或关闭并重新打开日志窗口来解锁它。
          </li>
          <li>[
            <img src="../_assets/bt-trash.png"/>]: 这会清除屏幕上显示的事件。它只清除屏幕，而内部记录的日志不会被删除。</li>
          <li>[
            <img src="../_assets/bt-refresh.png"/>]: 当日志屏幕被清除时，按下此按钮将重新检索日志并在屏幕上显示。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c4.png"/>
      </td>
      <td style="text-align:left">这是所选类型的日志。新事件以黄色背景突出显示在顶部。</td>
    </tr>
  </tbody>
</table>