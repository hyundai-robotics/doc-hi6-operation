# 2.3.1 步骤语句参数

步骤语句参数是机器人步骤移动所需的运动条件，包括机器人位置、插值、速度、精度和工具编码号，以及移动指令。

步骤语句的参数分为默认参数和可选参数。默认参数是步骤所必需的基本参数，而可选参数是可以根据需要添加的参数。

步骤语句的配置如下。

![](../../../_assets/image_77.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">编号</th>
      <th style="text-align:left">参数</th>
      <th style="text-align:left">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">插值</td>
      <td style="text-align:left">
        <p>步骤之间的插值路径</p>
        <p>P（关节插值）、L（线性插值）、C（圆形插值）、 
          SP（ stationary tool interpolation off），SL（静止工具线性插值），
          SC（静止工具圆形插值）</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">姿态</td>
      <td style="text-align:left">
        <p>用于记录位置的参数。此参数可以省略，并且可以在语句后指定一个姿态（隐藏姿态）。</p>
        <p>目标姿态（X，Y，Z，Rx，Ry，Rz，Cfg）{坐标系统} + 偏移（X，
          Y，Z，Rx，Ry，Rz）{坐标系统}</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">速度</td>
      <td style="text-align:left">机器人操作速度 （单位：mm/sec, cm/min, %, sec）</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">精度</td>
      <td style="text-align:left">当前位与记录位之间的误差允许值（0–7），当机器人移动到目标步骤时发生</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">工具编号</td>
      <td style="text-align:left">正在使用的工具编号（0–31）</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">赋值语句</td>
      <td style="text-align:left">在移动开始时，每个赋值语句从左到右依次执行</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left">停止条件</td>
      <td style="text-align:left">机器人停止移动以执行下一个命令（步骤或功能）的条件</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c8.png" alt/>
      </td>
      <td style="text-align:left">注释</td>
      <td style="text-align:left">步骤的描述</td>
    </tr>
  </tbody>
</table>