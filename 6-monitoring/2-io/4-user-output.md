# 6.2.4 公共输出

在面板选择窗口中触摸 `[public Output]`。然后，公共输出信号窗口将出现。

您可以检查控制器中I/O板的CNOUT连接器输出的公共输出信号的状态。

![Figure 40 公共输出信号 - 开/关状态 \(左\)/值状态 \(右\)](../../_assets/tp630/pane-univoutsig-mode_eng.png)

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
        <p>显示一般输出信号的状态</p>
        <ul>
          <li>指定为系统的基本规格或用户分配的一般输出信号将以 <b>粗体</b> 显示。</li>
          <li>当前正在输出的信号将以黄色显示。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[FB0]: 您可以通过触摸下拉菜单选择要监控的FB块 (FB0 - FB15)。您最多可以配置16个I/O块，并且使用一个块可以监控960个信号点。</li>
          <li>[手动输出]: 您可以强制输出所选信号。</li>
          <li><b>[ATTR.-APPLIED]</b>: 您可以勾选复选框，以便在通过正/负逻辑属性之前显示物理输入值。基本设置（未勾选）是显示通过正/负逻辑属性后的输入逻辑值。</li>
          <li>[开/关]/[值]: 您可以通过触摸单选按钮更改信号显示模式。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 在通过嵌入式PLC映射场总线信号等信号的情况下，输出信号的开/关状态可能会有所不同。
* 
  输出信号的流动如下。
{% endhint %}

![](../../_assets/user-input-flow_en.png)

#### 

#### 手动输出

您可以选择所需的信号并强制输出。

1.	您可以通过触摸一般输出信号窗口右侧的 `[ON/OFF]` 单选按钮将显示模式设置为开/关状态。

2.	触摸信号以在信号窗口中选择它，然后触摸 `[手动输出]` 按钮。

    ![](../../_assets/tp630/pane-univoutsig_eng.png)

3.	在手动输出确认窗口中检查输出条件后，触摸 `[ENTER]` 按钮。

    ![](../../_assets/tp630/pane-univoutsig-manual_eng.png)

| FbN | doN | =1/0 |
| :---: | :---: | :---: |
| N: 要监控的FB块编号 | N: 要输出的信号编号 | 输出状态 \(1: 输出, 0: 不输出\) |

4.	检查所选信号的输出状态。所选信号将切换到输出状态并在信号窗口中以黄色显示。

    ![](../../_assets/tp630/pane-univoutsig-onoff_eng.png)