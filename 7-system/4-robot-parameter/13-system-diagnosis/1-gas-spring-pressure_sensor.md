# 7.4.13.1 气弹簧压力传感器

气弹簧压力传感器的功能用于通过模拟输入不断读取压力传感器的数值，检测气弹簧中的异常压力，或在使用气弹簧并附有我们公司指定的压力传感器 (PN2570) 的机器人中通过数字输入生成警告或错误。 <br> 

[数字输入]
![](../../../_assets/tp630/gasp_sensor.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">项目</th>
      <th style="text-align:left">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"> 
        警告输入
      </td>
      <td style="text-align:left">
        设置接收警告的信号号。当测量的压力超过设定容差时，压力传感器可以输出警告。当设置信号开启时，控制器生成 W21020。 
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        错误输入
      </td>
      <td style="text-align:left">
        设置接收警告的信号号。当测量的压力超过设定容差时，压力传感器可以输出警告。当设置信号开启时，控制器生成 E21020。 
      </td>
    </tr>
  </tbody>
</table>

<br>

[模拟输入]
![](../../../_assets/tp630/gasp_sensor2.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">项目</th>
      <th style="text-align:left">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        通信信号
      </td>
      <td style="text-align:left">
        设置传入压力传感器值的数字信号。
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        当前值
      </td>
      <td style="text-align:left">
        压力传感器测量的压力值显示。
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        参考值
      </td>
      <td style="text-align:left">
        设置注入气弹簧的参考压力。 
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        容差警告和输出信号
      </td>
      <td style="text-align:left">
        如果测量压力低于参考压力减去设定的警告容差值，则会出现警告 W21018。 <br>
        如果设置了输出信号，则信号输出将被打开。 
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        容差错误和输出信号
      </td>
      <td style="text-align:left">
        如果测量压力低于参考压力减去设定的错误容差值，则会出现错误 E21018。 <br>
        如果设置了输出信号，则信号输出将被打开。  
      </td>
    </tr>
  </tbody>
</table>

<br>

{% hint style="info" %}
* 此功能在版本 V60.30.07及之后的版本中受到支持。   
{% endhint %}