# 6.4.2.2 气弹簧压力诊断监测

在下面的按钮列表中触摸 [Gas Spring Diagnostics] 以显示气弹簧压力诊断数据屏幕。

![Gas spring pressure diagnostics](../../../_assets/tp630/pane-sys-diagnosis-gas-pressure_eng.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">No.</th>
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
          <li><strong>[Timestamp]</strong>: 显示气弹簧诊断测试执行的时间。</li>
          <li><strong>[Pressure]</strong>: 显示参考压力、容差和估计压力。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}

* 此功能仅在配备气弹簧的机器人上支持。  
* 估计的气弹簧压力可能会根据测量开始时的初始姿势而有所不同。
在机器人的初始设置过程中，请根据在每个参考姿势下进行的测量管理压力值，并定期在相同姿势下测量压力以与初始值进行比较。
如果测量值存在显著差异，请检查设备的状况。
*有关气弹簧诊断功能的更多详细信息，请参阅 "${cont_model} Robot Controller Function Manual - HRScript Robot Language" 中 "[10.1.7 gasp_check](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/10-etc/1-proc/7-gasp_check?cont_model=${cont_model})" 命令的章节。  

{% endhint %}