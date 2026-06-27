# 9.1 使用属性功能

如果您在${cont_model}教学挂件屏幕的L按钮栏中使用`[property]`按钮，您可以通过单个按钮操作快速轻松地设置条件并检查位置。

![图 75 `[Attributes]` 按钮的功能](../_assets/tp630/lbt-property-arc_eng.png)

例如，如果您在'arc on'语句上触摸`[property]`按钮，该语句用于Arc On功能，则当前语句中使用的条件编号的内容将显示在屏幕上。您可以检查或更改焊接启动条件的详细信息。此外，如果有与相关条件文件关联的其他条件文件，您可以直接移动到它。换句话说，`[property]`按钮允许您快速轻松地检查和更改与特定语句（如条件文件或步骤位置）相关的内容的详细信息。

以下显示了使用`[property]`按钮检查和更改与特定命令相关的条件文件和详细信息的方法。

1. 选择一个特定的语句，将光标放在上面，然后触摸`[property]`按钮。

2. 参考下表，您可以检查和更改与所选语句相关的文件或详细信息。

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
        <p>当前步骤位置或全局姿态变量</p>
        <p>X Y Z (mm) Rx Ry Rz (deg) T1&#x2013;T10</p>
        <p>单位、坐标系和机器人配置</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">arcon asf=</td>
      <td style="text-align:left">
        <p>焊接启动条件</p>
        <p>焊接辅助条件</p>
        <p>弧焊机条件</p>
      </td>
      <td style="text-align:left">
        <ul>
          <li>焊接启动条件：条件编号、描述、电压检查、重试、操作模式、输出电流、输出电压、WCR等待时间、机器人延迟时间等。</li>
          <li>焊接辅助条件
            <ul>
              <li>重试：计数、回缩时间/速度、回退步骤/焊接线移动量、偏移移动量、速度、电流、电压</li>
              <li>重新启动：计数、重叠量、移动速度、焊接电流、电压、电流</li>
              <li>重叠条件设置（焊接中间）：弧、气体、焊丝和冷却液</li>
            </ul>
          </li>
          <li>弧焊机条件：焊机编号、标题、描述、电源控制模式、焊丝直径、突出距离、沉积检测时间、ARC OFF检测时间等。
            <ul>
              <li>电流特性：极性、指令值（V）、测量值（A）和补偿值</li>
              <li>电压特性：极性、指令值（V）、测量值（V）和补偿值</li>
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
          <li>焊接结束条件：条件编号、描述、电压检查、输出电流、输出电压、下坡、条件保持时间和气体后流</li>
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
          <li>弧感应条件：弧感应、左右感应启动周期、上下感应周期、电压因子、每个样本的补偿距离等。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

3. 触摸`[Record]`按钮或按`[ESC]`键以结束操作。

* `[Record]`：您可以保存更改并结束操作。
* `[ESC]`：您可以取消更改并结束操作。