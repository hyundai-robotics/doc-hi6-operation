
[__SOURCE](README.md)
# ${cont_model} 控制器操作手册 - TP630
[__SOURCE](0-about-this-manual/README.md)
# 关于手册

本手册描述了HD Hyundai Robotics的 ${cont_model} 控制器的基础知识和结构，以及工业机器人的常见操作。每一章不仅描述了基本操作方法，还描述了使用各种应用功能的方法。

本手册不涵盖详细的应用功能，例如使用协作机器人进行直接教学、安全功能设置方法、点焊、弧焊、定位器同步功能和传感器同步功能。有关相关信息的详细信息，请参阅协作机器人维护手册和各个应用功能手册。

[__SOURCE](0-about-this-manual/precautions.md)
# 注意事项

{% include file="zh/precautions.md" %}
[__SOURCE](0-about-this-manual/notation.md)
# 符号约定

在本手册中，使用以下符号约定和安全说明来帮助您理解内容。

### 图形描述

图形用于帮助您理解如何操作产品，并说明您在屏幕上可以看到的内容。图形描述中，相关部分将用数字标记，对应内容将如下描述。

![](../_assets/tp630/pane-prog-cmd-param.png)

### GUI \(图形用户界面\)

在GUI中，菜单名称和按钮名称用方括号括起，并以浅色背景显示。
当多个菜单必须依次选择时，它们的名称用连字符 (-) 分隔。

* 单个菜单：在手动或自动模式的初始屏幕上，触摸`[F1: 服务] ([F1: Service])`W按钮。
* 多个菜单：在手动模式的初始屏幕上，触摸`[F2: 系统] - 5: 初始化 - 6: 机构设置 ([F2: System] - 5: Initialization - 6: Mechanism setting)`。

### 操作键的符号方法

在教师挂件的操作部分按下的键将用方括号括起，并以浅色背景显示。

* 如果您按下`[Start]`键，机器人中创建的程序的自动操作将开始。

### 交叉引用

它提供了手册内相关信息的快捷方式。交叉引用将以双引号（" "）显示，如下所示。

* 有关如何更改日期和时间信息的详细信息，请参阅"[4.5 设置日期和时间.](../4-service/5-date-time-setting.md)"。

### 注意

本节包含一些在使用产品时可能有用的提示或附加信息，如下所示。

{% hint style="info" %}
当 ![](../_assets/eng-mode.png) 图标在状态栏中闪烁时，这意味着您处于工程师模式。
{% endhint %}
[__SOURCE](0-about-this-manual/safety-notice.md)
# 安全注意事项

{% include file="zh/safety-notice.md" %}

[__SOURCE](1-robot-system/README.md)
# 1. 机器人系统
[__SOURCE](1-robot-system/1-basic-constitution/README.md)
# 1.1 基础配置

工业机器人是“配备了基于自动控制的操作和移动功能的机器，以便它们能在工业现场通过使用程序执行各种工作”。协作机器人是一种工业机器人。

机器人系统由一个执行器和一个控制器组成，控制器控制执行器。用于设置和手动操作机器人系统的示教器附加在控制器上。

* 机器人：在工业现场执行各种工作，如运输物体、组装零件等。
* 控制器：根据通过示教器设置的程序设定值调整机器人的操作。它可以通过控制器的输入/输出端口与各种外部设备或装置进行互操作。
* 示教器：管理整个机器人系统的设备。它使您能够教导机器人特定的姿势或设置并控制程序。

以下展示了根据机器人类型的机器人系统的基本配置示例。

![Figure 1 基础配置的LCD机器人系统](../../_assets/image_286.png)

![Figure 2 基础配置的垂直关节机器人系统](../../_assets/image_285.png)
[__SOURCE](1-robot-system/1-basic-constitution/1-controller.md)
# 1.1.1 控制器

#### 垂直关节机器人控制器 

![图4 控制器的前面（左）/ 背面（右）](../../_assets/image_33.png)

| No. | 名称 | 描述 |
| :--- | :--- | :--- |
| ![](../../_assets/c1.png)  | 连接部分 | 用于将仪器和教学挂件连接到控制器或将应用设备连接到内部模块的通道 |
| ![](../../_assets/c2.png)  | 电源开关 | 打开或关闭控制器的电源 |
| ![](../../_assets/c3.png)  | 存放TP的挂钩 | 用于悬挂教学挂件或存放它 |
| ![](../../_assets/c4.png)  | 紧急停止开关 | 在紧急情况下按下时导致机器人停止操作 |
| ![](../../_assets/c5.png)  | 冷却风扇 | 强制排出控制器内部加热空气的设备 |
[__SOURCE](1-robot-system/1-basic-constitution/2-teach-pendant.md)
# 1.1.2 教学挂件

本操作手册描述了如何使用基于TP630型号的教学挂件。TP630是专为${cont_model}控制器开发的型号，提供了一个大触摸屏。

![](../../_assets/tp630/TP-hw.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">编号</th>
      <th style="text-align:left">名称</th>
      <th style="text-align:left">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">操作键</td>
      <td style="text-align:left">控制机器人的操作、输入命令或选择菜单</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">模式切换开关</td>
      <td style="text-align:left">你可以旋转模式切换开关选择
  操作模式 (
        <img src="../../_assets/sb-manual.png" alt/>手动/
        <img src="../../_assets/sb-auto.png" alt/>自动/
        <img src="../../_assets/sb-remote.png" alt/>遥控)。如果你将模式
  切换开关从教学挂件上移除，所选的操作模式将被锁定。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">显示屏</td>
      <td style="text-align:left">触摸屏可让你检查和
  更改操作状态以及设置机器人的信息。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">紧急停止开关</td>
      <td style="text-align:left">在紧急情况下按下时会导致机器人停止操作</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">USB连接端口</td>
      <td style="text-align:left">可以用于连接可以通过USB通信访问的设备，例如可移动存储设备<br>
      请使用FAT32格式。请注意不支持exFAT、NTFS格式。
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">安装支架</td>
      <td style="text-align:left">用来固定或悬挂教学挂件以便存放</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left">启用开关</td>
      <td
      style="text-align:left">
        <p>用于在手动模式下使用教学挂件操作机器人时作为安全开关的开关</p>
        <ul>
          <li>阶段
       1，阶段 3：机器人操作将停止。在第3阶段的情况下，开关将
       直接恢复到第1阶段，而不经过第2阶段。</li>
          <li>阶段 2：你可以操作机器人。</li>
        </ul>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c8.png" alt/>
      </td>
      <td style="text-align:left">电缆连接连接器</td>
      <td
      style="text-align:left">用于将电缆连接到控制器的连接器</td>
    </tr>
  </tbody>
</table>

<br>

#### 操作键 </span></p>

<table class=MsoNormalTable border=0 cellpadding=0 style='mso-cellspacing:1.5pt;
 mso-yfti-tbllook:1184'>
 <thead>
  <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes'>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal><b><span lang=EN-US>操作键<o:p></o:p></span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal><b><span lang=EN-US>名称<o:p></o:p></span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal><b><span lang=EN-US>描述<o:p></o:p></span></b></p>
   </td>
  </tr>
 </thead>
 <tr style='mso-yfti-irow:1'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=52 height=49 id="_x0000_i1042" src="../../_assets/tp630/k-shift_eng.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>SHIFT</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>当你想执行显示在按键顶部的功能（蓝绿色）时，必须使用此按钮。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l3 level1 lfo2;tab-stops:list 36.0pt'><span lang=EN-US>当按下此键与[快速向前/
       向后]功能一起操作时，可以以高速激活向前/ 向后步骤</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l3 level1 lfo2;tab-stops:list 36.0pt'><span lang=EN-US>在 输入显示窗口编辑字符串时，你可以通过按带有`[←/→]`键的按钮移动光标。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l3 level1 lfo2;tab-stops:list 36.0pt'><span lang=EN-US>在任务编辑窗口中，你可以通过按带有`[↑/↓]`键的按钮按每个屏幕移动光标。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=47 height=48 id="_x0000_i1041" src="../../_assets/tp630/k-ctrl_eng.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>CTRL</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>特定功能只能通过`[CTRL]`键执行。</span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:3'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=73 height=75 id="_x0000_i1040"
  src="../../_assets/tp630/k-bwd-fwd_eng.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>步进前/后</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>在手动模式下逐步向前或向后使用。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l5 level1 lfo3;tab-stops:list 36.0pt'><span lang=EN-US>查看`[cond.set] - 步进前/后最大速度`以获取详细描述。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l5 level1 lfo3;tab-stops:list 36.0pt'><span lang=EN-US>当按下此键与`[SHIFT]`时，可以激活快速步进
       向前/ 向后功能。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:4'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=47 height=46 id="_x0000_i1039" src="../../_assets/tp630/k-esc_eng.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>ESC</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于取消按键输入或各种正在进行的功能。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l11 level1 lfo4;tab-stops:list 36.0pt'><span lang=EN-US>此键还具有返回上一级而不保存的功能。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:5'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=160 height=162 id="_x0000_i1038"
  src="../../_assets/tp630/k-axes_eng.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>轴操作</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>根据坐标系统用于机器人操作。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l12 level1 lfo5;tab-stops:list 36.0pt'><span lang=EN-US>每个
       轴在关节坐标系统中移动。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l12 level1 lfo5;tab-stops:list 36.0pt'><span lang=EN-US>机器人在机器人坐标系统中以矩形方向移动。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:6'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=104 height=101 id="_x0000_i1037"
  src="../../_assets/tp630/k-direction_eng.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>方向</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于在TP面板上移动光标。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l1 level1 lfo6;tab-stops:list 36.0pt'><span lang=EN-US>`[↑/↓]`
       键移动步骤和功能。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l1 level1 lfo6;tab-stops:list 36.0pt'><span lang=EN-US>`[←/→]`
       键移动录制步骤或功能的参数。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:7'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=53 height=56 id="_x0000_i1036" src="../../_assets/tp630/k-r.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>R-代码</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于快速执行已注册的功能。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l14 level1 lfo7;tab-stops:list 36.0pt'><span lang=EN-US>按下
       R-代码键会弹出一个输入代码编号的窗口。更多信息，请参阅“8. R代码”。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l14 level1 lfo7;tab-stops:list 36.0pt'><span lang=EN-US>没有代码编号的R-代码键后跟`[ENTER]`与“R0 : 步数计数器重置”相同。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l14 level1 lfo7;tab-stops:list 36.0pt'><span lang=EN-US>在是非问题中，按下R-代码表示否定答案。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:8'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=51 height=51 id="_x0000_i1035" src="../../_assets/tp630/k-enter.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>输入</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于反映输入数据。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l6 level1 lfo8;tab-stops:list 36.0pt'><span lang=EN-US>如果使用此键完成数字输入，则输入框的内容会反映在编辑框上。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l6 level1 lfo8;tab-stops:list 36.0pt'><span lang=EN-US>当选择许可（是）作为许可/拒绝（是/否）的响应时，此键也可以使用。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l6 level1 lfo8;tab-stops:list 36.0pt'><span lang=EN-US>当你按下此键时，句子光标会切换到单词光标，可以编辑参数。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:9'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=101 height=48 id="_x0000_i1034" src="../../_assets/tp630/k-motor-on.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>电机开启</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于为每个轴的电机提供伺服电源。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l4 level1 lfo9;tab-stops:list 36.0pt'><span lang=EN-US>[MOTOR ON]灯在手动模式下闪烁。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l4 level1 lfo9;tab-stops:list 36.0pt'><span lang=EN-US>[MOTOR ON]灯在自动模式下点亮。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:10'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=102 height=48 id="_x0000_i1033" src="../../_assets/tp630/k-start.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>开始</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于自动播放作业程序。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l15 level1 lfo10;tab-stops:list 36.0pt'><span lang=EN-US>在模式切换在AUTO条件下，且电机打开的情况下，<START>键将自动播放作业程序。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l15 level1 lfo10;tab-stops:list 36.0pt'><span lang=EN-US>如果机器人的自动操作启动，[START]灯亮起，[STOP]灯熄灭。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:11'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=103 height=46 id="_x0000_i1032" src="../../_assets/tp630/k-stop.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>停止</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于在自动操作期间暂时停止机器人。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l2 level1 lfo11;tab-stops:list 36.0pt'><span lang=EN-US>如果机器人停止，[STOP]灯亮起，[START]灯熄灭。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l2 level1 lfo11;tab-stops:list 36.0pt'><span lang=EN-US>当机器人停止时，不会有与其他设备碰撞的风险，因为它停留在原定路径上。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:12'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=45 height=44 id="_x0000_i1031"
  src="../../_assets/tp630/k-previous_eng.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>历史</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于查看之前的工作历史。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l17 level1 lfo12;tab-stops:list 36.0pt'><span lang=EN-US>这会显示记录执行历史、错误历史、信息历史等任务命令的历史消息框。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l17 level1 lfo12;tab-stops:list 36.0pt'><span lang=EN-US>当你按一次时，它显示主板的输出历史，再按一次时，显示教学挂件的输出历史。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:13'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=53 height=52 id="_x0000_i1030" src="../../_assets/tp630/k-gun.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>枪</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于点焊和弧焊应用，LED显示开关状态。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l13 level1 lfo13;tab-stops:list 36.0pt'><span lang=EN-US>当你按下这个按钮与[SHIFT (FAST)]键时，GUN1信号将手动输出。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l13 level1 lfo13;tab-stops:list 36.0pt'><span lang=EN-US>在点焊的情况下，当你按下`[REC]`键时，SPOT命令会自动跟随MOVE。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l13 level1 lfo13;tab-stops:list 36.0pt'><span lang=EN-US>当这个LED在使用弧焊的自动操作中点亮时，机器人将实际执行弧焊。当这个LED熄灭时，不会执行弧焊，只会检查教导的轨迹。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:14'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=45 height=47 id="_x0000_i1029"
  src="../../_assets/tp630/k-crdsys_eng.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>工具 / 坐标</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于选择参考坐标系。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l16 level1 lfo14;tab-stops:list 36.0pt'><span lang=EN-US>按下轴操作键时，可以选择坐标系（轴、笛卡尔、工具）以移动机器人。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l16 level1 lfo14;tab-stops:list 36.0pt'><span lang=EN-US>当按下`[SHIFT]`键时，将打开选择工具编号的消息框。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:15'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=44 height=44 id="_x0000_i1028"
  src="../../_assets/tp630/k-record_eng.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>位置模式 / 记录</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于在程序中记录步骤，即添加MOVE命令时。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l9 level1 lfo15;tab-stops:list 36.0pt'><span lang=EN-US>通过此键插入的MOVE命令包含隐藏姿态。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l9 level1 lfo15;tab-stops:list 36.0pt'><span lang=EN-US>当光标在某个步骤上时，可以插入下一步。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l9 level1 lfo15;tab-stops:list 36.0pt'><span lang=EN-US>可以通过按`[SHIFT]`键修改所选步骤位置。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:16'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=45 height=44 id="_x0000_i1027"
  src="../../_assets/tp630/k-prog-step_eng.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>程序 / 步骤</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于选择步骤。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l8 level1 lfo16;tab-stops:list 36.0pt'><span lang=EN-US>使用`[SHIFT]`键时，此键会弹出作业程序窗口。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l8 level1 lfo16;tab-stops:list 36.0pt'><span lang=EN-US>当你按两次[PROG]键时，程序列表将显示。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:17'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=44 height=46 id="_x0000_i1026"
  src="../../_assets/tp630/k-unit-mech_eng.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>机制</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于选择机制和单元。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l7 level1 lfo17;tab-stops:list 36.0pt'><span lang=EN-US>对于机制，机器人是0，对于附加轴，它遵循用户在初始设置菜单中设置的设置。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l7 level1 lfo17;tab-stops:list 36.0pt'><span lang=EN-US>当按下此按钮与SHIFT键时，你可以将此按钮用于单元。在用户想要配置程序时，单元用于特定单位的组合。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:18;mso-yfti-lastrow:yes'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=139 height=183 id="_x0000_i1025"
  src="../../_assets/tp630/k-number_eng.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>数字键</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于输入数字或删除。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l0 level1 lfo18;tab-stops:list 36.0pt'><span lang=EN-US>使用`[SHIFT]`键，你可以输入'+'和'-'符号或删除
       一条命令句子或参数。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l0 level1 lfo18;tab-stops:list 36.0pt'><span lang=EN-US>`[BS]`
       键逐个字符向后删除。（退格键）。此外，当编辑命令句子时，所有参数值都被删除。</span></li>
  </ul>
  </td>
 </tr>
</table>

[__SOURCE](1-robot-system/2-basic-usage/README.md)
# 1.2    基本使用
[__SOURCE](1-robot-system/2-basic-usage/1-power-on/README.md)
# 1.2.1 开启电源

{% hint style="info" %}
开启和关闭电源的方法可能会根据控制器的类型而有所不同。
{% endhint %}

#### 直立关节机器人控制器

要启动机器人，必须为机器人控制器供电。

将机器人控制器左侧的电源开关转向ON方向，以连接控制器的主电源。 当电源连接后，机器人系统将启动，教学挂件的显示屏将与所有设备一起开启。

![](../../../_assets/image_12.png)
[__SOURCE](1-robot-system/2-basic-usage/1-power-on/1-input-of-the-power-to-the-mot.md)
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
[__SOURCE](1-robot-system/2-basic-usage/2-power-off.md)
# 1.2.2 关闭电源

它指的是在完成所有工作后停止机器人并关闭控制器的电源按钮的所有操作。

{% hint style="warning" %}
* 如果机器人长时间不使用，编码器电池可能会放电，因此请将机器人移动到参考位置，然后关闭电源。

* 请小心，如果在编码器电池有电压下降警报时关闭电源，编码器数据可能会被破坏。 
{% endhint %}

#### 垂直关节机器人控制器

1.	按下教学挂件上的 `[Stop]` 键。然后，正在操作的机器人将停止，停止灯将亮起。

2.	按下教学挂件上的紧急停止开关。然后，机器人电机的伺服电源将被切断，然后电机将关闭。

![](../../_assets/image_36.png)

3.	将机器人控制器左侧的电源开关拨向 OFF 方向。然后，机器人系统将断电。

![](../../_assets/image_29.png)
[__SOURCE](1-robot-system/2-basic-usage/3-change-language-of-tp.md)
# 1.2.3 更改教导挂件屏幕的语言

如果您需要更改教导挂件的语言，可以使用以下步骤进行更改。以下是将英语更改为韩语模式的示例。

### A. 通过教导挂件选项更改（仅在 V70.00-00 及以上版本中支持）

1. 单击 `[F1: 服务] ([F1: service])` 按钮。

    ![](../../_assets/tp630/service/fb-service.png)

2. 输入 `11: 教导挂件选项`。

    ![](../../_assets/tp630/service/menu-tp-option.png)

3. 从语言设置中选择 `韩语`。

    ![](../../_assets/tp630/service/tp-option-lang.png)

4. 按 `[ESC]` 键返回到顶层 HOME 屏幕，然后稍等片刻。

<br>

### B. 在关闭教导挂件软件后更改

1. 单击 `[F1: 服务] ([F1: service])` 按钮。

   ![](../../_assets/tp630/service/fb-service.png)

2. 选择 9: 退出 TP 应用程序。

    ![](../../_assets/tp630/service/exit-application.png)

3. 单击左下角的语言组合框。

    ![](../../_assets/tp630/service/autorun-sub-lang.png)

    {% hint style="info" %}

    对于 V60.32-00 以下版本，请单击右上角的地球图标。

    ![](../../_assets/tp630/service/autorun-sub-lang-old.png)

    {% endhint %}

4. 从弹出菜单中选择 `英语`。

5. 单击右下角的 `[run TP]` 按钮，等待大约 15 秒。
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/README.md)
# 1.2.4 ${cont_model} 教学挂件的屏幕

下图表示教学挂件上显示的屏幕。${cont_model} 控制器的教学挂件屏幕由 10 个彩色触摸屏窗口组成。
<br>

![](../../../_assets/tp630/TP-main_eng.png)

| No. | Description | 
| :--- | :--- | 
| ![](../../../_assets/c1.png) | 标题显示窗口：TP 通信、机器人系统、机械等的各种状态图标。 ([1.2.3.1 标题显示窗口](1-title-area.md)) |
| ![](../../../_assets/c2.png) | 状态显示窗口：操作模式和设置 ([1.2.3.2 状态显示窗口](2-status-bar.md)) |
| ![](../../../_assets/c3.png) | R 按钮栏：主屏幕右侧的菜单组 ([1.2.3.3 R 按钮栏](3-Rbt-bar.md)) |
| ![](../../../_assets/c4.png) | 监视窗口：操作期间的运行数据 ([1.2.3.4 监视窗口](4-mon-area.md)) |
| ![](../../../_assets/c5.png) | 功能按钮栏：主屏幕底部的菜单组，支持主要设置和监控 ([1.2.3.5 功能按钮栏](5-function-buttons.md)) |
| ![](../../../_assets/c6.png) | 输入显示窗口：任务编辑窗口的直接输入区域 ([1.2.3.6 输入显示窗口](6-input-area.md)) |
| ![](../../../_assets/c7.png) | 引导显示窗口：操作期间的引导信息 ([1.2.3.7 引导显示窗口](7-guide-area.md)) |
| ![](../../../_assets/c8.png) | 任务编辑窗口：编辑 JOB 程序的区域 ([1.2.3.8 任务编辑窗口](8-work-area.md)) |
| ![](../../../_assets/c9.png) | 记录条件显示窗口：记录步骤的条件 ([1.2.3.9 记录条件显示窗口](9-record-cnd-area.md)) |
| ![](../../../_assets/c10.png) | L 按钮栏：主屏幕左侧的菜单组 ([1.2.3.10 L 按钮栏](10-Lbt-bar.md)) |
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/1-title-area.md)
# 1.2.4.1	标题显示窗口

此窗口在主屏幕的顶部显示机器人系统的状态。

<br>


![](../../../_assets/tp630/TP-main-title.png)


| No. | 描述 | 
| :--- | :--- | 
| ![](../../../_assets/c1.png) | 显示网络状态。 (![](../../../_assets/flag-comm-ok.png) : 已连接, ![](../../../_assets/flag-comm-ng.png) : 未连接)|
| ![](../../../_assets/c2.png) | 在插入USB存储设备时显示图标。 |
| ![](../../../_assets/c3.png) | 显示连续路径（CONTPATH）模式。 (CP# : CP(连续路径)+模式编号) <br> (参考: [R360](../../../8-r-code/15-r360.md?cont_model=${cont_model})) |
| ![](../../../_assets/c4.png) | 显示每个应用功能的当前状态。 (SW : 焊接记录状态, PBk : 喷涂部分) |
| ![](../../../_assets/c5.png) | 显示定位器同步状态。 (M:S{站点编号}) |
| ![](../../../_assets/c6.png) | 显示协作控制状态。 (I:独立, M:主控, S:从控) |
| ![](../../../_assets/c7.png) | 显示轴控制状态。 (如果关闭则显示 j_{轴编号}) |
| ![](../../../_assets/c8.png) | 显示轴锁定状态。 |
| ![](../../../_assets/c9.png) | 显示编码器电池错误状态。 (出现错误时闪烁) |
| ![](../../../_assets/c10.png) | 显示减速器寿命错误状态。 (出现错误时显示并闪烁轴编号) |
| ![](../../../_assets/c11.png) | 显示用户级别。 (E : 工程师模式) <br> (参考: [R314](../../../8-r-code/12-r314.md?cont_model=${cont_model})) |
| ![](../../../_assets/c12.png) | 显示PLC操作状态。 |
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/2-status-bar.md)
# 1.2.4.2 状态显示窗口

此部分显示机器人的各种操作状态。您可以通过触摸每个适用的部分来设置显示的信息。

![](../../../_assets/tp630/TP-main-status_eng.png)

| No. | Description | 
| :--- | :--- |
| ![](../../../_assets/c1.png) | 机器人的操作模式显示。<li>手动：用于手动操作和编辑JOB程序的模式</li> <li>自动：用于自动运行JOB程序的模式</li> <li>远程手动：通过I/O信号远程设置手动或自动模式的模式（当前状态：手动模式）</li> <li>远程自动：通过I/O信号远程设置手动或自动模式的模式（当前状态：自动模式）</li> |
| ![](../../../_assets/c2.png) | 您可以检查当前工具信息并在弹出消息框中更改它。|
| ![](../../../_assets/c3.png) | 机制显示所选附加轴的机器人类型或编号。机器人为0，用户请参考 `系统 - 5: 初始化 - 6: 机构设置 (System - 5: Initialize - 6: Mechanism setting)`。 |
| ![](../../../_assets/c4.png) | 这显示为手动操作选择的参考坐标系统的状态。状态显示为“关节”、“用户”、“机器人”或“工具”，每次按下状态窗口时依次变化。使用`[轴操作]`键，您可以根据参考坐标系统移动机器人。 <li>关节坐标系统：机器人的每个轴将根据`[轴操作]`键的下部名称独立移动。</li> <li>机器人坐标系统：机器人TCP基于机器人坐标系统通过`[轴操作]`键进行平移和旋转。</li> <li>用户坐标系统：机器人TCP基于用户坐标系统通过`[轴操作]`键进行平移和旋转。</li> <li><img src="../../../_assets/bt-crd-tool (1) (1) (2).png" alt/>工具坐标系统：机器人TCP基于工具坐标系统通过`[轴操作]`键进行平移和旋转。</li> |
| ![](../../../_assets/c5.png) | 确定在手动模式下操作机器人的速度。在手动模式中，有两种不同类型的操作。一种是手动运行，另一种是向前/向后逐步操作。在手动操作的速度等级中有8个不同的步骤（1~8）。<li>按下教学挂架的速度HI键时，速度等级增加一步；按下速度LOW键时，速度等级降低一步。如果同时按下[SHIFT (FAST)] + 速度HI键，速度等级设置为8；如果同时按下[SHIFT (FAST)] + 速度LOW键，速度等级设置为1。</li> |
| ![](../../../_assets/c6.png) | 显示日期和时间信息。<br>您可以在[服务 - 8：日期、时间设置]菜单中更改此设置。 ([4.5 日期和时间设置](../../../4-service/5-date-time-setting.md))|
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/3-Rbt-bar.md)
# 1.2.4.3 R(Right) 按钮条

5 个按钮显示在屏幕右侧，您可以触摸这些按钮。未激活的按钮将变为灰色。在自动模式下，“prev/next”被禁用，这使得无法使用这些功能。

![](../../../_assets/tp630/TP-main-rbt_eng.png)

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
        <p>此按钮用于手动输出通用输出、现场总线输出等或手动设置参数值。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>此按钮将拆分监控窗口或合并拆分窗口。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <p>此按钮用于编辑命令句或注释。作为触摸屏，使用方式与键盘相同。</p>
        <p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p>此按钮用于在 F 按钮条中定义和使用用户键。</p>
        <p>预设功能用于点焊或弧焊。如需更多信息，请参阅应用手册。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">
        <p>此按钮用于移动到功能按钮条的下一页。</p>
        <p>当当前屏幕中有超过 7 个按钮时，该按钮将被激活，每次按下此按钮时，它将切换到下一个按钮组。当您按下`[SHIFT]` + 该按钮时，它将向后切换。
      </td>
    </tr>
    </tr>
  </tbody>
</table>
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/4-mon-area.md)
# 1.2.4.4 监视窗口

这是一个用于实时显示每个应用程序每个轴的位置数据、I/O 数据和状态数据的窗口。将主屏幕分割并选择一个监视面板。您可以最多拥有 3 个监视面板。 (请参阅 "[6. Monitoring](../../../6-monitoring/README.md)"。)

<br>

![](../../../_assets/tp630/TP-main-mon_eng.png)
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/5-function-buttons.md)
# 1.2.4.5 功能按钮栏

7 个功能按钮显示在主窗口的底部。功能按钮根据当前操作屏幕而变化。例如，在最高级别的屏幕中，显示进入服务菜单和系统菜单的按钮。此外，在编辑任务程序时，显示命令列表或命令参数设置的按钮。

![](../../../_assets/tp630/TP-main-functions_eng.png)

| No. | 描述 | 
| :--- | :--- | 
| ![](../../../_assets/c1.png) | service : 各种便利项目，例如监视、变量和文件管理器 ([4.Service](../../../4-service/README.md)) |
| ![](../../../_assets/c2.png) | system : 机器人操作和应用的详细设置 ([7.System](../../../7-system/README.md)) |
| ![](../../../_assets/c3.png) | rel.WAIT : 通过按 `[SHIFT]` 键释放信号等待，例如输入信号或焊接完成信号 (前提条件 : `[F2: 系统] - 1: 用户环境 - 'Wait(di/wi) release' - 禁用 ([F2: system] - 1: User environment - 'Wait(di/wi) release' - Disable)`) |
| ![](../../../_assets/c4.png) | log : 错误或警告历史，包括错误代码、通知消息、错误发生时间等 ([2.5.2 Error Handling](../../../2-operation/5-error-info/2-error-handle.md)) |
| ![](../../../_assets/c5.png) | cmd.input : 显示在手动模式的初始页面，用于输入程序命令 ([3.2.2.1 Statements](../../../3-programming/2-prog-edit/1-statement.md)) |
| ![](../../../_assets/c6.png) | cond.set : 机器人操作条件，例如前进/后退的机器人速度和路径恢复 ([5.Condition Setting](../../../5-conditional-setting/README.md)) |
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/6-input-area.md)
# 1.2.4.6 输入显示窗口

此区域显示要编辑的内容的输入值，如命令语言、字符或功能。您可以通过 [cmd.input] 按钮直接插入命令，而无需选择命令。如果输入未定义的命令或语法不正确，将会发生以下错误。

![](../../../_assets/tp630/pop-error-nocmd_eng.png)

<br>

下面的表格是 'move' 命令的每个参数的输入。
<br>

|command parameters|inputs |
|--|--|
|![](../../../_assets/tp630/pane-prog-mov-argument.png)|![](../../../_assets/tp630/TP-main-input.png)|
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/7-guide-area.md)
# 1.2.4.7 指南显示窗口

此窗口显示用户操作的指南或方向消息，并且是当在“打印”命令中设置打印方向为 T/P 时显示打印消息的区域。

<br>

下表为“移动”命令每个参数的指南消息。

<br>

|command parameters|guide messages|
|--|--|
|![](../../../_assets/tp630/pane-prog-mov-argument.png)|![](../../../_assets/tp630/TP-main-guide.png)|
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/8-work-area.md)
# 1.2.4.8 任务编辑窗口

这是编辑程序的窗口。有关程序编辑，请参阅
"[3. 程序编写](../../../3-programming/README.md)"。

<br>

![](../../../_assets/tp630/pane-job-area.png)



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
        选定的 JOB 程序的名称
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p> JOB 程序的步骤和功能编号</p>
        <ul>
          <li>P101 : 当前 JOB 程序的编号</li>
          <li>S3 : 当前选定行的步骤编号</li>
          <li>F1 : 当前选定行的功能编号</li>
        </ul>
      </td>
    </tr>
    <tr>
    </tr>
  </tbody>
</table>

当您尝试编辑程序时，由于文件的属性可能会发生以下错误。有关文件属性，请参阅 "[4.2.4 文件保护](../../../4-service/2-file-manager/4-file-protect.md)"。

![](../../../_assets/tp630/pop-error-fileprotect_eng.png)
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/9-record-cnd-area.md)
# 1.2.4.9 记录条件显示窗口

这是编辑记录步骤条件的窗口（速度、准确性、工具选项等）。请按下 [rec.cond] <img src="../../../_assets/tp630/lbt-record_eng.png" width="35mm"></img> 在 L 按钮栏中进行编辑。有关更多详细信息，请参阅 "[3.2.2.3 记录条件](../../../3-programming/2-prog-edit/2-statement-input/3-rec-cond.md)"。

<br>

![](../../../_assets/tp630/TP-main-recordcnd.png)
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/10-Lbt-bar.md)
# 1.2.4.10 L(Left) button bar

5 个按钮显示在屏幕的左侧，您可以触摸这些按钮。非活动按钮将显示为灰色。在自动模式下，记录条件、慢速移动功能被禁用，因此无法使用这些功能。

<br>

![](../../../_assets/tp630/TP-main-lbt_eng.png)

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
        <p>这是用于编辑记录步骤的条件，包括速度、精度、工具编号、步骤选项等的键。编辑在记录条件窗口中进行。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>选择在向前/向后移动步骤时是否逐步执行或以功能执行，或者是否连续执行直到任务程序结束。目前选定的条件在按钮上以图标显示。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <p>这是您希望以指定量手动移动机器人时在微调级别使用的键。当 jog inching 功能被激活时，绿色指示灯会亮起。</p>
        <p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p>如果在光标放置于某个命令句时按下此键，将执行与该命令句相关的快速打开功能。详细描述请参见快速打开。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">
        <p>根据每个状态显示相关的帮助。如果在光标存在于命令句时按下此键，将显示命令句的语法形式。在发生错误时，您可以通过按下此键查看内容、措施或诊断方法。</p>
      </td>
    </tr>
    </tr>
  </tbody>
</table>
[__SOURCE](2-operation/README.md)
# 2. 操作

操作是指将工作的内容指示给机器人并检查其内容的行为。一般而言，在工业机器人中，使用手动和自动模式。手动操作是指直接将工作的内容指示给机器人的行为，而自动操作是指让机器人重复执行所指示工作的内容。
[__SOURCE](2-operation/1-manual-operation/README.md)
# 2.1 手动操作

手动操作是一种以安全速度直接教导和检查机器人的操作方法。
[__SOURCE](2-operation/1-manual-operation/1-how-to-op.md)
# 2.1.1 操作方法

使用 jog 键指示工作的内容并检查所指示工作的内容的方法如下。

1.	检查安全围栏和机器人的操作范围内是否有人或障碍物。

2.	通过切换教导盒的模式开关将操作模式设置为手动模式。

    ![](../../_assets/tp630/TP-hw-switch-manual.png)

3.	在 ${cont_model} 教导盒屏幕的状态栏中，检查操作模式是否设置为手动模式。

    ![](../../_assets/tp630/sbar-mode_eng.png)

    * 如果设置为自动模式，则通过切换教导盒的模式开关将操作模式设置为手动模式。

4.	同时按下 `[PROG]` 键和 `[SHIFT]`。然后，程序选择窗口将会出现。

    ![](../../_assets/tp630/k-prog-step_eng.png)

5.	从程序选择窗口中的列表中选择一个程序或输入程序编号，然后按 `[ENTER]` 键。

    ![](../../_assets/tp630/k-prg-select_eng.png)

6.	按下教导盒上的 `[motor]` 键。然后，马达指示灯将闪烁，伺服电源将准备供电给机器人每个轴的马达。

7.	按下教导盒背面的启用开关。然后，马达指示灯将点亮，马达刹车将释放，允许伺服电源供电。机器人将准备移动。

8.	根据坐标系统的速度等级或运动条件使用 jog 键操作机器人。

    * 要保存机器人的位置，请在所需位置触碰 `[REC]` 键。然后，该步骤将被记录。
    * 要记录该步骤所需的功能，请触碰 `[cmd.input]` 按钮。
    * 要在手动向前或向后移动时检查机器人的位置，请按 `[STEP.FWD/STEP.BWD]` 键。在按下 `[STEP.FWD/STEP.BWD]` 键时，机器人将按步移动。当机器人到达目标步时，执行完成标记 \( . \) 将出现在命令前面，然后机器人将停止。
[__SOURCE](2-operation/1-manual-operation/2-op-speed.md)
# 2.1.2 操作速度调整

在手动模式下，您可以使用向前/向后操作和手动滑动操作来操作机器人。当前速度设置在状态显示窗口的速度窗口中显示。

![](../../_assets/tp630/sbar-spd-manual_eng.png)

'Man. spd'仅用于手动模式，在自动模式中被'Play spd'替代。速度窗口底部的数字'1'表示滑动速度级别，'200mm/s'表示向前/向后的速度限制。

例如，如果手动模式下的速度限制设置为250 mm/s，且记录的步速为1,000 mm/s，则在向前/向后操作时，步速将限制为250 mm/s。当记录速度为100 mm/s时，机器人将以100 mm/s的速度移动，因为记录的速度未超过速度限制。


{% hint style="info" %}
要设置步速限制，请参考"[5.1 操作条件设置](../../5-conditional-setting/1-op-cond-set.md)"。
{% endhint %}

要设置滑动速度级别 \(1: 低到 8: 高\)，请重复按下<SPEED: HI, LOW>键，直到所需速度级别出现。即使在这种情况下，机器人工具和链接的最大速度也将限制在速度限制以下。

{% hint style="info" %}
在自动模式下，`[Speed Adjustment]`按钮将显示播放速度 \(%\)，而不是步速限制 \(mm/sec\)。
{% endhint %}


{% hint style="warning" %}
如果工具数据中的长度和角度与实际值设置不同，工具可能在手动模式下操作过快。在操作机器人之前，您必须确保工具数据设置正确。
{% endhint %}
[__SOURCE](2-operation/1-manual-operation/3-step-fwd-bwd.md)
# 2.1.3 步进前/后

步进前/后是手动模式下操作机器人的一种方法，指的是回放记录的程序。通过操控机器人进行步进前/后操作，您可以在安全速度范围内检查记录的程序路径及相互联锁关系。

步进前/后操作的执行单元可以从 ${cont_model} 教学挂件屏幕左侧的 `[run to]` 按钮进行检查和设置。

![](../../_assets/tp630/lbt-runto_eng.png)  

要设置步进前/后操作的执行单元，请反复触摸 `[run to]` 按钮，直到出现所需选项。

![](../../_assets/tp630/lbt-runto-sw_eng.png)

* `[cmd]`: 将逐行执行命令
* `[Step]`: 将逐步执行
* `[End]`: 将执行到结束语句

<Br>

当执行单元设置为 'Cmd' 或 'Step' 时，机器人将忽略设定的精度区域并到达记录的步骤。如果设置为 end，机器人将沿着与自动模式播放相同的路径操作。

当您将执行单元设置为 'Cmd' 或 'Step' 并执行步进前/后操作时，机器人将在没有转角的路径上操作。有关转角的详细信息，请参阅 "[2.3.1.4 精度](../3-step/1-step-cmd-param/4-accuracy.md)"。

![图11 当执行 cmd/step 设置时的前/后路径回放](../../_assets/path-cmd-step-pback-fwd-bwd-en.png)

如果您将执行单元设置为 end 然后执行步进前/后操作，机器人的路径将根据停止位置而变化。换句话说，如果机器人在非转角处停止后执行前进操作，机器人将恢复原来的转角路径，但如果机器人执行后退操作，机器人将移动到记录的步骤，此时，机器人将在记录的步骤处停止，然后立即移动到上一个步骤。当机器人在转角处停止时，无论是向前移动还是向后移动，机器人都将保持其先前的转角路径。

![图12 当执行 end 设置时的前/后路径回放](../../_assets/path-end-pback-fwd-bwd-en.png)

当机器人在转角处停止并执行前进操作时，机器人将沿着原来的转角路径操作。在这里，如果机器人执行后退操作，然后在未完全达到上一个步骤的情况下再次执行前进操作，机器人在某些情况下可能无法创建原始的转角路径。换句话说，如果步骤的距离缩短到小于原始距离，从而无法满足现有的准确性条件，则将创建一个小于原始的转角路径。

![图13 步进前/后操作期间机器人路径变化示例](../../_assets/path-step-bwd-then-fwd-en.png)

您可以设置步进前/后操作的最大速度，并设置是否执行功能。在 ${cont_model} 教学挂件屏幕左侧轻触 `[run to]` 按钮后，在设置窗口中设置速度值和功能执行选项。

![](../../_assets/tp630/cond-set-step-fwd-bwd-spd_eng.png)

* `2: 步进前/后最大速度 (2: Step FWD/BWD maximum speed)`: 与手动操作中设定的速度值相同
* `[3: 步进前执行功能]`: 您可以选择功能执行选项。
  * Off: 功能将不执行步进前/后操作。无论外部 I/O 条件如何，您只能检查机器人路径。请注意，与外部系统的联锁将无效。
  * On: 您可以执行所有功能。应在外部联锁完成后使用。
  * I On: 您只能执行输入等待功能。当需要通过外部联锁检查安全性时应使用。
[__SOURCE](2-operation/2-automatic-operation/README.md)
# 2.2 自动操作

自动操作是教机器人执行它应该执行的工作内容的操作方法，然后使机器人执行该工作。
[__SOURCE](2-operation/2-automatic-operation/1-how-to-op.md)
# 2.2.1 操作方法

教机器人工作内容并使其执行工作的方式如下。

1.	检查安全围栏内和机器人操作范围内是否有人员或障碍物。

2.	通过旋转教学挂件的模式开关将操作模式设置为自动模式。

    <div style="max-width: 35vw">  

     ![](../../_assets/tp630/TP-hw-switch-auto.png)
     
    </div>

3.	在 ${cont_model} 教学挂件屏幕的状态栏上，检查操作模式是否设置为自动模式。

    ![](../../_assets/tp630/sbar-mode-auto1_eng.png)

* 如果设置为手动模式，请将教学挂件的模式开关转动以将操作模式设置为自动模式。

4.	触摸初始屏幕左侧的 `[Recording Condition]` 按钮。然后，将出现条件设置窗口。

    ![](../../_assets/tp630/fbt-condset_eng.png)

5.	设置程序重复选项和机器人操作速度。

    ![](../../_assets/tp630/cond-set-cycle-auto-spd_eng.png)

* `1: 操作循环类型 (Operation Cycle type)`：您可以设置是否重复在自动操作期间将执行的程序。
* `6: 自动驾驶速度比率 (6: Playback speed rate)`：您可以设置机器人在自动模式下回放程序时的操作速度（%）。  
  例如，如果操作速度设置为 100，则机器人将以步骤记录的速度移动，如果设置为 50，则机器人将以记录速度的 50% 的比例移动。

6.	按下教学挂件上的 `[start]` 键。启动灯将亮起，机器人将根据创建的程序执行工作。
[__SOURCE](2-operation/2-automatic-operation/2-adjust-op-spd.md)
# 2.2.2 操作速度调整

在自动操作中，${cont_model} 教学挂件屏幕左侧的 `[Speed Adjustment]` 按钮将在程序回放时显示机器人的操作速度 \(%\)。显示的操作速度是机器人的移动速度与步骤中记录的速度之比。

![](../../_assets/tp630/sbar-spd-auto_eng.png)

{% hint style="info" %}
在手动模式下，`[Speed Adjustment]` 按钮将显示步骤速度限制，而不是回放速度 \(%\)。
{% endhint %}

在自动模式下，您可以通过更改条件设置中的自动操作速度比值来调整机器人的操作速度，而无须修改程序。在触摸 ${cont_model} 教学挂件屏幕左侧的 `[Speed Adjustment]` 按钮后，在设置窗口中设置 `2: 步进前/后最大速度 (2: Step FWD/BWD maximum speed)` 和 `[6: Playback speed rate]` 的选项值。

![](../../_assets/tp630/cond-set-step-fwd-bwd-spd-auto-spd_eng.png)
[__SOURCE](2-operation/3-step/README.md)
# 2.3 步骤

步骤指的是要在工作程序中记录的特定姿势（每个轴的位置或工具提示的位置），机器人将采取该姿势。换句话说，步骤是机器人通过移动达到的一个位置。

机器人在从一个步骤移动到另一个步骤时执行各种功能。要从一个步骤移动到另一个步骤，需要一个移动条件，比如移动，这是一种移动命令。

* 这是机器人编程的基本单位。它是操纵器移动的命令。它包含了机器人操作所需的最少信息。
* 移动条件：这些是步骤陈述参数，如机器人位置、插值、速度、精度和工具编号。
[__SOURCE](2-operation/3-step/1-step-cmd-param/README.md)
# 2.3.1 步骤语句参数

步骤语句参数是机器人步骤运动所需的运动条件，如机器人位置、插补、速度、精度以及工具编号，除了移动，一个运动命令。

步骤语句的参数分为默认参数和可选参数。默认参数是步骤所必需的基本参数，而可选参数是在必要时可以添加的参数。

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
      <td style="text-align:left">插补</td>
      <td style="text-align:left">
        <p>步骤之间的插值路径</p>
        <p>P (关节插补), L (线性插补), C (圆形插补),
          SP (静态工具插补关闭), SL (静态工具线性插补),
          SC (静态工具圆形插补)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">姿态</td>
      <td style="text-align:left">
        <p>记录位置的参数。此参数可以省略，并且姿态可以在语句后指定（隐式姿态）。</p>
        <p>目标姿态 (X, Y, Z, Rx, Ry, Rz, Cfg) {坐标系} + 偏移 (X,
          Y, Z, Rx, Ry, Rz) {坐标系}</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">速度</td>
      <td style="text-align:left">机器人的操作速度 (单位: mm/秒, cm/分钟, %, 秒)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">精度</td>
      <td style="text-align:left">在机器人移动到目标步骤时当前位
        置与记录位置之间允许误差的值 (0&#x2013;7)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">工具编号</td>
      <td style="text-align:left">使用的工具编号 (0&#x2013;31)</td>
    </tr>
        <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">赋值语句</td>
      <td style="text-align:left">移动开始时，赋值语句按从左到右的顺序逐个执行</td>
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
[__SOURCE](2-operation/3-step/1-step-cmd-param/1-interpolation.md)
# 2.3.1.1 插值

插值是指步骤之间的插值路径，而 `[Step N]` 的插值方法决定了 `[Step N-1]` 和 `[Step N]` 之间的路径形式。

* P-PTP \(点对点\) 它是一般插值模式中最快的，因为它基于单独的轴，而不是工具末端插值两个步骤之间的路径。考虑到由旋转关节组成的工业机器人特性，工具末端的路径通常呈 C 形。

![图 14 P-PTP 插值中工具路径的示例](../../../_assets/image_73.png)

* L-线性插值 它在笛卡尔空间中的两个步骤之间沿直线移动。它用于需要线性路径的情况，例如弧焊部分。运动会在手腕姿态自动变化的情况下进行，如下所示。

![图 15 L-线性插值示例](../../../_assets/image_48.png)

在线性插值期间，在某些条件下，机器人无法自动改变手腕姿态，这种情况称为奇异姿态。

{% hint style="info" %}
无法执行姿态插值的奇异姿态如下。

* 如果 B 轴接近死区：有关死区设置的详细信息，请参考 "[7.4.5 B 轴死区](../../../7-system/4-robot-parameter/5-b-axis-deadzone.md)"。
* 当 B 轴的符号改变时：当 B 轴角度的符号切换 \( - → + \) 或 \( + → - \)
* 当 R2 和 R1 轴的角度变化超过 180 度
* 当 B 轴 \(轴 5\) 或工具末端通过 S 轴 \(轴 1\) 的旋转中心时：在姿态和轨迹中可能会出现错误。
* 当 S 轴的角度变化超过 180 度
{% endhint %}

* C-圆形插值

  它在两个步骤之间创建的圆形路径中移动。确定圆形需要三个点，选择这些点的参考如下。

  * 在从 `[Step n]` 移动到 `[Step n+1]` 时，如果 `[Step n+1]` 的插值方法是 C-圆形插值，则需要参考下一个步骤 `[Step n+2]`。

  * 如果 `[Step n+2]` 的插值方法是 C-圆形插值，则需要基于 `[Step n]`、`[Step n+1]` 和 `[Step n+2]` 确定圆形，并在其中沿 `[Step n]` - `[Step n+1]` 的段的弧线移动。

  * 如果 `[Step n+2]` 的插值方法不是圆形插值，则需要参考前一步骤 `[Step n-1]` 并基于 `[Step n-1]`、`[Step n]` 和 `[Step n+1]` 确定圆形，并在其中沿 `[Step n]` - `[Step n+1]` 的段的弧线移动。

![图 16 C-圆形插值示例 1](../../../_assets/image_338.png)

如果使用选择确定圆形所需的三个点的标准，您可以通过对相同点进行双重注册来创建程序，即使在连续弧的情况下也是如此。

通过确定步骤的插值方法以考虑沿移动路径，并使用相同点的双重注册功能，您可以按需创建程序。

![图 17 C-圆形插值示例 2](../../../_assets/image_302.png)

* 固定工具插值

  当机器人拥有工件并使用外部固定工具进行工作时，将使用此方法。在这种情况下，插值将在机器人拥有的工件基础上进行。

  有关固定工具的插值类型的详细信息，请参考 "[7.3.6.2 固定工具坐标系统](../../../7-system/3-control-parameter/6-cordsys-reg/2-stationary-tool-crdsys.md)"。
[__SOURCE](2-operation/3-step/1-step-cmd-param/2-pose.md)
# 2.3.1.2 位姿

位姿是记录位置的参数。如果您通过使用 `[Command]` 按钮输入移动，该运动命令，您应该在 tg \(target\) 参数中指定位姿表达。当使用 `[REC]` 键输入移动语句时，tg 参数不会出现。在触碰 `[REC]` 按钮的瞬间，机械手的位置信息和姿态将被记录，但它们不会在 JOB 编辑屏幕上显示，这就是它们被称为隐藏位姿的原因。

输入位姿的方法如下。

1. 声明一个位姿变量，po1。
   选择 [cmd.input > var_io > global or var] 菜单，然后输入 'po1'。
2. 使用 `[cur.pose]` 按钮将位姿变量初始化为位姿类型。
3. 执行声明和初始化命令，以便在每个命令前标记句点。
4. 在触碰 `[cmd.input]` 按钮后，选择 `[motion]` 然后输入语句。

    ![](../../../_assets/tp630/fbt-cmd-input-motion_eng.png)

5. 在触碰 `[property]` 按钮后，设置当前机器人位姿的属性，然后触碰 `[Apply]` 按钮。

    ![](../../../_assets/tp630/prg-step-pose_eng.png)

<br>

位姿变量和位移变量将以以下格式保存。

<table>
  <thead>
    <tr>
      <th style="text-align:center">位姿变量</th>
      <th style="text-align:center">位移变量</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center">(X, Y, Z, Rx, Ry, Rz, {坐标系}, {config.})</td>
      <td style="text-align:center">(X, Y, Z, Rx, Ry, Rz, {坐标系})</td>
    </tr>
    <tr>
      <td style="text-align:center">
        <p>{坐标系}:</p>
        <p>&quot;base&quot; = 基坐标系
          <br />&quot;robot&quot; = 机器人坐标系
          <br />&quot;user{n}&quot; = 用户坐标系 (n 指的是数字)
          <br
          />&quot;joint&quot; = 关节坐标系
          <br />&quot;encoder&quot;= 编码器</p>
      </td>
      <td style="text-align:center">
        <p>{坐标系}:</p>
        <p>&quot;base&quot; = 基坐标系
          <br />&quot;robot&quot; = 机器人坐标系
          <br />&quot;user{n}&quot; = 用户坐标系 (n 指的是数字)
          <br
          />&quot;joint&quot; = 关节坐标系</p>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](2-operation/3-step/1-step-cmd-param/3-speed.md)
# 2.3.1.3 速度

机器人操作速度可以使用以下四种单位进行显示。它们可以在所有插补方法中使用。

* mm/sec, cm/min: 设置机器人工具中心点 \(Tool Center Point\) 的最大速度。 机器人最大速度将由控制器根据位置和加速度/减速度参数自动计算。如果设置值超过机器人的性能最大速度限制，机器人将仅以最大速度限制运行。



* sec: 设置机器人移动时间。 机器人最短移动时间将由控制器根据位置和加速度/减速度参数自动计算。如果设置值短于机器人的性能最短时间限制，机器人将仅以最短时间限制运行。



* %: 设置机器人移动速度与机器人可以操作的最大速度的比例。当该值设置为 100% 时，机器人将在允许范围内以最大速度运行。



### 机械特定速度规划
* {mech:Mechanism number, spd:Speed}(速度单位) : 根据所选机械编号规划相应步骤的速度轨迹。
* 代码示例
```python
S2 move P,spd={mech:1,spd:100}mm/sec,accu=0,tool=0
```
| 机械特定速度规划 (机械 100mm/sec)| 机器人速度规划 (机器人 100mm/sec)| 
|---|---| 
| ![alt text](../../../_assets/tp630/Vel_Profile_2Mec_Addaxis.gif) | ![alt text](../../../_assets/tp630/Vel_Profile_1Mec_Rob.gif) |

* 上面的黄色圆圈表示设置为机械 1 的附加轴。
  * 机械特定速度: 附加轴 (机械 1) 生成与 100 mm/sec 速度匹配的轨迹。
  * 默认设置: 机器人生成与 100 mm/sec 速度匹配的轨迹。

<br>

{% hint style="info" %}
机械特定速度规划功能在版本 V60.32-00 中可用。

* 当单位为 mm/sec 或 cm/min 时，规格适用。
* 如果所选机械处于停止状态，则根据机器人的速度进行移动。
* 如果附加轴为旋转类型，则根据 `[System → 5: Initialization → 5: Additional Axis Parameter Settings]` 中配置的旋转半径，以 mm/sec 或 cm/min 规划速度。
* 使用旋转定位器静止编织功能时，速度根据定位器上工件的旋转半径进行规划。（定位器校准必须完成。）
{% endhint %}
[__SOURCE](2-operation/3-step/1-step-cmd-param/4-accuracy.md)
# 2.3.1.4 精度

它将确定机器人在推进目标步骤时经过该步骤的精度 \(接近记录位置的程度\)。当机器人移动到目标步骤时，如果当前位置信息与机器人移动到目标步骤时发生的记录位置之间的误差小于某个值，则机器人将移动到下一步。此时所允许的误差值称为精度。

在精度范围内 \(0~7\) 新创建的路径称为转角路径。一般而言，精度越高，转角速度越快，这在移动时间上是有利的。



![图18 由于精度而改变的路径 P2](../../../_assets/image_53.png)

精度0具有最高的精度，而精度7具有最大的误差。精度将在不能大于目标步骤两个轨迹中较短轨迹长度的1/2的方式下进行应用。换句话说，可以在上述示例中应用表达式 "Accuracy ≤ min\(P1-P2, P2-P3\) / 2"。在这个表达式中，使用了TCP距离进行说明，但相同的概念可以应用于角度。

在机器人的情况下，适用的精度级别的值将根据机器人的工具距离和姿态角度来定义。当涉及附加轴时，线性轴的值将基于长度来定义，而旋转轴的值将基于角度来定义。您可以直接在 `[system - 3: Robot Parameter - 6: Accuracy]` 菜单中更改值。有关精度级别值的详细信息，请参阅 "[7.4.6 精度](../../../7-system/4-robot-parameter/6-accuracy.md)"。



下图显示了根据精度级别的值如何创建转角路径。如果有一个一般的6轴关节机器人及附加轴，则可以为TCP \(工具距离\)、ORN \(位置角度\) 和AUX \(附加轴距离\) 单独设置精度级别的值。由于相关精度级别的所有值都应得到满足，因此转角路径将基于TCP、ORN和AUX之间的最小值创建。转角路径将在满足凸包性质的情况下，以恒定的曲线形式创建，无论速度变化如何。然而，由于伺服延迟，在低速和高速下可能会发生几毫米 \(mm\) 的误差。

![图19 根据精度级别的值创建转角路径](../../../_assets/image_79.png)

{% hint style="info" %}
根据精度级别的值创建转角路径的模式将以相同的方式应用于所有类型的插值。在P插值的情况下，将应用TCP距离精度，但可能会出现误差。
{% endhint %}

由于凸包性质，转角路径不会超过凸多边形区域，如下所示。

![图20 转角路径上所有点在凸多边形区域内](../../../_assets/image_87.png)
[__SOURCE](2-operation/3-step/1-step-cmd-param/5-tool-no.md)
# 2.3.1.5 工具编号

机器人位置将由工具头的位置和姿态决定。您可以指定将使用的工具编号 \(0-31\)。有关更多详细信息，请参阅 "[7.4.1.1 工具数据设置](../../../7-system/4-robot-parameter/1-tool-data/1-tool-data-set.md)"。
[__SOURCE](2-operation/3-step/1-step-cmd-param/6-until.md)
# 2.3.1.6 停止条件

当条件表达式“在...之后”满足时，机器人停止移动并执行下一条命令（步骤或功能）。

条件表达式“在...之后”的值可以通过结果 \(\) 函数的返回值进行检查。您可以检查移动操作是否通过条件表达式终止。

![Figure 21 Example of Stop Conditions](../../../_assets/image_46_1.png)

{% hint style="info" %}
有关机器人语言的详细信息，请参考 "[Robot Language Function Manual](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/README)。"
{% endhint %}
[__SOURCE](2-operation/3-step/1-step-cmd-param/7-comment.md)
# 2.3.1.7 注释

您可以为步骤的描述输入注释。您可以使用软键盘方便地输入注释内容。
有关如何使用软键盘的更多详细信息，请参考 "[3.2.4.4 软键盘](../../../3-programming/2-prog-edit/4-statement-edit/4-softkeyboard.md)"。
[__SOURCE](2-operation/3-step/2-step-pose-modify/README.md)
# 2.3.2 记录和更改步骤位置

您可以使用 `[REC]` 键记录或更改记录步骤的机器人位置和姿态。
[__SOURCE](2-operation/3-step/2-step-pose-modify/1-joint-crd-sys.md)
# 2.3.2.1 轴角录制坐标

在手动模式下，如果在 `[system - 1: User Environment]` 菜单中的 `[1: Pose Recording Form]` 选项设置为轴角，触摸移动语句中的 `[property]` 按钮。将出现以下属性窗口。由编码器记录的机器人位置只能查看，位置数据无法修改。

![](../../../_assets/tp630/lbt-property_eng.png)

![](../../../_assets/tp630/dlg-property-axis_eng.png)
[__SOURCE](2-operation/3-step/2-step-pose-modify/2-base-robot-crd-sys.md)
# 2.3.2.2 基座和机器人记录坐标

机器人的位置和姿态可以根据坐标系统的不同而有所不同。如果没有移动轴，基座坐标和机器人坐标通常是相同的。如果定义了移动轴，则机器人工具的位置和姿态将根据基座坐标和机器人坐标的不同而有所不同。

在手动模式下，如果在 `[system - 1: User Environment]` 菜单中的 `[1: Pose Recording Form]` 选项设置为基座或机器人，请触摸移动语句中的 `[property]` 按钮。您可以在属性窗口中检查机器人工具的位置和姿态。

{% hint style="info" %}
如果您想更改姿态记录形式，请联系客户支持团队以咨询专家或工程师。
{% endhint %}

对于一个工具提示位置及其方向，由于仪器的特性，可能会有多种姿态，因此为了定义一个姿态， 应该指定机器人形式 \(config.\)。

协作机器人由于其机械结构可以受到软限制的限制。当机器人不在操作时，您可以释放软限制或将其设置为较大值。

* auto: 关于机器人当前的姿态，后续的项目将会自动确定。如果未设置此模式，则将根据下面项目的指定与否进行判断。
* back: 机器人的工具提示位于机器人坐标系统的 X 轴的 - 方向，意味着后方。如果未指定，则工具提示位于 + 方向，意味着前方。
* down: H 轴和 V 轴之间的关系。如果指定此项，结果将是底部。如果未指定，则结果将是顶部。

![图 22 H 轴和 V 轴的姿态: 上 \(左\), 下 \(右\)](../../../_assets/image_58_1.png)

* flip: 使用 B 轴坐标为 + 值进行翻转。如果未指定，结果将是非翻转，与 - 值相对应。图中的红色箭头显示了腕轴顶部的方向。

![图 23 翻转 \(左\) / 非翻转 \(右\) 姿态](../../../_assets/image_75.png)

* `S (|S|>=180)`: S 轴角度的绝对值超过 180 度。如果未指定，将小于 180 度。
* `B (|B|>=180)`: B 轴角度的绝对值超过 180 度。如果未指定，将小于 180 度。

* `R2 (|R2|>=180)`: R2 轴角度的绝对值超过 180 度。如果未指定，将小于 180 度。

* `R1 (|R1|>=180)`: R1 轴角度的绝对值超过 180 度。如果未指定，将小于 180 度。

坐标系统将被保存为 `[Pose Variable]`.crd \(示例: po32.crd\)，并将指定以下字符串之一。如果是空字符串，则基本值将被识别为关节。

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>基座坐标系统 = &quot;base&quot;
          <br />
        </p>
        <p>机器人坐标系统 = &quot;robot&quot;
          <br />
        </p>
        <p>关节坐标系统 = &quot;joint&quot;
          <br />
        </p>
        <p>编码器 = &quot;encoder&quot;
          <br />
        </p>
        <p>用户坐标系统 = &quot;u1&quot; &#x2013; &quot;u10&quot;
          <br />
        </p>
        <p>
          <br />
        </p>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](2-operation/4-r-code.md)
# 2.4 R 代码

R 代码是分配给特定功能的唯一代码编号。为常用功能分配唯一代码编号可以帮助您快速使用这些功能。有关 R 代码的详细信息，请参阅 "[8 R 代码](../r-code/)."

触摸 `[R..[NO]]` 键后，输入代码编号并触摸 `[OK]` 按钮。然后将执行预定义的功能。

![](../_assets/tp630/k-r.png)
[__SOURCE](2-operation/5-error-info/README.md)
# 2.5 错误信息

当问题发生时，通知将出现在${cont_model}教学挂件屏幕底部的任务栏上，并闪烁约一分钟。您可以检查错误代码、通知消息以及错误发生的时间。

![](../../_assets/tp630/wg-alarm_eng.png)
[__SOURCE](2-operation/5-error-info/1-error-type.md)
# 2.5.1 错误类型

机器人系统中的故障由错误和警告组成。

![](../../_assets/tp630/wg-err-wrn_eng.png)

* 错误：这是一个足够严重的故障，足以停止机器人的操作，通知消息中的代码编号以 E 开头。

* 警告：机器人将继续运行，但警告是一个需要您检查是否采取了响应措施的问题。通知消息中的代码编号以 W 开头。
[__SOURCE](2-operation/5-error-info/2-error-handle.md)
# 2.5.2 错误处理

以下展示了如何检查和处理各种系统故障，比如系统故障或操作错误。

* 当警告或错误发生时，带有代码号码和标题的通知将出现在指导显示窗口。

  ![](../../_assets/tp630/wg-alarm_eng.png)

* 在指导显示窗口上点击 [log] 按钮。然后，错误和警告历史将会在一个新窗口中出现。

  * 错误和警告历史将按时间顺序显示，最新的故障将以黄色突出显示。
  
  ![](../../_assets/tp630/fbt-log_eng.png)

  ![](../../_assets/tp630/wg-alarm-log_eng.png)

* 在 ${cont_model} 教学挂件屏幕的 L 按钮栏上点击 `[Help]` 按钮。您可以查看错误代码、通知消息、故障原因以及如何采取措施。

  ![](../../_assets/tp630/lbt-help_eng.png)

  ![](../../_assets/tp630/help-alarm_eng.png)
[__SOURCE](2-operation/6-log.md)
# 2.6 事件日志

存储从过去到现在发生的事件日志，例如错误、警告、通知、开始/停止操作、操作、I/O 值变化和机器人语言执行。(存储的记录最大数量根据类型而异。)<br>
您可以查看每个日志的类型、消息、发生时间、发生时的程序/步骤/功能编号以及相关的辅助信息。此信息可作为分析问题原因和应对问题的线索。

请触摸功能按钮栏上的`[Log]`按钮。然后，日志窗口将出现。

![](../_assets/tp630/log/11_fb_log.PNG)

您可以查看事件日志。请触摸右侧的上箭头图标。

![](../_assets/tp630/log/21_log.PNG)

日志的过滤选项和辅助信息如下所示。

![](../_assets/tp630/log/31_log.PNG)
![](../_assets/tp630/log/44_di.PNG)

{% hint style="info" %}
辅助信息的显示从 V60.30-01 开始支持。
{% endhint %}

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
        <img src="../_assets/c1.png"/>
      </td>
      <td style="text-align:left">
        辅助信息：发生错误或警告时系统的状态也会被记录，您可以在辅助信息窗口中查看。在顶部点击标签可以选择并查看所需的辅助信息。活动输入/输出信号值以黄色背景显示，分配的用户 I/O 以加粗显示。
        <ul>  
          <li>姿态：机器人、附加轴值。(单位：mm 或 deg.)</li>
          <li>S/In：系统输入值。仅记录前 8 字节。(si0~63)</li>
          <li>S/Out：系统输出值。仅记录前 8 字节。(so0~63)</li>
          <li>D/In：用户输入值。仅记录 fb0 的前 32 字节。</li>(fb0.dib0~31)
          <li>D/Out：用户输出值。仅记录 fb0 的前 32 字节。</li>(fb0.dob0~31)
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png"/>
      </td>
      <td style="text-align:left">
        您可以使用过滤按钮仅显示所需类型的日志。当过滤按钮打开时，相应的类型将被显示，关闭时将被隐藏。
        <ul>
          <li>[全部]：一次打开或关闭所有过滤按钮。</li>
          <li>[+E]/[+W]：查看错误或警告日志。</li>
          <li>[+N]：查看通知（Notice）日志。</li>
          <li>[+ST]：查看机器人启动（START）和停止（STOP）日志。</li>
          <li>[+P]：查看定期记录的状态日志。</li>
          <li>[+OP]：查看用户操作日志。</li>
          <li>[+IO]：查看输入/输出信号变化日志。</li>
          <li>[+H]：查看作业程序执行日志。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c3.png"/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[
            <img src="../_assets/bt-menu.png"/>]: 您可以打开弹出菜单。
            <ul>
              <li>另存为日志文件：事件首先存储在内存缓冲区中，当缓冲区满时，它们会自动保存到文件中。通过选择此菜单，仍在缓冲区中的任何日志将立即保存到文件。</li>
              <li>清除日志文件：您可以清除内存缓冲区中的日志并删除所有日志文件。（已删除的文件无法恢复。）</li>
            </ul>
          </li>
          <li>[
            <img src="../_assets/bt-lock.png"/>]: 此功能锁定屏幕上新事件的显示。即使被锁定，新事件仍将继续记录；仅屏幕刷新被阻止。当日志屏幕不停更新并阻挡视线时，此功能可能很有用。您可以通过再次按锁定按钮或关闭并重新打开日志窗口来解锁。
          </li>
          <li>[
            <img src="../_assets/bt-trash.png"/>]: 此操作清除屏幕上显示的事件。它仅清除屏幕，内部记录的日志不会被删除。</li>
          <li>[
            <img src="../_assets/bt-refresh.png"/>]: 当日志屏幕被清除时，按此按钮将重新获取日志并在屏幕上显示。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c4.png"/>
      </td>
      <td style="text-align:left">这是选定类型的日志。新事件在上方以黄色背景突出显示。</td>
    </tr>
  </tbody>
</table>
[__SOURCE](2-operation/7-user-key/README.md)
# 2.7 用户键

通过将所需的功能分配给 ${cont_model} 教学挂件屏幕 R 按钮栏上的用户按钮区域，您可以在教导机器人时方便地使用它们。
[__SOURCE](2-operation/7-user-key/1-user-key-region.md)
# 2.7.1 用户键区域的切换

在 ${cont_model} 教学挂件屏幕的 R 按钮栏上触摸 `[user key]` 按钮，直到所需区域出现。然后，菜单按钮区域将切换到用户按钮区域。在用户键区域中，键信号输出功能和点应用功能默认分配和提供。

![](../../_assets/tp630/user-bar/user-bar.png)

* 如果您在按下 `shift` 键的同时按下 `[user key]` 按钮，可以反向切换区域。
  
* 键信号输出功能区域将在没有注册按钮的初始状态下保持为空。
[__SOURCE](2-operation/7-user-key/2-button-registration/README.md)
# 2.7.2 按钮注册区域

您可以在用户键区域通过按钮注册所需的功能。
[__SOURCE](2-operation/7-user-key/2-button-registration/1-key-signal-output.md)
# 2.7.2.1 关键信号输出功能区域

`键信号输出 (Key Signal Output)` 是一个允许您将所需变量分配给 F键并通过按钮操作将该变量的值设置为 1 或 0 的功能。 主要用于通过操作分配了输出变量的 F键打开或关闭 I/O 输出信号。 （所有类型的变量都可以被指定，包括一般变量、别名和输出变量。）

您可以通过按 HOME 屏幕右侧的 `[R4: User Key]` 打开 `键信号输出 (Key Signal Output)` 按钮。 如果没有进行任何设置，所有按钮将为空。

您可以按如下方式配置按钮：

1. 在 `键信号输出 (Key Signal Output)` 按钮开启的情况下，触摸 `[CTRL] + [User Key]`。 `键信号输出设置` 窗口出现。

2. 设置要显示在按钮上的功能名称和选项，然后触摸 `[F7: 确认] ([F7: OK])`。

![](../../../_assets/tp630/ctrl-key-outsignal_eng.png)

* `标题 (title)`：显示在按钮上的名称
* `on-var`：当指定变量名时，按钮打开时会将值 1 分配给该变量。
* `off-var`：当指定变量名时，按钮关闭时会将值 1 分配给该变量。
* `切换 (toggle)`：
  + Checked: 按钮每次按下时在开启和关闭之间切换。
  + Unchecked: 按钮被按下时开启，释放时关闭。
* `允许 在 自动 模式 (Permit on auto mode)`：
  + Checked: 此功能在自动模式下也可操作。
  + Unchecked: 此功能在自动模式下不操作。
* `关闭 开启 自动 模式 (OFF on auto mode)`：切换到自动模式时，此功能设置的所有变量将被关闭。

{% hint style="info" %}
对于 `on-var` 和 `off-var`，例如，如果您输入 3.5 并按下 `[ENTER]`，则 fb3.do5 被输入。 如果您输入 5 并按下 `[ENTER]`，则 do5 被输入。 或者，您可以使用屏幕底部的 F 键 [fb]、[do] 和 [so] 输入值。
{% endhint %}

3. 打开 `键信号输出 (Key Signal Output)` 按钮，并触摸注册的 F 键和 `[SHIFT]` 键以验证设置是否正确应用。

![](../../../_assets/tp630/rbt-userkey-keysig_eng.png)

{% hint style="info" %}
您还可以通过 `[F2: 系统] - 2: 控制参数 - 2: 输入/输出信号设置 - 5: 关键信号输出 ([F2: system] - 2: Control parameter - 2: Input/Output signal setting - 5: Key signal output)` 访问相同的设置界面。 有关更多详细信息，请参阅 "[7.3.2.8 Key Signal Output](../../../7-system/3-control-parameter/2-io-signal-setting/8-key-signal-output.md)"。
{% endhint %}
[__SOURCE](2-operation/7-user-key/2-button-registration/2-rob-appl-cfg.md)
# 2.7.2.2 机器人应用用户键配置

长按 ${cont_model} 教导终端屏幕上的 `[user key]` 按钮，直到所需区域出现。然后，F 按钮区域将切换到机器人应用用户键区域，例如 spotweld-bar 和 arcweld-bar。



![](../../../_assets/tp630/user-bar/ubar-spotweld-cfg.png)

按 `控制 (ctrl)` 键并按 `user-key` 按钮以打开配置屏幕，在此屏幕中您可以调整用户按钮的布局。

屏幕底部的列表是可选择的 F 按钮列表，您可以使用 `[Arrow Up]`/`[Arrow Down]` 移动光标。

屏幕顶部是用户按钮的布局，您可以使用 `[Arrow Left]`/`[Arrow Right]` 移动光标。

按 `[ENTER]` 键或 `[F1:选择] ([F1:Select])` 按钮将所选 F 按钮放置到所选位置。
如果您按 `[DEL]` 键或 `[F2:删除] ([F2:Delete])` 按钮，则所选位置的按钮将被删除并变为空。

完成放置后，按 `[F7:确认] ([F7:OK])` 按钮以保存用户按钮布局。


* 有关点应用功能的详细信息，请参阅 "[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。

* 有关弧应用功能的详细信息，请参阅 "[${cont_model} 控制器弧焊功能手册](https://hrbook-hrc.web.app/#/view/doc-arc-weld/zh/README)"。
[__SOURCE](2-operation/8-coord-sys/README.md)
# 2.8 坐标系统

空间中的坐标用于确定机器人运动的方向。 ${cont_model} 控制器具有关节坐标系统、机器人坐标系统、用户坐标系统和工具坐标系统。
[__SOURCE](2-operation/8-coord-sys/1-jog-key.md)
# 2.8.1 Jog Keys

它可以在手动模式下使用。当您按住使能开关，电机开启并按下 jog 按键时，您可以以低速移动机器人。

机器人的运动方向取决于参考坐标系。关节在轴坐标系中单独移动，而在其他坐标系统中同时移动，以便 TCP 可以朝选定的矩形坐标系方向移动。

![](../../_assets/tp630/sbar-joint-crdsys_eng.png)

![](../../_assets/tp630/keypad-jog_eng.png)

J7 和 J8 按键的运动由您设置的机器人模型和附加轴决定。7 轴机器人的 J7 可以通过分配给 R3 轴（第三轴）的 jog 按键进行操作。对于其他类型的机器人，您可以根据机制设置通过 jog 按键操作附加轴。

仅在所选机制为在 jog 时选择的机制 `[0]` 的情况下，如果下一个机制 `[1]` 的总轴数少于两个，将根据注册的附加轴的顺序进行分配。此时，如果机制 `[1]` 中还有未分配的按键，并且下一个机制在可以分配剩余轴的轴数方面有空间，它们将按顺序分配。

例如，是否根据附加轴的机制轴数对 J7 和 J8 轴进行分配将如下所示。

| Mechanism `[0]` | Mechanism `[1]` | Mechanism `[2]` | 是否为 J7 轴 / J8 轴分配 |
| :--- | :--- | :--- | :--- |
| 6 轴机器人 | 运动轴，轴 1 | 定位器，轴 1 | J7: 运动轴 / J8: 定位器 |
| 6 轴机器人 | 运动轴，轴 1 | 定位器，轴 2 | J7: 运动轴 / J8: 未分配 |
| 6 轴机器人 | 运动轴，轴 2 | 定位器，轴 2 | J7: 运动轴 1 / J8: 运动轴 2 |
| 6 轴机器人 | 运动轴，轴 3 | 定位器，轴 1 | J7: 未分配 / J8: 未分配 |
[__SOURCE](2-operation/8-coord-sys/2-joint-crdsys.md)
# 2.8.2 关节坐标系统

<table>
	<th style="background:lightgreen">关节坐标系统</th>
	<th>机器人坐标系统</th>
	<th>用户坐标系统</th>
	<th>工具坐标系统</th>
<tr>
	<td><img src="../../_assets/tp630/sbt-crd-axis_eng.png"/></td>
	<td><img src="../../_assets/tp630/sbt-crd-robot_eng.png"/></td>
	<td><img src="../../_assets/tp630/sbt-crd-user_eng.png"/></td>
	<td><img src="../../_assets/tp630/sbt-crd-tool_eng.png"/></td>
</tr>
</table>

1.	在手动模式下打开电机，并按住教导盒背面的启用开关。

2.	通过重复按触 ${cont_model} 教导盒屏幕状态显示窗口上的 `[Crd. Sys]` 按钮来选择关节坐标系统。然后，操作杆将显示每个关节的名称。

    ![](../../_assets/tp630/k-crdsys_eng.png)

    ![](../../_assets/tp630/sbar-joint-crdsys_eng.png)


3.	使用操控键操作机器人。机器人的每个关节独立移动。

    ![](../../_assets/image_85.png)

{% hint style="info" %}
有关机器人在与操控键相关的进展方向的详细信息，请参阅 "[2.7.1 Jog Keys](jog-key.md)"。 
{% endhint %}
[__SOURCE](2-operation/8-coord-sys/3-robot-crdsys.md)
# 2.8.3 机器人坐标系统

<table>
	<th>关节坐标系统</th>
	<th style="background:lightgreen">机器人坐标系统</th>
	<th>用户坐标系统</th>
	<th>工具坐标系统</th>
<tr>
	<td><img src="../../_assets/tp630/sbt-crd-axis_eng.png"/></td>
	<td><img src="../../_assets/tp630/sbt-crd-robot_eng.png"/></td>
	<td><img src="../../_assets/tp630/sbt-crd-user_eng.png"/></td>
	<td><img src="../../_assets/tp630/sbt-crd-tool_eng.png"/></td>
</tr>
</table>

1. 在手动模式下打开电动机，并按住教学挂件背面的启用开关。

2. 通过不断触摸 ${cont_model} 教学挂件屏幕状态显示窗口中的 `[Crd. Sys]` 按钮来选择机器人坐标系统。

    ![](../../_assets/tp630/k-crdsys_eng.png)

    ![](../../_assets/tp630/sbar-robot-crdsys_eng.png)


3. 使用走动键操作机器人。机器人将如以下所示移动。

    ![](../../_assets/image_62.png)

{% hint style="info" %}
* 有关机器人进度方向与走动键之间的关系，请参阅 "[2.7.1 走动键](1-jog-key.md)。" 
* 
  如果您使用右手，您可以更容易理解机器人坐标系统中的机器人操作。

  ![](../../_assets/crd-direction.png) 

图26 坐标系统方向（左）/ 旋转方向（右）

* 如果您将右食指的进度方向放在机器人坐标系统的 X 方向上，当您站在机器人的背面时，拇指的进度方向便成为 Z 方向，中指的进度方向便成为 Y 方向。
* 如果您将右手的拇指放在旋转中心轴的方向上，其他折叠手指的方向便成为旋转方向的 + 方向。
{% endhint %}
[__SOURCE](2-operation/8-coord-sys/4-user-crdsys.md)
# 2.8.4 用户坐标系统

<table>
	<th>关节坐标系统</th>
	<th>机器人坐标系统</th>
	<th style="background:lightgreen">用户坐标系统</th>
	<th>工具坐标系统</th>
<tr>
	<td><img src="../../_assets/tp630/sbt-crd-axis_eng.png"/></td>
	<td><img src="../../_assets/tp630/sbt-crd-robot_eng.png"/></td>
	<td><img src="../../_assets/tp630/sbt-crd-user_eng.png"/></td>
	<td><img src="../../_assets/tp630/sbt-crd-tool_eng.png"/></td>
</tr>
</table>

1.	在初始屏幕的右侧，触摸 `[system]` 按钮 - `[2: 控制参数 - 7: 坐标系统注册 - 1: 用户坐标系统]` 菜单，然后注册用户坐标系统。

{% hint style="info" %}
有关如何注册用户坐标系统的详细信息，请参阅 "[7.3.6.1 用户坐标系统](../../7-system/3-control-parameter/6-cordsys-reg/1-user-crdsys.md)。"
{% endhint %}

2.	触摸初始屏幕左上角的 `[Speed Adjustment]` 按钮，然后在 `[9: 选择用户坐标]` 选项中设置坐标系统。您可以选择用户坐标系统，而不是笛卡尔坐标系统。

	![](../../_assets/tp630/fbt-condset_eng.png)

	![](../../_assets/tp630/cond-set-usercrd_eng.png)

3.	使用手动键操作机器人。机器人将按如下方式移动。

	![](../../_assets/tp630/k-crdsys_eng.png)

	![](../../_assets/tp630/sbar-user-crdsys_eng.png)

{% hint style="info" %}
有关机器人在手动键操作下的进展方向的详细信息，请参阅 "[2.7.1 手动键](1-jog-key.md)。" 
{% endhint %}
[__SOURCE](2-operation/8-coord-sys/5-tool-crdsys.md)
# 2.8.5 工具坐标系统

<table>
	<th>关节坐标系统</th>
	<th >机器人坐标系统</th>
	<th>用户坐标系统</th>
	<th style="background:lightgreen">工具坐标系统</th>
<tr>
	<td><img src="../../_assets/tp630/sbt-crd-axis_eng.png"/></td>
	<td><img src="../../_assets/tp630/sbt-crd-robot_eng.png"/></td>
	<td><img src="../../_assets/tp630/sbt-crd-user_eng.png"/></td>
	<td><img src="../../_assets/tp630/sbt-crd-tool_eng.png"/></td>
</tr>
</table>

1.	以手动模式开启电机，同时按住教导控制器背面的启用开关。

2.	通过反复触碰 ${cont_model} 教导控制器屏幕状态显示窗口上的`[Crd. Sys]`按钮选择工具坐标系统。

    ![](../../_assets/tp630/k-crdsys_eng.png)

    ![](../../_assets/tp630/sbar-tool-crdsys_eng.png)

3.	使用手动键操作机器人。机器人将如以下所示移动。

* 如果机器人上附加了焊接枪

    ![](../../_assets/image_68.png)



* 如果机器人上没有附加焊接枪

    ![](../../_assets/image_92.png)

{% hint style="info" %}
有关机器人在与手动键相关的移动方向的详细信息，请参阅"[2.7.1 Jog Keys](1-jog-key.md)."
{% endhint %}
[__SOURCE](2-operation/9-axis-origin.md)
# 2.9 轴原点和工具长度的优化

您可以使轴整数和工具长度自动设置，以提高线性插值轨迹和坐标偏移的准确性。

* 您可以使工具提示的距离（在3D中难以测量）自动设置。要校准的参数是H、V、R2和B轴的轴原点以及X、Y和Z方向的工具长度。
* 您可以执行“轴原点和工具长度的优化”和“工具长度的优化”。

{% hint style="warning" %}
您应该在教学机器人程序之前优化“轴原点和工具长度”。如果在已经创建机器人的程序时优化了“轴原点和工具长度”，现有程序中的位置可能会发生变化。
{% endhint %}

以下显示了如何设置轴原点和工具长度的优化：

1. 使用教学 pendant 上的模式开关将操作模式设置为手动模式。

2. 在JOB程序窗口中，按住 `[SHIFT]` 并触摸 `[PROG]` 键，输入程序编号，然后触摸 `[OK]` 按钮。

    ![](../_assets/tp630/k-prog-step_eng.png)

    ![](../_assets/tp630/dlg-prog-sel_eng.png)

3. 按下教学 pendant 上的 `[motor]` 键，然后电机指示灯会闪烁。

* 如果电机未开启，请查看日志条上的错误信息并解决问题。

4. 在按住教学 pendant 背面的启用开关时，使用 jog 键操作机器人。

5. 在机器人操作范围内的任意位置放置一个尖针，然后将机器人的工具提示对准它。机器人前端到匹配工具提示的距离将被优化。

6. 通过触摸键盘上的 `[REC]` 键记录步骤。

    ![](../_assets/tp630/k-record_eng.png)

7. 改变机器人的姿势，并重复以上步骤 5-6 四次以上。

* 尽可能使用所有六个轴来改变机器人的姿势。此外，将轴角度至少改变 30 度。

8. 触摸 `[system]` 按钮 - `[6: Auto Calibration - 1: Optimize axis origin and tool length] ([6: Auto Calibration  - 1: Optimize axis origin and tool length])` 菜单。

    ![](../_assets/tp630/menu-axis-origin-tool-opt_eng.png)

9. 设置为自动校准创建的程序编号、工具编号和步骤位置误差允许范围，然后触摸 `[Execute]` 按钮。然后所选的轴原点和工具长度将被设置。

    ![](../_assets/tp630/axis-origin-tool-opt_eng.png)

* 当您使用多个工具时，应在第二个工具的 `[Optimization Selection]` 选项中选择工具长度。如果您选择了轴原点和工具长度，则之前设置的工具信息将会不正确。

{% hint style="info" %}
有关此功能的详细信息，请参阅 "[7.7.1 轴原点和工具长度的优化](../7-system/7-auto-calibration/1-axis-origin-tool-length-optimization.md)。"
{% endhint %}
[__SOURCE](2-operation/10-tool-data-auto-calib.md)
# 2.10 工具数据自动校准

在通过自动校准等确定轴原点和工具长度后，如果工具变形，可以简单地确定新的工具数据。此时，轴原点应已被确定并保持。此外，在确定工具长度和完成角度校准后，应教导一个固定参考点。如果发生工具变形，请将工具放置在变形之前指定的参考点的相同位置，然后执行自动工具数据校准。

1. 触摸`[system]`按钮 - `[3: Robot Parameter - 1: Tool Data]`菜单。

    ![](../_assets/tp630/menu-tool-data_eng.png)

2. 触摸`[Auto Calibration]`按钮后，使用手动键将工具提示移动到原始位置。

    ![](../_assets/tp630/tool-data-auto-calib_eng.png)

3. 在检查预定参考点的程序编号、步骤编号和工具编号后，触摸`[Execute]`按钮。

    ![](../_assets/tp630/tool-data-auto-calib2_eng.png)

{% hint style="info" %}
有关此功能的详细信息，请参阅"[7.4.1 Tool Data](../setting/robot-parameter/tool-data/)."
{% endhint %}
[__SOURCE](3-programming/README.md)
# 3. 编程

您可以编写和管理程序，使机器人能够执行工作并达到预期的结果。
[__SOURCE](3-programming/1-prog-manage.md)
# 3.1 程序管理

在机器人停止时，您可以创建、修改和删除程序。

1. 在JOB程序窗口中，按下带有<SHIFT>的`[PROG]`键。然后，程序选择窗口将出现。

    ![](../_assets/tp630/k-prog-step_eng.png)

2. 您可以创建、修改和删除程序。

* 要添加新程序，请输入新的程序编号并按<ENTER>键，参考“[3.2 程序编写](2-prog-edif/../2-prog-edit/README.md)”。

    ![](../_assets/tp630/k-prg-select_eng.png)

* 要打开程序以检查和修改其内容，输入程序编号，或从列表中选择一个程序，然后按下`[OK]`按钮。然后，所选程序将在JOB程序窗口中打开。

* 要删除程序，从列表中选择程序并按\<DEL>键。

* 您还可以从文件列表中删除程序 \(`服务 - 5: File Management (service - 5: File Management)`\)。有关详细信息，请参考“[4.2.1 文件管理](../4-service/2-file-manager/1-file-management.md)”。
  
* 您可以使用R代码\(R117\)快速删除程序。有关详细信息，请参考“[8.4 R117用于删除程序](../8-r-code/4-r117.md)”。
[__SOURCE](3-programming/2-prog-edit/README.md)
# 3.2 程序编写

为了实现您应用程序的目的，您可以编写和编辑一个程序，该程序由各种语句组成，以指示机器人操作。您可以在手动模式下编写程序。
[__SOURCE](3-programming/2-prog-edit/1-statement.md)
# 3.2.1 声明

一个一般程序由一个步骤命令组成，该命令指示机器人移动，以及一个功能命令，该命令指示机器人在移动后执行工作。

声明主要分为命令和参数，参数是附加项。参数分为声明所必需的默认参数和可以省略的可选参数。

![](../../_assets/image_82.png)

| No. | 描述 | No. | 描述 |
| :--- | :--- | :--- | :--- |
| ![](../../_assets/c1.png)  | 步骤编号 | ![](../../_assets/c3.png)  | 参数 |
| ![](../../_assets/c2.png)  | 命令 | ![](../../_assets/c4.png)  | 注释 |

{% hint style="info" %}
有关参数的详细信息，请参阅 "[2.3.1 步骤语句参数](../../operation/step/step-cmd-param/)."
{% endhint %}

当您输入声明时，基本设置值将自动输入到默认参数中，并可以更改。可选参数用符号 \( \_ \) 标记，您可以通过选择参数输入参数值。此外，可以输入的参数将在功能按钮栏上显示为按钮。

![图27 编辑命令 &#x2013; 输入参数值](../../_assets/tp630/pane-prog-move-option.png)

在编辑命令参数时，您可以使用教学手柄上的操作键和屏幕底部的菜单按钮，或使用软键盘编辑变量、表达式和字符串。
[__SOURCE](3-programming/2-prog-edit/2-statement-input/README.md)
# 3.2.2 声明输入
[__SOURCE](3-programming/2-prog-edit/2-statement-input/1-gen-statement-input.md)
# 3.2.2.1 一般语句输入

1. 在手动模式下，触摸初始屏幕右下角的 `[cmd.input]` 按钮。然后，命令输入窗口将出现。

    ![](../../../_assets/tp630/sbt-cmd_eng.png)

2. 触摸语句组，然后从列表中选择命令。语句将立即插入到当前光标位置下方。

    ![](../../../_assets/tp630/sbt-cmd-list_eng.png)

* 如果命令列表中的命令超过七个，您可以通过触摸 [prev/next] 按钮查看更多命令。

* 有关每个语句的详细信息，请参阅 "[${cont_model} Robot Language Function Manual](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/README)。"
[__SOURCE](3-programming/2-prog-edit/2-statement-input/2-step-input.md)
# 3.2.2.2 输入带有隐藏姿态的步骤语句

要将机器人的当前姿态输入为移动命令，请按下键盘上的 `[REC]` 键。



![](../../../_assets/tp630/k-record_eng.png)

当您使用 `[REC]` 键输入命令时，姿态变量不会出现在步骤中，与一般的命令输入模式不同，因此称为隐藏姿态。
[__SOURCE](3-programming/2-prog-edit/2-statement-input/3-rec-cond.md)
# 3.2.2.3 记录条件

当使用 `[REC]` 键输入语句时，机器人的当前姿态将被记录为目标姿态，并且将应用事先通过 `[rec.cond]` 按钮设置的值到移动命令 \(move\) 参数。以下显示了设置语句记录条件的方法。

1. 触摸 ${cont_model} 教导吊坠屏幕左侧的 `[rec.cond.]` 按钮。然后，记录条件设置窗口将出现。

    ![](../../../_assets/tp630/lbt-record_eng.png)

2. 设置插值、移动速度和单位、精度和工具编号后，触摸 `[check]` 按钮 \(![](../../../_assets/icon-ok.png)\)。

    ![](../../../_assets/tp630/lbt-record-edit_eng.png)

* 当执行位置记录时，移动语句将基于记录条件中设置的条件进行记录。
* 在机制设置中，您可以指定在执行位置记录时要存储的机制配置。

    * 如果轻触 `[mechsets]` 按钮，预定义的机制设置编号将依次出现。
    * 如果按住 `[mechsets]` 按钮，您可以在机制设置窗口中修改现有设置配置，或使用 `[+]` 或 `[-]` 按钮添加或删除机制设置。

        ![](../../../_assets/tp630/pop-mechanism_eng.png)
[__SOURCE](3-programming/2-prog-edit/3-statement-constitution.md)
# 3.2.3 声明配置

声明由地址区域和声明区域组成。 

![图 28 组成声明的区域](../../_assets/tp630/pane-prog-section.png)

| No. | 区域 | 描述 |
| :--- | :--- | :--- |
| ![](../../_assets/c1.png) | 地址区域 | 显示行号 \(1 到 9999\) 和步骤号 \(S1 到 S999\) |
| ![](../../_assets/c2.png) | 声明区域 | 显示一条声明 |

您可以通过按 `[←/→]` 键在地址区域和声明区域之间移动光标位置。按 `[↓/↑]` 键可以在选定区域内的行之间上下移动光标。

![图 29 在区域之间移动光标 \(左：地址区域。右：声明区域\)](../../_assets/tp630/pane-prog-sectionchng.png)
[__SOURCE](3-programming/2-prog-edit/4-statement-edit/README.md)
# 3.2.4 语句编辑

您可以使用教学挂件上的操作键和功能按钮栏上的菜单按钮编辑JOB程序窗口中的语句。使用软键盘，您可以编辑变量、表达式和字符串。

在语句区域中，您可以通过根据所选对象切换光标状态来检查和编辑语句。

* 语句光标状态：您可以在整个语句行被选中时检查语句。

    ![](../../../_assets/tp630/pane-prog-cmd-edit.png)

* 单词光标状态：您可以在语句的各个参数被选中时检查和编辑语句。

    ![](../../../_assets/tp630/pane-prog-cmd-edit1.png)
[__SOURCE](3-programming/2-prog-edit/4-statement-edit/1-how-to-edit-statement.md)
# 3.2.4.1 语句编辑方法

以下显示如何编辑语句。

1. 在JOB程序窗口中，通过按下`[↑/↓]`键选择语句区域。语句区域将在语句光标状态下被选中。

2. 在语句光标状态下，按下`[ENTER]`键。然后，将切换到语句光标状态，并选择一个参数，所选参数的值将出现在底部的输入区域。

3. 使用教学挂件上的操作键和屏幕的菜单按钮编辑参数值。

* 按下`[←/→]`键可以在参数之间向左或向右移动光标
* 可输入的参数将在功能按钮栏上显示为按钮。您可以通过选择所需按钮轻松输入参数。
* 您可以使用软键盘编辑变量、表达式和字符串。

4. 按下`[ENTER]`键。然后，所做更改的内容将被应用，使语句的参数值发生变化，并将光标移动到下一个参数。

* 若要取消更改，请按下`[ESC]`键。

5. 可以通过重复上述步骤2-3编辑另一个参数。

6. 按下`[ENTER]`键完成编辑。更改将在JOB程序中保存，光标将返回到语句光标状态。
[__SOURCE](3-programming/2-prog-edit/4-statement-edit/2-statement-edit-example.md)
# 3.2.4.2 编辑语句示例

通过将插值参数从 P \(关节插值\) 更改为 L \(线性插值\) 的示例，以下描述了如何编辑语句。

1. 在语句光标状态下，按下 `[ENTER]` 键。然后，语句光标将更改为单词光标状态，使得可以选择移动语句的插值参数 P \(关节插值\)。在输入区域，将显示当前插值设置值 P，能够输入的插值参数将作为按钮显示在屏幕的功能按钮栏上。

    ![](../../../_assets/tp630/pane-prog-move-P.png)

2. 在功能按钮栏上的按钮中触摸 `[L]` 按钮。然后，输入区域将显示 L \(线性插值\)。

    ![](../../../_assets/tp630/pane-prog-move-L.png)

3. 按下 `[ENTER]` 键。语句的插值参数将更改为 L，然后光标将移动到下一个参数，允许选定移动速度。

    ![](../../../_assets/tp630/pane-prog-move-spd.png)

4. 按下 `[ENTER]` 键以完成编辑。这次更改的内容将保存在 JOB 程序中，然后光标将返回到语句光标状态。
[__SOURCE](3-programming/2-prog-edit/4-statement-edit/3-how-to-edit-line-no.md)
# 3.2.4.3 行号编辑方法

行号可以设置为1到9999之间的任何数字。

1. 在JOB程序窗口中，通过按下`[←/→]`键选择地址区域。然后，地址区域将被选中。

* 如果光标在语句区域处于语句光标状态，按下`[←]`键将光标移动到地址区域。

    ![](../../../_assets/tp630/pane-prog-linenum.png)

2. 在地址区域，通过按下`[↓/↑]`键选择一行，然后编辑行号。

* 输入行号时，请使用数字键在输入区域输入行号。

    ![](../../../_assets/tp630/pane-prog-linenum1.png)

* 要删除行号，请按`[BS]`键。然后，行号的地址值将从输入区域中删除。

3. 按下`[ENTER]`键以完成编辑。更改的内容将保存在JOB程序中。

    ![](../../../_assets/tp630/pane-prog-linenum2.png)
[__SOURCE](3-programming/2-prog-edit/4-statement-edit/4-softkeyboard.md)
# 3.2.4.4 软件键盘

您可以在 ${cont_model} 教学挂件屏幕上使用软件键盘轻松输入变量、表达式和字符串。

1.	触摸 ${cont_model} 教学挂件屏幕的日志栏上的 `[![](../../../_assets/tp630/rbt-softkb_eng.png)]` 按钮。然后，软件键盘将出现在屏幕底部。

2.	您可以在输入区域使用软件键盘输入变量、表达式和字符串。现有的参数值将被移除，输入的文本将被显示。

    ![](../../../_assets/tp630/rbt-softkb-prog_eng.png)


* 如果您触摸输入区域左侧的 `[![](../../../_assets/bt-cursor-left.png)/![](../../../_assets/bt-cursor-right.png)]` 按钮，您可以移动光标位置，使您能够在所需位置插入文本。

* 您可以通过触摸 `[![](../../../_assets/bt-lang.png)]` 按钮来更改输入语言。

* 您可以通过按下 `[SHIFT]` 键时触摸键盘上的键来输入大写字母或符号。

* 您可以通过触摸 `[![](../../../_assets/tp630/bt-dock-softkb_eng.png)]` 按钮将键盘移到屏幕顶部。

3.	编辑文本完成后，您可以通过按 `[ENTER]` 键来隐藏软件键盘。
[__SOURCE](3-programming/2-prog-edit/4-statement-edit/5-block-edit-mode.md)
# 3.2.4.5 块编辑模式

您可以将程序的一行或多行设置为块，以执行复制、移动、删除和备注操作。
<br>

#### 1. 进入块编辑模式

在作业编辑面板中，使用左箭头键将光标移动到地址区域。
单击 `F2: Blk.edit` 按钮以进入块编辑模式，此时光标会变成灰色。

![](../../../_assets/tp630/blockedit/11_blockeditmode2.PNG)
![](../../../_assets/tp630/blockedit/12_blockeditmode.PNG)
<br><br>

#### 2. 设置块

使用上下箭头键将光标移动到块的起始位置，然后按 `确认 (ENTER)` 键。接着，使用上下箭头键将光标移动到块的结束位置，再次按 `确认 (ENTER)` 键。所选块将以蓝色背景高亮显示。

![](../../../_assets/tp630/blockedit/20_set_block.PNG)

（如果您在不移动光标的情况下执行复制或删除等操作，则无需第二次按 `确认 (ENTER)`。） 
<br><br>

#### 3. 复制

在块被选中时，单击 `F2: copy` 将内容复制到剪贴板。
或者，您可以在未选择块的情况下单击 `F2: copy` 以仅复制一行。
<br><br>

#### 4. 粘贴

使用上下箭头键将光标移动到要粘贴的行上方，然后单击 `F3: paste`。
例如，如果您想将复制的块粘贴到 S1 中 `delay 1` 语句的下方，请将光标放在 `delay 1` 上并单击 `F3: paste`。

![](../../../_assets/tp630/blockedit/30_paste.PNG)
![](../../../_assets/tp630/blockedit/32_paste.PNG)
<br><br>

#### 5. 剪切

当选中一个块时，单击 `F1: cut` 会使该块显示为浅灰色，表示它已被剪切。  
或者，您可以在未选择块的情况下单击 `F1: cut` 来剪切一行。

![](../../../_assets/tp630/blockedit/40_cut.PNG)

粘贴一个剪切的块遵循上述所述的方法。
<br><br>

#### 6. 删除
当选中一个块时，单击 `F4: delete` 然后确认 `删除吗？ (Delete?)` 提示将删除该块。  
或者，您可以在未选择块的情况下单击 `F4: delete` 来删除一行。

 ![](../../../_assets/tp630/blockedit/50_delete.PNG)
<br><br>

#### 7. 备注, 取消备注

此功能用于在不删除特定部分的情况下暂时禁用作业程序的执行。  
当选中一个块并单击 `F5: remark` 时，块内的语句将被注释掉（备注）。
当选中一个块并单击 `F6: unremark` 时，注释将被移除（取消备注）。  
此外，您可以在未选择块的情况下注释或取消注释单行。

{% hint style="info" %}
- 小于版本 V60.30-00：步骤不被备注。
- 版本 V60.30-00 或更高：步骤也会被备注。
{% endhint %}

 ![](../../../_assets/tp630/blockedit/60_remark.PNG)
<br><br>

#### 8. 关闭块编辑模式

可以通过单击 `F7: close` 或按 `ESC` 键关闭块编辑模式。
<br><br>

#### 9. 自动调整步骤 #

例如，如果将步骤 S1-S2 复制并粘贴到下方，原本在 S3 的 `move` 语句将由于插入的 2 个步骤向下推移并重新编号为 S5。

在这种情况下，作业中的所有分支语句，如 `goto`、`gosub`、`if` 语句，以及 `wait` 语句目标地址的超时地址将自动从 S3 调整到 S5。

例如，在下面的示例中，条件分支语句 `if di45==0 then S3` 将更新为 S5，以确保它仍然分支到之前的 `move` 语句。

![](../../../_assets/tp630/blockedit/71_branch_adjust.PNG)
![](../../../_assets/tp630/blockedit/72_branch_adjust.PNG)

此自动步骤编号调整适用于会前移或后移步骤编号的操作，如记录、删除和块编辑。

{% hint style="info" %}
以下规格适用于版本 V60.30-00 及更高版本。
{% endhint %}

如果由于删除或备注而删除了目标步骤，则将调整为 `deleted_step#` 或 `remarked_step#`，如下所示。  
请手动将这些修改后的目标地址调整为适当的步骤编号（或行编号/标签）。
（如果未更改，则在执行语句时将发生语法错误。）

![](../../../_assets/tp630/blockedit/76_branch_adjust.PNG)
[__SOURCE](4-service/README.md)
# 4. 服务

您可以使用程序的各种服务功能菜单，例如变量和文件管理。
[__SOURCE](4-service/1-service-usage.md)
# 4.1 服务的使用

1.	在手动或自动模式下，触摸初始屏幕功能按钮栏上的 `[service]` 按钮。程序的各种服务菜单将显示。

2.	选择所需菜单将使您能够管理文件、程序、教学挂件，或检查机器人系统的状态。

    ![](../_assets/tp630/svc-list.png)



* `5: 文件管理器 (5: 文件管理器)`: 您可以管理主板内部存储器、教学挂件或可移动存储设备中的文件。
* `6: 程序转换`: 您可以批量或单独转换数据，例如创建程序的条件和位置。
* `7: 系统诊断`: 您可以检查机器人和控制器的状态并更新系统版本。
* `8: 日期时间设置 (8: 日期时间设置)`: 您可以设置控制器的日期和时间。
* `9: 退出TP应用程序 (9: 退出TP应用程序)`: 退出TP（教学挂件）应用程序。
* `10: 应用程序(App) (10: 应用程序)`: 管理已安装并在教学挂件上运行的软件。
* `11: 教学挂件选项 (11: 教学挂件选项)`: 设置教学挂件的声音和屏幕保护时间。
* `12: 教学挂件共享 (12: 教学挂件共享)`: 连接教学挂件到多个控制器或HRSpace4中的虚拟控制器。
* `14: 系统程序 (14: 系统程序)`: 您可以查看和移除安装在控制器上的系统程序（例如OPC-UA服务器）。
* `19: 工业通信监控 (19: 工业通信监控)`: 监控固件信息和通信状态。
[__SOURCE](4-service/2-file-manager/README.md)
# 4.2 文件管理

您可以管理主板的内部存储器、教学挂件或可移动存储设备中的文件。

1.	触摸 `[5: 文件管理器]` 菜单。然后，将显示每个设备的文件夹列表和所选文件夹中保存的文件列表。

2.	按设备检查和管理文件夹结构和保存的文件。

    ![](../../_assets/tp630/file-manager/fl-manage_eng.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>这是主板内部存储器、教学挂件和可移动存储设备中的文件夹列表。您可以检查文件夹结构。</p>
        <ul>
          <li>[<img src="../../_assets/icon-mb.png" alt/>MAIN]: 保存于主板 (M/B) 的文件将用于实际的机器人操作。</li>
          <li>[<img src="../../_assets/icon-tp.png" alt/>TP] / [<img src="../../_assets/icon-usb.png" alt/>USB]: 教学挂件 (T/P) 和可移动存储设备 (USB) 将用于数据备份。<b>[<img src="../../_assets/icon-usb.png" alt/><b>USB]</b> 文件夹仅在可移动存储设备连接到教学挂件时出现。</li>
          <li>您可以通过旋转教学挂件上的 jog 旋转盘在文件夹列表中移动光标。</li>
          <li>如果您在文件夹列表中选择 <img src="../../_assets/icon-gt.png" alt/>] 或 [<img src="../../_assets/icon-wedge.png" alt/>] 并按下 <b>`[ENTER]`</b> 键，您可以显示或隐藏子文件夹。</li>
          <li>当您选择一个文件夹时，可以检查该文件夹中保存的文件列表。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">显示所选文件夹中保存的文件列表。您可以检查每个文件的名称、大小、最后修改日期、保护状态和其他信息。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">您可以使用功能按钮管理文件和文件夹。</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 它与 R 代码的 "R17 文件管理" 功能相同。
* 当可移动存储设备连接到教学挂件时，状态栏上将显示 `[USB]` 图标 \(![](../../_assets/icon-usb2.png)\) 在 ${cont_model} 教学挂件屏幕上。
{% endhint %}

{% hint style="warning" %}
在执行复制或删除文件等操作时，切勿从教学挂件中移除可移动存储设备。数据可能会损坏。
{% endhint %}
[__SOURCE](4-service/2-file-manager/1-file-management.md)
# 4.2.1 文件管理

选择一个或多个文件进行复制、移动或删除。

1. 使用教学手柄上的 jog dial 在文件夹列表中选择一个文件夹。所选文件夹中保存的文件列表将出现。

    ![](../../_assets/tp630/file-manager/fl-folder-select_eng.png)

2. 通过触摸文件列表中的所需文件进行选择。

    ![](../../_assets/tp630/file-manager/fl-file-select_eng.png)

* 您可以通过按住 `[CTRL]` 键逐个触摸每个文件以选择多个文件。
* 如果在按住 `[SHIFT]` 键的同时触摸两个文件，您可以一次选择这两个文件之间的所有文件。
* 如果您在屏幕的功能按钮栏上触摸 `[全选]` 按钮，您可以一次选择所有文件。

  按 `[ESC]` 键取消文件选择。

3. 您可以使用屏幕的功能按钮栏上的功能按钮复制、移动或删除所选文件。

* `[复制]`：复制所选文件并将其保存到临时文件夹，以便可以粘贴到另一个文件夹中。
* `[粘贴]`：您可以将保存在剪贴板中的文件粘贴到所需文件夹中。
* `[剪切]`：您可以剪切所选文件并将其保存到临时文件夹，以便可以粘贴到另一个文件夹中。
* `[删除]`：您可以删除所选文件。带有保护标记 \(W\_\) 的受保护文件无法删除。

4. 要将文件粘贴到文件夹中，请使用 jog dial 选择该文件夹，然后触摸 `[粘贴]` 按钮。然后，文件将粘贴到所选文件夹中。

    ![](../../_assets/tp630/file-manager/fl-copy_eng.png)

* 如果所选文件夹中已有相同名称的文件，将出现重复通知窗口。通过设置是否覆盖来处理它。

    ![](../../_assets/tp630/file-manager/fl-copy-pop_eng.png)

* 要删除文件，请触摸 `[删除]` 按钮，然后在确认窗口中触摸 `[ENTER]` 按钮。

    ![](../../_assets/tp630/file-manager/fl-delete-pop_eng.png)
[__SOURCE](4-service/2-file-manager/2-rename-file-folder.md)
# 4.2.2 文件和文件夹重命名

您可以重命名文件或文件夹。您还可以一次性重命名多个文件或文件夹。

1.	在文件（或文件夹）列表中触摸所需的文件（或文件夹）以选择它，然后触摸屏幕功能按钮条上的 `[rename]` 按钮。

    ![](../../_assets/tp630/file-manager/fld-rename-select_eng.png)

2.	在输入区域输入文件（或文件夹）名称。

    ![](../../_assets/tp630/file-manager/fld-rename_eng.png)

* 您可以简单地使用教学挂件上的操作键输入数字。（`[←/→]` 键：用于移动光标。数字键：用于输入数字）
* 若要输入包含数字的文本，请触摸日志条上的 ![](../../_assets/tp630/rbt-softkb_eng.png) 按钮以使用软键盘。

3.	按下 `[ENTER]` 键。然后，您输入的新名称将在列表中出现。

{% hint style="info" %}
* 您也可以重命名受保护的文件。
* 
  即使文件被重命名，大小、修改日期和属性等信息也将保持不变。

* 
  这是与 R 代码的 "R116 程序编号更改" 相同的功能。


{% endhint %}
[__SOURCE](4-service/2-file-manager/3-folder-management/README.md)
# 4.2.3 文件管理

您可以删除一个文件夹或添加一个新文件夹。
[__SOURCE](4-service/2-file-manager/3-folder-management/1-folder-removal.md)
# 4.2.3.1 文件删除

1. 使用教导 pendant 上的 jog dial 选择文件夹列表中的一个文件夹，然后按下 ![](../../../_assets/tp630/k-delete_eng.png) 键盘上的键。

    ![](../../../_assets/tp630/file-manager/fld-delete.png)

2. 在确认窗口中，按下 `[ENTER]` 按钮。所选文件夹及其中保存的所有文件将被删除。

    ![](../../../_assets/tp630/file-manager/fld-delete-pop_eng.png)
[__SOURCE](4-service/2-file-manager/3-folder-management/2-folder-generation.md)
# 4.2.3.2 文件创建

1. 使用教学挂件的 jog dial 在文件夹列表中选择一个文件夹，然后触摸功能按钮栏上的 `[New Folder]` 按钮。然后，将在所选文件夹下添加一个新文件夹。

    ![](../../../_assets/tp630/file-manager/fld-create_eng.png)

2. 输入新文件夹的名称，然后按 `[ENTER]` 键。

    ![](../../../_assets/tp630/file-manager/fld-create-rename_eng.png)
[__SOURCE](4-service/2-file-manager/4-file-protect.md)
# 4.2.4 文件保护

通过执行可以使更改或删除程序不可能的设置来保护您的重要文件。

1. 选择文件并触摸 `[property]` 按钮。然后，属性设置窗口将出现。

    ![](../../_assets/tp630/file-manager/fl-attribute_eng.png)

2. 检查文件名并触摸 `[Read Only]` 复选框以选择它，然后触摸 `[OK]` 按钮。保护标记 \(W\_\) 将出现在文件列表的属性中。

    ![](../../_assets/tp630/file-manager/fl-attribute-pop_eng.png)
[__SOURCE](4-service/2-file-manager/5-data-backup.md)
# 4.2.5 备份所有

您可以备份控制器的文件，例如项目、日志。

1. 在教学挂件\(T/P\)或USB存储设备的文件夹树中，使用教学挂件上的方向键选择您希望保存备份的目标文件夹。

    ![](../../_assets/tp630/file-manager/fl-backup-select.png)

2. 按下`SHIFT`键并点击屏幕底部的`[backup all]`按钮。

    ![](../../_assets/tp630/file-manager/fl-backup-button.png)

3. 点击“开始”按钮以` (start)`开始备份。一旦备份（大约1分钟）完成，请在结果窗口中检查备份结果。

    ![](../../_assets/tp630/file-manager/fl-backup-pop.png)
[__SOURCE](4-service/2-file-manager/6-data-restore.md)
# 4.2.6 恢复所有

您可以将使用 `全部备份 (backup all)` 功能备份的文件，例如项目、日志，恢复到系统中。

1. 在教导终端\(T/P\)或可移动存储\(USB\)的文件夹列表中，使用教导终端上的方向键选择您备份的文件夹。

    ![](../../_assets/tp630/file-manager/fl-backup-select.png)

2. 按下 `SHIFT` 键，并点击屏幕底部的 `全部恢复 (restore all)` 按钮。

    ![](../../_assets/tp630/file-manager/fl-restore-button.png)

3. 点击 `启动 (Start)` 按钮以开始恢复。一旦恢复完成（大约需要 1 分钟），请在结果窗口中检查恢复结果。

    ![](../../_assets/tp630/file-manager/fl-restore-report.png)

4. 关闭并打开控制器的电源。
[__SOURCE](4-service/2-file-manager/7-data-restore-partial.md)
# 4.2.6 部分恢复

在仅恢复备份数据的某些文件夹或文件时，请使用 `复制 (Copy)` 和 `粘贴 (Paste)` 功能。

1. 使用教导台的 jog dial，选择备份在教导台 \(T/P\) 或可移动存储设备 \(USB\) 中的项目 \(project/\) 文件夹，然后点击 `[copy]` 按钮。

    ![](../../_assets/tp630/file-manager/fl-restore-copy_eng.png)

2. 使用教导台的 jog dial，选择文件夹列表中的 `[MAIN]` 文件夹，然后触摸 `[Paste]` 按钮。

    ![](../../_assets/tp630/file-manager/fl-restore-paste_eng.png)

3. 在重复通知窗口中，触摸 `[All]` 的复选框以选择它，然后触摸 `[OK]` 按钮。备份数据将被恢复到主板上。

    ![](../../_assets/tp630/file-manager/fl-restore-pop_eng.png)

4. 重新打开控制器的电源。
[__SOURCE](4-service/2-file-manager/8-toggle-root.md)
# 4.2.8 切换根目录

{% hint style="info" %}
支持从 V60.26-00 开始。
{% endhint %}

在文件管理器左侧的树形窗口中，MAIN 和 TP 节点只显示用户允许访问的主文件夹。主文件夹外的区域是系统文件夹，用户不应访问。

如果在维护过程中必要，可以点击屏幕底部的 `[toggle root]` 按钮进入系统文件夹可访问模式。

一旦进入可访问模式，将显示以下警告信息，MAIN 和 TP 节点显示系统的根文件夹。

![](../../_assets/tp630/file-manager/fl-toggle-root0.png)

![](../../_assets/tp630/file-manager/fl-toggle-root1.png)

再次点击 `[toggle root]` 按钮以释放可访问模式。
[__SOURCE](4-service/3-program-conversion/README.md)
# 4.3 程序转换

您可以通过批量或单独修改创建程序的条件和位置，或通过移动坐标来编写新程序。

1.	触摸 `[6: Program Conversion]` 菜单。然后，程序转换菜单将出现。

2.	选择所需的菜单，然后修改程序条件和位置，或编写新程序。

    ![](../../_assets/tp630/prg-modi-menu_eng.png)

<br>

{% hint style="info" %}
在机器人启动期间，将限制使用菜单 `[4: The reference coordinate system]`、`[5: Coordinate transformation]`、`[6: Mirror Image]` 和 `[7: Step Copy]`。
{% endhint %}
[__SOURCE](4-service/3-program-conversion/1-rec-condition.md)
# 4.3.1 录制条件

您可以更改并设置程序特定步骤的录制条件，然后将其应用于现有程序，或编写新程序。

1. 触摸`[6: 程序转换 - 1: 录制条件转换] ([6: 程序转换 - 1: 录制条件转换])`菜单。然后，录制条件转换设置窗口将出现。

2. 设置录制条件选项后，触摸`[OK]`按钮。

    ![](../../_assets/tp630/prg-cond-modi_eng.png)

* `[源程序]`/`[目标程序]`：您可以输入要更改其录制条件的原始程序的编号 \(初始设置值：当前选择的程序\) 和在更改录制条件后要保存的新程序的编号。如果您将目标程序的编号设置为与原始程序相同的编号，则原始程序将被新程序覆盖和替换。
* `[开始步骤]`/`[结束步骤]`：您可以设置将应用录制条件更改的步骤范围 \(初始设置值：1/最后一步\)。
* `[精度]`，`[工具]`：您可以更改录制条件。
[__SOURCE](4-service/3-program-conversion/2-rec-speed.md)
# 4.3.2 记录速度转换

您可以为程序的特定步骤更改记录速度，并将其应用于现有程序，或创建新程序。

1. 触摸`[6: 程序转换 - 2: 记录速度转换] ([6: 程序转换 - 2: 记录速度转换])`菜单。然后，记录速度转换设置窗口将出现。

2. 设置完记录速度选项后，触摸`[确定]`按钮。

    ![](../../_assets/tp630/prg-speed-modi_eng.png)

* `[源程序]`/`[目标程序]`：您可以输入要更改记录速度的原始程序的编号 \(初始设置值：当前选择的程序\)以及在更改记录速度后要保存的新程序的编号。如果您将目标程序的编号设置为与原始程序相同，则原始程序将被新程序覆盖并替换。
* `[起始步骤]`/`[结束步骤]`：您可以设置将应用记录速度更改的步骤范围 \(初始设置值：1/最后一步\)。
* `[方法]`：您可以设置指定速度的方法。
  * `[指定速度]`：您可以批量转换记录的速度。
  * `[指定比率]`：如果记录速度的单位与`[单位]`选项中选择的速度单位匹配，则速度可以转换为相对于记录速度的比率。
  * `[更改单位]`：您可以转换记录速度的单位。
* `[范围]`：您可以设置要更改记录速度的步骤范围内的应用部分。
* `[单位]`：您可以设置速度单位。当速度指定方法选择为`[指定比率]`时，只有那些与步骤中记录的速度单位匹配的才会转换为比率的百分比。
* `[速度]`：如果您选择`[指定比率]`作为速度指定方法，这将表示比率值。
[__SOURCE](4-service/3-program-conversion/3-rec-position.md)
# 4.3.3 记录位置

您可以更改并设置在程序特定步骤中作为隐藏姿态记录的步骤位置的坐标系统，并将其应用于现有程序或创建新程序。

1. 触摸 `[6: 程序转换 - 3: 记录姿态转换] ([6: 程序转换 - 3: 记录姿态转换])` 菜单。然后记录位置转换设置窗口将出现。

2. 设置记录位置选项后，触摸 `[确定]` 按钮。

  ![](../../_assets/tp630/prg-position-modi_eng.png)

* `[源程序]`/`[目标程序]`: 您可以输入要更改记录位置的原始程序的编号 \(初始设置值: 当前选定的程序\) 和在更改记录位置后要保存的新程序的编号。如果您将目标程序的编号设置为与原始程序相同，原始程序将被新程序覆盖并替换。
* `[步骤范围]`: 您可以设置将应用记录位置更改的步骤范围 \(初始设置值: 1/最后一步\)。
* `[坐标系统格式]`: 您可以选择坐标系统来转换记录在步骤中的位置数据。如果您选择基准、机器人、工具或用户，位置数据将转换为笛卡尔坐标值；如果您选择关节，位置数据将转换为轴角。
[__SOURCE](4-service/3-program-conversion/4-rec-crdsys.md)
# 4.3.4 记录坐标系统

您可以更改作为隐藏姿态记录的步位置的坐标系统。您可以通过按下相关步骤的快速打开按钮检查您所更改的坐标系统。在机器人启动期间，使用 `[4: 参考坐标系统的变换]` 菜单将受到限制。

1. 触摸 `[6: 程序转换 - 4: 参考坐标系统的变换] ([6: 程序转换 - 4: 参考坐标系统的变换])` 菜单。然后，记录坐标系统偏移设置窗口将出现。

2. 设置记录坐标系统选项后，触摸 `[OK]` 按钮。

    ![](../../_assets/tp630/prg-coordisys-modi_eng.png)


* `[源程序]`/`[目标程序]`：您可以输入要更改的原始程序的记录坐标系统的编号（初始设置值：当前选择的程序）和更改记录坐标系统后要保存的新程序的编号。如果您将目标程序的编号设置为与原始程序的编号相同，则原始程序将被新程序覆盖。
* `[开始步骤]`/`[结束步骤]`：您可以设置将应用记录坐标系统更改的步骤范围（初始设置值：1/最后一步）。
* `[坐标系统格式]`：您可以选择要新指定的坐标系统。
[__SOURCE](4-service/3-program-conversion/5-rec-conversion.md)
# 4.3.5 坐标移动

坐标移动功能是一个使您能够在没有额外教学的情况下创建程序的功能，即使在工作件的位置不同的情况下，仍然可以将相同形状的工作件放置在不同的位置，如图2所示，在工作件上进行了教学的程序（图1）。

![左：图1，右：图2](../../_assets/image_369.png)

使用坐标移动功能需要有三个参考点。您可以通过在工作件的初始位置标记三个参考点来创建程序A。在移动工作件位置后，使用之前标记的三个参考点编写程序B。

![左：程序A，右：程序B](../../_assets/image_368.png)

{% hint style="info" %}
* 坐标移动程序的准确性将受到教学三个参考点准确性的影响。尽可能准确地对三个参考点进行教学。
* 在坐标移动中，将三个参考点之间的距离设置得尽可能远。
{% endhint %}

您可以通过计算坐标移动量，将现有程序（程序1）移至新程序（程序2），其基础是程序A和程序B的三个步骤。

![](../../_assets/image_315.png)

<br>

---

在机器人操作期间不允许使用该功能。使用坐标移动的方法如下。

1. 选择[6: 程序转换 - 5: 坐标变换]菜单。坐标移动的设置窗口将出现。
2. 设置完成后，按`[确定]`按钮。

    ![](../../_assets/tp630/prg-coordinate-modi_eng.png)


* [源程序]：现有教学程序编号（[图1]的程序编号）

* [目标程序]：通过执行坐标转换新创建的程序编号（[图2]的程序编号）

* [先前基准程序]：具有3个标准点的程序编号（[程序A]的编号）

* [后基准程序]：记录转换参考的3个点的程序编号（[程序B]的编号）
[__SOURCE](4-service/3-program-conversion/6-mirror-image.md)
# 4.3.6 镜像

您可以编写一个程序，使得 S 轴的位置和腕轴的姿态基于机器人 S 轴 0° 位置的 Y-Z 平面对称。

当指导左右两个机器人执行相同的操作（例如焊接车辆车身）时，此功能非常有用。首先，将一个操作教授给一个机器人，然后打开已教授操作的程序并将其转换为镜像。然后，将编写一个与 S 轴对称的程序。

![图 32 原始程序 \(左\) / 通过镜像转换的程序 \(右\)](../../_assets/image_379.png)

{% hint style="info" %}
镜像功能不支持协作机器人。
{% endhint %}

在机器人启动期间，将限制使用 `[6: 镜像]` 菜单。使用镜像功能的方法如下。

1.	触摸 `[6: 程序转换 - 6: 镜像] ([6: 程序转换  - 6: 镜像])` 菜单。然后，镜像设置窗口将出现。

2.	设置镜像转换选项后，触摸 `[OK]` 按钮。

* `[源程序]`/`[目标程序]`: 您可以设置现有程序的编号和通过镜像转换要创建的新程序的编号。

    ![](../../_assets/tp630/prg-mirror-img_eng.png)
[__SOURCE](4-service/3-program-conversion/7-step-copy/README.md)
# 4.3.7 步骤复制

您可以将程序的部分复制到另一个程序或同一程序中。在步骤中记录的功能也会被复制。在机器人启动期间，将限制使用 `[7: 步骤复制]` 菜单。

1. 触摸 `[6: 程序转换 - 7: 步骤复制] ([6: 程序转换 - 7: 步骤复制])` 菜单。步骤复制设置窗口将出现。

2. 在设置步骤复制选项后，触摸 `[确定]` 按钮。

    ![](../../../_assets/tp630/prg-step-copy_eng.png)

* `[源程序]`/`[目标程序]`: 您可以设置要复制步骤的原始程序的编号和通过粘贴复制步骤来创建的新程序的编号。如果您将目标程序编号设置为与原始程序编号相同，则原始程序将被新程序覆盖和替换。
* `[起始步骤]`/`[结束步骤]`: 您可以设置要复制的步骤范围（初始设定值：1/最后一步）。
* `[插入步骤]`: 您可以设置要粘贴复制步骤的参考步骤。复制的步骤将紧接在参考步骤之后粘贴。
* `[复制方式]`: 您可以选择复制步骤的进展方向。
  * `[前进/逆向]`: 您可以以与原始程序相同的顺序或原始程序的逆序粘贴复制的步骤。

{% hint style="info" %}
* 您无法复制受保护的程序。
* 如果在复制的步骤中记录了 END 功能，功能将被一同复制。必要时请删除该功能。
* 如果复制的步骤中记录了可以跳转（GOTO, GOSUB）到复制范围外步骤的功能，该功能将被复制，但编号不会自动更改。请在复制后更改编号。
{% endhint %}
[__SOURCE](4-service/3-program-conversion/7-step-copy/1-step-copy-example.md)
# 4.3.7.1 步骤复制示例

您可以将程序1的步骤2-5复制到程序2的步骤2（设为输入步骤）中，方向可以是向右或反向。

原程序（程序1）的步骤2-5将紧接在目标程序（程序2）的输入步骤（步骤2）之后插入，方向可以是向右（与原程序相同的顺序）或反向（原程序的反向顺序）。

![](../../../_assets/image_321.png)
[__SOURCE](4-service/4-system-diagnosis/README.md)
# 4.4 系统诊断

您可以检查和管理机器人的状态和控制器。您可以检查和更新控制器每个模块的版本。
[__SOURCE](4-service/4-system-diagnosis/1-system-version/README.md)
# 4.4.1 系统版本

1. 触摸`[7: System Diagnosis - 1: System version] ([7: System Diagnosis  - 1: System version])`菜单。然后，系统环境设置窗口将出现。

2. 检查和管理机器人和控制器的系统环境（软件版本）信息。

![](../../../_assets/tp630/svc-system-version_eng.png)


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
      <td style="text-align:left">机器人和控制器的系统环境（软件版本）信息</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>使用功能按钮编辑和管理系统环境。</p>
        <ul>
          <li>[OK]: 菜单将被关闭。</li>
          <li>[Ver. up]: 您可以更新控制器各模块的版本。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](4-service/4-system-diagnosis/1-system-version/1-controller-system-update.md)
# 4.4.1.1 控制器系统更新

您可以使用集成的压缩文件更新控制器各模块的版本。

1.	将包含集成压缩文件的可移动存储设备连接到教导终端的USB插槽。当可移动存储设备连接到教导终端时，状态栏中将出现`[USB]`图标 \(![](../../../_assets/icon-usb2.png)\)。

2.	触摸功能按钮栏上的`[Ver. Up]`按钮。然后，版本升级程序执行窗口将出现。

3.	通过触摸下拉菜单选择`[Version Up]`模式，使用`[Open]`按钮选择集成压缩文件，然后触摸`[OK]`按钮。

    ![](../../../_assets/image_311.png)

4.	选择您想要更新的模块后，触摸`[OK]`按钮。然后，更新将开始。

    ![](../../../_assets/image_255.png)

5.	更新完成后，重新启动控制器。

    ![](../../../_assets/image_367.png)
[__SOURCE](4-service/5-date-time-setting.md)
# 4.5 设置日期和时间

您可以设置控制器的日期和时间。

1. 触摸 `8: 日期时间设置 (8: Date, time setting)` 菜单。日期和时间设置窗口将出现。

2. 设置日期和时间信息后，触摸 `[OK]` 按钮。

    ![](../_assets/tp630/svc-date_eng.png)


* 您可以通过使用教导 pendant 的操作键输入日期和时间来进行设置。
* 如果您按箭头键，光标将在日期和时间项目间移动 \(年/月/日/小时/分钟/秒/上午/下午\)。

* 您可以通过按数字键输入数字。您也可以使用 `[SHIFT]`+`[↓]` 键调整数值。
* 在日历上设置日期。触摸 `[◁/▷]` 按钮以选择年和月，然后触摸日期。
[__SOURCE](4-service/6-app.md)
# 4.6 应用程序

管理安装并运行在教学吊 pendant 上的软件。

有关更多信息，请参阅 "[${cont_model} 控制器功能手册 - 教学吊 pendant 应用程序](https://hrbook-hrc.web.app/#/view/doc-hi6-tp-app/zh/README)"。
[__SOURCE](4-service/7-tp-option.md)
# 4.7 教学挂件选项

设置教学挂件的偏好选项。

![](../_assets/tp630/svc-option.png)

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
        声音
      </td>
      <td style="text-align:left">打开或关闭教学挂件的蜂鸣声。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        屏幕保护时间
      </td>
      <td style="text-align:left">在上次操作后，激活屏幕保护程序的设置时间。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        屏幕保护亮度
      </td>
      <td style="text-align:left">将屏幕保护程序的亮度设置为0（关闭）到6（稍微暗淡）。<br>
      （支持从版本 V60.32-06 及更高版本。）</td>
    </tr>
    <tr>
      <td style="text-align:left">
        屏幕保护期间通信周期
      </td>
      <td style="text-align:left">在屏幕保护程序活动期间，设置从控制器接收信息的通信延迟。如果设置为0，通信将不延迟进行。<br>
      （支持从版本 V60.30-08 及更高版本。）</td>
    </tr>
    <tr>
      <td style="text-align:left">
        触摸屏开启
      </td>
      <td style="text-align:left">打开或关闭触摸屏。<br>如果由于意外屏幕接触存在意外教学挂件操作的风险，请禁用此选项。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        是否使用作业键
      </td>
      <td style="text-align:left">选择是否分别使用 jog 键 `J7-`/`J7+` 和 `J8-`/`J8+`。<br>如果由于不正确的 jog 键操作存在位置器碰撞或其他问题的风险，请关闭此选项。<sup>1)</sup></td>
    </tr>
    <tr>
      <td style="text-align:left">
        语言
      </td>
      <td style="text-align:left">更改教学挂件的显示语言。更改在返回主屏幕后生效。<br>
      （支持从版本 V70.00-00 及更高版本。<sup>2)</sup>）</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
1\) 有关 jog 键使用的更多细节，请参阅“[7.6.6 机械设置](../7-system/6-initialization/6-mechannism-set.md)”中的机制 jog 规则。

2\) 对于上述提到的版本之前的版本，仅在执行 `[F1: 服务] - 9: 退出TP应用程序 ([F1: Service] - 9: Exit TP application)` 后才能切换显示语言。

{% endhint %}
[__SOURCE](4-service/8-tp-share.md)
# 4.8 教学挂件共享

![](../_assets/tp630/tp-sharing.png)

使用屏幕顶部的单选按钮选择模式。

* OFF : 共享功能已禁用。在正常情况下，应设置为 OFF，以便教学挂件可以正确连接到控制器。

* VRC (PC) : 物理教学挂件连接到运行在桌面 PC 上的多个虚拟控制器 (VRC)，并可以通过在它们之间切换来使用。有关连接说明，请参考 HRSpace4 帮助中的以下部分。  
  + HRSpace4 手册 - 8.4 实际教学挂件 (RTP)

* RRC (真实机器人控制器) : 一个教学挂件连接到多个控制器并通过在它们之间切换来使用。  
  + 需要额外的可选硬件。目前不支持此功能。
[__SOURCE](4-service/9-industrial-communication-monitoring.md)
# 4.9 工业通信监控

监控固件信息和通信状态。

有关更多信息，请参阅 "[${cont_model} 控制器功能手册 - 工业通信 > 1. CIFX PCI 通信 > 1.4 CIFX PCI - 监控工业通信](https://hrbook-hrc.web.app/#/view/doc-industrial-communication/zh/1-cifx-pci-communication/4-cifx-pci-monitoring-industrial-communication/README)"
[__SOURCE](4-service/10-system-program.md)
# 4.10 系统程序

您可以查看和移除安装在控制器上的系统程序（例如 OPC-UA 服务器）。

<br>

1. 安装系统程序

   * 将包含 ${cont_model} 系统程序安装文件 (hps) 的 USB 驱动器连接到教导操作器 (TP)。
   * 运行 `5: 文件管理器 (5: File Manager)` 菜单。从 [USB] 文件列表中选择文件并按 Enter 键。
   * 当程序安装对话框出现时，按 `运行 (Run)` 按钮开始安装。
   * 安装完成后，按 `退出 (Exit)` 按钮。
   * 要启动程序，请重新启动系统。

<br>

2. 移除系统程序

   * 运行 `14: System Program` 菜单以查看已安装程序的列表。
   * 选择一个程序并按屏幕底部的 `Remove` 按钮。
   * 当程序移除对话框出现时，按运行按钮开始移除过程。
   * 移除完成后，按 `退出 (Exit)` 按钮。
[__SOURCE](5-conditional-setting/README.md)
# 5. 条件设置

您可以简单地更改操作条件，而无需修改程序。即使控制器重新启动，修改的设置值仍将保持不变。
[__SOURCE](5-conditional-setting/1-op-cond-set.md)
# 5.1 操作条件设定

1. 在初始屏幕的左上角点击 `[Speed Adjustment]` 按钮。然后，操作条件设定窗口将出现。

    ![](../_assets/tp630/sbar-spd-auto_eng.png)  ![](../_assets/tp630/sbar-spd-manual_eng.png)

{% hint style="info" %}
在 `[Speed Adjustment]` 按钮上，手动模式下将显示速度限制 \(mm/sec\)，而自动模式下将显示播放速度 \(%\)。
{% endhint %}



2. 更改操作条件设定值，然后点击 `[OK]` 按钮。

    ![](../_assets/tp630/sbar-condi-setting_eng.png)

    
[__SOURCE](5-conditional-setting/2-op-cond-set-info.md)
# 5.2 操作条件设置的信息



* `[1: 操作周期类型]`: 您可以设置在自动操作期间是否重复将要执行的程序。它也可以在机器人启动时进行设置，并且设置值不会在手动操作期间应用。
  * 1 次周期: 工作程序将运行一次，然后停止。当程序达到 END 时，机器人将停止。
  * 连续: 工作程序将连续并重复运行。如果有外部停止操作，机器人将停止。
</br>
</br>

* `[2: 步骤 FWD/BWD 最大速度]`: 您可以设置向前/向后步骤的速度限制。有关此选项的详细信息，请参阅 "[2.1 手动操作](../2-operation/1-manual-operation/README.md)"。
</br>

* `[3: 步骤 FWD期间的功能执行]`: 您可以设置在步骤向前操作期间在工作程序中记录的功能的执行选项（模式）。
  * 关闭: 只有在工作程序中记录的 END 将被执行。除了 END 之外的所有其他功能都不会被执行。
  * 开启: 所有在工作程序中记录的功能将被执行。
  * 1 开: 仅输入信号等待功能和程序 END 功能将被执行。



{% hint style="warning" %}
在步骤向后操作期间，仅输入等待信号功能将被执行，所有其他功能将不会被执行。
{% endhint %}

* `[4: 在步骤向后和向前后的功能重执行]`: 您可以以一种方式进行设置，即在步骤向后操作后再次在步骤向前操作时，可以重新执行工作程序中记录的先前执行的功能。
</br>

* `[5: 步骤 FWD/BWD期间的路径恢复]`: 您可以设置在步骤向前/向后操作期间执行路径恢复的模式。
  * 禁用: 不会执行路径恢复
  * 启用: 将执行路径恢复而不与用户确认是否执行路径恢复
</br>
</br>

* `[6: 播放速度比率]`: 您可以设置机器人在自动模式下播放程序的操作速度（%）。这并不涉及更改工作程序步骤中记录的速度，而是指更改机器人移动速度与步骤中记录的速度之间的比率，范围从 1% 到 100%。




{% hint style="info" %}
如果在自动操作期间通过外部输入输入了低速命令，将不适用自动操作速度比率，而将适用手动最大速度 \(250 mm/s\)。
{% endhint %}

* `[7: 机器人锁定]`: 您可以以一种方式设置工作程序，使自动操作在不移动机器人的情况下进行。您可以检查 I/O 与外围设备的状态、软限制、周期时间等。
</br>

* `[8: 插值基准]`: 您可以设置作为机器人的手动移动参考的工具。一般而言，机器人工具被用作插值参考。
  * 机器人工具: 插值操作将基于附加在机器人前端的工具执行。
  * 固定工具: 插值将基于固定在地面上的工具的前端执行。如果选择固定工具作为插值参考，初始屏幕左侧的工具编号将标记为 ST0 \(![](../_assets/tp630/sbt-crd-st0-small_eng.png)\)。



{% hint style="info" %}
如果选择固定工具作为插值参考，则必须设置固定工具坐标系。有关详细信息，请参阅 "[7.3.6.2 固定工具坐标系](../7-system/3-control-parameter/6-cordsys-reg/2-stationary-tool-crdsys.md)"。
{% endhint %}

* `[9: 选择用户坐标系指定]`: 您可以在手动操作期间为笛卡尔操作设置用户坐标系编号 \(0~10\)。然后，机器人将在指定的用户坐标系的 X、Y 和 Z 轴方向上进行操作，所选用户坐标系的坐标值将在监视姿态时显示为工具前端的 X、Y 和 Z 坐标值。



  * 如果设置为 0，机器人坐标系图标 \(![](../_assets/tp630/sbt-crd-robot-small_eng.png)\) 将显示在状态显示窗口的 `[坐标系统]` 按钮上。基于用户坐标系的操作将被停用，基于笛卡尔坐标的操作和监视将被执行。 <br>
  ![](../_assets/tp630/pane-pose-robotcoord_eng.png)

  * 如果设置为 1 到 10 之间的数字，用户坐标系图标 \(![](../_assets/tp630/sbt-crd-user-small_eng.png)\) 将显示在 `[坐标系统]` 按钮上。通过使用 `[轴操作]` 键更改的坐标值将基于用户坐标系。 <br>
  ![](../_assets/tp630/pane-pose-usrcoord_eng.png)


{% hint style="info" %}
您可以在 `[system - 2: 控制参数 - 6: 坐标系统注册  -1: 用户坐标系统] ([system  - 2: 控制参数  - 6: 坐标系统注册  -1: 用户坐标系统])` 中注册用户坐标系编号。
{% endhint %}


* `[10: Plc 运行模式]`: 当机器人控制器使用嵌入式 PLC 控制输入/输出信号时，设置控制嵌入式 PLC 的模式。共有 4 种嵌入式 PLC 模式。有关详细信息，请参阅 "[${cont_model} 控制器功能手册 - 嵌入式 PLC](https://hrbook-hrc.web.app/#/view/doc-hi6-embedded-plc/zh/README?cont_model=${cont_model})"。

  * 关闭: 禁用该功能。
  * 停止: 停止嵌入式 PLC 操作。
  * R - 停止（远程停止）: 这是远程模式，并停止与控制器连接的 PC 中 HRLadder 的嵌入式 PLC 操作。
  * R - 运行（远程运行）: 这是远程模式，从与控制器连接的 PC 中的 HRLadder 执行嵌入式 PLC 操作。
  * 运行: 控制器操作下载到控制器的 PLC 程序。在 PC 的 HRLadder 中仅能进行监控。
[__SOURCE](6-monitoring/README.md)
# 6. 监控

您可以检查机器人系统的状态以及控制器的各种数据。

1. 按顺序触摸面板右上角的`[pane layout]`按钮，底部的[split]，以及左下角的[select]。面板选择窗口将出现。

    ![](../_assets/tp630/rbt-window-divide_eng.png)

2. 触摸您想要监控的项目并检查显示的数据。

    ![](../_assets/tp630/pane-list_eng.png)

{% hint style="info" %}
* 所有可以监控的项目将在面板选择窗口中显示。
* 
  可监控的项目将根据控制器的设置以不同方式显示。 

* 
  有关如何使用面板堆栈和工作区窗口的详细信息，请参阅 "[1.2.3.8 任务编辑窗口](../1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/8-work-area?cont_model=${cont_model})"。
{% endhint %}
[__SOURCE](6-monitoring/1-basic/README.md)
# 6.1 基础
[__SOURCE](6-monitoring/1-basic/1-pose.md)
# 6.1.1 位姿

在面板选择窗口中触摸 `[Pose]`。然后，机器人位姿信息窗口将出现。您可以检查机器人的每个轴的当前角度、工具中心点 \(TCP\) 的坐标值，以及编码器的当前值和命令值。

![](../../_assets/tp630/pane-pose_eng.png)
[__SOURCE](6-monitoring/1-basic/2-op-info.md)
# 6.3.2 操作时间

在面板选择窗口中，触摸 `[Operation time]`。然后，控制器的操作信息窗口将出现。

您可以检查在系统初始化、电源输入以及最近循环开始后立即创建的控制器每个操作的累积时间和周期数。您可以通过触摸信息底部每个项目的 `[Clear]` 按钮来初始化操作信息。

![Figure 41 操作信息](../../_assets/tp630/pane-operating_eng.png)

根据各个项目的条件，反射的时机如下。

![](../../_assets/image_449.png)
[__SOURCE](6-monitoring/1-basic/3-history.md)
# 6.1.3 历史

在面板选择窗口中，触摸 `[history]`。历史窗口将出现。

您可以查看输出作业程序的执行日志和时间戳的历史。



![](../../_assets/tp630/pane-history_eng.png)
[__SOURCE](6-monitoring/2-io/README.md)
# 6.2 IO, PLC, 通信
[__SOURCE](6-monitoring/2-io/1-system-input.md)
# 6.2.1 系统输入

在面板选择窗口中，触摸 `[System Input]`。然后，输入信号窗口将出现。

您可以检查与机器人操作相关的信号状态以及预先分配的输入信号的状态，以检测机器人和控制器发生的任何异常。

![](../../_assets/tp630/pane-system-input_eng.png)



* 在 ON/OFF 状态和序列状态中，当前输入的信号将以黄色显示。
* 
  在序列状态中，仅显示控制器序列信号的状态。

* 
  `[ON/OFF]`/`[Value]`/`[Sequence]`：您可以通过触摸单选按钮更改输入信号窗口的显示模式。
[__SOURCE](6-monitoring/2-io/2-system-output.md)
# 6.2.2 系统输出

在面板选择窗口中触摸 `[System Output]`。然后，输出信号窗口将会出现。

您可以检查与机器人操作相关的信号并检查制动控制的状态。



![](../../_assets/tp630/pane-system-output_eng.png)

* 在 ON/OFF 状态和序列状态中，当前输出的信号将以黄色显示。
* 在序列状态中，仅显示控制器序列信号的状态。
* `[ON/OFF]`/`[Value]`/`[Sequence]`：您可以通过触摸单选按钮来更改输出信号窗口的显示模式。
* `[Manual output]`：您可以在 ON/OFF 和序列状态下强制输出所选信号。



### 手动输出

您可以选择所需信号并强制输出。

1. 您可以通过触摸系统输出信号窗口右侧的 `[ON/OFF]` 或 `[Sequence]` 单选按钮来设置显示模式为 ON/OFF 状态或序列状态。

2. 在信号窗口中触摸一个信号以选择它，然后触摸 `[Manual Output]` 按钮。

    ![](../../_assets/tp630/pane-system-output1_eng.png)

3. 在手动输出确认窗口中检查输出条件后，触摸 `[ENTER]` 按钮。

    ![](../../_assets/tp630/pane-system-output-manual-pop_eng.png)


    | soN | =1/0 |
    | :---: | :---: |
    | N: 要输出的信号的编号 | 输出状态 \(1: 输出, 0: 不输出\) |


4. 检查所选信号的输出状态。所选信号将切换为输出状态并在信号窗口中以黄色显示。

    ![](../../_assets/tp630/pane-system-output2_eng.png)
[__SOURCE](6-monitoring/2-io/3-user-input.md)
# 6.2.3 公共输入

在面板选择窗口中触摸 `[public Input]`。然后，公共输入信号窗口将出现。

您可以检查通过控制器的 I/O 板的 CNIN 连接器输入的公共输入信号的状态。

![](../../_assets/tp630/pane-public-input_eng.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>显示一般输入信号的状态</p>
        <ul>
          <li>被指定为系统的基本规格或用户分配的一般输入信号将<b>以粗体</b>显示。</li>
          <li>当前输入的信号将以黄色显示。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[FB0]：您可以通过触摸下拉菜单（FB0 - FB15）选择要监视的 FB 块。最多可以配置 16 个 I/O 块，并且可以监视 960 点信号。</li>
          <li><b>[ATTR.-APPLIED]</b>：您可以选中复选框以执行设置，以便在通过正/负逻辑属性之前显示物理输入值。基本设置（未选中）是显示经过正/负逻辑属性后的输入逻辑值。</li>
          <li>[开/关]/[值]：您可以通过触摸单选按钮更改信号显示模式。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 在使用信号时，例如通过嵌入式 PLC 映射的现场总线信号，输入信号的开/关状态可能会有所不同。
* 
  输入信号的流向如下所示。
{% endhint %}

![](../../_assets/user-input-flow_en.png)
[__SOURCE](6-monitoring/2-io/4-user-output.md)
# 6.2.4 公共输出

在面板选择窗口中触摸 `[public Output]`。然后，公共输出信号窗口将出现。

您可以检查控制器中I/O板的CNOUT连接器输出的公共输出信号的状态。

![Figure 40 公共输出信号 - 开/关状态 \(左\)/值状态 \(右\)](../../_assets/tp630/pane-univoutsig-mode_eng.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>显示一般输出信号的状态</p>
        <ul>
          <li>指定为系统的基本规格或用户分配的一般输出信号将以 <b>粗体</b> 显示。</li>
          <li>当前正在输出的信号将以黄色显示。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[FB0]: 您可以通过触摸下拉菜单选择要监控的FB块 (FB0 - FB15)。您最多可以配置16个I/O块，并且使用一个块可以监控960个信号点。</li>
          <li>[手动输出]: 您可以强制输出所选信号。</li>
          <li><b>[ATTR.-APPLIED]</b>: 您可以勾选复选框，以便在通过正/负逻辑属性之前显示物理输入值。基本设置（未勾选）是显示通过正/负逻辑属性后的输入逻辑值。</li>
          <li>[开/关]/[值]: 您可以通过触摸单选按钮更改信号显示模式。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 在通过嵌入式PLC映射场总线信号等信号的情况下，输出信号的开/关状态可能会有所不同。
* 
  输出信号的流动如下。
{% endhint %}

![](../../_assets/user-input-flow_en.png)

#### 

#### 手动输出

您可以选择所需的信号并强制输出。

1.	您可以通过触摸一般输出信号窗口右侧的 `[ON/OFF]` 单选按钮将显示模式设置为开/关状态。

2.	触摸信号以在信号窗口中选择它，然后触摸 `[手动输出]` 按钮。

    ![](../../_assets/tp630/pane-univoutsig_eng.png)

3.	在手动输出确认窗口中检查输出条件后，触摸 `[ENTER]` 按钮。

    ![](../../_assets/tp630/pane-univoutsig-manual_eng.png)

| FbN | doN | =1/0 |
| :---: | :---: | :---: |
| N: 要监控的FB块编号 | N: 要输出的信号编号 | 输出状态 \(1: 输出, 0: 不输出\) |

4.	检查所选信号的输出状态。所选信号将切换到输出状态并在信号窗口中以黄色显示。

    ![](../../_assets/tp630/pane-univoutsig-onoff_eng.png)
[__SOURCE](6-monitoring/2-io/5-fn-io.md)
# 6.2.5 fn 输入, fn 输出

您可以通过指定 fb 对象的特定区域来定义 fn 对象。
如果 ${cont_model} 控制器是总线主设备，并且有多个总线从设备，您可以将每个从设备的区域设置为每个 fn 对象，以直观地处理这些从设备。

设置的 fn 对象可以像机器人语言和嵌入式 PLC 中的 fb 对象一样使用。


![](../../_assets/io/io_fn.png)


在面板选择窗口中选择 `[fn 输入]` 或 `[fn 输出]`。fn 输入或输出面板将出现，您可以检查每个 fn 对象的输入和输出信号的值。

有关如何设置 fn 对象，请参阅下面的链接。

[7.3.2.12 fn 块分配](../../7-system/3-control-parameter/2-io-signal-setting/12-fn-block?cont_model=${cont_model})


单击 '[F6:prev]' / '[F7:next]' 按钮以更改要显示的 fn 对象的数量。

其余 F 按钮的使用与 [公共输入](6-user-input?cont_model=${cont_model}) 和 [公共输出](7-user-output?cont_model=${cont_model}) 监控窗口相同。


![](../../_assets/io/io_fn_mon.png)
[__SOURCE](6-monitoring/2-io/6-forced-io.md)
# 6.2.6 强制 IO

您可以在强制 IO 面板中注册 IO 继电器变量，以强制某些更改的 IO 值。

{% hint style="warning" %}
* 此功能仅用于测试或问题分析。
* 强制 IO 功能的误操作可能会导致严重事故，例如碰撞、掉落和人员伤亡。仅在您充分了解系统的 IO 连接并清楚预测强制值更改的后果时谨慎使用。
* 在测试和问题分析后，请务必完全清除强制 IO 并将其恢复到正常 IO 状态。

{% endhint %}

#### 打开强制 IO 面板

1. 分割屏幕并按左下角的 [选择] 按钮。

![](../../_assets/tp630/panel-split.png)
&nbsp;
![](../../_assets/tp630/panel-sel.png)

2. 在面板选择窗口中双击 `强制 io (forced io)`。强制 I/O 面板打开。

![](../../_assets/tp630/panel-forced-io/panel-forced-io.png)

![](../../_assets/tp630/panel-forced-io/panel-forced-io-mon.png)


#### 如何使用

选择 `名称 (Name)` 列，输入所需的 IO 继电器变量名称，然后按 `确认 (ENTER)` 键将变量注册到表中。  
(您可以通过再次单击名称列来修改您输入的变量名称。)

![](../../_assets/tp630/panel-forced-io/panel-forced-io-name.png)

选择 `力控制变量 (Value)` 列，输入您想要应用的新 IO 值，然后按 `确认 (ENTER)` 键。

![](../../_assets/tp630/panel-forced-io/panel-forced-io-val.png)

如果您有更多要应用的强制 IO 条目，请以同样的方式输入。您最多可以输入 100 个条目。

![](../../_assets/tp630/panel-forced-io/panel-forced-io-multi.png)

面板标题栏上的 * 标记表示表格已被修改，并且此修改尚未应用。  
按 [F7: 应用] 按钮以应用强制 IO。  
当您在警告消息框中按 `确认 (OK)` 按钮时，所有强制 I/O 条目将被应用。

![](../../_assets/tp630/panel-forced-io/panel-forced-io-apply.png)

面板标题栏上的 * 标记消失，您可以看到强制 IO 值已被应用。  
标题栏上的红色 F 标记闪烁。这是强制 IO 正在应用的警告。

![](../../_assets/tp630/panel-forced-io/panel-forced-io-result.png)


* 在编辑过程中按 `SHIFT+DEL` 删除项目。
* 您可以通过按 [F5: 上移]、[F6: 下移] 按钮来改变项目的顺序。
* 如果在编辑表时单击 [F3: 取消编辑]，它将重新加载最后应用的状态。

在完成测试和问题分析后，请务必按 [F2: 清除] 按钮以完全清除强制 IO。

![](../../_assets/tp630/panel-forced-io/panel-forced-io-clear.png)

{% hint style="warning" %}
* 如果多个条目强制相同继电器（或重叠位）冲突的值，则强制为表格中下方项目的值。
* 当 ${cont_model} 控制器断电时，所有注册为强制 IO 的内容将被清除。

{% endhint %}
[__SOURCE](6-monitoring/2-io/7-memory-variables.md)
# 6.2.7 内存变量


在面板选择窗口中触摸 `[memory variables]`。
来自Robot Language的可访问内存PLC继电器变量被显示。

![](../../_assets/tp630/pane-memory-variables_eng.png)
[__SOURCE](6-monitoring/2-io/8-EC-device-info.md)
# 6.2.8 EtherCAT 设备

在面板选择窗口中，触摸 `[EtherCAT dev.]`。此监控面板显示从属设备列表及其网络状态，这些设备与 ${cont_model} 控制器内部和外部组成 EtherCAT 网络。在 EtherCAT 网络中，控制器主板作为主设备工作。

![](../../_assets/tp630/pane-EC-device_eng.png) 

-	ENI-配置的从属设备数量：构成 EtherCAT 网络的从属设备数量
-	连接的从属设备数量：当前连接的从属设备数量，应与 'ENI-配置的从属设备数量' 相同
-	设备：与主板连接的 EtherCAT 从属设备名称
-	地址：EtherCAT 网络上的唯一地址
-	连接
    -	NG：网络故障
    -	OK：网络成功
-	模式
    -	未知：由于网络故障而无法检查当前状态
    -	初始化：网络通道已初始化的状态
    -	预操作：从属设备只能通过非周期邮箱进行通信的状态
    -	安全操作：从属设备仅能通过传输数据（Tx PDO）进行通信的状态
    -	操作：从属设备可以同时传输和接收数据（Tx/RxPDO）的状态
[__SOURCE](6-monitoring/3-job/README.md)
# 6.3 工作程序，机器人语言
[__SOURCE](6-monitoring/3-job/1-job.md)
# 6.3.1 作业

在面板选择窗口中触摸 `[job]`。要获取总程序列表，请按 `[SHIFT]`+`[PROG]` 键，进入程序选择窗口。然后，您可以创建、删除和选择程序。

![](../../_assets/tp630/k-prg-select_eng.png)

您可以在任务编辑窗口中修改所选的作业程序。

![](../../_assets/tp630/pane-job_eng.png)

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
        <img src="../../_assets/tp630/k-prog-step_eng.png" alt/>
      </td>
      <td style="text-align:left"> <ul>  `[SHIFT]`+`[PROG]` : 在程序选择窗口中，您可以创建、删除或选择程序。 </ul> </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <ul> 显示基本信息和命令。您可以检查和修改每个命令的详细信息。
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li> <b>[&#x2026;]</b>: 如果自动缩进应用不正确，
            可以再次执行作业程序中的自动缩进。</li>
          <li>当程序被写入时，所选语句的参数值
            将显示在输入区域。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
有关如何管理和编写程序的详细信息，请参阅 "[3 Program Writing](../../3-programming/README.md?cont_model=${cont_model})."
{% endhint %}
[__SOURCE](6-monitoring/3-job/2-hot-edit.md)
# 6.3.2 热编辑

这是在播放仍在运行时编辑程序的功能。

{% hint style="warning" %}
* 当你编辑并应用当前处于自动操作中的程序或即将被调用的程序时，它将在下一个循环中应用（在程序结束执行后）并使用编辑过的程序回放机器人。请务必小心，因为错误的编辑可能导致重大事故，例如机器人与夹具之间的碰撞。
{% endhint %}
<br><br>

### 入口

触摸面板上的 `[hot edit]` 按钮，当前程序的热编辑窗口将被打开。

![](../../_assets/tp630/pane-hot-edit-0_eng.png)

<br>

### 可编辑的类型

虽然操作与手动模式相同，但以下功能不可使用。

1) `[REC]` 键（记录隐藏姿态移动）：显示“在热编辑状态下不允许操作”消息。
2) `[POS. MOD]` 键：显示“在热编辑状态下不允许操作”消息。


    ![](../../_assets/tp630/pane-hot-edit-1_eng.png)

<br>

### 反映

如果你完成了程序编辑，点击指南显示栏左侧的按钮 ![](../../_assets/tp630/bt-menu.png) 打开弹出菜单，并选择 [hotedit: request to apply]。

![](../../_assets/tp630/pane-hot-edit-apply2_eng.png)

<br>

实际反映的时间在以下表中显示。

<u>V60.32-03 或更高版本：</u>
<table>
<thead>
  <tr>
    <th>状态</th>
    <th>程序</th>
    <th>请求后，反映时间</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="2">无论 <br>是否运行<br>或 运行中</td>
    <td>未运行程序<br>(不在调用栈中的作业)</td>
    <td>立即应用</td>
  </tr>
  <tr>
    <td>正在运行程序<br>(在调用栈中的作业)</td>
    <td>在循环结束时<br>或 RESET 0</td>
  </tr>
</tbody>
</table>
<br>

<br>
<u>V60.32-02 或更早版本：</u>

<table>
<thead>
  <tr>
    <th>状态</th>
    <th>程序</th>
    <th>请求后，反映时间</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>未运行</td>
    <td>-</td>
    <td>立即应用</td>
  </tr>
  <tr>
    <td rowspan="2">运行中</td>
    <td>未运行程序<br>(不在调用栈中的作业)</td>
    <td>立即应用</td>
  </tr>
  <tr>
    <td>正在运行程序<br>(在调用栈中的作业)</td>
    <td>在循环结束时</td>
  </tr>
</tbody>
</table>

<br>

### 标题栏显示

当前状态符号显示在热编辑窗口标题栏的右侧。

'*' 符号表示教学程序已经被修改，并且与当前运行的程序不同。

![](../../_assets/tp630/pane-hot-edit-apply3.png)

'>' 符号表示在程序运行时已经请求热编辑。

![](../../_assets/tp630/pane-hot-edit-apply4.png)

' '（空白）符号意味着请求尚未反映，或已经反映，因此程序与运行的程序相同。

![](../../_assets/tp630/pane-hot-edit-apply5.png)


<Br>

### 不同程序选择

当你按下 `[SHIFT]` + `[PROG]` 键时，可以选择不同的程序。你也可以创建一个新程序。
[__SOURCE](6-monitoring/3-job/3-global-variable/README.md)
# 6.3.3 全局变量

显示所有全局变量的列表。您还可以创建/删除变量并编辑类型和值。


#### 打开全局变量面板

1. 拆分屏幕并按左下角的 [Select] 按钮。

![](../../../_assets/tp630/panel-split.png)
&nbsp;
![](../../../_assets/tp630/panel-sel.png)

2. 在面板选择窗口中，触摸 `[global variable]`。`全局变量 (global variables)` 面板打开。

![](../../../_assets/tp630/pane-gvar.png)


![](../../../_assets/tp630/panel-gvar/panel-gvar0.png)
[__SOURCE](6-monitoring/3-job/3-global-variable/1-basic-feature.md)
# 6.3.3.1 基本特征


##### 寻找变量

如果由于变量数量众多而难以找到所需的变量，请在顶部的过滤器中只输入变量名称的一部分。仅显示以您输入的过滤字符串开头的变量，便于查找。

![](../../../_assets/tp630/panel-gvar/gv-find.png)


##### 更改变量的值（对于 bool、int、double、string 类型）

选择所需变量的 `值 (value)` 列并输入新值。
按 ENTER 键以将输入的值应用于该变量。

![](../../../_assets/tp630/panel-gvar/gv-edit-value.png)

##### 更改变量的值（对于 pose、shift 类型）

选择所需姿态或位移变量的 `值 (value)` 列。

![](../../../_assets/tp630/panel-gvar/gv-edit-pose1.png)

按 ENTER 键打开姿态或位移属性窗口。
编辑后，单击 [F7: OK] 按钮。

![](../../../_assets/tp630/panel-gvar/gv-edit-pose2.png)


##### 更改变量类型

选择所需变量的 `类型 (type)` 列并按 ENTER。将出现如下所示的创建变量对话框。

![](../../../_assets/tp630/panel-gvar/gv-edit-type.png)

![](../../../_assets/tp630/panel-gvar/gv-create-var.png)

从类型列表中选择所需类型，然后单击 OK 按钮以更改变量的类型。请注意，如果类型更改，值将被初始化。

您还可以选择多个变量的类型，并按 ENTER 一次性更改它们。
（您可以通过按SHIFT+向上/向下箭头键选择多个连续单元格。或者，您可以在按住 CTRL 键的同时触摸多个单元格进行选择。）

![](../../../_assets/tp630/panel-gvar/gv-sel-multi-type.png)


##### 重命名变量

选择您想要的变量的 `名称 (name)` 列，然后打开软键盘输入新名称。
按 ENTER 键将其更改为您输入的名称。

![](../../../_assets/tp630/panel-gvar/gv-edit-name.png)


##### 创建变量

在顶部的过滤器中输入您要创建的变量名称。

![](../../../_assets/tp630/panel-gvar/gv-new.png)

确认没有重复名称的变量，然后单击过滤器旁边的 + 按钮。变量将以默认类型 `int`（整数）创建。使用上述方法更改创建的变量的类型。


![](../../../_assets/tp630/panel-gvar/gv-new2.png)


##### 删除变量

选择您要删除的变量。
按 DEL (CTRL+BACKSPACE) 键以显示确认/取消对话框。确认变量名称后，按 OK 按钮。

![](../../../_assets/tp630/panel-gvar/gv-delete.png)
[__SOURCE](6-monitoring/3-job/3-global-variable/2-array-object.md)
# 6.3.3.2 数组和对象

##### 创建数组

我们现在将使用一个生成 5x200 的二维姿态数组变量 `pos` 的示例。
使用上述描述的方法创建一个名为 `pos` 的变量。

![](../../../_assets/tp630/panel-gvar/gv-new-arr1.png)

选择 `类型 (type)` 列并按下 ENTER 键。创建变量对话框如下所示。

![](../../../_assets/tp630/panel-gvar/gv-new-arr2.png)

在类型列表中选择 `姿势 (Pose)`。如果输入 5,200 作为元素的数量并按下 OK 按钮，pos 的类型将变为 Pose[5][200] 的数组。

![](../../../_assets/tp630/panel-gvar/gv-new-arr3.png)

{% hint style="warning" %}
`[Warning]` 请注意，定义一个过大的数组可能会导致保存或加载的时间更长，并可能在断电的情况下无法自动保存。
{% endhint %}


##### 查看和更改数组元素值

数组变量的值仅显示为 []，元素的值不显示。
选择 `值 (value)` 列并按下 ENTER 键或点击 [F5: sub.level] 按钮以展开数组到下一级并查看元素值。

![](../../../_assets/tp630/panel-gvar/gv-arr-level1.png)

您还可以通过上述描述的方法更改数组元素的值或类型。

在二维数组 `pos` 中，`pos[0]` ~ `pos[4]` 也是数组。按 ENTER 或 [F5] 继续进入下一级。当前显示的数组的级别和索引可以在全局变量面板的标题栏中找到。

点击 [F4: up.level] 按钮或按 ESC 键返回到上一级。

![](../../../_assets/tp630/panel-gvar/gv-arr-level2.png)

因为数组一次只显示 100 个元素，默认情况下您只能看到 [0] 到 [99] 的索引范围。如果更改左上角的起始索引编辑框中的值，您可以查看其他元素范围。例如，如果在 `/pos[4]` 的起始索引中输入 190，则可以看到 [190]~[199] 的元素。

##### 查看和更改对象属性值

选择对象变量的 `值 (value)` 列并按下 ENTER 键或点击 [F5: sub.level] 按钮以展开对象到下一级并查看属性值。操作方法与数组变量类似。然而，启动索引编辑框不使用。

![](../../../_assets/tp630/panel-gvar/gv-obj2.png)




<br>

##### 固定变量

例如，您已经在全局变量窗口中创建了大量名为 `weld_points` 的姿态，通过执行以下赋值语句可以删除所有数据。

```python
weld_points=0
```

通过将变量指定为固定，您可以防止此错误。

![](../../../_assets/tp630/panel-gvar/fixed-var.png)

如果在全局变量窗口的顶层选择数组变量并按下 [F4: toggle fixed]，类型将从 'array' 更改为 'F.array'（固定数组）。
如果指定为固定变量，则无法分配其他值。当 `weld_points` 是一个固定的二维数组时，以下每个赋值语句的结果与注释相同。

```python
global weld_points  # ignored.
global weld_points=0  # cannot assign error occurs
weld_points=0  # cannot assign error occurs
weld_points[2]=Array[30]  # new value can be assigned to an element
weld_points[2][1]="light"  # new value can be assigned to an element
weld_points[2][1].j2=90.5  # new value can be assigned to an property
```

如果再次执行 [F4: toggle fixed]，固定将被释放，`F.array` 将恢复为 `array`。
[__SOURCE](6-monitoring/3-job/3-global-variable/3-var-files.md)
# 6.3.3.3 变量文件

变量值也会以文件形式保存，因为即使在关机时也必须保留它们，而全局变量根据类型以两种形式存储：

<table>
  <thead>
    <tr>
      <th style="text-align:left">类型</th>
      <th style="text-align:left">路径</th>
      <th style="text-align:left">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        全局根数组变量
      </td>
      <td style="text-align:left">MAIN/project/vars/*.csv</td>
      <td style="text-align:left">为每个变量创建一个文件，文件标题与变量名称相同。</td>
    </tr>
	 <tr>
      <td style="text-align:left">
        其他变量
      </td>
      <td style="text-align:left">MAIN/project/vars/vars.json</td>
      <td style="text-align:left">所有其他全局变量作为一个文件保存。</td>
    </tr>
	</tbody>
</table>

<br>


##### vars/.csv 文件

当您在文件管理器中打开文件夹 `MAIN/project/vars/` 时，将创建一个名为 `weld_points.csv` 的文件。指定为预定义的变量创建一个与变量名称相同的 .csv 文件，当从预定义中释放时，该文件会被自动删除。

![](../../../_assets/tp630/panel-gvar/csv0.png)

通过 USB 存储器或 FTP 复制此文件，并在您的 PC 上打开它。 .csv 文件是一种非常简单的文本格式标准，表示以逗号分隔的值。

参考： [维基百科：逗号分隔值](https://en.wikipedia.org/wiki/Comma-separated_values)

该 .csv 文件表示一个单一的二维表。列通过逗号分隔，行通过换行符分隔。

![](../../../_assets/tp630/panel-gvar/csv1.png)

csv 文件按顺序包含构建 `weld_points` 二维数组的过程。

对于每一行，第一列是索引，第二列是类型，第三至最后一列是值。第一行将其描述为表的标题。

第二行是创建顶层的行，即 `weld_points` 本身。因此，索引列为空，类型为数组，数字为 10。换句话说，创建了 weld_points[10]，并用零填充了 10 个元素。

```python
, , array, 10
```

以下行生成并分配姿态类型值给 `weld_points[0]` 的元素。

```python
[0][0][0], Pose, 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
[0][0][1], Pose, 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
...
```

如果对 `weld_points[0]` 执行 100 行，以下行将跟随 `weld_points[1]` 的操作，如下所示：

```python
[1][1], array; 100
[1][1][0], Pose; 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
[1][1][1], Pose; 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
[1][1][2], Pose; 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
...
```

您可以在文件管理器中双击 .csv 文件以使用 Microsoft Excel 打开并进行编辑。编辑完成时按 `Ctrl+S` 或 `保存 (Save)` 按钮保存。

![](../../../_assets/tp630/panel-gvar/csv2.png)

在 Excel 中保存会导致不必要的逗号，如下所示，坐标系中的引号消失，导致格式略有变化。这是因为 Excel 以这样的方式处理 .csv。无论如何，${cont_model} 控制器也能够识别这种格式，因此没关系。

```python
, , array,10,,,,,,
[0][0], array,100,,,,,,
[0][0][0], Pose,0,90,10,0,20,0,
[0][0][1], Pose,0,0,0,0,0,0,base
[0][0][2], Pose,0,10,0,0,0,0,robot
[0][0][3], Pose,0,20,0,0,0,0,base
[0][0][4], Pose,0,0,0,0,0,0,base
[0][0][5], Pose,0,0,0,0,0,0,base
```

<br>

##### 加载 .csv

您可以将编辑后的文件覆盖到 `MAIN/project/vars/` 中，但它不会自动反映到内存中。

当您在全局变量窗口中单击 [F2: load all] 按钮时，`vars/` 文件夹中的所有变量文件将重新加载到内存中。
(请注意，删除变量文件并单击 [F2: load all] 也会删除内存中对应的变量。)

![](../../../_assets/tp630/panel-gvar/fixed-var.png)
[__SOURCE](6-monitoring/3-job/4-local-variable.md)
# 6.3.4 本地变量

显示当前调用框架的所有本地变量的列表。您不能创建/删除变量或更改变量名称或类型，但可以编辑值。

1. 分割屏幕并按左下角的 [Select] 按钮。

![](../../_assets/tp630/panel-split.png)
&nbsp;
![](../../_assets/tp630/panel-sel.png)

2. 在面板选择窗口中，触摸 `[local variable]`。`局部变量 (local variables)` 面板打开。

![](../../_assets/tp630/pane-lvar.png)

3. 检查变量名称、类型和值。更改变量值的方法与上一节中描述的全局变量相同。

![](../../_assets/tp630/pane-lvar-mon.png)
[__SOURCE](6-monitoring/3-job/5-watch.md)
# 6.3.5 观察

您可以将变量或表达式注册到观察面板以监控或更改值。


#### 打开观察面板

1. 分割屏幕并按左下角的 [选择] 按钮。

![](../../_assets/tp630/panel-split.png)
&nbsp;
![](../../_assets/tp630/panel-sel.png)

2. 在面板选择窗口中触摸 `Watch`。各种数据窗口打开。

![](../../_assets/tp630/panel-watch/panel-watch.png)

![](../../_assets/tp630/panel-watch/panel-watch-mon.png)


#### 如何使用

在顶部输入框中输入所需的变量或表达式，然后单击 '+' 按钮将新项目输入到表中。

![](../../_assets/tp630/panel-watch/panel-watch2.png)


您可以通过再次单击 `名称 (Name)` 列来修改您输入的变量名称或表达式。

![](../../_assets/tp630/panel-watch/panel-watch-rename.png)

如果您在 `力控制变量 (Value)` 列中单击以输入新值，您将更改该变量的值。更改表达式的值将被忽略。

选择姿态/偏移变量或表达式的 `力控制变量 (Value)` 列，然后按 `确认 (ENTER)` 键打开姿态/偏移属性窗口以查看和修改值。

![](../../_assets/tp630/panel-gvar/gv-edit-pose2.png)

要删除一行，选择该行并按 `SHIFT+DEL` 键。

如果您按下底部 F 按钮上的 [F7: 保存所有] 按钮，输入的变量和表达式列表将保存在 `cfg/watch.json` 文件中。此文件将在电源重启时自动加载。
您还可以通过 FTP 接收并编辑列表。如果您用编辑过的文件覆盖 `cfg/` 文件夹并单击 [F1: 加载所有] 按钮，它将应用于观察面板。

![](../../_assets/tp630/panel-watch/panel-watch-fbt.png)

单击 [F2: 向上交换] 和 [F3: 向下交换] 按钮以在与顶部和底部行交换的同时移动当前选定行的位置。  

在各种数据窗口中共有 10 页，因此您可以分组和管理您想要显示的变量或表达式。单击 [F4: 页面] 按钮以显示下一页，单击 `SHIFT`+[F4: 页面] 按钮以显示上一页。

可以使用 [F6: 子级] 按钮或 `确认 (ENTER)` 键查看数组或对象的元素，并可以使用 [F5: 上级] 按钮或 `ESC` 键上移到上一级。

您可以在 `起始索引` 编辑框中输入一个值，以从特定索引显示数组。([全局变量](3-global-variable/README?cont_model=${cont_model}) 窗口也有相同的操作方法。)

{% hint style="warning" %}
* 要更新结果值的显示，表达式会在快速的周期内反复计算。请注意不要在表达式中包含会导致系统特定创建或更改的函数，例如 mkucs()。
{% endhint %}
[__SOURCE](6-monitoring/3-job/6-call-stack.md)
# 6.3.6 调用堆栈

在面板选择窗口中点击 `[Call Stack]` 以显示调用堆栈窗口。要理解本节内容，必须先了解 `call`~`return` 语句和 hrscript 的局部变量。

[调用、跳转语句和子程序](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/3-flowcontrol-subprogram/7-call-jump/README?cont_model=${cont_model})

[局部变量](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/3-flowcontrol-subprogram/8-local-global-var/1-local-variables?cont_model=${cont_model})


### 机器人语言的调用和返回

在机器人语言中，可以使用 `call` 语句调用一个子作业程序。当执行 `end` 或 `return` 语句时，子程序返回到调用它的 `call` 语句的下一语句位置。例如，在下图中，您可以看到作业 5 调用作业 8，运行到 `return` 语句，然后继续执行作业 5 的 `call` 语句的下一语句。

![子作业的调用和返回](../../_assets/call-return.png)

绘制在程序旁边的容器形状是一个称为调用堆栈的存储空间。调用堆栈构建当前运行程序的调用帧。调用帧包含一组实际参数和局部变量以及作业程序的返回地址。  
因为在调用子程序时，新调用帧被推到顶部，所以调用它的程序的局部变量被保留，并准备了一个新的局部变量空间。  
当子程序返回时，顶部的调用帧被丢弃（弹出），下面的调用帧再次变为顶部。因为调用帧保留了调用前的实际参数和区域变量，并且还具有返回的位置信息，所以被调用的程序可以继续执行在调用之前正在进行的任务。


### 调用堆栈面板

您可以在调用堆栈面板中查看当前调用堆栈的内容。
<br><br>

0001_main.job
```python
var n_work=10
call 0005_init,12
end
```

0005_init.job
```python
param mode
var sensor_id
call 0008_go_home
for sensor_id=1 to 5
  call 0009_check_sensor,sensor_id # --------- (A)
next
end
```

0008_go_home.job
```python
var pos1, pos2
# 做某事
end
```

0009_check_sensor.job
```python
param id
var sensor_value
# 做某事 --------- (B)
end
```

在作业编辑窗口、调用堆栈面板和局部变量面板打开的情况下，如果当前程序处于作业 5 的 `for`~`next` 循环中第三次执行的 `call` 语句并执行到 (B) 位置，教学挂件屏幕将显示如下状态。

![作业编辑、调用堆栈、局部变量](../../_assets/call-stack.png)


调用堆栈的底部帧是作业 1，中间帧是作业 5，顶部帧是作业 9。> 形状的光标指向作业 9，并且局部变量面板显示参数 ` (id)` 和局部变量 `sensor_value` 的值。因此，您可以检查作业 9 是被作业 5 调用的，而作业 5 是被作业 1 调用的。  
如果您想查看作业 5 调用的位置，请选择作业 5 的帧并按 `确认 (ENTER)` 键。作业编辑面板中的光标将立即移动到 (A) 位置，以显示调用的位置。局部变量面板显示作业 5 的帧内容，即参数 `模式 (mode)` 和局部变量 `sensor_id`，分别为 12 和 3 的值。

![作业编辑、调用堆栈、局部变量- 2](../../_assets/call-stack2.png)

通过选择被调用作业的帧，您可以轻松理解到目前为止的程序流。

{% hint style="warning" %}
`[caution]` 在进行步进向前 (Step-FWD) 或播放操作时，确保在恢复操作时将 > 光标恢复到顶部帧位置。否则，将认为作业光标的位置发生了变化，并将初始化调用堆栈。
{% endhint %}
[__SOURCE](6-monitoring/3-job/7-multi-task.md)
# 6.3.7 多任务

在面板选择窗口中触摸 `[multitask]`。
这将显示在主任务和子任务 1 - 7 中自动运行的程序的信息，包括步骤、功能、操作状态和工作状态。

![](../../_assets/tp630/pane-multi-task_eng.png)

<br>

{% hint style="info" %}
有关详细信息，请参阅 ["${cont_model} 控制器多任务功能手册"](https://hrbook-hrc.web.app/#/view/doc-multi-task/zh/README?cont_model=${cont_model})。
{% endhint %}
[__SOURCE](6-monitoring/3-job/8-program-reservation.md)
# 6.3.8 程序预留执行

为了进行监视，需进行预设。您必须在`系统 - 2:控制参数 - 7:程序预留执行 (system - 2:Control parameter - 7:Program reservation execution)`页面上选择注册号为20EA或1EA。

![](../../_assets/tp630/ctrl-prog-reserve_eng.png)

在面板选择窗口中，触摸`[program reserve]`。然后，计划的程序执行窗口将出现。

当通过外部信号安排程序并按计划顺序执行时，您可以在计划程序列表中检查和更改状态。

![Figure 50 Program reserve](../../_assets/tp630/pane-prog-reserv_eng.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>计划程序的列表。您可以安排1–20个程序。</p>
        <ul>
          <li>当在远程模式下执行的程序终止时，程序将根据计划顺序自动执行。</li>
          <li>当计划程序执行完成后，这些程序将从列表中删除。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[编辑]</b>: 您可以编辑计划程序的列表。</li>
          <li><b>[插入]</b>: 您可以将一个将在计划中执行的程序添加到计划程序列表中。</li>
          <li><b>[删除]</b>: 您可以从计划程序列表中删除一个已安排的程序。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>



{% hint style="info" %}
* 仅当应用功能中的传感器同步功能的同步状态设为输送机或压力时，`[Program reserve]`项目才会被激活。
* 如果`[system - 2: Control Parameter - 8: Program reserve] ([system  - 2: Control Parameter  - 8: Program reserve])`菜单中的`[Applied Register Count]`选项被设为禁用，则`[Program reserve]`项目将不会被激活。
* 有关计划程序执行的详细信息，请参阅"${cont_model}控制器计划程序执行功能手册"。
{% endhint %}
[__SOURCE](6-monitoring/4-system/README.md)
# 6.4 系统
[__SOURCE](6-monitoring/4-system/1-system-spec.md)
# 6.4.1 系统字符

在面板选择窗口中，触摸 `[System character]`。然后，系统字符窗口将出现。

您可以检查机器人系统的所有各种数据或仅检查特定类型的信息数据。

![](../../_assets/tp630/pane-syscharacter_eng.png)

| No. | 描述 |
| :--- | :--- |
| ![](../../_assets/c1.png) | 显示机器人系统的数据。您可以通过选择上面显示的特定信息类型来检查特定类型的详细数据。 |
| ![](../../_assets/c2.png) | `[clear]`：除了每个轴的运动之外，您可以按类型将系统数据的最大值初始化为当前值。 |

{% hint style="info" %}
系统字符监控功能仅在工程师模式下可用。
{% endhint %}

{% hint style="warning" %}
* 在工程师模式下，工程师模式图标 \(![](../../_assets/eng-mode.png)\) 将在状态栏上闪烁。
* 请谨慎操作，因为如果设置不正确，机器人系统可能会出现严重问题。
{% endhint %}

<Br> 

### 初始化

您可以通过选择要初始化的信息类型来初始化数据的最大值。

1. 触摸系统属性窗口底部的 `[Clear]` 按钮。

2. 触摸您想要初始化的信息类型。然后，所选项的最大值将被初始化为当前值。

![](../../_assets/tp630/pane-syscharacter-clear_eng.png)
[__SOURCE](6-monitoring/4-system/2-system-diagnosis/README.md)
# 6.4.2 系统诊断

在面板选择窗口中触摸`System Diagnostics`。
首次执行时，出现刹车诊断屏幕。

![System diagnostics monitoring](../../../_assets/tp630/pane-sys-diagnosis_eng.png)

<table> 
  <thead> 
    <tr> 
      <th style="text-align:left">编号</th> 
      <th style="text-align:left">描述</th> 
    </tr> 
  </thead> 
  <tbody> 
    <tr> 
      <td style="text-align:left"> <img src="../../../_assets/c1.png" alt/> 
      </td> 
      <td style="text-align:left"> 
        <p> 当<strong>[System Diagnostics]</strong>面板被选中时，可以通过点击下面的按钮切换到其他诊断项目。 </p> 
        <ul> 
          <li><strong>[Brake Diagnostics]</strong>: 切换到刹车诊断屏幕。</li> 
          <li><strong>[Gas Spring Diagnostics]</strong>: 切换到气弹簧诊断屏幕。</li> 
        </ul> 
      </td> 
    </tr> 
  </tbody> 
</table>
[__SOURCE](6-monitoring/4-system/2-system-diagnosis/1-brake-check.md)
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
[__SOURCE](6-monitoring/4-system/2-system-diagnosis/2-gas-pressure-check.md)
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
[__SOURCE](6-monitoring/4-system/3-system-task.md)
# 6.4.3 任务监视器


在面板选择窗口中，触摸 `[任务监视器]`。然后，任务窗口将出现。

您可以检查每个任务的操作周期和执行时间信息。

![图 45 任务监视器](../../_assets/tp630/pane-task_eng.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
          <ul>显示每个任务的操作周期和执行时间信息</ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[周期时间]/[执行时间]</b>: 您可以更改每个任务的信息类型。</li>
          <li><b>[初始化]</b>: 您可以初始化显示的信息。</li>
          <li><b>[计数器]</b>: 通过检查增加的计数器，您可以将任务视为正常。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](6-monitoring/4-system/4-hw-monitoring.md)
# 6.4.4 硬件

 在面板选择窗口中，触摸 `[hardware]`。您可以监控 COM 模块的当前电压和温度。如果状态值超出公差范围，将会在 24 小时内发出警告信息。

 ![](../../_assets/tp630/pane-hw-monitoring_eng.png)
 
 
- 如果您想更改公差，请选择相应的单元格并进行编辑。然后，按 [Save Min/Max] 按钮。
- 如果您想用默认值初始化，请按 [Reset Min/Max] 按钮。
[__SOURCE](6-monitoring/5-appl/README.md)
# 6.5 高级功能和机器人应用
[__SOURCE](6-monitoring/5-appl/1-sensor-sync.md)
# 6.5.1 传感器同步

在面板选择窗口中触碰 `[Sensor Sync]`。然后，传感器同步窗口将出现。

您可以查看与传送带相关的信息并按下同步功能。传感器同步功能可以通过在 `[system - 4: Application Parameter - 4: Sensor Sync] ([system  - 4: Application Parameter  - 4: Sensor Sync])` 菜单中设置同步状态为传送带或按压来激活。

![Figure 49 Sensor Sync Monitoring](../../_assets/tp630/pane-sensorsynch_eng.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left"> <ul>显示与所选传感器的传送带和压力同步功能相关的信息</ul></td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[Sensor #1]</b>: 您可以通过触碰下拉菜单选择一个传感器进行监控。</li>
          <li><b>[Manual reset]</b>: 您可以手动删除各种传感器相关的数据（编码脉冲、传感器位置、传感器速度、工件进入计数、同步播放状态等）。</li>
          <li><b>[Limit Switch Operate]</b>: 输入时可以使用此功能。</li>
          <li><b>[Work Position Input]</b>: 您可以手动输入传感器位置值（线性：毫米。圆形：度）。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>



{% hint style="info" %}
有关传感器同步功能的详细信息，请参阅 ["${cont_model} Sensor Sync Function Manual."](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/zh/README?cont_model=${cont_model})
{% endhint %}
[__SOURCE](6-monitoring/5-appl/2-coldet-monitoring.md)
# 6.5.2 ColDet 监控

 ![](../../_assets/tp630/coldet_monitoring_pane.png)
 ![](../../_assets/tp630/coldet_monitoring.png)
 
#### 描述 
* ColDet 监控 

#### 参数 
 - [灵敏度] : 比例值越高，检测到的碰撞越敏感。 (0: 禁用) [0~200]
   - 可在常规标签中设置 [系统- 3:机器人参数>14:冲击检测]  
 - [外部扭矩]-[当前] : 当前估计的外部扭矩 [Nm]
 - [外部扭矩]-[最大] : 当前外部扭矩的最大值 [Nm]
 - [参考] : 阈值扭矩 [Nm]
 - [最大/参考] : 比例 [最大] 与 [参考]，如果该值超过一，轴向冲击将发生。
[__SOURCE](6-monitoring/5-appl/10-spot.md)
# 6.5.10 点焊数据

在面板选择窗口中触摸 `[spot]`。
这将显示点焊枪的轴数据、输入/输出信号和点焊的操作信息。

![](../../_assets/tp630/pane-spot_eng.png) 

<br>

{% hint style="info" %}
 更多详细信息请参阅点焊手册的 "[3.1 监控](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/3-Related-functions/3-1-monitoring/README?cont_model=${cont_model})"。
{% endhint %}
[__SOURCE](6-monitoring/5-appl/11-tool-change.md)
# 6.5.11 伺服工具更换

在面板选择窗口中，触摸 `[servo tool change]`。这会显示伺服工具和编码器电源供应的输入/输出状态，当伺服工具更换功能被使用时。

![](../../_assets/tp630/pane-tool-change_eng.png) 

<br>

{% hint style="info" %}
 详细信息请参见 ["${cont_model} 控制器伺服工具更换功能手册"](https://hrbook-hrc.web.app/#/view/doc-svtool-change/zh/README?cont_model=${cont_model})。
{% endhint %}
[__SOURCE](6-monitoring/5-appl/20-arc.md)
# 6.5.20 弧焊数据

Refer to Arc Welding Manual's "[7. 焊接数据监控](https://hrbook-hrc.web.app/#/view/doc-arc-weld/zh/7_Monitoring/README?cont_model=${cont_model})".
[__SOURCE](6-monitoring/5-appl/28-forcecontrol-monitoring.md)
# 6.5.28 力控制监测
 
![](../../_assets/tp630/force_monitoring.png)

#### 描述 
* 在力控制的情况下，该监测数据会显示估计的 [外部力] 
 
#### 参数 

 - [cartesian] : 符号空间中的外部力或扭矩
    - 在 fctrl 函数的情况下 : 机器人坐标
    - 在 softxyz 函数的情况下 : 机器人坐标
    - 在 softjoint 函数的情况下 : 不显示 
 - [joint] : 关节空间中的外部扭矩    
    - 在 fctrl 函数的情况下 : 不显示
    - 在 softxyz 函数的情况下 : 不显示
    - 在 softjoint 函数的情况下 : 关节坐标 
[__SOURCE](6-monitoring/6-safety-funtion.md)
# 6.6 安全功能

{% hint style="info" %}
此功能在 Hi7 控制器中支持。
{% endhint %}

在面板选择窗口中，触摸 `[Safety Function]`。然后，安全功能状态窗口将出现。
您可以检查安全功能、手动速度、停止时间、停止距离、MCU-A 和 MCU-B 的状态。

![](../_assets/image_552.png)

{% hint style="info" %}
* 有关安全功能的详细信息，请参考 "[SafeSpace2.0 手册](https://hrbook-hrc.web.app/#/view/doc-safespace2.0/zh/README)"。
{% endhint %}
[__SOURCE](7-system/README.md)
# 7. 系统

在“系统”中，您可以检查和设置用户信息以及各种参数信息。
[__SOURCE](7-system/1-setting-menu.md)
# 7.1 在 'system' 中使用菜单

1. 在手动或自动模式下，触摸功能按钮栏上的 `[system]` 按钮。然后，程序的设置菜单将被显示。

    ![](../_assets/tp630/sbt-system_eng.png)

2. 你可以通过选择所需的菜单来检查和设置用户信息和各种参数信息。

    ![](../_assets/tp630/sbt-system-menu_eng.png)

* `[1: User Environment]`：你可以检查和设置各种用户条件。
* 
  `[2: Control Parameter]`：你可以设置控制器和输入/输出信号的各种条件，通信信息，机器人准备信号条件，归位信号和坐标系统。

* 
  `[3: Robot Parameter]`：你可以设置与机器人操作和信息相关的各种数据，例如每个轴的原点和操作范围。

* `[4: Application Parameter]`：你可以检查和设置使用机器人应用功能的各种参数。
* 
  `[5: Initialize]`：你可以执行机器系统的初始设置。你还可以初始化串行编码器。

* 
  `[6: Auto Calibration]`：你可以使用教导程序来校准机器人轴原点、工具长度、负载质量和基轴方向等，也可以通过使用将自动操作的运动来进行校准。
[__SOURCE](7-system/2-user-environment.md)
# 7.2 用户环境

您可以检查和设置各种用户条件。

1. 触摸 `[1: 用户环境]` 菜单。然后，用户环境设置窗口将出现。

2. 设置用户环境后，触摸 `[OK]` 按钮。

    ![](../_assets/tp630/system-user-environ_eng.png)

* `1: 姿势记录类型 (1: Pose record type)`：您可以设置要记录为隐藏姿势的步骤的位置记录类型。 ("[2.3.1.2 Pose](../2-operation/3-step/1-step-cmd-param/2-pose.md)")
  * `[Base]`/`[Robot]`/`[Axis Angle]`：您可以根据基本坐标、机器人和轴角值记录步骤的位置。

  * `[U]`：您可以在用户坐标系统中记录位置。
* `2: 删除命令时的确认 (2: Confirmation in deleting commands)` 您可以设置在手动模式下删除语句时是否显示删除确认窗口。

* `3: Wait\(di/wi\) release`：在输入信号等待或焊接完成信号待机状态下，您可以设置是否通过按 `[SHIFT]` + [rel.WAIT] 强制解除信号等待状态。
* `4: 程序触发信号使用 (4: Program strobe signal use)`：选择外部程序时，通过接收外部数字信号，您可以设置选择外部程序的时间。

  * `[Disable]`：仅通过读取外部程序选择信号来选择外部程序。

  * `[Enable]`：在输入程序触发信号时，通过读取外部程序选择信号来选择外部程序。

* `5: 播放程序的外部更新 (5: Ext. update of playback prog.)`：您可以设置是否允许外部 \(PC\) 修改正在回放的程序，然后允许将其下载到控制器中 \(关于正在回放的程序编号，下载的程序将从下一个周期开始应用\)。

{% hint style="warning" %}
如果正在回放的程序被外部 \(PC\) 修改并下载到控制器，可能会导致产品故障或异常。请联系客户支持团队以咨询专家或工程师。
{% endhint %}


* `[6: 碰撞传感器处理]`：您可以设置在碰撞传感器操作时停止机器人的方法。
  * `[(1) Em.stop]`：机器人将进入紧急停止模式，机器人处于掉落电机关闭状态。

  * `[(2) Stop]`：机器人将进入正常停止模式，机器人保持在电机开启状态。

* `[7: 以字节显示信号]`：您可以通过选择 `[Enable]` 以字节单位显示信号地址。
  * '输入信号分配' 页面根据您的选择如下更改。
  
    ![](../_assets/tp630/system-user-environ-byte-index_eng.png)

* `8: 手动操作停止信号时`：您可以设置在输入外部停止信号时是否启用走动操作。

* `[9: 教学挂钩断开]`：您可以将教学挂钩从控制器断开，以在自动模式下操作机器人。

  * 如果设置为 `断开 (Disconnect)`，在教学挂钩与主板之间的通信断开时不会出现 "E2800 教学挂钩操作异常" 错误。 （即使在通信断开时，机器人仍然可以操作。）

  * 在 `连接 (Connect)` 状态下，您可以设置超时期限来确定通信是否丢失。

  * 当设置为 `断开 (Disconnect)` 并且教学挂钩从控制器断开且供电时，控制器将识别当前模式为远程模式，允许通过外部电机开启和外部启动进行自动操作。

  * 如果将其设置为 `连接 (Connect)`，教学挂钩与主板之间的通信故障将触发 "E2800 教学挂钩通信错误"，导致电机关闭。 （输入工程师代码 (R314) 后，您可以配置通信超时持续时间。）

  * 因为紧急开关和模式转换开关通过信号线单独连接到教学挂钩，所以必须适当布线该信号线。

  * 将 CNRTP 连接器针脚 #9 (Auto) 连接到 #2 (M1)，并将针脚 #5 (Emergency stop 1) 连接到 #2 (M1)，使用专用 CNRTP 连接器，将针脚 #6 (Emergency stop 2) 连接到 #1 (P1) 代替教学挂钩。
[__SOURCE](7-system/3-control-parameter/README.md)
# 7.3 控制参数

您可以设置控制器的各种条件，并设置输入/输出信号、通信信息、机器人准备就绪信号条件、原点信号和坐标系。

1.	触摸`[2: Control parameter]`菜单。然后，控制参数菜单将出现。

2.	选择所需的菜单，检查并设置控制器的各种条件。

    ![](../../_assets/tp630/ctrl-menu_eng.png)
[__SOURCE](7-system/3-control-parameter/1-control-env-setting.md)
# 7.3.1 控制环境设置

您可以设置控制器的各种条件并执行必要的操作。

1. 触摸 `[2: Control Parameter - 1: Control Environment Setting] ([2: Control Parameter  - 1: Control Environment Setting])` 菜单。

2. 设置每个控制环境条件后，触摸 `[OK]` 按钮。

    ![](../../_assets/tp630/ctrl-environment-setting_eng.png)   

* `[节能功能]`：您可以设置是否使用节能功能并设置等待时间。

  当使用节能功能时，如果机器人在自动模式中长时间处于操作停止状态，等待启动或等待输入信号，等候时间到时会切断电机的电源，从而帮助节省能耗。当在机器人中输入操作命令时，节能功能将自动停用，电源将供应给电机，机器人将开始操作。

{% hint style="info" %}
在启用/禁用节能功能的过程中可能会发生延迟。当期望机器人的速度进行操作时，应将节能功能设置为禁用。
{% endhint %}

* `[自动模式下的路径恢复]`：您可以设置自动模式下的路径恢复允许距离和允许角度。

  在路径恢复过程中，如果距离和角度超过设定的允许范围，将检测到错误。如果允许距离设置为1，则不会进行路径恢复。

* `[冷却风扇关闭时间]`：当机器人在运行时，由于再生电阻，控制器内部的温度会升高，必须开启冷却风扇以防止温度上升。

  当机器人不运行时，控制器内部的温度不再上升，因此此时没有必要让冷却风扇运转。相反，当冷却风扇运转时，只会出现风扇寿命缩短、噪音产生和能耗增加等不利影响。

  当机器人处于操作状态（电机开启）时，冷却风扇必须立即运行。当机器人处于不可操作状态（电机关闭，节能运行）时，冷却风扇在经过一定时间后将不再运转。如果冷却风扇没有立即运转，由于再生电阻的潜热，控制器内部的温度会上升。

  控制冷却风扇开/关操作的信号输出在 `[System/Control parameter/Input/Output signal setting/Output signal assign]` 菜单中的 "冷却风扇控制" 项目中设置，控制冷却风扇电源的电路也通过此输出信号创建。必须进行配置。

  如果 "冷却风扇关闭操作时间" 设置为0或 "冷却风扇控制" 输出信号设置为-1，则冷却风扇会始终运转。

* `[互锁错误时间]`：此功能设置输入信号的最大等待时间。 <br>
  如果输入信号待机时间在播放期间超过指定时间，将输出互锁错误信号。此指定时间为互锁异常时间。

  互锁错误信号是分配给 `[System/Control Parameter/Input/Output signal setting/Output signal assign]` 菜单中的 "互锁异常警告" 的信号。

* `[第一次安全移动]`：启动机器人时，设置是否将第一次步骤限制为安全速度，并以当前设定速度移动。
  * 启用：移动到安全限制速度。
  * 禁用：以当前设定速度移动。

  出于安全原因，机器人在启动第一次步骤时以安全速度移动是基本的。特殊工作如密封或喷涂可能会导致质量问题，因此仅在这些情况下使用。

* `[PLC执行时间比率]`：使用嵌入式PLC时，您可以调整控制器内部的PLC执行时间。控制器每5ms内部执行一次PLC梯形图程序，因此设置分配多少PLC执行。这个比例越大，PLC程序的扫描时间越短。但如果过大，CPU执行时间可能不足，可能会发生任务执行时间超出错误。

* `[周期时间优化模式]`：此功能在自动播放期间减少机器人的步进移动时间，以提高生产力。
  - 启用
    - 动态调整加速/减速曲线和最大速度，以便更快移动。
    - 应用动态运动调整

  - 禁用
    - 使用预定义的加速、减速和最大速度设置。
    - 在标准运动特征模式下运行

  - 动态运动比率 (`0 ~ 100`)
    - `0`：禁用（静态运动）
    - `1 ~ 100`：调整动态运动的强度
    - 较高的值适用更激进的速度和加速度优化

{% hint style="info" %}
对于周期时间关键的过程（例如，重复的取放），应用高动态运动比率可以帮助提高通量。
{% endhint %}

{% hint style="warning" %}
请注意，较高的值可能会导致机械振动或触发过载故障，尤其是在高负载或快速方向变化时。
{% endhint %}
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/README.md)
# 7.3.2 输入/输出信号设置

1. 触摸 `2: 控制参数 - 2: 输入/输出信号设置 (2: 控制参数 - 2: 输入/输出信号设置)` 菜单。然后，输入/输出信号设置菜单将出现。

2. 选择所需的菜单并设置输入/输出信号属性和信号分配等。

    ![](../../../_assets/tp630/ctrl-inoutsing-menu_eng.png)
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/1-input-signal-prop.md)
# 7.3.2.1 输入信号属性

您可以设置一般输入信号的逻辑和名称。

1. 触摸 `2: 控制参数 - 2: 输入/输出信号设置 - 1: 输入信号属性 (2: 控制参数 - 2: 输入/输出信号设置 - 1: 输入信号属性)` 菜单。

2. 检查并设置一般输入信号列表，然后触摸 `[OK]` 按钮。

    ![](../../../_assets/tp630/ctrl-insignal-attri_eng.png)

* `[Append]`: 您可以将新的一般输入信号添加到列表中。
* `[Delete]`: 您可以从列表中删除一般输入信号。
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/2-output-signal-prop.md)
# 7.3.2.2 输出信号属性

您可以为常规输入信号设置逻辑、脉冲和名称。

1. 触摸 `2: 控制参数 - 2: 输入/输出信号设置 - 1: 输出信号属性 (2: 控制参数 - 2: 输入/输出信号设置 - 1: 输出信号属性)` 菜单。

2. 检查并设置常规输入信号列表，然后触摸 `[OK]` 按钮。

    ![](../../../_assets/tp630/ctrl-outsignal-attri_eng.png)

* `[Append]`: 您可以将一个新的常规输出信号添加到列表中。
* `[Delete]`: 您可以从列表中删除常规输出信号。
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/3-io-signal-set-info.md)
# 7.3.2.3 输入/输出信号设置信息

* `[Signal]`: 要应用属性的信号。fb块信号可以通过输入块编号、小数点和信号编号的顺序来指定。

  例如，如果您想指定块fb1的信号35，可以通过输入1.35来设置。

* 
  `[Negative Logic]`: 一般输入/输出信号的正逻辑和负逻辑如下所示。

![](../../../_assets/image_457.png)

* `[Pulse Count]`: 脉冲计数。这是脉冲的计数。如果设置为1到100之间的值，则会发生脉冲输出，如果设置为0，则会发生延迟输出。
* 
  `[Pulse On]`/`[Pulse Off]`: 这是脉冲输出或延迟输出发生时输出信号的开状态时间和关状态时间。

  根据脉冲属性值的脉冲输出示例如下。

* 
  脉冲输出：计数：3。开状态时间：1秒。关状态时间：0.2秒

![](../../../_assets/image_468.png)



* 延迟输出：计数：0。开状态时间：1秒。关状态时间：0.5秒

![](../../../_assets/image_464.png)

* `[Name]`: 一般输入/输出信号的名称
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/4-input-signal-assign.md)
# 7.3.2.4 输入信号分配

您可以使用控制器输入信号远程控制控制器的状态或操作。远程控制项中分配输入信号编号的方法如下。

1. 触摸 `2: 控制参数 - 2: 输入/输出信号设置 - 3: 输入信号分配 (2: 控制参数 - 2: 输入/输出信号设置 - 3: 输入信号分配)` 菜单。

2. 在远程控制项中输入输入信号编号后，触摸 `[OK]` 按钮。

    ![](../../../_assets/tp630/ctrl-insignal-assign_eng.png)

* `[Reset All]`: 您可以重置分配给所有远程控制项的输入信号编号。
* 
  `[Reset One]`: 您可以重置分配给所选远程控制项的输入信号编号。

* 
  `[Reset Channel]`: 您可以初始化设置的输入信号的输入通道。通道由 fb0 到 fb9 组成，显示中将省略 fb0 的情况。

* 
  `[S]`: 当使用远程控制作为系统输入信号时，您可以指定系统信号。系统信号由 "s+编号" 组成，将字母 s 与信号编号结合。例如，您可以将系统信号 49 设置为 s49。
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/5-input-signal-set-info.md)
# 7.3.2.5 输入信号设置信息

#### 远程模式

当教学挂钩的模式开关选择为远程 \(![](../../../_assets/sb-remote.png)\) 时，相应的信号应被开启，以便选择远程模式。如果相应的信号被关闭，将选择内部模式。一般来说，如果教学挂钩的模式开关选择为远程 \(![](../../../_assets/sb-remote.png)\)，用户希望选择远程模式，这就是基本值设定为 254 的原因，相应的信号将在输入信号属性中指定为负逻辑。

#### 手动（教学）模式

在选择远程模式时，如果相应的信号被开启，您将处于可以手动操作机器人在远程模式下的状态。然而，通常情况下，在这种状态下操作机器人是没有的，并且此模式很少使用。

#### 自动（回放）模式

在选择远程模式时，如果相应的信号被开启，您将处于可以自动操作机器人在远程模式下的状态。然而，通常情况下，如果教学挂钩的模式开关选择为远程 \(![](../../../_assets/sb-remote.png)\)，用户希望在远程模式下自动操作机器人，这就是基本值设定为 255 的原因，相应的信号将在信号属性中指定为负逻辑。

#### 外部启动

此功能用于在远程自动模式下启动机器人。

#### 外部停止

此功能用于在远程自动模式下停止机器人。

#### 外部程序选择

当机器人被外部启动时，读取程序选择位并确定为外部程序的时机取决于是否使用闪烁信号。

* 当程序闪烁信号使用设置为启用：如果在有外部启动输入的情况下程序闪烁信号处于开启状态，则将读取程序选择位，并且读取的值将被确定为程序编号。

![图51 当程序闪烁信号设置为 &amp;lt;启用&amp;gt; 的外部程序选择示意图](../../../_assets/image_438.png)

* 当程序闪烁信号使用设置为禁用：在有外部启动输入后，将读取程序选择位，如果此值在 90 ms 内未发生变化，将确定为程序编号。

![](../../../_assets/image_465.png)

#### 程序选择位和二进制/离散（关 -> 二进制）

程序选择位是输入外部启动信号时选择要执行的程序的信号组合。仅在当前在 TP 的头部或结束指向步骤时应用。当程序正在执行时，将执行程序至结束。

二进制/离散信号是一个选项，用于确定程序选择位的解释，如果为 0，将被识别为二进制，如果为 1，将被识别为离散。

例如，如果程序选择位设置如下，则根据输入要执行的 JOB 示例如下。

![](../../../_assets/image_436.png)

#### 外部重置

此功能用于通过外部信号执行与从教学挂钩执行 R0 步骤计数器重置功能相同的操作。当机器人启动时，此功能将不会操作。如果此功能正常操作，执行位置将移动到程序的开头，并且各种错误或警告的发生状态将被清除。有关此功能的信息，请参考 "[8.2 R0 重置步骤计数器](../../../8-r-code/2-r0.md)"。

#### 

#### 限速指令

此功能用于通过外部信号将机器人移动速度限制在安全速度 \(250 mm/s\) 以内。

#### 碰撞传感器

此功能用于检测机器人的碰撞并停止机器人。结合在 `[System - 1: User Environment - 6: Collision Sensor]` 菜单中的设置，将确定停止机器人的条件和信号逻辑。

#### 错误/警告信号清除

此功能用于通过外部信号清除各种错误和警告的发生状态。

#### 

#### 操纵杆模式

此功能用于手动操控机器人。一般在 LCD 宏检验设备中使用。有关使用该功能的详细手册，请参阅单独的功能手册。

#### 门开关

此功能用于在安全围栏的门打开时停止机器人移动。

#### 屏幕保护程序禁用

如果教学挂钩没有操作，当在 `[service - 11: Teach Pendant Option] ([service  - 11: Teach Pendant Option])` 菜单中设置的屏幕关闭时间到期时，教学挂钩将切换到屏幕保护状态。此功能用于通过外部信号打开教学挂钩的屏幕。

#### 外部电机开启

此功能用于从外部操作面板开启电机。

#### 外部电机关闭

此功能用于从外部操作面板关闭电机。
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/6-output-signal-assign.md)
# 7.3.2.6 输出信号分配

在控制器中发生的事件信息或状态信息可以通过控制器输出信号传送到外部。将输出信号分配给要传送到外部的信息的方法如下。

1.	触摸 `2: 控制参数 - 2: 输入/输出信号设置 - 4: 输出信号分配-主任务 (2: 控制参数  - 2: 输入/输出信号设置  - 4: 输出信号分配-主任务)` 菜单。

2.	在信息项中输入输出信号号码后，触摸 `[OK]` 按钮。

    ![](../../../_assets/tp630/ctrl-outsignal-assign_eng.png)

* `[Reset All]`: 您可以重置分配给所有信息项的输出信号的号码。
*  `[Reset One]`: 您可以重置分配给选定信息项的输出信号的号码。 
* 
  `[Reset Channel]`: 您可以重置分配给信息项的输出信号的输入通道 \(0-16: 数字信号\)

* 
  `[Previous Task]`/`[Next Task]`: 您可以移动到上一个或下一个任务屏幕。

* 
  `[S]`: 您可以在通过系统输入信号使用遥控器时指定系统信号。系统信号形式为 "s+数字"，将字母 s 与信号号码组合。例如，您可以将系统信号 49 设置为 s49。
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/7-output-signal-set-info.md)
# 7.3.2.7 输出信号设置信息

#### 远程模式

当教学挂件的模式开关选择为远程 \(![](../../../_assets/sb-remote.png)\) 时，应在信号输入分配部分设置输入信号为“打开”状态，以激活远程状态。此功能用于将状态输出到外部。

#### 手动 \(教学\) 模式

此功能用于将控制器的操作模式为手动的状态输出到外部。

#### 自动 \(回放\) 模式

此功能用于将控制器的操作模式为自动的状态输出到外部。

#### 电机开启

当通过输入电机开启信号为每个电机供电并准备好驱动时，此功能用于将状态输出到外部。

#### 机器人就绪 OK

当当前控制器状态满足在 `[system - 2: Control Parameter - 4: Robot Ready Condition] ([system  - 2: Control Parameter - 4: Robot Ready Condition])` 菜单中设定的所有条件时，此功能用于将状态输出到外部。

#### 机器人启动

当机器人通过手动模式的前进/后退操作启动或通过自动模式的启动信号输入启动时，此功能用于将此状态输出到外部。

#### 机器人移动

当机器人正在移动时，此功能用于将此状态输出到外部。

#### 机器人停止 \(保持\)

当机器人停止时，与启动信号的输出相反，此功能用于将此状态输出到外部。

#### 紧急停止

当来自教学挂件前面或控制器的紧急停止按钮的输入信号被输入时，此功能用于将状态输出到外部。

#### 紧急停止 \(外部\)

此功能用于将来自连接到系统板的外部紧急停止设备的信号输出到外部。

#### 低速模式

当在信号输入分配部分为低速命令设置的信号打开时，或当机器人在手动模式下以安全速度运行时，此功能用于将此状态输出到外部。

#### 程序结束

当在作业程序中执行结束循环时，此功能用于将此状态输出到外部。

#### 整体错误

控制器中发生的错误分为由系统错误引起的错误和由用户操作失误引起的错误。当因为系统错误而发生错误时，此功能用于将此状态输出到外部。由系统错误引起的错误范围为 1 到 999 和 2000 到 7999。

#### 操作错误

控制器中发生的错误分为由系统错误引起的错误和由用户操作失误引起的错误。当因为用户操作失误而发生错误时，此功能用于将此状态输出到外部。供参考，由系统错误引起的错误范围为 1 到 999 和 2000 到 7999。

#### 警告

当控制器中发生警告时，此功能用于将此状态输出到外部。

#### 碰撞传感器

当在信号输入分配部分设定的碰撞传感器信号输入打开，并确认机器人发生碰撞时，此功能用于将此状态输出到外部。

#### 步骤设定警告

在自动模式下，如果当前选择的光标位置与之前执行的位置不同，可能会有危险。此功能用于将此状态输出到外部。

#### 联锁异常警告

当作业程序的 wait 语句中的等待时间超过在 `[System - 2: Control Parameter - 1: Control Environment Setting]` 菜单中的 `[Interlock Abnormal Time]` 选项设定的时间时，此功能用于将此状态输出到外部。

错误/警告输出位，错误/警告输出选择和错误/警告输出闪烁

对于错误/警告输出位、错误/警告输出闪烁、整体异常、操作错误和警告发生信号，请参考以下顺序。

![Figure 53 16Bit Output](../../../_assets/image_456.png)

#### 外部复位确认

当在信号输入分配部分设定的外部复位信号打开时，此功能用于将此状态输出到外部。该信号将持续 200 毫秒，然后自动关闭。

#### 程序回显位

当通过在信号输入分配部分设定的程序选择位选择程序时，此功能用于将所选程序编号输出到外部。

#### 程序确认

当机器人通过在远程模式下输入外部启动信号启动时，此功能用于将状态输出到外部。该信号将持续 200 毫秒，然后自动关闭。

#### 弧焊异常

当发生与弧焊相关的错误时，此功能用于将此状态输出到外部。

#### 弧沉积警告

当在弧焊期间发生焊接沉积时，此功能用于将此状态输出到外部。该信号将持续 200 毫秒，然后自动关闭。

#### 机器人锁定状态 \(有效=开\)

此功能用于将 `[Condition Setting]` 中的机器人锁定设置状态输出到外部。

#### 现场总线异常，和现场总线空闲

当使用 CC-LINK 和 DeviceNet 等现场总线通信板时，此功能用于将通信状态输出到外部。

#### 电池 \(备份，编码器\) 电压下降

当备份电池的电压下降以维持安装在主板上的 SRAM 状态或编码器电池的电压下降以维持安装在每个电机上的编码器值时，此功能用于将此状态输出到外部。

#### 扭矩监测

此功能用于将施加在机器人六个轴上的扭矩值输出到外部。将输出到外部的扭矩值是1/2倍率的%值。

#### 润滑剂注入警报

此功能用于将需要注入润滑剂的状态输出到外部。

#### 平均负载因子异常警报

此功能用于将机器人在操作过程中是否超过平均负载因子的状态输出到外部。
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/8-key-signal-output.md)
# 7.3.2.8 键信号输出

`键信号输出 (Key Signal Output)` 是一个功能，允许您将所需变量分配给 F-key，并通过按键操作将该变量的值设置为 1 或 0。
它主要用于通过操作已分配输出变量的 F-key 来开启或关闭 I/O 输出信号。
（可以指定所有类型的变量，包括一般变量、别名和输出变量。）

您可以通过在 HOME 屏幕右侧按下 `[R4: User Key]` 打开 `键信号输出 (Key Signal Output)` 按钮。
如果未进行任何设置，所有按钮将为空。

您可以按如下方式配置按钮：

1. 触摸菜单 `[F2: 系统] - 2: 控制参数 - 2: 输入/输出信号设置 - 5: 关键信号输出 ([F2: system] - 2: Control parameter - 2: Input/Output signal setting - 5: Key signal output)`。

2. 设置要在按钮上显示的功能名称和选项，然后触摸 `[F7: 确认] ([F7: OK])` 按钮。

![](../../../_assets/tp630/ctrl-key-outsignal_eng.png)

* `标题 (title)`：显示在按钮上的名称
* `on-var`：当指定变量名称时，按钮打开时该变量的值被分配为 1。
* `off-var`：当指定变量名称时，按钮关闭时该变量的值被分配为 1。
* `切换 (toggle)`：
  + 已选中：每次按下按钮时，它在开启和关闭之间切换。
  + 未选中：按钮按下时开启，释放时关闭。
* `允许 在 自动 模式 (Permit on auto mode)`：
  + 已选中：此功能即使在自动模式下也会操作。
  + 未选中：此功能在自动模式下不操作。
* `关闭 开启 自动 模式 (OFF on auto mode)`：切换到自动模式时，为此功能设置的所有变量将被关闭。

{% hint style="info" %}
对于 `on-var` 和 `off-var`，例如，如果您输入 3.5 并按下 `[ENTER]`，则 fb3.do5 被输入。
如果您输入 5 并按下 `[ENTER]`，则 do5 被输入。
另外，您可以使用屏幕底部的 F-keys [fb]、[do] 和 [so] 来输入值。
{% endhint %}

3. 打开 `键信号输出 (Key Signal Output)` 按钮，并按住 `[SHIFT]` 键触摸注册的 F-key，以验证设置是否已正确应用。

![](../../../_assets/tp630/rbt-userkey-keysig_eng.png)

{% hint style="info" %}
您可以在 ${cont_model} 教导挂件的用户键区域用按钮注册所需的输出信号。有关注，请参考 " [2.7.2.1 键信号输出功能区域](../../../2-operation/7-user-key/2-button-registration/1-key-signal-output.md)"。
{% endhint %}
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/9-dio-block-assign.md)
# 7.3.2.9 FB 块分配

您可以设置控制器的一般输入/输出信号的使用方法。

1. 触摸 `2: 控制参数 - 2: 输入/输出信号设置 - 6: FB 块分配 (2: 控制参数 - 2: 输入/输出信号设置 - 6: FB 块分配)` 菜单。

2. 设置与所选 FB 地址的 DIO 块的连接，然后触摸 `[OK]` 按钮。

    ![](../../../_assets/tp630/ctrl-dio-blockassign_eng.png)

{% hint style="info" %}
可用的连接选项如下：
* [PCI Slot 1]
* [PCI Slot 2]
* [PCI Slot 3]
* [EtherNet/IP Adapter]
* [EtherCAT I/O]
* [EtherNet/IP Scanner]
* [User DIO]
{% endhint %}
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/10-multi-signal-output.md)
# 7.3.2.10 多信号输出

输出信号（最多 16 个信号）可以作为一个组创建，数据可以通过各个信号输出。

数据以二进制格式表示，决定输出是打开还是关闭。例如，以下屏幕上显示 do41 和 do43 的数据是二进制的 0101（十进制的 5）。

1.	触摸 `2: 控制参数 - 2: 输入/输出信号设置 - 7: 多信号输出 (2: 控制参数 - 2: 输入/输出信号设置 - 7: 多信号输出)` 菜单

2.	设置输出信号组的名称、信号和脉冲。

    ![](../../../_assets/tp630/ctrl-multi-outsignal_eng.png)





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
        <p>所选输出信号组列表的详细信息。您可以设置该组的名称、描述、信号和脉冲。</p>
        <ul>
          <li><b>[全部重置]/[单个重置]:</b> 您可以将所有信号的设置值或选定信号的设置值重置为 -1。</li>
          <li><b>[重置通道]:</b> 您可以重置设置信号的输出通道（0&#x2013;9: 数字信号）</li>
          <li><b>[设置范围]</b>: 您可以通过指定起始和结束信号快速设置信号。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[确定]:</b> 您可以保存编辑的内容。</li>
          <li><b>[+]/[-]:</b> 您可以添加新的输出信号组或删除输出信号组。</li>
          <li>此处显示输出信号组的列表。选择组名称可查看和编辑详细信息。</li>
          <li><b>[复制页面/粘贴页面]:</b> 您可以复制输出信号组信息并粘贴到另一个组。</li>
          <li>从列表中选择要复制的组名称，触摸 <b>[复制页面]</b> 按钮，选择要应用值的组名称，然后触摸 <b>[粘贴页面]</b> 按钮。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

例如，当按照上面屏幕中的设置执行作业程序时，操作将如下。

![图51 作业程序执行示例](../../../_assets/image_429.png)

当机器人从 S1 向 S2 移动，且 S2 的准确性为 OK 时，脉冲信号将与指定组的信号一起输出。脉冲信号将在 200 ms 后关闭。（脉冲信号为 200 ms 的脉冲信号。）
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/11-multi-signal-input.md)
# 7.3.2.11 多信号输入

输入信号（最多16个信号）可以作为一个组创建，可以通过单个信号获取数据。

数据采用二进制格式，通过输入的开或关来确定。例如，如果di41和di43为开，所有其他信号为关，则数据将为0101（十进制中的5）。

1. 触摸 `2: 控制参数 - 2: 输入/输出信号设置 - 8: 多信号输入 (2: 控制参数 - 2: 输入/输出信号设置 - 8: 多信号输入)` 菜单。

2. 设置输入信号组的名称、信号和波特率。

    ![](../../../_assets/tp630/ctrl-multi-insignal_eng.png)

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
        <p>有关从输入信号组列表中选择的组的详细信息。您可以设置组的名称、描述和信号。</p>
        <ul>
          <li><b>[重置所有]</b>/<b>[重置一个]</b>: 您可以将所有信号或选定信号的设置值重置为-1。</li>
          <li><b>[重置通道]</b>: 您可以重置设置信号的输入通道（0–9：数字信号）</li>
          <li><b>[设置范围]</b>: 您可以通过指定开始和结束信号快速设置信号。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[确定]: 您可以保存编辑的内容。</li>
          <li>[+]/[-]:您可以添加一个新的输入信号组或删除一个输入信号组。</li>
          <li>这显示输入信号组的列表。选择一个组名称可以检查和编辑详细信息。</li>
          <li><b>[复制页面]</b>/<b>[粘贴页面]: </b>您可以复制输入信号组信息并将其粘贴到另一个组中。
            <br />从列表中选择要复制的组名称，触摸<b>[复制页面]</b>按钮，选择要应用值的组名称，然后触摸<b>[粘贴页面]</b>按钮。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

例如，当按照上面屏幕中的设置配置的作业程序执行时，操作将如下所示。

![图55 作业程序执行示例](../../../_assets/image_407.png)

从S1开始到S2，机器人执行等待语句。如果在S2的准确性尚可之前满足等待条件，机器人将移动到红色路径。如果不是这样，机器人将等待直到满足等待条件。
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/12-fn-block.md)
# 7.3.2.12 fn 块分配

您可以通过指定 fb 对象的特定区域定义 fn 对象。
如果 ${cont_model} 控制器是现场总线主设备，并且有多个现场总线从设备，您可以将每个从设备的区域设置为每个 fn 对象，以直观地处理这些从设备。

设置的 fn 对象可以在机器人语言和嵌入式 PLC 中像 fb 对象一样使用。

![](../../../_assets/io/io_fn.png)


1. 选择菜单 `[2: 控制参数 - 2: 输入/输出信号设置 - 9: Fn 块分配]`。

2. 如果还没有进行 fn 设置，屏幕是空的。单击右侧的 + 按钮以添加新的 fn 对象。fn 索引编号会从 0 自动增加到 63。

3. 要更改 fn 索引编号，输入新名称并单击 `[F7: 确认] ([F7: OK])` 或 `SHIFT+[F7:应用]` 按钮。
  ![](../../../_assets/io/io_fn_rename.png)

4. 对于每个 fn 对象，单独设置输入信号和输出信号的区域。

5. 在 ` (fb#)` 列中，设置放置 fn 区域的 fb 对象的索引编号 (0-9)。

6. 在 `字节基 (byte base)` 列中，指定在 fb 对象内启动 fn 区域的字节索引。

7. 在 `字节数 (N.bytes)` 列中，指定 fn 区域的大小（以字节为单位）。


&nbsp;  

例如，如果设置如下图所示；

![](../../../_assets/io/io_fn_fn0.png)

![](../../../_assets/io/io_fn_fn3.png)

&nbsp;  

则映射如表格所示。

<table>
  <thead>
    <tr>
      <th></th>
      <th>fn0</th>
      <th>fb</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>输入</td>
      <td>
        fn0.dib[0~2]<br>
        fn0.xb[0~2]
      </td>
      <td>
        fb1.dib[2~4]<br>
        fb1.xb[2~4]
      </td>
    </tr>
    <tr>
      <td>输出</td>
      <td>
        fn0.dob[0~3]<br>
        fn0.yb[0~3]
      </td>
      <td>
        fb2.dob[3~6]<br>
        fb2.yb[3~6]
      </td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th></th>
      <th>fn3</th>
      <th>fb</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>输入</td>
      <td>
        -
      </td>
      <td>
        -
      </td>
    </tr>
    <tr>
      <td>输出</td>
      <td>
        fn3.dob[0~4]<br>
        fn3.yb[0~4]
      </td>
      <td>
        fb3.dob[4~8]<br>
        fb3.yb[4~8]
      </td>
    </tr>
  </tbody>
</table>

您可以打开 fn 输入/输出监控面板，以查看或手动输出每个 fn 对象的 dio 或 xy 中继的当前值。有关更多信息，请参见以下链接。

[6.8 fn 输入，fn 输出](../../../6-monitoring/2-io/5-fn-io.md)
[__SOURCE](7-system/3-control-parameter/3-serial-port.md)
# 7.3.3 串口

您可以设置串口通信所需的信息。

1. 触摸`[2: 控制参数 - 3: 串口] ([2: 控制参数  - 3: 串口])`菜单。

2. 设置每个串口的参数。

    ![](../../_assets/tp630/ctrl-serial.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">从串口列表中选择的端口的详细信息。您可以设置端口名称和参数值。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><strong>串口列表</strong>：选择一个端口名称以查看和编辑其详细信息。</li><li><strong>[确定]</strong>：保存更改。</li>
          <li><strong>[+]/[-]</strong>：添加新的串口或删除现有的串口。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          执行环回测试。将串口的RX和TX引脚连接以检查通信是否正常。
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
设置串口使用时请参考以下信息。

* 传感器：通过访问视觉传感器接收位移数据
* LVS：用于连接激光视觉传感器以跟踪焊接线
* MODBUS：${cont_model}控制器的MODBUS从属功能
{% endhint %}
[__SOURCE](7-system/3-control-parameter/4-robot-ready-cond.md)
# 7.3.4 机器人准备条件

当机器人准备完成时，在 `[Robot Ready OK]` 项中设置信号输出的条件，位于 `系统 - 2: 控制参数 - 2: 输入/输出信号设置 - 4: 输出信号分配 (系统 - 2: 控制参数 - 2: 输入/输出信号设置 - 4: 输出信号分配)` 菜单中。

1. 点击 `[2: 控制参数 - 4: 机器人准备条件] ([2: 控制参数 - 4: 机器人准备条件])` 菜单。

2. 设置完机器人准备条件后，点击 `[OK]` 按钮。

    ![](../../_assets/tp630/ctrl-robot-readycond_eng.png)
[__SOURCE](7-system/3-control-parameter/5-home-position.md)
# 7.3.5 家庭位置注册

通过将机器人的任意姿态注册为家位置，您可以在机器人进入此位置时将家位置信号输出到输出信号域。家位置可以根据每个轴的姿态指定，最多可以注册和使用十六个姿态，并且每个轴的余量可以另外设置。

1.	触摸 `[2: 控制参数 - 5: 家庭位置注册] ([2: 控制参数 - 5: 家庭位置注册])` 菜单。

2.	选择家位置标签，然后设置使用、输出信号、轴角和范围。

    ![](../../_assets/tp630/ctrl-home-position_eng.png)



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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>在选项卡中选择的家位置的详细信息。您可以设置使用、输出信号、轴角和范围及描述。</p>
        <ul>
          <li>[使用]: 您可以设置是否使用。</li>
          <li>[输出信号]: 您可以输入输出信号编号。</li>
          <li>[轴角]/[范围]: 您可以输入机器人的轴角和家位置的范围。</li>
          <li>如果范围设置为0，则不会对该轴进行家位置检查。</li>
          <li>范围指的是覆盖家点的 + 方向和 - 方向的范围。例如，如果范围设置为0.5，则家位置信号的输出范围将为1。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>`[确定]`: 您可以保存更改。</li>
          <li><b>[当前机器人姿态]</b>: 当前机器人姿态的轴角和范围将被自动输入。</li>
          <li><b>[程序/步骤]</b>: 如果您输入程序和步骤编号，则相关步骤的轴角和范围将被自动输入。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](7-system/3-control-parameter/6-cordsys-reg/README.md)
# 7.3.6 坐标系统注册

1. 触摸 `[2: Control Parameter - 6: Coordinate Registration] ([2: Control Parameter  - 6: Coordinate Registration])` 菜单。然后，坐标系统注册菜单将出现。

2. 通过选择所需的菜单，可以相对于用户坐标系统或静止工具坐标系统设置坐标系统。

    ![](../../../_assets/tp630/ctrl-coord-menu_eng.png)
[__SOURCE](7-system/3-control-parameter/6-cordsys-reg/1-user-crdsys.md)
# 7.3.6.1 用户坐标系统

用户坐标系统是一个坐标系统，可在用户指定的位置进行设置。要使用用户坐标系统，首先需要教导定义用户坐标系统所需的三个参考步骤，然后通过指定教导的程序编号和步骤顺序来注册用户坐标系统。

按照以下步骤教导三个参考步骤。以下程序解释了步骤顺序指定为“OXY”时的情况（O：原点姿态，X：轴姿态，Y：平面姿态）。

![图56 定义用户坐标系统的三个参考步骤教学方法](../../../_assets/image_427.png)

1. 定义用户坐标系统的原点：教导一个任意点。

2. 定义用户坐标系统中的 X 轴：教导 X 轴线上的一个任意点，使得此点尽可能远离原点 200 mm。

3. 定义用户坐标系统中的 XY 平面 \(确定 Y 轴和 Z 轴方向\)：教导在 X 轴和 Y 轴组成的平面上一个任意点，此点离原点的距离尽可能 200 mm 或以上。

{% hint style="info" %}
* 在进行用户坐标系统设置程序的教学时，TCP 应设置为正确值。检查当前选择工具的工具数据是否正确输入。
* 您可以注册最多 20 个用户坐标系统。
{% endhint %}

{% hint style="warning" %}
记录用于定义坐标系统的参考点时的注意事项如下。

* 参考 3 点不应位于同一条直线上。
* 参考 3 点之间的距离不应太近。
* S3 之后的后续步骤将不会对坐标系统注册产生影响。
{% endhint %}

通过指定教导的程序编号和步骤顺序注册用户坐标系统的方法如下。

1. 点击 `[2: 控制参数 - 6: 坐标系统注册 - 1: 用户坐标系统] ([2: 控制参数 - 6: 坐标系统注册 - 1: 用户坐标系统])` 菜单。

2. 转到您想注册的用户坐标系统（可以使用“+”按钮创建）。
3. 在指定程序编号和步骤顺序后，按下 [F1: JOB 计算] 按钮。
4. 计算得到的用户坐标系统原点的位置将会显示。

    ![](../../../_assets/tp630/ctrl-user-coord_eng.png)

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
      <td style="text-align:left">从用户坐标系统列表中选择的坐标系统的详细信息。您可以设置坐标系统名称和描述、教导的程序编号、步骤顺序和基于基轴原点的原点姿态。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>`[OK]`：您可以保存更改。</li>
          <li><b>[+]/[-]</b>：您可以添加新的用户坐标系统或删除用户坐标系统。</li>
          <li>用户坐标系统列表。选择坐标系统名称可以查看和编辑详细信息。</li>
          <li><b>[复制页面]/[粘贴页面]</b>：您可以复制用户坐标系统信息并粘贴到另一个坐标系统中。
            <br />从列表中选择要复制的坐标系统信息名称，然后点击<b>[复制页面]</b>按钮，选择要将值应用到的坐标系统名称，再点击<b>[粘贴页面]</b>按钮。</li>
          <li><b>[从作业计算]</b>：您可以基于教导的程序和步骤顺序计算用户坐标系统以定义用户坐标系统。
            <br />如果在<b>[作业编号]</b>选项和步骤顺序中输入教导的程序编号后点击<b>[从作业计算]</b>按钮，将计算出用户坐标系统的原点。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](7-system/3-control-parameter/6-cordsys-reg/2-stationary-tool-crdsys.md)
# 7.3.6.2 静态工具坐标系统

机器人工具是附加在机器人前端的工具。一般来说，机器人使用附加在机器人的工具进行操作。一个典型的例子是弧焊。弧焊工具通常附加在机器人的前端，并用于对外部固定的工件进行焊接。

另一方面，在静态工具的情况下，工具是附加在外部，而不是机器人。在这种情况下，机器人处理工件并将其放置在外部固定的工具上进行操作。使用静态工具的典型操作是密封操作。通常，在密封操作中，当外部工具排放出一定量用于密封的溶剂时，机器人持有工件并创建所需的轨迹进行操作。

![图57 密封操作示例](../../../_assets/tp630/stationary_crd_sealing_eng.png)

为了创建所需的轨迹，机器人基于外部附加工具而不是基于自身附加的工具执行线性 \(L\) 和圆形 \(C\) 插值。这时，将使用静态工具插值功能。

当使用静态工具插值功能时，即使机器人持有的工件的姿态发生变化，静态工具在工件上的移动路径仍然可以保持线性和弧形。因此，对于外部工具移动路径重要的操作，必须始终使用静态工具插值功能。

要使用静态工具插值功能，必须设置静态工具坐标系统。

设置静态工具坐标系统的方法如下。

1.	触摸 `[2: 控制参数 - 6: 坐标注册 2: 静态工具坐标系统] ([2: 控制参数  - 6: 坐标注册 2: 静态工具坐标系统])` 菜单。

2.	选择所需的选项卡并注册静态工具坐标系统的位置。 

    ![](../../../_assets/tp630/ctrl-stationary-coord_eng.png)



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
      <td style="text-align:left">您可以通过选择选项卡设置最多二十个静态工具坐标系统（工具 0
        - 工具 19）。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[<b>确定</b>]: 您可以保存更改。</li>
          <li>[<b>当前机器人姿态</b>]: 您可以将当前 TCP 位置设为静态工具坐标系统的位置。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>



### 将当前 TCP 位置设为静态工具坐标系统的位置

在根据机器人基座坐标系统准确找到 TCP 后，您应该将静态工具和机器人工具匹配，如下图所示，然后使用 `[当前机器人姿态]` 按钮执行自动设置功能。然后，当前 TCP 位置将被注册。

![](../../../_assets/tp630/stationary_crd_autoset_eng.png)



### 使用静态工具坐标系统编写程序

要执行静态工具插值步骤的记录，您应该将步骤记录为 SL 或 SC。使用 ${cont_model} 教学挂件屏幕左上角的 `[记录条件]` 按钮，您可以将记录条件更改为 SL \(静态工具线性插值\) 或 SC \(静态工具圆形插值\)。

例如，如果您注册并使用静态工具坐标系统编号 1，您可以创建如下程序。

![](../../../_assets/tp630/pane-prog-cmd-SL_eng.png)

{% hint style="info" %}
在使用静态伺服枪的情况下，不需要静态工具插值功能。这是因为在伺服枪焊接中，静态伺服枪的工件移动路径不需要形成直线或弧形，而仅焊接点是重要的。
{% endhint %}
[__SOURCE](7-system/3-control-parameter/7-prog-reservation.md)
# 7.3.7 定时程序执行

有关如何执行定时程序的详细信息，请参阅 "[${cont_model} 控制器定时程序执行功能手册](https://hrbook-hrc.web.app/#/view/doc-reserved-program-execution/zh/README?cont_model=${cont_model})"。
[__SOURCE](7-system/3-control-parameter/8-auto-backup-restore.md)
# 7.3.8 自动备份和恢复

有关如何自动备份和恢复控制器数据的详细信息，请参考 "[${cont_model} 控制器自动备份功能手册](https://hrbook-hrc.web.app/#/view/doc-hi6-auto-backup/zh/README?cont_model=${cont_model})"。
[__SOURCE](7-system/3-control-parameter/9-network-setting/README.md)
# 7.3.9 网络

1.  `[2: Control parameter - 9: Network] ([2: Control parameter  - 9: Network])` 点击菜单。网络设置菜单将会出现。

2.  选择所需的菜单以设置环境设置、服务等。
[__SOURCE](7-system/3-control-parameter/9-network-setting/1-environment-setting.md)
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
[__SOURCE](7-system/3-control-parameter/9-network-setting/2-service/README.md)
# 7.3.9.2 服务
[__SOURCE](7-system/3-control-parameter/9-network-setting/2-service/1-modbus-slave.md)
# 7.3.9.2.1 Modbus 从站

本节涵盖使用控制器的 Modbus TCP 从站通信时的设置和监控。 <br>
有关更多信息，请参考 "[${cont_model} 机器人控制器功能手册 - Modbus](https://hrbook-hrc.web.app/#/view/doc-modbus/zh/README?cont_model=${cont_model})"。
[__SOURCE](7-system/3-control-parameter/9-network-setting/2-service/3-ntp-client.md)
# 7.3.9.2.3 NTP 客户端

控制器的时间可以与 NTP 服务器自动同步。 <br>

有关更多信息，请参阅 "[${cont_model} 控制器功能手册 - NTP 时间同步](https://hrbook-hrc.web.app/#/view/doc-hi6-ntp-time-synchronization/zh/README)"。
[__SOURCE](7-system/3-control-parameter/10-license-key/README.md)
# 7.3.10 注册选项功能的许可证密钥
[__SOURCE](7-system/3-control-parameter/10-license-key/1-summary.md)
# 7.3.10.1 可选功能的许可证密钥是什么？

在 ${cont_model} 机器人控制器的功能中，某些可选功能是单独出售的，客户必须购买可选功能才能使用它们。可选功能的许可证密钥是通过将分配给机器人控制器主板的唯一编号与购买的可选功能结合而通过单独的许可证密钥生成程序生成的，因此所购买的功能仅在购买的控制器上运行。
因此，使用可选功能的机器人控制器的主板不能更换为其他控制器。
如果主板发生故障，我们将提供一个临时密钥，可在需要用备件更换时使用30天。
在这种情况下，您必须至少提前30天联系我们的 A/S 以获得官方许可证密钥。
 
* 功能配置 <br>
  设置是否购买可选功能 <br>
  许可证密钥设置
[__SOURCE](7-system/3-control-parameter/10-license-key/2-registration-process.md)
# 7.3.10.2 许可证密钥注册程序

* 购买与您的系统序列号匹配的可选功能许可证密钥。系统序列号位于许可证注册屏幕上。

  ![](../../../_assets/tp630/license-key1.png)


* 首先选择是否购买可选功能，然后输入许可证密钥。如果购买选择和许可证密钥不匹配，则在执行该功能时会发生错误。
[__SOURCE](7-system/3-control-parameter/10-license-key/3-registration.md)
# 7.3.10.3 注册许可证密钥

* 注册屏幕

  ![](../../../_assets/tp630/license-key2.png)


* 如果许可证密钥输入正确，"==> OK" 将显示在许可证密钥输入框的右侧。

* 如果显示 "==> NG"，则许可证密钥不正确或购买选项选择错误。
[__SOURCE](7-system/3-control-parameter/10-license-key/4-temporary-key.md)
# 7.3.10.4 什么是临时密钥？

* 临时密钥只能使用30天，并且只能签发一次。

* 如果临时密钥的剩余日期少于10天，每次控制器启动时会出现以下警告。 <br>
  "W0025 可选功能临时许可证密钥的免费试用期仅剩（0）天。"

* 临时密钥的目的，是在控制器的主板出现问题并更换备用件时，直到我们的A/S重新签发许可证密钥为止。
[__SOURCE](7-system/3-control-parameter/10-license-key/5-temporary-key-registration.md)
# 7.3.10.5 临时密钥注册

* 可以通过按[F]键发放临时密钥。

  ![](../../../_assets/tp630/license-key3.png)


* 如果成功发放，剩余的使用天数将在以下屏幕中显示。

  ![](../../../_assets/tp630/license-key4.png)


* 注意）如果剩余天数为0，则不再可以使用可选功能，此后将发放1天使用的临时密钥。由于可选功能可能导致生产线停滞，请在剩余天数达到0之前务必与我们联系以获取正式许可证密钥。
[__SOURCE](7-system/3-control-parameter/11-industrial-comm/README.md)
# 7.3.11 工业通信 \(fieldbus\)

"[${cont_model} 机器人控制器功能手册. - 工业通信](https://hrbook-hrc.web.app/#/view/doc-industrial-communication/zh-${cont_model}/README?cont_model=${cont_model})"

[__SOURCE](7-system/4-robot-parameter/README.md)
# 7.4 机器人参数

您可以设置与机器人操作相关的各种数据，以及每个轴的原点和操作范围等信息。

1. 触摸 `[3: Robot Parameter]` 菜单。然后，机器人参数菜单将出现。

2. 您可以通过选择所需菜单来检查和设置操作器的各种参数。

    ![](../../_assets/tp630/robot-menu_eng.png)
[__SOURCE](7-system/4-robot-parameter/1-tool-data/README.md)
# 7.4.1    工具数据

您可以根据机器人的 R1 轴法兰设置 TCP 的距离和角度，并注册工具的重量、重心和惯性。您可以使用 `[1: Tool data]` 菜单手动进行注册。

另一种方式是使用自动校准功能设置工具长度，并使用负载估计功能注册工具的重量、重心和惯性。

在进行线性或圆形插值等插值操作时，轨迹将基于 TCP 创建，因此在教学之前应准确设置工具的长度和角度。

${cont_model} 控制器根据机器人的动力学进行控制。只有当工具的重量、中心和惯性正确设置时，机器人才能快速安全地运行。如果工具的重量、中心和惯性值不正确或错误，可能会在机器人性能和服务寿命中出现严重问题。

特别是，在使用工具更换功能的情况下，所有与工具更换相关的工具信息，不仅仅是每种工具的信息，还应输入分配给断开工具的单独编号。此外，即使在处理操作期间，工件的附加/拆卸状态也应分配给每个工具编号以供使用。

工具的长度是法兰坐标系中每个方向的长度。 \(X 轴方向的长度: Xt / Y 轴方向的长度: Yt / Z 轴方向的长度: Zt\)

![图 60 各类机器人法兰坐标系](../../../_assets/image_213.png)

工具的角度是法兰坐标系中每个方向的姿态转换量。 \(X 轴方向的角度: Rx / Y 轴方向的角度: Ry / Z 轴方向的角度: Rz\)

![图 61 工具角度: 旋转 Rx \(左\) / 旋转 Ry \(中\) / 旋转 Rz \(右\)](../../../_assets/image_211.png)

工具的长度和角度将根据法兰坐标系设置。工具长度可以设置为法兰坐标系中心到 TCP 的距离。

工具姿态是根据上述设置的工具角度在法兰坐标系中按顺序在 X、Y 和 Z 方向进行旋转获得的值。

Rxyz = Rot\(z, Rz\)Rot\(y, Ry\)Rot\(x, Rx\)

* Rxyz: 基于工具法兰的工具姿态旋转矩阵
* Rot\(z, Rz\): 在法兰坐标系的 Z 轴方向上旋转 Rz 的旋转矩阵
* Rot\(y, Ry\): 在法兰坐标系的 Y 轴方向上旋转 Ry 的旋转矩阵
* Rot\(x, Rx\): 在法兰坐标系的 X 轴方向上旋转 Rx 的旋转矩阵
[__SOURCE](7-system/4-robot-parameter/1-tool-data/1-tool-data-set.md)
# 7.4.1.1 工具数据设置

根据机器人 R1 轴法兰手动设置 TCP 的距离和角度，并注册工具的重量、重心和惯性的方法如下。

1. 触摸 `[3: Robot Parameter - 1: Tool Data] ([3: Robot Parameter  - 1: Tool Data])` 菜单。

2. 设置工具数据名称、重量、每个轴的详细条件和允许比率。

    ![](../../../_assets/tp630/robot-tool_eng.png)

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
      <td style="text-align:left"><ul>从工具数据列表中选择的工具数据的详细信息。
        您可以设置工具数据名称和描述、重量、每个轴的详细条件和允许比率。</ul></td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[自动校准]</b>: 您可以创建新的工具数据，也可以通过使用现有程序简单地创建工具数据。如果您想在之前教授的步骤位置重新进行设置，您应首先放置工具，然后执行自动校准功能以重新创建工具长度和角度。
            <br />
            <img src="../../../_assets/tp630/robot-tool-autocal_eng.png" alt/>
            <br />
          </li>
          <ul>
            <li>[前一程序编号]: 您可以输入在工具变形发生之前教授的程序编号。</li>
            <li>[前一步编号]: 您可以输入将要执行自动工具数据校准的步骤编号。</li>
            <li>[要设置的工具编号]: 您可以输入要新设置的工具编号。</li>
          </ul>
          <li>
            <p>[角度校准]: 您可以校准工具的角度。</p>
            <p>
              <img src="../../../_assets/tp630/robot-tool-anglecal_eng.png" alt/>
            </p>
          </li>
          <li>[应用 CAD 数据]: 如果您有工具的 CAD 数据并用它编辑工具数据，则这被视为负载估算的完成。
            <br />
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
          <li>[确定]: 您可以保存更改。</li>
          <li>[+]/[-]: 您可以添加新的工具数据或删除工具数据。</li>
          <li>工具数据列表。选择工具数据名称将允许您检查和编辑详细信息。</li>
          <li>[复制页面]/[粘贴页面]: 您可以复制工具数据信息，然后粘贴到另一个工具数据。
            <br />在从列表中选择要复制的工具数据信息的名称并触摸<b>[复制页面]</b>按钮后，选择要应用数值的工具数据名称，然后触摸<b>[粘贴页面]</b>按钮。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 在工具数据列表中，未执行负载估算的工具数据将在名称的右侧标记为 \(X\)。
* 您必须在使用工具之前先执行负载估算。使用未执行负载估算的工具可能会导致机器人速度和耐用性的问题。
* 
  当工具数据被复制时，负载估算数据也将被复制。工具数据的复制和粘贴功能仅在已执行负载估算的工具编号的选项卡上执行。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/1-tool-data/2-tool-data-set-info.md)
# 7.4.1.2 工具数据设置信息

* `[Weight]`: 工具的重量 \(kg\)
* `[Length]`: 工具的长度 \(mm\)。您可以使用自动校准功能或自动校准进行设置。
* `[Angle]`: 工具的角度 \(deg\)。您可以使用自动校准功能或角度校准功能进行设置。
* `[Center]`: 工具重心相对于法兰中心的位置 \(mm\)。您可以使用负载估算功能进行设置。
* `[Inertia]`: 工具相对于工具坐标的转动惯量 \(kg/m2\)。您可以使用负载估算功能进行设置。
* 允许比率: \(仅适用于启动高负载模式的机器人型号\) 这是当前设置与允许参考值的比率。根据允许比率，机器人操作如下。

| Classification | Normal | High-load mode | Exception allowable mode | Playback impossible \(Large size\) |
| :--- | :--- | :--- | :--- | :--- |
| 重量比 \(%\) | - 100 | 100-120 | 100-120 | 120 - |
| 转矩比 \(%\) | - 100 | 100-110 | 100-115 \(150\) | 115 \(150\) - |
| 转动惯量比 \(%\) | - 100 | 100-130 | 100-150 \(600\) | 150 \(600\) - |

{% hint style="info" %}
允许比率可以根据机器人型号和控制器软件版本进行更改。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/2-axis-origin.md)
# 7.4.2 轴原点

您可以注册每个轴的机械原点位置。

1. 触摸 `[3: Robot Parameter - 2: Axis Origin] ([3: Robot Parameter  - 2: Axis Origin])` 菜单。

2. 注册每个轴的机械原点位置。

    ![](../../_assets/tp630/robot-origin_eng.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>每个轴的机械原点位置的详细信息。您可以设置轴的编码器和位置。</p>
        <ul>
          <li>S轴：您可以根据机器人和周围夹具的安装情况更改S轴原点。</li>
          <li>R1轴：您可以根据工具附件方向更改R1轴的原点。</li>
          <li>H、V、R2和B轴：可以通过自动校准功能自动设置。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[确认]：您可以保存更改。</li>
          <li>[应用一个]：您可以将选定的原点位置应用于选定的轴信息。</li>
          <li>[应用全部]：您可以将选定的原点位置应用于所有轴信息。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
* 轴原点设置会影响机器人的笛卡尔操作精度。尽可能将其更改为准确的值。
* 
  如果更改轴原点设置，则之前创建的程序位置将会改变。因此，轴原点设置必须仅在初始安装阶段执行。

* 
  如果更改编码器偏移设置，则应重新设置轴原点。因此，编码器偏移设置必须在轴原点设置之前完成。
{% endhint %}

{% hint style="info" %}
发货时，每个轴的机械原点位置设置为标准值 \(0X400000\)。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/3-soft-limit.md)
# 7.4.3 软件限制

您可以根据机器人的使用环境调整每个轴的操作范围。

1. 触摸 `3: Robot Parameter - 3. Soft Limit (3: Robot Parameter  - 3. Soft Limit)` 菜单。

2. 设置每个轴的操作范围。

    ![](../../_assets/tp630/robot-softlimit_eng.png)



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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">每个轴的操作范围的详细信息。您可以设置一个轴的最小和最大操作范围以及当前轴的位置。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[确认]: 您可以保存更改。</li>
          <li>[当前值]: 您可以基于当前机器人位置设置每个轴的操作范围。</li>
          <li>[重置全部]: 您可以初始化所有轴的操作范围。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
在出厂时，机器人每个轴的操作范围设置为最大值。 
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/4-encoder-offset/README.md)
# 7.4.4 编码器偏移

当前编码器位置可以设置为编码器原点位置 \(position 0X400000\)。您可以在机器人的每个轴的参考位置处确定编码器原点 \(每个轴附着刻度的位置\)。

1. 触摸 `[3: Robot Parameter - 4: Encoder Offset] ([3: Robot Parameter  - 4: Encoder Offset])` 菜单。

2. 通过调整每个轴的位置设置编码器偏移值。编码器偏移值将以十六进制数 \(a hexadecimal number\) 形式记录。

    ![](../../../_assets/tp630/robot-encoder-offset_eng.png)



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
      <td style="text-align:left">每个轴的编码器偏移值的详细信息。您可以设置已校准的编码器值、当前编码器值和轴的当前位置。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: 您可以保存更改。</li>
          <li>[Reset One]/[Reset All]: 您可以初始化所选或所有轴的编码器偏移值。</li>
          <li>[Calculate Correction Value]: 您可以校准所选轴的编码器偏移值。</li>
          <li>[Previous Correction Value]: 您可以检索在选定轴的校准之前存在的编码器偏移值。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
编码器偏移值在出厂时设置。只有在必要时，例如更换马达或编码器时，才应重置编码器偏移值。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/4-encoder-offset/1-encoder-offset-utilization.md)
# 7.4.4.1 编码器偏移值的使用

要继续使用现有程序，即使当前工作程序已备份并且系统已初始化 `系统 - 5: 初始化 - 1: 系统初始化 (system - 5: Initialize - 1: System Initialization)`，机器人应该保持初始化之前存在的参考位置信息。如果记录编码器偏移值，机器人之前的位置信息可以被检索。

在系统初始化后，直接将编码器偏移值作为十六进制值输入。如果使用软键盘，将更容易输入该值。

如果编码器偏移值记录为轴位置值 \(mm 或度\)，你需要在按住 `[SHIFT]` 键的同时触摸 `[Reset One]` 按钮时，输入弹出窗口中出现的轴位置值。

![](../../../_assets/tp630/robot-encoder-backup_eng.png)



{% hint style="info" %}
轴位置输入窗口中的基本设置值是参考位置值。如果不输入轴位置值直接保存，当前编码器位置将设置为原点位置 \(0X400000\)。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/4-encoder-offset/2-axis-posi-restore.md)
# 7.4.4.2 轴原点位置恢复

当机器人机构（特别是电机或减速器）发生组件故障并进行替换时，必须在与原始原点位置相同的条件下对编码器进行校准，以便重新启动现有的教学程序。  
然而，当服务人员在现场手动执行此程序时，原点位置可能会经过多次试验和错误进行设置。提供此专用功能以简化该过程。

* 机械维修后的原点位置恢复是什么？

![](../../../_assets/tp630/axis-posi-restore1.png)

换句话说，原点位置恢复是指：  
在替换组件后，使用外部参考点（量具），通过补偿不准确校准的原点位置 Ωo' 的值 ⓒ − ⓐ，将其恢复到准确的原点位置 Ωo。  
（这在重新使用教学程序时是必需的。）

{% hint style="warning" %}
外部参考点的位置 (ⓑ) 在组件更换前后必须保持不变。换句话说，它在更换前后必须完全处于相同的位置。
{% endhint %}


### 示例

以下示例解释了假设更换 S 轴电机的功能。

1. 指定一个新程序 (101.job)，并教 S1 [验证点 - 接近] 和 S2 [原点位置验证点，仅 S 轴相对于 S1 旋转]，使得固定在牢固安装工具上的点接近夹具或外围设备。  

   ![](../../../_assets/tp630/axis-posi-restore2.png)

2. 更换 S 轴电机后，手动移动 S 轴至接近更换前的编码器校准位置，然后在 `系统 - Robot Parameter - Encoder Calibration (System - Robot Parameter - Encoder Calibration)` 屏幕上进行 S 轴的编码器校准。

3. 手动运行教学程序 (101.job) 移动到 S1，然后移动到 S2。当位置变得与机械组件更换前相同后，教 S3 [原点位置验证点，仅 S 轴相对于 S1 旋转]。  

   ![](../../../_assets/tp630/axis-posi-restore3.png)

4. 自动计算 S 轴的编码器校准值。

   1) 进入 `系统 - Robot Parameter - Encoder Calibration (System - Robot Parameter - Encoder Calibration)` 屏幕。  
   2) 将光标移动到 S 轴并按下 `[F3: 计算校准值]`。 

      ![](../../../_assets/tp630/axis-posi-restore4.png)

   3) 将程序号设置为 101，步骤号设置为 2，以表示“更换 S 轴电机之前”，  
      将程序号设置为 101，步骤号设置为 3，以表示“更换 S 轴电机之后”，  
      然后按下 `[执行]` 按钮。  

      (* 如果“更换 S 轴电机之后”的程序或步骤号设置为 0，则编码器校准值将使用机器人当前的 S 轴位置进行计算。)  

      ![](../../../_assets/tp630/axis-posi-restore5.png)

   4) S 轴的计算编码器校准值将在屏幕上显示。按下 `[F7: 确认]` 以应用校准的编码器值。  

      ![](../../../_assets/tp630/axis-posi-restore6.png)

5. 移动到教学程序 (101.job) 的 S2，并验证位置与电机更换前相同。
[__SOURCE](7-system/4-robot-parameter/5-b-axis-deadzone.md)
# 7.4.5 B轴死区

在B轴的0度附近，R1轴的旋转中心和R2轴的旋转中心轴几乎是平行的。当机器人执行线性插补或圆形插补等插补时，手腕轴即使在小范围运动中也会快速移动。

设置B轴不使用区域。

1.	触摸`[3: Robot Parameter - 5: B-axis Deadzone] ([3: Robot Parameter  - 5: B-axis Deadzone])`菜单。

2.	在设置确定不使用区域的角度和插补处理模式后，触摸`[OK]`按钮。

    ![](../../_assets/tp630/robot-baxis-deadz_eng.png)



* `[Setting Value]`: 您可以输入确定B轴不使用区域的角度。
* 
  `[Dead zone interpolation]`: 当机器人轨迹在插补操作中必须经过B轴不使用区域时，您可以进行有关错误处理和机器人停止的设置。
[__SOURCE](7-system/4-robot-parameter/6-accuracy.md)
# 7.4.6 精度

您可以设置精度级别的详细条件，指的是机器人在执行目标步骤时通过该步骤的精度。

1. 触摸 `[3: Robot Parameter - 6: Accuracy] ([3: Robot Parameter  - 6: Accuracy])` 菜单。

2. 为每个精度级别设置工具提示位置 \(TCP\) 和姿态。

    ![](../../_assets/tp630/robot-accuracy_eng.png)



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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>每个级别的详细信息。您可以为每个精度级别设置工具提示位置 (TCP) 和姿态。</p>
        <ul>
          <li>精度级别可以设置为从 0 到 7 的值，精度级别将被记录为步骤语句参数之一。</li>
          <li>精度级别 0&#x2013;6: 输入每个级别的 TCP 距离和姿态，以及附加轴的距离和角度。<br />对于不支持线性或圆形插补的机器人，例如 LCD 机器人，将应用与附加轴相同的方法。</li>
          <li>精度级别 7: 值将自动计算并显示在控制器中，因此您不需要直接输入该值。<br />当应用精度级别 7 时，将创建满足步骤距离 1/2 的条件的最大转弯路径。精度级别 7 在需要使机器人尽可能平滑和快速移动的情况下非常有用，例如 LDC 手进出操作。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[确定]: 您可以保存更改。</li>
          <li>[重置所有]: 您可以初始化所有精度级别的 TCP 距离和姿态。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 如果您根据对 "[2.3 步骤](../../2-operation/3-step/README.md)" 内容的理解来接近精度级别，您可以更轻松地使用它。
* 在使用伺服枪或无均衡器枪的焊接步骤中，控制器将自动根据设置的精度级别执行限制。 


{% endhint %}
[__SOURCE](7-system/4-robot-parameter/7-axis-add-weight/README.md)
# 7.4.7 每个轴的额外重量

您可以注册安装在机器人基本轴上的变压器或接线支架的信息。

1. 触摸 `[3: Robot Parameter - 7: Additional Weight on Each Axis] ([3: Robot Parameter  - 7: Additional Weight on Each Axis])` 菜单。

2. 选择基本轴选项卡，设置安装的额外重量信息，然后触摸 `[OK]` 按钮。 

    ![](../../../_assets/tp630/robot-addweight_eng.png)



{% hint style="warning" %}
如果机器人由于安装了变压器或接线支架而有额外重量，您必须注册每个轴的额外重量信息。如果没能正确注册额外重量，在执行工具负载估算时可能会出现较大错误。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/7-axis-add-weight/1-crdsys-origin-of-each-axis.md)
# 7.4.7.1 每个轴的坐标系原点

每个轴的X、Y和Z方向与机器人坐标系统的方向相同。有关每个轴的坐标系原点，请参阅以下内容。

![图62 每个机器人配置的每个轴的坐标系原点](../../../_assets/image_476.png)
[__SOURCE](7-system/4-robot-parameter/8-collision-detection/README.md)
# 7.4.8 影响检测

当机器人操作过程中发生碰撞时，影响检测（碰撞检测）是一种功能，它将机器人运动过程中正常生成的扭矩与当前生成的扭矩进行比较，并在检测到异常扭矩时将其视为错误，以尽量减少碰撞造成的损害。

${cont_model} 控制器通过在机器人在异常条件下操作或表现出异常行为时，以互补的方式使用碰撞检测功能，与现有的安全功能（例如过流、过载、过速和位置偏差错误检测）增强机器人的安全性。

触摸 `[3: Robot Parameter - 14: Impact Detection] ([3: Robot Parameter  - 14: Impact Detection])` 来使用此功能。

{% hint style="info" %}
* 碰撞检测功能仅在电机开启时操作。
* 在使用碰撞检测功能之前，请务必设置正确的工具/附加重量或执行负载估计。
* 如果每个轴的工具重量或附加重量与实际值不同，可能会发生误检测。
* 在进行负载估计或传感器基础 / 无传感器的力控制功能时，无法检测到碰撞。
* 与未安装在机器人的定位器、点焊机、夹具或其他设备的碰撞无法被检测到。
* 不支持针对定制机器人模型的基于模型的碰撞检测。
* 当在从自主驾驶模式切换到手动驾驶模式后发生碰撞检测错误时，此现象不是错误（需要检查碰撞检测设置值）。

{% endhint %}

![](../../../_assets/tp630/coldet/robot_impact_detection.png)
[__SOURCE](7-system/4-robot-parameter/8-collision-detection/1-coldet-model-based.md)
# 7.4.8.1 基于模型的碰撞检测

基于模型的碰撞检测功能通过计算在机器人运动过程中应正常产生的扭矩与实际测量的扭矩之间的差异来检测碰撞。可以调整灵敏度以控制对碰撞的响应，并且在机器人以低速移动时与外部物体的接触也可以被检测到。

1. 触摸菜单 `[3: Robot parameter - 14: Impact Detection - 1: Model-Based Collision Detection] ([3: Robot parameter  - 14: Impact Detection  - 1: Model-Based Collision Detection])`。

![](../../../_assets/tp630/coldet/model_based_coldet_tab_general.png)

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
      <td style="text-align:left">启用或禁用基于模型的碰撞检测功能。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">表示所有轴的默认灵敏度。较高的值会增加碰撞检测灵敏度。 (默认: 100, 最大: 200)  </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">启用或禁用低速碰撞检测功能。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">检测低速碰撞的设置时间。如果碰撞力施加超过这个参考时间，则被识别为碰撞。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">只有当链节速度低于设置值时，碰撞才被视为低速碰撞。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">将设置重置为默认值。</td>
    </tr>
  </tbody>
</table>

![](../../../_assets/tp630/coldet/model_based_coldet_tab_axis.png)

{% hint style="info" %}
每轴设置标签仅在工程模式或更高模式中启用。
{% endhint %}

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
      <td style="text-align:left">相对于每个轴的碰撞检测阈值的比例（%）。较低的值会导致更灵敏的响应。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">截止频率值，通常根据机器人的控制环境设置。如果任何轴设置为0，则禁用该轴的碰撞检测。（最大值：100） </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">将设置重置为默认值。</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
每个轴的最终灵敏度值与每轴灵敏度值成正比，与所有轴的整体默认灵敏度成反比。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/8-collision-detection/2-coldet-axis.md)
# 7.4.8.2 设置每个轴的碰撞检测

碰撞检测功能监控每个机器人轴上发生的干扰扭矩和干扰扭矩变化率。如果测量值超过配置的阈值，则视为错误。

* 如果干扰扭矩超过设定阈值，则显示`[E0160 (Axis O) 碰撞检测]`。
* 如果干扰扭矩变化率超过设定阈值，则显示`[E0161 (Axis O) 冲击检测]`。


![](../../../_assets/tp630/coldet/collision_detection_of_axis.png)

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
      <td style="text-align:left">启用或禁用每个轴的碰撞检测功能。即使在启用状态下，当机器人停止或点焊枪施加压力时，该功能也不会工作。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">设置在碰撞后是否保持灵敏度。启用时，即使检测到碰撞，当前检测级别也会保持不变。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left"> 
        <p>[测量] 显示在碰撞检测命令（coldet level.id）活动期间发生的最大“干扰扭矩”。</p>
        <p>[阈值] 用户可以参考此值为每个级别配置“干扰扭矩”的阈值。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p>[测量] 显示在碰撞检测命令（coldet level.id）活动期间发生的最大“干扰扭矩变化率”。</p>
        <p>[阈值] 用户可以参考此值为每个级别配置“干扰扭矩变化率”的阈值。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">重新测量每个轴的干扰扭矩和干扰扭矩变化率的最大测量值。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">用于将每个轴配置的所有级别值重置为其默认值。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left">用于添加额外的级别。可配置的最大级别数为16。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c8.png" alt/>
      </td>
      <td style="text-align:left">用于删除最高级别。删除可以从级别6及以上开始。</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
碰撞检测测量值最多显示2分钟。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/9-jog-inch-level/README.md)
# 7.4.9 Jog Inching Level Setting

您可以通过指定移动距离来限制操作。这在您希望使用手动模式中的 jog 键将机器人移动到所需距离时非常有用。

1. 触摸 `[3: Robot Parameter - 11: Set the Jog Inching Level] ([3: Robot Parameter  - 11: Set the Jog Inching Level])` 菜单。

2. 在为每个 jog inching level 设置距离和角度后，触摸 `[OK]` 按钮。

    ![](../../../_assets/tp630/robot-jog-inching_eng.png)
[__SOURCE](7-system/4-robot-parameter/9-jog-inch-level/1-jog-inch-main-funcs.md)
# 7.4.9.1 主动瞬态功能的主要功能

* 适用的瞬态坐标系统
  * 
    在关节坐标系统中的瞬态：运动将按照为每个关节指定的距离 \(mm\) 和角度 \(deg\) 进行。

  * 在笛卡尔坐标系统中的瞬态
  * 在工具坐标系统中的瞬态 
  * 在用户坐标系统中的瞬态：运动将按为 X、Y 和 Z 位置 \(mm\) 以及 Rx、Ry 和 Rz 姿态 \(deg\) 指定的量进行。
* 瞬态级别 

  您可以将瞬态距离设置为与现有 jog 速度相同的级别，因此您可以选择八个速度级别，并可以为每个级别设置瞬态距离。
[__SOURCE](7-system/4-robot-parameter/9-jog-inch-level/2-inch-jog-operation.md)
# 7.4.9.2 微调操作

微调功能是一种功能，它不允许运动超过每次按下微调键的最大移动距离。

即使达到微调距离，如果您继续按住微调键然后松手，机器人将减速至微调距离，然后停止。

![Figure 63 When Releasing the Key After Reaching the Inching Distance](../../../_assets/image_488.png)

如果您在达到微调距离之前释放微调键，机器人将从您释放微调键的时刻开始减速，然后停止。此时，模式将与普通微调模式相同。

![Figure 64 When Releasing the Hand Before Reaching the Inching Distance](../../../_assets/image_473.png)

{% hint style="info" %}
在关节坐标系中，速度等级1固定为机器人将按编码器的1位移动的模式。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/12-system-maintenance/README.md)
# 7.4.10 减速器寿命设置

如果机器人轴的减速器被更换，则应初始化减速器的额定寿命。  
减速器额定寿命的消耗速度取决于工作负载条件和速度。速度越高，负载越大，寿命减少的速度也越快。  
减速器寿命数据可以在系统特性数据中找到。  
监控菜单显示减速器的剩余额定寿命和基于最新机器人操作模式的预期寿命。  

额定寿命 : 在额定负载和额定速度条件下持续驱动时的剩余寿命<br>  
预期寿命: 基于最近实际驱动条件的估计剩余寿命。<br>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 寿命预期可能会根据机器人的最近运动模式而增加或减少。  

减速器寿命初始化  
1.    触摸`[3: Robot parameter - 12: 系统维护 - 2:Reducer Lifespan setting] ([3: Robot parameter  - 12: System maintenance  - 2:Reducer Lifespan setting])`菜单。  

2.    将光标移动到对应于更换的减速器的位置并触摸`[Reset one]`按钮。  
如果所有减速器都被更换，或机身被替换为新的机器人，则触摸`[Reset all]`按钮。在减速器的额定寿命被初始化的情况下，初始化日期会记录在更改日期列中。  

![](../../../_assets/tp630/reducer_lifetime_setting.png)  

寿命计算周期`[min]` : 减速器寿命的更新周期。最小周期为10分钟。  

{% hint style="info" %}
减速器额定寿命和预期寿命是基于减速器寿命预测模型的预测参考值。减速器的实际寿命可能会根据驱动条件与预期模型有所不同。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/13-system-diagnosis/README.md)
# 7.4.13 系统诊断

它用于多种功能以诊断机器人系统中的故障。
[__SOURCE](7-system/4-robot-parameter/13-system-diagnosis/1-gas-spring-pressure_sensor.md)
# 7.4.13.1 气弹簧压力传感器

气弹簧压力传感器功能用于通过模拟输入不断读取压力传感器的值来检测气弹簧中的异常压力，或在使用气弹簧并附带我公司指定的压力传感器（PN2570）的机器人中通过数字输入生成警告或错误。 <br> 

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
        设置接收警告的信号编号。当测量的压力超过设定的容差时，压力传感器可以输出警告。当设定信号开启时，控制器生成 W21020。 
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        错误输入
      </td>
      <td style="text-align:left">
        设置接收警告的信号编号。当测量的压力超过设定的容差时，压力传感器可以输出警告。当设定信号开启时，控制器生成 E21020。 
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
        设置输入压力传感器值的数字信号。
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        当前值
      </td>
      <td style="text-align:left">
        由压力传感器测量的压力值被显示。
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
        如果测量的压力小于参考压力减去设定的警告容差值，则会发生警告 W21018。 <br>
        如果设置了输出信号，则信号输出会开启。 
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        容差错误和输出信号
      </td>
      <td style="text-align:left">
        如果测量的压力小于参考压力减去设定的错误容差值，则会发生错误 E21018。 <br>
        如果设置了输出信号，则信号输出会开启。  
      </td>
    </tr>
  </tbody>
</table>

<br>

{% hint style="info" %}
* 此功能在版本 V60.30.07 及更高版本中受支持。   
{% endhint %}
[__SOURCE](7-system/5-application-parameter/README.md)
# 7.5 应用参数

1. 触摸`[4: Application Parameter]`菜单。然后，应用参数菜单将显示。

2. 选择所需的菜单，然后检查和设置机器人应用功能的各种参数。

    ![](../_assets/tp630/app-menu_eng.png)


<br>

{% hint style="info" %}
有关本手册未涵盖的项目，请参阅每个单独应用功能的“功能手册”。
{% endhint %}
[__SOURCE](7-system/5-application-parameter/10-cmd-idp-exe.md)
# 7.5.10 命令独立执行

这是一个功能，当设置的输入信号从 OFF 变为 ON 时，单独执行相应的语句。<br>
该语句使用未使用的子任务执行，通常使用子任务 1。<br>
有关多任务的更多信息，请参阅 "[${cont_model} 控制器功能手册 - 多任务](https://hrbook-hrc.web.app/#/view/doc-multi-task/zh/README)"。

![](../../_assets/tp630/cmd-idp-exe.png)

  * 输入信号：设置信号输入到控制器。
  * 命令：
    * 记录输入信号从 OFF 变为 ON 时要执行的语句。
    * 通常，任务启动用于静态伺服枪的枪搜索和尖端装饰工作，而移动用于定位器的独立操作。
    * 使用任务启动时，使用子任务 1 执行此命令，因此请指定子任务为 2 或更多，或将其设置为 0。（0=自动分配）
  * 正在执行的输出信号：
    * 当语句执行开始时，变为 ON，当执行完成时，变为 OFF。
    * 如果语句不是移动，则由于执行时间非常短是没有意义的。
  * 执行完成后的输出信号：
    * 当相应语句的执行开始时，变为 OFF，当执行完成时，变为 ON。
    * 如果语句不是移动，则由于执行时间非常短是没有意义的。

{% hint style="info" %}
* 仅在电机处于自动模式且开启的情况下可以执行。
* 执行移动语句时，轴必须通过机制与主任务分离，或者必须通过 axisctrl off 禁用轴控制状态。
{% endhint %}
[__SOURCE](7-system/5-application-parameter/13-user-def-error/README.md)
# 7.5.13 用户定义错误

此功能允许用户为 ${cont_model} 机器人控制器中的特定条件定义错误。当满足定义的条件时，将触发用户定义的错误。

{% hint style="info" %}
支持从 V60.30-00 开始。
{% endhint %}
[__SOURCE](7-system/5-application-parameter/13-user-def-error/1-setting.md)
# 7.5.13.1 用户定义错误设置

1. 触摸 `[System - 4: Application Parameters - 13: User-Defined Error] ([System  - 4: Application Parameters  - 13: User-Defined Error])` 菜单。<br><br>

2. 点击 "创建示例文件" 按钮。<br>
将会在 MAIN/project 目录中创建一个名为 "help_user_err.json" 的文件。<br>
![](../../../_assets/tp630/user-def-code/image1.png)

3. 重新进入设置屏幕时，将显示示例文件中写入的用户定义错误。<br>
- 错误代码：指定要触发的错误代码。
- 条件表达式：定义触发错误的条件。可以使用任何可以在 if 语句中使用的条件表达式。
- 消息：指定错误发生时显示的消息。
- 电机关闭：确定当发生用户定义错误时电机是否应关闭。<br>
![](../../../_assets/tp630/user-def-code/image2.png)

4. 将 USB 驱动器插入教学柜，访问文件管理器菜单，并将 'help_user_err.json' 文件复制到 USB 存储路径。<br><br>
![](../../../_assets/tp630/user-def-code/image3.png)

5. 在 PC 上打开文件，并根据示例文件格式编辑错误（可以使用记事本进行编辑）。<br><br>
- E65###：错误代码（范围：E65001 ~ E65500）
    - cnd：条件表达式
    - msg：显示在错误帮助中的原因消息
    - remedy：显示在错误帮助中的纠正措施
    - mot_off：电机关闭<br>
![](../../../_assets/tp630/user-def-code/image4.png)

6. 将编辑后的文件复制回教学柜。
[__SOURCE](7-system/5-application-parameter/13-user-def-error/2-example.md)
# 7.5.13.2 用户定义错误示例

1. 修改 'help_user_err.json' 文件如下所示。<br>
![](../../../_assets/tp630/user-def-code/image9.png)

2. 当 di5 信号被打开以满足条件表达式时，E65001 将被触发。<br>
![](../../../_assets/tp630/user-def-code/image10.png)

3. 检查错误帮助将显示与文件中写入的相同内容。<br>
![](../../../_assets/tp630/user-def-code/image11.png)
[__SOURCE](7-system/5-application-parameter/14-user-def-warn/README.md)
# 7.5.14 用户定义警告

此功能允许用户为 ${cont_model} 机器人控制器中的特定条件定义警告。当满足定义的条件时，将触发用户定义的警告。

{% hint style="info" %}
支持从 V60.30-00 开始。
{% endhint %}
[__SOURCE](7-system/5-application-parameter/14-user-def-warn/1-setting.md)
# 7.5.14.1 用户定义警告设置

1. 触摸`[System - 4: Application Parameters - 14: User-Defined Warning] ([System  - 4: Application Parameters  - 14: User-Defined Warning])`菜单。<br><br>

2. 点击“创建示例文件”按钮。<br>
* 将在MAIN/project目录中创建一个名为'help_user_warn.json'的文件。<br>
![](../../../_assets/tp630/user-def-code/image5.png)

3. 重新进入设置屏幕时，将显示在示例文件中写入的用户定义警告。
- 警告代码：指定要触发的警告代码。
- 条件表达式：定义触发警告的条件。可以使用if语句中的任何条件表达式。
- 消息：指定在发生警告时显示的消息。<br>
![](../../../_assets/tp630/user-def-code/image6.png)

4. 将USB驱动器插入教学挂件，访问文件管理器菜单，并将'help_user_warn.json'文件复制到USB存储路径。<br><br>
![](../../../_assets/tp630/user-def-code/image7.png)

5. 在PC上打开文件并根据示例文件格式编辑警告（可以使用记事本进行编辑）。<br><br>
- W65###: 警告代码（范围：W65001 ~ W65100）
    - cnd: 条件表达式
    - msg: 在警告帮助中显示的原因消息
    - remedy: 在警告帮助中显示的纠正措施<br>
![](../../../_assets/tp630/user-def-code/image8.png)

6. 将编辑后的文件复制回教学挂件。
[__SOURCE](7-system/5-application-parameter/14-user-def-warn/2-example.md)
# 7.5.14.2 用户定义警告示例

1. 修改 'help_user_warn.json' 文件，如下所示。<br>
![](../../../_assets/tp630/user-def-code/image12.png)

2. 当 di6 信号被打开以满足条件表达式时，将触发 W65001<br>
![](../../../_assets/tp630/user-def-code/image13.png)

3. 检查警告帮助将显示文件中写的相同内容。<br>
![](../../../_assets/tp630/user-def-code/image14.png)
[__SOURCE](7-system/5-application-parameter/16-joystick-mode/README.md)
# 7.5.16 操纵杆模式

此功能用于通过外部设备，例如操纵杆，操作机器人。

![](../../../_assets/tp630/joystick_mode_menu.png)

* 操纵杆慢速行驶启用 <br>
   为了执行与操纵杆模式对应的功能，输入信号必须设置并开启。

* 执行类型 <br>
   选择是否根据设置信号的输入状态或Open-api的输入状态执行慢速运动。 <br>
   慢速操作与T/P手动模式中的慢速键操作完全相同。


{% hint style="info" %}
* 仅在自动模式下电机打开时才会操作。
{% endhint %}
[__SOURCE](7-system/5-application-parameter/16-joystick-mode/1-jogging-in-signal.md)
# 7.5.16.1 手动操作（输入信号）

通过信号输入手动操作机器人，请设置与每个方向键对应的输入信号。 <br>
在相应输入信号为 ON 的部分，相应轴将在指定方向上移动。 <br>

当输入信号设置为坐标系统时，如果输入信号开启，则选择匹配的坐标系统。 <br>

与机制编号对应的输入信号可以根据状态更改机制。 <br>

![](../../../_assets/tp630/jogging_in_signal.png)
[__SOURCE](7-system/5-application-parameter/16-joystick-mode/2-jogging-open-api.md)
# 7.5.16.2 Jogging(open-api)

请参阅关于open-api通信的单独手册。 <br>
有关机器人操纵的url地址和请求体的信息如下。

* url : POST /project/robot/joystick/joy
* body <br>
    axis : 由双精度类型数组组成。 axis[0] 对应于 J1。 值为 -1 表示向左移动，值为 +1 表示向右移动。 <br>


{% hint style="info" %}
如果在300ms内未收到数据，操纵运动将停止。  
{% endhint %}
[__SOURCE](7-system/5-application-parameter/16-joystick-mode/3-speed-level.md)
# 7.5.16.3 速度

此功能通过信号输入改变机器人慢跑的速度等级。 <br>
当设定的输入信号变为 ON 时，它会变更为相应的速度等级，并将相应的输出信号也设置为 ON。 <br>

![](../../../_assets/tp630/speed_level.png)
[__SOURCE](7-system/5-application-parameter/16-joystick-mode/4-robot-move.md)
# 7.5.16.4 移动

这是一个将机器人指定的轴通过信号输入移动到指定位置的功能，移动速度为指定速度。 <br>
在下图中，当 fb2.di34 信号开启时，机器人以 10% 的速度移动，使机器人的 6 个轴的位置达到 30 度。 <br>

如果您想同时移动两个或多个轴，请将输入信号设置为相同的值。此时，运动速度应用于其中第一个记录的设置值。 <br>

![](../../../_assets/tp630/robot_move.png)
[__SOURCE](7-system/5-application-parameter/22-reduced-speed-mode.md)
# 7.5.22 降速模式

当输入信号（di）从关闭变为开启时，机器人速度将根据设定的降低比率降低。 <br>
在移动命令中，机器人速度通过将原始速度值与自动模式下的机器人速度和降低比率结合应用。 <br>

![](../../_assets/tp630/reduced_spd_mode.png)

  * 输入信号：设定控制器接收的信号。
  * 活动：
    * 高：信号为开启时应用降低，信号为关闭时取消。
    * 低：信号为关闭时应用降低，信号为开启时取消。
  * 降低速度比率：  
    * 决定速度降低的比率。
    * 当接收到降速模式输入信号时，机器人速度设定为自动模式的机器人速度乘以降低速度比率。

{% hint style="info" %}
* 在手动模式下不应用降低比率。
{% endhint %}

{% hint style="warning" %}
* 选择与输入信号状态匹配的正确激活条件。
* 在播放期间接收到I/O信号时，仍会应用降速模式。
{% endhint %}
[__SOURCE](7-system/5-application-parameter/23-scurve-condition/README.md)
# 7.5.23 S-curve Condition

S-curve指的是根据任务调整路径准确性和 residual vibration 的运动轨迹规划，使最佳过程的设计成为可能。

![](../../../_assets/tp630/s-curve_velocity_comparison.png)

该图比较了默认的速度轮廓法与 S-curve 速度轮廓法。

默认（蓝色实线）：加速的开始和结束都伴随突变的加速，这可能会导致振动。  
S-curve（红色虚线）：加速和减速期间的速度变化更为平滑。这最小化了机器人振动并减少了路径误差，即使在运动速度改变时也是如此。

{% hint style="warning" %}
* 如果连续运动生成失败，运动将作为不连续（中断）运动执行。在该区域，调整参数或切换回默认运动（Default）以确保可靠操作。  
* 历史日志可用于查看连续运动失败的记录。  
{% endhint %}

{% hint style="info" %}
* 此功能支持从版本 V70.00‑00 开始。  
* 请参考 ${cont_model} 控制器手册中的命令语法 "[5.22 scurve](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/5-moving-robot/22-s-curve?cont_model=${cont_model})"  
{% endhint %}
[__SOURCE](7-system/5-application-parameter/23-scurve-condition/1-scurve-condition.md)
# 7.5.23.1 S-curve condition

S‑curve 条件设置允许您详细定义机器人操作时发生的加速和减速阶段的特性。配置以下项目以匹配每个过程所需的特性（例如路径精度或振动减少）。

![](../../../_assets/tp630/s-curve_condition.png)

  * 状态名称：输入条件的名称。
  * 路径精度 <br>
    决定机器人遵循指定轨迹的忠实度。对于如加工或精密组装等过程，建议使用更高的值，以最小化轨迹偏差。
    较大的值提高路径精度，但也可能导致相对较高的振动。
  * 平稳运动 <br>
    决定加速和减速变化的温和程度。当您需要保护易碎工件（例如玻璃）、过程对振动敏感或希望减少对机器人硬件的机械冲击时，使用更高的值。较大的值产生更平滑的运动，但也会增加周期时间。如果设置的值过高，可能会导致机器人无法执行连续运动，导致其以不连续的方式移动。

## 示例设置

* 精密加工和点胶（路径精度优先）
  * 机器人必须准确地遵循预定轨迹。

  * 推荐设置：
    * 路径精度：高（例如，80 ~ 100）
    * 平稳运动：低到中等（例如，20 ~ 40）

  * 用例：沿汽车零件的复杂曲线涂抹密封剂或进行激光切割。为了最小化轨迹误差，设置高精度；保持路径比轻微振动更重要。

  * 注意：根据实际机器人的振动行为和特定过程规格调整参数。

* 敏感货物运输（振动减少，平稳运动优先）
  * 一个过程，其中振动可能损坏产品或导致错位。

  * 推荐设置：
    * 路径精度：中等（例如，50）
    * 平稳运动：高（例如，80 ~ 100）

  * 用例：运输半导体晶圆、大型玻璃面板（LCD/OLED）或含有易溢液体的容器。在加速/减速期间最小化冲击，以防止滑动或晃动。

  * 注意：由于运动变得更加平滑，整体周期时间（操作时间）可能会增加，或者可能需要执行不连续的运动。
[__SOURCE](7-system/5-application-parameter/23-scurve-condition/2-acceldecel-parameter.md)
# 7.5.23.2 加速/减速参数

S曲线条件和**最大加加速度**相辅相成。当仅用S曲线设置优化某个过程困难时，或者当需要为每个关节调整最大加加速度限制时，您可以调整参数。

![](../../../_assets/tp630/s-curve_acceldecel_parameter.png)

加加速度与运动之间的关系
加加速度是加速度变化的速率，修改此值会产生以下特征变化。

- **减少最大加加速度 (↓)：** 加速度变化更为渐进，使运动更平滑，并减少振动。然而，达到目标速度所需的时间更长，这可能会增加循环时间。

- **增加最大加加速度 (↑)：** 提供更灵敏的运动，但如果值过高，则S曲线条件的“平滑运动”效果会减弱，从而导致更大的机械冲击。

最大加加速度的自动更新
每当关键参数更改时，系统会自动重新计算最大加加速度值，以保持设备的稳定性。

{% hint style="warning" %}
**警告：** 当您手动设置一个值时，修改最高速度或加速时间将会用系统计算的值覆盖手动输入的最大加加速度。如果您已针对特定过程优化了加加速度值，请确保在进行更改之前备份现有值。
{% endhint %}


{% hint style="info" %}
由于加速/减速参数对机器人运动特性有很大影响，因此仅在工程模式或更高模式下启用。
{% endhint %}
[__SOURCE](7-system/6-initialization/README.md)
# 7.6 初始化

如果机器人控制器无法正常运行，请初始化系统。系统初始化必须由具有 HD Hyundai Robotics 机器人初始设置经验的工程师执行。

1. 触摸 `[5: 初始化]` 菜单。然后，初始化菜单将出现。

2. 选择所需的菜单，然后执行机器人系统的初始设置，然后初始化串行编码器。

    ![](../../_assets/tp630/init-menu_eng.png)

{% hint style="info" %}
在 `[初始化]` 菜单中的某些项目仅在选择特定类型的附加轴时支持。
{% endhint %}

{% hint style="info" %}
* 要初始化系统，您应联系客户支持团队并请求专家或合格的工程师以防止错误操作。
* 
  当系统初始化时，控制器中保存的所有数据和程序将被删除。在初始化系统之前，您应备份您的数据和程序，并在必要时恢复它们。

  有关数据备份和恢复的详细信息，请参阅 "[4.2.5 数据备份](../../4-service/2-file-manager/5-data-backup.md)" 和 "[4.2.6 数据恢复](../../4-service/2-file-manager/6-data-restore.md)"。
{% endhint %}
[__SOURCE](7-system/6-initialization/1-system-format.md)
# 7.6.1 系统格式

1. 在${cont_model}示教器屏幕的状态栏上，检查操作模式是否设置为手动模式。

    ![](../../_assets/tp630/sbar-mode-manual_eng.png)

    如果设置为自动模式，请将示教器的模式开关切换到手动模式。

    ![](../../_assets/tp630/TP-hw-switch-manual.png)

2. 点击`[system]`按钮 - `[5: 初始化 - 1: 系统格式] ([5: 初始化 - 1: 系统格式])`菜单。

3. 在检查已保存的数据后，点击`[Initialize]`按钮。所有数据和程序，包括控制参数文件和机器参数文件，将被删除，初始设置值将被恢复。

    ![](../../_assets/tp630/pop-system-init_eng.png)
[__SOURCE](7-system/6-initialization/2-robot-type-sel.md)
# 7.6.2 机器人类型选择

1. 触摸 `[5: Initialize - 2: Robot Type Selection] ([5: Initialize - 2: Robot Type Selection])` 菜单。或者触摸 ${cont_model} 教学挂件屏幕右上角的 `[Mechanism]` 按钮。

2. 在机器人型号选择窗口中选择一个机器人，然后触摸 `[OK]` 按钮。

    ![](../../_assets/tp630/init-robot-select_eng.png)

* 您可以滚动浏览机器人型号列表以检查型号名称，或者可以输入型号名称进行搜索。
* 如果您触摸机器人使用按钮，则仅可在列表中查看属于该用途的机器人。
* 
  如果您选择了一个新机器人型号，机器参数文件 \(hi6\_porj.json\) 将恢复为初始设置值，各种历史文件也将被初始化。

* 
  如果您选择一个包含额外轴（如旅行轴或伺服枪）的系统，则应设定额外轴的数量。如果系统仅由机器人轴组成而没有额外轴，请输入 0。

  ![](../../_assets/tp630/init-addaxis-pop_eng.png)

{% hint style="warning" %}
* 操作臂和控制器作为一个系统发货。因此，机器人控制器配备了适合作为系统部分的机器人的驱动能力的驱动器。
* 当通过初始化重置系统时，必须检查出厂时设置为初始设置值的机器人的型号，然后设置正确的型号。

{% endhint %}

3. 在 ${cont_model} 教学挂件屏幕右下角触摸 `[Favorites]` 按钮，在收藏窗口的输入区域输入 314，然后触摸 `[OK]` 按钮。

    ![](../../_assets/tp630/pop-rcode-314_eng.png)

{% hint style="warning" %}
* 在工程师模式下，工程师模式图标\(![](../../_assets/eng-mode.png)\)将在状态栏上闪烁。
* 请注意，如果设置不正确，机器人系统可能会发生严重问题。
{% endhint %}

4. 触摸 `[system]` 按钮 - `[3: Robot Parameter - 4: Encoder Offset] ([3: Robot Parameter - 4: Encoder Offset])` 菜单。

5. 执行编码器偏移校准。即使机器人位置不是参考位置，也应临时设置编码器偏移以启动车载电机。

    ![](../../_assets/tp630/robot-encoder-offset__eng.png)

{% hint style="info" %}
* 您应在机器人移动到参考位置后正常执行编码器偏移设置。
* 对于初始设置，即使机器人位置不是参考位置，您也应执行编码器偏移设置。否则，电机将无法启动车辆，导致无法驱动机器人。

{% endhint %}

6. 关闭控制器电源，然后重新开启电源，接着给电机供电。

7. 在手动模式下，以低速安全移动机器人到参考位置，然后根据步骤 7-8 再次执行编码器偏移校准。

* 在编码器偏移设置项中，当前编码器位置将设置为 0X400000 \(十六进制\)。
* 更换电机因为故障时，如果在同一位置执行编码器偏移设置，记录的程序可以完全相同地使用。

8. 按下教学挂件上的 `[Program]` 键，选择程序 9999，然后记录一个步骤。您可以轻松将机器人移动到参考位置。

{% hint style="warning" %}
* 要初始化系统，请联系客户支持团队并寻求专家的帮助。
* 
  有关协作机器人的初始化，请参阅协作机器人安全功能手册。

* 
  当系统初始化时，包括控制参数文件和机器参数文件在内的所有数据和程序将被删除。如果在初始化系统之前备份您的数据，则可以在必要时恢复并使用。
{% endhint %}
[__SOURCE](7-system/6-initialization/3-usage-set/README.md)
# 7.6.3 使用设置

您可以根据操作使用情况选择操作使用并初始化用户密钥和输入/输出分配信号。

1. 触摸 `[5: Initialize - 3: Usage Setting] ([5: Initialize  - 3: Usage Setting])` 菜单。

2. 选择操作使用情况并根据使用情况设置环境条件后，触摸 `[OK]` 按钮。然后，您可以使用与所选操作使用相关的命令并访问相关菜单。
[__SOURCE](7-system/6-initialization/3-usage-set/1-spot-welding.md)
# 7.6.3.1 点焊

如果您选择操作使用为点焊，则可以使用与点焊相关的命令并访问与点焊相关的菜单。

![](../../../_assets/tp630/init-usage-spot_eng.png)

1. 将 `[Spot Welding]` 设置为启用。然后，其他用途将被处理为禁用。

2. 分别单击 `[User Key Initialization]` 下拉菜单和 `[Input/Output Assign Initialization]` 下拉菜单，然后选择点焊。
[__SOURCE](7-system/6-initialization/3-usage-set/2-arc-welding.md)
# 7.6.3.2 弧焊

如果您选择操作用法为弧焊，您可以使用与弧焊相关的命令并访问与弧焊相关的菜单。

![](../../../_assets/tp630/init-usage-arc_eng.png)

1. 在 `[Arc Welding]` 中设置焊机类型 \(模拟或数字\)。其他用法将被处理为禁用，并且系统支持的焊机列表将出现在屏幕的底部。

2. 检查焊机列表后，设置焊机编号。

3. 点击 `[User Key Initialization]` 下拉菜单和 `[Input/Output Assign Initialization]` 下拉菜单，并分别选择弧焊。
[__SOURCE](7-system/6-initialization/4-serial-encoder-reset.md)
# 7.6.4 串行编码器重置

串行编码器将编码器旋转速度信息存储在内部内存中。通过解决电机错误状态或重置编码器的零点，可以将编码器旋转速度清零。

1.	触摸`[5: Initialize - 4: Serial Encoder Reset] ([5: Initialize - 4: Serial Encoder Reset])`菜单。

2.	为每个轴设置编码器重置模式并检查状态，然后执行重置。

    ![](../../_assets/tp630/init-serialenco-reset_eng.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>您可以为每个轴设置是否使用编码器重置功能，并为每个轴设置模式。</p>
        <ul>
          <li>[禁用]: 不执行串行编码器重置。</li>
          <li>[错误释放]: 您可以清除与电机编码器相关的错误，而不清除编码器旋转速度。</li>
          <li>[重置]: 通过解决与电机编码器相关的错误，然后重置编码器的零点，可以清除旋转速度。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[执行]: 您可以执行串行编码器重置。</li>
          <li>[全选]: 您可以一次选择所有轴。</li>
          <li>[全取消]: 您可以一次取消所有轴的选择。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
* 在执行机器人系统的初始设置时，您可以执行编码器重置，但绝不要在机器人正常操作时执行编码器重置。然而，如果发生通信错误等与编码器相关的错误或编码器电池丢失，您可以执行编码器重置。在这种情况下，请在机器人程序中检查实际位置，以便与现有机器人原点位置不发生差异。
* 如果控制器和编码器未供电，编码器的位置信息可能会丢失，可能会导致使用机器人作业程序时出现问题。为解决此问题，专用电池连接到串行编码器，使其能够在控制器的电源状态下记录位置信息。如果在编码器电池中发生电压错误，必须在控制器仍然通电的情况下更换电池，以防止丢失位置信息。
{% endhint %}
[__SOURCE](7-system/6-initialization/5-add-axis-param.md)
# 7.6.5 额外轴参数设置

除了机器人本身，可以使用的附加轴包括机器人的基轴（移动轴）、伺服枪轴、定位器轴和夹具轴。有关每个附加轴规格的详细信息，请参阅《附加轴功能手册》。

设置正在使用的附加轴的规格和配置等参数的方法如下。

1. 触摸 `5: 初始化 - 5: 附加轴参数设置 (5: Initialize - 5: Additional Axis Parameter Setting)` 菜单。

2. 设置附加轴的规格和配置等参数。

    ![](../../_assets/tp630/init-addaxis_eng.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>附加轴的详细参数设置信息。您可以查看和设置附加轴的名称、规格和配置等。</p>
        <ul>
          <li><b>[名称]</b>: 正在使用的附加轴的名称</li>
          <li><b>[轴规格]</b>: 附加轴的规格。您可以根据规格使用为每种附加轴的用途单独开发的功能。</li>
          <li><b>[轴结构]</b>: 附加轴的机制类型。在某些轴的规格中，您可以指定提前注册的机制类型。作为示例，您可以在定位器的情况下选择标准定位器型号。</li>
          <li><b>[轴位置]</b>: 这是轴连接到DSP板的位置。您可以根据接线规格依次指定BD号、DSP号、轴号和刹车号。</li>
          <li><b>[减速比]</b>: 附加轴的电机和连杆的减速比信息
            <ul>
              <li>当附加轴连杆朝（+）方向移动时，减速比符号可以根据电机轴的旋转方向进行设置。从正面来看，如果轴逆时针旋转，则符号为（+），如果顺时针旋转，则符号为（-）。</li>
              <li>减速比的分子参数是连杆的移动距离（mm或度），而分母对应的参数是与连杆的移动距离相对应的电机转速。设置项的参数将以整数形式定义。对于需要显示小数的参数，通过将分子和分母乘以某个倍数，将减速比设置为整数。</li>
            </ul>
          </li>
          <li><b>[软限制]</b>: 附加轴的最小和最大操作范围</li>
          <li><b>[AMP规格]</b>: 附加轴的放大器规格</li>
          <li><b>[电机规格]</b>: 连接到附加轴的电机型号名称</li>
          <li><b>[加速/减速参数]</b>: 附加轴的最大速度和加速时间</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[旋转半径]</b>: 您可以添加一个新的附加轴或删除一个附加轴。</li>
          <li><b>[减速比校准]</b>: 您可以校准真实轴位置与显示位置之间的差异。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>`[确定]`: 您可以保存更改。</li>
          <li><b>[+]/[-]</b>: 您可以添加一个新的附加轴或删除一个附加轴。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](7-system/6-initialization/6-mechannism-set.md)
# 7.6.6 机制设置

机制将在 jog 操作期间作为一组使用，jog 键将分配给它。此外，机制也是一组单元，每个单元在记录或编辑步骤位置的过程中要被区分。当机制被设置之后，将为每个轴的单独组分配机制编号 \(M\#\)。

设置无尽功能的方法如下。

1. 触摸 `[5: Initialization - 6: Mechanism Setting] ([5: Initialization  - 6: Mechanism Setting])` 菜单。

2. 在设置机制编号并为每个轴配置无尽功能之后，点击 `[OK]` 按钮。

    ![](../../_assets/tp630/robot-mechanism_eng.png)

* `[Mech]`: 通过触摸下拉菜单，您可以设置轴的机制编号。
  * 如果轴的规格是机器人，机制编号将固定为 M0。
  * 
    从附加轴开始，您可以将机制编号指定为介于 M1 和 M7 之间的值。

  * 
    设置相同机制编号的轴将作为同一组进行管理。

  * 
    要 jog 附加轴，您可以使用 `[Mech]` 按钮在机制之间切换。在此时，如果您按下 jog 键，将在相关机制的轴的顺序中进行 jog 操作。
* 
  `[Positioner Group]`: 您可以设置定位器组编号。只有在规格设置为定位器的轴上才能设置定位组编号。

* 
  `[Endless]`: 您可以设置是否在轴上使用无尽功能。



{% hint style="info" %}
集成的机制单元是可以分配给每个任务的最小单元，并且可以驱动。可以将复杂的机制组合分配给各个任务。
{% endhint %}

#### 




#### 机制 Jog 规则 

* ${cont_model} 控制器提供总共八个 jog 键。
* 
  机制将在 jog 操作期间作为一个组使用。

* 
  如果将机制编号选择为 `[M0]`，则轴 7 和 8 的 jog 键将作为特例操作，并且可以在包括下一个机制的轴总数为八个或更少的范围内操作 M1 和 M2。即使在这种情况下，如果您将机制编号设置为 `[M1]`，您也可以对 M1 的配置元素执行 jog 操作。

* 
  以下显示了用法示例。

  示例 1\) M0: 机器人 \(轴 1-6\)。 M1: 移动轴 \(轴 7\)。 M2: 伺服枪 \(轴 8\)

  * 选择 `[M0]` => 轴 1-6 的 jog 键: M0。 轴 7 的 jog 键: M1。 轴 8 的 jog 键: M2
  * 选择 `[M1]` => 轴 1 的 jog 键: M1
  * 选择 `[M2]` => 轴 1 的 jog 键: M2

  示例 2\) M0: 机器人 \(轴 1-6\)。 M1: 移动轴 \(轴 7\)。 M2: 伺服枪 \(轴 8-9\)

  * 选择 `[M0]` => 轴 1-6 的 jog 键: M0。 轴 7 的 jog 键: M1
  * 选择 `[M1]` => 轴 1 的 jog 键: M1
  * 选择 `[M2]` => 轴 1-2 的 jog 键: M2

  示例 3\) M0: 机器人 \(轴 1-7\)。 M1: 移动轴 \(轴 8\)。 M2: 伺服枪 \(轴 9-10\)

  * 选择 `[M0]` => 轴 1-7 的 jog 键: M0。 轴 8 的 jog 键: M1
  * 选择 `[M1]` => 轴 1 的 jog 键: M1
  * 选择 `[M2]` => 轴 1 的 jog 键: M2
[__SOURCE](7-system/7-auto-calibration/README.md)
# 7.7 自动校准

要正确使用机器人，可以使用教导程序和将自动执行的移动找到机器人的轴原点、工具长度、负载质量和基轴方向。这些校准值将自动反映在机器人中。

1. 触摸`[6: 自动校准]`菜单。然后，自动校准菜单将出现。

2. 通过选择所需菜单校准机器人的轴原点、工具长度、负载质量、基轴方向等。

    ![](../../_assets/tp630/system-calib-menu_eng.png)
[__SOURCE](7-system/7-auto-calibration/1-axis-origin-tool-length-optimization.md)
# 7.7.1 优化轴原点和工具长度

轴原点和工具长度的优化功能是用来校准机器人每个轴的原点和工具长度，而无需使用外部测量传感器。

准备两个尖头。一个固定在外侧，另一个固定在工具上。然后，仅根据外部固定尖头改变机器人的工具提示的姿态，您需要使用机器人程序记录多个点。在此过程中，您需要教七个点来寻找轴原点和工具长度，而四个点或更多仅用于寻找工具长度。

![图67 轴原点和工具长度优化功能的教学方法](../../_assets/image_228.png)

使用轴原点和工具长度优化功能，即使没有可用的CAD数据，您也可以找到优化的工具长度X、Y和Z以及机器人H、V、R2和B轴的优化原点。

{% hint style="warning" %}
当使用轴原点和工具长度优化功能时，编码器偏移和工具长度将会改变，从而也改变以前教学程序的操作位置。因此，您应该在编写教学程序之前进行轴原点和工具长度的优化。
{% endhint %}

{% hint style="info" %}
* 在使用轴原点和工具长度优化功能时，教学的准确性与最大步骤位置误差结果的准确性成正比。因此，您应该准备两个尖头，并尽可能准确地进行工具提示的教学，使两个尖头保持匹配。确保工具提示与空间中固定点之间的匹配精度在视觉检查时不超过0.5mm。
* 通过设置姿态，确保每个步骤之间的差异在30度或以上，以使步骤的姿态不相似。
* 在一个步骤中尽可能大地操作手腕轴\(R2, B, R1\)，并在每个步骤保持手腕轴的充分角度差异。
* 教学程序必须由隐藏姿态步骤命令组成。
{% endhint %}

使用轴原点和工具长度优化功能的方法如下。

1. 触摸 `6: Auto Calibration - 1: Optimize Axis Origin and Tool Length` 菜单。

2. 选择优化目标并设置详细选项。

    ![](../../_assets/tp630/system-calib-tool_eng.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>附加轴的详细参数设置信息。您可以检查并设置附加轴的名称、规格和配置。</p>
        <ul>
          <li><b>[优化选择]</b>: 您可以选择优化目标。
            <ul>
              <li><b>[工具长度]</b>: 您可以校准机器人的工具长度值。
                如果机器人原点设置正确，您只能校准工具长度。</li>
              <li><b>[轴原点 &amp; 工具长度]</b>: 您可以同时校准机器人的
                原点和工具长度值。
                <br />通常，这个功能可以在安装机器人后初始设置正确原点时使用。</li>
            </ul>
          </li>
          <li><b>[程序编号]</b>: 您可以设置同一个点在多个姿态下记录的程序编号。</li>
          <li><b>[工具编号]</b>: 这是要自动设置的工具编号。
            这应与记录在设置程序中的工具编号匹配。</li>
          <li><b>[步骤位置误差容差]</b>: 您可以设置自动校准结果的误差范围（初始设置值为0.6mm）。如果预期误差在误差范围内，整数数据将会自动更新；如果误差超出误差范围，是否要反映整数将通知并确认用户，然后进行必要的处理。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>`[确定]`: 您可以保存更改。</li>
          <li>`[执行]`: 您可以根据设置的信息执行优化。
            优化结果将出现在 [最大步骤位置误差] 中。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
请注意，如果您校准机器人原点和工具长度值，机器人的所有原点将会改变，因此会改变之前创建程序的位置。
{% endhint %}

{% hint style="info" %}
* 您还可以在设置菜单中设置机器人的每个轴的原点和工具长度。
  * 工具长度: `[system] - 3: Robot Parameter - 1: Tool Data`。
  * 每个轴的原点: `[system] - 3: Robot Parameter - 2: Axis Origin`
* 如果您使用角度校准功能\( `[system] - 3: Robot Parameter - 1: Tool Data`\) 校准工具角度，您应该首先执行原点轴和工具长度优化功能，然后再执行角度校准。这样，可以正确设置工具数据。
{% endhint %}
[__SOURCE](7-system/7-auto-calibration/2-positioner-calib.md)
# 7.7.2 位置器校准

位置器校准是一项功能，使机器人能够与安装在机器人外部的夹具设备的操作进行同步跟随，或相对于夹具设备执行线性或圆形操作。将在位置器校准功能应用于的外部夹具设备称为位置器或工作站。

使用位置器校准功能可以补偿由于机器人操作区域的限制而导致的操作困难。换句话说，即使位置器在工件固定在其上的情况下移动，机器人仍然可以通过跟随位置器的移动在工件上执行线性或圆形操作。

您可以通过教学1轴位置器的三个点或2轴位置器的五个点来简单地设置位置器的坐标系统。

![图68 1轴位置器 \(左\) / 2轴位置器 \(右\)](../../_assets/image_244.png)

位置器校准的主要功能信息如下。

| 主要功能 | 描述 |
| :--- | :--- |
| 位置器组 | 支持1-4个组 |
| 位置器轴计数 | 支持1轴位置器和2轴位置器 \(旋转轴\) |
| 插值模式 | 支持线性插值和圆形插值 |

{% hint style="info" %}
* 位置器校准功能可以在设置好位置器组的情况下使用。
* 有关更多详细信息，请参阅"[${cont_model} 控制器位置器同步功能手册](https://hrbook-hrc.web.app/#/view/doc-positioner-sync/zh/README?cont_model=${cont_model})"。
{% endhint %}
[__SOURCE](7-system/7-auto-calibration/3-load-estimation.md)
# 7.7.3 负载估算功能

负载估算是一个通过特定操作自动计算工具的物理属性（质量、中心位置、惯性）的功能，这些工具连接在机器人的前端。

操纵器信息（质量、质心、每个连杆的惯性）登记在控制器中。然而，由于工具在必要时会附加在机器人的前端使用，因此需要输入工具信息。工具物理属性的信息包括工具质量（kg）、中心位置、以及安全使用机器人所必需的惯性。

如果CAD数据包含工具的物理属性信息，则可以通过触摸`[system]`按钮 - `[3: Robot Parameter - 1: Tool Data] ([3: Robot Parameter  - 1: Tool Data])`作业程序菜单直接输入工具的质量、中心位置和惯性。

![](../../_assets/tp630/robot-tool_1_eng.png)

工具数据设置的信息如下。

![Figure 70 Tool Data](../../_assets/image_505.png)

* `[Weight]`: 安装在机器人前端的工具的总重量（kg）
* `[Center]`: 从机器人法兰面中心到工具重心位置的x、y、z方向的距离（mm）
* `[Inertia]`: 相对于工具坐标系的工具的转动惯量（kg/m²）。转动惯量将根据重心周围的x、y、z轴质量分布决定，并且当负载质量远离旋转轴分布时，将增加。
* 工具数据坐标系：惯性和中心将以相对于x、y、z轴方向的值表示。

然而，在许多情况下，难以从CAD数据中确定工具的物理属性，如质量、惯性和工具的重心。此时，可以使用机器人控制器中的负载估算功能检查工具的物理属性。

![Figure 71 Load Estimation Function](../../_assets/tp630/system-calib-load_eng.png)

1. 触摸`[6: Auto Calibration - 4: Load Estimation Function] ([6: Auto Calibration  - 4: Load Estimation Function])`菜单。

2. 在触摸`[Add. Weight on Each Axis]`按钮后，输入每个轴的附加重量信息。

如果在存在附加重量的情况下执行负载估算功能，将判断所有装在机器人的重量物体位于前端。为了准确进行负载估算，应输入每个轴的附加重量信息。

3. 通过移动机器人的主轴将机器人移动到安全区域后，触摸`[Set pose]`按钮。

4. 在触摸`[Wrist Axis Operation Area]`按钮后，指定在负载估算操作中使用的腕轴操作区域。负载估算可以在与附近设施以及操纵器没有干扰的操作区域内进行。

如果不支持`[Wrist Axis Operation Area]`按钮，请跳过此步骤，执行下一步。

5. 触摸`[Play check]`按钮。然后，在机器人以低速运行时，可以检查与附近设施或操纵器的任何干扰。

6. 输入安装在机器人的工具编号后，触摸`[Play Normal]`按钮。然后，将执行负载估算，从而计算出工具的物理属性。

7. 在检查负载估算结果后，触摸`[End]`按钮。然后，计算出的工具物理属性将注册在工具编号中。

{% hint style="info" %}
* 附加重量是用户附加到机器人上的所有设备的总体重量，如焊接装置和焊接信号线继电器箱，但不包括安装在机器人前端的工具。

* 一些机器人可能不支持腕轴操作区域功能。

* 负载估算功能的执行可能会依赖于腕轴操作区域功能的设定值，请注意。
* 有关负载估算功能的详细信息，请参阅“负载估算功能手册”。
{% endhint %}
[__SOURCE](7-system/7-auto-calibration/4-base-axis-calibration/README.md)
# 7.7.4 基座轴校准

基座轴校准是一个用于校准轴的安装方向的功能。

几乎不可能将基座轴安装到机器人坐标系统的任一方向 \(X, Y, 或 Z\) 完全匹配。当您使用基座轴校准功能在控制器中计算基座轴的方向时，可以提高系统（包括基座轴）的线性插补轨迹的性能。

在机器人安装在基座轴上之后，此功能使得通过找到安装机器人所用的任何基座轴的方向向量来执行位置插补成为可能。

![Figure 72 Base Axis Calibration](../../../_assets/image_497.png)


一般来说，基座轴用于将机器人移动到操作位置。在特殊情况下，基座轴也可以在机器人移动在基座轴上时需要保证线性轨迹的情况下使用。

* 当两台基座轴校准的机器人交付工件时 \(未来将支持多机器人\)
* 当您需要在操作基座轴时执行插补时
[__SOURCE](7-system/7-auto-calibration/4-base-axis-calibration/1-base-axis-initial-set.md)
# 7.7.4.1 基轴初始设置

1. 在手动模式下，触摸 `系统 - 5: 初始化 - 5: 附加轴参数设置 (system - 5: Initialize - 5: Additional Axis Parameter Setting)`。

2. 在设置了附加轴的规格和配置等参数后，触摸 `[OK]` 按钮。

* `[轴规格]`: 您可以选择将附加轴作为基轴的规格。
* `[轴配置]`: 您可以选择附加轴的机制为任意。
* 其他参数: 您可以根据仪器设计值和控制器配置规格设置其他参数。

{% hint style="info" %}
* 当系统初始化时，附加轴设置菜单将出现，允许您执行基轴的初始设置。
* 
  附加轴参数设置菜单是工程师的功能，因此不支持一般用户。如需了解附加轴参数设置菜单的详细信息，请联系工程师进行咨询。
{% endhint %}

{% hint style="warning" %}
您只能对第一个基轴使用校准功能，并且在设置附加轴参数时可以将轴配置设置为任意。除第一个基轴外，请勿将其他基轴的轴配置设置为任意。
{% endhint %}
[__SOURCE](7-system/7-auto-calibration/4-base-axis-calibration/2-base-axis-calib-prog-teach.md)
# 7.7.4.2 基础轴校准程序教学

1. 在空间中建立一个参考点，然后记录第一个参考点。

2. 将基础轴移动超过 200 mm，并将相同的点记录为第二步。

3. 在与第二步中移动的方向相同的方向上移动 200 mm 或更多，然后将相同的点记录为第三步和第四步。

![](../../../_assets/image_526.png)



{% hint style="warning" %}
* 使用已完成机器人校准（轴原点和工具长度的优化）的工具来教学行程轴校准程序。
* 
  记录步骤时，使用工具编号进行基础轴校准。

* 
  尽可能设置基础轴在记录步骤之间的移动距离来记录位置。
{% endhint %}
[__SOURCE](7-system/7-auto-calibration/4-base-axis-calibration/3-base-axis-calib-exec.md)
# 7.7.4.3 基座轴校准执行

1. 触摸 `[6: Auto Calibration - 6: Base Axis Calibration] ([6: Auto Calibration  - 6: Base Axis Calibration])` 菜单。

2. 输入基座轴校准的程序编号后，触摸 `[Auto Setting]` 按钮。

    ![](../../../_assets/tp630/system-calib-base_eng.png)

3. 查看基座轴的安装方向向量值后，触摸 `[OK]` 按钮。
[__SOURCE](7-system/7-auto-calibration/4-base-axis-calibration/4-operation-after-base-calib.md)
# 7.7.4.4 基座轴校准后的操作

如果在执行基座轴校准后移动基座轴，基座轴创建的方向向量中的行程将转换为当前坐标值。

![图73 基座轴校准后的操作](../../../_assets/image_528.png)

1. 触摸工作区面板堆栈右上角的`[+]`按钮，然后在面板选择窗口中触摸`[Pose]`。

2. 移动基座轴。沿基座轴移动的距离将转换为X、Y和Z值，并在位置信息窗口中显示。

3. 按照 usual way 记录和回放步骤。

{% hint style="warning" %}
将 jog 坐标系统设置为工具坐标系统，并移动基座轴以检查基座轴是否正确校准。如果执行了工具提示固定操作，则表示基座轴已正确校准。
{% endhint %}
[__SOURCE](7-system/7-auto-calibration/5-gravity-direction-auto-set.md)
# 7.7.5 重力方向自动设置

${cont_model} 控制器基于动态，因此设置重力方向非常重要。

通常，机器人安装方向垂直于重力方向，如下所示。如果机器人斜放在地面上，则需要在机器人控制器中设置重力方向。在此时，可以使用自动重力方向设置功能。

![图74 安装在地面上的机器人重力方向（左）/ 安装在斜坡上的机器人重力方向（右）](../../_assets/image_507.png)



设置重力方向的方法如下。

1.	在外部附加一个重量以指示重力方向，然后教学两个点（步骤1，步骤2）在重力作用的方向上。

2.	触摸 `[6: 自动校准 - 8: 重力方向的自动设置] ([6: 自动校准 - 8: 重力方向的自动设置])` 菜单。

3.	在输入程序编号后，触摸 `[执行]` 按钮。然后，方向向量将被计算并显示。

    ![](../../_assets/tp630/system-calib-gravity_eng.png)


4.	在检查方向向量值后，触摸 `[确定]` 按钮。然后，方向将被设置为重力方向。
[__SOURCE](7-system/7-auto-calibration/6-robot-tool-calibration.md)
# 7.7.6 机器人的校准和工具

机器人和工具的校准功能将在可以使用3D测量设备测量机器人位置的环境中使用。

1. 在机器人的工具提示中选择要测量的位置，移动机器人的位置和姿态，以多种方式测量超过15个点的位置，并将机器人位置记录为程序。

    ![](../../_assets/image_245.png)

2. 将测量到的机器人的位置数据（测量点数据）整理为X、Y和Z格式，然后创建一个文件（格式：ASCII 扩展名：MSR）。

    ![](../../_assets/tp630/system-calib-robottool-msr.png)

3. 将位置数据文件保存到可移动存储设备中，然后将可移动存储设备连接到教学挂件。`[USB]` 图标（ ）将在 ${cont_model} 教学挂件屏幕的状态栏中出现。

4. 点击 `[6: 自动校准 - 9: 机器人和工具校准条件] ([6: Auto Calibration  - 9: Robot and Tool calibration condition])` 菜单。

5. 点击 `[Explorer]` 按钮以选择位置数据文件并设置用于测量的机器人程序。

    ![](../../_assets/tp630/system-calib-robottool_eng.png)

6. 点击 `[OK]` 按钮。然后，屏幕将切换到机器人和工具校准屏幕。

7. 点击机器人和工具校准执行屏幕上的 `[Execute]` 按钮。然后，校准结果将出现。

    ![](../../_assets/tp630/system-calib-robottool-exe_eng.png)

8. 检查校准结果后，点击 `[OK]` 按钮。然后，校准结果将自动应用于轴原点和工具整数。

9. 点击 `[3: 机器人参数 - 1: 工具数据] ([3: Robot Parameter  - 1: Tool Data])` 菜单。然后，您可以检查机器人校准执行结果。

    ![](../../_assets/tp630/system-calib-robottool-toolinfo_eng.png)

<Br>

{% hint style="info" %}
选择校准参数中轴2-5（H、V、R2和B轴）的轴原点和工具长度X、Y和Z值。要仅校准工具，请在取消选择每个轴的值后执行。
{% endhint %}

<br>

#### 恢复校准数据

在执行机器人和工具校准时，校准数据作为校准.json 文件单独存储在路径 /ata0:2/lib/hi6/backup/ 中。<br>
如果由于系统初始化等操作而丢失校准数据，可以使用存储的文件恢复数据。（但是，如果通过执行串行编码器重置初始化了编码器数据，则无法恢复。）

1. 如果校准.json 文件存在于路径 /ata0:2/lib/hi6/backup/ 中，"恢复" 按钮将被激活。
2. 在执行恢复并重新启动后，将应用之前执行的机器人和工具校准数据。

![](../../_assets/tp630/robot_calib_recover.png)
[__SOURCE](7-system/7-auto-calibration/7-addaxis-autotuning.md)
# 7.7.7 额外轴自调节

* 从版本 V60.28-00 开始可用。
</br>

### A. 概述

该功能通过在用户设置的范围内移动额外轴来找到最佳增益。当额外轴没有合适的增益设置，导致噪声或控制性能差时，可以使用该功能。

| ![alt text](../../_assets/직동축.gif) | ![alt text](../../_assets/회전축.gif) |
|---|---|
| 线性轴运动 | 圆形轴运动 |
<!-- ![additional_axis](../../_assets/_7.7.7_additional_axis.jpg) -->

### B. 调节说明

![](../../_assets/_7.7.7_intro_en.png)

![c1](../../_assets/c1.png)  **调节前设置**

`额外轴 (Additional axis)`: 选择您要调节的额外轴。

`运动范围`: 设置额外轴的运动范围（线性轴：2, 5, 10[mm] / 圆形轴：2, 5, 10[deg]）。通过手动移动调整额外轴的位置，以设置合适的额外轴运动范围。较大的运动范围可以实现更好的调节（超出当前规格最大范围的运动10 mm（或10 deg）需要额外开发）。

* 起始位置：额外轴自调节开始时的起始位置。
* 结束位置：额外轴自调节开始时的结束位置。
* 当前位置信息：指示额外轴的当前位置。

**调节后的增益(Kv)**: 正在调节的参数值。

</br>

![c2](../../_assets/c2.png) **调节过程（范围测试 > 运动测试 > 运行）**

**1. 范围测试**

* 在设定的运动范围内以低速移动。如果额外轴运动范围有任何问题，请按停止按钮并重置运动范围。

**2. 运动测试**

* 在设定的运动范围内以高速移动，以检查初始调节增益值。

**3. 运行**

* 额外轴自调节过程开始。
* 调节过程中，额外轴可能会发出短暂的巨大噪音（在寻找振动增益值时）
* 调节完成后，调节参数 Kv 的增益值在调节前后将被显示。按下 `[OK]` 将弹出一个窗口询问是否应用调节后的增益。如果按下 `[enter]`，调节后的增益将被应用。如果按下 `[No]`，原始增益值将被保留。

{% hint style="warning" %}

由于数据分析噪声较为困难，调节的精度无法与调节专家手动调整时相提并论。如果需要手动调节，可以通过调整 Kv 增益来完成。
{% endhint %}

* 如果调节后的增益导致噪声，运动跟踪性能可能下降，导致较大震动。
* 反之，如果 Kv 增益过高，电机可能产生高频噪音。

如果调节后的增益导致噪声，请导航到 `[System] - 3:机器人参数 - 33:伺服参数 - 1:伺服回路增益 ([System] - 3:Robot parameter - 33:Servo parameter - 1:Servo loop gain)`，逐渐将 Kv 值调低（当 Kv 值变化时，其他增益值会自动重新计算），直到高频噪声消失。

如果噪声仍然存在，请与我们联系以获取进一步的帮助。
[__SOURCE](7-system/8-safety-system.md)
# 7.8 安全系统 

{% hint style="info" %}
此功能由 Hi7 控制器支持。
{% endhint %}

1. 触摸 `[8: 安全系统]` 菜单。然后，安全系统的菜单将出现。

2. 选择所需菜单以执行基本设置、参数设置、监控、证书或安全雷达。

![](../_assets/tp630/system-safety-menu.png)

{% hint style="info" %}
有关安全系统的 1: 基本设置、2: 参数设置、3: 监控和 4: 证书的详细信息，请参阅 "[SafeSpace2.0 手册](https://hrbook-hrc.web.app/#/view/doc-safespace2.0/zh/README)"。
{% endhint %}

{% hint style="info" %}
有关安全雷达的详细信息，请参阅 "[目标检测系统](https://github.com/hyundai-robotics/doc-Object-Detection-System)"。
{% endhint %}
[__SOURCE](7-system/9-cobot-system.md)
# 7.9 Cobot 系统

{% hint style="info" %}
此功能在 Hi7 控制器上支持。
{% endhint %}

1. 触摸 `[Cobot System]`。协作机器人系统菜单将出现。

2. 选择所需菜单以执行碰撞检测或直接教学。

![](../../_assets/tp630/system-cobot-menu.png)

{% hint style="info" %}
有关协作机器人系统的详细信息，请参阅 "[Cobot Safety Function Manual](https://hrbook-hrc.web.app/#/view/doc-cobot-safety-function/korean/README)"。
{% endhint %}
[__SOURCE](7-system/10-option-system/README.md)
# 7.10 选项系统

{% hint style="info" %}
此功能仅在 Hi7 控制器中支持。
{% endhint %}

1. 触摸 `[Option System]`。选项系统菜单出现。

2. 选择所需菜单以执行相应功能。

![](../../_assets/tp630/system-option-menu.png)
[__SOURCE](7-system/10-option-system/1-userdio-board-setting.md)
# 7.10.1 用户DIO板设置

{% hint style="info" %}
此功能支持 Hi7 控制器。
{% endhint %}

在 Hi7 控制器中，用户 DIO 板 (BD681) 和扩展 DIO 板 (BD682) 可用于处理数字输入/输出信号和输送机接口。

![](../../_assets/tp630/system-option-dio.png)

{% hint style="info" %}
有关用户 DIO 板设置的详细信息，请参阅 "[Hi7 机器人控制器功能手册 - 用户 DIO, 扩展 DIO](https://hrbook-hrc.web.app/#/view/doc-userDIO-ExtensionDIO/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/README.md)
# 8. R 代碼

當涉及到經常使用的功能的操作程序，如修改程序內容或更改控制器的設置狀態時，您可以通過指定特定的服務代碼 \(R 代碼\) 來輕鬆使用它們。

R 代碼以 "R+號碼" 格式配置，將表示重置和快速的 R 與一個數字相結合。
[__SOURCE](8-r-code/1-use-r-code.md)
# 8.1 使用 R 代码

执行指定函数的方法使用 R 代码如下。

1. 按下 `[R..[NO]]` 键盘上的键。然后，R 代码的弹出窗口将出现。

    ![](../_assets/tp630/k-r.png)

2. 在输入区域输入代码编号，然后触摸 `[OK]` 按钮或按下 `[ENTER]` 键。然后，将执行指定给选定 R 代码的函数。

    ![](../_assets/tp630/pop-rcode_eng.png)

<table style="text-align:left">
  <thead>
    <tr>
      <th>R 代码</th>
      <th>描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>R0 : 重置任务</td>
      <td>初始化步数计数器并移动到 STEP0。</td>
    </tr>
    <tr>
      <td>R1 : 重置错误</td>
      <td>当发生错误或警告时清除状态。</td>
    </tr>
    <tr>
      <td>R17 : 打开文件管理器</td>
      <td>快速启动 [服务] -> [5: 文件管理器]</td>
    </tr>
    <tr>
      <td>R86 : 显示剩余内存</td>
      <td>用于在 T/P 屏幕顶部显示 T/P 或主板的剩余内存。</td>
    </tr>
    <tr>
      <td>R99 : 保存</td>
      <td>将存在于内存中的历史数据保存为文件。</td>
    </tr>
    <tr>
      <td>R115 : 复制作业文件</td>
      <td>将创建的作业程序复制到另一个作业程序。</td>
    </tr>
    <tr>
      <td>R117 : 删除作业文件</td>
      <td>这是单独删除已编写作业的功能。</td>
    </tr>
    <tr>
      <td>R286 : 显示软件版本</td>
      <td>快速启动 [服务] -> [7: 系统诊断] -> [1: 系统版本]</td>
    </tr>
    <tr>
      <td>R321 : 轴同步操控设置</td>
      <td>显示设置屏幕，以将任意轴分组为一个同步组，并使用单个操控键进行操控。</td>
    </tr>
    <tr>
      <td>R360 : 手动设置 contpath</td>
      <td>这是强制更改 CONTPATH 执行状态的功能。</td>
    </tr>
    <tr>
      <td>R361 : 设置 jog-微调级别</td>
      <td>当您要更改当前设定级别的微调距离时使用此功能。</td>
    </tr>
    <tr>
      <td>R362 : 轴控制状态改变</td>
      <td>手动执行辅助轴的控制状态（轴控制开/关）。</td>
    </tr>
  </tbody>
</table>
[__SOURCE](8-r-code/2-r0.md)
# 8.2 R0 用于重置步进计数器

在收藏夹窗口中输入 0 后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

![](../_assets/tp630/pop-rcode_eng.png)

您可以初始化步进计数器以移动到 STEP0。您还可以执行以下功能。

* 清除播放执行状态
* 关闭整体异常信号和指示灯
* 关闭警报信号
* 清除等待状态
* 清除各种应用功能的状态和信号



{% hint style="info" %}
R0 代码在机器人启动期间无法使用。
{% endhint %}
[__SOURCE](8-r-code/3-r115.md)
# 8.3 R115 复制程序

您可以将主板上的 JOB 程序复制到主板上的另一个程序。输入您想要复制的程序的编号后，输入您想要将复制的程序复制到的程序编号。

1. 输入 115 在收藏夹窗口中，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

2. 输入您想要复制的程序 \(original\) 的编号以及您想要将复制的程序复制到的程序 \(target\) 的编号，触摸 `[OK]` 按钮或按 `[ENTER]` 键。然后，程序将被复制。

    ![](../_assets/tp630/pop-rcode-115_end.png)

* 如果要复制的目标程序已经存在相同编号的程序，您应该选择是否覆盖文件。
* 
  如果没有可复制的原始文件，将出现通知消息 \("没有原始文件存在."\)。



{% hint style="info" %}
代码 R115 在程序运行时无法使用；它必须在程序停止时使用。
{% endhint %}
[__SOURCE](8-r-code/4-r117.md)
# 8.4 R117 删除程序

您可以单独删除内部存储器中的程序。

1. 在收藏夹窗口输入117后，触摸`[OK]`按钮或按`[ENTER]`键。

2. 输入您想要删除的程序编号后，触摸`[OK]`按钮或按`[ENTER]`键。然后，删除确认窗口将出现。

    ![](../_assets/tp630/pop-rcode-117_eng.png)

* 如果没有文件可以删除，将出现通知消息（"没有文件存在。"）。
* 如果您想删除被保护的程序，将出现通知消息（"受保护的文件。"）。

3. 在删除确认窗口中，触摸`[OK]`按钮或按`[ENTER]`键。然后，选定的程序将被删除。

{% hint style="info" %}
R117代码无法在自动模式下使用。必须在手动模式下使用。
{% endhint %}
[__SOURCE](8-r-code/5-r210.md)
# 8.5 R210 选择点焊枪编号

在使用多个点焊枪（伺服枪或气动枪）时，您可以选择要使用的点焊枪。

1. 在收藏窗口中输入210后，触摸`[OK]`按钮或按`[ENTER]`键。

2. 输入要使用的点焊枪编号后，触摸`[OK]`按钮或按`[ENTER]`键。

    ![](../_assets/tp630/pop-rcode-210_eng.png)

* 选定的点焊枪编号将在${cont_model}示教器屏幕的右下角显示。
* 如果更改点焊枪编号，则相应的工具编号将自动更改。您可以在`[system - 4: Application Parameter - 1: Spot Welding - 2:Welding gun parameter] ([system  - 4: Application Parameter  - 1: Spot Welding  - 2:Welding gun parameter])`菜单中检查相应的点焊枪工具编号。



{% hint style="info" %}
* R210代码在机器人启动期间无法使用。
* 只有在点焊环境中才能设置点焊枪编号（`[system - 5: 初始化 - 3: Usage Setting] ([system  - 5: Initialize - 3: Usage Setting])`菜单中的`[Spot Welding]`项设置为启用）。
* 您可以手动打开、关闭和挤压选定的点焊枪。有关点焊功能的详细信息，请参阅"${cont_model} Controller Spot Welding Function Manual."
{% endhint %}
[__SOURCE](8-r-code/6-r211.md)
# 8.6 R211 用于设置伺服枪夹紧力

您可以在执行伺服枪夹紧时手动设置夹紧力。

1. 在收藏夹窗口输入211后，触摸`[OK]`按钮或按`[ENTER]`键。

2. 输入夹紧力后，触摸`[OK]`按钮或按`[ENTER]`键。

    ![](../_assets/tp630/pop-rcode-211_eng.png)



* 焊接条件文件中的夹紧力不会被更改。
* 如果输入的夹紧力大于或小于伺服枪参数的电流/压力表的上限，将显示警告信息。



{% hint style="info" %}
* R211代码在机器人启动期间无法使用。 
* 
  仅在点焊环境中可以设置点焊枪编号 \(`[Spot Welding]`项目在`[system - 5: 初始化 - 3: Usage Setting] ([system  - 5: Initialize - 3: Usage Setting])`菜单中设置为启用\)。 

* 有关伺服枪夹紧力的手动设置的详细信息，请参阅"[${cont_model} Controller Spot Welding Function Manual](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/7-r212.md)
# 8.7 R212 用于预置伺服枪移动电极磨损量

您可以手动设置伺服枪移动电极磨损量。

1. 在收藏夹窗口中输入 212 后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

2. 输入移动电极磨损量后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

    ![](../_assets/tp630/pop-rcode-212_eng.png)

{% hint style="warning" %}
请注意，如果设置的值大于或小于电极的实际磨损量，可能会导致挤压力不匹配或与工件干扰。
{% endhint %}

{% hint style="info" %}
* R212 代码在机器人启动时无法使用。
* 点焊编号只能在点焊环境中设置 \(`[Spot Welding]` 项在 `[system - 5: 初始化 - 3: Usage Setting] ([system  - 5: Initialize - 3: Usage Setting])` 菜单中设置为启用\)。
* 有关伺服枪移动电极磨损量的手动设置的详细信息，请参阅 "[${cont_model} Controller Spot Welding Function Manual](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/8-r213.md)
# 8.8 R213 用于预设伺服枪固定电极磨损量

您可以手动设置伺服枪固定电极磨损量。

1. 在收藏窗口中输入213后，触摸`[OK]`按钮或按`[ENTER]`键。

2. 输入固定电极磨损量后，触摸`[OK]`按钮或按`[ENTER]`键。

    ![](../_assets/tp630/pop-rcode-213_eng.png)

{% hint style="warning" %}
请注意，如果设置的值大于或小于电极的实际磨损量，可能会导致夹紧力不匹配或与工件干涉。
{% endhint %}

{% hint style="info" %}
* R213代码在机器人启动期间无法使用。
* 点焊枪编号仅可在点焊环境中设置 \(`[Spot Welding]` 项在 `[system - 5: 初始化 - 3: Usage Setting] ([system  - 5: Initialize - 3: Usage Setting])` 菜单中设置为启用\)。
* 有关伺服枪固定电极磨损量的手动设置的详细信息，请参阅 "[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/9-r214.md)
# 8.9 R214 同时选择焊接枪

您可以选择在焊接操作中将同时使用的点焊枪（伺服枪或气动枪）的数量。

1. 在收藏夹窗口输入 214 后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

2. 输入要同时使用的焊接枪的数量后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

    ![](../_assets/tp630/pop-rcode-214_eng.png)

* 所选的点枪号码会显示在 ${cont_model} 教学挂件屏幕的右下角。
* 如果您选择的点焊枪类型不同，将出现通知消息（“当前选择的枪的类型设置不正确。”）。

<Br>

{% hint style="info" %}
* R214 代码在机器人启动期间不能使用。
* 点枪号码只能在点焊环境中设置（`[Spot Welding]` 项在 `[system - 5: 初始化 - 3: Usage Setting] ([system  - 5: Initialize  - 3: Usage Setting])` 菜单中设置为启用）。
* 您可以在 `[system - 4: Application Parameter - 1: Spot Welding - 2:Welding gun parameter] ([system  - 4: Application Parameter  - 1: Spot Welding  - 2:Welding gun parameter])` 菜单中检查点焊枪的设置状态。
  * 当枪被选为多同步枪时，所选择枪的手动挤压/打开/关闭操作将与之前选择的枪同步进行。
  * 当枪被选为多同步枪时，如果枪 LED 处于打开状态，SPOT 命令将以同步点格式记录。
* 所选的点焊枪可以手动操作。有关点焊功能的详细信息，请参考 "[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/10-r215.md)
# 8.10 R215用于设置点焊条件下的挤压力

您可以在焊接条件表中设置伺服枪焊接所需的挤压力。您还可以在`系统 - 4: 应用参数 - 1: 点焊 - 4: 焊接数据 (条件, 顺序) - 2: 焊接条件 (系统 - 4: 应用参数 - 1: 点焊 - 4: 焊接数据 (条件, 顺序) - 2: 焊接条件)`菜单中设置挤压力。

1. 在收藏夹窗口中输入215后，触摸`[OK]`按钮或按`[ENTER]`键。

2. 输入焊接条件编号后，触摸`[OK]`按钮或按`[ENTER]`键。

    ![](../_assets/tp630/pop-rcode-215-1_eng.png)

3. 输入伺服枪挤压力后，触摸`[OK]`按钮或按`[ENTER]`键。

    ![](../_assets/tp630/pop-rcode-215-2_eng.png)
[__SOURCE](8-r-code/11-r220.md)
# 8.11 R220 设定面板厚度 \(Sv\)

您可以手动设定面板厚度，以记录伺服枪点焊步骤。

如果您执行一键记录，其中 MOVE 和 SPOT 指令在伺服枪固定电极仅与面板接触的状态下同时被记录，则移动电极的位置将根据面板厚度和磨损量自动记录在 MOVE 指令中。

1. 在收藏窗口输入 220 后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

2. 在输入面板厚度后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

    ![](../_assets/tp630/pop-rcode-220_eng.png)



{% hint style="info" %}
有关面板厚度手动设置的详细信息，请参阅 "[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/12-r314.md)
# 8.12 R314 工程师模式

在 R 代码窗口中，输入 314，然后触摸 `[OK]` 按钮或按 `[ENTER]` 键。

![](../_assets/tp630/pop-rcode-314.png)

完成后，屏幕右上角会闪烁以下显示。

![](../_assets/tp630/eng-mode.png)

在工程师模式中可以设置以下功能。

* 轴原点（机器人参数） 
* 软限制（机器人参数） 
* 编码器偏移（机器人参数） 
* 伺服参数（机器人参数） 
* 加速和减速参数（机器人参数） 
* 伺服工具更换（应用参数） 
* 系统初始化（初始化）
* 机器人类型选择（初始化）
* 额外轴参数（初始化）
* 轴锁定（初始化）
* 其他详细应用

{% hint style="warning" %}

* 请注意，工程师模式下的错误设置可能会导致机器人系统严重问题。{% endhint %}
[__SOURCE](8-r-code/13-r358.md)
# 8.13 R358 更改伺服工具

您可以手动连接和断开伺服工具在伺服工具更换系统中。

要在伺服工具更换系统中更换伺服工具，您需要使用物理自动工具更换 \(ATC\) 设备断开或连接电源和各种信号线。

当伺服工具是伺服枪时，如果您想手动进行更换工作，您需要在电机开启的情况下移动机器人到可以连接或断开机器人的伺服枪支撑桌，然后进行更换工作。如果伺服工具是其他类型，例如定位器，您可以在连接和断开工作准备完成后进行更换工作。

R358 伺服工具更换参数及示例如下。

![](../_assets/image_546.png)

使用 R358 代码更换伺服工具的方法如下。

1. 在收藏夹窗口输入358后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

2. 输入更换操作编号 \(0: 断开, 1: 连接, 2: 固定\) 后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

    ![](../_assets/tp630/pop-rcode-358-1_eng.png)

3. 输入要更换的焊接枪编号后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。所选的焊接枪编号将在 ${cont_model} 教导挂架屏幕的右下角显示。

    ![](../_assets/tp630/pop-rcode-358-2_eng.png)

{% hint style="info" %}
* R358 代码不能在自动模式下使用。必须在手动模式下使用。
* 
  当点焊枪编号更改时，对应点焊枪指定的工具编号将自动更改。您可以在 `[system - 4: Application Parameter - 1: Spot Welding - 2:Welding gun parameter] ([system  - 4: Application Parameter  - 1: Spot Welding  - 2:Welding gun parameter])` 菜单中查看对应点焊枪的工具编号。

* 
  伺服工具更换设置只能在电机开启时进行。

* 有关伺服工具更换的详细信息，请参阅 "[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/14-r359.md)
# 8.14 R359 伺服工具编码器电源开启继电器

如果伺服枪应用于伺服工具更换系统，则需要在第一次安装伺服工具时执行此功能以重置伺服工具轴的编码器。

1.	在收藏夹窗口输入359后，触摸`[OK]`按钮或按下`[ENTER]`键。

2.	在输入1后，触摸`[OK]`按钮或按下`[ENTER]`键。然后，电源将供应给编码器。

    ![](../_assets/tp630/pop-rcode-359_eng.png)



{% hint style="info" %}
* R359代码不能在自动模式下使用。必须在手动模式下使用。
* 
  要禁用对伺服枪编码器的强制供电，您应该关闭控制器的电源，然后再重新开启。因此，当编码器重置完成后，请关闭控制器的电源并重新开启，然后进行手动连接。

* 伺服工具编码器电源设置功能是为工程师设计的，因此不支持一般用户。有关该功能的更多信息，请与我们的工程师联系。
* 有关伺服工具编码器电源设置的详细信息，请参阅"[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}

{% hint style="warning" %}
在强制供电的情况下，绝不要机械连接或断开伺服枪。
{% endhint %}
[__SOURCE](8-r-code/15-r360.md)
# 8.15 R360 手动设置 CONTPATH

它手动更改 CONTPATH（连续路径）模式。输入范围为 0、1 和 2，每个数字的描述如下。（与 [contpath](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/5-moving-robot/6-contpath) 语句相同。）

<table>
  <thead>
    <tr>
      <th style="text-align:left">数字</th>
		<th style="text-align:left">含义</th>
      <th style="text-align:left">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
		<td>不连续</td>
      <td style="text-align:left">
        如果步骤包含功能，当达到步骤位置时，机器人暂停，执行功能，然后移动到下一个步骤。
      </td>
	 </tr>
	 <tr>
		<td>1</td>
		<td>连续。<br>但是，输入信号是不连续的（默认）</td>
      <td style="text-align:left">
        在步骤移动期间，当机器人移动时，目标步骤中的功能被执行，然后通过目标步骤移动到下一个步骤。<br>
		但是，在输出功能的情况下，实际输出点在命令值达到精度范围内时输出。<br>
		此外，如果输入信号用于命令的参数，当机器人暂停时，执行功能，然后移动到下一个步骤。
      </td>
	 </tr>
	 <tr>
		<td>2</td>
		<td>连续。<br>输入信号也是连续的</td>
      <td style="text-align:left">
        即使命令包含输入信号，它也会提前解释并连续移动。
      </td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

<br>
<br>

{% hint style="info" %}

- 输入信号 : fb.di

- 输出信号 : fb.do, _s, _m, _mo,

- 其他不连续条件
  1) 不连续操作：在不连续条件下的前进步骤，后退步骤，逐步回放
  2) GUN1 或 GUN2 步骤。
  3) 如果 accu=0 且值为 0
  4) 如果工具编号发生变化

{% endhint %}

操作方式如下：

1. 按下 R 按钮，输入 360，触摸 `[OK]` 按钮，或按 <b>ENTER</b> 键。

2. 输入连续通行证号（0~2），触摸 `[OK]` 按钮，或按 <b>ENTER</b> 键。

![](../_assets/tp630/pop-rcode-360.png)

3. 可以通过标题栏中的 `CP0`、`CP1` 或 `CP2` 标志检查已更改的模式。

![](../_assets/tp630/flag-cp.png)
[__SOURCE](8-r-code/16-r361.md)
# 8.16 R361 设置 Jog 进给级别

R361 jog 进给级别设置信息如下。

![](../_assets/image_538.png)

更改当前设置级别的进给距离的方法如下。

1. 在收藏窗口中输入 361 后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

2. 输入 jog 进给级别的单位 \(0: 距离. 1: 角度\)，然后触摸 `[OK]` 按钮或按 `[ENTER]` 键。

    ![](../_assets/tp630/pop-rcode-361-1_eng.png)

3. 如果输入 '1'，请输入进给角度，然后触摸 `[OK]` 按钮或按 `[ENTER]` 键。

    ![](../_assets/tp630/pop-rcode-361-2_eng.png)

{% hint style="info" %}
* R361 代码不能在自动模式下使用。必须在手动模式下使用。
* 使用 R361 代码设置的进给距离将用于当前设置的 jog 级别。因此，如果当前 jog 速度级别为 8，则将更改与 8 对应的进给距离。
* 仅当激活 jog 进给键 \(LED 开\) 时，才能进行 jog 进给。
{% endhint %}
[__SOURCE](8-r-code/17-r321.md)
# 8.17 R321 轴同步 jog 设置

这是一个将任意轴分组到一个同步组并用单个 jog 按键进行 jog 的功能。

![](../_assets/tp630/init-axis-sync-jog.png)

使用轴同步 jog 功能的方法如下。

1. 将您希望通过一个按键移动的轴设置到同一同步组，然后按下 `[OK]` 按钮。
2. 使用 jog 按键进行轴同步 jog。
3. 当您完成使用轴同步 jog 功能时，将所有同步组设置为无效。

{% hint style="info" %}
* 此功能仅在 jog 时有效。同步功能不适用于自动模式。
* 同步 jog 配对在重启时不会初始化。
* 同步 jog 配对在笛卡尔坐标系中的姿态值与实际机器人的姿态情况不匹配（简单 jog 功能）。
{% endhint %}
[__SOURCE](9-property/README.md)
# 9. 属性

当为焊接操作教学作业程序时，除了电压和电流等焊接条件外，还应设置弧焊特定细节，例如摆动、重试/重新启动和焊工的特性。此外，有时还应检查步进或辅助点的位置。
[__SOURCE](9-property/1-use-property.md)
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
[__SOURCE](9-property/2-move-step-position/README.md)
# 9.2 移动步骤位置

您可以检查或修改当前选定行中 JOB 程序的步骤位置。
[__SOURCE](9-property/2-move-step-position/1-hidden-pose-move.md)
# 9.2.1 隐藏位姿移动语句

您可以检查或修改当前步骤在隐藏位姿移动语句中的位置 \(由 `[REC]` 键记录的步骤，即不包括位姿变量的移动语句\)。

1.	触摸作为隐藏位姿记录的移动命令 \(移动语句\) 中的 `[property]` 按钮。然后，当前步骤位置将显示。

2.	检查并修改当前步骤位置。

    ![](../../_assets/tp630/step-info_eng.png)



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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>当前步骤的位置信息。您可以检查并设置名称、坐标值和坐标系统格式等。</p>
        <ul>
          <li><b>[名称]</b>: 当前步骤的编号。输入步骤编号后，按 <b>`[ENTER]` </b>键移动到相关步骤。</li>
          <li><b>坐标值</b>: 当前步骤的当前坐标值
            <ul>
              <li>使用光标键选择项目。</li>
              <li>在所需项目中输入值后，按 `[ENTER]` 键以反映该更改。</li>
              <li>如果坐标系统格式设置为编码器，则坐标值将不会更改。</li>
            </ul>
          </li>
          <li><b>[坐标系]</b>: 表达当前步骤位置的坐标系统格式</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>`[OK]`: 您可以保存更改。</li>
          <li><b>[上一页]/[下一页]</b>: 您可以显示上一个或下一个步骤的信息。</li>
          <li><b>[原始值]</b>: 您可以显示当前步骤的原始隐藏位姿值。</li>
          <li><b>[当前机器人位姿]</b>: 您可以显示机器人当前采取的姿态值。</li>
          <li><b>[移动]</b>: 触摸该按钮将使机器人移动到记录的步骤位置 (Jog)。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

3.	触摸 `[OK]` 按钮。然后，更改将保存在作业程序中，操作将结束。 

* 如果您通过按 `[ESC]` 键结束操作，更改将不会被保存。 

{% hint style="info" %}
* 如果 `[Robot Configuration]` 设置为未指定，机器人将指定最接近当前机器人位置的配置。
* 
  关于机器人配置的指定，请参考 "[2.3.2.2 基座和机器人记录坐标](../../2-operation/3-step/2-step-pose-modify/2-base-robot-crd-sys.md)"。
{% endhint %}
[__SOURCE](9-property/2-move-step-position/2-pose-rec-move.md)
# 9.2.2 姿态记录移动语句和姿态赋值语句

您可以编辑移动语句中的姿态变量值，包括姿态变量或姿态变量赋值语句。

1. 触摸记录为姿态变量的移动命令 \(移动语句\) 中的 `[property]` 按钮。然后，姿态变量设置屏幕将会出现。

2. 检查并修改当前姿态变量。

    ![](../../_assets/tp630/step-pose-global_eng.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>当前姿态变量信息。您可以检查并设置名称、坐标值、坐标系统格式等。</p>
        <ul>
          <li><b>[名称]</b>: 当前姿态变量的名称</li>
          <li><b>坐标值</b>: 当前姿态变量的坐标值
            <ul>
              <li>使用光标键选择项目。</li>
              <li>在所需项目中输入值后，按 <b>`[ENTER]`</b> 键以反映更改。</li>
              <li>如果坐标系统格式设置为编码器，坐标值将不会更改。</li>
            </ul>
          </li>
          <li><b>[坐标系统]</b>: 表达当前姿态变量位置的坐标系统格式</li>
          <li><b>[配置]</b>: 描述机器人位置时，由于设备特性存在多种解决方案，因此机器人配置被指定为唯一描述配置。
            <ul>
              <li>此功能仅在坐标系统类型设置为基座或机器人时可用。</li>
              <li>有关机器人配置的详细信息，请参阅 “<a href="../../operation/step/step-pose-modify/">2.3.2 记录和改变一步位置</a><b>.</b> ”</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>`[确定]`: 您可以保存更改。</li>
          <li><b>[上一步]/[下一步]</b>: 您可以显示上一或下一步骤的信息。</li>
          <li><b>[原始值]</b>: 您可以显示当前步骤的原始隐藏姿态值。</li>
          <li><b>[当前机器人姿态]</b>: 您可以显示机器人当前所处的姿态值。</li>
          <li><b>[移动]</b>: 触摸按钮将使机器人移动到记录的步骤位置（Jog）。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

3. 触摸 `[确定]` 按钮。然后，更改将被保存到作业程序中，操作将结束。

* 如果您通过按 `[ESC]` 键结束操作，更改将不会被保存。
[__SOURCE](9-property/3-spot-welding-func.md)
# 9.3 点焊功能

在编写程序时，如果在手动模式下将光标放置在点焊功能位置并触摸 `[property]` 按钮，则在应用参数设置菜单屏幕中，`[1: 点焊]` 菜单将被高亮显示。使用点焊功能，您可以快速修改焊接条件的内容以及进行点焊时的焊接顺序。

![Figure 76 Spot Welding Function](../_assets/tp630/app-spot-menu_eng.png)

{% hint style="info" %}
* 您可以通过触摸 `[system]` 按钮 - `[4: 应用参数 - 1: 点焊] ([4: Application Parameter  - 1: Spot Welding])` 来使用点焊功能。
* 
  有关点焊功能的详细信息，请参阅 "[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](10-robot-language.md)
# 10. 机器人语言

有关机器人语言的详细信息，请参阅 "[${cont_model} 机器人控制器功能手册. - 机器人语言 HRScript](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/README?cont_model=${cont_model})"
[__SOURCE](11-etc/README.md)
# 11. 其他

本章解释了之前未涵盖的其他信息。
[__SOURCE](11-etc/1-controller-files/README.md)
# 11.1 机器人控制器中的主要文件夹和文件

各种配置、教学和日志文件存储在机器人控制器内部。
在本节中，我们将描述文件夹结构和各个文件的角色。
[__SOURCE](11-etc/1-controller-files/1-caution-ftp.md)
# 11.1.1 通过 FTP 加载到 project/ 文件夹时的注意事项

{% hint style="warning" %}
`[警告]` TP 文件管理器或 FTP 服务允许您修改文件夹和文件。
然而，粗心的修改或删除文件可能会导致严重的问题，例如启动失败、故障或数据丢失。
除非您完全了解它们的机制或在合格专家的指导下工作，否则请勿修改这些文件。
{% endhint %}

您可以使用 HRWorkbench、文件管理器或备份功能在项目文件夹中备份和恢复配置和教学文件。

然而，在某些情况下，使用熟悉的 FTP 软件将文件备份到 PC 或将它们恢复到机器人控制器可能更方便。
本节描述进行此操作时需要注意的重要事项。
(项目文件夹中每个文件的详细信息将在下一节中解释。)

#### 在 project/jobs/ 文件夹中修改 .job 文件后应用更改

当您使用 FTP 软件在 `project/jobs/` 文件夹中添加或覆盖 .job 文件时，机器人控制器不会立即在内存中反映这些更改。
(使用 HRWorkbench 或文件管理器时，变化会被即时检测并自动加载到内存中。)

有两种方法将更新的文件应用于内存：

- 在 HOME 屏幕上，点击控制台栏上的 ` (...)` 按钮，然后选择 `重新加载更新的作业 (reload updated jobs)`。

  ![](../../_assets/tp630/etc/console_reload_job.png)

- 重新启动机器人控制器。

#### 在 project/vars/ 文件夹中修改 .json 和 .csv 文件后应用更改

当您使用 FTP 软件在 `project/vars/` 文件夹中添加或覆盖全局变量文件时，机器人控制器不会立即在内存中反映这些更改。
(使用 HRWorkbench 或文件管理器时，变化会被即时检测并自动加载到内存中。)

要将更新的文件应用于内存，请使用以下方法：

- 打开全局变量监控窗口，然后点击底部的 `Load All` (F-button)。

![](../../_assets/tp630/etc/gvar_load.png)

{% hint style="warning" %}
请勿重启机器人控制器以应用更新的全局变量文件。
当控制器断电时，当前内存中的全局变量值将被保存回文件中，这将覆盖您刚刚更新的文件。
{% endhint %}
[__SOURCE](11-etc/1-controller-files/2-project.md)
# 11.1.2 project/

这是存储机器人配置、教学数据和状态的最重要文件夹。
在备份或恢复控制器系统时，此文件夹是核心组件。

#### project/

此文件夹包含各种配置文件以及在控制器关闭前立即保存的状态备份文件。
状态备份包括在关机时为以下目的存储的信息：

    - 在控制器再次启动时恢复关机前正在运行的任务
      （注意：对于复杂操作，例如机器人应用程序或插件，可能无法恢复。）

    - 保留关机前的输出信号并在开机后恢复


* arc_weld.json
  
  弧焊应用配置文件

* arc_weld_bkup.json
  
  在关机前保存的弧焊应用状态的备份数据

* calibration.json

  机器人校准配置文件

* context.json

  所有任务的 .job 文件的执行上下文，包括指令指针位置、带参数的 .job 文件调用历史、局部变量值等。

* dout.json

  在关机前保存的一般数字信号的输出状态

* force_control.json

  力控制配置文件

* hi6_proj.json

  主项目文件。大部分基础特性的配置存储在这里。

* kw.json
  
  在关机前保存的内置 PLC `kw` 继电器值

* maintenance.json

  各种维护和系统信息，包括机器人型号、轴数、运行时间、软件版本、剩余内存和存储、系统代码以及每线程执行时间

* motion_bkup.bin
  
  与机器人运动相关的在关机前保存的备份数据

* mw.json
  
  在关机前保存的内置 PLC `mw` 继电器值

* playback_bkup.bin

  在关机前保存的与 .job 执行相关的备份数据

* sealing.json

  密封应用配置文件

* sout.json

  在关机前保存的系统信号输出值

* spot_weld.json

  点焊应用配置文件

* spot_weld_bkup.json

  在关机前保存的点焊应用状态的备份数据

* svtool_change.json

  额外轴配置文件，用于伺服工具更换操作

* version.json

  用于确定软件版本升级后第一次启动时是否需要数据更新的信息（当前版本号）
  

#### project/jobs/
  
存储教学程序 (.job 文件) 的文件夹。


#### project/lads/
  
存储内置 PLC 梯形图程序 (.lad 文件) 的文件夹。


#### project/safety/
  
（HI7 控制器）存储功能安全配置文件的文件夹。

* safety_parameter.json

  功能安全配置文件

* safety_parameter.json.cert

  功能安全配置的认证文件。
  只有在以正确的密码保存配置时才会发放有效证书。如果无效，控制器将无法操作。


#### project/vars/

存储变量和别名的文件夹。

* aliases.json

  机器人语言别名文件

* *.csv

  顶层数组文件（逗号分隔值格式）

* vars.json

  全局变量文件
[__SOURCE](11-etc/1-controller-files/3-log.md)
# 11.1.3 log/


该文件夹存储各种日志文件。在下面的文件名中，? 表示一个数字；当达到最大数字时，文件会以循环方式从 0 开始覆盖，或者它可能表示格式为 YYYYMMDD_HHMMSS 的时间戳。

这些文件中：

事件日志可以在教导挂件日志窗口中查看或通过 HRWorkbench 查看。

范围日志只能通过 HRWorkbench 查看。

其余 .txt 文件可以用任何标准文本编辑器打开。


* bootlog_?.txt

  存储控制器启动历史的日志文件。  
  用于分析如启动失败等问题。每次控制器启动时，都会循环创建一个新文件。

* evlog_alarm_??.txt

  存储错误和警告事件的日志文件。

* evlog_hist_??.txt

  存储历史事件的日志文件。  
  主要记录 .job 文件的执行历史。

* evlog_io_??.txt

  存储 I/O 转换事件的日志文件。

* evlog_noti_??.txt

  存储通知事件的日志文件。

* evlog_oper_00.txt

  存储用户操作事件的日志文件。

* evlog_stst_00.txt

  存储机器人的启动和停止事件的日志文件。

* pow_stage.txt

  存储开机、断电恢复和断电备份状态的文件。

* sclog_base_????????_??????.bin

  存储各轴位置、速度和加速度等时间序列数据的范围日志文件。  
  ????????_?????? 表示 YYYYMMDD_HHMMSS 格式的时间戳。  
  当检测到机器人冲击或发生特定错误时生成。可以通过 HRWorkbench 的范围日志功能查看。

* sclog_base_????????_??????.json

  描述存储在对应 .bin 文件中数据类型的模式文件。  
  打开日志时，.bin 和 .json 文件必须成对存在。

* shutdownlog_?.txt

  存储控制器关机历史的日志文件。  
  用于分析断电备份操作是否正确执行。每次控制器关机时，都会循环创建一个新文件。

* updatesvclog_?.txt

  存储控制器软件版本升级历史的日志文件。  
  用于分析版本升级是否成功。
[__SOURCE](11-etc/1-controller-files/4-backup.md)
# 11.1.4 backup/

此文件夹存储控制器的MAIN侧备份。  
文件夹名称按格式 `bYYYYMMDD_HHMM` 生成，包含子文件夹：project/，log/，cifX/，EC_LOG/ 和 EDR_LOG/。


#### backup/ev/

存储事件备份的文件夹。  
当发生特定错误时，备份会自动创建。


#### backup/ts/

存储定期备份的文件夹。  
备份会在预定时间自动创建。
[__SOURCE](11-etc/1-controller-files/5-etc.md)
# 11.1.5 其他文件夹

#### apps/

安装和存储在 MAIN 端执行的插件应用的文件夹。


#### fbrr/

基于文件的机器人注册表文件夹。  
存储每个机器人机制模型的信息文件 (.fbr)。  
当添加一个新的模型信息文件时，可以在系统初始化期间通过选择模型来配置机器人系统。


#### gather/

存储时间序列数据收集功能结果文件 (.GDT) 的文件夹。


#### help/

存储机器人语言 HRScript 的 HTML 帮助文件的文件夹。


#### roblang/

存储机器人语言 HRScript 语法文件的文件夹。

* procs_?.json
  
  按类别划分的过程语法文件

* funcs_?.json

  按类别划分的函数语法文件

* svars_?.json
  
  按类别划分的系统变量语法文件
[__SOURCE](appendices/README.md)
# 附录
[__SOURCE](appendices/rules-occupational-safety.md)
# 职业安全与健康标准的规则，以及安全检查通知

工业机器人应在考虑《职业安全与健康标准的规则》和《安全检查通知》的检查标准下安装（如需检查）。

"[职业安全与健康标准的规则](https://hrbook-hrc.web.app/#/view/rules-on-occupational-safety-and-health-standards/zh/README)"
[__SOURCE](quality-assurance.md)
# 质量保证

"[质量保证](https://hrbook-hrc.web.app/#/view/quality-assurance/zh/README)"