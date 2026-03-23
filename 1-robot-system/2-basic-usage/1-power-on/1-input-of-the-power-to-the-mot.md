# 1.2.1.1 输入电源到电机和可操作状态

教导 pendant 的模式开关和安全插头的状态决定电源输入到电机和可操作状态。

<table>
  <thead>
    <tr>
      <th style="text-align:left">安全插头</th>
      <th style="text-align:left">模式开关：手动</th>
      <th style="text-align:left">模式开关：自动</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">释放</td>
      <td style="text-align:left">
        <ul>
          <li>电机开启启用</li>
          <li>向前/向后步进启用</li>
        </ul>
      </td>
      <td style="text-align:left">紧急（电机关闭）</td>
    </tr>
    <tr>
      <td style="text-align:left">接入</td>
      <td style="text-align:left">
        <ul>
          <li>电机开启启用</li>
          <li>向前/向后步进启用</li>
        </ul>
      </td>
      <td style="text-align:left">
        <ul>
          <li>电机开启启用</li>
          <li>正常速度操作</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
安全插头用于一般工业机器人，而LCD机器人则使用光幕代替安全插头。
{% endhint %}