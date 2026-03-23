# 6.4.2.2 气弹簧压力诊断监测

在下面的按钮列表中触摸 [气弹簧诊断] 以显示气弹簧压力诊断数据屏幕。

![气弹簧压力诊断](../../../_assets/tp630/pane-sys-diagnosis-gas-pressure_eng.png)

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
      <td style="text-align:left">
        <p>显示最近五次气弹簧压力诊断的结果。</p>
        <ul>
          <li><strong>[时间戳]</strong>: 显示执行气弹簧诊断测试的时间。</li>
          <li><strong>[压力]</strong>: 显示参考压力、容差和估计压力。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}

* 此功能仅在配备气弹簧的机器人上支持。  
* 估计的气弹簧压力可能会根据测量开始时的初始姿态而有所不同。
在机器人初始设置时，请根据每个参考姿态的测量值管理压力值，并定期在相同姿态下测量压力以与初始值进行比较。
如果在测量值中观察到显著差异，请检查设备的状态。
* 有关气弹簧诊断功能的更多详细信息，请参考 "${cont_model} 机器人控制器功能手册 - HRScript 机器人语言"，部分 "[10.1.7 gasp_check](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/10-etc/1-proc/7-gasp_check?cont_model=${cont_model})" 命令。  

{% endhint %}