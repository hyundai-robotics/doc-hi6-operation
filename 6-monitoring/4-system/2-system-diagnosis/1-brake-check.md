# 6.4.2.1 刹车诊断监测

在下面的按钮列表中触摸 [刹车诊断] 以显示刹车诊断数据屏幕。

![刹车诊断监测](../../../_assets/tp630/pane-sys-diagnosis-brake_eng.png)

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
      <p>显示在刹车保持/释放状态下施加扭矩时的当前角位移、最大角位移和参考角位移。</p> 
      <ul> 
        <li>当前角位移仅针对正在检查的轴显示。</li> 
        <li>当参考值设置模式激活时，轴名称会以黄色高亮显示。</li> 
      </ul> 
    </td> 
  </tr> 
<tr> 
  <td style="text-align:left"> <img src="../../../_assets/c2.png" alt/> </td> 
  <td style="text-align:left"> 
    <strong>[扭矩比]</strong>
    <p>显示在刹车诊断期间施加的扭矩比。</p> 
  </td> 
</tr> 
</tbody> 
</table>

{% hint style="info" %}

* 有关刹车诊断功能的更多详细信息，请参见 "${cont_model} 机器人控制器功能手册 - HRScript 机器人语言" 中的 "[10.1.16 brake_check](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/10-etc/1-proc/16-brake_check?cont_model=${cont_model})" 命令部分。

{% endhint %}