# 6.4.2.1 刹车诊断监测

点击下面按钮列表中的 [Brake Diagnostics] 以显示刹车诊断数据屏幕。

![Brake diagnostics monitoring](../../../_assets/tp630/pane-sys-diagnosis-brake_eng.png)

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
      <strong>[角位移]</strong>
      <p>在刹车保持/释放状态下，当施加扭矩时，显示当前角位移、最大角位移和参考角位移。</p> 
      <ul> 
        <li>仅在检查的轴上显示当前角位移。</li> 
        <li>当参考值设置模式处于激活状态时，轴名称会以黄色高亮显示。</li> 
      </ul> 
    </td> 
  </tr> 
<tr> 
  <td style="text-align:left"> <img src="../../../_assets/c2.png" alt/> </td> 
  <td style="text-align:left"> 
    <strong>[扭矩比]</strong>
    <p>显示在刹车诊断过程中施加的扭矩比。</p> 
  </td> 
</tr> 
</tbody> 
</table>

{% hint style="info" %}

* 有关刹车诊断功能的更多详细信息，请参阅 "${cont_model} Robot Controller Function Manual - HRScript Robot Language" 中 "[10.1.16 brake_check](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/10-etc/1-proc/16-brake_check?cont_model=${cont_model})" 命令的章节。

{% endhint %}