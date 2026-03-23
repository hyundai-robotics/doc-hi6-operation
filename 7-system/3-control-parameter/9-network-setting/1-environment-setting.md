# 7.3.9.1 环境设置

您可以设置 LAN 端口所需的网络设置信息。

1.	触摸`[ System - 2: Control Parameter - 9: 网络 - 1: Environment setting ] ([ System  - 2: Control Parameter  - 9: Network  - 1: Environment setting ])`菜单。

2.	设置每个 LAN（公共）端口的参数。支持 Class C 类型 IP 地址。

3.	设置的参数将在您重启系统时调整。

<img src ="../../../_assets/image_551.png">

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">在 LAN 端口选择选项卡中，仅可修改公共 LAN 端口。EtherCAT 和 T/P-Main 端口是固定的，无法更改。
	  </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          更改端口设置。可以修改 IP 地址、子网掩码和网关。
          <li><b>IP 地址 : </b> 您可以为目标端口设置 IP 地址。</li>
          <li><b>子网掩码 : </b> 目标端口的子网掩码设置。通常子网掩码为 255.255.255.0</li>
          <li><b>网关 : </b>您可以为目标端口设置网关地址。第 3 条信息并将其粘贴到另一个端口。
          </li>
          <li><b>MAC : </b>显示控制器的 MAC 地址。
          </li>
        </ul>
      </td>
    </tr>
	<tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>`[OK]`: 您可以保存更改。重启系统后，所有更改将被调整。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>