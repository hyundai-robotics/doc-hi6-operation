# 8.1 使用 R 代码

使用 R 代码执行指定功能的方法如下。

1. 按下键盘上的 `[R..[NO]]` 键。然后，R 代码的弹出窗口将出现。

    ![](../_assets/tp630/k-r.png)



2. 在输入区输入代码号码，然后触摸 `[OK]` 按钮或按下 `[ENTER]` 键。然后，将执行指定于所选 R 代码的功能。

    ![](../_assets/tp630/pop-rcode_eng.png)



<table style="text-align:left">
  <thead>
    <tr>
      <th>R 代码</th>
      <th>描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>R0 : 重置任务</td>
      <td>初始化步进计数器并移动到 STEP0。</td>
    </tr>
    <tr>
      <td>R1 : 重置错误</td>
      <td>发生错误或警告时清除状态。</td>
    </tr>
    <tr>
      <td>R17 : 打开文件管理器</td>
      <td>快速启动 [服务] -> [5: 文件管理器]</td>
    </tr>
    <tr>
      <td>R86 : 显示剩余内存</td>
      <td>用于在 T/P 屏幕顶部显示 T/P 或主板的剩余内存。</td>
    </tr>
    <tr>
      <td>R99 : 保存</td>
      <td>将存在于内存中的历史数据保存为文件。</td>
    </tr>
    <tr>
      <td>R115 : 复制作业文件</td>
      <td>将创建的作业程序复制到另一个作业程序。</td>
    </tr>
    <tr>
      <td>R117 : 删除作业文件</td>
      <td>此功能用于单独删除已写入的作业。</td>
    </tr>
    <tr>
      <td>R286 : 显示软件版本</td>
      <td>快速启动 [服务] -> [7: 系统诊断] -> [1: 系统版本]</td>
    </tr>
    <tr>
      <td>R321 : 轴同步 jog 设置</td>
      <td>显示设置屏幕以将任意轴分组为一个同步组，并使用单个 jog 键进行 jog 功能。</td>
    </tr>
    <tr>
      <td>R360 : 手动设置 contpath</td>
      <td>此功能强制更改 CONTPATH 的执行状态。</td>
    </tr>
    <tr>
      <td>R361 : 设置 jog 缓冲级别</td>
      <td>当您想要更改当前设置级别的缓冲距离时使用此功能。</td>
    </tr>
    <tr>
      <td>R362 : 轴控制状态更改</td>
      <td>手动执行辅助轴的控制状态 (axisctrl 开/关)。</td>
    </tr>
  </tbody>
</table>