# 6.2.3 公共输入

在面板选择窗口中触摸 `[public Input]`。然后，将出现公共输入信号窗口。

您可以检查通过控制器中 I/O 板的 CNIN 连接器输入的公共输入信号的状态。

![图 40 公共输入信号 - 开/关状态 (左) / 值 (右)](../../_assets/tp630/pane-public-input_eng.png)

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
        <p>显示公共输入信号的状态</p>
        <ul>
          <li>被指定为系统基本规格或用户分配的公共输入信号将以 <b>加粗</b> 显示。</li>
          <li>当前输入的信号将以黄色显示。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[FB0]: 您可以通过触摸下拉菜单选择要监控的 FB 块 (FB0 - FB15)。您可以配置最多 16 个 I/O 块，并且可以监控 960 点信号</li>
          <li><b>[ATTR.-APPLIED]</b>: 您可以勾选复选框，以便在通过正/负逻辑属性之前显示物理输入值。基础设置（未选中）是在通过正/负逻辑属性之后显示输入逻辑值。</li>
          <li>[开/关]/[值]: 您可以通过触摸单选按钮更改信号显示模式。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 在使用信号的情况下，例如通过嵌入式 PLC 映射的现场总线信号，输入信号的开/关状态可能会有所不同。 
* 
  输入信号的流动如下。
{% endhint %}

![](../../_assets/user-input-flow_en.png)