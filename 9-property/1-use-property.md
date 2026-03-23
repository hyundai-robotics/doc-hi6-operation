# 9.1 使用属性功能

如果您在 ${cont_model} 教导挂钩屏幕的 L 按钮栏上使用 `[property]` 按钮，您可以通过一次按钮操作快速轻松地设置条件并检查位置。

![Figure 75 Function for the `[Attributes]` Button](../_assets/tp630/lbt-property-arc_eng.png)

例如，如果您在用于 Arc On 功能的 'arcon' 语句上触摸 `[property]` 按钮，将显示当前语句中用于焊接启动条件的条件编号的内容。在屏幕上，您可以检查或更改焊接启动条件的详细信息。此外，如果与相关条件文件关联的其他条件文件存在，您可以直接转到它。换句话说，`[property]` 按钮允许您迅速轻松地检查和更改与特定语句相关的内容的详细信息，例如条件文件或步骤位置。

以下显示了使用 `[property]` 按钮检查和更改与特定命令相关的条件文件和详细信息的方法。

1. 选择一个特定语句，将光标放在其上，并触摸 `[property]` 按钮。

2. 参照以下表格，您可以检查和更改与所选语句相关的文件或详细信息。

<table>
  <thead>
    <tr>
      <th style="text-align:left">语句</th>
      <th style="text-align:left">文件和内容</th>
      <th style="text-align:left">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>move</p>
        <p></p>
        <p>refp</p>
        <p></p>
      </td>
      <td style="text-align:left">
        <p>步骤位置</p>
        <p></p>
        <p>参考位置</p>
      </td>
      <td style="text-align:left">
        <p>当前位置或全局位姿变量</p>
        <p>X Y Z (mm) Rx Ry Rz (度) T1&#x2013;T10</p>
        <p>单位、坐标系和机器人配置</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">arcon asf=</td>
      <td style="text-align:left">
        <p>焊接启动条件</p>
        <p>焊接辅助条件</p>
        <p>电弧焊条件</p>
      </td>
      <td style="text-align:left">
        <ul>
          <li>焊接启动条件：条件编号、描述、电压检查、重试、操作模式、输出电流、输出电压、WCR 等待时间、机器人延迟时间等。</li>
          <li>焊接辅助条件
            <ul>
              <li>重试：计数、收回时间/速度、反向步骤/焊接线移动量、偏移移动量、速度、电流、电压</li>
              <li>重新启动：计数、重叠量、移动速度、焊接电流、电压、电流</li>
              <li>重叠条件设置（在焊接中间）：电弧、气体、焊丝和冷却液</li>
            </ul>
          </li>
          <li>电弧焊条件：焊机编号、标题、描述、功率控制模式、焊丝直径、突出的距离、沉积检测时间、ARC OFF 检测时间等。
            <ul>
              <li>电流属性：极性、指令值 (V)、测量值 (A) 和补偿值</li>
              <li>电压属性：极性、指令值 (V)、测量值 (V) 和补偿值</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">arcon aef=</td>
      <td style="text-align:left">
        <p>焊接结束条件</p>
        <p>焊接辅助条件</p>
      </td>
      <td style="text-align:left">
        <ul>
          <li>焊接结束条件：条件编号、描述、电压检查、输出电流、输出电压、降坡、条件保持时间和气体后流</li>
          <li>焊接辅助条件：自动沉积释放：计数、电流、电压、延迟时间</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">weavon wev=</td>
      <td style="text-align:left">编织条件</td>
      <td style="text-align:left">
        <ul>
          <li>编织条件：枪号、编织类型、频率、基本模式、进度角、边界限制、移动时间和定时器</li>
          <li>电弧感应条件：电弧感应、左右感应启动周期、上下感应周期、电压因子、每次采样的补偿距离等。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

3. 触摸 `[Record]` 按钮或按 `[ESC]` 键以结束操作。

* `[Record]`：您可以保存更改并结束操作。
* `[ESC]`：您可以取消更改并结束操作。