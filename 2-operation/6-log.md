# 2.6 事件日志

存储从过去到现在发生的事件日志，例如错误、警告、通知、开始/停止操作、操作、I/O 值变化和机器人语言执行。(存储的记录最大数量根据类型而异。)<br>
您可以查看每个日志的类型、消息、发生时间、发生时的程序/步骤/功能编号以及相关的辅助信息。此信息可作为分析问题原因和应对问题的线索。

请触摸功能按钮栏上的`[Log]`按钮。然后，日志窗口将出现。

![](../_assets/tp630/log/11_fb_log.PNG)

您可以查看事件日志。请触摸右侧的上箭头图标。

![](../_assets/tp630/log/21_log.PNG)

日志的过滤选项和辅助信息如下所示。

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
        辅助信息：发生错误或警告时系统的状态也会被记录，您可以在辅助信息窗口中查看。在顶部点击标签可以选择并查看所需的辅助信息。活动输入/输出信号值以黄色背景显示，分配的用户 I/O 以加粗显示。
        <ul>  
          <li>姿态：机器人、附加轴值。(单位：mm 或 deg.)</li>
          <li>S/In：系统输入值。仅记录前 8 字节。(si0~63)</li>
          <li>S/Out：系统输出值。仅记录前 8 字节。(so0~63)</li>
          <li>D/In：用户输入值。仅记录 fb0 的前 32 字节。</li>(fb0.dib0~31)
          <li>D/Out：用户输出值。仅记录 fb0 的前 32 字节。</li>(fb0.dob0~31)
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png"/>
      </td>
      <td style="text-align:left">
        您可以使用过滤按钮仅显示所需类型的日志。当过滤按钮打开时，相应的类型将被显示，关闭时将被隐藏。
        <ul>
          <li>[全部]：一次打开或关闭所有过滤按钮。</li>
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
              <li>另存为日志文件：事件首先存储在内存缓冲区中，当缓冲区满时，它们会自动保存到文件中。通过选择此菜单，仍在缓冲区中的任何日志将立即保存到文件。</li>
              <li>清除日志文件：您可以清除内存缓冲区中的日志并删除所有日志文件。（已删除的文件无法恢复。）</li>
            </ul>
          </li>
          <li>[
            <img src="../_assets/bt-lock.png"/>]: 此功能锁定屏幕上新事件的显示。即使被锁定，新事件仍将继续记录；仅屏幕刷新被阻止。当日志屏幕不停更新并阻挡视线时，此功能可能很有用。您可以通过再次按锁定按钮或关闭并重新打开日志窗口来解锁。
          </li>
          <li>[
            <img src="../_assets/bt-trash.png"/>]: 此操作清除屏幕上显示的事件。它仅清除屏幕，内部记录的日志不会被删除。</li>
          <li>[
            <img src="../_assets/bt-refresh.png"/>]: 当日志屏幕被清除时，按此按钮将重新获取日志并在屏幕上显示。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c4.png"/>
      </td>
      <td style="text-align:left">这是选定类型的日志。新事件在上方以黄色背景突出显示。</td>
    </tr>
  </tbody>
</table>