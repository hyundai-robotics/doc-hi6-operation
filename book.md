
[__SOURCE](README.md)
# ${cont_model} 控制器操作手册 - TP630
[__SOURCE](0-about-this-manual/README.md)
# 关于手册

本手册描述了HD Hyundai Robotics的${cont_model}控制器的基础知识和结构，以及工业机器人的常见操作。每一章不仅描述了基本操作方法，还介绍了使用各种应用功能的方法。

本手册不涵盖详细的应用功能，如使用协作机器人进行直接教学、安全功能设置方法、点焊、弧焊、定位器同步功能和传感器同步功能的相关信息。如需详细信息，请参阅协作机器人维护手册和各个应用功能手册。
[__SOURCE](0-about-this-manual/precautions.md)
# 注意事项

{% include file="zh/precautions.md" %}
[__SOURCE](0-about-this-manual/notation.md)
# 记号约定

在本手册中，使用以下记号约定和安全说明来帮助您理解内容。

### 图形描述

使用图形帮助您理解如何操作产品，并说明您在屏幕上可以看到的内容。图形的描述中，将为相关部分标记数字，并按照如下描述相应内容。

![](../_assets/tp630/pane-prog-cmd-param.png)

### 图形用户界面 \(GUI\)

在GUI中，菜单名称和按钮名称用方括号括起来，并以浅色背景显示。
当必须依次选择多个菜单时，它们的名称用连字符 (-) 分隔。

* 单个菜单：在手动或自动模式的初始屏幕上，触摸`[F1: 服务] ([F1: Service])`W按钮。
* 多个菜单：在手动模式的初始屏幕上，触摸`[F2: 系统] - 5: 初始化 - 6: 机制设置 ([F2: System] - 5: Initialization - 6: Mechanism setting)`。

### 操作键的记号方法

需要在教导挂件的操作部分按下以操作功能的键将用方括号括起来，并以浅色背景显示。

* 如果按下`[Start]`键，机器人中创建的程序的自动操作将开始。

### 交叉引用 

它提供了指向手册中相关信息的快捷方式。交叉引用将以双引号显示（“ ”），如下所示。

* 有关如何更改日期和时间信息的详细信息，请参阅“[4.5 设置日期和时间。](../4-service/5-date-time-setting.md)”。

### 注意

本节包含一些在使用产品时可能有用的提示或附加信息，如下所示。

{% hint style="info" %}
当状态栏中的![](../_assets/eng-mode.png)图标闪烁时，意味着您处于工程师模式。
{% endhint %}
[__SOURCE](0-about-this-manual/safety-notice.md)
# 安全警告

{% include file="zh/safety-notice.md" %}
[__SOURCE](1-robot-system/README.md)
# 1. 机器人系统
[__SOURCE](1-robot-system/1-basic-constitution/README.md)
# 1.1 基本配置

工业机器人是“配备了基于自动控制的操作和移动功能的机器，以便它们能够在工业场所通过使用程序执行各种工作。” 协作机器人是工业机器人的一种类型。

机器人系统由操纵器和控制器组成，控制器控制操纵器。用于设定和手动操作机器人系统的示教器连接到控制器上。

* 机器人：在工业现场执行各种工作，如运输物体、组装零件等。
* 控制器：根据通过示教器设定的程序设置值调整机器人的操作。可以通过控制器的输入/输出端口与各种外部设备或装置进行互操作。
* 示教器：管理整个机器人系统的设备。它使您能够教机器人特定的姿态或设置并控制程序。

以下展示了根据机器人类型的机器人系统基本配置示例。

![Figure 1 Basic Configuration of the LCD Robot System](../../_assets/image_286.png)

![Figure 2 Basic Configuration of the Vertical Articulated Robot System ](../../_assets/image_285.png)
[__SOURCE](1-robot-system/1-basic-constitution/1-controller.md)
# 1.1.1 控制器

#### 垂直关节机器人控制器 

![图 4 控制器的前面 \(左\) / 后面 \(右\)](../../_assets/image_33.png)

| No. | 名称 | 描述 |
| :--- | :--- | :--- |
| ![](../../_assets/c1.png)  | 连接部分 | 连接仪器和教学挂件到控制器的通道，或连接应用设备到内部模块 |
| ![](../../_assets/c2.png)  | 电源开关 | 打开或关闭控制器的电源 |
| ![](../../_assets/c3.png)  | 存储TP的钩子 | 用于悬挂教学挂件或存放它 |
| ![](../../_assets/c4.png)  | 紧急停止开关 | 在紧急情况下按下后使机器人停止操作 |
| ![](../../_assets/c5.png)  | 冷却风扇 | 强制排放控制器内部加热空气的设备 |
[__SOURCE](1-robot-system/1-basic-constitution/2-teach-pendant.md)
# 1.1.2 教学终端

本操作手册描述了如何使用基于TP630型号的教学终端。TP630是专为${cont_model}控制器开发的型号，并提供了一个大型触摸屏。

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
      <td style="text-align:left">控制机器人的操作，输入命令或选择菜单</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">模式开关</td>
      <td style="text-align:left">您可以旋转模式开关以选择操作模式 (
        <img src="../../_assets/sb-manual.png" alt/>手动/
        <img src="../../_assets/sb-auto.png" alt/>自动/
        <img src="../../_assets/sb-remote.png" alt/>远程)。如果您将模式开关从教学终端上移除，所选操作模式将被锁定。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">显示屏</td>
      <td style="text-align:left">触摸屏使您能够检查和更改操作状态并设定机器人的信息。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">紧急停止开关</td>
      <td style="text-align:left">在紧急情况下按下时使机器人停止操作</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">USB连接端口</td>
      <td style="text-align:left">可用于连接可以通过USB通信访问的设备，如可移动存储设备<br>
      请使用FAT32格式。请注意，不支持exFAT、NTFS格式。
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">安装支架</td>
      <td style="text-align:left">固定或悬挂教学终端以便存放</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left">启用开关</td>
      <td
      style="text-align:left">
        <p>在手动模式下使用教学终端操作机器人时作为安全开关的开关</p>
        <ul>
          <li>阶段
       1，阶段 3：机器人操作将停止。在阶段 3 的情况下，
       开关将恢复到阶段 1，而无需经过阶段 2。</li>
          <li>阶段 2：您可以操作机器人。</li>
        </ul>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c8.png" alt/>
      </td>
      <td style="text-align:left">电缆连接器</td>
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
  <p><span lang=EN-US>您必须在想要执行键顶部（蓝绿色）显示的功能时使用此按钮。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l3 level1 lfo2;tab-stops:list 36.0pt'><span lang=EN-US>当
       此键在操作[快速向前/
       向后]功能时一起按下，能够以高速激活向前/向后步进</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l3 level1 lfo2;tab-stops:list 36.0pt'><span lang=EN-US>当
       从输入显示窗口编辑字符串时，可以通过按下带有`[←/→]`键的按钮来移动光标。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l3 level1 lfo2;tab-stops:list 36.0pt'><span lang=EN-US>从
       任务编辑窗口，可以通过按下带有`[↑/↓]`键的按钮逐屏移动光标。</span></li>
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
  <p class=MsoNormal><span lang=EN-US>步进前进/后退</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>在手动模式下逐步向前或向后移动时使用。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l5 level1 lfo3;tab-stops:list 36.0pt'><span lang=EN-US>请
       参阅`[cond.set] - 步进前进/后退最大速度`以获取详细描述。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l5 level1 lfo3;tab-stops:list 36.0pt'><span lang=EN-US>当
       此键与`[SHIFT]`一起按下时，可以激活快速步进
       前进/后退功能。</span></li>
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
       auto;mso-list:l11 level1 lfo4;tab-stops:list 36.0pt'><span lang=EN-US>此
       键还具有返回到上级而不保存的功能。</span></li>
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
  <p><span lang=EN-US>根据坐标系进行机器人的操作。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l12 level1 lfo5;tab-stops:list 36.0pt'><span lang=EN-US>每
       个轴在关节坐标系中移动。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l12 level1 lfo5;tab-stops:list 36.0pt'><span lang=EN-US>机器人
       在机器人坐标系中以直角方向移动。</span></li>
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
       键移动记录步骤或功能的参数。</span></li>
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
  <p><span lang=EN-US>用于快速执行注册的功能。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l14 level1 lfo7;tab-stops:list 36.0pt'><span lang=EN-US>按下
       R-代码键会弹出一个输入代码号码的窗口。有关更多信息，请参阅“8. R 代码”。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l14 level1 lfo7;tab-stops:list 36.0pt'><span lang=EN-US>R-代码
       键后跟`[ENTER]`而没有代码号码与“R0 : 步数计数重置”相同。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l14 level1 lfo7;tab-stops:list 36.0pt'><span lang=EN-US>在
       是非问题中，按下R-代码意味着负面答案。</span></li>
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
       auto;mso-list:l6 level1 lfo8;tab-stops:list 36.0pt'><span lang=EN-US>如果使用此键完成数字输入，则输入框的内容会反映在编辑框中。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l6 level1 lfo8;tab-stops:list 36.0pt'><span lang=EN-US>在
       Permit/Refuse (是/否) 的响应中选择Permit (是) 时也可以使用此键。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l6 level1 lfo8;tab-stops:list 36.0pt'><span lang=EN-US>当
       您在句子光标处按下此键时，它将切换到单词光标，可以编辑参数。</span></li>
  </ul>
  </td>
 </tr>
 <tr style='mso-yfti-irow:9'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US><span style='mso-no-proof:yes'><img
  width=101 height=48 id="_x0000_i1034" src="../../_assets/tp630/k-motor-on.png"></span></span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>电机开</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于为机器人每个轴提供伺服电源。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l4 level1 lfo9;tab-stops:list 36.0pt'><span lang=EN-US>[MOTOR
       ON]灯在手动模式下闪烁。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l4 level1 lfo9;tab-stops:list 36.0pt'><span lang=EN-US>[MOTOR
       ON]灯在自动模式下点亮。</span></li>
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
  <p><span lang=EN-US>用于自动播放工作程序。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l15 level1 lfo10;tab-stops:list 36.0pt'><span lang=EN-US>在
       模式开关处于自动状态且电机开启的条件下，<START>键会自动播放工作程序。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l15 level1 lfo10;tab-stops:list 36.0pt'><span lang=EN-US>如果
       机器人开始自动操作，[START]灯点亮，[STOP]灯熄灭。</span></li>
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
  <p><span lang=EN-US>用于在自动操作过程中暂时停止机器人。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l2 level1 lfo11;tab-stops:list 36.0pt'><span lang=EN-US>如果
       机器人停止，[STOP]灯点亮，[START]灯熄灭。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l2 level1 lfo11;tab-stops:list 36.0pt'><span lang=EN-US>当
       机器人停止时，它在原计划路径上停止，没有与其他设备碰撞的风险。</span></li>
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
  <p><span lang=EN-US>用于检查以前的工作历史。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l17 level1 lfo12;tab-stops:list 36.0pt'><span lang=EN-US>这
       会显示记录执行历史、错误历史、消息历史等的历史消息框</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l17 level1 lfo12;tab-stops:list 36.0pt'><span lang=EN-US>当
       您按下此键一次时，它会显示主板的输出历史，再按一次，则显示教学终端的输出历史。</span></li>
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
       auto;mso-list:l13 level1 lfo13;tab-stops:list 36.0pt'><span lang=EN-US>当
       您按下此按钮与[SHIFT(FAST)]键时，GUN1信号将手动输出。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l13 level1 lfo13;tab-stops:list 36.0pt'><span lang=EN-US>在进行点焊时，当您按下`[REC]`键时，SPOT命令会自动跟随MOVE。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l13 level1 lfo13;tab-stops:list 36.0pt'><span lang=EN-US>当
       在使用弧焊的自动操作期间此LED点亮时，机器人将实际执行弧焊。此LED熄灭时，它将不执行弧焊，仅检查教学轨迹。</span></li>
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
       auto;mso-list:l16 level1 lfo14;tab-stops:list 36.0pt'><span lang=EN-US>您
       可以在按下轴操作键时选择坐标系统（轴、笛卡尔、工具）以移动机器人。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l16 level1 lfo14;tab-stops:list 36.0pt'><span lang=EN-US>当
       您按下`[SHIFT]`键时，将弹出选择工具编号的消息框。</span></li>
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
  <p class=MsoNormal><span lang=EN-US>POS.MOD / REC</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于在程序中记录步骤，即添加MOVE命令时。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l9 level1 lfo15;tab-stops:list 36.0pt'><span lang=EN-US>此键插入的MOVE命令由隐藏姿态组成。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l9 level1 lfo15;tab-stops:list 36.0pt'><span lang=EN-US>当光标置于步骤时，可以插入下一步</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l9 level1 lfo15;tab-stops:list 36.0pt'><span lang=EN-US>通过按下`[SHIFT]`键可以修改选定的步骤位置。</span></li>
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
       auto;mso-list:l8 level1 lfo16;tab-stops:list 36.0pt'><span lang=EN-US>使用
       `[SHIFT]`键，此键将弹出工作程序窗口。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l8 level1 lfo16;tab-stops:list 36.0pt'><span lang=EN-US>按
       下[PROG]键两次，将显示程序列表。</span></li>
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
  <p class=MsoNormal><span lang=EN-US>机械</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p><span lang=EN-US>用于选择机制和单元。</span></p>
  <ul type=disc>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l7 level1 lfo17;tab-stops:list 36.0pt'><span lang=EN-US>对于
       机制，机器人是0，对于附加轴，遵循用户在初始设置菜单中设置的设置。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l7 level1 lfo17;tab-stops:list 36.0pt'><span lang=EN-US>当
       您按下此按钮与SHIFT键时，您可以将此按钮用于单位。当用户希望按照特定单位组合配置程序时，将使用单位。</span></li>
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
       auto;mso-list:l0 level1 lfo18;tab-stops:list 36.0pt'><span lang=EN-US>与
       `[SHIFT]`键一起，您可以输入'+'和'-'符号或删除
       命令句子或参数。</span></li>
   <li class=MsoNormal style='mso-margin-top-alt:auto;mso-margin-bottom-alt:
       auto;mso-list:l0 level1 lfo18;tab-stops:list 36.0pt'><span lang=EN-US>`[BS]`
       键按字符反向删除。(Backspace)。而且，在编辑命令句子时，所有参数值都被删除。 </span></li>
  </ul>
  </td>
 </tr>
</table>

[__SOURCE](1-robot-system/2-basic-usage/README.md)
# 1.2    基本使用
[__SOURCE](1-robot-system/2-basic-usage/1-power-on/README.md)
# 1.2.1 开启电源

{% hint style="info" %}
开启和关闭电源的方法可能会因控制器的类型而异。
{% endhint %}

#### 垂直关节机器人控制器

要启动机器人，应该给机器人控制器供电。

将机器人控制器左侧的电源开关拨到ON方向，以连接控制器的主电源。当电源连接时，机器人系统将启动，教学手持操作器的显示屏会一起打开，所有设备也会开启。

![](../../../_assets/image_12.png)
[__SOURCE](1-robot-system/2-basic-usage/1-power-on/1-input-of-the-power-to-the-mot.md)
# 1.2.1.1 电源输入到电机和可操作状态

教导终端的模式开关和安全插头的状态决定了电机的电源输入和可操作状态。

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
          <li>电机开启允许</li>
          <li>前进/后退步骤允许</li>
        </ul>
      </td>
      <td style="text-align:left">紧急情况（电机关闭）</td>
    </tr>
    <tr>
      <td style="text-align:left">输入</td>
      <td style="text-align:left">
        <ul>
          <li>电机开启允许</li>
          <li>前进/后退步骤允许</li>
        </ul>
      </td>
      <td style="text-align:left">
        <ul>
          <li>电机开启允许</li>
          <li>以正常速度操作</li>
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

它指的是在完成所有工作后停止机器人并关闭控制器电源按钮的所有操作。

{% hint style="warning" %}
* 如果机器人长时间不使用，编码器电池可能会放电，因此请将机器人移动到参考位置，然后再关闭电源。

* 请注意，如果在编码器电池出现电压下降警报时关闭电源，可能会损坏编码器数据。 
{% endhint %}

#### 垂直关节机器人控制器

1. 按下教导 Pendant 上的 `[Stop]` 按钮。然后，正在运行的机器人将停止，并且停止指示灯将亮起。

2. 按下教导 Pendant 上的紧急停止开关。然后，机器人电机的伺服电源将被切断，然后电机将关闭。

![](../../_assets/image_36.png)

3. 将机器人控制器左侧的电源开关转到 OFF 方向。然后，机器人系统将断电。

![](../../_assets/image_29.png)
[__SOURCE](1-robot-system/2-basic-usage/3-change-language-of-tp.md)
# 1.2.3 更改教学挂件屏幕的语言

如果您需要更改教学挂件的语言，可以通过以下程序进行更改。以下是将英语更改为韩语模式的示例。

### A. 通过教学挂件选项更改 (仅支持 V70.00-00 及以上版本)

1. 点击 `[F1: 服务] ([F1: service])` 按钮。

    ![](../../_assets/tp630/service/fb-service.png)

2. 输入 `11: 教学挂件选项`。

    ![](../../_assets/tp630/service/menu-tp-option.png)

3. 从语言设置中选择 `韩语`。

    ![](../../_assets/tp630/service/tp-option-lang.png)

4. 按 `[ESC]` 键返回到顶层首页屏幕，然后稍等片刻。

<br>

### B. 关闭教学挂件软件后更改

1. 点击 `[F1: 服务] ([F1: service])` 按钮。

   ![](../../_assets/tp630/service/fb-service.png)

2. 选择 9: 退出 TP 应用程序。

    ![](../../_assets/tp630/service/exit-application.png)

3. 点击左下角的语言组合框。

    ![](../../_assets/tp630/service/autorun-sub-lang.png)

    {% hint style="info" %}

    对于 V60.32-00 以下的版本，请点击右上角的地球图标。

    ![](../../_assets/tp630/service/autorun-sub-lang-old.png)

    {% endhint %}

4. 从弹出菜单中选择 `英语`。

5. 点击右下角的 `[运行 TP]` 按钮，并等待约 15 秒钟。
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/README.md)
# 1.2.4 ${cont_model} 教教导器的屏幕

下图表示在教导器上显示的屏幕。${cont_model} 控制器的教导器屏幕由 10 个彩色触摸屏窗口组成。
<br>

![](../../../_assets/tp630/TP-main_eng.png)

| No. | 描述 | 
| :--- | :--- | 
| ![](../../../_assets/c1.png) | 标题显示窗口： TP 通信、机器人系统、机制等的各种状态图标。 ([1.2.3.1 标题显示窗口](1-title-area.md)) |
| ![](../../../_assets/c2.png) | 状态显示窗口：操作模式和设置 ([1.2.3.2 状态显示窗口](2-status-bar.md)) |
| ![](../../../_assets/c3.png) | R 按钮栏：主屏幕右侧的菜单组 ([1.2.3.3 R 按钮栏](3-Rbt-bar.md)) |
| ![](../../../_assets/c4.png) | 监视窗口：操作期间的运行数据 ([1.2.3.4 监视窗口](4-mon-area.md)) |
| ![](../../../_assets/c5.png) | 功能按钮栏：主屏幕底部的菜单组，支持主要设置和监控 ([1.2.3.5 功能按钮栏](5-function-buttons.md)) |
| ![](../../../_assets/c6.png) | 输入显示窗口：任务编辑窗口的直接输入区域 ([1.2.3.6 输入显示窗口](6-input-area.md)) |
| ![](../../../_assets/c7.png) | 引导显示窗口：操作期间的引导消息 ([1.2.3.7 引导显示窗口](7-guide-area.md)) |
| ![](../../../_assets/c8.png) | 任务编辑窗口：用于编辑 JOB 程序的区域 ([1.2.3.8 任务编辑窗口](8-work-area.md)) |
| ![](../../../_assets/c9.png) | 记录条件显示窗口：记录步骤的条件 ([1.2.3.9 记录条件显示窗口](9-record-cnd-area.md)) |
| ![](../../../_assets/c10.png) | L 按钮栏：主屏幕左侧的菜单组 ([1.2.3.10 L 按钮栏](10-Lbt-bar.md)) |
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/1-title-area.md)
# 1.2.4.1	标题显示窗口

该窗口显示机器人系统在主屏幕顶部的状态。

<br>


![](../../../_assets/tp630/TP-main-title.png)


| No. | 描述 | 
| :--- | :--- | 
| ![](../../../_assets/c1.png) | 显示网络状态。 (![](../../../_assets/flag-comm-ok.png) : 已连接, ![](../../../_assets/flag-comm-ng.png) : 未连接)|
| ![](../../../_assets/c2.png) | 插入USB存储设备时显示图标。 |
| ![](../../../_assets/c3.png) | 显示连续路径（CONTPATH）模式。 (CP# : CP(连续路径)+模式编号) <br> (参考: [R360](../../../8-r-code/15-r360.md?cont_model=${cont_model})) |
| ![](../../../_assets/c4.png) | 显示每个应用功能的当前状态。 (SW : 焊接记录状态, PBk : 涂装区) |
| ![](../../../_assets/c5.png) | 显示定位器同步状态。 (M:S{站号}) |
| ![](../../../_assets/c6.png) | 显示协作控制状态。 (I:独立, M:主控指定, S:从控指定) |
| ![](../../../_assets/c7.png) | 显示轴控制状态。 (关闭时显示 j_{轴编号}) |
| ![](../../../_assets/c8.png) | 显示轴锁定状态。 |
| ![](../../../_assets/c9.png) | 显示编码器电池故障状态。 (发生故障时闪烁) |
| ![](../../../_assets/c10.png) | 显示减速器寿命故障状态。 (发生故障时显示及闪烁轴编号) |
| ![](../../../_assets/c11.png) | 显示用户级别。 (E : 工程师模式) <br> (参考: [R314](../../../8-r-code/12-r314.md?cont_model=${cont_model})) |
| ![](../../../_assets/c12.png) | 显示PLC运行状态。 |
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/2-status-bar.md)
# 1.2.4.2 状态显示窗口

这显示机器人的各种操作状态。您可以通过触摸每个相关部分来设置显示的信息。

![](../../../_assets/tp630/TP-main-status_eng.png)

| No. | 描述 | 
| :--- | :--- |
| ![](../../../_assets/c1.png) | 机器人的操作模式显示。 <li>manual: 用于手动操作和编辑 JOB 程序的模式</li> <li>auto: 用于自动运行 JOB 程序的模式</li> <li>remote manual: 通过 I/O 信号远程设置手动或自动模式的模式（当前状态：手动模式）</li> <li>remote auto: 通过 I/O 信号远程设置手动或自动模式的模式（当前状态：自动模式）</li> |
| ![](../../../_assets/c2.png) | 您可以在弹出消息框中查看当前工具信息并进行更改。 |
| ![](../../../_assets/c3.png) | 机制显示机器人的类型或所选附加轴的编号。机器人为 0，供用户参考 `系统 - 5: 初始化 - 6: 机制设置 (System - 5: Initialize - 6: Mechanism setting)`。 |
| ![](../../../_assets/c4.png) | 显示为手动操作选择的参考坐标系的状态。 状态显示为“joint”、“user”、“robot”或“tool”，每次按下状态窗口时依次变化。 使用 `[Axis Operation]` 键，您可以根据参考坐标系移动机器人。<li>关节坐标系：机器人的每个轴将根据 `[Axis Operation]` 键的下部名称独立移动。</li> <li>机器人坐标系：机器人的 TCP 根据机器人坐标系通过 `[Axis Operation]` 键进行平移和旋转。</li> <li>用户坐标系：机器人的 TCP 根据用户坐标系通过 `[Axis Operation]` 键进行平移和旋转。</li> <li><img src="../../../_assets/bt-crd-tool (1) (1) (2).png" alt/> 工具坐标系：机器人的 TCP 根据工具坐标系通过 `[Axis Operation]` 键进行平移和旋转。</li> |
| ![](../../../_assets/c5.png) | 确定在手动模式下操作机器人的速度。在手动模式下，有两种不同的操作类型。一种是手动运行，另一种是步进前进/后退操作。 手动操作的速度有 8 个不同的级别（1~8）。 <li>如果按下教学挂架的速度 HI 键，速度级别增加一个步骤；如果按下速度 LOW 键，速度级别降低一个步骤。 按下 [SHIFT (FAST)] + 速度 HI 键时，速度级别设置为 8；按下 [SHIFT (FAST)] + 速度 LOW 键时，速度级别设置为 1。</li> |
| ![](../../../_assets/c6.png) | 显示日期和时间信息。 <br> 您可以在 [service - 8: 日期、时间设置] 菜单中更改此信息。 ([4.5 日期和时间设置](../../../4-service/5-date-time-setting.md)) |
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/3-Rbt-bar.md)
# 1.2.4.3 R(Right) 按钮栏

5 个按钮显示在屏幕右侧，您可以触摸这些按钮。未激活的按钮将被灰显。在自动模式下，'prev/next' 被禁用，无法使用这些功能。

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
        <p>这会手动输出常见输出、现场总线输出等，或手动设置参数的值。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>这将分割监视窗口，或组合已分割的窗口。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <p>这用于编辑命令句子或备注。作为触摸屏，它可以像键盘一样使用。</p>
        <p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p>这用于在 F 按钮栏中定义和使用用户键。</p>
        <p>预先指定的功能显示用于点焊或弧焊。有关更多信息，请参考应用手册。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">
        <p>这用于移动到功能按钮栏的下一页。</p>
        <p>当当前屏幕中有超过 7 个按钮时，按钮将被激活，每次按下此按钮时，将切换到下一个按钮集。当您按 `[SHIFT]` + 按钮时，将向相反方向切换回去。
      </td>
    </tr>
    </tr>
  </tbody>
</table>
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/4-mon-area.md)
# 1.2.4.4 监视窗口

这是一个窗口，用于实时显示每个轴的位置信息、I/O 数据和每个应用程序的状态数据。划分主屏幕并选择监视面板。您可以拥有多达 3 个监视面板。（参见 "[6. Monitoring](../../../6-monitoring/README.md)"。）

<br>

![](../../../_assets/tp630/TP-main-mon_eng.png)
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/5-function-buttons.md)
# 1.2.4.5 功能按钮栏

7 个功能按钮显示在主窗口的底部。功能按钮根据当前操作屏幕而变化。在最高级别屏幕中，显示进入服务菜单和系统菜单的按钮。同时，在编辑任务程序时，显示命令列表或命令参数设置的按钮。

![](../../../_assets/tp630/TP-main-functions_eng.png)

| No. | 描述 | 
| :--- | :--- | 
| ![](../../../_assets/c1.png) | service : 各种便利项，例如监控、变量和文件管理器 ([4.Service](../../../4-service/README.md)) |
| ![](../../../_assets/c2.png) | system : 机器人操作和应用的详细设置 ([7.System](../../../7-system/README.md)) |
| ![](../../../_assets/c3.png) | rel.WAIT : 释放信号等待，例如通过按 `[SHIFT]` 键释放输入信号或焊接完成信号 (前提条件：`[F2: 系统] - 1: 用户环境 - 'Wait(di/wi) release' - 不执行 ([F2: system] - 1: User environment - 'Wait(di/wi) release' - Disable)`) |
| ![](../../../_assets/c4.png) | log : 包括错误代码、通知消息、错误发生时间等的错误或警告历史 ([2.5.2 Error Handling](../../../2-operation/5-error-info/2-error-handle.md))|
| ![](../../../_assets/c5.png) | cmd.input : 显示在手动模式的初始页面，用于输入程序命令 ([3.2.2.1 Statements](../../../3-programming/2-prog-edit/1-statement.md))|
| ![](../../../_assets/c6.png) | cond.set : 机器人操作条件，例如前进/后退步骤的机器人速度和路径恢复 ([5.Condition Setting](../../../5-conditional-setting/README.md))|
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/6-input-area.md)
# 1.2.4.6 输入显示窗口

此区域显示要编辑的内容的输入值，例如命令语言、字符或功能。您可以通过 [cmd.input] 按钮直接插入命令，而无需选择命令。如果输入未定义的命令或语法错误的命令，将发生以下错误。

![](../../../_assets/tp630/pop-error-nocmd_eng.png)

<br>

下表是“移动”命令的每个参数的输入。
<br>

|command parameters|inputs |
|--|--|
|![](../../../_assets/tp630/pane-prog-mov-argument.png)|![](../../../_assets/tp630/TP-main-input.png)|
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/7-guide-area.md)
# 1.2.4.7 指导显示窗口

这显示了用户操作的指导或方向信息，并且是在'print'命令中设置打印方向为T/P时显示打印信息的区域。

<br>

下表是'move'命令每个参数的指导信息。

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

当您尝试编辑程序时，可能会由于文件属性而发生以下错误。有关文件属性的信息，请参阅 "[4.2.4 文件保护](../../../4-service/2-file-manager/4-file-protect.md)"。

![](../../../_assets/tp630/pop-error-fileprotect_eng.png)
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/9-record-cnd-area.md)
# 1.2.4.9 记录条件显示窗口

这是编辑记录步骤条件的窗口（速度、精度、工具选项等）。按下 [rec.cond] <img src="../../../_assets/tp630/lbt-record_eng.png" width="35mm"></img> 在 L 按钮栏上进行编辑。更多详细信息，请参阅 "[3.2.2.3 记录条件](../../../3-programming/2-prog-edit/2-statement-input/3-rec-cond.md)"。

<br>

![](../../../_assets/tp630/TP-main-recordcnd.png)
[__SOURCE](1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/10-Lbt-bar.md)
# 1.2.4.10 L(Left) button bar

5 个按钮显示在屏幕的左侧，您可以触摸这些按钮。非活动按钮将显示为灰色。在自动模式下，记录条件、手动移动被禁用，这使得无法使用这些功能。

<br>

![](../../../_assets/tp630/TP-main-lbt_eng.png)

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
        <p>这是用于编辑录制步骤的条件，包括速度、精度、工具编号、步骤选项等的键。编辑在录制条件窗口中进行。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>此按钮选择在前进/后退步骤时是逐步执行还是功能执行，或者是否连续执行到任务程序的结束。当前选择的条件以图标的形式显示在按钮上。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <p>这是当您希望按指定数量手动移动机器人时在微调级别使用的键。当 jog inching 功能激活时，绿灯会亮起。</p>
        <p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p>如果在某个命令句子处按下此键，将执行与该命令句子相关的快速打开功能。有关详细描述，请参见快速打开。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">
        <p>根据每个状态显示相关帮助。如果光标处于命令句子中，按下此键将显示命令句子的语法形式。发生错误时，按此键可查看内容、措施或诊断方法。
</p>
      </td>
    </tr>
    </tr>
  </tbody>
</table>
[__SOURCE](2-operation/README.md)
# 2. 操作

操作是指向机器人指示工作内容并检查内容的行为。一般来说，工业机器人使用手动和自动模式。手动操作是指直接向机器人指示工作内容的行为，而自动操作是指让机器人重复执行指示工作内容的行为。
[__SOURCE](2-operation/1-manual-operation/README.md)
# 2.1 手动操作

手动操作是一种以安全速度直接教导和检查机器人的操作方法。

{% hint style="danger" %}
[DANGER] 与正常操作不同，手动操作的教学模式是一个高风险工作阶段，操作员直接进入机器人的操作范围。在教学过程中意外的机器人移动可能导致碰撞、夹住或压伤事故，可能导致严重伤害或死亡。
{% endhint %}
[__SOURCE](2-operation/1-manual-operation/1-how-to-op.md)
# 2.1.1 操作方法

通过使用 jog 键指导机器人的工作内容并检查指导工作的内容的方法如下。

1. 检查安全围栏和机器人操作范围内是否有人员或障碍物。

2. 通过旋转教导挂件的模式开关将操作模式设置为手动模式。

    ![](../../_assets/tp630/TP-hw-switch-manual.png)

3. 在 ${cont_model} 教导挂件屏幕的状态栏中，检查操作模式是否设置为手动模式。

    ![](../../_assets/tp630/sbar-mode_eng.png)

    * 如果设置为自动模式，通过旋转教导挂件的模式开关将操作模式设置为手动模式。

4. 用 `[SHIFT]` 触碰 `[PROG]` 键。然后，程序选择窗口将出现。

    ![](../../_assets/tp630/k-prog-step_eng.png)

5. 从程序选择窗口的列表中选择一个程序，或输入程序编号，然后按 `[ENTER]` 键。

    ![](../../_assets/tp630/k-prg-select_eng.png)

6. 按下教导挂件上的 `[motor]` 键。然后，电动机灯将闪烁，伺服电源将准备为机器人的每个轴的电动机提供。

7. 按下教导挂件背面的使能开关。然后，电动机灯将点亮，电动机刹车将释放，允许伺服电源供应。机器人将准备移动。

8. 使用 jog 键根据坐标系统的速度级别或运动条件操作机器人。

    * 要保存机器人的位置，在所需位置触碰 `[REC]` 键。然后该步骤将被记录。
    * 要记录步骤所需的功能，请触碰 `[cmd.input]` 按钮。
    * 要在手动前进或后退时检查机器人的位置，请按 `[STEP.FWD/STEP.BWD]` 键。在按住 `[STEP.FWD/STEP.BWD]` 键时，机器人将以步骤单位移动。当机器人到达目标步骤时，执行完成标记 \( . \) 将出现在命令前方，然后机器人将停止。
[__SOURCE](2-operation/1-manual-operation/2-op-speed.md)
# 2.1.2 操作速度调整

在手动模式下，您可以通过前进/后退操作和手动关节操作来操作机器人。当前的速度设置在状态显示窗口的速度窗口中显示。

![](../../_assets/tp630/sbar-spd-manual_eng.png)

'Man. spd' 仅用于手动模式，在自动模式下被 'Play spd' 取代。速度窗口下方的数字 '1' 表示关节速度级别，而 '200mm/s' 表示前进/后退速度限制。

例如，如果手动模式下的速度限制设置为 250 mm/s，而记录的步进速度为 1,000 mm/s，则步进的移动速度在前进/后退操作期间将限制为 250 mm/s。当记录的速度为 100 mm/s 时，机器人将以 100 mm/s 的速度移动，因为记录的速度没有超过速度限制。

{% hint style="info" %}
要设置步进速度限制，请参考 "[5.1 操作条件设置](../../5-conditional-setting/1-op-cond-set.md)"。
{% endhint %}

要设置关节速度级别 \(1: 低到 8: 高\)，请反复按 <SPEED: HI, LOW> 键，直到所需的速度级别出现。在这种情况下，机器人工具和连接件的最大速度将限制在速度限制以下。

{% hint style="info" %}
在自动模式下， `[Speed Adjustment]` 按钮将显示播放速度 \(%\)，而不是步进速度限制 \(mm/sec\)。
{% endhint %}


{% hint style="warning" %}
如果工具数据中的长度和角度与实际值设置不同，工具在手动模式下可能会操作得太快。在操作机器人之前，您必须确保工具数据设置正确。
{% endhint %}
[__SOURCE](2-operation/1-manual-operation/3-step-fwd-bwd.md)
# 2.1.3 向前/向后步骤

向前/向后步骤是手动模式下操作机器人的方法之一，指的是播放录制程序的动作。通过在向前/向后操作中操控机器人，可以在安全的速度范围内检查录制的程序路径和相互锁定关系。

向前/向后操作的执行单元可以从 ${cont_model} 教学手持屏幕左侧的 `[run to]` 按钮进行检查和设置。

![](../../_assets/tp630/lbt-runto_eng.png)  

要设置向前/向后操作的执行单元，反复点击 `[run to]` 按钮，直到所需选项出现。

![](../../_assets/tp630/lbt-runto-sw_eng.png)

* `[cmd]`：将逐行执行命令
* `[Step]`：将逐步执行
* `[End]`：将执行到结束语句

<Br>

当执行单元设置为 'Cmd' 或 'Step' 时，机器人将忽略设置的精度区域并到达记录的步骤。如果设置为end，机器人将在与播放 b/n 自动模式相同的路径上操作。

当您将执行单元设置为 'Cmd' 或 'Step' 并执行向前/向后操作时，机器人将在没有拐角的路径上操作。有关拐角的详细信息，请参见 "[2.3.1.4 精度](../3-step/1-step-cmd-param/4-accuracy.md)"。

![图11 当执行 cmd/step 设置时播放向前/向后路径](../../_assets/path-cmd-step-pback-fwd-bwd-en.png)

如果您将执行单元设置为end，然后执行向前/向后操作，机器人的路径将根据停止位置而变化。换句话说，如果机器人停在非拐角的位置，然后执行向前操作，机器人将恢复原始拐角路径，但如果机器人执行向后操作，机器人将移动到记录的步骤，此时机器人将在记录的步骤处停止，然后立即移动到上一个步骤。当机器人停在拐角处时，机器人将在向前和向后移动时保持其先前的拐角路径。

![图12 当执行end设置时播放向前/向后路径](../../_assets/path-end-pback-fwd-bwd-en.png)

当机器人停在拐角处然后执行向前操作时，机器人将在原始拐角路径上操作。在这里，如果机器人执行向后操作，而后又在没有完全到达上一个步骤的情况下再次执行向前操作，机器人可能无法在某些情况下创建原始的拐角路径。换句话说，如果步骤的距离变短于原始距离，导致无法满足现有的精度条件，则将创建一个小于原始的拐角路径。

![图13 在向前/向后操作期间机器人路径变化的示例](../../_assets/path-step-bwd-then-fwd-en.png)

您可以设置向前/向后操作的最大速度，并设置是否执行功能。触摸 ${cont_model} 教学手持屏幕左侧的 `[run to]` 按钮后，在设置窗口中设置速度值和功能执行选项。

![](../../_assets/tp630/cond-set-step-fwd-bwd-spd_eng.png)

* `2: 步骤前进/后退最大速度 (2: Step FWD/BWD maximum speed)`：与手动操作中设置的速度值相同
* `[3: 步骤向前执行功能]`：您可以选择功能执行选项。
  * Off：在步骤向前/向后操作中不会执行功能。无论外部 I/O 的条件如何，只能检查机器人路径。请注意，外部系统的互锁将不起作用。
  * On：您可以执行所有功能。应在外部互锁完成后使用。
  * I On：您只能执行输入等待功能。应在需要通过外部互锁检查安全时使用。
[__SOURCE](2-operation/2-automatic-operation/README.md)
# 2.2 自动操作

自动操作是一种教学机器人应该执行的工作的内容，然后让机器人执行工作的操作方法。
[__SOURCE](2-operation/2-automatic-operation/1-how-to-op.md)
# 2.2.1 操作方法

教机器人工作内容并让其执行工作的方式如下。

1. 检查安全围栏内及机器人操作范围内是否有人员或障碍物。

2. 通过转动教导挂件的模式开关，将操作模式设置为自动模式。

    <div style="max-width: 35vw">  

     ![](../../_assets/tp630/TP-hw-switch-auto.png)
     
    </div>

3. 在 ${cont_model} 教导挂件屏幕的状态栏上，检查操作模式是否设置为自动模式。

    ![](../../_assets/tp630/sbar-mode-auto1_eng.png)

* 如果设置为手动模式，请转动教导挂件的模式开关，将操作模式设置为自动模式。

4. 点击初始屏幕左侧的 `[Recording Condition]` 按钮。然后，将出现条件设置窗口。

    ![](../../_assets/tp630/fbt-condset_eng.png)

5. 设置程序重复选项和机器人操作速度。

    ![](../../_assets/tp630/cond-set-cycle-auto-spd_eng.png)

* `1: Operation Cycle type`: 您可以设置是否重复在自动操作期间将要执行的程序。
* `6: 自动运行速率 (6: Playback speed rate)`: 您可以设置程序在自动模式下回放时机器人的操作速度 \(%\)。  
  例如，如果设置操作速度为100，机器人将在记录的步骤速度下移动；如果设置为50，机器人将以记录速度的50%比例移动。

6. 按下教导挂件上的 `[start]` 键。启动灯会亮起，机器人将根据创建的程序执行工作。
[__SOURCE](2-operation/2-automatic-operation/2-adjust-op-spd.md)
# 2.2.2 操作速度调整

在自动操作中，${cont_model} 教学点屏幕左侧的 `[Speed Adjustment]` 按钮将在程序播放时显示机器人的操作速度 \(%\)。显示的操作速度是机器人移动速度与步骤中记录的速度的比率。

![](../../_assets/tp630/sbar-spd-auto_eng.png)

{% hint style="info" %}
在手动模式下，`[Speed Adjustment]` 按钮将显示步骤速度限制，而不是播放速度 \(%\)。
{% endhint %}

在自动模式中，您可以通过更改条件设置中的自动操作速度比例值来调整机器人操作速度，而无需修改程序。在触摸 ${cont_model} 教学点屏幕左侧的 `[Speed Adjustment]` 按钮后，在设置窗口中设置 `2: 步骤前进/后退最大速度 (2: Step FWD/BWD maximum speed)` 和 `[6: Playback speed rate]` 的选项值。

![](../../_assets/tp630/cond-set-step-fwd-bwd-spd-auto-spd_eng.png)
[__SOURCE](2-operation/3-step/README.md)
# 2.3 步骤

步骤是指在作业程序中记录的特定姿势（每个轴的位置或工具提示的位置），由机器人采取。换句话说，步骤是机器人通过移动达到的一个位置。

机器人在从一个步骤移动到另一个步骤时执行各种功能。为了从一个步骤移动到另一个步骤，需要一个运动条件，例如移动，这是一个运动命令。

* 它是机器人编程的基本单元。这是操纵器移动的命令。它由机器人操作所需的最少信息组成。
* 运动条件：这些是步骤语句参数，如机器人位置、插值、速度、精度和工具编号。
[__SOURCE](2-operation/3-step/1-step-cmd-param/README.md)
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
[__SOURCE](2-operation/3-step/1-step-cmd-param/1-interpolation.md)
# 2.3.1.1 插值

插值是指步骤之间的插值路径，[Step N] 的插值方法决定了 `[Step N-1]` 和 `[Step N]` 之间路径的形式。

* P-PTP \(Point-to-Point\) 这是一般插值模式中最快的，因为它基于各个轴而不是工具提示进行两个步骤之间的路径插值。考虑到由旋转关节组成的工业机器人特性，工具提示的路径通常呈 C 形。




![Figure 15 Example of the Tooltip Path in P-PTP Interpolation](../../../_assets/image_73.png)

* L-线性插值 它在笛卡尔空间内两个步骤之间沿线性路径移动。它用于需要线性路径的情况，如弧焊部分。移动的同时，手腕姿态会自动按如下方式变化。

![Figure 16 Example of L-Linear Interpolation](../../../_assets/image_48.png)

在进行线性插值时，在某些条件下，机器人无法自动改变手腕姿态，这种情况称为奇异姿态。



{% hint style="info" %}
无法执行姿态插值的奇异姿态如下。

* 如果 B 轴接近死区：有关死区设置的详细信息，参见 "[7.4.5 B-axis Deadzone](../../../7-system/4-robot-parameter/5-b-axis-deadzone.md)"。
* 当 B 轴的符号改变时：当 B 轴角度的符号切换 \( - → + \) 或 \( + → - \)
* 当 R2 和 R1 轴的角度变化超过 180 度
* 当 B 轴 \(轴 5\) 的中心或工具提示经过 S 轴 \(轴 1\) 的旋转中心时：姿态和轨迹可能会有误差。
* 当 S 轴的角度变化超过 180 度
{% endhint %}

* C-圆形插值

  它在两个步骤之间创建的圆形路径上移动。确定圆的需要三个点，选择它们的参考如下。



  * 在从 `[Step n]` 移动到 `[Step n+1]` 时，如果 `[Step n+1]` 的插值方法是 C-圆形插值，则需要参考下一个步骤 `[Step n+2]`。

  * 如果 `[Step n+2]` 的插值方法是 C-圆形插值，则需要根据 `[Step n]`、`[Step n+1]` 和 `[Step n+2]` 确定圆，并在它们之间的运动应该沿 `[Step n]` - `[Step n+1]` 的弧进行。

  * 如果 `[Step n+2]` 的插值方法不是圆形插值，则需要参考前一个步骤 `[Step n-1]`，根据 `[Step n-1]`、`[Step n]` 和 `[Step n+1]` 确定圆，并在它们之间的运动应该沿 `[Step n]` - `[Step n+1]` 的弧进行。



![Figure 16 Example 1 of C-Circular Interpolation](../../../_assets/image_338.png)

如果您使用选择确定圆的三个点的标准，即使在连续弧的情况下，也可以通过同一点的双重注册创建程序。

通过考虑沿运动路径确定步骤的插值方法，并使用同一点双重注册功能，可以创建所需的程序。

![Figure 17 Example 2 of C-Circular Interpolation](../../../_assets/image_302.png)

* 静态工具插值

  当机器人拥有工件并使用外部固定工具进行工作时，将使用此方法。在这种情况下，将根据机器人拥有的工件进行插值。

  有关静态工具的插值类型的详细信息，请参见 "[7.3.6.2 Stationary Tool Coordinate System](../../../7-system/3-control-parameter/6-cordsys-reg/2-stationary-tool-crdsys.md)"。
[__SOURCE](2-operation/3-step/1-step-cmd-param/2-pose.md)
# 2.3.1.2 姿态

姿态是记录位置的参数。如果您通过使用`[Command]`按钮输入一个移动，您应该在tg \(target\)参数中指定姿态表达。当使用`[REC]`键输入移动指令时，tg参数将不会出现。在按下`[REC]`键的那一刻，操作器的位置和姿态将被记录，但不会在工作编辑屏幕上显示，这就是为什么它们被称为隐藏姿态。

输入姿态的方法如下。

1. 声明一个姿态变量，po1。
   选择[cmd.input > var_io > global or var]菜单，然后输入'po1'。
2. 使用`[cur.pose]`按钮将姿态变量初始化为姿态类型。
3. 执行声明和初始化命令，以便在每个命令的前面标记句点。
4. 按下`[cmd.input]`按钮后，选择`[motion]`，然后输入该语句。

    ![](../../../_assets/tp630/fbt-cmd-input-motion_eng.png)

5. 按下`[property]`按钮，设置当前机器人姿态的属性，然后按下`[Apply]`按钮。

    ![](../../../_assets/tp630/prg-step-pose_eng.png)

<br>

姿态变量和偏移变量将以以下格式保存。

<table>
  <thead>
    <tr>
      <th style="text-align:center">姿态变量</th>
      <th style="text-align:center">偏移变量</th>
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
          <br />&quot;user{n}&quot; = 用户坐标系 (n 指一个数字)
          <br
          />&quot;joint&quot; = 关节坐标系
          <br />&quot;encoder&quot;= 编码器</p>
      </td>
      <td style="text-align:center">
        <p>{坐标系}:</p>
        <p>&quot;base&quot; = 基坐标系
          <br />&quot;robot&quot; = 机器人坐标系
          <br />&quot;user{n}&quot; = 用户坐标系 (n 指一个数字)
          <br
          />&quot;joint&quot; = 关节坐标系</p>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](2-operation/3-step/1-step-cmd-param/3-speed.md)
# 2.3.1.3 速度

机器人的操作速度可以使用以下四种单位显示。它们可以用于所有插值方法。

* mm/sec, cm/min: 设置机器人的TCP（工具中心点）的最大速度。机器人的最大速度将由控制器根据位置和加速度/减速度参数自动计算。如果设置值超过机器人的性能最大速度限制，机器人将仅以最大速度限制运行。

* sec: 设置机器人移动时间。机器人的最短移动时间将由控制器根据位置和加速度/减速度参数自动计算。如果设置值短于机器人的性能最短时间限制，机器人将仅以最短时间限制运行。

* %: 设置机器人移动速度与机器人可以操作的最大速度的比率。当该值设置为100%时，机器人将在允许范围内以最大速度运行。

### 机制指定速度规划
* {mech:机制编号, spd:速度}(速度单位): 根据选择的机制编号规划相应步骤的速度轨迹。
* 代码示例
```python
S2 move P,spd={mech:1,spd:100}mm/sec,accu=0,tool=0
```
| 机制指定速度规划（机制100mm/sec）| 机器人速度规划（机器人100mm/sec）| 
|---|---| 
| ![alt text](../../../_assets/tp630/Vel_Profile_2Mec_Addaxis.gif) | ![alt text](../../../_assets/tp630/Vel_Profile_1Mec_Rob.gif) |

* 上面的黄色圆圈表示设置为机制1的附加轴。
  * 机制指定速度：附加轴（机制1）生成与100 mm/sec速度匹配的轨迹。
  * 默认设置：机器人生成与100 mm/sec速度匹配的轨迹。

<br>

{% hint style="info" %}
机制指定速度规划功能从版本V60.32-00开始提供。

* 该规范仅适用于单位为mm/sec或cm/min时。
* 如果选择的机制处于停止状态，则根据机器人速度执行移动。
* 如果附加轴为旋转类型，则根据`[系统→5: 初始化→5: 附加轴参数设置]`中配置的旋转半径以mm/sec或cm/min规划速度。
* 当使用旋转定位器静止编织功能时，速度根据定位器上工件的旋转半径进行规划。（必须完成定位器校准。）
{% endhint %}
[__SOURCE](2-operation/3-step/1-step-cmd-param/4-accuracy.md)
# 2.3.1.4 精度

它将决定机器人在进行目标步骤时经过该步骤的精度（接近记录位置的程度）。当机器人移动到目标步骤时，如果当前位置信息与机器人在移动到目标步骤时产生的记录位置之间的误差小于某个值，机器人将移动到下一个步骤。此时允许的误差值称为精度。

根据精度，在精度范围内（0~7）新创建的路径称为转弯路径。通常，精度越高，转弯速度越快，这在移动时间上是有利的。

![图 19 因精度而改变的路径 P2](../../../_assets/image_53.png)

精度 0 具有最高的精度，而精度 7 具有最大的误差。精度将以不超过目标步骤两个轨迹中较短轨迹长度的 1/2 的方式进行应用。换句话说，您可以在上述示例中应用表达式 “精度 ≤ min\(P1-P2, P2-P3\) / 2”。在此表达式中，TCP 距离用于解释，但同样的概念可以应用于角度。

在机器人的情况下，适用精度等级的数值将基于机器人的工具提示距离和姿态角度进行定义。当涉及附加轴时，线性轴的值将基于长度进行定义，旋转轴的值将基于角度进行定义。您可以直接更改 `[system - 3: Robot Parameter - 6: Accuracy]` 菜单中的值。有关精度等级值的详细信息，请参阅 “[7.4.6 精度](../../../7-system/4-robot-parameter/6-accuracy.md)”。

下面的图显示了如何根据精度等级的值创建转弯路径。如果有一个普通的 6 轴关节机器人和一个附加轴，则可以分别为 TCP（工具提示距离）、ORN（位置角度）和 AUX（附加轴距离）设置精度等级的值。因为所有相关精度等级的值都应满足，所以转弯路径将基于 TCP、ORN 和 AUX 中的最小值创建。转弯路径将以恒定曲线创建，无论速度变化如何，同时满足凸包性质。然而，在低速和高速下可能会因伺服延迟而出现几毫米（mm）的误差。

![图 19 根据精度等级的值创建转弯路径](../../../_assets/image_79.png)

{% hint style="info" %}
根据精度等级的值创建转弯路径的模式将以相同的方式应用于所有类型的插值。在 P 插值的情况下，将应用 TCP 距离精度，但可能会出现误差。
{% endhint %}

由于凸包性质，转弯路径不会超过凸多边形区域，如下所示。

![图 20 转弯路径上的所有点都在凸多边形区域内](../../../_assets/image_87.png)
[__SOURCE](2-operation/3-step/1-step-cmd-param/5-tool-no.md)
# 2.3.1.5 工具编号

机器人位置将由工具提示的位置信息和姿态决定。您可以指定将要使用的工具编号 \(0-31\)。有关更多详细信息，请参阅 "[7.4.1.1 工具数据设置](../../../7-system/4-robot-parameter/1-tool-data/1-tool-data-set.md)"。
[__SOURCE](2-operation/3-step/1-step-cmd-param/6-until.md)
# 2.3.1.6 停止条件

当条件表达式“在...之后”满足时，机器人停止移动并执行下一个命令 \(步骤或功能\)。

条件表达式“在...之后”的值可以通过结果 \( \) 函数的返回值进行检查。您可以检查移动操作是否因条件表达式而终止。

![Figure 21 Example of Stop Conditions](../../../_assets/image_46_1.png)

{% hint style="info" %}
有关机器人语言的详细信息，请参阅 "[Robot Language Function Manual](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/README)。"
{% endhint %}
[__SOURCE](2-operation/3-step/1-step-cmd-param/7-comment.md)
# 2.3.1.7 注释

您可以为步骤的描述输入注释。您可以通过使用软键盘方便地输入注释的内容。
有关如何使用软键盘的更多详细信息，请参考 "[3.2.4.4 软键盘](../../../3-programming/2-prog-edit/4-statement-edit/4-softkeyboard.md)"。
[__SOURCE](2-operation/3-step/2-step-pose-modify/README.md)
# 2.3.2 记录和改变步骤位置

您可以使用 `[REC]` 键记录或改变记录步骤的机器人位置和姿态。
[__SOURCE](2-operation/3-step/2-step-pose-modify/1-joint-crd-sys.md)
# 2.3.2.1 轴角记录坐标

在手动模式下，如果在 `[system - 1: User Environment]` 菜单中的 `[1: Pose Recording Form]` 选项设置为轴角，则触摸移动语句中的 `[property]` 按钮。将出现以下属性窗口。编码器记录的机器人位置只能查看，位置数据无法修改。

![](../../../_assets/tp630/lbt-property_eng.png)

![](../../../_assets/tp630/dlg-property-axis_eng.png)
[__SOURCE](2-operation/3-step/2-step-pose-modify/2-base-robot-crd-sys.md)
# 2.3.2.2 基座和机器人记录坐标

机器人的位置和姿态可以根据坐标系统以不同方式显示。如果没有移动轴，基座坐标和机器人坐标通常是相同的。如果定义了移动轴，机器人工具的位置和姿态将根据基座坐标和机器人坐标的不同而不同。

在手动模式下，如果在 `[system - 1: User Environment]` 菜单中将 `[1: Pose Recording Form]` 选项设置为基座或机器人，则触摸移动语句中的 `[property]` 按钮。您可以在属性窗口中检查机器人工具的位置和姿态。

{% hint style="info" %}
如果您想更改姿态记录形式，请联系我们的客户支持团队以咨询专家或工程师。
{% endhint %}

对于一个工具提示位置及其方向，由于仪器的特性，可能会有多个姿态，因此为了定义一个姿态，机器人形式 \(config.\) 应该被指定。

协作机器人由于其机械结构可以受到软限制的限制。当机器人不在操作时，您可以解除软限制或将其设置为较大值。

* auto: 关于机器人的当前姿态，后面的项将自动确定。如果未设置此模式，则根据以下项是否被指定进行判断。
* back: 机器人的工具提示在机器人坐标系统的 X 轴的 - 方向上，表示后方。如果未指定，则工具提示将在 + 方向上，表示前方。
* down: H轴和V轴之间的关系。如果指定了这一点，结果将是底部。如果未指定，结果将是顶部。

![图 23 H轴和V轴的姿态：上 \(左\)，下 \(右\)](../../../_assets/image_58_1.png)

* flip: B轴坐标为 + 值时翻转。如果未指定，结果将为非翻转并为 - 值。图中的红色箭头显示腕轴顶部的方向。

![图 24 翻转 \(左\) / 非翻转 \(右\) 姿态](../../../_assets/image_75.png)

* `S (|S|>=180)`: S轴角度的绝对值大于 180 度。如果未指定，将小于 180 度。
* `B (|B|>=180)`: B轴角度的绝对值大于 180 度。如果未指定，将小于 180 度。

* `R2 (|R2|>=180)`: R2轴角度的绝对值大于 180 度。如果未指定，将小于 180 度。

* `R1 (|R1|>=180)`: R1轴角度的绝对值大于 180 度。如果未指定，将小于 180 度。

坐标系统将保存为 `[Pose Variable]`.crd \(示例: po32.crd\)，并将指定以下字符串之一。如果是空字符串，则基本值将被识别为关节。

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

R 代码是分配给特定功能的唯一代码数字。为常用功能分配唯一代码数字可以帮助您快速使用这些功能。有关 R 代码的详细信息，请参阅 "[8. R 代码](../8-r-code/README.md)。"

在触摸 `[R..[NO]]` 键后，输入代码数字并触摸 `[OK]` 按钮。然后将执行预定义功能。

![](../_assets/tp630/k-r.png)
[__SOURCE](2-operation/5-error-info/README.md)
# 2.5 错误信息

当出现问题时，通知将在 ${cont_model} 教学挂件屏幕底部的任务栏上显示，并闪烁约一分钟。您可以检查错误代码、通知消息和错误发生时间。

![](../../_assets/tp630/wg-alarm_eng.png)
[__SOURCE](2-operation/5-error-info/1-error-type.md)
# 2.5.1 错误类型

机器人系统中的故障由错误和警告组成。

![](../../_assets/tp630/wg-err-wrn_eng.png)

* 错误：这是一个严重到足以停止机器人操作的问题，通知消息中的代码编号以 E 开头。

* 警告：机器人将继续操作，但警告是一个需要您检查是否采取了响应措施的问题。通知消息中的代码编号以 W 开头。
[__SOURCE](2-operation/5-error-info/2-error-handle.md)
# 2.5.2 错误处理

以下内容展示了如何检查和处理各种系统问题，例如系统故障或操作错误。

* 当发生警告或错误时，带有编码和标题的通知将显示在指导显示窗口中。

  ![](../../_assets/tp630/wg-alarm_eng.png)

* 在指导显示窗口上触摸 [log] 按钮。然后，错误和警告历史将在新窗口中显示。

  * 错误和警告历史将按时间顺序显示，最新的问题将用黄色突出显示。
  
  ![](../../_assets/tp630/fbt-log_eng.png)

  ![](../../_assets/tp630/wg-alarm-log_eng.png)

* 在 ${cont_model} 教学挂件屏幕的 L-button 栏上触摸 `[Help]` 按钮。您可以查看错误代码、通知消息、故障原因以及如何采取措施。

  ![](../../_assets/tp630/lbt-help_eng.png)

  ![](../../_assets/tp630/help-alarm_eng.png)
[__SOURCE](2-operation/6-log.md)
# 2.6 事件日志

存储从过去到当前时间点发生的事件日志，例如错误、警告、通知、开始/停止操作、操作、I/O 值变化和机器人语言执行。（存储的最大记录数根据类型而异。）<br>
您可以查看每个日志的类型、消息、发生时间、发生时的程序/步骤/功能编号及相关辅助信息。这些信息可以作为分析问题原因及应对问题的线索。

请触摸功能按钮栏上的 `[Log]` 按钮。然后，日志窗口将出现。

![](../_assets/tp630/log/11_fb_log.PNG)

您可以查看事件日志。请触摸右侧的向上箭头图标。

![](../_assets/tp630/log/21_log.PNG)

日志的过滤选项和辅助信息如下所示；

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
        辅助信息：错误或警告发生时系统的状态也被记录，您可以在辅助信息窗口中查看。通过点击顶部的选项卡，您可以选择并查看所需的辅助信息。活动输入/输出信号值以黄色背景显示，分配的用户 I/O 以粗体显示。
        <ul>  
          <li>姿态 : 机器人，附加轴值。(单位：mm 或 deg.)</li>
          <li>S/In : 系统输入值。仅记录前 8 字节。(si0~63)</li>
          <li>S/Out : 系统输出值。仅记录前 8 字节。(so0~63)</li>
          <li>D/In : 用户输入值。仅记录 fb0 的前 32 字节。</li>(fb0.dib0~31)
          <li>D/Out : 用户输出值。仅记录 fb0 的前 32 字节。</li>(fb0.dob0~31)
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png"/>
      </td>
      <td style="text-align:left">
        您可以使用过滤按钮仅显示所需类型的日志。当过滤按钮开启时，对应的类型将显示，关闭时将隐藏。
        <ul>
          <li>[全部]：同时开启或关闭所有过滤按钮。</li>
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
              <li>另存为日志文件：事件首先存储在内存缓冲区中，当缓冲区满时，它们会自动保存到文件中。通过选择此菜单，缓冲区中仍然存在的任何日志将立即保存到文件。</li>
              <li>清除日志文件：您可以清除内存缓冲区中的日志并删除所有日志文件。（删除的文件无法恢复。）</li>
            </ul>
          </li>
          <li>[
            <img src="../_assets/bt-lock.png"/>]: 此功能锁定屏幕上新事件的显示。即使被锁定，新事件仍将继续记录；只有屏幕刷新被阻止。当日志屏幕不断更新并阻碍视野时，此功能可能会很有用。您可以再次按锁定按钮或关闭并重新打开日志窗口来解锁它。
          </li>
          <li>[
            <img src="../_assets/bt-trash.png"/>]: 这会清除屏幕上显示的事件。它只清除屏幕，而内部记录的日志不会被删除。</li>
          <li>[
            <img src="../_assets/bt-refresh.png"/>]: 当日志屏幕被清除时，按下此按钮将重新检索日志并在屏幕上显示。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c4.png"/>
      </td>
      <td style="text-align:left">这是所选类型的日志。新事件以黄色背景突出显示在顶部。</td>
    </tr>
  </tbody>
</table>
[__SOURCE](2-operation/7-user-key/README.md)
# 2.7 用户键

通过将所需功能分配给${cont_model}教导挂件屏幕上的R按钮栏中的用户按钮区域，您可以在教学机器人时方便地使用它们。
[__SOURCE](2-operation/7-user-key/1-user-key-region.md)
# 2.7.1 用户密钥区域的切换

在 ${cont_model} 教导挂件屏幕的 R 按钮栏上，触摸 `[user key]` 按钮，直到出现所需区域。然后，菜单按钮区域将切换到用户按钮区域。在用户密钥区域，密钥信号输出功能和点应用功能是默认分配和提供的。

![](../../_assets/tp630/user-bar/user-bar.png)

* 如果您在按住 `shift` 键的同时按下 `[user key]` 按钮，可以向相反方向切换区域。
  
* 密钥信号输出功能区域将保持为空，即没有注册按钮的初始状态。
[__SOURCE](2-operation/7-user-key/2-button-registration/README.md)
# 2.7.2 各区域的按钮注册

您可以通过按钮在用户按键区域注册所需的功能。
[__SOURCE](2-operation/7-user-key/2-button-registration/1-key-signal-output.md)
# 2.7.2.1 Key Signal Output Function Area

`KEY 信号输出 (Key Signal Output)` 是一个允许您将所需变量分配给 F 键并通过按钮操作将该变量的值设置为 1 或 0 的功能。 它主要用于通过操作分配了输出变量的 F 键来打开或关闭 I/O 输出信号。 （可以指定所有类型的变量，包括一般变量、别名和输出变量。）

您可以通过按 HOME 屏幕右侧的 `[R4: User Key]` 打开 `KEY 信号输出 (Key Signal Output)` 按钮。 如果没有进行设置，则所有按钮将为空。

您可以按如下方式配置按钮：

1. 打开 `KEY 信号输出 (Key Signal Output)` 按钮，轻触 `[CTRL] + [User Key]`。 `Key Signal Output Setting` 窗口将出现。

2. 设置要在按钮上显示的功能名称和选项，然后轻触 `[F7: 确定] ([F7: OK])`。

![](../../../_assets/tp630/ctrl-key-outsignal_eng.png)

* `标题 (title)`: 显示在按钮上的名称
* `on-var`: 当指定变量名称时，按钮打开时会将值 1 分配给该变量。
* `off-var`: 当指定变量名称时，按钮关闭时会将值 1 分配给该变量。
* `切换 (toggle)`:
  + Checked: 每次按下按钮时，按钮在 ON 和 OFF 之间切换。
  + Unchecked: 按下按钮时变为 ON，释放时变为 OFF。
* `自动 模式下 允许 (Permit on auto mode)`:
  + Checked: 该功能在自动模式下也能操作。
  + Unchecked: 该功能在自动模式下不操作。
* `自动 模式下 关闭 (OFF on auto mode)`: 切换到自动模式时，为此功能设置的所有变量都将被关闭。

{% hint style="info" %}
对于 `on-var` 和 `off-var`，例如，如果您输入 3.5 并按下 `[ENTER]`，则输入 fb3.do5。 如果您输入 5 并按下 `[ENTER]`，则输入 do5。 或者，您可以使用屏幕底部的 F 键 [fb]、[do] 和 [so] 输入值。
{% endhint %}

3. 打开 `KEY 信号输出 (Key Signal Output)` 按钮，并同时触摸注册的 F 键和 `[SHIFT]` 键，以确认设置已正确应用。

![](../../../_assets/tp630/rbt-userkey-keysig_eng.png)

{% hint style="info" %}
您也可以从 `[F2: 系统] - 2: 控制参数 - 2: 输入/输出信号设置 - 5: 键信号输出 ([F2: system] - 2: Control parameter - 2: Input/Output signal setting - 5: Key signal output)` 访问相同的设置屏幕。 有关更多详细信息，请参阅 "[7.3.2.8 Key Signal Output](../../../7-system/3-control-parameter/2-io-signal-setting/8-key-signal-output.md)"。
{% endhint %}
[__SOURCE](2-operation/7-user-key/2-button-registration/2-rob-appl-cfg.md)
# 2.7.2.2 机器人应用用户键配置

在 ${cont_model} 教学 pendant 屏幕的 R 按钮栏上触摸 `[user key]` 按钮，直到所需区域出现。然后，F 按钮区域将切换到机器人应用用户键区域，例如点焊条和弧焊条。

![Figure 25 用户键按钮分配](../../../_assets/tp630/user-bar/ubar-spotweld-cfg.png)

按下 `控制 (ctrl)` 键并按下 `user-key` 按钮，打开一个配置屏幕，您可以在其中调整用户按钮的布局。

屏幕底部的列表是可选择的 F 按钮列表，您可以使用 `[Arrow Up]`/`[Arrow Down]` 移动光标。

屏幕顶部是用户按钮的布局，您可以使用 `[Arrow Left]`/`[Arrow Right]` 移动光标。

按下 `[ENTER]` 键或 `[F1:选择] ([F1:Select])` 按钮将所选 F 按钮放置到所选位置。
如果按下 `[DEL]` 键或 `[F2:删除] ([F2:Delete])` 按钮，则所选位置的按钮将被删除并变为空。

完成放置后，按下 `[F7:确定] ([F7:OK])` 按钮以保存用户按钮布局。


* 有关点焊应用功能的详细信息，请参阅 "[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。

* 有关弧焊应用功能的详细信息，请参阅 "[${cont_model} 控制器弧焊功能手册](https://hrbook-hrc.web.app/#/view/doc-arc-weld/zh/README)"。
[__SOURCE](2-operation/8-coord-sys/README.md)
# 2.8 坐标系统

空间中的坐标用于确定机器人的运动方向。 ${cont_model} 控制器具有关节坐标系统、机器人坐标系统、用户坐标系统和工具坐标系统。
[__SOURCE](2-operation/8-coord-sys/1-jog-key.md)
# 2.8.1 运动键

可以在手动模式下使用。当您按住启用开关，电机开启并按下运动键时，可以以低速移动机器人。

机器人运动的方向取决于参考坐标系。在轴坐标系中，关节独立移动，而在其他坐标系中，它们会同时移动，从而使TCP可以沿选定的矩形坐标系移动。

![](../../_assets/tp630/sbar-joint-crdsys_eng.png)

![图26 教练面板运动键](../../_assets/tp630/keypad-jog_eng.png)

J7和J8键的运动由您设置的机器人模型和附加轴决定。在7轴机器人中，J7可以通过分配在R3轴（第三轴）的运动键进行操作。对于其他类型的机器人，您可以根据机制设置，通过运动键操作附加轴。

仅当选择的机制是运动 `[0]` 中选择的机器人时，如果下一个机制 `[1]` 的总轴数少于两个，它们将根据注册的附加轴的顺序进行分配。这时，如果机制 `[1]` 中仍有未分配的键，并且下一个机制在可以分配剩余轴的轴数方面有空间，它们将按顺序分配。

例如，根据附加轴的机制轴数，是否为J7和J8轴进行分配如下所示。

| 机制 `[0]` | 机制 `[1]` | 机制 `[2]` | J7轴 / J8轴的分配情况 |
| :--- | :--- | :--- | :--- |
| 6轴机器人 | 旅行轴，轴1 | 定位器，轴1 | J7: 旅行轴 / J8: 定位器 |
| 6轴机器人 | 旅行轴，轴1 | 定位器，轴2 | J7: 旅行轴 / J8: 未分配 |
| 6轴机器人 | 旅行轴，轴2 | 定位器，轴2 | J7: 旅行轴1 / J8: 旅行轴2 |
| 6轴机器人 | 旅行轴，轴3 | 定位器，轴1 | J7: 未分配 / J8: 未分配 |
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

1.	在手动模式下打开电机，并按住教学挂件背面的启用开关。

2.	通过反复触摸 ${cont_model} 教学挂件屏幕状态显示窗口上的 `[Crd. Sys]` 按钮来选择关节坐标系统。然后，手动控制条将显示每个关节的名称。

    ![](../../_assets/tp630/k-crdsys_eng.png)

    ![](../../_assets/tp630/sbar-joint-crdsys_eng.png)


3.	使用手动键操作机器人。机器人的每个关节独立移动。

    ![](../../_assets/image_85.png)

{% hint style="info" %}
有关机器人在手动键相对于的进展方向的详细信息，请参阅 "[2.8.1 手动键](./1-jog-key.md)"。
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

1. 在手动模式下打开电机，并按住教学挂件背面的启用开关。

2. 通过反复触摸${cont_model}教学挂件屏幕状态显示窗口上的`[Crd. Sys]`按钮来选择机器人坐标系统。

    ![](../../_assets/tp630/k-crdsys_eng.png)

    ![](../../_assets/tp630/sbar-robot-crdsys_eng.png)


3. 使用走动键操作机器人。机器人将如以下方式移动。

    ![](../../_assets/image_62.png)

{% hint style="info" %}
* 有关机器人相对于走动键的进程方向的详细信息，请参阅"[2.8.1 Jog Keys](1-jog-key.md)." 
* 
  如果使用右手，您可以轻松理解机器人坐标系统中的机器人操作。

  ![](../../_assets/crd-direction.png) 

图27 坐标系统方向 \(左\) / 旋转方向 \(右\)

* 如果您将右手食指的进程方向放在机器人坐标系统的X方向上，而站在机器人的背面，则拇指的进程方向变为Z方向，中指的进程方向变为Y方向。
* 如果您将右手的拇指放在旋转中心轴的方向上，则其他折叠手指的方向变为旋转方向的+方向。
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

1.	在初始屏幕的右侧，触摸`[system]`按钮 - `[2: Control Parameter - 7: Coordinate System Registration - 1: User Coordinate System]`菜单，然后注册用户坐标系统。

{% hint style="info" %}
有关如何注册用户坐标系统的详细信息，请参阅"[7.3.6.1 用户坐标系统](../../7-system/3-control-parameter/6-cordsys-reg/1-user-crdsys.md)。"
{% endhint %}

2.	在初始屏幕左下角触摸`[cond.set]`按钮，然后在`[9: Select user coordinate]`选项中设置坐标系统。您可以选择用户坐标系统，而不是笛卡尔坐标系统。

	![](../../_assets/tp630/fbt-condset_eng.png)

	![](../../_assets/tp630/cond-set-usercrd_eng.png)

3.	在教学手柄上重复按下`[crd.sys]`键或在状态栏上按下坐标系统按钮以选择用户坐标系统。

	![](../../_assets/tp630/k-crdsys_eng.png)

	![](../../_assets/tp630/sbar-user-crdsys_eng.png)


4. 使用关节键操作机器人。机器人将如下移动。	

	![](../../_assets/image_103.png)

{% hint style="info" %}
有关机器人与关节键的移动方向的详细信息，请参阅"[2.8.1 Jog Keys](1-jog-key.md)。" 
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

1. 在手动模式下开启电机，并按住教导手柄背面的使能开关。

2. 通过反复触摸 ${cont_model} 教导手柄屏幕状态显示窗口上的 `[Crd. Sys]` 按钮，选择工具坐标系统。

    ![](../../_assets/tp630/k-crdsys_eng.png)

    ![](../../_assets/tp630/sbar-tool-crdsys_eng.png)

3. 使用 jog 键操作机器人。机器人将按如下方式移动。

* 如果机器人上安装了焊炬

    ![](../../_assets/image_68.png)

* 如果机器人未安装焊炬

    ![](../../_assets/image_92.png)

{% hint style="info" %}
有关机器人在 jog 键相关的运动方向的详细信息，请参阅 "[2.8.1 Jog Keys](1-jog-key.md)."
{% endhint %}
[__SOURCE](2-operation/8-coord-sys/6-align-crdaxis.md)
# 2.8.6 坐标轴对齐

此功能在保持XYZ位置固定的情况下，将TCP坐标系与选定坐标系的轴对齐。

![](../../_assets/tp630/align-crd-axis-example_eng.png)

对齐分为两个步骤：
* 轴对齐（步骤1）：在此步骤中，工具的Z轴与选定坐标系对齐。
* 坐标系对齐（步骤2）：完成轴对齐（步骤1）后，TCP坐标系调整为与选定坐标系正交。
* 返回原始位置：当进入此功能时，将机器人移回初始位置。无论对齐步骤是否完成，都会执行返回。

坐标轴对齐的流程
1.  在移动到期望位置后，确保：
    * 机器人已停止
    * 电机已打开
    * 系统处于手动模式

2. 按下教导终端上的 **`[Ctrl]`** 按钮和 `[crd.sys]`，或通过R300进入坐标轴对齐屏幕。

3. 选择要对齐的坐标系。

4. 按下期望轴方向的移动键以对齐工具的Z轴。（步骤1）

5. 在完成轴对齐（步骤1）后，按下与先前选择的轴相对应的旋转方向键以执行坐标对齐。（步骤2 - 可选）

6. 一旦达到期望位置，按下 `[ESC]` 键以退出坐标轴对齐屏幕。

![](../../_assets/tp630/align-crd-axis_eng.png)

移动键功能摘要
  - 轴对齐：+X, +Y, +Z 键
  - 返回原始位置：-X, -Y, -Z 键
  - 坐标对齐：与Z轴对齐时选定轴相对应的旋转方向键（+Rx, +Ry, +Rz）

{% hint style="info" %}
* 当坐标轴对齐窗口处于活动状态时，移动功能被禁用。
* 坐标对齐仅在完成轴对齐后可用。
* 一旦工具Z轴对齐完成，按下移动按钮将保持当前位置信息。
* 对齐是在避免软限制的方向上执行。如果不存在有效路径，将显示超出软限制的错误。（如果期望路径为顺时针但导致软限制，则系统将改为逆时针旋转。）
* 当选择基座、机器人或用户坐标系时，移动将遵循所选择的坐标系作为参考。
{% endhint %}

{% hint style="warning" %}
* 此功能仅在机器人停止且处于手动模式时执行。
（无法在自动模式下执行。）
* 如果在按住移动键时按下 `[ESC]` 键，弹出窗口将关闭，并重新启用移动。操作时请谨慎。
* 如果附加轴设置为基座且X、Y、Z未定义（未定义状态），将显示错误日志。
* 如果期望的对齐方向即使在移动时也无法到达，将出现指示无法到达XYZ位置的错误消息。
* 如果尝试再次在不可插值的姿势下进行对齐，将发生错误。在这种情况下，请按返回原始位置键以避免问题区域并重试。
* 在奇点处对齐时，再次按下释放按钮将继续运动。由于路径从当前位点重新计算，因此以正常速度运行。（速度略微增加，但这是正常速度。）
{% endhint %}
[__SOURCE](2-operation/9-axis-origin.md)
# 2.9 轴原点和工具长度的优化

您可以使轴整型和工具长度自动设置，从而提高线性插补轨迹和坐标偏移的准确性。

* 您可以使难以在 3D 中测量的工具提示到工具的距离自动设置。需要校准的参数是 H、V、R2 和 B 轴的轴原点以及 X、Y 和 Z 方向的工具长度。
* 您可以执行“轴原点和工具长度”的“优化”和“工具长度”。

{% hint style="info" %}
* 从版本 V70.02-00 开始，轴原点优化功能将不再支持一般用户。如果您希望在后续版本中更改轴原点，请联系客户支持团队咨询专家或工程师。
{% endhint %}


{% hint style="warning" %}
您应该在教导机器人程序之前优化“轴原点和工具长度”。如果在已创建机器人程序时优化“轴原点和工具长度”，现有程序中的位置可能会改变。
{% endhint %}

以下显示了如何设置轴原点和工具长度的优化：

1. 使用教导盘上的模式开关将操作模式设置为手动模式。

2. 在 JOB 程序窗口中，按下 `[PROG]` 键和 `[SHIFT]`，输入程序编号，然后按下 `[Enter]` 按钮。


    ![](../_assets/tp630/k-prog-step_eng.png)

    ![](../_assets/tp630/dlg-prog-sel_eng.png)


3. 按下教导盘上的 `[motor]` 键，电动机灯将闪烁。

* 如果电动机未开启，请检查日志栏上的错误信息并解决故障。

4. 在按住教导盘背面的使能开关的同时，使用 jog 键操作机器人。

5. 在机器人操作范围内的任意位置放置一个尖针，然后将机器人的工具提示与其对齐。机器人前端与匹配工具提示之间的距离将被优化。

6. 通过按下键盘上的 `[REC]` 键记录步骤。

    ![](../_assets/tp630/k-record_eng.png)


7. 改变机器人的姿势，并重复步骤 5-6 超过四次。

* 尽量使用所有六个轴来改变机器人的姿势。此外，轴角度至少改变 30 度。

8. 按下 `[system]` 按钮 - `[6: Auto Calibration - 1: Optimize axis origin and tool length] ([6: Auto Calibration  - 1: Optimize axis origin and tool length])` 菜单。

    ![](../_assets/tp630/menu-axis-origin-tool-opt_eng.png)


9. 设置为自动校准而创建的程序编号、工具编号和步骤位置误差允许范围，然后按下 `[Execute]` 按钮。然后选定的轴原点和工具长度将被设置。

    ![](../_assets/tp630/axis-origin-tool-opt_eng.png)

* 当您使用多个工具时，您应该在第二个工具的 `[Optimization Selection]` 选项中选择工具长度。如果选择轴原点和工具长度，先前设置的工具信息将会不正确。

{% hint style="info" %}
有关此功能的详细信息，请参阅“[7.7.1 轴原点和工具长度的优化](../7-system/7-auto-calibration/1-axis-origin-tool-length-optimization.md)。”
{% endhint %}
[__SOURCE](2-operation/10-tool-data-auto-calib.md)
# 2.10 工具数据自动校准

在通过自动校准等确定轴原点和工具长度后，如果工具变形，可以简单地确定新的工具数据。此时，轴原点应已确定并保持。此外，应在工具长度确定和角度校准完成后教授固定参考点。如果发生工具变形，将工具放置在变形之前指定的参考点的相同位置，然后执行自动工具数据校准。

1. 触摸 `[system]` 按钮 - `[3: Robot Parameter - 1: Tool Data]` 菜单。

    ![](../_assets/tp630/menu-tool-data_eng.png)

2. 触摸 `[Auto Calibration]` 按钮后，使用操作键将工具提示移动到原始位置。

    ![](../_assets/tp630/tool-data-auto-calib_eng.png)

3. 在检查预定参考点的程序编号、步骤编号和工具编号后，触摸 `[Execute]` 按钮。

    ![](../_assets/tp630/tool-data-auto-calib2_eng.png)


{% hint style="info" %}
有关此功能的详细信息，请参阅 "[7.4.1 Tool Data](../7-system/4-robot-parameter/1-tool-data/README.md)."
{% endhint %}
[__SOURCE](3-programming/README.md)
# 3. 程序编写

您可以编写和管理程序，以便机器人能够执行工作并达到预期的结果。
[__SOURCE](3-programming/1-prog-manage.md)
# 3.1 程序管理

当机器人停止时，您可以创建、修改和删除程序。

1. 在 JOB 程序窗口中，按 <SHIFT> 的 `[PROG]` 键。然后，程序选择窗口将出现。

    ![](../_assets/tp630/k-prog-step_eng.png)

2. 您可以创建、修改和删除程序。

* 要添加新程序，请输入新的程序编号并按 <ENTER> 键，参照 "[3.2 程序编写](2-prog-edif/../2-prog-edit/README.md)"。

    ![](../_assets/tp630/k-prg-select_eng.png)

* 要打开程序以检查和修改其内容，请输入程序编号，或从列表中选择程序，然后按 `[OK]` 按钮。然后，所选程序将在 JOB 程序窗口中打开。

* 要删除程序，从列表中选择程序并按 \<DEL> 键。

* 您还可以从文件列表中删除程序 \(`服务 - 5: 文件管理 (service  - 5: File Management)`\)。有关详细信息，请参见 "[4.2.1 文件管理](../4-service/2-file-manager/1-file-management.md)"。

* 您可以使用 R 代码 \(R117\) 快速删除程序。有关详细信息，请参阅 "[8.4 R117 删除程序](../8-r-code/4-r117.md)"。
[__SOURCE](3-programming/2-prog-edit/README.md)
# 3.2 程序编写

为了实现您的应用程序的目的，您可以编写和编辑由各种语句组成的程序，指示机器人操作。您可以在手动模式下编写程序。
[__SOURCE](3-programming/2-prog-edit/1-statement.md)
# 3.2.1 语句

一个通用程序由一个步骤命令组成，该命令指示机器人移动，以及一个功能命令，该命令指示机器人在移动后执行工作。

语句主要分为命令和参数，参数是额外项。参数分为对语句至关重要的默认参数和可以省略的可选参数。

![](../../_assets/image_82.png)



| No. | 描述 | No. | 描述 |
| :--- | :--- | :--- | :--- |
| ![](../../_assets/c1.png)  | 步骤编号 | ![](../../_assets/c3.png)  | 参数 |
| ![](../../_assets/c2.png)  | 命令 | ![](../../_assets/c4.png)  | 注释 |

{% hint style="info" %}
有关参数的详细信息，请参阅 "[2.3.1 步骤语句参数](../../2-operation/3-step/1-step-cmd-param/README.md)。"
{% endhint %}

当您输入语句时，基本设置值将自动输入到默认参数中，并可以更改。可选参数用符号 \( \_ \) 标记，您可以通过选择参数输入参数值。此外，可以输入的参数将在功能按钮栏上显示为按钮。

![图 27 编辑命令 - 输入参数值](../../_assets/tp630/pane-prog-move-option.png)

在编辑命令参数时，您可以使用教导挂件上的操作键和屏幕底部的菜单按钮，或者使用软键盘编辑变量、表达式和字符串。
[__SOURCE](3-programming/2-prog-edit/2-statement-input/README.md)
# 3.2.2 声明输入
[__SOURCE](3-programming/2-prog-edit/2-statement-input/1-gen-statement-input.md)
# 3.2.2.1 一般语句输入

1. 在手动模式下，触摸初始屏幕右下角的`[cmd.input]`按钮。然后，命令输入窗口将出现。

    ![](../../../_assets/tp630/sbt-cmd_eng.png)

2. 触摸语句组，然后从列表中选择命令。语句将立即插入到当前光标位置下方。

    ![](../../../_assets/tp630/sbt-cmd-list_eng.png)

* 如果命令列表中的命令超过七个，可以通过触摸[prev/next]按钮查看额外的命令。

* 有关每个语句的详细信息，请参阅"[${cont_model} Robot Language Function Manual](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/README)。"
[__SOURCE](3-programming/2-prog-edit/2-statement-input/2-step-input.md)
# 3.2.2.2 输入带有隐藏姿势的步骤语句

要将机器人的当前姿势输入为移动命令，请按下键盘上的`[REC]`键。



![](../../../_assets/tp630/k-record_eng.png)

当您使用`[REC]`键输入命令时，姿势变量不会出现在步骤中，与一般命令输入模式不同，因此称为隐藏姿势。
[__SOURCE](3-programming/2-prog-edit/2-statement-input/3-rec-cond.md)
# 3.2.2.3 记录条件

当使用 `[REC]` 键输入语句时，机器人的当前姿态将被记录为目标姿态，并且通过 `[rec.cond]` 按钮提前设置的值将应用于移动命令 \(move\) 参数。以下显示了设置语句记录条件的方法。

1. 在 ${cont_model} 教 pendant 屏幕左侧触摸 `[rec.cond.]` 按钮。然后，将出现记录条件设置窗口。

    ![](../../../_assets/tp630/lbt-record_eng.png)

2. 设置插值、移动速度和单位、精度以及工具编号后，触摸 `[check]` 按钮 \(![](../../../_assets/icon-ok.png)\)。

    ![](../../../_assets/tp630/lbt-record-edit_eng.png)

* 当进行位置记录时，移动语句将根据记录条件设置进行记录。
* 在机制集设置中，可以指定在进行位置记录时要存储的机制配置。

    * 如果短暂触摸 `[mechsets]` 按钮，预定义的机制集编号将依次出现。
    * 如果长按 `[mechsets]` 按钮，可以在机制集设置窗口中修改现有集配置，或通过使用 `[+]` 或 `[-]` 按钮添加或删除机制集。

        ![](../../../_assets/tp630/pop-mechanism_eng.png)
[__SOURCE](3-programming/2-prog-edit/3-statement-constitution.md)
# 3.2.3 语句配置

一个语句由地址区域和语句区域组成。 

![Figure 28 Areas Comprising a Statement](../../_assets/tp630/pane-prog-section.png)

| No. | Area | Description |
| :--- | :--- | :--- |
| ![](../../_assets/c1.png) | 地址区域 | 显示行号 \(1 到 9999\) 和步骤号 \(S1 到 S999\) |
| ![](../../_assets/c2.png) | 语句区域 | 显示语句 |

您可以通过按下 `[←/→]` 键在地址区域和语句区域之间移动光标位置。按下 `[↓/↑]` 键将允许您在所选区域的行之间上下移动光标。

![Figure 29 Moving the Cursor Between Areas \(Left: Address Area. Right: Statement Area\)](../../_assets/tp630/pane-prog-sectionchng.png)
[__SOURCE](3-programming/2-prog-edit/4-statement-edit/README.md)
# 3.2.4 语句编辑

您可以使用教学挂件上的操作键和功能按钮栏上的菜单按钮在作业程序窗口中编辑语句。使用软键盘，您可以编辑变量、表达式和字符串。

在语句区域，您可以通过根据所选对象切换光标的状态来检查和编辑语句。

* 语句光标状态：当整行语句被选中时，您可以检查语句。

    ![](../../../_assets/tp630/pane-prog-cmd-edit.png)

* 单词光标状态：当单个参数被选中时，您可以检查和编辑语句。

    ![](../../../_assets/tp630/pane-prog-cmd-edit1.png)
[__SOURCE](3-programming/2-prog-edit/4-statement-edit/1-how-to-edit-statement.md)
# 3.2.4.1 声明编辑方法

以下显示如何编辑声明。

1.	在JOB程序窗口中，通过按下`[↑/↓]`键选择声明区域。当处于声明光标状态时，声明区域将被选中。

2.	在声明光标状态下，按下`[ENTER]`键。然后，将切换到声明光标状态，选择一个参数，所选参数值将出现在屏幕底部的输入区域。

3.	使用教学挂件上的操作键和屏幕的菜单按钮编辑参数值。

* 按下`[←/→]`键可以让您在参数之间向左或向右移动光标
* 可以输入的参数将显示为功能按钮栏上的按钮。您可以通过选择所需的按钮轻松输入参数。
* 您可以使用软键盘编辑变量、表达式和字符串。

4.	按下`[ENTER]`键。然后，更改的内容将被应用，允许声明的参数值被更改，光标将移动到下一个参数。

* 要取消更改，请按下`[ESC]`键。

5.	您可以通过重复上述步骤2-3来编辑另一个参数。

6.	按下`[ENTER]`键以完成编辑。更改将保存在JOB程序中，光标将返回到声明光标状态。
[__SOURCE](3-programming/2-prog-edit/4-statement-edit/2-statement-edit-example.md)
# 3.2.4.2 编辑语句的示例

以将插值参数从 P \(关节插值\) 更改为 L \(线性插值\) 的示例，以下描述了如何编辑语句。

1. 在语句光标状态下，按下 `[ENTER]` 键。然后，语句光标将变为单词光标状态，允许选择 P \(关节插值\)，这是移动语句的插值参数。在输入区域，将显示当前插值设置值 P，屏幕的功能按钮栏上将显示可以输入的插值参数作为按钮。

    ![](../../../_assets/tp630/pane-prog-move-P.png)

2. 在功能按钮栏中触摸 `[L]` 按钮。然后，输入区域将显示 L \(线性插值\)。

    ![](../../../_assets/tp630/pane-prog-move-L.png)

3. 按下 `[ENTER]` 键。语句的插值参数将更改为 L，然后光标将移动到下一个参数，允许选择移动速度。

    ![](../../../_assets/tp630/pane-prog-move-spd.png)

4. 按下 `[ENTER]` 键以完成编辑。更改的内容将保存在 JOB 程序中，然后光标将返回到语句光标状态。
[__SOURCE](3-programming/2-prog-edit/4-statement-edit/3-how-to-edit-line-no.md)
# 3.2.4.3 行号编辑方法

行号可以设置为1到9999之间的任何数字。

1. 在JOB程序窗口中，通过按下`[←/→]`键选择地址区域。然后，将选择地址区域。

* 如果光标在语句区域处于语句光标状态，请按`[←]`键将光标移动到地址区域。

    ![](../../../_assets/tp630/pane-prog-linenum.png)

2. 在地址区域，通过按下`[↓/↑]`键选择一行，然后编辑行号。

* 要输入行号，请使用数字键在输入区域中输入行号。

    ![](../../../_assets/tp630/pane-prog-linenum1.png)

* 要删除行号，请按`[BS]`键。然后，行号的地址值将从输入区域中删除。

3. 按`[ENTER]`键完成编辑。更改的内容将保存在JOB程序中。

    ![](../../../_assets/tp630/pane-prog-linenum2.png)
[__SOURCE](3-programming/2-prog-edit/4-statement-edit/4-softkeyboard.md)
# 3.2.4.4 软件键盘

您可以通过 ${cont_model} 教学挂架屏幕上的软件键盘轻松输入变量、表达式和字符串。

1.	触摸 ${cont_model} 教学挂架屏幕日志栏上的 ![](../../../_assets/tp630/rbt-softkb_eng.png ) 按钮。然后，屏幕底部将出现软件键盘。

2.	您可以在输入区使用软件键盘输入变量、表达式和字符串。现有的参数值将被移除，输入的文本将显示出来。

    ![](../../../_assets/tp630/rbt-softkb-prog_eng.png)

* 如果您触摸输入区域左侧的 ![](../../../_assets/bt-cursor-left.png)/![](../../../_assets/bt-cursor-right.png) 按钮，您可以移动光标位置，从而在所需位置插入文本。

* 您可以通过触摸 ![](../../../_assets/bt-lang.png) 按钮来更改输入语言。

* 您可以通过按住 `[SHIFT]` 键的同时触摸按键输入大写字母或符号。

* 您可以通过触摸 ![](../../../_assets/tp630/bt-dock-softkb_eng.png) 按钮将键盘移动到屏幕顶部。

3.	完成文本编辑后，您可以通过按 `[ENTER]` 键隐藏软件键盘。
[__SOURCE](3-programming/2-prog-edit/4-statement-edit/5-block-edit-mode.md)
# 3.2.4.5 块编辑模式

您可以将程序的单行或多行设置为块，以执行复制、移动、删除和备注操作。
<br>

#### 1. 进入块编辑模式

在作业编辑面板中，使用左箭头键将光标移动到地址区域。
单击 `F2: Blk.edit` 按钮进入块编辑模式，光标将变为灰色。

![](../../../_assets/tp630/blockedit/11_blockeditmode2.PNG)
![](../../../_assets/tp630/blockedit/12_blockeditmode.PNG)
<br><br>

#### 2. 设置块

使用上下箭头键将光标移动到块的起始位置，然后按 `确认 (ENTER)` 键。接着，使用上下箭头键将光标移动到块的结束位置，并再次按 `确认 (ENTER)`。选定的块将以蓝色背景高亮显示。

![](../../../_assets/tp630/blockedit/20_set_block.PNG)

（如果在不移开光标的情况下执行复制或删除等操作，则不需要第二次按 `确认 (ENTER)`。）
<br><br>

#### 3. 复制

在块被选中时，单击 `F2: copy` 将内容复制到剪贴板。
或者，您可以在不选择块的情况下单击 `F2: copy` 仅复制一行。
<br><br>

#### 4. 粘贴

使用上下箭头键将光标移动到您希望粘贴的位置上方的行，然后单击 `F3: paste`。
例如，如果您希望将复制的块粘贴在 S1 中的 `delay 1` 语句下方，请将光标放在 `delay 1` 上，然后单击 `F3: paste`。

![](../../../_assets/tp630/blockedit/30_paste.PNG)
![](../../../_assets/tp630/blockedit/32_paste.PNG)
<br><br>

#### 5. 剪切

当选择块时，单击 `F1: cut` 将使块呈现浅灰色，表示该块已被剪切。  
或者，您可以在不选择块的情况下单击 `F1: cut` 来剪切一行。

![](../../../_assets/tp630/blockedit/40_cut.PNG)

粘贴剪切块的方法与上述描述相同。
<br><br>

#### 6. 删除
当选择块时，单击 `F4: delete` 然后确认 `删除吗？ (Delete?)` 提示将删除该块。  
或者，您可以在不选择块的情况下单击 `F4: delete` 来删除一行。

 ![](../../../_assets/tp630/blockedit/50_delete.PNG)
<br><br>

#### 7. 备注、取消备注

此功能用于暂时禁用作业程序中特定部分的执行而不删除它。  
当选择块并单击 `F5: remark` 时，块内的语句将被注释掉（备注）。
当选择块并单击 `F6: unremark` 时，注释将被移除（取消备注）。  
此外，您可以在不选择块的情况下注释或取消注释一行。

{% hint style="info" %}
- 小于版本 V60.30-00 : 步骤未被备注。
- 版本 V60.30-00 及更高版本 : 步骤也被备注。
{% endhint %}

 ![](../../../_assets/tp630/blockedit/60_remark.PNG)
<br><br>


#### 8. 自动注释 / 移除注释

（此功能支持从版本 V70.02-00 及以后的版本。）

- 按 `[R5: Prev/next]` 按钮以显示 `[F1: 自动注释] ([F1: auto comment])` 和 `[F2: 取消注释] ([F2: uncomment])` 按钮。

- 当您按 `[F1: 自动注释] ([F1: auto comment])` 时，已注册的数据注释会自动插入到选定语句上。

  * 有关如何配置数据注释，请参见 [4.11 data comment](../../../4-service/11-data-cmts.md)。

  * 有关应用条件，请参阅 [4.3.9 Statement data comment](../../../4-service/3-program-conversion/9-stmt-comment.md) 部分。

- 当您按 `[F2: uncomments]` 时，所选语句的注释将被移除（无论是否注册数据）。

![](../../../_assets/tp630/blockedit/66_auto_comment.PNG)


#### 9. 关闭块编辑模式

可以通过单击 `F7: close` 或按 `ESC` 键来关闭块编辑模式。
<br><br>


----

#### 自动调整步骤 #

例如，如果步骤 S1-S2 被复制并粘贴在下面，原本在 S3 的 `移动 (move)` 语句将由于插入的 2 步而被向下推，并重新编号为 S5。

在这种情况下，所有在同一作业中的跳转语句，例如 `goto`、`gosub`、`如果 (if)` 语句，以及 `等待 (wait)` 语句的目标地址的超时地址将会自动调整，从 S3 变为 S5。

例如，在下面的示例中，条件跳转语句 `if di45==0 then S3` 将被更新为 S5，以确保它仍然跳转到与之前相同的 `移动 (move)` 语句。

![](../../../_assets/tp630/blockedit/71_branch_adjust.PNG)
![](../../../_assets/tp630/blockedit/72_branch_adjust.PNG)

这种自动步号调整适用于向前或向后移动步号的操作，例如记录、删除和块编辑。

{% hint style="info" %}
以下规格适用于版本 V60.30-00 及更高版本。
{% endhint %}

如果由于删除或备注而移除目标步骤，则将其调整为 `deleted_step#` 或 `remarked_step#`，如下所示。  
请手动将这些修改的目标地址调整为适当的步骤号码（或行号/标签）。
（如果不作更改，执行语句时将发生语法错误。）

![](../../../_assets/tp630/blockedit/76_branch_adjust.PNG)
[__SOURCE](4-service/README.md)
# 4. 服务

您可以使用程序的各种服务功能菜单，例如变量和文件管理。
[__SOURCE](4-service/1-service-usage.md)
# 4.1 服务的使用

1. 在手动或自动模式下，触摸初始屏幕功能按钮栏上的 `[service]` 按钮。程序的各种服务菜单将会显示。

2. 选择所需的菜单将使您能够管理文件、程序、示教器或检查机器人系统的状态。

    ![](../_assets/tp630/svc-list.png)


* `4: 数据注释 (4: Data comment)`: 您可以管理输入/输出变量、继电器和各种其他变量的注释。
* `5: 文件管理器 (5: File Manager)`: 您可以管理主板内部存储器、示教器或可移动存储设备中的文件。
* `6: Program Conversion`: 您可以按批次或单独转换已创建程序的条件和位置等数据。
* `7: System Diagnosis`: 您可以检查机器人和控制器的状态并更新系统版本。
* `8: 日期，时间设置 (8: Date, time setting)`: 您可以设置控制器的日期和时间。
* `9: 退出TP应用程序 (9: Exit TP application)`: 退出 TP（示教器）应用程序。
* `10: 应用程序(App) (10: App)`: 管理安装和运行在示教器上的软件。
* `11: 示教器选项 (11: Teach pendant option)`: 设置示教器的声音和屏幕保护时间。
* `12: 示教器共享 (12: Teach pendant sharing)`: 将示教器连接到多个控制器或 HRSpace4 中的虚拟控制器。
* `14: 系统程序 (14: System program)`: 您可以查看和移除安装在控制器上的系统程序（例如，OPC-UA 服务器）。
* `19: 工业通信监控 (19: Industrial Communication Monitoring)`: 监控固件信息和通信状态。
[__SOURCE](4-service/2-file-manager/README.md)
# 4.2 文件管理

您可以管理主板的内部存储、教学挂件或可移动存储设备中的文件。

1. 触摸`[5: 文件管理]`菜单。然后，将显示各设备的文件夹列表以及所选文件夹中保存的文件列表。

2. 按设备检查和管理文件夹结构和保存的文件。

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
        <p>这是主板内部存储、教学挂件和可移动存储设备中的文件夹列表。您可以检查文件夹结构。</p>
        <ul>
          <li>[<img src="../../_assets/icon-mb.png" alt/>主板]: 保存于主板 (M/B) 的文件将用于实际的机器人操作。</li>
          <li>[<img src="../../_assets/icon-tp.png" alt/>教学挂件] / [<img src="../../_assets/icon-usb.png" alt/>USB]: 教学挂件 (T/P) 和可移动存储设备 (USB) 将用于数据备份。[</b> <img src="../../_assets/icon-usb.png"
            alt/><b>USB]</b> 文件夹仅在可移动存储设备连接到教学挂件时出现。</li>
          <li>您可以通过旋转教学挂件上的 jog 旋钮在文件夹列表中移动光标。</li>
          <li>如果您在文件夹列表中选择<img src="../../_assets/icon-gt.png" alt/>或[
            <img src="../../_assets/icon-wedge.png" alt/>]并按下<b>`[ENTER]`</b>键，您可以显示或隐藏子文件夹。</li>
          <li>当您选择一个文件夹时，可以检查文件夹中保存的文件列表。</li>
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
* 这是R代码中“R17 文件管理”的相同功能。
* 当可移动存储设备连接到教学挂件时，`[USB]`图标 \(![](../../_assets/icon-usb2.png)\) 将出现在 ${cont_model} 教学挂件屏幕的状态栏上。
{% endhint %}

{% hint style="warning" %}
在执行复制或删除文件等操作时，请勿从教学挂件中移除可移动存储设备。数据可能会损坏。
{% endhint %}
[__SOURCE](4-service/2-file-manager/1-file-management.md)
# 4.2.1 文件管理

选择一个或多个文件进行复制、移动或删除。

1. 使用教学手柄上的 Jog Dial 选择文件夹列表中的一个文件夹。将出现选定文件夹中保存的文件列表。

    ![](../../_assets/tp630/file-manager/fl-folder-select_eng.png)

2. 通过触摸文件列表中的所需文件进行选择。

    ![](../../_assets/tp630/file-manager/fl-file-select_eng.png)

* 您可以按住 `[CTRL]` 键逐个选择多个文件。
* 如果您在按住 `[SHIFT]` 键时触摸两个文件，可以一次性选择这两个文件之间的所有文件。
* 如果您在屏幕功能按钮栏上触摸 `[Select All]` 按钮，可以一次性选择所有文件。

  按 `[ESC]` 键取消文件选择。

3. 您可以使用屏幕功能按钮栏上的功能按钮复制、移动或删除选定的文件。

* `[Copy]`：复制所选文件并保存到临时文件夹，以便可以粘贴到另一个文件夹中。
* `[Paste]`：您可以将保存在剪贴板中的文件粘贴到所需文件夹。
* `[Cut]`：您可以剪切所选文件并保存到临时文件夹，以便可以粘贴到另一个文件夹中。
* `[Delete]`：您可以删除所选文件。受保护的文件（在属性中带有保护标记 \(W\_\)）无法被删除。

4. 要将文件粘贴到文件夹中，使用 Jog Dial 选择文件夹，然后触摸 `[Paste]` 按钮。然后，文件将粘贴到所选文件夹中。

    ![](../../_assets/tp630/file-manager/fl-copy_eng.png)

* 如果所选文件夹中有文件名称重复，将出现重复通知窗口。通过设置是否覆盖来处理。

    ![](../../_assets/tp630/file-manager/fl-copy-pop_eng.png)

* 要删除文件，触摸 `[Delete]` 按钮，然后在确认窗口中触摸 `[ENTER]` 按钮。

    ![](../../_assets/tp630/file-manager/fl-delete-pop_eng.png)
[__SOURCE](4-service/2-file-manager/2-rename-file-folder.md)
# 4.2.2 文件和文件夹重命名

您可以重命名文件或文件夹。您还可以一次重命名多个文件或文件夹。

1. 在文件（或文件夹）列表中触摸所需的文件（或文件夹）以选择它，然后触摸屏幕功能按钮栏上的 `[rename]` 按钮。

    ![](../../_assets/tp630/file-manager/fld-rename-select_eng.png)

2. 在输入区域输入文件（或文件夹）名称。

    ![](../../_assets/tp630/file-manager/fld-rename_eng.png)

* 您可以通过使用教学挂件上的操作键简单输入数字。 (`[←/→]` 键：用于移动光标。数字键：用于输入数字)
* 要输入包含数字的文本，请触摸日志栏上的 ![](../../_assets/tp630/rbt-softkb_eng.png) 按钮以使用软键盘。

3. 按 `[ENTER]` 键。然后，您在列表中输入的新名称将出现。

{% hint style="info" %}
* 您还可以重命名受保护的文件。
* 
  即使文件被重命名，大小、修改日期和属性等信息也将保持不变。

* 
  这是与 R 代码的 "R116 程序编号更改" 相同的功能。

{% endhint %}
[__SOURCE](4-service/2-file-manager/3-folder-management/README.md)
# 4.2.3 文件管理

您可以删除一个文件夹或添加一个新的。
[__SOURCE](4-service/2-file-manager/3-folder-management/1-folder-removal.md)
# 4.2.3.1 文件删除

1.	使用教学挂件上的 jog dial 选择文件夹列表中的一个文件夹，然后触摸键盘上的 ![](../../../_assets/tp630/k-delete_eng.png) 键。

    ![](../../../_assets/tp630/file-manager/fld-delete.png)

2.	在确认窗口中，触摸 `[ENTER]` 按钮。所选文件夹及其保存的所有文件将被删除。

    ![](../../../_assets/tp630/file-manager/fld-delete-pop_eng.png)
[__SOURCE](4-service/2-file-manager/3-folder-management/2-folder-generation.md)
# 4.2.3.2 文件夹创建

1. 使用教学挂件的 jog dial 在文件夹列表中选择一个文件夹，然后点击功能按钮栏上的 `[New Folder]` 按钮。然后，一个新文件夹将被添加到选择的文件夹下。

    ![](../../../_assets/tp630/file-manager/fld-create_eng.png)

2. 输入新文件夹的名称，然后按 `[ENTER]` 键。

    ![](../../../_assets/tp630/file-manager/fld-create-rename_eng.png)
[__SOURCE](4-service/2-file-manager/4-file-protect.md)
# 4.2.4 文件保护

通过执行可以使更改或删除程序变得不可能的设置来保护您的重要文件。

1. 选择文件并点击 `[property]` 按钮。然后，属性设置窗口将出现。

    ![](../../_assets/tp630/file-manager/fl-attribute_eng.png)

2. 检查文件名并点击 `[Read Only]` 复选框以选择它，然后点击 `[OK]` 按钮。保护标记 \(W\_\) 将出现在文件列表的属性中。

    ![](../../_assets/tp630/file-manager/fl-attribute-pop_eng.png)
[__SOURCE](4-service/2-file-manager/5-data-backup.md)
# 4.2.5 备份所有

您可以备份控制器的文件，例如项目、日志。

1. 在教导操作面板\(T/P\)或USB存储设备的文件夹树中，使用教导操作面板上的方向键选择您想要保存备份的目标文件夹。

    ![](../../_assets/tp630/file-manager/fl-backup-select.png)

2. 按下 `SHIFT` 键，然后点击屏幕底部的 `[backup all]` 按钮。

    ![](../../_assets/tp630/file-manager/fl-backup-button.png)

3. 点击 'Start' 按钮以 ` (start)` 备份。一旦备份（大约 1 分钟）完成，请在结果窗口中检查备份结果。

    ![](../../_assets/tp630/file-manager/fl-backup-pop.png)
[__SOURCE](4-service/2-file-manager/6-data-restore.md)
# 4.2.6 恢复所有

您可以将使用 `全部备份 (backup all)` 功能备份的项目、日志等文件恢复到系统中。

1. 在教导手柄\(T/P\)或可移动存储\(USB\)的文件夹列表中，使用教导手柄上的方向键选择您备份的文件夹。

    ![](../../_assets/tp630/file-manager/fl-backup-select.png)

2. 按下 `SHIFT` 键并点击屏幕底部的 `全部恢复 (restore all)` 按钮。

    ![](../../_assets/tp630/file-manager/fl-restore-button.png)

3. 点击 `开始 (Start)` 按钮以开始恢复。一旦恢复（大约需要 1 分钟）完成，请在结果窗口中检查恢复结果。

    ![](../../_assets/tp630/file-manager/fl-restore-report.png)

4. 关闭控制器的电源，然后再重新打开。
[__SOURCE](4-service/2-file-manager/7-data-restore-partial.md)
# 4.2.7 部分恢复

当仅恢复备份数据的某些文件夹或文件时，请使用 `复制 (Copy)` 和 `粘贴 (Paste)` 功能。

1. 使用操作面板的 jog dial，选择在操作面板 \(T/P\) 或可移动存储设备 \(USB\) 中备份的项目 \(project/\) 文件夹，然后点击 `[copy]` 按钮。

    ![](../../_assets/tp630/file-manager/fl-restore-copy_eng.png)

2. 使用操作面板的 jog dial，选择文件夹列表中的 `[MAIN]` 文件夹，然后触摸 `[Paste]` 按钮。

    ![](../../_assets/tp630/file-manager/fl-restore-paste_eng.png)

3. 在重复通知窗口中，触摸 `[All]` 的复选框以选择它，然后触摸 `[OK]` 按钮。备份数据将恢复到主板上。

    ![](../../_assets/tp630/file-manager/fl-restore-pop_eng.png)

4. 重新开启控制器的电源。
[__SOURCE](4-service/2-file-manager/8-toggle-root.md)
# 4.2.8 切换根目录

{% hint style="info" %}
支持从 V60.26-00 开始。
{% endhint %}

在文件管理器左侧的树形窗口中，MAIN 和 TP 节点仅显示用户允许访问的主文件夹。主文件夹外的区域是系统文件夹，用户不应访问。

如果在维护期间必需，您可以点击屏幕底部的 `[toggle root]` 按钮以进入系统文件夹可访问模式。

一旦进入可访问模式，将显示以下警告信息，MAIN 和 TP 节点显示系统的根文件夹。

![](../../_assets/tp630/file-manager/fl-toggle-root0.png)

![](../../_assets/tp630/file-manager/fl-toggle-root1.png)

再次点击 `[toggle root]` 按钮以释放可访问模式。
[__SOURCE](4-service/2-file-manager/9-tp-backup.md)
# 4.2.9 导入自动备份

导入在系统 - 自动备份和恢复中配置的自动备份。

1. 在文件管理器屏幕上，导航至 \(T/P\) 项下的 backup/ts，并使用教导挂件的箭头键选择要导入的备份文件夹。

![](../../_assets/tp630/file-manager/fl-autobackup-copy-select_eng.png)

2. 点击 `[F2: 复制] ([F2: copy])` 按钮以复制备份。 （这可能需要大约 3 分钟。）

![](../../_assets/tp630/file-manager/fl-autobackup-copy-button_eng.png)

3. 从文件夹列表中，使用教导挂件的箭头键选择可移动存储设备 (USB) 上的目标文件夹。

![](../../_assets/tp630/file-manager/fl-autobackup-paste-select_eng.png)

4. 点击 `[F3: 粘贴] ([F3: paste])` 按钮将备份传输到存储设备 (USB)。

![](../../_assets/tp630/file-manager/fl-autobackup-paste-button_eng.png)

5. 完成后，在文件管理器屏幕上验证结果。

![](../../_assets/tp630/file-manager/fl-autobackup-paste-done_eng.png)
[__SOURCE](4-service/3-program-conversion/README.md)
# 4.3 程序转换

您可以通过批量或单独修改创建程序的条件和位置，或通过移动坐标来编写新程序。

1.	触摸 `[6: 程序转换]` 菜单。然后，将显示程序转换菜单。

2.	选择所需的菜单，然后修改程序条件和位置，或编写新程序。

    ![](../../_assets/tp630/prg-modi-menu_eng.png)

<br>

{% hint style="info" %}
在机器人启动期间，菜单 `[4: 参照坐标系统]`、`[5: 坐标变换]`、`[6: 镜像]` 和 `[7: 步骤复制]` 的使用将受到限制。
{% endhint %}
[__SOURCE](4-service/3-program-conversion/1-rec-condition.md)
# 4.3.1 录制条件

您可以更改和设置程序特定步骤的录制条件，然后将其应用于现有程序，或编写新程序。

1. 触摸 `[6: Program Conversion - 1: Record condition conversion] ([6: Program Conversion  - 1: Record condition conversion])` 菜单。然后，录制条件转换设置窗口将出现。

2. 在设置录制条件选项后，触摸 `[OK]` 按钮。

    ![](../../_assets/tp630/prg-cond-modi_eng.png)

* `[Source program]`/`[Target program]`: 您可以输入要更改其录制条件的原始程序的编号 \(初始设置值: 当前选定程序\) 和更改录制条件后您想保存的新程序的编号。如果您将目标程序的编号设置为与原始程序的编号相同，则原始程序将被新程序覆盖和替换。
* `[Start Step]`/`[End Step]`: 您可以设置将应用录制条件更改的步骤范围 \(初始设置值: 1/最后一步\)。
* `[Accuracy]`, `[Tool]`: 您可以更改录制条件。
[__SOURCE](4-service/3-program-conversion/2-rec-speed.md)
# 4.3.2 录制速度转换

您可以更改程序特定步骤的录制速度，并将其应用于现有程序，或创建新程序。

1.	触摸 `[6: Program Conversion - 2: Record speed conversion] ([6: Program Conversion  - 2: Record speed conversion])` 菜单。然后，录制速度转换设置窗口将出现。

2.	在设置录制速度选项后，触摸 `[OK]` 按钮。

    ![](../../_assets/tp630/prg-speed-modi_eng.png)

* `[Source program]`/`[Target program]`：您可以输入要更改其录制速度的原始程序的编号 \(初始设置值：当前选定的程序\) 和更改录制速度后要保存的新程序的编号。如果您将目标程序的编号设置与原始程序的编号相同，则原始程序将被新程序覆盖和替换。
* `[Start Step]`/`[End Step]`：您可以设置要应用录制速度更改的步骤范围 \(初始设置值：1/最后一步\)。
* `[Method]`：您可以设置指定速度的方法。
  * `[specify Speed]`：您可以批量转换录制的速度。
  * `[specify ratio]`：如果录制速度的单位和在 `[Unit]` 选项中选择的速度单位匹配，则速度可以转换为相对于录制速度的比例。
  * `[change unit]`：您可以转换录制速度的单位。
* `[Range]`：您可以在希望更改录制速度的步骤范围内设置应用部分。
* `[Unit]`：您可以设置速度单位。当速度指定方法选择为 `[specify ratio]` 时，仅与步骤中记录的速度单位匹配的那些将转换为比例的百分比。
* `[Speed]`：如果您选择 `[specify ratio]` 作为速度指定方法，则这将表示比例值。
[__SOURCE](4-service/3-program-conversion/3-rec-position.md)
# 4.3.3 录制位置

您可以更改和设置在程序特定步骤中记录为隐藏姿势的步骤位置的坐标系统，并将其应用于现有程序或创建新程序。

1. 触摸`[6: 程序转换 - 3: 录制姿势转换] ([6: 程序转换  - 3: 录制姿势转换])`菜单。然后将出现录制位置转换设置窗口。

2. 在设置录制位置选项后，触摸`[确定]`按钮。

  ![](../../_assets/tp630/prg-position-modi_eng.png)

* `[源程序]`/`[目标程序]`：您可以输入想要更改的原始程序的编号 \(初始设置值：当前选定的程序\) 和您希望在更改录制位置后保存的新程序的编号。如果您将目标程序的编号设置为与原始程序相同，则原始程序将被新的程序覆盖和替换。
* `[步长范围]`：您可以设置要应用录制位置更改的步骤范围 \(初始设置值：1/最后一步\)。
* `[坐标系统格式]`：您可以选择用于移位在步骤中记录的位置数据的坐标系统。如果选择基准、机器人、工具或用户，则位置数据将被转换为笛卡尔坐标值。如果选择关节，则位置数据将被转换为轴角度。
[__SOURCE](4-service/3-program-conversion/4-rec-crdsys.md)
# 4.3.4 记录坐标系

您可以更改记录为隐藏姿态的步骤位置的坐标系。您可以通过按下相关步骤的快速打开按钮来检查您更改后的坐标系。在机器人的启动过程中，使用`[4: 参考坐标系的转换]`菜单将受到限制。

1. 触摸`[6: 程序转换 - 4: 参考坐标系的转换] ([6: 程序转换 - 4: 参考坐标系的转换])`菜单。然后，记录坐标系转换设置窗口将出现。

2. 在设置记录坐标系选项后，触摸`[确定]`按钮。

    ![](../../_assets/tp630/prg-coordisys-modi_eng.png)


* `[源程序]`/`[目标程序]`：您可以输入想要更改其记录坐标系的原始程序的编号（初始设置值：当前选择的程序）和更改记录坐标系后想要保存的新程序的编号。如果您将目标程序的编号设置为与原始程序的编号相同，则原始程序将被覆盖并替换为新程序。
* `[开始步骤]`/`[结束步骤]`：您可以设置要应用记录坐标系更改的步骤范围（初始设置值：1/最后一步）。
* `[坐标系格式]`：您可以选择要新指定的坐标系。
[__SOURCE](4-service/3-program-conversion/5-rec-conversion.md)
# 4.3.5 坐标转移

坐标转移功能是一种功能，可以让您在同一形状的工件（如图2所示）被放置在不同位置后，无需额外教学即可创建程序，该程序基于在工件上教授的程序\(图1\)。

![左: 图1, 右: 图2](../../_assets/image_369.png)

使用坐标转移功能需要三个参考点。您可以通过在初始位置的工件上标记三个参考点来创建程序A。在移动工件位置后，使用之前标记的三个参考点编写程序B。

![左: 程序A, 右: 程序B](../../_assets/image_368.png)

{% hint style="info" %}
* 坐标转移程序的准确性将受到在坐标转移中教授三个参考点的准确性影响。尽可能准确地进行三个参考点的教学。
* 在坐标转移中，尽量将三个参考点之间的距离设置得尽可能远。
{% endhint %}

您可以通过计算坐标转移量，将现有程序\(程序1\)转移到新程序\(程序2\)，这一过程基于程序A和程序B的三个步骤。

![](../../_assets/image_315.png)

<br>

---

此功能在机器人操作期间不允许使用。使用坐标转移的方法如下。

1. 选择[6: 程序转换 - 5: 坐标变换]菜单。将出现坐标转移的设置窗口。
2. 进行设置后，按`[OK]`按钮。

![](../../_assets/tp630/prg-coordinate-modi_eng.png)

* [源程序] : 现有教学程序编号（[图1]的程序编号）

* [目标程序] : 通过执行坐标转换新创建的程序编号（[图2]的程序编号）

* [前基程序] : 具有三个标准点的程序编号（[程序A]的编号）

* [后基程序] : 记录转换参考的三个点的程序编号（[程序B]编号）
[__SOURCE](4-service/3-program-conversion/6-mirror-image.md)
# 4.3.6 镜像

您可以编写一个程序，其中 S 轴的位置和腕轴的姿势基于机器人 S 轴 0° 位置的 Y-Z 平面是对称的。

此功能在指示左右两个机器人执行相同操作时非常有用，例如焊接车辆的车身。首先，给一个机器人教一个操作，然后打开该操作的程序并将其转换为镜像。然后，将写入与 S 轴对称的程序。

![图32 原程序 \(左\) / 通过镜像转换的程序 \(右\)](../../_assets/image_379.png)

{% hint style="info" %}
镜像功能不支持协作机器人。
{% endhint %}

在机器人启动期间，将限制使用 `[6: 镜像]` 菜单。使用镜像功能的方法如下。

1. 触摸 `[6: 程序转换 - 6: 镜像] ([6: 程序转换 - 6: 镜像])` 菜单。然后，镜像设置窗口将出现。

2. 在设置镜像转换选项后，触摸 `[OK]` 按钮。

* `[源程序]`/`[目标程序]`: 您可以设置现有程序的编号和通过镜像转换要创建的新程序的编号。

    ![](../../_assets/tp630/prg-mirror-img_eng.png)
[__SOURCE](4-service/3-program-conversion/7-step-copy/README.md)
# 4.3.7 步骤复制

您可以将程序的某部分复制到另一个程序或同一程序中。步骤中记录的功能也将被复制。在机器人启动时，使用 `[7: 步骤复制]` 菜单将受到限制。

1. 触摸 `[6: 程序转换 - 7: 步骤复制] ([6: 程序转换 - 7: 步骤复制])` 菜单。步骤复制设置窗口将出现。

2. 设置步骤复制选项后，触摸 `[OK]` 按钮。

    ![](../../../_assets/tp630/prg-step-copy_eng.png)

* `[源程序]`/`[目标程序]`：您可以设置要复制步骤的原始程序的编号，以及您希望通过粘贴复制步骤创建的新程序的编号。如果您将目标程序编号设置为与原始程序编号相同，则原始程序将被新程序覆盖和替换。
* `[开始步骤]`/`[结束步骤]`：您可以设置要复制的步骤范围（初始设置值：1/最后一步）。
* `[插入步骤]`：您可以设置要粘贴复制步骤的参考步骤。复制的步骤将紧接在参考步骤之后粘贴。
* `[复制方法]`：您可以选择复制步骤的进度方向。
  * `[前进/反向]`：您可以按照原始程序的顺序或原始程序的反向顺序粘贴复制的步骤。

{% hint style="info" %}
* 您无法复制受保护的程序。
* 如果复制的步骤中记录了 END 功能，该功能将一起复制。必要时请删除该功能。
* 如果在复制的步骤中记录了可跳转到复制范围外的步骤的功能 \(GOTO, GOSUB\)，该功能将会被复制，但编号不会自动更改。请在复制后更改该编号。
{% endhint %}
[__SOURCE](4-service/3-program-conversion/7-step-copy/1-step-copy-example.md)
# 4.3.7.1 步骤复制示例

您可以将程序 1 的步骤 2-5 复制到程序 2 的步骤 2 \(设置为输入步骤\) 中，方向可以是正向或反向。

原始程序的步骤 2-5 \(程序 1\) 将在目标程序 \(程序 2\) 的输入步骤 \(步骤 2\) 之后插入，正向时遵循原始程序的相同顺序，或反向时按照原始程序的逆序。

![](../../../_assets/image_321.png)
[__SOURCE](4-service/3-program-conversion/9-stmt-comment.md)
# 4.3.9 语句注释

(此功能在版本 V70.02-00 及以后版本中支持。)

此功能使用预配置的数据注释自动将注释附加到语句上。它还包括批量删除注释或为 `点 (spot)` 语句（点焊命令）分配序列号的功能。

有关如何配置数据注释的详细信息，请参阅 [4.11 数据注释](../11-data-cmts.md)。

* 执行示例 1：信号分配，`等待 (wait)`，`移动 (move)` 语句

  ![](../../_assets/tp630/prog-conv/prog-conv-data-job1.png)

* 执行示例 2：`点 (spot)` 语句
  
  ![](../../_assets/tp630/prog-conv/prog-conv-data-job2.png)

### 操作方法

(1) 选择 `[F1: Service] -> 6: 程序转换 -> 9: 语句数据注释`。

![](../../_assets/tp630/prog-conv/prog-conv-data-cmt.png)

(2) 配置以下设置，然后按 `[F7: 确定] ([F7: OK])` 键以运行该过程。

- `源程序 (Source Program)`

  您希望应用注释的原始程序的编号。如果设置为 0，操作将在所有作业的所有范围内执行。

- `目标程序 (Target Program)`

  将保存结果的程序编号。如果与 `源程序 (Source program)` 编号相同，则文件将被覆盖。

- `开始步骤 (Start step)` ~ `结束步骤 (End step)`

  您希望应用更改的具体步骤范围。 （默认值：0 ~ 最后一步）。
  例如，如果设置为 2-5，则更改将从步骤 2 的移动语句开始应用，直到步骤 5 的最后一个功能。

- `现有注释 (Existing comment)`

  * `全部删除 (Delete all)` : 删除现有的注释，而不是应用新的注释。 （这仅删除附加到语句的注释；它不删除注释语句行。）
    
  * `覆盖 (Overwrite)` : 如果语句已经有注释，将被新的注释替换。

  * `跳过 (Skip)` : 如果语句已经有注释，该特定语句将被跳过并保持不变。

- `受影响的命令 (Affected commends)` （如果 `现有注释 (Existing comment)` 设置为 `全部删除 (Delete all)`，则隐藏。）

  选择您希望应用注释的命令类型。

  * `赋值的左侧 (LHS of assignment)`: 使用与赋值语句左侧变量关联的注释作为语句注释。

  * `移动 (move)`: 对于包含 `tg=` 参数的 `移动 (move)` 语句，使用分配姿态表达式中第一个姿态变量的注释。 （注意：这不适用于隐藏姿态 `移动 (move)` 语句。）

  * `等待 (wait)`，`如果 (if)` （包括 `elseif`），`切换 (switch)`: 使用条件参数中指定的变量的注释作为语句注释。

  * `点 (spot)`: 在作业范围内分配一个序列号作为语句注释。
  例如，如果您将前缀设置为 `W.P.=`，起始编号设置为 101，则第一个点语句将注释为 `W.P.=101`，第二个为 `W.P.=102`，依此类推。

- `前缀 (Prefix)`
  
  定义应用于 `点 (spot)` 语句评论的序列号的前缀。您可以使用软键盘编辑此内容。

- `起始编号 (Starting number)`

  设置应用于 `点 (spot)` 语句注释的序列的初始编号。

----

### 注意事项

- 如果语句的条件参数是表达式，则注释根据占据该表达式第一个字符的变量决定。例如，如果 `di1` 注释为 `part check` 而 `di2` 为 `vacuum check`，则以下 `如果 (if)` 语句将被分配注释 `part check`：

    ```python
    if di1=0 and di2=0 then 90 # part check
    ```

- 在作业编辑屏幕的块编辑模式下，您还可以为选定的语句自动插入或删除注释。与此屏幕不同的是，此模式的应用条件固定如下：

  * `现有注释 (Existing comment)`: `覆盖 (Overwrite)`

  * `受影响的命令 (Affected commands)`: 除 `点 (spot)` 外的所有命令

有关更多详细信息，请参阅 [3.2.4.5 块编辑模式](../../3-programming/2-prog-edit/4-statement-edit/5-block-edit-mode.md)。
[__SOURCE](4-service/4-system-diagnosis/README.md)
# 4.4 系统诊断

您可以检查和管理机器人和控制器的状态。您可以检查和更新控制器每个模块的版本。
[__SOURCE](4-service/4-system-diagnosis/1-system-version/README.md)
# 4.4.1 系统版本

1.	触摸`[7: 系统诊断 - 1: 系统版本] ([7: 系统诊断 - 1: 系统版本])`菜单。然后，系统环境设置窗口将出现。

2.	检查和管理机器人的系统环境（软件版本）信息及控制器。

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
          <li>[确定]: 菜单将关闭。</li>
          <li>[版本更新]: 您可以更新控制器每个模块的版本。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](4-service/4-system-diagnosis/1-system-version/1-controller-system-update.md)
# 4.4.1.1 控制器系统更新

您可以使用集成的压缩文件更新控制器每个模块的版本。

1. 将包含集成压缩文件的可移动存储设备连接到教导 pendant 的 USB 插槽。当可移动存储设备连接到教导 pendant 时，状态栏中会出现 `[USB]` 图标 \(![](../../../_assets/icon-usb2.png)\)。

2. 在功能按钮栏中触摸 `[Ver. Up]` 按钮。然后，会出现版本升级程序执行窗口。

3. 通过触摸下拉菜单选择 `[Version Up]` 模式，使用 `[Open]` 按钮选择集成压缩文件，然后触摸 `[OK]` 按钮。

    ![](../../../_assets/image_311.png)

4. 选择您要更新的模块后，触摸 `[OK]` 按钮。然后，更新将开始。

    ![](../../../_assets/image_255.png)

5. 更新完成后，请重启控制器。

    ![](../../../_assets/image_367.png)
[__SOURCE](4-service/5-date-time-setting.md)
# 4.5 日期和时间的设置

您可以设置控制器的日期和时间。

1. 点按 `8: 日期，时间设置 (8: Date, time setting)` 菜单。日期和时间设置窗口将出现。

2. 设置日期和时间信息后，点按 `[OK]` 按钮。

    ![](../_assets/tp630/svc-date_eng.png)

* 您可以通过使用教学挂件上的操作键输入日期和时间进行设置。
* 如果按箭头键，光标将在日期和时间项目之间移动 \(年/月/日/时/分/秒/上午/下午\)。

* 您可以通过按数字键输入数字。您也可以使用 `[SHIFT]`+`[↓]` 键调整值。
* 在日历上设置日期。点按 `[◁/▷]` 按钮选择年和月，然后点按日期。
[__SOURCE](4-service/6-app.md)
# 4.6 应用程序

管理安装和运行在教学挂件上的软件。

有关更多信息，请参阅 "[${cont_model} 控制器功能手册 - 教学挂件应用程序](https://hrbook-hrc.web.app/#/view/doc-hi6-tp-app/zh/README?cont_model=${cont_model})"。
[__SOURCE](4-service/7-tp-option.md)
# 4.7 教学挂件选项

设置教学挂件的首选项。

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
      <td style="text-align:left">在最后操作后的设置周期激活屏幕保护。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        屏幕保护亮度
      </td>
      <td style="text-align:left">将屏幕保护的亮度设置为从 0（关闭）到 6（稍微暗）。<br>
      （支持从版本 V60.32-06 及以后。）</td>
    </tr>
    <tr>
      <td style="text-align:left">
        屏幕保护期间的通信周期
      </td>
      <td style="text-align:left">设置在屏幕保护激活时接收控制器信息的通信延迟。如果设置为 0，则通信没有延迟。<br>
      （支持从版本 V60.30-08 及以后。）</td>
    </tr>
    <tr>
      <td style="text-align:left">
        触摸屏开
      </td>
      <td style="text-align:left">打开或关闭触摸屏。<br> 如果由于意外接触屏幕而有意外操作教学挂件的风险，请禁用此选项。<br>
      要重新启用触摸屏选项，请按 Ctrl + ←(退格键) 激活 F 按钮栏键盘模式，然后再次启用该选项。<sup>1)</sup></td>
    </tr>
    <tr>
      <td style="text-align:left">
        是否使用工作键
      </td>
      <td style="text-align:left">选择是否分别使用 jog 键 `J7-`/`J7+` 和 `J8-`/`J8+`。 <br>如果由于不正确的 jog 键操作而有位置器碰撞或其他问题的风险，请关闭此选项。<sup>2)</sup></td>
    </tr>
    <tr>
      <td style="text-align:left">
        语言
      </td>
      <td style="text-align:left">更改教学挂件的显示语言。返回主屏幕后，改动生效。<br>
      （支持从版本 V70.00-00 及以后。<sup>3)</sup>）</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}

1\) 有关键盘模式的更多详细信息，请参阅 "[11.2 键盘模式](../11-etc/2-keypad-mode.md)"。

2\) 有关 jog 键使用的更多详细信息，请参阅 "[7.6.6 机制设置](../7-system/6-initialization/6-mechannism-set.md)" 中的机制 jog 规则。

3\) 对于提到的版本之前，只有在执行 `[F1: 服务] - 9: 退出TP应用程序 ([F1: Service] - 9: Exit TP application)` 后，才能切换显示语言。

{% endhint %}
[__SOURCE](4-service/8-tp-share.md)
# 4.8 教学 pendant 共享

![](../_assets/tp630/tp-sharing.png)

使用屏幕顶部的单选按钮选择模式。

* OFF : 共享功能被禁用。在正常情况下，应该设置为 OFF，以便教学 pendant 能够正确连接到控制器。

* VRC (PC) : 一个物理教学 pendant 连接到多个在桌面 PC 上运行的虚拟控制器 (VRCs)，并可以通过在它们之间切换来使用。
请参阅 HRSpace4 帮助中的以下部分以获取连接说明。
  + HRSpace4 手册 - 8.4 实际教学 pendant (RTP)

* RRC (真实机器人控制器) : 一个教学 pendant 连接到多个控制器并通过在它们之间切换来使用。
  + 需要额外的可选硬件。此功能目前不受支持。
[__SOURCE](4-service/9-industrial-communication-monitoring.md)
# 4.9 工业通信监控

监控固件信息和通信状态。

有关更多信息，请参阅 "[${cont_model} 控制器功能手册 - 工业通信 > 1. CIFX PCI 通信 > 1.4 CIFX PCI - 监控工业通信](https://hrbook-hrc.web.app/#/view/doc-industrial-communication/zh-${cont_model}/1-cifx-pci-communication/4-cifx-pci-monitoring-industrial-communication/README?cont_model=${cont_model})
[__SOURCE](4-service/10-system-program.md)
# 4.10 系统程序

您可以查看和删除安装在控制器上的系统程序（例如 OPC-UA 服务器）。

<br>

1. 安装系统程序

   * 将包含 ${cont_model} 系统程序安装文件 (hps) 的 USB 驱动器连接到示教端 (TP)。
   * 运行 `5: 文件管理器 (5: File Manager)` 菜单。从 [USB] 文件列表中选择文件并按 Enter。
   * 当程序安装对话框出现时，按 `运行 (Run)` 按钮以开始安装。
   * 安装完成后，按 `退出 (Exit)` 按钮。
   * 要启动程序，请重新启动系统。

<br>

2. 删除系统程序

   * 运行 `14: System Program` 菜单以查看已安装程序的列表。
   * 选择一个程序并按屏幕底部的 `Remove` 按钮。
   * 当程序删除对话框出现时，按运行按钮以开始删除过程。
   * 删除完成后，按 `退出 (Exit)` 按钮。
[__SOURCE](4-service/11-data-cmts.md)
<script id="page-config" type="application/json">
{
	"permittedStrs": ["Hi6", "Hi7"]
}
</script>

# 4.11 数据注释

(此功能支持从 V70.02-00 版本及更高版本。)

您可以为 IO 变量、内置 PLC 的继电器和其他一般变量注册注释。注册的注释将在监控面板中显示为工具提示。 (`公共输入 (public input)`, `公共输出 (public output)`, `fn 输入 (fn input)`, `fn 输出 (fn output)`, `全局变量 (global variable)`, `内存变量 (memory variable)`, `多种数据 (watch)` 监控)

![](../_assets/tp630/data-cmt/data-cmt-di_eng.png)

此外，通过使用以下功能，注册的注释可以自动附加到作业程序的每个语句上。

* [4.3.9 语句数据注释](3-program-conversion/9-stmt-comment.md)
* [3.2.4.5 块编辑模式](../3-programming/2-prog-edit/4-statement-edit/5-block-edit-mode.md) - `[auto comment]` 按钮。

在此屏幕上配置的注释将保存到 `project/DataCmt.txt` 文件中。

![](../_assets/tp630/data-cmt/data-cmt.png)


### 数据注释屏幕

   1. 选择 `[F1: 服务] - 4: 数据注释 ([F1: Service] - 4: Data comment)` 打开屏幕。

   2. 使用顶部的过滤组合框选择所需的数据类别和类型。

   3. 所选数据将以表格形式显示。您可以查看每个项目的名称、注释和当前值。

   4. 对于 `fb.dio`、`fn.dio` 和 `relay` 对象，所有索引都会显示。具有注册注释的索引将显示注释，而没有注册的索引将有一个空的注释字段。

   5. `etc` 仅显示各种全局变量中具有注册注释的项目（排除 IO 和继电器）。(不要为局部变量注册注释，因为它们的含义可能因子作业而异。) 数据类型根据变量类型显示。

![](../_assets/tp630/data-cmt/data-cmt-etc_eng.png)

### 导航

   1. 您可以通过按 `上 (Up)`/`下 (Down)` 箭头键在项目之间移动。按住 `Ctrl` 键时按下可以更快地移动。

   2. 或者，您可以直接在 `名称 (Name)` 列中输入数字以跳转到特定索引。(注意：此功能不适用于 `etc` 对象。)

   3. 最多可以同时显示 1,000 个项目。对于具有更大最大索引的类型（例如 ` (M)`-继电器），您不能在一个屏幕上查看所有内容。必须使用上述方法通过页面进行导航。

### 编辑、保存和加载

   1. 您可以使用数字键盘或软键盘在 `注释 (Comment)` 列中输入或编辑注释。

   2. 要删除现有的注释，只需删除注释列中的文本。（空字符串被视为未注册。）

   3. 按下 `[F7: 确定] ([F7: OK])` 或 `[SHIFT]+[F7: 应用]` 将把您的编辑应用于主模块并将其保存到 `DataCmt.txt` 文件中。

   4. 按下 `[F1: 初始化] ([F1: 清除])` 将删除所有项目。（更改仅在按下 `[F7: 确定] ([F7: OK])` 后在文件中反映。）

   5. 按下 `[F2: 重新加载] ([F2: Reload])` 重新加载 `DataCmt.txt` 文件并刷新 TP 上的数据注释屏幕。

   6. 按下 `[F3: 排序] ([F3: Sort])` 将不会更改当前屏幕显示，但当您按下 `[F7: 确定] ([F7: OK])` 时，数据将以排序状态保存。如果您在不排序的情况下保存，文件中的原始顺序将被保留。

   7. 值列无法编辑。


### `DataCmt.txt` 文件

   1. 或者，您可以使用文本编辑器直接在 PC 上编辑 `DataCmt.txt` 文件。下面的图片显示了在 `Visual Studio Code` 中打开该文件的示例。

      ![](../_assets/tp630/data-cmt/data-cmt-file.png)

   2. 文件采用 `tsv (Tab-Separated Values)` 格式。每行由名称和注释对组成。名称和注释必须用至少一个制表符分隔。

   3. 文件格式与 HRLadder 中的 `导入继电器描述` / `导出继电器描述` 功能兼容。因此，创建的文件可以在 Hi6/Hi7 控制器和 HRLadder 之间交替使用。(它也与 Hi5a 控制器兼容；不过，继电器或变量名称的差异可能需要进行调整。)

   4. 对于 I/O 或继电器名称，系统将内置 PLC 样式（大写）和 hrscript 样式（小写）视为相同。(例如，`FB5.DIB3` 和 `fb5.dib3` 被视为相同.) 但对于变量，区分大小写必须完全匹配。

   5. 如果注释包含非英语字符，则文件编码必须保存为 UTF8-BOM。（如果只使用英语注释，则 ANSI 和 UTF8-BOM 都可以接受。）
[__SOURCE](5-conditional-setting/README.md)
# 5. 条件设置

您可以简单地更改操作条件，而无需修改程序。即使控制器重新启动，已更改的设置值也将保持不变。
[__SOURCE](5-conditional-setting/1-op-cond-set.md)
# 5.1 操作条件设置

1. 在初始屏幕的左上角触摸 `[Speed Adjustment]` 按钮。然后，操作条件设置窗口将显示。

    ![](../_assets/tp630/sbar-spd-auto_eng.png)  ![](../_assets/tp630/sbar-spd-manual_eng.png)

{% hint style="info" %}
在 `[Speed Adjustment]` 按钮上，手动模式下将显示速度限制 \(mm/sec\)，自动模式下将显示播放速度 \(%\)。
{% endhint %}



2. 更改操作条件设置值，然后触摸 `[OK]` 按钮。

    ![](../_assets/tp630/sbar-condi-setting_eng.png)

    
[__SOURCE](5-conditional-setting/2-op-cond-set-info.md)
# 5.2 操作条件设置的信息



* `[1: 操作周期类型]`: 您可以设置在自动操作期间是否重复执行程序。也可以在机器人启动时进行设置，设置值在手动操作期间将不被应用。
  * 1 周期: 工作程序将执行一次然后停止。当达到程序 END 时，机器人将停止。
  * 连续: 工作程序将连续地重复执行。如果有外部停止操作，机器人将停止。
</br>
</br>

* `[2: 步骤 FWD/BWD 最大速度]`: 您可以设置前进/后退的速度限制。有关此选项的详细信息，请参阅 "[2.1 手动操作](../2-operation/1-manual-operation/README.md)"。
</br>

* `[3: 步骤 FWD 执行功能]`: 您可以设置在进行前进步骤操作时，在工作程序中记录的功能执行选项（模式）。
  * 关闭: 仅执行工作程序中记录的 END。除了 END 之外的所有其他功能将不被执行。
  * 打开: 将执行工作程序中记录的所有功能。
  * 1 打开: 仅将执行输入信号等待功能和程序结束功能。



{% hint style="warning" %}
在后退步骤操作期间，将仅执行输入等待信号功能，所有其他功能将不被执行。
{% endhint %}

* `[4: 后退和前进步骤后功能的重新执行]`: 您可以进行设置，以便在后退操作后再次进行前进操作时，可以重新执行工作程序中记录的之前执行的功能。
</br>

* `[5: 步骤 FWD/BWD 期间的路径恢复]`: 您可以设置在进行前进/后退操作时执行路径恢复的模式。
  * 禁用: 不执行路径恢复
  * 启用: 将在不确认用户是否执行路径恢复的情况下执行路径恢复
</br>
</br>

* `[6: 播放速度比率]`: 您可以设置机器人在自动模式下播放程序的操作速度（%）。这不是指更改工作程序步骤中记录的速度，而是指更改机器人移动速度与批处理中记录的步骤速度的比率，从 1% 到 100% 的范围。




{% hint style="info" %}
如果在自动操作期间通过外部输入输入低速命令，将不应用自动操作速度比率，但将应用手动最大速度（250 mm/s）。
{% endhint %}

* `[7: 机器人锁定]`: 您可以设置工作程序，使自动操作在不移动机器人的情况下进行。您可以检查 I/O 与外部设备的状态、软极限、循环时间等。
</br>

* `[8: 插补基座]`: 您可以设置一个工具，作为机器人手动走动时的参考。一般来说，机器人工具用作插补参考。
  * 机器人工具: 插补操作将基于安装在机器人前端的工具执行。
  * 固定工具: 插补将基于固定在地板等位置的工具前端执行。如果选择固定工具作为插补参考，初始屏幕左侧的工具编号将标记为 ST0 \(![](../_assets/tp630/sbt-crd-st0-small_eng.png)\)。




{% hint style="info" %}
如果选择固定工具作为插补参考，您必须设置固定工具坐标系。有关详细信息，请参阅 "[7.3.6.2 固定工具坐标系统](../7-system/3-control-parameter/6-cordsys-reg/2-stationary-tool-crdsys.md)"。
{% endhint %}

* `[9: 选择用户坐标系统指定]`: 您可以设置用户坐标系统编号（0~10），以便在手动走动操作期间进行笛卡尔操作。然后，机器人将根据指定用户坐标系统的 X、Y 和 Z 轴进行操作，并在监控姿态时显示所选用户坐标系统的坐标值作为工具前端的 X、Y 和 Z 坐标值。



  * 如果设置为 0，机器人坐标系统图标 \(![](../_assets/tp630/sbt-crd-robot-small_eng.png)\) 将显示在状态显示窗口的 `[坐标系统]` 按钮上。将停用基于用户坐标系统的操作，并将执行基于笛卡尔坐标的操作和监控。 <br>
  ![](../_assets/tp630/pane-pose-robotcoord_eng.png)

  * 如果设置为 1 到 10 之间的数字，则用户坐标系统图标 \(![](../_assets/tp630/sbt-crd-user-small_eng.png)\) 将显示在 `[坐标系统]` 按钮上。通过使用 `[轴操作]` 键更改的坐标值将基于用户坐标系统。 <br>
  ![](../_assets/tp630/pane-pose-usrcoord_eng.png)


{% hint style="info" %}
您可以在 `[system - 2: 控制参数 - 6: 坐标系统注册 -1: 用户坐标系统] ([system - 2: 控制参数 - 6: 坐标系统注册 -1: 用户坐标系统])` 中注册用户坐标系统编号。
{% endhint %}


* `[10: Plc 运行模式]`: 当机器人控制器使用嵌入式 PLC 控制输入/输出信号时，请设置控制嵌入式 PLC 的模式。总共有 4 种嵌入式 PLC 模式。有关更多详细信息，请参阅 "[${cont_model} 控制器功能手册 - 嵌入式 PLC](https://hrbook-hrc.web.app/#/view/doc-hi6-embedded-plc/zh/README?cont_model=${cont_model})"。

  * 关闭: 禁用该功能。
  * 停止: 停止嵌入式 PLC 操作。
  * R - 停止(远程停止): 这是远程模式，并在连接到控制器的 PC 的 HRLadder 中停止嵌入式 PLC 操作。
  * R - 运行(远程运行): 这是远程模式，嵌入式 PLC 操作从连接到控制器的 PC 的 HRLadder 中执行。
  * 运行: 控制器操作下载到控制器的 PLC 程序。仅在 PC 上的 HRLadder 中可以进行监控。
[__SOURCE](6-monitoring/README.md)
# 6. 监控

您可以检查机器人系统的状态和控制器的各种数据。

1. 按顺序触摸面板右上角的 `[pane layout]` 按钮，[split] 底部，和 [select] 左下角。面板选择窗口将出现。

    ![](../_assets/tp630/rbt-window-divide_eng.png)

2. 触摸您想要监控的项目并检查显示的数据。

    ![](../_assets/tp630/pane-list_eng.png)

{% hint style="info" %}
* 所有可以监控的项目将在面板选择窗口中显示。
* 
  可以监控的项目将根据控制器的设置不同而显示不同。

* 
  有关如何使用面板堆栈和工作区窗口的详细信息，请参阅 "[1.2.4.8 Task edit window](../1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/8-work-area?cont_model=${cont_model})"。
{% endhint %}
[__SOURCE](6-monitoring/1-basic/README.md)
# 6.1 基础
[__SOURCE](6-monitoring/1-basic/1-pose.md)
# 6.1.1 位姿

在面板选择窗口中点击 `[Pose]`。然后，机器人位姿信息窗口将出现。您可以查看每个轴的当前角度、工具中心点 \(TCP\) 的坐标值，以及编码器的当前值和命令值。

![](../../_assets/tp630/pane-pose_eng.png)
[__SOURCE](6-monitoring/1-basic/2-op-info.md)
# 6.1.2 操作时间

在面板选择窗口中，触摸 `[Operation time]`。然后，控制器的操作信息窗口将出现。

您可以检查在系统初始化、电源输入和最近周期开始后立即创建的控制器的每个操作的累积时间和循环次数。您可以通过触摸信息底部每个项目的 `[Clear]` 按钮来初始化操作信息。

![Figure 41 操作信息](../../_assets/tp630/pane-operating_eng.png)

根据各个项目的条件反映的时机如下。

![](../../_assets/image_449.png)
[__SOURCE](6-monitoring/1-basic/3-history.md)
# 6.1.3 历史

在面板选择窗口中，触摸 `[history]`。历史窗口将出现。

您可以查看作业程序的执行日志和时间戳的历史。  

![Figure 44 History](../../_assets/tp630/pane-history_eng.png)
[__SOURCE](6-monitoring/2-io/README.md)
# 6.2 IO, PLC, 通信
[__SOURCE](6-monitoring/2-io/1-system-input.md)
# 6.2.1 系统输入

在面板选择窗口中，触摸 `[System Input]`。然后，输入信号窗口将出现。

您可以检查与机器人操作相关的信号状态以及预先分配用于检测机器人和控制器发生的任何异常的输入信号状态。

![Figure 37 System Input - ON/OFF,Value, Sequence status](../../_assets/tp630/pane-system-input_eng.png)



* 在 ON/OFF 状态和序列状态中，当前输入的信号将以黄色显示。
* 
  在序列状态中，将仅显示控制器序列信号的状态。

* 
  `[ON/OFF]`/`[Value]`/`[Sequence]`：您可以通过触摸单选按钮更改输入信号窗口的显示模式。
[__SOURCE](6-monitoring/2-io/2-system-output.md)
# 6.2.2 系统输出

触摸 `[System Output]` 在面板选择窗口中。然后，输出信号窗口将会出现。

您可以检查与机器人操作相关的信号，并检查刹车控制的状态。



![Figure 39 System Output - ON/OFF,Value, Sequence status](../../_assets/tp630/pane-system-output_eng.png)

* 在 ON/OFF 状态和序列状态中，当前输出的信号将以黄色显示。
* 在序列状态中，仅将显示控制器序列信号的状态。
* `[ON/OFF]`/`[Value]`/`[Sequence]`: 您可以通过触摸单选按钮更改输出信号窗口的显示模式。
* `[Manual output]`: 您可以在 ON/OFF 和序列状态下强制输出所选信号。



### 手动输出

您可以选择所需的信号并强制输出。

1. 您可以通过触摸系统输出信号窗口右侧的 `[ON/OFF]` 或 `[Sequence]` 单选按钮将显示模式设置为 ON/OFF 状态或序列状态。

2. 在信号窗口中触摸一个信号以选择它，然后触摸 `[Manual Output]` 按钮。

    ![](../../_assets/tp630/pane-system-output1_eng.png)

3. 在手动输出确认窗口中检查输出条件，然后触摸 `[ENTER]` 按钮。

    ![](../../_assets/tp630/pane-system-output-manual-pop_eng.png)


    | soN | =1/0 |
    | :---: | :---: |
    | N: 要输出的信号的编号 | 输出状态 \(1: 输出, 0: 不输出\) |


4. 检查所选信号的输出状态。所选信号将切换到输出状态，并在信号窗口中以黄色显示。

    ![](../../_assets/tp630/pane-system-output2_eng.png)
[__SOURCE](6-monitoring/2-io/3-user-input.md)
# 6.2.3 公共输入

在面板选择窗口中触摸 `[public Input]`。然后，将出现公共输入信号窗口。

您可以检查通过控制器中 I/O 板的 CNIN 连接器输入的公共输入信号的状态。

![图 40 公共输入信号 - 开/关状态 (左) / 值 (右)](../../_assets/tp630/pane-public-input_eng.png)

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
        <p>显示公共输入信号的状态</p>
        <ul>
          <li>被指定为系统基本规格或用户分配的公共输入信号将以 <b>加粗</b> 显示。</li>
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
          <li>[FB0]: 您可以通过触摸下拉菜单选择要监控的 FB 块 (FB0 - FB15)。您可以配置最多 16 个 I/O 块，并且可以监控 960 点信号</li>
          <li><b>[ATTR.-APPLIED]</b>: 您可以勾选复选框，以便在通过正/负逻辑属性之前显示物理输入值。基础设置（未选中）是在通过正/负逻辑属性之后显示输入逻辑值。</li>
          <li>[开/关]/[值]: 您可以通过触摸单选按钮更改信号显示模式。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 在使用信号的情况下，例如通过嵌入式 PLC 映射的现场总线信号，输入信号的开/关状态可能会有所不同。 
* 
  输入信号的流动如下。
{% endhint %}

![](../../_assets/user-input-flow_en.png)
[__SOURCE](6-monitoring/2-io/4-user-output.md)
# 6.2.4 公共输出

在面板选择窗口中触摸 `[public Output]`。然后，公共输出信号窗口将出现。

您可以检查通过控制器的 I/O 板的 CNOUT 连接器输出的公共输出信号状态。

![图41 公共输出信号 - 开/关状态 \(左侧\) / 值状态 \(右侧\)](../../_assets/tp630/pane-univoutsig-mode_eng.png)

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
          <li>指定为系统基本规格或由用户分配的普通输出信号将以 <b>粗体</b> 显示。</li>
          <li>当前输出的信号将以黄色显示。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[FB0]：您可以通过触摸下拉菜单选择要监控的 FB 块 (FB0 - FB15)。您可以配置最多 16 个 I/O 块，并且可以使用一个块监控 960 个信号点。</li>
          <li>[手动输出]：您可以强制选择的信号输出。</li>
          <li><b>[ATTR.-APPLIED]</b>：您可以勾选复选框，以使物理输入值在通过正/负逻辑属性之前显示。基本设置（未选中）是输入逻辑值在通过正/负逻辑属性之后将显示。</li>
          <li>[开/关]/[值]：您可以通过触摸单选按钮更改信号显示模式。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 在通过嵌入式 PLC 映射信号（如现场总线信号）的情况下，输出信号的开/关状态可能会有所不同。
* 
  输出信号的流向如下。
{% endhint %}

![](../../_assets/user-input-flow_en.png)

#### 

#### 手动输出

您可以选择所需的信号并强制其输出。

1.	您可以通过触摸一般输出信号窗口右侧的 `[ON/OFF]` 单选按钮，将显示模式设置为开/关状态。

2.	在信号窗口中触摸一个信号以选择它，然后触摸 `[手动输出]` 按钮。

    ![](../../_assets/tp630/pane-univoutsig_eng.png)


3.	在手动输出确认窗口中检查输出条件后，触摸 `[ENTER]` 按钮。

    ![](../../_assets/tp630/pane-univoutsig-manual_eng.png)

| FbN | doN | =1/0 |
| :---: | :---: | :---: |
| N: 要监控的 FB 块的编号 | N: 要输出的信号的编号 | 输出状态 \(1: 输出, 0: 无输出\) |

4.	检查所选信号的输出状态。所选信号将切换到输出状态并在信号窗口中以黄色显示。

    ![](../../_assets/tp630/pane-univoutsig-onoff_eng.png)
[__SOURCE](6-monitoring/2-io/5-fn-io.md)
# 6.2.5 fn 输入，fn 输出

您可以通过指定 fb 对象的特定区域来定义 fn 对象。
如果 ${cont_model} 控制器是一个现场总线主设备，并且有多个现场总线从设备，您可以将每个从设备的区域设置为每个 fn 对象，以直观地处理这些从设备。

设置的 fn 对象可以像机器人语言和嵌入式 PLC 中的 fb 对象一样使用。

![](../../_assets/io/io_fn.png)

在面板选择窗口中选择 `[fn input]` 或 `[fn output]`。fn 输入或输出面板会出现，您可以检查每个 fn 对象的输入和输出信号的值。

有关如何设置 fn 对象的信息，请参考下面的链接。

[7.3.2.12 fn 块分配](../../7-system/3-control-parameter/2-io-signal-setting/12-fn-block?cont_model=${cont_model})

单击 '[F6:prev]' / '[F7:next]' 按钮以更改要显示的 fn 对象的数量。

其余 F 按钮的使用与 [6.2.3 公共输入](./3-user-input.md) 和 [6.2.4 公共输出](./4-user-output.md?cont_model=${cont_model}) 监视窗口相同。

![](../../_assets/io/io_fn_mon.png)
[__SOURCE](6-monitoring/2-io/6-forced-io.md)
# 6.2.6 强制 IO

您可以在强制 IO 面板中注册 IO 继电器变量，以强制更改一些 IO 值。

{% hint style="warning" %}
* 此功能仅用于测试或问题分析。
* 强制 IO 功能的误操作可能导致严重事故，如碰撞、掉落和人员伤亡。仅在您完全理解系统的 IO 连接并清楚预测强制值更改的后果时谨慎使用。
* 测试和问题分析后，请确保完全清除强制 IO，并将其恢复到正常 IO 状态。

{% endhint %}

#### 打开强制 IO 面板

1. 分屏并按下左下角的 [选择] 按钮。

![](../../_assets/tp630/panel-split.png)
&nbsp;
![](../../_assets/tp630/panel-sel.png)

2. 在面板选择窗口中双击 `强制 IO (forced io)`。强制 I/O 面板打开。

![](../../_assets/tp630/panel-forced-io/panel-forced-io.png)

![](../../_assets/tp630/panel-forced-io/panel-forced-io-mon.png)


#### 如何使用

选择 `名称 (Name)` 列，输入所需的 IO 继电器变量名称，按下 `确认 (ENTER)` 键以在表中注册该变量。  
（您可以通过再次点击名称列来修改输入的变量名称。）

![](../../_assets/tp630/panel-forced-io/panel-forced-io-name.png)

选择 `力控制变量 (Value)` 列，输入您要应用的新 IO 值，然后按下 `确认 (ENTER)` 键。

![](../../_assets/tp630/panel-forced-io/panel-forced-io-val.png)

如果您有更多强制 IO 条目要应用，请以相同方式输入。您最多可以输入 100 个条目。

![](../../_assets/tp630/panel-forced-io/panel-forced-io-multi.png)

面板标题栏上的 * 标记表示表已被修改且该修改尚未应用。  
按下 [F7: 应用] 按钮以应用强制 IO。  
当您在警告消息框中按下 `确定 (OK)` 按钮时，所有强制 I/O 条目将被应用。

![](../../_assets/tp630/panel-forced-io/panel-forced-io-apply.png)

面板标题栏上的 * 标记消失，您可以看到强制 IO 值已应用。  
标题栏上闪烁着红色 F 标记。这是一个强制 IO 正在应用的警告。

![](../../_assets/tp630/panel-forced-io/panel-forced-io-result.png)


* 在编辑过程中按 `SHIFT+DEL` 可删除一项。
* 您可以通过按 [F5: 上移]、[F6: 下移] 按钮来更改项的顺序。
* 如果在编辑表时单击 [F3: 取消编辑]，它将重新加载最后应用的状态。

完成测试和问题分析后，请务必按下 [F2: 清除] 按钮以完全清除强制 IO。

![](../../_assets/tp630/panel-forced-io/panel-forced-io-clear.png)

{% hint style="warning" %}
* 如果多个条目强制相同继电器（或叠加位）冲突的值，则强制为表中较低项的值。
* 当 ${cont_model} 控制器断电时，所有注册为强制 IO 的内容均被清除。

{% endhint %}
[__SOURCE](6-monitoring/2-io/7-memory-variables.md)
# 6.2.7 内存变量


在面板选择窗口中触摸 `[memory variables]`。
来自机器人语言的可访问变量显示在内部 PLC 继电器中。

![](../../_assets/tp630/pane-memory-variables_eng.png) 

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
      <ul>
          以十六进制、带符号十进制、长整型和浮点格式显示数据内存 (mw) 和系统内存 (sw) 的当前值。
      </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[start addr.]: 选择此按钮并在对话框中输入起始地址以在屏幕的第一行显示。</li>
          <li>[manual setting]: 在屏幕上选择所需的地址单元并单击此按钮以输入新值。</li>
          <li>[_mw/_sw]: 单击此按钮在显示 mw 和 sw 变量之间切换。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](6-monitoring/2-io/8-EC-device-info.md)
# 6.2.8 EtherCAT 设备

在面板选择窗口中，触摸 `[EtherCAT dev.]`。该监控面板显示从设备列表和设备的网络状态，这些设备与 ${cont_model} 控制器共同组成一个 EtherCAT 网络。在 EtherCAT 网络中，控制器主板作为主控。

![](../../_assets/tp630/pane-EC-device_eng.png) 


-	ENI-配置从设备数量：组成 EtherCAT 网络的从设备数量  
-	连接从设备数量：当前连接的从设备数量，应该与“ENI-配置从设备数量”相同  
-	设备：与主板连接的 EtherCAT 从设备的名称  
-	地址：EtherCAT 网络上的唯一地址  
-	连接  
    -	NG：网络故障  
    -	OK：网络成功  
-	模式  
    -	未知：由于网络故障无法检查当前状态  
    -	初始化：网络通道已初始化的状态  
    -	预操作：从设备只能使用非周期邮件进行通信的状态  
    -	安全操作：从设备只能传输数据(Tx PDO)的状态  
    -	操作：从设备可以同时传输和接收数据(Tx/RxPDO)的状态  
[__SOURCE](6-monitoring/3-job/README.md)
# 6.3 工作程序，机器人语言
[__SOURCE](6-monitoring/3-job/1-job.md)
# 6.3.1 工作

在面板选择窗口中触摸 `[job]`。要查看总程序列表，按 `[SHIFT]`+`[PROG]` 键将进入程序选择窗口。然后，您可以创建、删除和选择程序。

![](../../_assets/tp630/k-prg-select_eng.png)

您可以在任务编辑窗口中修改所选的工作程序。

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
        <ul> 基本信息和命令会显示出来。您可以检查并修改每个命令的详细情况。
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
            可以再次在 JOB 程序中执行自动缩进。</li>
          <li>在编写程序时，所选语句的参数值
            将显示在输入区域。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
有关如何管理和编写程序的详细信息，请参阅 "[3 Program Writing](../../3-programming/README.md?cont_model=${cont_model})"。
{% endhint %}
[__SOURCE](6-monitoring/3-job/2-hot-edit.md)
# 6.3.2 热编辑

这是在播放仍在运行时编辑程序而不停止它的功能。

{% hint style="warning" %}
* 当您编辑并应用当前处于自动操作中或将要调用的程序时，将从下一个周期（执行程序结束后）开始应用，并用编辑过的程序回放机器人。请务必谨慎，因为错误的编辑可能会导致重大事故，例如机器人与夹具之间的碰撞。
{% endhint %}
<br><br>

### 输入

触摸面板上的 `[hot edit]` 按钮，当前程序的热编辑窗口将打开。

![](../../_assets/tp630/pane-hot-edit-0_eng.png)

<br>

### 可编辑的类型

尽管操作与手动模式相同，但以下功能无法使用。

1) `[REC]` 键（记录隐藏的姿态MOVE）：显示“在热编辑过程中不允许操作”的消息。
2) `[POS. MOD]` 键：显示“在热编辑过程中不允许操作”的消息。

    ![](../../_assets/tp630/pane-hot-edit-1_eng.png)

<br>

### 反映

如果您完成了程序编辑，请点击 ![](../../_assets/tp630/bt-menu.png) 导航显示条左侧的按钮以打开弹出菜单，并选择 [hotedit: request to apply]。

![](../../_assets/tp630/pane-hot-edit-apply2_eng.png)

<br>

实际的反映时间显示在以下表格中。

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
    <td rowspan="2">无论是 <br>不运行<br> 还是运行</td>
    <td>不运行程序<br>(不包含在调用栈中的作业)</td>
    <td>立即应用</td>
  </tr>
  <tr>
    <td>运行程序<br>(包含在调用栈中的作业)</td>
    <td>在周期结束时<br>或RESET 0</td>
  </tr>
</tbody>
</table>
<br>

<br>
<u>V60.32-02 或之前版本：</u>

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
    <td>不运行</td>
    <td>-</td>
    <td>立即应用</td>
  </tr>
  <tr>
    <td rowspan="2">运行</td>
    <td>不运行程序<br>(不包含在调用栈中的作业)</td>
    <td>立即应用</td>
  </tr>
  <tr>
    <td>运行程序<br>(包含在调用栈中的作业)</td>
    <td>在周期结束时</td>
  </tr>
</tbody>
</table>

<br>

### 标题栏显示

  当前状态符号显示在热编辑窗口标题栏的右侧。

  \'*' 符号表示教学程序已被修改，并与当前运行的程序不同。

  ![](../../_assets/tp630/pane-hot-edit-apply3.png)

  \'>' 符号表示在程序运行时已请求热编辑。

  ![](../../_assets/tp630/pane-hot-edit-apply4.png)

  ' '(空白) 符号表示请求尚未反映，或已反映，因此程序与运行的程序相同。

  ![](../../_assets/tp630/pane-hot-edit-apply5.png)

<Br>

### 不同程序选择

当您按下 `[SHIFT]` + `[PROG]` 键时，您可以选择不同的程序。您还可以创建一个新程序。
[__SOURCE](6-monitoring/3-job/3-global-variable/README.md)
# 6.3.3 全局变量

显示所有全局变量的列表。您还可以创建/删除变量并编辑类型和值。


#### 打开全局变量面板

1. 分割屏幕并按左下角的 [选择] 按钮。

![](../../../_assets/tp630/panel-split.png)
&nbsp;
![](../../../_assets/tp630/panel-sel.png)

2. 在面板选择窗口中，触摸 `[全局变量]`。`全局变量 (global variables)` 面板打开。

![](../../../_assets/tp630/pane-gvar.png)


![](../../../_assets/tp630/panel-gvar/panel-gvar0.png)
[__SOURCE](6-monitoring/3-job/3-global-variable/1-basic-feature.md)
# 6.3.3.1 基本功能

##### 查找变量

如果由于变量数量众多而难以查找所需的变量，请在顶部的过滤器中输入变量名称的一部分。仅以您输入的过滤器字符串开头的变量将显示在屏幕上，方便您找到它们。

![](../../../_assets/tp630/panel-gvar/gv-find.png)

##### 更改变量的值（对于 bool, int, double, string 类型）

选择所需变量的 `值 (value)` 列并输入新值。
按 ENTER 键将所输入的值应用于变量。

![](../../../_assets/tp630/panel-gvar/gv-edit-value.png)

##### 更改变量的值（对于 pose, shift 类型）

选择所需姿态或位移变量的 `值 (value)` 列。

![](../../../_assets/tp630/panel-gvar/gv-edit-pose1.png)

按 ENTER 键打开姿态或位移属性窗口。
编辑后，点击 [F7: OK] 按钮。

![](../../../_assets/tp630/panel-gvar/gv-edit-pose2.png)

##### 更改变量类型

选择所需变量的 `类型 (type)` 列并按 ENTER。将出现如下所示的创建变量对话框。

![](../../../_assets/tp630/panel-gvar/gv-edit-type.png)

![](../../../_assets/tp630/panel-gvar/gv-create-var.png)

从类型列表中选择所需类型，然后点击 OK 按钮以更改变量的类型。请注意，如果类型更改，值将被初始化。

您还可以为多个变量选择类型并按 ENTER 一次性更改它们。
（您可以通过按 SHIFT+上/下箭头键选择多个连续单元格。或者，您可以在按住 CTRL 键的同时触摸多个单元格进行选择。）

![](../../../_assets/tp630/panel-gvar/gv-sel-multi-type.png)

##### 重命名变量

选择您想要的变量的 `名称 (name)` 列，然后打开软键盘以输入新名称。
按 ENTER 键将其更改为您输入的名称。

![](../../../_assets/tp630/panel-gvar/gv-edit-name.png)

##### 创建变量

在顶部的过滤器中，输入您想要创建的变量名称。

![](../../../_assets/tp630/panel-gvar/gv-new.png)

验证没有具有重复名称的变量后，点击过滤器旁边的 + 按钮。变量将使用默认类型 `int`（整数）创建。使用上述方法更改创建变量的类型。

![](../../../_assets/tp630/panel-gvar/gv-new2.png)

##### 删除变量

选择您想要删除的变量。
按 DEL (CTRL+BACKSPACE) 键显示确认/取消对话框。在确认变量名称后，按 OK 按钮。

![](../../../_assets/tp630/panel-gvar/gv-delete.png)
[__SOURCE](6-monitoring/3-job/3-global-variable/2-array-object.md)
# 6.3.3.2 数组和对象

##### 创建数组

我们现在将使用生成一个名为 `pos` 的 5x200 二维姿态数组变量的示例。使用上面描述的方法创建一个名为 `pos` 的变量。

![](../../../_assets/tp630/panel-gvar/gv-new-arr1.png)


选择 `类型 (type)` 列并按 ENTER 键。创建变量对话框如下所示。

![](../../../_assets/tp630/panel-gvar/gv-new-arr2.png)

在类型列表中选择 `姿势 (Pose)`。如果您输入 5,200 作为元素数量并按 OK 按钮，pos 的类型将更改为 Pose[5][200] 的数组。

![](../../../_assets/tp630/panel-gvar/gv-new-arr3.png)

{% hint style="warning" %}
`[Warning]` 请注意，定义一个过大的数组可能会导致保存或加载时间变长，并且在停电事件中可能无法自动保存。
{% endhint %}


##### 视图和更改数组元素值

数组变量的值仅显示为 []，而元素的值不显示。选择 `值 (value)` 列并按 ENTER 键或单击 [F5: sub.level] 按钮以展开数组到下一级并查看元素值。

![](../../../_assets/tp630/panel-gvar/gv-arr-level1.png)

您也可以按照上面描述的方法更改数组元素的值或类型。  

在二维数组 `pos` 中，`pos[0]` ~ `pos[4]` 也是数组。按 ENTER 或 [F5] 继续进入下一级。当前显示的数组的级别和索引可以在全局变量面板的标题栏中找到。

单击 [F4: up.level] 按钮或按 ESC 键返回上一级。

![](../../../_assets/tp630/panel-gvar/gv-arr-level2.png)

因为数组仅同时显示 100 个元素，所以默认情况下您只能看到 [0] 到 [99] 索引的范围。如果您更改左上角的起始索引编辑框的值，您可以看到其他范围的元素。例如，如果您在 `/pos[4]` 的起始索引中输入 190，您可以看到 [190]~[199] 的元素。

##### 视图和更改对象属性值

选择对象变量的 `值 (value)` 列并按 ENTER 键或单击 [F5: sub.level] 按钮以展开对象到下一级并查看属性值。操作方法与数组变量类似。不过，Startup Index 编辑框不使用。

![](../../../_assets/tp630/panel-gvar/gv-obj2.png)




<br>

##### 固定变量

例如，您已经在全局变量窗口中创建了大量名为 `weld_points` 的姿态，通过执行下面的赋值语句可以删除所有数据。

```python
weld_points=0
```

通过将变量指定为固定，您可以防止这个错误。

![](../../../_assets/tp630/panel-gvar/fixed-var.png)

如果您在全局变量窗口的顶层选择一个数组变量并按 [F4: toggle fixed]，类型将从 'array' 更改为 'F.array' (固定数组)。  
如果指定为固定变量，不能分配其他值。当 `weld_points` 是一个固定的二维数组时，下面每个赋值语句的结果与注释相同。


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

变量值也作为文件保存，因为它们必须在断电时仍然保留，并且全局变量根据类型以两种形式存储：

<table>
  <thead>
    <tr>
      <th style="text-align:left">类型</th>
      <th style="text-align:left">路径名</th>
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
      <td style="text-align:left">所有其他全局变量保存为一个文件。</td>
    </tr>
	</tbody>
</table>

<br>

##### vars/.csv 文件

当您在文件管理器中打开文件夹 `MAIN/project/vars/` 时，会创建一个名为 `weld_points.csv` 的文件。指定的变量作为预定义的创建一个与变量名称相同的 .csv 文件，当从预定义中释放时，该文件会自动删除。

![](../../../_assets/tp630/panel-gvar/csv0.png)

通过 USB 存储器或 FTP 复制此文件，并在您的 PC 上打开。 .csv 文件是表示以逗号分隔值的非常简单的文本格式标准。

参考： [Wikipedia: Comma-separated values](https://en.wikipedia.org/wiki/Comma-separated_values)

.csv 文件表示一个二维表。列由逗号分隔，行由换行符分隔。

![](../../../_assets/tp630/panel-gvar/csv1.png)

包含构建 `weld_points` 二维数组的过程的 csv 文件，按顺序排列。

对于每一行，第一列是索引，第二列是类型，第三到最后几列是值。第一行描述作为表头。

第二行是创建顶层的行，即 `weld_points` 本身。因此，索引列为空，类型为数组，数字为 10。换句话说，创建了 weld_points[10]，并用零的默认值填充了 10 个元素。

```python
, , array, 10
```

随后的行生成并分配姿态类型值给 `weld_points[0]` 的元素。

```python
[0][0][0], Pose, 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
[0][0][1], Pose, 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
...
```

如果对 `weld_points[0]` 执行 100 行，则随后的行将按照如下所示的 `weld_points[1]` 的操作：

```python
[1][1], array; 100
[1][1][0], Pose; 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
[1][1][1], Pose; 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
[1][1][2], Pose; 0.000, 0.000, 0.000, 0.000, 0.000, 0.000, "base"
...
```

您可以双击文件管理器中的 .csv 文件，用 Microsoft Excel 打开并编辑它。编辑完成后，按 `Ctrl+S` 或 `保存 (Save)` 按钮保存。

![](../../../_assets/tp630/panel-gvar/csv2.png)

在 Excel 中保存会导致多余的逗号，如下所示，并且坐标系统中的引号消失，从而导致格式的轻微变化。这是因为 Excel 这样处理 .csv。但是，${cont_model} 控制器也识别那种格式，因此没有关系。

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

您可以将编辑后的文件再次覆盖到 `MAIN/project/vars/` 中，但它不会自动反映在内存中。

当您在全局变量窗口中单击 [F2: load all] 按钮时，`vars/` 文件夹中的所有变量文件都将重新加载到内存中。
(请注意，删除变量文件并单击 [F2: load all] 也将删除内存中的相应变量。)

![](../../../_assets/tp630/panel-gvar/fixed-var.png)
[__SOURCE](6-monitoring/3-job/4-local-variable.md)
# 6.3.4 本地变量

显示当前调用帧的所有本地变量的列表。您无法创建/删除变量或更改变量名称或类型，但可以编辑值。


1. 拆分屏幕并按左下角的 [选择] 按钮。

![](../../_assets/tp630/panel-split.png)
&nbsp;
![](../../_assets/tp630/panel-sel.png)


2. 在面板选择窗口中，触摸 `[local variable]`。`局部变量 (local variables)` 面板打开。

![](../../_assets/tp630/pane-lvar.png)


3. 检查变量名称、类型和值。改变变量值的方法与前面章节中描述的全局变量相同。

![](../../_assets/tp630/pane-lvar-mon.png)
[__SOURCE](6-monitoring/3-job/5-watch.md)
# 6.3.5 监视

您可以将变量或表达式注册到监视面板，以监视或更改值。

#### 打开监视面板

1. 分割屏幕并按左下角的 [选择] 按钮。

![](../../_assets/tp630/panel-split.png)
&nbsp;
![](../../_assets/tp630/panel-sel.png)

2. 在面板选择窗口中触摸 `监视 (Watch)`。各种数据窗口将打开。

![](../../_assets/tp630/panel-watch/panel-watch.png)

![](../../_assets/tp630/panel-watch/panel-watch-mon.png)

#### 如何使用

在顶部输入框中输入所需的变量或表达式，然后单击 '+' 按钮以将新项输入到表格中。

![](../../_assets/tp630/panel-watch/panel-watch2.png)

您可以通过再次单击 `名称 (Name)` 列来修改您输入的变量名称或表达式。

![](../../_assets/tp630/panel-watch/panel-watch-rename.png)

如果您在 `力控制变量 (Value)` 列中单击以输入新值，将更改该变量的值。更改表达式的值将被忽略。

选择姿态/偏移变量或表达式的 `力控制变量 (Value)` 列，然后按 `确认 (ENTER)` 键以打开姿态/偏移属性窗口以查看和修改值。

![](../../_assets/tp630/panel-gvar/gv-edit-pose2.png)

要删除一行，选择该行并按 `SHIFT+DEL` 键。

如果您在底部的 F 按钮上按 [F7: Save all] 按钮，将输入的变量和表达式列表保存到 `cfg/watch.json` 文件中。该文件在电源重启时会自动加载。
您还可以通过 FTP 将列表接收至外部 PC 进行编辑。如果您用 `cfg/` 文件夹覆盖编辑过的文件并单击 [F1: Load All] 按钮，则会将其应用于监视面板。

![](../../_assets/tp630/panel-watch/panel-watch-fbt.png)

单击 [F2: swap up] 和 [F3: swap down] 按钮以在当前选择的行与顶部和底部行交换时移动其位置。

在各种数据窗口中共有 10 页，因此您可以分组和管理想要显示的变量或表达式。单击 [F4: Page] 按钮以显示下一页，单击 `SHIFT`+[F4: Page] 按钮以显示上一页。

您可以使用 [F6: sub.level] 按钮或 `确认 (ENTER)` 键查看数组或对象的元素，使用 [F5: up.level] 按钮或 `ESC` 键可以上移到上一级。

您可以在 `起始索引 (Start Index)` 编辑框中输入值，以从特定索引显示数组。 ([全局变量](3-global-variable/README?cont_model=${cont_model}) 窗口具有相同的操作方法。)

{% hint style="warning" %}
* 为了更新结果值的显示，表达式会在快速周期内不断计算。请小心不要在表达式中包含导致系统特定创建或更改的函数，例如 mkucs()。
{% endhint %}
[__SOURCE](6-monitoring/3-job/6-call-stack.md)
# 6.3.6 调用栈

在面板选择窗口中点击 `[Call Stack]` 显示调用栈窗口。为了理解本节的内容，必须先理解 `call`~`return` 语句和 hrscript 的局部变量。

[调用、跳转语句和子程序](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/3-flowcontrol-subprogram/7-call-jump/README?cont_model=${cont_model})

[局部变量](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/3-flowcontrol-subprogram/8-local-global-var/1-local-variables?cont_model=${cont_model})


### 机器人语言的调用和返回

在机器人语言中，可以通过 `call` 语句调用子作业程序。当执行 `end` 或 `return` 语句时，子程序返回到调用它的 `call` 语句的下一个语句位置。例如，在下图中，可以看到作业 5 调用作业 8，进入 `return` 语句，然后继续执行作业 5 的 `call` 语句的下一个语句。

![调用和返回子作业](../../_assets/call-return.png)

画在程序旁边的容器形状是称为调用栈的存储空间。调用栈构建了当前正在运行程序的调用帧。调用帧包含一组实际参数和局部变量以及作业程序的返回地址。  
因为在调用子程序时新的调用帧被压入栈顶，调用它的程序的局部变量被保存，并准备了新的局部变量空间。  
当子程序返回时，顶层调用帧被丢弃（弹出），下面的调用帧再次成为顶层。因为调用帧保留了调用前的实际参数和区域变量，并且还有返回的位置信息，因此被调用程序可以继续执行在调用前正在做的任务。


### 调用栈面板

可以在调用栈面板中查看当前调用栈的内容。
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
# 做一些事情
end
```

0009_check_sensor.job
```python
param id
var sensor_value
# 做一些事情  --------- (B)
end
```

在作业编辑窗口、调用栈面板和局部变量面板打开的情况下，如果当前程序处于作业 5 的 `for`~`next` 循环中第 3 次执行 `call` 语句并执行到 (B) 位置，教导挂板屏幕将显示如下状态。

![作业编辑、调用栈、局部变量](../../_assets/call-stack.png)


调用栈的底部帧是作业 1，中间帧是作业 5，顶部帧是作业 9。> 形状的光标指向作业 9，参数 ` (id)` 和局部变量 `sensor_value` 的值显示在局部变量面板中。因此，可以检查作业 9 是由作业 5 调用的，作业 5 是由作业 1 调用的。  
如果想查看作业 5 的调用位置，选择作业 5 的帧并按 `确认 (ENTER)` 键。作业编辑面板中的光标会立即移动到 (A) 位置以显示其被调用的位置。局部变量面板显示作业 5 的帧内容，即参数 `模式 (mode)` 和局部变量 `sensor_id`，其值分别为 12 和 3。

![作业编辑、调用栈、局部变量 - 2](../../_assets/call-stack2.png)

通过选择被调用作业的帧，可以轻松理解到目前为止的程序流程。

{% hint style="warning" %}
`[caution]` 在执行 Step-FWD 或播放时，务必在恢复操作时将 > 光标恢复到顶部帧位置。否则，作业光标的位置将被视为已更改，调用栈将被初始化。
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
# 6.3.8 程序预约执行

对于此监控，需要预设。您必须在 `系统 - 2:控制参数 - 7:程序预约执行 (system - 2:Control parameter - 7:Program reservation execution)` 页面选择注册号为 20EA 或 1EA。

![](../../_assets/tp630/ctrl-prog-reserve_eng.png)

在面板选择窗口中，触摸 `[program reserve]`。然后，计划程序执行窗口将出现。

当程序通过外部信号安排并按照计划顺序执行时，您可以在已调度程序的列表中检查和更改状态。

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
        <p>已调度程序的列表。您可以调度 1&#x2013;20 个程序。</p>
        <ul>
          <li>当在远程模式下执行的程序被终止时，程序将会依据计划顺序自动执行。</li>
          <li>当已调度程序的执行完成后，这些程序将会从列表中删除。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[编辑]</b>：您可以编辑已调度程序的列表。</li>
          <li><b>[插入]</b>：您可以将按计划执行的程序添加到已调度程序的列表中。</li>
          <li><b>[删除]</b>：您可以从已调度程序的列表中删除已调度程序。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>



{% hint style="info" %}
* 仅当传感器同步功能的同步状态设置为传送带或压机时，`[Program reserve]` 项目才会被激活。
* 如果`[system - 2: Control Parameter - 8: Program reserve]` 菜单中的`[Applied Register Count]`选项设置为禁用，则`[Program reserve]` 项目将不会被激活。
* 有关已调度程序执行的详细信息，请参阅 "${cont_model} 控制器已调度程序执行功能手册。"
{% endhint %}
[__SOURCE](6-monitoring/4-system/README.md)
# 6.4 系统
[__SOURCE](6-monitoring/4-system/1-system-spec.md)
# 6.4.1 系统特征

在面板选择窗口中，触摸 `[System character]`。然后，系统特征窗口将出现。

您可以查看机器人系统的所有各种数据或仅查看特定类型信息的数据。

![](../../_assets/tp630/pane-syscharacter_eng.png)

| No. | 描述 |
| :--- | :--- |
| ![](../../_assets/c1.png) | 显示机器人系统的数据。您可以通过选择上面显示的单个类型的信息来查看特定类型的详细数据。 |
| ![](../../_assets/c2.png) | `[clear]`：对于每个轴的运动以外的其他项目，您可以按类型将系统数据的最大值初始化为当前值。 |

{% hint style="info" %}
系统特征监控功能仅在工程师模式下可用。
{% endhint %}

{% hint style="warning" %}
* 在工程师模式下，工程师模式图标 \(![](../../_assets/eng-mode.png)\) 将在状态栏中闪烁。
* 请谨慎操作，因为如果设置不正确，机器人系统可能会出现严重问题。
{% endhint %}

<Br>

### 初始化

您可以通过选择您想要的信息类型来初始化数据的最大值。

1. 触摸系统属性窗口底部的 `[Clear]` 按钮。

2. 触摸您想要初始化的信息类型。然后，所选项目的最大值将初始化为当前值。

    ![](../../_assets/tp630/pane-syscharacter-clear_eng.png)
[__SOURCE](6-monitoring/4-system/2-system-diagnosis/README.md)
# 6.4.2 系统诊断

触摸 `System Diagnostics` 在面板选择窗口中。
第一次执行时，会出现刹车诊断屏幕。

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
        <p> 在选择 <strong>[System Diagnostics]</strong> 面板时，可以通过点击下面的按钮切换到其他诊断项目。 </p> 
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
[__SOURCE](6-monitoring/4-system/2-system-diagnosis/2-gas-pressure-check.md)
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
[__SOURCE](6-monitoring/4-system/3-system-task.md)
# 6.4.3 任务监视器


在面板选择窗口中，触摸 `[Task monitor]`。然后，任务窗口将出现。

您可以查看每个任务的操作周期和执行时间信息。

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
          <ul>显示每个任务的操作周期和执行时间信息 </ul>
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
          <li><b>[计数器]</b>: 通过检查递增的计数器，您可以将任务视为正常。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](6-monitoring/4-system/4-hw-monitoring.md)
# 6.4.4 硬件

 在面板选择窗口中，触摸 `[hardware]`。您可以监控 COM 模块的当前电压和温度。如果状态值超出容差，将在 24 小时内发出警告信息。

 ![](../../_assets/tp630/pane-hw-monitoring_eng.png)
 
 
- 如果您想更改容差，请选择相应的单元格并进行编辑。然后，按 [Save Min/Max] 按钮。
- 如果您想使用默认值进行初始化，请按 [Reset Min/Max] 按钮。
[__SOURCE](6-monitoring/5-appl/README.md)
# 6.5 高级功能和机器人应用
[__SOURCE](6-monitoring/5-appl/1-sensor-sync.md)
# 6.5.1 传感器同步

在面板选择窗口中触摸 `[Sensor Sync]`。然后，传感器同步窗口将出现。

您可以查看与输送机相关的信息并按下同步功能。通过在 `[system - 4: Application Parameter - 4: Sensor Sync] ([system  - 4: Application Parameter  - 4: Sensor Sync])` 菜单中将同步状态设置为输送机或按压，可以激活传感器同步功能。

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
      <td style="text-align:left"> <ul>显示与所选传感器的输送机和按压同步功能相关的信息</ul></td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[传感器 #1]</b>: 您可以通过触摸下拉菜单选择要监控的传感器。</li>
          <li><b>[手动重置]</b>: 您可以手动删除各种与传感器相关的数据（编码器脉冲、传感器位置、传感器速度、工件进入计数、同步播放状态等）。</li>
          <li><b>[极限开关操作]</b>: 当您输入时，您可以使用此功能。</li>
          <li><b>[工位输入]</b>: 您可以手动输入传感器位置值（线性：mm，圆形：度）。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>



{% hint style="info" %}
有关传感器同步功能的详细信息，请参阅 ["${cont_model} 传感器同步功能手册。"](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/zh/README?cont_model=${cont_model})
{% endhint %}
[__SOURCE](6-monitoring/5-appl/2-coldet-monitoring.md)
# 6.5.2 碰撞检测监控

 ![](../../_assets/tp630/coldet_monitoring_pane.png)
 ![](../../_assets/tp630/coldet_monitoring.png)
 
#### 描述
* 碰撞检测监控

#### 参数
 - [灵敏度] : 比率值越高，碰撞检测越灵敏。 (0: 禁用) [0~200]
   - 可以在常规选项卡中设置 [系统- 3:机器人参数>14:碰撞检测]  
 - [外部扭矩]-[当前] : 当前估计的外部扭矩 [Nm]
 - [外部扭矩]-[最大] : 当前外部扭矩的最大值 [Nm]
 - [参考] : 阈值扭矩 [Nm]
 - [最大/参考] : 比率 [最大] 与 [参考]，如果该值超过1，轴向冲击将发生。
[__SOURCE](6-monitoring/5-appl/10-spot.md)
# 6.5.10 点焊数据

在面板选择窗口中触摸 `[spot]`。
这将显示点枪轴数据、输入/输出信号和点焊的操作信息。

![](../../_assets/tp630/pane-spot_eng.png) 

<br>

{% hint style="info" %}
 参阅点焊手册中的 "[3.1 监控](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/3-Related-functions/3-1-monitoring/README?cont_model=${cont_model})" 获取更多详细信息。
{% endhint %}
[__SOURCE](6-monitoring/5-appl/11-tool-change.md)
# 6.5.11 伺服工具更换

在面板选择窗口中，触摸 `[servo tool change]`。这将显示伺服工具和编码器电源输入/输出状态在使用伺服工具更换功能时的状态。

![](../../_assets/tp630/pane-tool-change_eng.png) 

<br>

{% hint style="info" %}
 请参阅 ["${cont_model} 控制器伺服工具更换功能手册"](https://hrbook-hrc.web.app/#/view/doc-svtool-change/zh/README?cont_model=${cont_model}) 以获取更多详细信息。
{% endhint %}
[__SOURCE](6-monitoring/5-appl/20-arc.md)
# 6.5.20 弧焊数据

请参阅弧焊手册中的 "[7. 焊接数据监控](https://hrbook-hrc.web.app/#/view/doc-arc-weld/zh/7_Monitoring/README?cont_model=${cont_model})"。
[__SOURCE](6-monitoring/5-appl/28-forcecontrol-monitoring.md)
# 6.5.28 力控制监控
 
![](../../_assets/tp630/force_monitoring.png)

#### 描述 
* 在力控制的情况下，此监控数据显示估计的 [外部力量] 
 
#### 参数 

 - [cartesian] : 笛卡尔空间中的外部力量或扭矩
    - 在 fctrl 函数的情况下 : 机器人坐标
    - 在 softxyz 函数的情况下 : 机器人坐标
    - 在 softjoint 函数的情况下 : 不显示 
 - [joint] : 关节空间中的外部扭矩    
    - 在 fctrl 函数的情况下 : 不显示
    - 在 softxyz 函数的情况下 : 不显示
    - 在 softjoint 函数的情况下 : 关节坐标 
[__SOURCE](6-monitoring/6-safety-funtion.md)
<script id="page-config" type="application/json">
{
	"permittedStrs": ["Hi7"]
}
</script>

# 6.6 安全功能

{% hint style="info" %}
此功能支持Hi7控制器。
{% endhint %}

在面板选择窗口中，触摸`[安全功能]`。然后，安全功能状态窗口将出现。
您可以检查安全功能、手动速度、停止时间、停止距离、MCU-A和MCU-B的状态。

![](../_assets/image_552.png)

{% hint style="info" %}
* 有关安全功能的详细信息，请参阅 "[SafeSpace2.0手册](https://hrbook-hrc.web.app/#/view/doc-safespace2.0/zh/README)"。
{% endhint %}
[__SOURCE](7-system/README.md)
# 7. 系统

在“系统”中，您可以检查和设置用户信息及各种参数信息。
[__SOURCE](7-system/1-setting-menu.md)
# 7.1 在“system”中的菜单使用

1. 在手动或自动模式下，触摸功能按钮栏上的 `[system]` 按钮。然后，程序的设置菜单将显示。

    ![](../_assets/tp630/sbt-system_eng.png)

2. 通过选择所需菜单，您可以检查和设置用户信息及各种参数信息。

    ![](../_assets/tp630/sbt-system-menu_eng.png)

* `[1: User Environment]`：您可以检查和设置各种用户条件。
* 
  `[2: Control Parameter]`：您可以设置控制器和输入/输出信号、通信信息、机器人准备好信号条件、原点信号和坐标系统的各种条件。

* 
  `[3: Robot Parameter]`：您可以设置与机器人操作相关的各种数据，如每个轴的原点和操作范围。

* `[4: Application Parameter]`：您可以检查和设置用于机器人应用功能的各种参数。
* 
  `[5: Initialize]`：您可以执行机器人系统的初始设置。您还可以初始化串行编码器。

* 
  `[6: Auto Calibration]`：您可以使用教导机器人正确使用的程序以及将自动操作的运动来校准机器人的轴原点、工具长度、负载质量和基轴方向等。
[__SOURCE](7-system/2-user-environment.md)
# 7.2 用户环境

您可以检查和设置各种用户条件。

1. 触摸 `[1: 用户环境]` 菜单。然后，用户环境设置窗口将出现。

2. 设置用户环境后，触摸 `[确定]` 按钮。

    ![](../_assets/tp630/system-user-environ_eng.png)

* `1: 姿势记录类型 (1: Pose record type)`: 您可以设置记录为隐藏姿势的步骤的位置记录类型。 ("[2.3.1.2 Pose](../2-operation/3-step/1-step-cmd-param/2-pose.md)")
  * `[基准]`/`[机器人]`/`[轴角]`: 您可以根据基准坐标、机器人和轴角值记录步骤的位置。

  * `[用户]`: 您可以在用户坐标系中记录该位置。
* `2: 删除指令确认 (2: Confirmation in deleting commands)` 您可以设置在手动模式下删除语句时是否显示删除确认窗口。

* `3: 强制释放“等待”指令`: 设置在等待“等待”指令时是否使用 `[SHIFT]` + [rel.WAIT] 键强制释放等待状态。
* `4: 程序选通信号启用 (4: Program strobe signal use)`: 在通过接收外部数字信号选择外部程序时，您可以设置选择外部程序的时间。

  * `[禁用]`: 只通过读取外部程序选择信号选择外部程序

  * `[启用]`: 在输入程序选通信号时，允许通过读取外部程序选择信号选择外部程序

* `5: 再现程序的外部更新 (5: Ext. update of playback prog.)`: 您可以设置是否允许外部 \(PC\) 修改正在回放的程序，并允许将其下载到控制器 \(关于正在回放的程序编号，下载的程序将从下一个循环开始应用\)。

{% hint style="warning" %}
如果正在回放的程序被外部 \(PC\) 修改并下载到控制器中，可能会导致产品故障或异常。请联系我们的客户支持团队咨询专家或工程师。
{% endhint %}

* `[6: 碰撞传感器处理]`: 您可以设置当碰撞传感器运行时停止机器人的方法。
  * `[(1) 紧急停止]`: 机器人将进入紧急停止模式，机器人处于掉落的电机关闭状态。

  * `[(2) 停止]`: 机器人将进入正常停止模式，机器人保持在电机开启状态。

* `[7: 字节中的信号显示]`: 您可以通过选择 `[启用]` 在字节单位中显示信号地址。
  * '输入信号分配' 页面根据您的选择发生如下变化。

    ![](../_assets/tp630/system-user-environ-byte-index_eng.png)

* `8: 停止信号的手动操作`: 您可以设置在输入外部停止信号时是否启用手动操作。

* `[9: 教学挂件断开]`: 您可以从控制器断开教学挂件，以在自动模式下操作机器人。

  * 如果设置为 `分离 (Disconnect)`，当教学挂件与主板之间的通信断开时，不会发生 "E2800 教学挂件操作异常" 错误。(当通信断开时，机器人仍然可以操作。)

  * 在 `连接 (Connect)` 状态下，您可以设置超时期限以确定通信是否丢失。

  * 当设置为 `分离 (Disconnect)` 并且教学挂件与控制器断开时，供电后，控制器将识别当前模式为远程模式，允许机器人通过外部电机开启和外部启动进行自动操作。

  * 如果您将其设置为 `连接 (Connect)`，教学挂件与主板之间的通信故障将触发 "E2800 教学挂件通信错误"，导致电机关闭。(在输入工程师代码 (R314) 后，您可以配置通信超时时间。)

  * 由于紧急开关和模式转换开关通过信号线分别连接到教学挂件，因此您必须适当地布线此信号线。

  * 将 CNRTP 连接器引脚 #9 (Auto) 连接到 #2 (M1)，将引脚 #5 (紧急停止 1) 连接到 #2 (M1)，并使用专用的 CNRTP 连接器，将引脚 #6 (紧急停止 2) 连接到 #1 (P1)，而不是教学挂件。
[__SOURCE](7-system/3-control-parameter/README.md)
# 7.3 控制参数

您可以设置控制器的各种条件，并设置输入/输出信号、通信信息、机器人准备就绪信号条件、原点信号和坐标系统。

1. 触摸`[2: Control parameter]`菜单。然后，控制参数菜单将出现。

2. 选择所需菜单并检查和设置控制器的各种条件。

    ![](../../_assets/tp630/ctrl-menu_eng.png)
[__SOURCE](7-system/3-control-parameter/1-control-env-setting.md)
# 7.3.1 控制环境设置

您可以设置控制器的各种条件并执行必要的操作。

1.	触摸 `[2: 控制参数 - 1: 控制环境设置] ([2: 控制参数  - 1: 控制环境设置])` 菜单。

2.	在设置每个控制环境条件后，触摸 `[OK]` 按钮。

    ![](../../_assets/tp630/ctrl-environment-setting_eng.png)   

* `[节能功能]`: 您可以设置是否使用节能功能并设置等待时间。

  当启用节能功能时，如果机器人在自动模式下处于长时间的操作停止状态，例如等待启动或等待输入信号，当等待时间到达时，电机的电源将被切断，有助于节省能耗。当机器人输入操作命令时，节能功能将自动禁用，从而为电机供电并使机器人操作。

{% hint style="info" %}
激活/禁用节能功能的过程中可能会出现延迟。在期待机器人的速度时，您应将节能功能设为禁用。
{% endhint %}


* `[自动模式下的路径恢复]`: 您可以设置自动模式下路径恢复的允许距离和允许角度。

  在路径恢复过程中，如果距离和角度超出设定的允许范围，将会检测到错误。如果允许距离设置为1，将不会进行路径恢复。


* `[冷却风扇关机时间]`: 当机器人在操作时，由于再生电阻，控制器内部的温度会上升，必须操作冷却风扇以防止温度升高。

  当机器人不在操作时，控制器内部的温度不再上升，因此此时没有理由让冷却风扇工作。相反，当冷却风扇运行时，只会产生一些不良影响，例如风扇寿命缩短、噪音产生和能耗增加。

  当机器人处于操作状态（电机开启）时，冷却风扇必须立即运行。当机器人处于不可以操作状态（电机关闭，节能操作）时，冷却风扇在经过一定的时间后不再运行。如果冷却风扇没有立即运行，控制器内部的温度会由于再生电阻的潜热而升高。

  控制冷却风扇开/关操作的信号输出在 `[系统/控制参数/输入/输出信号设置/输出信号分配]` 菜单的“冷却风扇控制”项中进行设置，并使用这个输出信号创建控制冷却风扇电源的电路。必须进行配置。

  如果将“冷却风扇关闭操作时间”设置为0或将“冷却风扇控制”输出信号设置为-1，则冷却风扇始终运行。


* `[互锁错误时间]`: 此功能设置输入信号的最长等待时间。 <br>
  如果输入信号的待机时间在播放过程中超过了指定的时间，将输出一个互锁错误信号。这个指定的时间就是互锁异常时间。

  互锁错误信号是分配给 `[系统/控制参数/输入/输出信号设置/输出信号分配]` 菜单中“互锁异常警告”的信号。


* `[第一步安全移动]`: 启动机器人时，设置是否将第一次移动限制为安全速度，并以当前设定的速度移动。
  * 启用 : 以安全限制速度移动。
  * 禁用 : 以当前设定的速度移动。

  出于安全原因，机器人在启动第一步时以安全速度移动是基本要求。特殊作业如密封或喷涂可能导致质量问题，因此仅在此类情况下使用。


* `[PLC执行时间比率]`: 在使用嵌入式PLC时，您可以调整控制器内部的PLC执行时间。控制器每5ms内部执行一次PLC梯形程序，因此请设置分配多少PLC执行时间。这个比率越大，会导致PLC程序的扫描时间缩短。但是，如果设置得太大，CPU执行时间可能会不足，并且可能会发生任务执行时间超限错误。

* `[循环时间优化模式]`: 此功能在自动播放期间减少机器人的步骤移动时间，以提高生产力。
  - 启用
    - 动态调整加速/减速曲线和最大速度，以实现更快的移动。
    - 应用动态运动调整

  - 禁用
    - 使用预定义的加速、减速和最大速度设置。
    - 在标准运动轮廓模式下运行

  - 动态运动比率 (`0 ~ 1.0`)
    - `0`: 禁用（静态运动）
    - `1 ~ 1.0`: 调整动态运动的强度
    - 更高的值适用更激进的速度和加速度优化


{% hint style="info" %}
对于循环时间至关重要的过程（例如，重复的取放），应用高动态运动比率可以帮助改善吞吐量。
{% endhint %}

{% hint style="warning" %}
请注意，更高的值可能会导致机械振动或触发过扭矩故障，特别是在高负载或快速方向变化时。
{% endhint %}
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/README.md)
# 7.3.2 输入/输出信号设置

1. 触摸 `2: 控制参数 - 2: 输入/输出信号设置 (2: 控制参数  - 2: 输入/输出信号设置)` 菜单。然后，输入/输出信号设置菜单将出现。

2. 选择所需菜单并设置输入/输出信号属性和信号分配等。

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

您可以设置一般输入信号的逻辑、脉冲和名称。

1. 触摸 `2: 控制参数 - 2: 输入/输出信号设置 - 2: 输出信号属性 (2: 控制参数  - 2: 输入/输出信号设置  - 2: 输出信号属性)` 菜单。

2. 检查并设置一般输入信号列表，然后触摸 `[OK]` 按钮。

    ![](../../../_assets/tp630/ctrl-outsignal-attri_eng.png)

* `[Append]`: 您可以将新的一般输出信号添加到列表中。
* `[Delete]`: 您可以从列表中删除一般输出信号。
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/3-io-signal-set-info.md)
# 7.3.2.3 输入/输出信号设置信息

* `[Signal]`: 应用属性的信号。fb块信号可以通过顺序输入块编号、小数点和信号编号来指定。

  例如，如果您想指定块fb1的信号35，可以通过输入1.35来设置。

* 
  `[Negative Logic]`: 一般输入/输出信号的正逻辑和负逻辑如下所示。

![](../../../_assets/image_457.png)

* `[Pulse Count]`: 脉冲计数。这是脉冲的计数。如果设置为1到100之间的值，将发生脉冲输出；如果设置为0，将发生延迟输出。
* 
  `[Pulse On]`/`[Pulse Off]`: 这是脉冲输出或延迟输出发生时输出信号的开启状态时间和关闭状态时间。

  根据脉冲属性值的脉冲输出示例如下。

* 
  脉冲输出：计数：3。开启状态时间：1秒。关闭状态时间：0.2秒

![](../../../_assets/image_468.png)

* 延迟输出：计数：0。开启状态时间：1秒。关闭状态时间：0.5秒

![](../../../_assets/image_464.png)

* `[Name]`: 一般输入/输出信号的名称
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/4-input-signal-assign.md)
# 7.3.2.4 输入信号分配

您可以使用控制器输入信号远程控制控制器的状态或操作。分配远程控制项中的输入信号编号的方法如下。

1. 触摸 `2: 控制参数 - 2: 输入/输出信号设置 - 3: 输入信号分配 (2: 控制参数 - 2: 输入/输出信号设置 - 3: 输入信号分配)` 菜单。

2. 在远程控制项中输入输入信号编号后，触摸 `[OK]` 按钮。

    ![](../../../_assets/tp630/ctrl-insignal-assign_eng.png)

* `[重置所有]`: 您可以重置分配给所有远程控制项的输入信号编号。
* 
  `[重置一个]`: 您可以重置分配给选定远程控制项的输入信号编号。

* 
  `[重置通道]`: 您可以初始化设定输入信号的输入通道。通道由 fb0 到 fb9 组成，在 fb0 的情况下，显示中将省略 fb0。

* 
  `[S]`: 您可以在使用远程控制作为系统输入信号时指定系统信号。系统信号由 "s+编号" 组成，将字母 s 与信号编号结合。例如，您可以将系统信号 49 设置为 s49。
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/5-input-signal-set-info.md)
# 7.3.2.5 输入信号设置信息

#### 远程模式

当教学挂件的模式开关选择为远程 \(![](../../../_assets/sb-remote.png)\) 时，应启用相应的信号以选择远程模式。如果相应信号被关闭，将选择内部模式。一般来说，如果教学挂件的模式开关选择为远程 \(![](../../../_assets/sb-remote.png)\)，用户希望选择远程模式，因此基本值设置为 254，且相应信号将在输入信号属性中指定为负逻辑。

#### 手动 \(教学\) 模式

在选择远程模式时，如果相应信号被启用，将处于在远程模式下手动操作机器人的状态。然而，通常情况下，很少有在这种状态下操作机器人的情况，该模式不常使用。

#### 自动 \(播放\) 模式 

在选择远程模式时，如果相应信号被启用，将处于在远程模式下自动操作机器人的状态。然而，通常来说，如果教学挂件的模式开关选择为远程 \(![](../../../_assets/sb-remote.png)\)，用户希望在远程模式下自动操作机器人，因此基本值设置为 255，且相应信号将在信号属性中指定为负逻辑。

#### 外部启动

这用于在远程自动模式下启动机器人。

#### 外部停止 

这用于在远程自动模式下停止机器人。

#### 外部程序选择 

当机器人被外部启动时，读取程序选择位并将其确定为外部程序的时机取决于是否使用了触发信号。

* 当程序触发信号使用设置为启用：如果在有外部启动输入时程序触发信号为开启，则将读取程序选择位，读取的值将被确定为程序编号。

![图 52 当程序触发信号设置为 \<启用\> 时外部程序选择的示意图](../../../_assets/image_438.png)

* 当程序触发信号使用设置为禁用：在有外部启动输入后，将读取程序选择位，如果该值在 90 ms 内没有变化，将被确定为程序编号。

![图 53 当程序触发信号设置为 \<禁用\> 时外部程序选择的时序图](../../../_assets/image_465.png)

#### 程序选择位和二进制/离散 \(关 -> 二进制\)

程序选择位是输入外部启动信号时选择要执行的程序的信号组合。它仅在 TP 中指向 Header 或 End 的步骤时应用。当程序正在执行时，程序将执行到底。

二进制/离散信号是确定程序选择位解释的选项，如果设为 0，则被识别为二进制，如果设为 1，则被识别为离散。

例如，如果程序选择位设置如下，执行的 JOB 示例如下。

![](../../../_assets/image_436.png)

#### 外部复位

此功能用于通过外部信号执行与从教学挂件执行 R0 步进计数器复位功能相同的操作。当机器人启动时，该功能将不操作。如果该功能正常运行，执行位置将移动到程序的开头，并且各种错误或警告的发生状态将被清除。有关该功能的信息，请参见 "[8.2 R0用于复位步进计数器](../../../8-r-code/2-r0.md)"。

#### 

#### 低速命令

此功能用于通过外部信号将机器人移动速度限制在安全速度 \(250 mm/s\) 以内。

#### 碰撞传感器

此功能用于检测机器人的碰撞并停止机器人。结合 `[System - 1: User Environment - 6: Collision Sensor]` 菜单中的设置，将确定停止机器人的条件和信号逻辑。

#### 错误/警告信号清除

此功能用于通过外部信号清除各种错误和警告的发生状态。 

#### 

#### 摇杆模式

此功能用于手动操控机器人。通常用于 LCD 宏检查设备。有关使用该功能的单独功能手册请参考。

#### 门开关

此功能用于在安全围栏的门打开时停止移动中的机器人。

#### 屏幕保护程序停用

如果教学挂件未被操作，当在 `[service - 11: Teach Pendant Option] ([service  - 11: Teach Pendant Option])` 菜单中设置的屏幕关闭时间过去后，教学挂件将切换到屏幕保护状态。此功能用于通过外部信号打开教学挂件的屏幕。

#### 外部电机开启

此功能用于从外部操作面板开启电机。

#### 外部电机关闭

此功能用于从外部操作面板关闭电机。
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/6-output-signal-assign.md)
# 7.3.2.6 输出信号分配

在控制器中发生的事件信息或状态信息可以通过控制器输出信号传输到外部。将输出信号分配给要传输到外部的信息的方法如下。

1.	触摸 `2: 控制参数 - 2: 输入/输出信号设置 - 4: 输出信号分配-主任务 (2: 控制参数  - 2: 输入/输出信号设置  - 4: 输出信号分配-主任务)` 菜单。

2.	在信息项中输入输出信号编号后，触摸 `[OK]` 按钮。

    ![](../../../_assets/tp630/ctrl-outsignal-assign_eng.png)

* `[重置所有]`：您可以重置分配给所有信息项的输出信号编号。
*  `[重置一个]`：您可以重置分配给所选信息项的输出信号编号。
* 
  `[重置通道]`：您可以重置分配给信息项的输出信号输入通道 \(0-16: 数字信号\)

* 
  `[上一个任务]`/`[下一个任务]`：您可以移动到上一个或下一个任务屏幕。

* 
  `[S]`：在通过系统输入信号使用遥控时，您可以指定一个系统信号。系统信号的形式为 "s+数字"，将字母 s 与信号编号结合。例如，您可以将系统信号 49 设置为 s49。
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/7-output-signal-set-info.md)
# 7.3.2.7 输出信号设置信息

#### 远程模式

通过将教导挂接器的模式开关选择为远程 \(![](../../../_assets/sb-remote.png)\)，在输入信号分配部分设置的信号应在开启状态下输入，以激活远程状态。此功能用于将状态输出到外部。

#### 手动 \(教导\) 模式

此功能用于将控制器的操作模式为手动的状态输出到外部。

#### 自动 \(回放\) 模式

此功能用于将控制器的操作模式为自动的状态输出到外部。

#### 电机开启

当通过输入电机开启信号为各电机供电且驱动准备就绪时，此功能用于将状态输出到外部。

#### 机器人准备好 OK

当当前控制器状态满足在 `[system - 2: Control Parameter - 4: Robot Ready Condition] ([system  - 2: Control Parameter - 4: Robot Ready Condition])` 菜单中设置的所有条件时，此功能用于将状态输出到外部。

#### 机器人启动

当机器人通过手动模式下的前进/后退操作启动或通过自动模式下的启动信号输入启动时，此功能用于将该状态输出到外部。

#### 机器人移动

当机器人正在移动时，此功能用于将该状态输出到外部。

#### 机器人停止 \(保持\)

当机器人停止时，与启动信号的输出相反，此功能用于将该状态输出到外部。

#### 紧急停止

当来自安装在教导挂接器前面或控制器上的紧急停止按钮的输入信号输入时，此功能用于将状态输出到外部。

#### 紧急停止 \(外部\)

此功能用于将连接到系统板的外部紧急停止设备的信号输出到外部。

#### 低速模式 

当在输入信号分配部分为低速命令设置的信号开启或当机器人在手动模式下以安全速度运行时，此功能用于将该状态输出到外部。

#### 程序结束 

当在作业程序中执行结束循环时，此功能用于将该状态输出到外部。

#### 总体错误

控制器中发生的错误分为由系统错误引起的错误和由用户操作失误引起的错误。当由于系统错误发生错误时，此功能用于将该状态输出到外部。由于系统错误引起的错误范围从 1 到 999 和 2000 到 7999。

#### 操作错误

控制器中发生的错误分为由系统错误引起的错误和由用户操作失误引起的错误。当由于用户操作失误发生错误时，此功能用于将该状态输出到外部。供参考，由系统错误引起的错误范围从 1 到 999 和 2000 到 7999。

#### 警告

当控制器中发生警告时，此功能用于将该状态输出到外部。

#### 碰撞传感器 

当输入信号分配部分设置的碰撞传感器信号开启，并确认机器人发生碰撞时，此功能用于将该状态输出到外部。

#### 步骤设置警告 

在自动模式下，如果当前选择的光标位置与之前执行的位置不同，可能会很危险。此功能用于将该状态输出到外部。

#### 联锁异常警告

当作业程序的等待语句中的等待时间超过 `[System - 2: Control Parameter - 1: Control Environment Setting]` 菜单中设置的 `[Interlock Abnormal Time]` 选项的时间时，此功能用于将该状态输出到外部。

错误/警告输出位，错误/警告输出选择和错误/警告输出脉冲

有关错误/警告输出位、错误/警告输出脉冲、总体异常、操作错误和警告发生信号，请参阅以下序列。

![Figure 53 16Bit Output](../../../_assets/image_456.png)

#### 外部复位确认

当输入信号分配部分设置的外部复位信号开启时，此功能用于将该状态输出到外部。此信号将在 200 ms 内开启，然后自动关闭。

#### 程序回显位 

当通过输入信号分配部分设置的程序选择位选择程序时，此功能用于将选定的程序编号输出到外部。

#### 程序确认 

当机器人通过在远程模式下输入外部启动信号启动时，此功能用于将状态输出到外部。该信号将在 200 ms 内开启，然后自动关闭。

#### 弧焊异常

当发生与弧焊相关的错误时，此功能用于将该状态输出到外部。

#### 弧沉积警告

当在弧焊过程中发生焊接沉积时，此功能用于将该状态输出到外部。该信号将在 200 ms 内开启，然后自动关闭。

#### 机器人锁定状态 \(有效=开启\)

此功能用于将 `[Condition Setting]` 中的机器人锁定设置状态输出到外部。

#### 现场总线异常，和现场总线空闲

当使用 CC-LINK 和 DeviceNet 等现场总线通信板时，此功能用于将通信状态输出到外部。

#### 电池 \(备用，编码器\) 电压下降

当用于维持安装在主板上的 SRAM 状态的备用电池或用于维持安装在各电机上的编码器值的编码器电池发生电压下降时，此功能用于向外部输出。

#### 扭矩监测

此功能用于将施加于机器人六个轴的扭矩值输出到外部。将输出到外部的扭矩值是 1/2 的乘数的 % 值。

#### 润滑油注入警报

此功能用于向外部输出需要润滑油注入的条件。

#### 平均负载因子异常警报 

此功能用于向外部输出机器人在操作期间是否超过平均负载因子的状态。
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/8-key-signal-output.md)
# 7.3.2.8 Key Signal Output

`KEY 信号输出 (Key Signal Output)` 是一个功能，允许您将所需变量分配给 F-key 并通过按钮操作将该变量的值设置为 1 或 0。
它主要用于通过操作分配了输出变量的 F-key 来打开或关闭 I/O 输出信号。
(可以指定所有类型的变量，包括一般变量、别名和输出变量。)

您可以通过在主页屏幕右侧按下 `[R4: User Key]` 打开 `KEY 信号输出 (Key Signal Output)` 按钮。
如果没有进行任何设置，所有按钮将为空。

您可以按如下方式配置按钮：

1. 触摸菜单 `[F2: 系统] - 2: 控制参数 - 2: 输入/输出信号设置 - 5: 键信号输出 ([F2: system] - 2: Control parameter - 2: Input/Output signal setting - 5: Key signal output)`。

2. 设置要显示在按钮上的功能名称和选项，然后触摸 `[F7: 确定] ([F7: OK])` 按钮。

![](../../../_assets/tp630/ctrl-key-outsignal_eng.png)

* `标题 (title)`: 显示在按钮上的名称
* `on-var`: 当指定变量名称时，在按钮打开时变量的值被赋值为 1。
* `off-var`: 当指定变量名称时，在按钮关闭时变量的值被赋值为 1。
* `切换 (toggle)`:
  + 选中: 按钮每次被按下时在 ON 和 OFF 之间切换。
  + 未选中: 按下按钮时打开，释放时关闭。
* `自动 模式下 允许 (Permit on auto mode)`:
  + 选中: 此功能即使在自动模式下也可以操作。
  + 未选中: 此功能在自动模式下不操作。
* `自动 模式下 关闭 (OFF on auto mode)`: 切换到自动模式时，所有为此功能设置的变量都关闭。

{% hint style="info" %}
对于 `on-var` 和 `off-var`，例如，如果您输入 3.5 并按 `[ENTER]`，则输入 fb3.do5。
如果您输入 5 并按 `[ENTER]`，则输入 do5。
另外，您可以使用屏幕底部的 F-keys [fb], [do], 和 [so] 来输入值。
{% endhint %}

3. 打开 `KEY 信号输出 (Key Signal Output)` 按钮，并同时按下注册的 F-key 和 `[SHIFT]` 键，以确认设置已正确应用。

![](../../../_assets/tp630/rbt-userkey-keysig_eng.png)

{% hint style="info" %}
您可以在 ${cont_model} 教学终端的用户键区域注册所需的输出信号。有关详细信息，请参阅 "[2.7.2.1 Key Signal Output Function Area](../../../2-operation/7-user-key/2-button-registration/1-key-signal-output.md)"。
{% endhint %}
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/9-dio-block-assign.md)
# 7.3.2.9 FB 块分配

您可以设置控制器的一般输入/输出信号的使用方法。

1. 触摸 `2: 控制参数 - 2: 输入/输出信号设置 - 6: FB 块分配 (2: 控制参数  - 2: 输入/输出信号设置  - 6: FB 块分配)` 菜单。

2. 设置与所选 FB 地址的 DIO 块的连接，然后触摸 `[OK]` 按钮。

    ![](../../../_assets/tp630/ctrl-dio-blockassign_eng.png)

{% hint style="info" %}
可用的连接选项如下：
* [PCI 插槽 1]
* [PCI 插槽 2]
* [PCI 插槽 3]
* [EtherNet/IP 适配器]
* [EtherCAT I/O]
* [EtherNet/IP 扫描仪]
* [用户 DIO]
{% endhint %}
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/10-multi-signal-output.md)
# 7.3.2.10 多信号输出

输出信号 \(最多 16 个信号\) 可以作为一个组创建，数据可以通过单独的信号输出。

数据以二进制格式表示，并决定输出是开启还是关闭。例如，在下面所示的屏幕上打印 do41 和 do43 的数据是 0101（在十进制中为 5）。

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
        <p>关于从输出信号组列表中选择的组的详细信息。您可以设置组的名称、描述、信号和脉冲。</p>
        <ul>
          <li><b>[重置全部]/[重置一个]:</b> 您可以将所有信号的设定值或选定信号的设定值重置为 -1。</li>
          <li><b>[重置通道]:</b> 您可以重置设定信号的输出通道（0&#x2013;9: 数字信号）</li>
          <li><b>[设定范围]</b>: 您可以通过指定起始信号和结束信号快速设定信号。</li>
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
          <li><b>[+]/[-]:</b> 您可以添加一个新的输出信号组或删除一个输出信号组。</li>
          <li>这显示了输出信号组的列表。选择一个组名允许您查看和编辑详细信息。</li>
          <li><b>[复制页面/粘贴页面]:</b> 您可以复制输出信号组信息并粘贴到另一个组。</li>
          <li>从列表中选择要复制的组名称，触摸 <b>[复制页面]</b> 按钮，选择要应用值的组名称，然后触摸 <b>[粘贴页面]</b> 按钮。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

例如，当按照上面屏幕中的设置配置的作业程序执行时，操作将如下。

![图 54 作业程序执行示例](../../../_assets/image_429.png)

当机器人从 S1 向 S2 移动，并且 S2 的精度为 OK 时，脉冲信号将与指定组的信号一起输出。脉冲信号将在 200 毫秒后关闭。（脉冲信号是 200 毫秒的脉冲信号。）
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/11-multi-signal-input.md)
# 7.3.2.11 多信号输入

输入信号（最多 16 个信号）可以作为一组创建，数据可以通过各个信号获取。

数据是二进制格式，将根据输入的开关状态决定。例如，如果 di41 和 di43 为开，其他信号均为关，则数据将为 0101（十进制为 5）。

1. 触摸 `2: 控制参数 - 2: 输入/输出信号设置 - 8: 多信号输入 (2: 控制参数 - 2: 输入/输出信号设置 - 8: 多信号输入)` 菜单。

2. 设置输入信号组的名称、信号和抽样。

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
        <p>从输入信号组列表中选择的组的详细信息。
          您可以设置该组的名称、描述和信号。</p>
        <ul>
          <li><b>[重置所有]</b>/<b>[重置一个]</b>：您可以将所有信号或选择的信号的设置值重置为 -1。</li>
          <li><b>[重置通道]</b>：您可以重置已设置信号的输入通道（0&#x2013;9：数字信号）</li>
          <li><b>[设置范围]</b>：您可以通过指定开始信号和结束信号快速设置信号。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[确认]：您可以保存编辑的内容。</li>
          <li>[+]/[-]：您可以添加一个新的输入信号组或删除一个输入信号组。</li>
          <li>这显示了输入信号组的列表。选择一个组名称可以让您检查和编辑详细信息。</li>
          <li><b>[复制页面]</b>/<b>[粘贴页面]：</b>您可以复制输入信号组信息并粘贴到另一个组中。
            <br />从列表中选择要复制的组名称，触摸 <b>[复制页面]</b> 按钮，选择要应用值的组名称，触摸 <b>[粘贴页面]</b> 按钮。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

例如，当配置如上屏幕设置的作业程序执行时，其操作将如下所示。

![图 55 作业程序执行示例](../../../_assets/image_407.png)

从 S1 向 S2 开始后，机器人执行等待语句。如果在 S2 的准确性尚可之前等待条件满足，则机器人将移动到红色路径。如果不是，机器人将等待直到等待条件满足。
[__SOURCE](7-system/3-control-parameter/2-io-signal-setting/12-fn-block.md)
# 7.3.2.12 fn 块分配

您可以通过指定 fb 对象的特定区域来定义 fn 对象。如果 ${cont_model} 控制器是字段总线主设备，并且有多个字段总线从设备，您可以将每个从设备的区域设置为每个 fn 对象，以直观地处理这些从设备。

设置的 fn 对象可以在机器人语言和嵌入式 PLC 中与 fb 对象以相同的方式使用。

![](../../../_assets/io/io_fn.png)

1. 选择菜单 `[2: 控制参数 - 2: 输入/输出信号设置 - 9: Fn 块分配]`。

2. 如果还未进行 fn 设置，屏幕是空的。单击右侧的 + 按钮添加新的 fn 对象。fn 索引号自动从 0 增加到 63。

3. 要更改 fn 索引号，输入新名称，然后单击 `[F7: 确定] ([F7: OK])` 或 `SHIFT+[F7:Apply]` 按钮。
  ![](../../../_assets/io/io_fn_rename.png)

4. 对于每个 fn 对象，分别设置输入信号和输出信号的区域。

5. 在 ` (fb#)` 列中，设置 fb 对象的索引号 (0-9)，以放置 fn 区域。

6. 在 `起始字节 (byte base)` 列中，指定在 fb 对象内开始 fn 区域的字节索引。

7. 在 `字节数 (N.bytes)` 列中，指定 fn 区域的字节大小。

&nbsp;  

例如，如果像下图所示设置；

![](../../../_assets/io/io_fn_fn0.png)

![](../../../_assets/io/io_fn_fn3.png)

&nbsp;  

则映射如下表所示。

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

您可以打开 fn 输入/输出监控面板，以查看或手动输出每个 fn 对象的 dio 或 xy 继电器的当前值。有关更多信息，请参见以下链接。

[6.2.5 fn 输入，fn 输出](../../../6-monitoring/2-io/5-fn-io.md)
[__SOURCE](7-system/3-control-parameter/3-serial-port.md)
# 7.3.3 串口

您可以设置串口通信所需的信息。

1.	点击`[2: 控制参数 - 3: 串口] ([2: 控制参数  - 3: 串口])`菜单。

2.	为每个串口设置参数。

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
          <li><strong>串口列表</strong>: 选择一个端口名称以查看和编辑其详细信息。</li><li><strong>[确定]</strong>: 保存更改。</li>
          <li><strong>[+]/[-]</strong>: 添加新串口或删除现有串口。</li>
        </ul>
      </td>
    </tr>
        <tr>
      <td style="text-align:left">
        <img src="../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          执行回路测试。连接串口的RX和TX引脚以检查通信是否正常。
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
设置串口使用时请参考以下信息。

* 传感器：通过访问视觉传感器接收位移数据
* LVS：用于连接激光视觉传感器以进行焊缝跟踪
* MODBUS：${cont_model}控制器的MODBUS从功能
{% endhint %}
[__SOURCE](7-system/3-control-parameter/4-robot-ready-cond.md)
# 7.3.4 机器人准备状态

当机器人准备完成后，在`[机器人准备 OK]`项目中设置信号输出的条件，位于`系统 - 2: 控制参数 - 2: 输入/输出信号设置 - 4: 输出信号分配 (系统 - 2: 控制参数 - 2: 输入/输出信号设置 - 4: 输出信号分配)`菜单中。

1. 触摸`[2: 控制参数 - 4: 机器人准备状态] ([2: 控制参数 - 4: 机器人准备状态])`菜单。

2. 设置机器人准备状态后，触摸`[确定]`按钮。

    ![](../../_assets/tp630/ctrl-robot-readycond_eng.png)
[__SOURCE](7-system/3-control-parameter/5-home-position.md)
# 7.3.5 主位置注册

通过将机器人的任意姿态注册为主位置，您可以允许当机器人进入该位置时主位置信号输出到输出信号字段。主位置可以根据每个轴的姿态指定，最多可以注册和使用十六个姿态，并且每个轴的余量可以另外设置。

1. 触摸 `[2: 控制参数 - 5: 主位置注册] ([2: 控制参数  - 5: 主位置注册])` 菜单。

2. 选择主位置选项卡，然后设置使用、输出信号、轴角度和范围。

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
        <p>在选项卡中选择的主位置的详细信息。您可以
          设置使用、输出信号、轴角度和范围以及描述。</p>
        <ul>
          <li>[使用]: 您可以设置是否使用。</li>
          <li>[输出信号]: 您可以输入输出信号编号。</li>
          <li>[轴角度]/[范围]: 您可以输入机器人在主位置的轴角度和范围。</li>
          <li>如果范围设置为0，则不会对该轴进行主位置检查。</li>
          <li>范围指的是覆盖主点的 + 方向和 - 方向的范围。例如，如果范围设置为0.5，则主位置信号的输出范围将为1。</li>
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
          <li><b>[当前机器人姿态]</b>: 当前机器人姿态的轴角度和范围将自动输入。</li>
          <li><b>[程序/步骤]</b>: 如果您输入程序和步骤编号，相关步骤的轴角度和范围将自动输入。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](7-system/3-control-parameter/6-cordsys-reg/README.md)
# 7.3.6 坐标系统注册

1. 触摸`[2: 控制参数 - 6: 坐标注册] ([2: 控制参数 - 6: 坐标注册])`菜单。然后，坐标系统注册菜单将出现。

2. 通过选择所需菜单，您可以根据用户坐标系统或静态工具坐标系统设置坐标系统。

    ![](../../../_assets/tp630/ctrl-coord-menu_eng.png)
[__SOURCE](7-system/3-control-parameter/6-cordsys-reg/1-user-crdsys.md)
# 7.3.6.1 用户坐标系

用户坐标系是由用户指定的位置设置的坐标系。要使用用户坐标系，首先需要教导三个参考步骤，这些步骤是定义用户坐标系所需的，然后通过指定教导的程序编号和步骤顺序来登记用户坐标系。

按照以下程序教导三个参考步骤。下面的程序解释了当步骤顺序指定为“OXY”（O：原点姿态，X：轴姿态，Y：平面姿态）时的情况。

![图56 定义用户坐标系的三参考步骤教学方法](../../../_assets/image_427.png)


1. 定义用户坐标系的原点：教导一个任意点。

2. 定义用户坐标系中的X轴：以任意点的方式教导X轴线上的一个任意点，使得该任意点与原点的距离尽可能为200 mm。

3. 定义用户坐标系中的XY平面（确定Y轴和Z轴方向）：教导X轴和Y轴组成的平面上的一个任意点，该点距离原点的距离尽可能为200 mm或更远。

{% hint style="info" %}
* 当进行用户坐标系设置程序的教学时，TCP应设置为正确的值。检查当前选定工具的工具数据是否正确输入。
* 您可以登记最多20个用户坐标系。

{% endhint %}

{% hint style="warning" %}
定义坐标系时记录参考点的注意事项如下。

* 参考的3个点不应处于同一条直线上。
* 参考的3个点之间的距离不应过于接近。
* S3之后的后续步骤不会对坐标系登记产生任何影响。
{% endhint %}

登记用户坐标系的方法是通过指定教导的程序编号和步骤顺序，具体如下。

1. 触摸`[2: 控制参数 - 6: 坐标系登记 - 1: 用户坐标系] ([2: 控制参数  - 6: 坐标系登记  - 1: 用户坐标系])`菜单。

2. 前往您想要登记的用户坐标系（您可以使用“+”按钮创建它）。
3. 在指定程序编号和步骤顺序后，按下[F1:JOB计算]按钮。
4. 计算出的用户坐标系原点位置将显示。

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
      <td style="text-align_assets">
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">从用户坐标系列表中选择的坐标系的详细信息。您可以设置坐标系名称和描述、教导的程序编号、步骤顺序以及基于基轴原点的原点姿态。</td>
    </tr>
    <tr>
      <td style="text-align_assets">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>`[确定]`：您可以保存更改。</li>
          <li><b>[+]/[-]</b>：您可以添加新的用户坐标系或删除用户坐标系。</li>
          <li>用户坐标系列表。选择坐标系名称可以查看和编辑详细信息。</li>
          <li><b>[复制页面]/[粘贴页面]</b>：您可以复制用户坐标系信息并粘贴到另一个坐标系中。
            <br />在从列表中选择要复制的坐标系信息的名称后，触摸<b>[复制页面]</b>按钮，选择要应用值的坐标系名称，然后触摸<b>[粘贴页面]</b>按钮。</li>
          <li><b>[根据作业计算]</b>：您可以基于教导的程序和步骤顺序计算用户坐标系，以定义用户坐标系。
            <br />如果在<b>[作业编号]</b>选项中输入教导的程序编号和步骤顺序后，触摸<b>[根据作业计算]</b>按钮，将计算用户坐标系的原点。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](7-system/3-control-parameter/6-cordsys-reg/2-stationary-tool-crdsys.md)
# 7.3.6.2 静态工具坐标系统

机器人工具是附加在机器人前端的工具。一般来说，机器人使用附加在机器人上的工具执行操作。一个典型的例子是弧焊。弧焊工具通常附加在机器人的前端，用于在外部固定的工件上进行焊接。

另一方面，在静态工具的情况下，工具附加在外部，而不是机器人上。在这种情况下，机器人处理工件并将其放置在外部固定的工具上以进行操作。使用静态工具的典型操作是密封操作。通常，在密封操作中，当外部工具释放出所需的某种量的溶剂以进行密封时，机器人持有工件并创建所需的轨迹进行操作。

![图57 密封操作示例](../../../_assets/tp630/stationary_crd_sealing_eng.png)

为了创建所需的轨迹，机器人基于外部附加的工具执行线性 \(L\) 和圆形 \(C\) 插补，而不是基于附加在自己上的工具。在此期间，将使用静态工具插补功能。

当使用静态工具插补功能时，即使机器人持有的工件的姿态发生变化，静态工具在工件上的移动路径仍然可以保持直线和弧线。因此，静态工具插补功能必须始终用于外部工具的移动路径重要的操作。

要使用静态工具插补功能，必须设置静态工具坐标系统。

设置静态工具坐标系统的方法如下。

1. 触摸`[2: 控制参数 - 6: 坐标注册 2: 静态工具坐标系统] ([2: 控制参数 - 6: 坐标注册 2: 静态工具坐标系统])`菜单。

2. 选择所需的选项卡并注册静态工具坐标系统的位置。

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
      <td style="text-align:left">可以通过选择选项卡设置总共二十个静态工具坐标系统（工具0 - 工具19）。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[<b>确定</b>]: 可以保存更改。</li>
          <li>[<b>当前机器人姿态</b>]: 可以将当前TCP位置设置为静态工具坐标系统的位置。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### 将当前TCP位置设置为静态工具坐标系统的位置

在准确找到基于机器人基坐标系统的TCP之后，应将静态工具与机器人工具匹配，如下图所示，然后使用`[当前机器人姿态]`按钮执行自动设置功能。然后，当前TCP位置将被注册。

![](../../../_assets/tp630/stationary_crd_autoset_eng.png)

### 使用静态工具坐标系统编写程序

要执行静态工具插补步骤的记录，您应该将步骤记录为SL或SC。在${cont_model}教学挂件屏幕左上角的`[录制条件]`按钮上，您可以将录制条件更改为SL \(静态工具线性插补\)或SC \(静态工具圆形插补\)。

例如，如果您注册并使用静态工具坐标系统编号1，则可以创建如下程序。

![](../../../_assets/tp630/pane-prog-cmd-SL_eng.png)

{% hint style="info" %}
在使用静态伺服枪的情况下，静态工具插补功能不是必需的。这是因为在伺服枪焊接中，静态伺服枪的工件移动路径不需要以直线或弧线形成，而焊接点则是重要的。
{% endhint %}
[__SOURCE](7-system/3-control-parameter/7-prog-reservation.md)
# 7.3.7 定时程序执行

有关如何执行定时程序的详细信息，请参阅 "[${cont_model} 控制器定时程序执行功能手册](https://hrbook-hrc.web.app/#/view/doc-reserved-program-execution/zh/README?cont_model=${cont_model})"。
[__SOURCE](7-system/3-control-parameter/8-auto-backup-restore.md)
# 7.3.8 自动备份与恢复

有关如何自动备份和恢复控制器数据的详细信息，请参阅 "[${cont_model} 控制器自动备份功能手册](https://hrbook-hrc.web.app/#/view/doc-hi6-auto-backup/zh/README?cont_model=${cont_model})"。
[__SOURCE](7-system/3-control-parameter/9-network-setting/README.md)
# 7.3.9 网络

1.  `[2: Control parameter - 9: Network] ([2: Control parameter  - 9: Network])` 触摸菜单。网络设置菜单将出现。

2.  选择所需菜单以设置环境设置、服务等。
[__SOURCE](7-system/3-control-parameter/9-network-setting/1-environment-setting.md)
# 7.3.9.1 环境设置

您可以设置 LAN 端口所需的网络设置信息。

1. 触摸 `[ System - 2: Control Parameter - 9: 网络 - 1: 环境设置 ] ([ System  - 2: Control Parameter  - 9: Network  - 1: Environment setting ])` 菜单。

2. 设置每个 LAN(公共) 端口的参数。支持 Class C 类型的 IP 地址分配。

3. 重启系统时，设置的参数将被调整。

<img src="../../../_assets/image_551.PNG">

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
      <td style="text-align:left">在 LAN 端口选择选项卡中，仅公共 LAN 端口可以修改。 EtherCAT 和 T/P-Main 端口是固定的，无法更改。
	  </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          修改端口设置。可以修改 IP 地址、子网掩码、网关。
          <li><b>IP 地址：</b>您可以为目标端口设置 IP 地址。</li>
          <li><b>子网掩码：</b>目标端口的子网掩码设置。通常子网掩码为 255.255.255.0</li>
          <li><b>网关：</b>您可以为目标端口设置网关地址。第三个信息并粘贴到另一个端口。
          </li>
          <li><b>MAC：</b>显示控制器的 MAC 地址。
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
          <li>`[OK]`: 您可以保存更改。重新启动系统后，所有更改将被调整。</li>
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
有关更多信息，请参阅 "[${cont_model} 机器人控制器功能手册 - Modbus](https://hrbook-hrc.web.app/#/view/doc-modbus/zh/README?cont_model=${cont_model})"。
[__SOURCE](7-system/3-control-parameter/9-network-setting/2-service/3-ntp-client.md)
# 7.3.9.2.3 NTP 客户端

控制器的时间可以与 NTP 服务器自动同步。 <br>

有关更多信息，请参阅 "[${cont_model} 控制器功能手册 - NTP 时间同步](https://hrbook-hrc.web.app/#/view/doc-hi6-ntp-time-synchronization/zh/README)"。
[__SOURCE](7-system/3-control-parameter/9-network-setting/2-service/4-enet-comm-setting.md)
# 7.3.9.2.4 以太网通信设置

在执行以太网通信之前，您必须首先创建和配置一个以太网通信对象。  
最多可以创建和使用八个以太网对象，当前的通信状态可以实时监控。  

目前，它用于通过HRScript或设置独立执行通信。 

![](../../../../_assets/tp630/image32.png)

您可以使用[关闭]按钮强制关闭相应以太网对象的套接字，或使用[连接]按钮建立通信连接。  
当控制器启动时，它会自动尝试使用配置的以太网对象建立通信连接。  

* **名称** 

    以太网通信对象的名称。每个名称必须设置在“enet0”和“enet7”之间。

* **协议** 

    选择通信协议。（UDP，TCP客户端，TCP服务器）

* **IP 地址** 

    设置目标设备的IP地址。

* **本地端口** 

    设置本地端口号。

* **远程端口** 

    设置远程端口号。

* **状态** 

    显示当前通信连接状态。
[__SOURCE](7-system/3-control-parameter/10-license-key/README.md)
# 7.3.10 注册选项功能的许可证密钥
[__SOURCE](7-system/3-control-parameter/10-license-key/1-summary.md)
# 7.3.10.1 什么是可选功能的许可证密钥？

在 ${cont_model} 机器人控制器的功能中，某些可选功能是单独出售的，客户必须购买可选功能才能使用它们。可选功能的许可证密钥是通过将分配给机器人控制器主板的唯一数字与购买的可选功能结合而生成的，因此购买的功能仅在购买的控制器上操作。
因此，使用可选功能的机器人控制器的主板不能替换为其他控制器。
如果主板发生故障，我们将提供一个临时密钥，该密钥可以在需要用备件更换时使用 30 天。
在这种情况下，您必须至少提前 30 天联系我们的 A/S 以获得正式的许可证密钥。

* 特性配置 <br>
  设置是否购买可选功能 <br>
  许可证密钥设置
[__SOURCE](7-system/3-control-parameter/10-license-key/2-registration-process.md)
# 7.3.10.2 许可密钥注册程序

* 购买与您的系统序列号匹配的可选功能的许可密钥。系统序列号位于许可注册屏幕上。

  ![](../../../_assets/tp630/license-key1.png)


* 首先选择是否购买可选功能，然后输入许可密钥。如果购买选择与许可密钥不匹配，执行功能时将发生错误。
[__SOURCE](7-system/3-control-parameter/10-license-key/3-registration.md)
# 7.3.10.3 注册许可证密钥

* 注册屏幕

  ![](../../../_assets/tp630/license-key2.png)


* 如果许可证密钥输入正确，则“==> OK”将显示在许可证密钥输入的右侧。

* 如果显示“==> NG”，则许可证密钥不正确或购买选项选择不正确。
[__SOURCE](7-system/3-control-parameter/10-license-key/4-temporary-key.md)
# 7.3.10.4 什么是临时密钥？

* 临时密钥只能使用30天，并且只能发行一次。

* 如果临时密钥的剩余日期少于10天，则在控制器每次启动时都会出现以下警告。 <br>
  "W0025 仅剩 (0) 天用于可选功能临时许可证密钥免费试用期。"

* 临时密钥的目的是在控制器主板使用可选功能时出现问题并更换为备件时，直到由我们的A/S重新发行许可证密钥为止。
[__SOURCE](7-system/3-control-parameter/10-license-key/5-temporary-key-registration.md)
# 7.3.10.5 临时密钥注册

* 可以通过按下 [F] 键来发放临时密钥。

  ![](../../../_assets/tp630/license-key3.png)


* 如果成功发放，剩余使用天数将在以下屏幕中显示。

  ![](../../../_assets/tp630/license-key4.png)


* 注意）如果剩余天数为 0，选项功能将无法再使用，此后将发放 1 天的临时密钥。由于可选功能可能导致生产线停滞，请务必在剩余天数达到 0 之前与我们联系以获取正式许可证密钥。
[__SOURCE](7-system/3-control-parameter/11-industrial-comm/README.md)
# 7.3.11 工业通信 \(fieldbus\)

有关工业通信的详细信息，请参阅 "[${cont_model} 机器人控制器功能手册 - 工业通信](https://hrbook-hrc.web.app/#/view/doc-industrial-communication/zh-${cont_model}/README?cont_model=${cont_model})"
[__SOURCE](7-system/4-robot-parameter/README.md)
# 7.4 机器人参数

您可以设置与机器人操作相关的各种数据，以及每个轴的原点和操作范围等信息。

1. 触摸 `[3: Robot Parameter]` 菜单。然后，机器人参数菜单将出现。

2. 您可以通过选择所需菜单来检查和设置操作臂的各种参数。

    ![](../../_assets/tp630/robot-menu_eng.png)
[__SOURCE](7-system/4-robot-parameter/1-tool-data/README.md)
# 7.4.1    工具数据

您可以根据机器人的 R1 轴法兰设置 TCP 的距离和角度，并注册工具的重量、重心和惯性。您可以使用 `[1: Tool data]` 菜单手动进行注册。

另一种方法是使用自动校准功能设置工具长度，并使用负载估计功能注册工具的重量、重心和惯性。

在进行线性或圆形插补等插补操作时，轨迹将基于 TCP 创建，因此在教学之前应准确设置工具的长度和角度。

${cont_model} 控制器根据机器人的动力学执行控制。只有在正确设置工具的重量、中心和惯性时，机器人才能快速安全地操作。如果工具的重量、中心和惯性值不正确，可能会对机器人的性能和使用寿命造成严重问题。

特别是在使用工具更换功能时，所有与工具更换相关的工具信息，不仅是每个工具的信息，还有分配给断开工具的单独编号，均应输入以供使用。此外，即使在处理操作期间，工件的装卸状态也应分配给每个工具编号以供使用。

工具的长度是在法兰坐标系统中每个方向的长度。 \(X 轴方向长度: Xt / Y 轴方向长度: Yt / Z 轴方向长度: Zt\)

![图 60 每种机器人类型的法兰坐标系统](../../../_assets/image_213.png)

工具的角度是在法兰坐标系统中每个方向的姿态转换量。 \(X 轴方向角度: Rx / Y 轴方向角度: Ry / Z 轴方向角度: Rz\)

![图 61 工具角度: 旋转 Rx \(左\) / 旋转 Ry \(中\) / 旋转 Rz \(右\)](../../../_assets/image_211.png)

工具的长度和角度将基于法兰坐标系统进行设置。工具长度可以设置为从法兰坐标系统的中心到 TCP 的距离。

工具姿态是根据上述设置的工具角度，基于工具法兰坐标系统在 X、Y 和 Z 方向上依次进行旋转而获得的值。

Rxyz = Rot\(z, Rz\)Rot\(y, Ry\)Rot\(x, Rx\)

* Rxyz: 基于工具法兰的工具姿态旋转矩阵
* Rot\(z, Rz\): 在法兰坐标系统的 Z 轴方向上旋转 Rz 的旋转矩阵 
* Rot\(y, Ry\): 在法兰坐标系统的 Y 轴方向上旋转 Ry 的旋转矩阵
* Rot\(x, Rx\): 在法兰坐标系统的 X 轴方向上旋转 Rx 的旋转矩阵
[__SOURCE](7-system/4-robot-parameter/1-tool-data/1-tool-data-set.md)
# 7.4.1.1 工具数据设置


手动设置基于机器人 R1 轴法兰的 TCP 距离和角度，并注册工具的重量、重心和惯性的方式如下。

1.	触摸 `[3: Robot Parameter - 1: Tool Data] ([3: Robot Parameter  - 1: Tool Data])` 菜单。

2.	设置工具数据名称、重量、每个轴的详细条件和允许的比率。

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
        您可以设置工具数据名称和描述、重量、每个轴的详细条件和允许的比率。</ul></td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[自动校准]</b>: 您可以创建新的工具数据，或仅通过使用现有程序创建工具数据。如果您希望在之前教授的步态位置重新进行设置，您应该首先放置工具，然后执行自动校准功能以重新创建工具长度和角度。
            <br />
            <img src="../../../_assets/tp630/robot-tool-autocal_eng.png" alt/>
            <br />
          </li>
          <ul>
            <li>[之前程序编号]: 您可以输入在工具变形发生之前教授的程序编号。</li>
            <li>[之前步骤编号]: 您可以输入将执行自动工具数据校准的步骤编号。</li>
            <li>[要设置的工具编号]: 您可以输入要新设置的工具编号。</li>
          </ul>
          <li>
            <p>[角度校准]: 您可以校准工具的角度。</p>
            <p>
              <img src="../../../_assets/tp630/robot-tool-anglecal_eng.png" alt/>
            </p>
          </li>
          <li>[应用 CAD 数据]: 如果您拥有工具的 CAD 数据并使用它编辑工具数据，则视为负载估算的完成。
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
          <li>[复制页面]/[粘贴页面]: 您可以复制工具数据信息，然后将其粘贴到另一个工具数据中。
            <br />在从列表中选择要复制的工具数据信息的名称并触摸<b> [复制页面] </b>按钮后，选择要应用值的工具数据名称，然后触摸<b>[粘贴页面]</b>按钮。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 在工具数据列表中，未执行负载估算的工具数据将在名称右侧标记为 \(X\)。
* 您必须先执行负载估算才能使用该工具。使用未执行负载估算的工具可能会导致机器人速度和耐用性出现问题。
* 
  复制工具数据时，负载估算数据也将被复制。工具数据的复制和粘贴功能只能在已执行负载估算的工具编号选项卡上执行。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/1-tool-data/2-tool-data-set-info.md)
# 7.4.1.2 工具数据设置信息

* `[Weight]`: 工具的重量 \(kg\)
* `[Length]`: 工具的长度 \(mm\)。您可以使用自动校准功能或自动校准进行设置。
* `[Angle]`: 工具的角度 \(deg\)。您可以使用自动校准功能或角度校准功能进行设置。
* `[Center]`: 基于法兰中心的工具重心位置 \(mm\)。您可以使用负载估算功能进行设置。
* `[Inertia]`: 相对于工具坐标的工具的惯性矩 \(kg/m2\)。您可以使用负载估算功能进行设置。
* 允许比率：\(仅适用于高负载模式应用的机器人型号\) 这是当前设置与允许参考值的比率。根据允许比率，机器人操作如下。

| 分类 | 正常 | 高负载模式 | 例外允许模式 | 播放不可 \(大尺寸\) |
| :--- | :--- | :--- | :--- | :--- |
| 重量比率 \(%\) | - 100 | 100-120 | 100-120 | 120 - |
| 力矩比率 \(%\) | - 100 | 100-110 | 100-115 \(150\) | 115 \(150\) - |
| 惯性比率 \(%\) | - 100 | 100-130 | 100-150 \(600\) | 150 \(600\) - |

{% hint style="info" %}
允许比率可以根据机器人型号和控制器软件版本进行更改。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/1-tool-data/3-tool-data-high-load_mode.md)
# 7.4.1.3 高负载模式

高负载模式的可用性可能因机器人型号而异。一般来说，高负载模式适用于额定负载能力为100 kg或更高的中型机器人。<br> 对于支持高负载模式的型号，您可以在`[F2: 系统] - 3: Robot Parameter - 33: 伺服参数 - 9: 伺服控制环境设定 ([F2: system] - 3: Robot Parameter - 33: Servo parameter - 9: Servo control environment)`菜单中按如下图配置“4. 高负载模式”。<br> 对于支持高负载模式的型号，自动应用是默认设置。

![Figure 63 高负载模式设定屏幕](../../../_assets/image_high_load_mode_setting_eng.png)

| 设置值 | 操作特性 |
| :--- | :--- |
|禁用| 在工具负载下以正常模式操作。 <br>- 当电机开启时，将产生警告（W0051），指示由于高负载模式为“禁用”而导致机器人提前失效的风险。 |
|自动应用| 当工具负载低于额定负载时以正常模式操作。<br> 当负载超过额定值时，切换到高负载模式，机器人操作速度和加速度/减速度将降低。 |
|允许异常| 如果工具负载低于高负载模式的最大允许比率，则以与自动应用相同的方式操作。<br> 如果超过高负载阈值，则以高负载异常模式操作。<br> - 当电机开启时，将产生警告（W00177），指示由于高负载“允许异常”模式而导致机器人提前失效的风险。|

可以如下面图所示检查当前施加的工具负载下的高负载模式应用状态。<br>

![Figure 64 根据工具负载检查高负载模式应用状态](../../../_assets/home_tool_no_eng.png)

![正常模式工具（常规字体）](../../../_assets/tp630/normal_mode_tool_eng.png) : 正常模式（常规字体）

![高负载模式（粗体字）](../../../_assets/tp630/high_load_mode_tool_eng.png) : **高负载模式**（粗体字）

![高负载异常模式（红色字体）](../../../_assets/tp630/high_load_exception_mode_tool_eng.png) : <span style="color: red; font-weight: bold;">高负载异常模式</span>（红色字体）

{% hint style="info" %}
高负载模式的允许比率可能因机器人型号和控制器软件版本而异。
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
        <p>每个轴机械原点位置的详细信息。您
          可以设置轴的编码器和位置。</p>
        <ul>
          <li>S轴：您可以根据机器人和周围夹具的安装情况更改S轴原点。</li>
          <li>R1轴：您可以根据工具安装方向更改R1轴原点。</li>
          <li>H、V、R2 和 B 轴：可以通过自动校准功能自动设置。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[确定]：您可以保存更改。</li>
          <li>[应用单个]：您可以将选定的原点位置应用于选定的轴信息。</li>
          <li>[应用所有]：您可以将选定的原点位置应用于所有轴信息。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
* 轴原点设置会影响机器人的笛卡尔操作精度。尽量将其更改为准确值。
* 
  如果更改轴原点设置，先前创建的程序的位置将会改变。因此，轴原点设置必须仅在初始安装阶段执行。

* 
  如果更改了编码器偏移设置，则应重新设置轴原点。因此，在设置轴原点之前，必须完成编码器偏移设置。
{% endhint %}

{% hint style="info" %}
在出厂时，每个轴的机械原点位置设置为标准值 \(0X400000\)。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/3-soft-limit.md)
# 7.4.3 软极限

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
      <td style="text-align:left">每个轴的操作范围的详细信息。您可以设置一个轴的最小和最大操作范围以及当前轴位置。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: 您可以保存更改。</li>
          <li>[Cur. Value]: 您可以根据当前机器人位置设置每个轴的操作范围。</li>
          <li>[Reset All]: 您可以初始化所有轴的操作范围。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
出厂时，机器人的每个轴的操作范围设置为最大值。 
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/4-encoder-offset/README.md)
# 7.4.4 编码器偏移

当前的编码器位置可以设置为编码器原点位置 \(position 0X400000\)。您可以在机器人每个轴的参考位置确定编码器原点 \(每个轴附加刻度的位置\)。

1. 触摸 `[3: Robot Parameter - 4: Encoder Offset] ([3: Robot Parameter  - 4: Encoder Offset])` 菜单。

2. 通过调整每个轴的位置设置编码器偏移值。编码器偏移值将记录为十六进制值 \(一个十六进制数字\)。

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
      <td style="text-align:left">每个轴的编码器偏移值的详细信息。您可以
        设置校准的编码器值、当前编码器值和轴的当前位置。</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[确定]: 您可以保存更改。</li>
          <li>[重置单个]/[重置所有]: 您可以初始化选定或所有轴的编码器偏移值。</li>
          <li>[计算修正值]: 您可以校准选定轴的编码器偏移值。</li>
          <li>[先前修正值]: 您可以恢复在所有轴校准之前存在的编码器偏移值。</li>
          <li>[机器人移动]: 点击 [机器人移动] 按钮将机器人移动到记录的步骤位置（Jog）。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
编码器偏移值在出厂时设置。只有在必要时，例如更换电机或编码器时，才应重置编码器偏移值。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/4-encoder-offset/1-encoder-offset-utilization.md)
# 7.4.4.1 编码器偏移值的利用

为了在当前工作程序备份并初始化系统后继续使用现有程序，机器人必须保持初始化前存在的参考位置信息。如果记录编码器偏移值，机器人之前的位置信息可以被检索。

系统初始化后，直接输入编码器偏移值为十六进制值。如果使用软键盘输入该值会更加方便。

如果编码器偏移值以轴位置值 \(mm 或度\) 记录，需要在按下 `[SHIFT]` 键的同时触摸 `[Reset One]` 按钮时，输入窗口中输入轴位置值。

![](../../../_assets/tp630/robot-encoder-backup_eng.png)

{% hint style="info" %}
轴位置输入窗口中的基本设置值是参考位置值。如果不输入轴位置值就保存，当前编码器位置将被设置为原点位置 \(0X400000\)。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/4-encoder-offset/2-axis-posi-restore.md)
# 7.4.4.2 轴原点位置恢复

当机器人机构中的组件发生故障（尤其是电机或减速器）并更换组件时，必须在与原始原点相同的条件下校准编码器，以便重新启动现有的教学程序。  
然而，当服务人员在现场手动执行此程序时，原点可能需要经过多次试验和错误进行设置。这个专用功能旨在简化该过程。

* 机械维修后的原点恢复是什么？

![](../../../_assets/tp630/axis-posi-restore1.png)

换句话说，原点恢复是指：  
使用外部参考点（指示规），在更换组件后，通过值 ⓒ - ⓐ 来补偿校准不准确的原点 Ωo'，以将其恢复到准确的原点 Ωo。  
（这在重用教学程序时是必需的。）

{% hint style="warning" %}
外部参考点（ⓑ）的位置在组件更换前后必须保持不变。换句话说，更换前后必须位于完全相同的位置。
{% endhint %}


### 示例

以下示例解释了假设更换 S 轴电机的功能。

1. 指派一个新程序（101.job），并教导 S1 [验证点 - 接近] 和 S2 [原点验证点，仅 S 轴相对于 S1 旋转]，使固定在稳固安装工具上的点接近夹具或外围设备。

   ![](../../../_assets/tp630/axis-posi-restore2.png)

2. 更换 S 轴电机后，手动将 S 轴移至接近更换前编码器校准位置的地方，然后在 `系统 - Robot Parameter - Encoder Calibration (System - Robot Parameter - Encoder Calibration)` 屏幕上执行 S 轴的编码器校准。

3. 手动运行所教的程序（101.job）以移动到 S1，然后移动到 S2。当位置与机械组件更换前相同时，教导 S3 [原点验证点，仅 S 轴相对于 S1 旋转]。

   ![](../../../_assets/tp630/axis-posi-restore3.png)

4. 自动计算 S 轴的编码器校准值。

   1) 进入 `系统 - Robot Parameter - Encoder Calibration (System - Robot Parameter - Encoder Calibration)` 屏幕。  
   2) 将光标移动到 S 轴，并按下 `[F3: 计算校准值]`。 

      ![](../../../_assets/tp630/axis-posi-restore4.png)

   3) 将程序编号设置为 101，步骤编号设置为 2，表示“更换 S 轴电机之前”，  
      并将程序编号设置为 101，步骤编号设置为 3，表示“更换 S 轴电机之后”，  
      然后按下 `[执行]` 按钮。  

      (* 如果“更换 S 轴电机之后”的程序或步骤编号设置为 0，则编码器校准值将使用机器人的当前 S 轴位置计算。)  

      ![](../../../_assets/tp630/axis-posi-restore5.png)

   4) 计算出的 S 轴编码器校准值将在屏幕上显示。按 `[F7: 确认]` 以应用校准后的编码器值。  

      ![](../../../_assets/tp630/axis-posi-restore6.png)

5. 移动到所教程序（101.job）的 S2 并验证位置是否与电机更换前相同。
[__SOURCE](7-system/4-robot-parameter/5-b-axis-deadzone.md)
# 7.4.5 B-Axis Deadzone

在 B 轴的 0 度附近，R1 轴的旋转中心和 R2 轴的旋转中心轴几乎是平行的。当机器人的 TCP 进行线性插补或圆形插补等插补操作时，即使是小的移动，手腕轴也会迅速移动。

设置 B 轴无使用区域。

1.	触摸 `[3: Robot Parameter - 5: B-axis Deadzone] ([3: Robot Parameter  - 5: B-axis Deadzone])` 菜单。

2.	在设置确定无使用区域的角度和设置插补处理模式后，触摸 `[OK]` 按钮。

    ![](../../_assets/tp630/robot-baxis-deadz_eng.png)



* `[Setting Value]`: 您可以输入用于确定 B 轴无使用区域的角度。
* 
  `[Dead zone interpolation]`: 当机器人的轨迹必须在插补操作中经过 B 轴无使用区域时，您可以执行关于错误处理和机器人停止的设置。
[__SOURCE](7-system/4-robot-parameter/6-accuracy.md)
# 7.4.6 精度

您可以设置精度级别的详细条件，这指的是当机器人执行目标步骤时通过该步骤的精度。

1. 触摸 `[3: Robot Parameter - 6: Accuracy] ([3: Robot Parameter - 6: Accuracy])` 菜单。

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
        <p>每个级别的详细信息。您可以为每个精度级别设置工具提示位置
          (TCP) 和姿态。</p>
        <ul>
          <li>精度级别可以设置为 0 到 7 的值，精度级别将作为步骤语句参数之一被记录。</li>
          <li>精度级别 0&#x2013;6：为每个级别输入 TCP 距离和姿态，以及额外轴的距离和角度。
            <br />对于不支持线性或圆形插补的机器人，例如 LCD 机器人，将采用与额外轴相同的方法。</li>
          <li>精度级别 7：该值将自动计算并显示在控制器上，因此您无需直接输入值。
            <br />当应用精度级别 7 时，将创建一个满足步幅距离 1/2 条件的最大弯曲路径。精度级别 7 在需要使机器人尽可能平稳和快速移动时非常有效，例如 LDC 手进出时的动作。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[确定]：您可以保存更改。</li>
          <li>[重置所有]：您可以初始化所有精度级别的 TCP 距离和姿态。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 如果您根据对 “[2.3 步骤](../../2-operation/3-step/README.md)” 内容的理解接近精度级别，您可以更轻松地使用它。
* 在使用伺服枪或无均衡枪的焊接步骤中，控制器将自动执行限制，无论设置的精度级别如何。 
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/7-axis-add-weight/README.md)
# 7.4.7 每个轴的附加重量

您可以注册安装在机器人基本轴上的变压器或电缆支架的信息。

1. 触摸`[3: Robot Parameter - 7: Additional Weight on Each Axis] ([3: Robot Parameter  - 7: Additional Weight on Each Axis])`菜单。

2. 选择基本轴选项卡，设置安装的附加重量的信息，然后触摸`[OK]`按钮。

    ![](../../../_assets/tp630/robot-addweight_eng.png)

{% hint style="warning" %}
如果机器人因为安装了变压器或电缆支架而有附加重量，则必须注册每个轴的附加重量的信息。如果附加重量未正确注册，在执行工具负载估算时错误可能会增大。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/7-axis-add-weight/1-crdsys-origin-of-each-axis.md)
# 7.4.7.1 每个轴的坐标系原点

每个轴的 X、Y 和 Z 方向与机器人坐标系的方向相同。有关每个轴坐标系原点的信息，请参阅以下内容。

![图62 每个机器人配置的每个轴的坐标系原点 ](../../../_assets/image_476.png)
[__SOURCE](7-system/4-robot-parameter/8-collision-detection/README.md)
# 7.4.8 碰撞检测

当机器人操作过程中发生碰撞时，碰撞检测（冲击检测）是一个将机器人运动过程中正常产生的扭矩与当前产生的扭矩进行比较的功能，当检测到异常扭矩时将其视为错误，以最小化碰撞造成的损害。

${cont_model} 控制器通过在机器人在异常条件下操作或表现出异常行为时，以互补方式使用碰撞检测功能与现有安全功能（如过流、过载、超速和位置偏差错误检测）来增强机器人安全性。

触摸 `[3: Robot Parameter - 14: Impact Detection] ([3: Robot Parameter  - 14: Impact Detection])` 以使用此功能。

{% hint style="info" %}
* 碰撞检测功能仅在电机开启时运行。
* 在使用碰撞检测功能之前，请确保正确设置工具/附加重量或执行负载估算。
* 如果每轴的工具重量或附加重量与实际值不符，可能会发生误检测。
* 在执行负载估算或基于传感器/无传感器的力控制功能时，无法检测到碰撞。
* 无法检测到与未安装在机器人上的定位器、点焊机、夹具或其他设备的碰撞。
* 不支持针对定制机器人模型的基于模型的碰撞检测。
* 在从自主驾驶模式切换到手动驾驶模式后发生碰撞检测错误时，此现象不是错误（需要检查碰撞检测设置值）。

{% endhint %}

![](../../../_assets/tp630/coldet/robot_impact_detection.png)
[__SOURCE](7-system/4-robot-parameter/8-collision-detection/1-coldet-model-based.md)
# 7.4.8.1 基于模型的冲击检测

基于模型的冲击检测功能通过计算在机器人运动期间正常应生成的扭矩与实际测量的扭矩之间的差异来检测碰撞。可以调整灵敏度以控制对碰撞的响应，并且可以检测robot在低速移动时与外部物体接触的情况。


1. 触摸菜单 `[3: Robot parameter - 14: Impact Detection - 1: Model-Based Collision Detection] ([3: Robot parameter  - 14: Impact Detection  - 1: Model-Based Collision Detection])`。


![](../../../_assets/tp630/coldet/model_based_coldet_tab_general.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">No.</th>
      <th style="text-align:left">Description</th>
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
      <td style="text-align:left">代表所有轴的默认灵敏度。较高的值增加碰撞检测灵敏度。
      (默认: 100, 最大: 200)  </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">启用或禁用低速碰撞检测功能。 </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">检测低速碰撞的设定时间。如果碰撞力施加的时间超过该参考时间，则被识别为碰撞。 </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">只有当连杆速度低于设定值时，碰撞才被视为低速碰撞。 </td>
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
每个轴的设置选项卡仅在工程模式或更高模式下启用。
{% endhint %}

<table>
  <thead>
    <tr>
      <th style="text-align:left">No.</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">相对于每个轴的碰撞检测阈值的比率（%）。较低的值导致更灵敏的响应。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">截止频率值，通常根据机器人的控制环境设置。如果任何轴设置为0，则禁用该轴的碰撞检测。（最大: 100） </td>
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
每个轴的最终灵敏度值与每个轴的灵敏度值成正比，与所有轴的整体默认灵敏度成反比。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/8-collision-detection/2-coldet-axis.md)
# 7.4.8.2 设置每轴碰撞检测

碰撞检测功能监测每个机器人轴上发生的干扰扭矩和干扰扭矩的变化率。如果测量值超过配置的阈值，则视为错误。

* 如果干扰扭矩超过设置的阈值，将显示`[E0160 (Axis O) 检测到碰撞]`。
* 如果干扰扭矩速率超过设置的阈值，将显示`[E0161 (Axis O) 检测到冲击]`。

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
      <td style="text-align:left">启用或禁用每轴碰撞检测功能。即使启用，该功能在机器人停止或点焊枪施加压力时也不运行。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">设置在碰撞后是否保持灵敏度。当启用时，即使在检测到碰撞后，当前检测水平也会保持不变。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left"> 
        <p>[测量] 显示在碰撞检测命令（coldet level.id）处于激活状态期间发生的最大"干扰扭矩"。</p>
        <p>[阈值] 用户可以参考此值为每个级别配置"干扰扭矩"阈值。</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p>[测量] 显示在碰撞检测命令（coldet level.id）处于激活状态期间发生的最大"干扰扭矩变化率"。</p>
        <p>[阈值] 用户可以参考此值为每个级别配置"干扰扭矩变化率"阈值。</p>
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
      <td style="text-align:left">用于将每个轴配置的所有级别值重置为默认值。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left">用于添加额外的级别。可配置的最大级别数量为16。</td>
    </tr>
    <tr>
      <td style="text-align:left"> 
        <img src="../../../_assets/c8.png" alt/>
      </td>
      <td style="text-align:left">用于删除最高级别。可以从第6级及以上开始删除。</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
碰撞检测测量值最多可显示2分钟。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/9-jog-inch-level/README.md)
# 7.4.9 Jog Inching Level Setting

您可以通过指定移动距离来限制操作。这在您希望在手动模式下使用 jog 按钮将机器人移动到所需距离时非常有用。

1. 触摸`[3: Robot Parameter - 11: Set the Jog Inching Level] ([3: Robot Parameter  - 11: Set the Jog Inching Level])`菜单。

2. 设置每个 jog inching level 的距离和角度后，触摸`[OK]`按钮。

    ![](../../../_assets/tp630/robot-jog-inching_eng.png)
[__SOURCE](7-system/4-robot-parameter/9-jog-inch-level/1-jog-inch-main-funcs.md)
# 7.4.9.1 Jog增量功能的主要功能

* 增量适用的坐标系统
  * 
    在关节坐标系统中的增量：每个关节指定的距离 \(mm\) 和角度 \(deg\) 将使运动发生。

  * 在笛卡尔坐标系统中的增量
  * 在工具坐标系统中的增量 
  * 在用户坐标系统中的增量：X、Y 和 Z 位置 \(mm\) 及 Rx、Ry 和 Rz 姿态 \(deg\) 指定的量将使运动发生。
* 增量等级 

  您可以将增量距离设置为与现有 jog 速度相同的等级，因此您可以选择八个速度级别，并为每个级别设置增量距离。
[__SOURCE](7-system/4-robot-parameter/9-jog-inch-level/2-inch-jog-operation.md)
# 7.4.9.2 碰触 jog 操作

碰触功能是不允许移动超过每次按下 jog 键的最大移动距离的功能。

即使在达到碰触距离后，如果您继续按下 jog 键，然后松开手，机器人将减速到碰触距离，然后停止。

![图63 在达到碰触距离后释放键](../../../_assets/image_488.png)

如果您在达到碰触距离之前释放 jog 键，机器人将从您释放 jog 键的时刻开始减速，然后停止。此时，模式将与一般 jog 模式相同。

![图64 在达到碰触距离之前释放手](../../../_assets/image_473.png)

{% hint style="info" %}
在关节坐标系统中，速度级别 1 固定为机器人将移动 1 个编码器位的模式。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/12-system-maintenance/README.md)
# 7.4.10 减速机使用寿命设置

如果机器人轴的减速机被更换，则应初始化减速机的额定使用寿命。
减速机额定使用寿命耗尽的速率取决于操作负载条件和速度。速度越高，负载越大，使用寿命下降得越快。
减速机寿命数据可以在系统特性数据中找到。
监控菜单显示减速机的剩余额定寿命和基于最新机器人操作模式的预期寿命。

额定寿命：在额定负载和额定速度条件下持续驱动时的剩余寿命<br>
预期寿命：根据最近实际驱动条件估算的剩余寿命。<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  寿命预期可能会因机器人最近的运动模式而增加或减少。

减速机使用寿命初始化
1.    触摸`[3: Robot parameter - 12: 系统维护 - 2:Reducer Lifespan setting] ([3: Robot parameter  - 12: System maintenance  - 2:Reducer Lifespan setting])`菜单。

2.    将光标移动到与更换的减速机相对应的位置并触摸`[Reset one]`按钮。
如果所有减速机都被更换或机身被更换为新机器人，请触摸`[Reset all]`按钮。在初始化额定寿命的减速机的情况下，初始化日期会记录在更改日期列中。

![](../../../_assets/tp630/reducer_lifetime_setting.png)


使用寿命计算周期`[min]`：减速机使用寿命的更新周期。最短周期为10分钟。

{% hint style="info" %}
减速机的额定和预期寿命是基于减速机寿命预测模型的预测参考值。实际减速机的寿命可能会根据驾驶条件与预期模型有所不同。
{% endhint %}
[__SOURCE](7-system/4-robot-parameter/13-system-diagnosis/README.md)
# 7.4.13 系统诊断

它用于诊断机器人系统中的故障的各种功能。
[__SOURCE](7-system/4-robot-parameter/13-system-diagnosis/1-gas-spring-pressure_sensor.md)
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
[__SOURCE](7-system/5-application-parameter/README.md)
# 7.5 应用参数

1.	触摸`[4: 应用参数]`菜单。然后，应用参数菜单将出现。

2.	选择所需的菜单，然后检查和设置机器人的应用功能的各种参数。

    ![](../../_assets/tp630/app-menu_eng.png)

<br>

{% hint style="info" %}
对于本手册未涵盖的项目，请参考每个单独应用功能的“功能手册”。
{% endhint %}
[__SOURCE](7-system/5-application-parameter/10-cmd-idp-exe.md)
# 7.5.10 命令独立执行

这是一个在设定输入信号从 OFF 转为 ON 时，独立于工作程序执行相应语句的功能。 <br>
该语句采用未使用的子任务执行，通常使用子任务 1。 <br>
有关多任务的更多信息，请参见 "[${cont_model} 控制器功能手册 - 多任务](https://hrbook-hrc.web.app/#/view/doc-multi-task/zh/README)"。


![](../../_assets/tp630/cmd-idp-exe.png)

  * 输入信号：设置信号输入到控制器。
  * 命令： 
    * 记录在输入信号从 OFF 变为 ON 时要执行的语句。 
    * 通常，任务启动用于静态伺服枪的枪搜索和尖端装饰工作，移动用于位置器的独立操作。 
    * 使用任务启动时，子任务 1 用于执行该命令，因此请指定子任务为 2 或更多，或设置为 0。 (0=自动分配)
  * 执行中的输出信号： 
    * 当语句执行开始时，它会被打开，当执行完成时会被关闭。 
    * 如果语句不是移动，则由于执行时间非常短而无意义。
  * 执行完成后的输出信号： 
    * 当对应语句的执行开始时变为 OFF，当执行完成时变为 ON。 
    * 如果语句不是移动，则由于执行时间非常短而无意义。

{% hint style="info" %}
* 仅在自动模式下电机处于 ON 状态时才可以执行。
* 当执行移动语句时，轴必须通过机制分离，以便其不在主任务中使用，或必须通过轴控状态关闭禁用轴控状态。
{% endhint %}
[__SOURCE](7-system/5-application-parameter/13-user-def-error/README.md)
# 7.5.13 用户定义错误

此功能允许用户为${cont_model}机器人控制器中的特定条件定义错误。当满足定义的条件时，用户定义的错误将被触发。

{% hint style="info" %}
支持版本 V60.30-00。
{% endhint %}
[__SOURCE](7-system/5-application-parameter/13-user-def-error/1-setting.md)
# 7.5.13.1 用户定义错误设置

1. 点击 `[System - 4: Application Parameters - 13: User-Defined Error] ([System  - 4: Application Parameters  - 13: User-Defined Error])` 菜单。<br><br>

2. 点击 "创建样本文件" 按钮。<br>
名为 "help_user_err.json" 的文件将在 MAIN/project 目录中创建。<br>
![](../../../_assets/tp630/user-def-code/image1.png)

3. 重新进入设置屏幕时，样本文件中写入的用户定义错误将显示。<br>
- 错误代码：指定要触发的错误代码。
- 条件表达式：定义触发错误的条件。可以使用任何可以用于 if 语句的条件表达式。
- 消息：指定发生错误时显示的消息。
- 电机关闭：确定当发生用户定义错误时电机是否应关闭。<br>
![](../../../_assets/tp630/user-def-code/image2.png)

4. 将 USB 驱动器插入教学挂件，访问文件管理器菜单，并将 'help_user_err.json' 文件复制到 USB 存储路径。<br><br>
![](../../../_assets/tp630/user-def-code/image3.png)

5. 在 PC 上打开文件，并根据样本文件格式编辑错误（使用记事本进行编辑是可能的）。<br><br>
- E65###：错误代码（范围：E65001 ~ E65500）
    - cnd：条件表达式
    - msg：在错误帮助中显示的原因消息
    - remedy：在错误帮助中显示的纠正措施
    - mot_off：电机关闭<br>
![](../../../_assets/tp630/user-def-code/image4.png)

6. 将编辑过的文件复制回教学挂件。
[__SOURCE](7-system/5-application-parameter/13-user-def-error/2-example.md)
# 7.5.13.2 用户定义错误示例

1. 修改 'help_user_err.json' 文件，如下所示。<br>
![](../../../_assets/tp630/user-def-code/image9.png)

2. 当 di5 信号被打开以满足条件表达式时，将触发 E65001。<br>
![](../../../_assets/tp630/user-def-code/image10.png)

3. 检查错误帮助将显示与文件中写入的相同内容。<br>
![](../../../_assets/tp630/user-def-code/image11.png)
[__SOURCE](7-system/5-application-parameter/14-user-def-warn/README.md)
# 7.5.14 用户定义警告

该功能允许用户为 ${cont_model} 机器人控制器中的特定条件定义警告。当满足定义的条件时，将触发用户定义的警告。

{% hint style="info" %}
支持从 V60.30-00 版本开始。
{% endhint %}
[__SOURCE](7-system/5-application-parameter/14-user-def-warn/1-setting.md)
# 7.5.14.1 用户定义的警告设置

1. 点击`[System - 4: Application Parameters - 14: User-Defined Warning] ([System  - 4: Application Parameters  - 14: User-Defined Warning])`菜单。<br><br>

2. 点击“创建示例文件”按钮。<br>
* 将在MAIN/project目录中创建名为'help_user_warn.json'的文件。<br>
![](../../../_assets/tp630/user-def-code/image5.png)

3. 当重新进入设置屏幕时，将显示示例文件中编写的用户定义警告。
- 警告代码：指定要触发的警告代码。
- 条件表达式：定义触发警告的条件。允许使用任何可以在if语句中使用的条件表达式。
- 消息：指定警告发生时显示的消息。<br>
![](../../../_assets/tp630/user-def-code/image6.png)

4. 将USB驱动器插入教学挂件，访问文件管理菜单，并将'help_user_warn.json'文件复制到USB存储路径。<br><br>
![](../../../_assets/tp630/user-def-code/image7.png)

5. 在PC上打开文件，并根据示例文件格式编辑警告（可以用记事本编辑）。<br><br>
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

2. 当 di6 信号打开以满足条件表达式时，W65001 将被触发<br>
![](../../../_assets/tp630/user-def-code/image13.png)

3. 检查警告帮助将显示与文件中写的相同内容。<br>
![](../../../_assets/tp630/user-def-code/image14.png)
[__SOURCE](7-system/5-application-parameter/16-joystick-mode/README.md)
# 7.5.16 摇杆模式

此功能用于通过外部设备（如摇杆）操作机器人。

![](../../../_assets/tp630/joystick_mode_menu.png)

* 摇杆慢走启用 <br>
   为了执行与摇杆模式对应的功能，必须设置输入信号并将其打开。

* 执行类型 <br>
   选择是否根据设置信号的输入状态或 Open-api 的输入状态执行慢走动作。 <br>
   慢走操作与 T/P 手动模式中的慢走键操作完全相同。


{% hint style="info" %}
* 仅在自动模式下电机开启时运行。
{% endhint %}
[__SOURCE](7-system/5-application-parameter/16-joystick-mode/1-jogging-in-signal.md)
# 7.5.16.1 Jogging(input signal)

要通过信号输入控制机器人移动，请设置对应于每个方向键的输入信号。 <br>
在对应输入信号为ON的部分，相应的轴将在指定方向上移动。 <br>

当输入信号被设置为坐标系时，如果输入信号被打开，则匹配的坐标系将被选中。 <br>

与机制编号对应的输入信号可以根据状态改变机制。 <br>

![](../../../_assets/tp630/jogging_in_signal.png)
[__SOURCE](7-system/5-application-parameter/16-joystick-mode/2-jogging-open-api.md)
# 7.5.16.2 Jogging(open-api)

请参阅单独的手册以获取 open-api 通信信息。 <br>
机器人驳接的 url 地址和使用的 body 信息如下。

* url : POST /project/robot/joystick/joy
* body <br>
    axis : 由 double 类型数组组成。 axis[0] 对应于 J1。值为 -1 表示向左移动，值为 +1 表示向右移动。 <br>


{% hint style="info" %}
如果在 300ms 内未收到数据，驳接动作将停止。  
{% endhint %}
[__SOURCE](7-system/5-application-parameter/16-joystick-mode/3-speed-level.md)
# 7.5.16.3 速度

此功能通过信号输入改变机器人慢跑的速度级别。 <br>
当设定的输入信号变为 ON 时，它会更改为相应的速度级别，并且输出相应的输出信号为 ON。 <br>

![](../../../_assets/tp630/speed_level.png)
[__SOURCE](7-system/5-application-parameter/16-joystick-mode/4-robot-move.md)
# 7.5.16.4 移动

这是一个将机器人指定轴通过信号输入移动到指定位置的功能，速度为指定速度。 <br>
在下图中，当fb2.di34信号打开时，机器人以10%的速度移动，使得机器人6个轴的位置为30度。 <br>

如果您想同时移动两个或更多机器人轴，请将输入信号设置为相同的值。在此时，运动速度应用于它们中首先记录的设置值。 <br>

![](../../../_assets/tp630/robot_move.png)
[__SOURCE](7-system/5-application-parameter/22-reduced-speed-mode.md)
# 7.5.22 减速模式

当输入信号（di）从关闭变为开启时，机器人速度根据设定的减速比率降低。 <br>
在移动命令中，机器人速度通过将原始速度值与自动模式机器人速度和减速比率结合应用。 <br>

![](../../_assets/tp630/reduced_spd_mode.png)

  * 输入信号：设置控制器接收到的信号。
  * 激活：
    * 高：当信号处于开启状态时应用减速，信号关闭时取消减速。
    * 低：当信号处于关闭状态时应用减速，信号开启时取消减速。
  * 减速率：  
    * 确定速度将降低的比例。
    * 当收到减速模式输入信号时，机器人速度设置为自动模式机器人速度乘以减速率。

{% hint style="info" %}
* 在手动模式下不应用减速比率。
{% endhint %}

{% hint style="warning" %}
* 选择与输入信号状态匹配的正确激活条件。
* 在播放过程中收到I/O信号时，仍然会应用减速模式。
{% endhint %}
[__SOURCE](7-system/5-application-parameter/23-scurve-condition/README.md)
# 7.5.23 S-curve Condition

S-curve指的是根据任务调整路径精度和剩余振动的运动轨迹规划，从而使得过程设计最优化。

![](../../../_assets/tp630/s-curve_velocity_comparison.png)

该图比较了默认速度轮廓方法与S-curve速度轮廓方法。

默认（蓝色实线）：加速度以突变的方式开始和结束，这可能导致振动。
S-curve（红色虚线）：加速和减速期间的速度变化更加平滑。这可以最小化机器人振动，即使在运动速度变化时也能减少路径错误。

{% hint style="warning" %}
* 如果连续运动生成失败，运动将作为不连续（中断）运动运行。在该区域，调整参数或切换回默认运动（默认）以确保可靠操作。
* 历史日志可用于查看连续运动失败的记录。
{% endhint %}

{% hint style="info" %}
* 此功能自版本V70.00-00起提供支持。
* 请参阅${cont_model}控制器手册中的命令语法 "[5.22 scurve](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/5-moving-robot/22-s-curve?cont_model=${cont_model})"
{% endhint %}
[__SOURCE](7-system/5-application-parameter/23-scurve-condition/1-scurve-condition.md)
# 7.5.23.1 S-curve condition

S-curve condition settings allow you to define the characteristics of the acceleration and deceleration phases that occur when the robot is operating in detail. Configure the items below to match each process's required characteristics (such as path accuracy or vibration reduction).

![](../../../_assets/tp630/s-curve_condition.png)

  * Condition Name: 输入条件名称。
  * Path Accuracy <br>
    确定机器人跟随指定轨迹的忠实程度。对于如加工或精密组装等必须最小化轨迹偏差的过程，建议使用较高的值。
    较大的值增加路径准确性，但也可能导致相对较高的振动。
  * Smooth Motion <br>
    确定加速和减速变化的平稳程度。在需要保护易碎工件（例如，玻璃）、过程对振动敏感，或希望减少对机器人硬件的机械冲击时，使用较高的值。较大的值产生更平稳的运动，但也会增加周期时间。将值设置得过高可能会阻止机器人进行连续运动，导致其以不连续的方式移动。

### Example Settings

* Precision machining and dispensing (path accuracy priority)
  * 机器人必须准确地跟随预定轨迹。

  * Recommended settings:
    * Path accuracy: 高 (例如，80 ~ 100)
    * Smooth motion: 低到中等 (例如，20 ~ 40)

  * Use case: 沿着复杂的汽车零件曲线应用密封剂，或进行激光切割。为了最小化轨迹误差，设置高精度；维持路径比轻微振动更重要。

  * Caution: 根据实际机器人的振动行为和特定过程规格调整参数。

* Sensitive cargo transport (vibration-reduction, smooth motion priority)
  * 一个过程，其中振动可能会损坏产品或导致位移错误。

  * Recommended settings:
    * Path accuracy: 中等 (例如，50)
    * Smooth motion: 高 (例如，80 ~ 100)

  * Use case: 运输半导体晶圆、大型玻璃面板 (LCD/OLED) 或容易溢出的液体容器。在加速/减速期间最小化冲击，以防止滑移或摇晃。

  * Caution: 由于运动变得更平滑，总体周期时间（操作时间）可能会增加，或可能需要执行不连续的运动。
[__SOURCE](7-system/5-application-parameter/23-scurve-condition/2-acceldecel-parameter.md)
# 7.5.23.2 加速/减速参数

S曲线条件和**最大冲击**互为补充。当仅使用S曲线设置优化过程困难时，或者您需要为每个关节调整最大冲击限制时，可以调整参数。

![](../../../_assets/tp630/s-curve_acceldecel_parameter.png)

冲击与运动之间的关系
冲击是加速度变化的速率，修改此值会产生以下特征变化。

- **减少最大冲击 (↓)：** 加速度变化更逐渐，使运动更平滑并减小振动。然而，达到目标速度需要更长的时间，这可能会增加循环时间。

- **增加最大冲击 (↑)：** 提供更灵敏的运动，但如果值过高，S曲线条件的“平滑运动”效果会减弱，从而导致更大的机械冲击。

最大冲击的自动更新
每当关键参数更改时，系统会自动重新计算最大冲击值，以保持设备稳定性。

{% hint style="warning" %}
**注意：** 当您手动设置一个值时，修改最高速度或加速时间会用系统计算的值覆盖手动输入的最大冲击。如果您已为特定过程优化了冲击值，请务必在进行更改之前备份现有值。
{% endhint %}


{% hint style="info" %}
由于加速/减速参数对机器人运动特性有很大影响，因此仅在工程模式或更高模式下启用。
{% endhint %}
[__SOURCE](7-system/6-initialization/README.md)
# 7.6 初始化

如果机器人控制器无法正常工作，请初始化系统。系统初始化必须由具有 HD 现代机器人初始设置经验的工程师进行。

1. 触摸 `[5: 初始化]` 菜单。然后，初始化菜单将出现。

2. 选择所需的菜单，然后执行机器人系统的初始设置，然后初始化串行编码器。

![](../../_assets/tp630/init-menu_eng.png)

{% hint style="info" %}
在 `[初始化]` 菜单中的某些项目仅在选择特定类型的附加轴时才会受到支持。
{% endhint %}

{% hint style="info" %}
* 要初始化系统，您应联系客户支持团队并请求专家或合格工程师以防止错误操作。
* 
  当系统初始化时，控制器中保存的所有数据和程序将被删除。在初始化系统之前，您应备份数据和程序，并在必要时恢复它们。

  有关数据备份和恢复的详细信息，请参阅 "[4.2.5 数据备份](../../4-service/2-file-manager/5-data-backup.md)" 和 "[4.2.6 数据恢复](../../4-service/2-file-manager/6-data-restore.md)"。
{% endhint %}
[__SOURCE](7-system/6-initialization/1-system-format.md)
# 7.6.1 系统格式

1.	在 ${cont_model} 教导编程器屏幕的状态栏上，检查操作模式是否设置为手动模式。

    ![](../../_assets/tp630/sbar-mode-manual_eng.png)

    如果设置为自动模式，请将教导编程器的模式开关切换到手动模式。

    ![](../../_assets/tp630/TP-hw-switch-manual.png)

2.	触摸 `[system]` 按钮 - `[5: Initialize - 1: System format] ([5: Initialize  - 1: System format])` 菜单。

3.	在检查保存的数据后，触摸 `[Initialize]` 按钮。所有数据和程序，包括控制参数文件和机器参数文件，将被删除，初始设置值将被恢复。

    ![](../../_assets/tp630/pop-system-init_eng.png)
[__SOURCE](7-system/6-initialization/2-robot-type-sel.md)
# 7.6.2 机器人类型选择

1. 触摸 `[5: Initialize - 2: Robot Type Selection] ([5: Initialize  - 2: Robot Type Selection])` 菜单。或者触摸 ${cont_model} 教教具屏幕右上方的 `[Mechanism]` 按钮。

2. 在机器人模型选择窗口中选择一个机器人，然后触摸 `[OK]` 按钮。

    ![](../../_assets/tp630/init-robot-select_eng.png)

* 您可以滚动机器人模型列表以查看模型名称，或输入模型名称进行搜索。
* 如果您触摸机器人使用按钮，列表中将仅显示属于该用途的机器人。
* 
  如果您选择一个新的机器人模型，机器参数文件 \(hi6\_porj.json\) 将恢复到初始设定值，各种历史文件也将被初始化。

* 
  如果您选择一个包含额外轴的系统，如行走轴或伺服枪，您需要设置额外轴的数量。如果系统仅由机器人轴组成而没有额外轴，请输入 0。

  ![](../../_assets/tp630/init-addaxis-pop_eng.png)

{% hint style="warning" %}
* 操纵器和控制器作为一个系统发货。因此，机器人控制器配备适合于系统组成部分的机器人驱动能力的驱动。
* 通过初始化系统重置时，必须检查出厂时设置为初始设定值的机器人模型，然后设置正确的模型。

{% endhint %}

3. 进入工程师模式。有关详细设置，请参考 "[8.12 Engineer Mode](../../8-r-code/12-r314.md)"。

4. 触摸 `[system]` 按钮 - `[3: Robot Parameter - 4: Encoder Offset] ([3: Robot Parameter  - 4: Encoder Offset])` 菜单。

5. 执行编码器偏移校准。要启动车马，即使机器人位置不是参考位置，您也应该暂时设置编码器偏移。有关详细信息，请参考 "[7.4.4 Encoder Offset](../../7-system/4-robot-parameter/4-encoder-offset/README.md)"。

    ![](../../_assets/tp630/robot-encoder-offset__eng.png)

{% hint style="info" %}
* 在将机器人移动到参考位置后，您应该正常执行编码器偏移设置。
* 对于初始设置，即使机器人位置不是参考位置，您也应该执行编码器偏移设置。否则，马达将无法启动，使得无法驱动机器人。

{% endhint %}

6. 关闭并重新打开控制器的电源，然后为电机供电。

7. 在手动模式下，以低速度安全地将机器人移动到参考位置，然后参考步骤 7-8 再次执行编码器偏移校准。

* 在编码器偏移设置项目中，当前编码器位置将设置为 0X400000 \(十六进制\)。
* 当电机因故障被更换时，如果在同一位置执行编码器偏移设置，则记录的程序可以被完全使用。

8. 按下教教具上的 `[Program]` 键，选择程序 9999，然后记录一个步骤。您可以轻松地将机器人移动到参考位置。

{% hint style="warning" %}
* 若要初始化系统，请联系客户支持团队并咨询专家。
* 
  有关协作根的初始化，请参考协作机器人安全功能手册。

* 
  当系统初始化时，所有数据和程序，包括控制参数文件和机器参数文件，将被删除。如果您在初始化系统之前备份数据，则可以在必要时恢复和使用。有关注意事项请参考 ["4.2.5 Data Backup"](../../4-service/2-file-manager/5-data-backup.md) 和 ["4.2.6 Data Restore"](../../4-service/2-file-manager/6-data-restore.md)。
{% endhint %}
[__SOURCE](7-system/6-initialization/3-usage-set/README.md)
# 7.6.3 使用设置

您可以根据操作使用情况选择操作用途并初始化用户键和输入/输出分配信号。

1. 触摸`[5: Initialize - 3: Usage Setting] ([5: Initialize  - 3: Usage Setting])`菜单。

2. 在选择操作用途并根据用途设置环境条件后，触摸`[OK]`按钮。然后，您可以使用与所选操作用途相关的命令并访问相关菜单。
[__SOURCE](7-system/6-initialization/3-usage-set/1-spot-welding.md)
# 7.6.3.1 点焊

如果您将操作用法选择为点焊，您可以使用与点焊相关的命令并访问与点焊相关的菜单。

![](../../../_assets/tp630/init-usage-spot_eng.png)

1. 设置 `[Spot Welding]` 为启用。

2. 分别点击`[User Key Initialization]`下拉菜单和`[Input/Output Assign Initialization]`下拉菜单，并选择点焊。
[__SOURCE](7-system/6-initialization/3-usage-set/2-arc-welding.md)
# 7.6.3.2 弧焊 

如果您选择操作用途为弧焊，则可以使用与弧焊相关的命令并访问与弧焊相关的菜单。

![](../../../_assets/tp630/init-usage-arc_eng.png)

1. 在 `[Arc Welding]` 中设置焊接机类型 \(模拟或数字\)。其他用途将被禁用，系统支持的焊机列表将在屏幕底部显示。

2. 检查焊机列表后，设置焊机编号。

3. 点击 `[User Key Initialization]` 下拉菜单和 `[Input/Output Assign Initialization]` 下拉菜单，分别选择弧焊。
[__SOURCE](7-system/6-initialization/4-serial-encoder-reset.md)
# 7.6.4 串行编码器重置

串行编码器将编码器的旋转速度信息存储在内部内存中。可以通过解除电机错误状态或重置编码器的零点将编码器的旋转速度清除为零。

1. 触摸`[5: 初始化 - 4: 串行编码器重置] ([5: Initialize  - 4: Serial Encoder Reset])`菜单。

2. 为每个轴设置编码器重置模式并检查状态，然后执行重置。

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
        <p>您可以设置是否为每个轴使用编码器重置功能并
          为每个轴设置模式。</p>
        <ul>
          <li>[禁用]: 不会执行串行编码器重置。</li>
          <li>[错误释放]: 您可以仅清除与电机编码器相关的错误，而不清除编码器旋转速度。</li>
          <li>[重置]: 您可以通过解除与电机编码器相关的错误，然后重置编码器的零点来清除旋转速度。</li>
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
          <li>[全选]: 您可以一次性选择所有轴。</li>
          <li>[全部取消]: 您可以一次性取消选择所有轴</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
* 在执行机器人系统的初始设置时，您可以进行编码器重置，但切勿在机器人正常操作时执行编码器重置。如果发生与编码器相关的错误，例如通信错误或编码器电池丢失，您可以执行编码器重置。在这种情况下，请在机器人程序中检查实际位置，以确保与现有机器人原点位置没有差异。
* 如果控制器和编码器未供电，编码器的位置信息可能会丢失，从而可能导致使用机器人作业程序时出现问题。为了解决这个问题，串行编码器上配有专用电池，使得无论控制器的电源状态如何都可以记录位置信息。如果在编码器电池中发生电压错误，必须在控制器仍然供电的情况下更换电池，以防止位置信息的丢失。
{% endhint %}
[__SOURCE](7-system/6-initialization/5-add-axis-param.md)
# 7.6.5 额外轴参数设置

除了机器人本身外，可使用的额外轴包括机器人的基轴（移动轴）、伺服枪轴、定位器轴和夹具轴。有关每个额外轴规格的详细信息，请参阅“额外轴功能手册”。

设置所使用的额外轴的规格和配置等参数的方法如下。

1.	触摸 `5: 初始化 - 5: 额外轴参数设置 (5: Initialize - 5: Additional Axis Parameter Setting)` 菜单。

2.	设置额外轴的规格和配置等参数。

    ![](../../_assets/tp630/init-addaxis_eng.png)





<table>
  <thead>
    <tr>
      <th style="text-align:left">序号</th>
      <th style="text-align:left">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>额外轴的详细参数设置信息。您可以检查并设置额外轴的名称、规格和配置等。</p>
        <ul>
          <li><b>[名称]</b>: 正在使用的额外轴的名称</li>
          <li><b>[轴规格]</b>: 额外轴的规格。您可以根据规格使用单独为每种额外轴用法开发的功能。</li>
          <li><b>[轴结构]</b>: 额外轴的机制类型。在某些轴的规格中，您可以指定提前注册的机制类型。作为示例，您可以在定位情况下选择标准定位器模型。</li>
          <li><b>[轴位置]</b>: 这是轴连接到DSP板的位置。您可以按接线规格顺序指定BD号、DSP号、轴号和刹车号。</li>
          <li><b>[减速比]</b>: 涉及额外轴的电机和连杆的减速比信息
            <ul>
              <li>减速比的符号可以根据当额外轴连杆向（+）方向移动时电机轴的旋转方向进行设置。当从正面查看时，如果轴逆时针旋转，符号将是（+），如果顺时针旋转，符号将是（-）。</li>
              <li>减速比的分子参数是连杆的移动距离（mm或度），分母参数是对应于连杆移动距离的电机转速。设置项的参数将以整数形式定义。对于将以小数显示的参数，请通过将分子和分母乘以某个倍数，将减速比设置为整数。</li>
            </ul>
          </li>
          <li><b>[软限制]</b>: 额外轴的最小和最大操作范围</li>
          <li><b>[AMP规格]</b>: 额外轴的放大器规格</li>
          <li><b>[电机规格]</b>: 连接到额外轴的电机型号</li>
          <li><b>[加速/减速参数]</b>: 额外轴的最大速度和加速时间</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[旋转半径]</b>: 您可以添加新的额外轴或删除额外轴。</li>
          <li><b>[减速比校准]</b>: 您可以校准实际轴位置与显示位置之间的差异。</li>
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
          <li><b>[+]/[-]</b>: 您可以添加新的额外轴或删除额外轴。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
[__SOURCE](7-system/6-initialization/6-mechannism-set.md)
# 7.6.6 机械设置

机械将在接驳操作期间作为一个组使用，接驳键将被分配给它。此外，机械也是一组单元，每个单元在记录或编辑步骤的位置过程中都要区分。当机械设置完成后，将为每个轴组分配机械编号 \(M\#\)。

设置无限功能使用的方法如下。

1. 触摸 `[5: Initialization - 6: Mechanism Setting] ([5: Initialization  - 6: Mechanism Setting])` 菜单。

2. 在设置机械编号并为每个轴配置无限功能后，单击 `[OK]` 按钮。

    ![](../../_assets/tp630/robot-mechanism_eng.png)



* `[Mech]`: 通过触摸下拉菜单，可以设置轴的机械编号。
  * 如果轴的规格是机器人，则机械编号将固定为 M0。
  * 从附加轴开始，您可以将机械编号指定为 M1 到 M7 之间的值。

  * 设置为相同机械编号的轴将作为同一组进行管理。

  * 要接驳附加轴，可以使用 `[Mech]` 按钮在机械之间切换。这时，如果您按下接驳键，将按照相关机械的轴的顺序进行接驳。
* 
  `[Positioner Group]`: 您可以设置定位器组编号。定位器组编号只能为规格设置为定位器的轴设置。

* 
  `[Endless]`: 您可以设置是否在轴上使用无限功能。



{% hint style="info" %}
一组机械单元是可以分配给每个任务并可驱动的最小单元。可以将复杂的机械组合分配给各个任务。
{% endhint %}

#### 




#### 机械接驳规则 

* ${cont_model} 控制器总共提供八个接驳键。
* 
  机械将在接驳操作期间作为一个组使用。

* 
  如果选择机械编号为 `[M0]`，则轴 7 和 8 的接驳键将作为特殊情况运行，并且可以在总轴数包括下一个机械时在八个或更少的范围内操作 M1 和 M2。即便在这种情况下，如果将机械编号设置为 `[M1]`，也可以对 M1 的配置元素执行接驳操作。

* 
  以下显示用法的示例。

  示例 1\) M0: 机器人 \(轴 1-6\)。 M1: 移动轴 \(轴 7\)。 M2: servo枪 \(轴 8\)

  * 选择 `[M0]` => 轴 1-6 的接驳键: M0。 轴 7 的接驳键: M1。 轴 8 的接驳键: M2
  * 选择 `[M1]` => 轴 1 的接驳键: M1
  * 选择 `[M2]` => 轴 1 的接驳键: M2

  示例 2\) M0: 机器人 \(轴 1-6\)。 M1: 移动轴 \(轴 7\)。 M2: servo枪 \(轴 8-9\)

  * 选择 `[M0]` => 轴 1-6 的接驳键: M0。 轴 7 的接驳键: M1
  * 选择 `[M1]` => 轴 1 的接驳键: M1
  * 选择 `[M2]` => 轴 1-2 的接驳键: M2

  示例 3\) M0: 机器人 \(轴 1-7\)。 M1: 移动轴 \(轴 8\)。 M2: servo枪 \(轴 9-10\)

  * 选择 `[M0]` => 轴 1-7 的接驳键: M0。 轴 8 的接驳键: M1
  * 选择 `[M1]` => 轴 1 的接驳键: M1
  * 选择 `[M2]` => 轴 1 的接驳键: M2
[__SOURCE](7-system/6-initialization/7-axis-sync.md)
# 7.6.7 轴同步功能

此功能将两个辅助轴组合成一个同步对，使它们始终移动到相同的位置。

启用轴同步时，指定的辅助轴的位置始终通过软件同步。因此，需要同步的辅助轴必须物理对齐，并且轴原点必须设置，以便软件识别为相同位置。此外，待同步的轴的物理运动方向必须设置为相同。

轴同步支持最多4对辅助轴之间的位置同步。当两个辅助轴分配到同一组时，它们将被视为一个同步对。

更改当前配置的轴同步对的过程如下。

![](../../_assets/tp630/axis-synchronization_eng.png)

1. 如果启用了 R321 同步组移动功能，将它们全部设置为 `不执行 (Disable)`。

2. 选择工程师模式 (R314)，然后导航至 `[F2: 系统] - 5. 初始化 - 8. 附加轴同步设置 ([F2: system] - 5. Initialization - 8. Additional Axis synchronization setting)`

3. 要启用轴同步功能，将 `使用 (Use)` 从 `不执行 (Disable)` 更改为 `启用 (Enable)`。

4. 将要视为一个轴的两个辅助轴分配到同一组。

5. 完成组分配后，按下 `[F7: 确定] ([F7: OK])` 按钮。


{% hint style="info" %}
* 完成轴同步设置后，当激活电机开启时，组对将对齐到中点。等待对齐完成。
* 一旦启用轴同步，单个轴不能独立移动，移动键被分配为单个轴。
* 此功能在执行作业文件时也适用，不仅限于移动操作。
* 即使在重启后，轴同步组对也会保留。
* 如果 `使用 (Use)` 设置为 `不执行 (Disable)`，轴同步功能将不会激活。
* 同步轴组的笛卡尔坐标姿态值与实际机器人姿态匹配。
* 如果由于紧急停止、伺服错误或其他因素导致同步轴之间出现位置误差，则在激活电机时，轴将移动到中点并重新对齐。
{% endhint %}

{% hint style="warning" %}
* 在使用前，请确保电机规格和辅助轴参数适当匹配以进行同步（相同的轴规格、配置、速度和加速度时间）。
* 如果不使用轴同步功能，将 `使用 (Use)` 设置为 `不执行 (Disable)` 并将组对重置为 `不执行 (Disable)`。
* 请勿将此功能与同步组移动功能一起使用。
* 验证作业文件中的步态姿态值在考虑轴同步的情况下实现。
* 请注意，在轴同步操作期间更改设置将影响笛卡尔坐标系统。
{% endhint %}
[__SOURCE](7-system/6-initialization/8-axis-lock/README.md)
# 7.6.8 轴锁

### 功能目的

轴锁功能的目的是在需要因电机、减速器或机器人的其他组件或辅助轴出现问题而进行修理或更换时，暂时禁用特定轴。这使得其他正常轴可以继续操作。通过允许正常轴的运行，此功能提高了机器人的维护便利性和可用性，并最小化某些机器人的生产线效率损失。

![](../../../_assets/tp630/init-axis-lock-purpose_eng.png)

<br>

### 功能范围

所提供的功能范围取决于机器人类型和应用轴锁功能的轴，如下表所示。

|Robot|Axis Lock|Motor ON|JOG(Axis)|JOG(Cartesian)|Step Recording|Command Recording|Command Execution|Step FWD/BWD|Auto Operation|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|所有机器人|机器人轴|o|o|x|x|o|x|x|x|
|所有机器人|辅助轴|o|o|o|o|o|x|o|x|
|*例外机器人|特定轴|o|o|o|o|o|o|o|o|

- *例外机器人的特定轴：
    - HH140G-0A的S轴
    - LCD机器人的L和R轴
    - LCD 2-DOF臂机器人的LA和RA轴

<br>

{% hint style="info" %}
-   仅当输入工程师代码（R314）时，此功能可用。
-   启用此功能时，无法在自动模式下播放。
-   当应用此功能时，相关轴处于锁定状态。

{% endhint %}
[__SOURCE](7-system/6-initialization/8-axis-lock/1-setting.md)
# 7.6.8.1 如何配置功能

### 菜单访问

通过导航到 `[F2: 系统] - 5: 初始化 - 9: 轴锁定设置 ([F2: system] - 5: Initialization - 9: Axis lock setting)` 选择菜单。进入菜单时，系统将提示您确认每个轴的刹车是否正常，如下所示。

{% hint style="warning" %}
由于如果刹车接线异常，机器人可能会跌落，因此请确保每个轴的刹车接线正常后再配置轴锁定功能。
{% endhint %}

![](../../../_assets/tp630/init-axis-lock-menu_eng.png)


### 功能配置

在确认刹车接线正常并进入菜单后，各轴的规格和轴锁定设置状态将如下面所示显示。选择要应用轴锁定的轴，然后按 `[OK]` 退出菜单。

![](../../../_assets/tp630/init-axis-lock-setting_eng.png)
[__SOURCE](7-system/6-initialization/8-axis-lock/2-function-check.md)
# 7.6.8.2 检查功能应用

当轴锁功能被应用时，机器人运动可能会因锁定的轴而有所不同。因此，在操作机器人之前，请始终验证轴锁是否处于激活状态。

您可以通过状态栏、警告信息和监控显示状态检查功能是否被应用。

### 状态显示窗口

状态显示窗口显示机器人操作所需的各种条件。

{% hint style="warning" %}
在使用轴锁功能时，务必在操作机器人之前检查相应的指示灯。
{% endhint %}

-   状态显示窗口：AxLk
-   右侧矩阵：“轴锁”

![](../../../_assets/tp630/init-axis-lock-status_eng.png)


### 监控窗口

在监控期间，轴数据将显示“轴锁”消息，对于任何应用了该功能的轴。如果机器人轴或基础轴被锁定，则坐标值无法显示。在这种情况下，笛卡尔坐标和锁定轴的值将显示为 '------'。

![](../../../_assets/tp630/init-axis-lock-monitor_eng.png)

### 警告信息

切换屏幕或模式时，锁定轴对应的功能范围将显示为警告信息。通过此消息，您可以始终知道轴锁功能是否被应用及其范围。

![](../../../_assets/tp630/init-axis-lock-warning_eng.png)
[__SOURCE](7-system/7-auto-calibration/README.md)
# 7.7 自动校准

要正确使用机器人，可以通过已教授的程序和将自动执行的运动找到机器人的轴原点、工具长度、负载质量和基轴方向。这些校准值将自动反映在机器人中。

1. 触摸`[6: 自动校准]`菜单。然后，自动校准菜单将出现。

2. 通过选择所需菜单，校准机器人的轴原点、工具长度、负载质量、基轴方向等。

    ![](../../_assets/tp630/system-calib-menu_eng.png)
[__SOURCE](7-system/7-auto-calibration/1-axis-origin-tool-length-optimization.md)
# 7.7.1 优化轴原点和工具长度

轴原点和工具长度的优化功能是在不使用外部测量传感器的情况下，校准机器人每个轴的原点和工具长度。

准备两个尖端。一个固定在外部，另一个固定在工具上。然后，仅根据外部固定尖端更改机器人的工具提示的姿态，您需要使用机器人程序记录多个点。在此时，您需要教授七个点以找到轴原点和工具长度，四个点或更多以仅找到工具长度。

![图67 轴原点和工具长度优化功能的教学方法](../../_assets/image_228.png)

{% hint style="info" %}
* 从版本 V70.02-00 开始，轴原点优化功能将不再支持一般用户。如果您希望在后续版本中更改轴原点，请联系客户支持团队以咨询专家或工程师。
{% endhint %}

使用轴原点和工具长度优化功能，即使没有 CAD 数据可用，您也可以找到优化后的工具长度 X、Y 和 Z，以及机器人的优化原点 H、V、R2 和 B 轴。

{% hint style="warning" %}
当使用轴原点和工具长度优化功能时，编码器偏移和工具长度将会改变，从而也改变以前教学程序的操作位置。因此，您应该在编写教学程序之前执行轴原点和工具长度的优化。
{% endhint %}

{% hint style="info" %}
* 使用轴原点和工具长度优化功能时，教学的准确性与最大步位置误差结果的准确性成正比。因此，您应该准备两个尖端，并尽可能准确地进行工具提示教学以匹配这两个尖端。确保在目测检查时，工具提示与空间中固定点的匹配精度在 0.5 mm 以内。
* 每一步设置一个姿态，差异应为 30 度或以上，使得各步的姿态不相似。
* 尽可能大幅度操作手腕轴 \(R2, B, R1\)，在保持各步手腕轴之间足够的 \(尽可能大\) 角度差的情况下进行教学。
* 教学程序必须由隐藏姿态步命令组成。
{% endhint %}

使用轴原点和工具长度优化功能的方法如下。

1. 触摸 `6: 自动校准 - 1: 优化轴原点和工具长度` 菜单。

2. 选择优化目标并设置详细选项。

    ![](../../_assets/tp630/system-calib-tool_eng.png)


<table>
  <thead>
    <tr>
      <th style="text-align:left">序号</th>
      <th style="text-align:left">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>输入轴原点和工具长度优化功能的选项并显示优化结果。</p>
        <ul>
          <li><b>[优化选择]</b>: 您可以选择优化目标。
            <ul>
              <li><b>[工具长度]</b>: 您可以校准机器人的工具长度值。
                如果机器人原点设置正确，您可以仅校准工具长度。</li>
              <li><b>[轴原点 &amp; 工具长度]</b>: 您可以校准机器人的
                原点和工具长度值。
                <br />通常，此功能可在安装机器人并首次设置正确原点时使用。</li>
            </ul>
          </li>
          <li><b>[程序编号]</b>: 您可以设置在多个姿态下记录同一点的程序编号。</li>
          <li><b>[工具编号]</b>: 这是要自动设置的工具的编号。
            这应与设定程序中记录的工具编号匹配。</li>
          <li><b>[步位置误差公差]</b>: 您可以设置自动校准结果的误差范围（初始设置值为 0.6 mm）。如果预期误差在误差范围内，整数数据将自动更新；如果误差超出误差范围，将通知用户是否反映该整数，并与用户确认，然后进行必要的处理。</li>
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
            优化结果将出现在 [最大步位置误差] 中。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
请注意，如果您校准机器人的原点和工具长度值，机器人的所有原点将发生变化，从而改变以前创建程序的位置。
{% endhint %}

{% hint style="info" %}
* 您还可以在设置菜单中设置机器人的每个轴的原点和工具长度。
  * 工具长度: `[system] - 3: Robot Parameter - 1: 工具数据 ([system] - 3: Robot Parameter - 1: Tool Data)`。
  * 每个轴的原点: `[system] - 3: Robot Parameter - 2: 轴原点`
* 如果您使用角度校准功能校准工具角度（`[system] - 3: Robot Parameter - 1: 工具数据 ([system] - 3: Robot Parameter - 1: Tool Data)`），应先执行原点轴和工具长度优化功能，然后再执行角度校准。通过这种方式，工具数据可以正确设置。
{% endhint %}
[__SOURCE](7-system/7-auto-calibration/2-positioner-calib.md)
# 7.7.2 定位器校准

定位器校准是一种功能，使机器人能够与安装在机器人外部的夹具设备的操作进行同步跟进，或相对于夹具设备进行线性或圆形操作。将应用定位器校准功能的外部夹具设备称为定位器或工作站。

使用定位器校准功能使得可以补偿由于机器人操作区域限制而带来的操作困难。换句话说，即使定位器在工件固定在其上时移动，机器人仍然可以通过跟随定位器的移动对工件进行线性或圆形操作。

您可以通过教学三个点来设置1轴定位器的坐标系统，或通过教学五个点来设置2轴定位器的坐标系统。

![图68 1轴定位器 \(左\) / 2轴定位器 \(右\)](../../_assets/image_244.png)

定位器校准的主要功能信息如下。

| 主要功能 | 描述 |
| :--- | :--- |
| 定位器组 | 支持1-4组 |
| 定位器轴数 | 支持1轴定位器和2轴定位器 \(旋转轴\) |
| 插值模式 | 支持线性插值和圆形插值 |

{% hint style="info" %}
* 定位器校准功能可以在设定定位器组时使用。
* 有关更多详细信息，请参阅 "[${cont_model} 控制器定位器同步功能手册](https://hrbook-hrc.web.app/#/view/doc-positioner-sync/zh/README?cont_model=${cont_model})"。
{% endhint %}
[__SOURCE](7-system/7-auto-calibration/3-load-estimation.md)
# 7.7.3 负载估算功能

负载估算是一个通过某种操作自动计算附加在机器人前端的工具的物理特性（质量、重心、惯性）的功能。

操纵器信息（质量、重心、每个链接的惯性）已经注册在控制器中。然而，由于工具在必要时将被附加到机器人前端，因此需要输入工具信息。工具物理特性的信息包括工具质量（kg）、重心位置和安全使用机器人所需的惯性。

如果CAD数据包含工具的物理特性信息，可以通过触摸`[system]`按钮 - `[3: Robot Parameter - 1: Tool Data] ([3: Robot Parameter - 1: Tool Data])`菜单直接输入工具质量、重心位置和惯性。

![](../../_assets/tp630/robot-tool_1_eng.png)

工具数据设置的信息如下。

![Figure 70 Tool Data](../../_assets/image_505.png)

* `[Weight]`：安装在机器人前端的工具的总重量（kg）
* `[Center]`：从机器人法兰面中心到工具重心位置在x、y、z方向的距离（mm）
* `[Inertia]`：关于工具坐标的工具的惯性矩（kg/m2）。惯性矩将根据重心周围的x、y和z轴的质量分布确定，若负载质量分布越远离旋转轴，则惯性将增加。
* 工具数据坐标系统：惯性和重心将相对于x、y和z轴方向表示为数值。

然而，在许多情况下，从CAD数据中确定工具的物理特性如质量、惯性和重心是困难的。这时，您可以使用机器人控制器中的负载估算功能来检查工具的物理特性。

![Figure 71 Load Estimation Function](../../_assets/tp630/system-calib-load_eng.png)

1. 触摸`[6: Auto Calibration - 4: Load Estimation Function] ([6: Auto Calibration - 4: Load Estimation Function])`菜单。

2. 在触摸`[Add. Weight on Each Axis]`按钮后，输入每个轴的附加重量信息。

如果在有附加重量的情况下执行负载估算功能，将判定到所有安装在机器人的重量物体都位于前端。为了准确的负载估算，应该输入每个轴的附加重量信息。

3. 在通过移动机器人的主轴将机器人移动到安全区域后，触摸`[Set pose]`按钮。

4. 在触摸`[Wrist Axis Operation Area]`按钮后，指定在负载估算操作中将使用的手腕轴的操作区域。负载估算可以在与附近设施及操纵器没有干扰的操作区域中进行。

如果不支持`[Wrist Axis Operation Area]`按钮，则跳过此步骤，执行下一步骤。

5. 触摸`[Play check]`按钮。然后，当机器人以低速度运行时，您可以检查与附近设施或操纵器的干扰。

6. 在输入安装在机器人上的工具编号后，触摸`[Play Normal]`按钮。然后，将执行负载估算，计算工具的物理特性。

7. 检查负载估算结果后，触摸`[End]`按钮。然后，计算的工具物理特性将注册在工具编号中。

{% hint style="info" %}
* 附加重量是用户连接到机器人的所有设备的总体重量，如焊接装置和焊接信号线继电器盒，但不包括安装在机器人前端的工具。
* 
  在某些机器人中将不支持手腕轴操作区域功能。

* 需要注意的是，负载估算功能可能无法执行，具体取决于手腕轴操作区域功能的设置值。
* 有关负载估算功能的详细信息，请参阅“负载估算功能手册”。
{% endhint %}
[__SOURCE](7-system/7-auto-calibration/4-base-axis-calibration/README.md)
# 7.7.4 基座轴校准

基座轴校准是一个用于校准轴的安装方向的功能。

几乎不可能将基座轴安装到完全匹配机器人的坐标系统的某个方向（X、Y或Z）。当您使用基座轴校准功能在控制器中计算基座轴的方向时，可以提高包括基座轴在内的系统的线性插值轨迹的性能。

在机器人安装在基座轴上后，此功能使得可以通过找到机器人安装的任何基座轴的方向向量来执行位置插值。

![Figure 72 Base Axis Calibration](../../../_assets/image_497.png)

通常，基座轴用于将机器人移动到操作位置。在特殊情况下，基座轴还可用于保证机器人在基座轴上移动时的线性轨迹。

* 当两个经过基座轴校准的机器人传送工件时（未来将支持多机器人）
* 当您需要在操作基座轴时执行插值时
[__SOURCE](7-system/7-auto-calibration/4-base-axis-calibration/1-base-axis-initial-set.md)
# 7.7.4.1 基轴初始设置

1. 在手动模式下，触摸 `系统 - 5: 初始化 - 5: 附加轴参数设置 (system - 5: Initialize - 5: Additional Axis Parameter Setting)`。

2. 设置完附加轴的规格和配置等参数后，触摸 `[OK]` 按钮。

* `[轴规格]`: 您可以选择附加轴作为基轴的规格。
* `[轴配置]`: 您可以选择附加轴的机制为任意。
* 其他参数: 您可以根据仪器设计值和控制器配置规范设置其他参数。



{% hint style="info" %}
* 当系统初始化时，附加轴设置菜单将会出现，允许您执行基轴的初始设置。
* 
  附加轴参数设置菜单是针对工程师的功能，因此一般用户将无法支持。有关附加轴参数设置菜单的详细信息，请联系工程师进行咨询。
{% endhint %}

{% hint style="warning" %}
* 您只能为第一个基轴使用校准功能，并且在设置附加轴参数时可以将轴配置设置为任意。
* 除第一个基轴外，其他基轴不要将轴配置设置为任意。
* 基轴校准仅在基轴配置为任意时可用。
{% endhint %}
[__SOURCE](7-system/7-auto-calibration/4-base-axis-calibration/2-base-axis-calib-prog-teach.md)
# 7.7.4.2 基座轴校准程序教学

1. 在空间中创建一个参考点，然后记录第一个参考点。

2. 将基座轴移动超过 200 毫米，并记录相同的点作为第二步。

3. 在与步骤 2 中移动的方向相同的方向上移动 200 毫米或更多，记录相同的点作为第三和第四步。

![](../../../_assets/image_526.png)

{% hint style="warning" %}
* 使用已完成机器人校准（轴原点和工具长度优化）的工具来教学行程轴校准程序。
* 
  记录步骤时，使用基座轴校准的工具编号进行记录。

* 
  尽可能设置基座轴在记录步骤之间的移动距离来记录位置。
{% endhint %}
[__SOURCE](7-system/7-auto-calibration/4-base-axis-calibration/3-base-axis-calib-exec.md)
# 7.7.4.3 基座轴校准执行

1. 触摸 `[6: Auto Calibration - 6: Base Axis Calibration] ([6: Auto Calibration  - 6: Base Axis Calibration])` 菜单。

2. 在输入基座轴校准的程序编号后，触摸 `[Auto Setting]` 按钮。

    ![](../../../_assets/tp630/system-calib-base_eng.png)

3. 在检查基座轴的安装方向向量值后，触摸 `[OK]` 按钮。
[__SOURCE](7-system/7-auto-calibration/4-base-axis-calibration/4-operation-after-base-calib.md)
# 7.7.4.4 基座轴校准后的操作

如果您在执行基座轴校准后进行基座轴的移动，基座轴创建方向向量中的行驶距离将转换为当前坐标值。

![图73 基座轴校准后的操作](../../../_assets/image_528.png)

1.	触摸工作区面板堆叠右上角的 `[+]` 按钮，然后在面板选择窗口中触摸 `[Pose]`。

2.	移动基座轴。沿基座轴行驶的距离将转换为 X、Y 和 Z 值，并显示在位姿信息窗口中。

3.	以通常的方式记录和回放步骤。

{% hint style="warning" %}
将移动坐标系设置为工具坐标系，并移动基座轴以检查基座轴是否正确校准。如果执行了工具提示固定操作，则表示基座轴已正确校准。
{% endhint %}
[__SOURCE](7-system/7-auto-calibration/5-gravity-direction-auto-set.md)
# 7.7.5 重力方向自动设置

${cont_model} 控制器基于动力学，因此设置重力方向非常重要。

一般而言，机器人安装方向垂直于重力方向，如下所示。如果机器人斜置于地面，则应在机器人控制器中设置重力方向。此时，可以使用自动重力方向设置功能。

![图74 安装在地面上的机器人重力方向 \(左\) / 安装在斜坡上的机器人重力方向 \(右\)](../../_assets/image_507.png)

设置重力方向的方法如下。

1. 在外部附上一个重物以指示重力方向，然后在重力作用方向上教导两个点 \(步骤1，步骤2\)。

2. 触摸 `[6: Auto Calibration - 8: Automatic setting of gravity direction] ([6: Auto Calibration  - 8: Automatic setting of gravity direction])` 菜单。

3. 输入程序编号后，触摸 `[Execute]` 按钮。然后，方向向量将被计算并显示。

    ![](../../_assets/tp630/system-calib-gravity_eng.png)

4. 检查方向向量值后，触摸 `[OK]` 按钮。然后，方向将被设置为重力方向。
[__SOURCE](7-system/7-auto-calibration/6-robot-tool-calibration.md)
# 7.7.6 机器人的校准和工具

机器人和工具的校准功能将在可以使用 3D 测量设备测量机器人位置的环境中使用。

1. 在机器人工具提示下选择要测量的位置，移动机器人的位置和姿势以多种方式测量超过 15 个点的位置，并将机器人的位置记录为程序。

    ![](../../_assets/image_245.png)

2. 将测量到的机器人位置数据（测量点数据）整理为 X、Y 和 Z 格式，然后创建一个文件（格式：ASCII 扩展名：MSR）。

    ![](../../_assets/tp630/system-calib-robottool-msr.png)

3. 将位置数据文件保存到可移动存储设备中，然后将可移动存储设备连接到教学挂件。状态栏中将出现 `[USB]` 图标（）。

4. 点击 `[6: 自动校准 - 9: 机器人和工具校准条件] ([6: Auto Calibration  - 9: Robot and Tool calibration condition])` 菜单。

5. 点击 `[Explorer]` 按钮选择一个位置数据文件，并设置用于测量的机器人程序。

    ![](../../_assets/tp630/system-calib-robottool_eng.png)

6. 点击 `[OK]` 按钮。然后，屏幕将切换到机器人和工具校准屏幕。

7. 点击机器人和工具校准执行屏幕上的 `[Execute]` 按钮。然后，校准结果将出现。

    ![](../../_assets/tp630/system-calib-robottool-exe_eng.png)

8. 检查校准结果后，点击 `[OK]` 按钮。然后，校准结果将自动应用于轴原点和工具整数。

9. 点击 `[3: 机器人参数 - 1: 工具数据] ([3: Robot Parameter  - 1: Tool Data])` 菜单。然后，您可以检查机器人校准执行结果。

    ![](../../_assets/tp630/system-calib-robottool-toolinfo_eng.png)

<Br>

{% hint style="info" %}
校准参数的轴原点和工具长度 X、Y 和 Z 值为轴 2-5（H、V、R2 和 B 轴）所选。仅校准工具时，需在取消选择每个轴的值后再执行。
{% endhint %}

<br>

#### 恢复校准数据

在执行机器人和工具校准时，校准数据作为 calibration.json 文件单独存储在路径 /ata0:2/lib/hi6/backup/ 中。<br>
如果因为系统初始化等操作而丢失校准数据，可以使用存储的文件进行恢复。（但是，如果通过执行串行编码器重置初始化了编码器数据，则无法恢复。）

1. 如果路径 /ata0:2/lib/hi6/backup/ 中存在 calibration.json 文件，则“恢复”按钮将被激活。
2. 在进行恢复并重新上电后，先前执行的机器人和工具校准数据将被应用。

![](../../_assets/tp630/robot_calib_recover.png)
[__SOURCE](7-system/7-auto-calibration/7-addaxis-autotuning.md)
# 7.7.7 额外轴自动调优

* 从版本 V60.28-00 可用。
</br>

### A. 概述

此功能通过在用户设置的范围内移动额外轴来找到最佳增益。当额外轴没有正确设置增益而导致噪音或控制性能不佳时，可以使用此功能。

| ![alt text](../../_assets/직동축.gif) | ![alt text](../../_assets/회전축.gif) |
|---|---|
| 线性轴运动 | 圆形轴运动 |


### B. 调优描述

![](../../_assets/_7.7.7_intro_en.png)

![c1](../../_assets/c1.png)  **调优前的设置**

`附加轴 (Additional axis)`: 选择您希望调优的额外轴。

`运动范围`: 设置额外轴运动范围(线性轴: 2, 5, 10[mm] / 圆形轴: 2, 5, 10[deg])。通过慢速移动额外轴，调整适当的额外轴运动范围。较大的运动范围可以获得更好的调优效果（超过当前规格的最大范围10 mm（或10 deg）的运动需要额外开发）。

* 起始位置: 额外轴自动调优开始时的起始位置。
* 结束位置: 额外轴自动调优开始时的结束位置。
* 当前 position: 指示额外轴的当前位置。

**调优增益(Kv)**: 正在调优的参数值。

</br>

![c2](../../_assets/c2.png) **调优过程（范围测试 > 运动测试 > 运行）**

**1. 范围测试**

* 在设定的运动范围内以低速移动。如果额外轴运动范围存在任何问题，请按停止按钮并重置运动范围。

**2. 运动测试**

* 在设定的运动范围内以高速移动以检查初始调优增益值。

**3. 运行**

* 额外轴自动调优过程开始。
* 在调优过程中，额外轴可能会发出短暂的响声（因为它正在寻找振动增益值）。
* 调优完成后，将显示调优参数 Kv 调优前后的增益值。按下 `[OK]` 会弹出一个窗口询问是否应用调优增益。如果按下 `[enter]`，将应用调优增益。如果按下 `[No]`，将保留原始增益值。

{% hint style="warning" %}

由于噪声数据分析困难，因此调优的精度无法与调优专家手动调整时一样。如果需要手动调优，可以通过调整 Kv 增益来进行。
{% endhint %}

* 如果调优增益导致噪音，运动跟踪性能可能会下降，导致大幅抖动。
* 反之，如果 Kv 增益过高，电机可能会产生高频噪音。

如果调优增益导致噪音，请导航至 `[System] - 3:机器人参数 - 33:伺服参数 - 1:伺服环路增益 ([System] - 3:Robot parameter - 33:Servo parameter - 1:Servo loop gain)`，逐渐降低 Kv 值（当 Kv 值变化时，其他增益值会自动重新计算），直到高频噪音消失。

如果噪音仍然存在，请联系我们以获得进一步帮助。
[__SOURCE](7-system/8-safety-system.md)
<script id="page-config" type="application/json">
{
	"permittedStrs": ["Hi7"]
}
</script>

# 7.8 安全系统 

{% hint style="info" %}
该功能由 Hi7 控制器支持。
{% endhint %}

1.	触摸 `[8: 安全系统]` 菜单。然后，安全系统的菜单将出现。

2.	选择所需菜单以执行基本设置、参数设置、监控、证书或安全雷达。

![](../_assets/tp630/system-safety-menu.png)

{% hint style="info" %}
有关安全系统 1: 基本设置，2: 参数设置，3: 监控和 4: 证书的详细信息，请参阅 "[SafeSpace2.0 Manual](https://hrbook-hrc.web.app/#/view/doc-safespace2.0/zh/README)"。
{% endhint %}

{% hint style="info" %}
有关安全雷达的详细信息，请参阅 "[Object Detection System](https://github.com/hyundai-robotics/doc-Object-Detection-System)"。
{% endhint %}
[__SOURCE](7-system/9-cobot-system.md)
<script id="page-config" type="application/json">
{
	"permittedStrs": ["Hi7"]
}
</script>

# 7.9 协作机器人系统

{% hint style="info" %}
此功能在 Hi7 控制器上受支持。
{% endhint %}


1.	触摸 `[Cobot System]`。协作机器人系统菜单将出现。

2.	选择所需菜单以执行碰撞检测或直接教学。

![](../../_assets/tp630/system-cobot-menu.png)

{% hint style="info" %}
有关协作机器人系统的详细信息，请参考 "[安全功能手册 - 协作机器人](https://hrbook-hrc.web.app/#/view/doc-cobot-safety-function/zh/README)"。
{% endhint %}
[__SOURCE](7-system/10-option-system/README.md)
<script id="page-config" type="application/json">
{
	"permittedStrs": ["Hi7"]
}
</script>

# 7.10 选项系统

{% hint style="info" %}
此功能从 Hi7 控制器开始支持。
{% endhint %}

1.	触摸 `[Option System]`。选项系统菜单出现。

2.	选择所需菜单以执行相应功能。

![](../../_assets/tp630/system-option-menu.png)
[__SOURCE](7-system/10-option-system/1-userdio-board-setting.md)
<script id="page-config" type="application/json">
{
	"permittedStrs": ["Hi7"]
}
</script>

# 7.10.1 用户 DIO 板设置

{% hint style="info" %}
此功能自 Hi7 控制器开始支持。
{% endhint %}


在 Hi7 控制器中，用户 DIO 板 (BD681) 和扩展 DIO 板 (BD682) 可以用于处理数字输入/输出信号和输送机接口。


![](../../_assets/tp630/system-option-dio.png)

{% hint style="info" %}
有关用户 DIO 板设置的详细信息，请参阅 "[Hi7 机器人控制器功能手册 - 用户 DIO，扩展 DIO](https://hrbook-hrc.web.app/#/view/doc-userDIO-ExtensionDIO/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/README.md)
# 8. R 代码

当涉及到常用功能的操作程序时，例如修改程序的内容或更改控制器的设置状态，您可以通过指定特定的服务代码 \(R 代码\) 轻松使用它们。

R 代码采用 "R+No." 格式配置，其中 R 代表重置和快速，后跟一个数字。
[__SOURCE](8-r-code/1-use-r-code.md)
# 8.1 使用 R 代码

使用 R 代码执行指定功能的方法如下。

1. 按下键盘上的 `[R..[NO]]` 键。然后，R 代码的弹出窗口将出现。

    ![](../_assets/tp630/k-r.png)



2. 在输入区输入代码号码，然后触摸 `[OK]` 按钮或按下 `[ENTER]` 键。然后，将执行指定于所选 R 代码的功能。

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
      <td>初始化步进计数器并移动到 STEP0。</td>
    </tr>
    <tr>
      <td>R1 : 重置错误</td>
      <td>发生错误或警告时清除状态。</td>
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
      <td>此功能用于单独删除已写入的作业。</td>
    </tr>
    <tr>
      <td>R286 : 显示软件版本</td>
      <td>快速启动 [服务] -> [7: 系统诊断] -> [1: 系统版本]</td>
    </tr>
    <tr>
      <td>R321 : 轴同步 jog 设置</td>
      <td>显示设置屏幕以将任意轴分组为一个同步组，并使用单个 jog 键进行 jog 功能。</td>
    </tr>
    <tr>
      <td>R360 : 手动设置 contpath</td>
      <td>此功能强制更改 CONTPATH 的执行状态。</td>
    </tr>
    <tr>
      <td>R361 : 设置 jog 缓冲级别</td>
      <td>当您想要更改当前设置级别的缓冲距离时使用此功能。</td>
    </tr>
    <tr>
      <td>R362 : 轴控制状态更改</td>
      <td>手动执行辅助轴的控制状态 (axisctrl 开/关)。</td>
    </tr>
  </tbody>
</table>
[__SOURCE](8-r-code/2-r0.md)
# 8.2 R0 用于重置步数计数器

在收藏夹窗口中输入 0 后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

![](../_assets/tp630/pop-rcode_eng.png)

您可以初始化步数计数器以移动到 STEP0。您还可以执行以下功能。

* 清除播放执行状态
* 关闭整体异常信号和灯
* 关闭报警信号
* 清除等待状态
* 清除各种应用功能的状态和信号



{% hint style="info" %}
R0 代码在机器人启动期间无法使用。
{% endhint %}
[__SOURCE](8-r-code/3-r115.md)
# 8.3 R115 复制程序

您可以将主板上的 JOB 程序复制到主板上的另一个程序。在输入要复制的程序编号后，输入要将复制的程序复制到的程序编号。

1. 在收藏窗口输入 115 后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

2. 在输入您要复制的程序 \(原始\) 的编号以及您要将复制的程序复制到的程序 \(目标\) 的编号后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。然后，程序将被复制。

    ![](../_assets/tp630/pop-rcode-115_end.png)

* 如果要将复制的程序复制到的程序已经存在相同编号的程序，您需要选择是否覆盖该文件。
* 
  如果没有原始文件可供复制，将会出现通知消息 \("没有原始文件存在."\)。



{% hint style="info" %}
代码 R115 在程序运行时无法使用；必须在程序停止时使用。
{% endhint %}
[__SOURCE](8-r-code/4-r117.md)
# 8.4 R117 用于删除程序

您可以单独删除内部存储器中的程序。

1. 在收藏夹窗口输入117后，触摸`[OK]`按钮或按下`[ENTER]`键。

2. 输入您想删除的程序的编号后，触摸`[OK]`按钮或按下`[ENTER]`键。然后，删除确认窗口将出现。

    ![](../_assets/tp630/pop-rcode-117_eng.png)

* 如果没有文件可供删除，将出现通知消息（“不存在文件。”）
* 如果您想删除受保护的程序，将出现通知消息（“受保护的文件。”）

3. 在删除确认窗口中，触摸`[OK]`按钮或按下`[ENTER]`键。然后，所选程序将被删除。

{% hint style="info" %}
R117 代码不能在自动模式下使用。必须在手动模式下使用。
{% endhint %}
[__SOURCE](8-r-code/5-r210.md)
# 8.5 R210 选择点焊枪号

您可以选择在使用多个点焊枪（伺服枪或气动枪）时使用的点焊枪。

1. 在收藏夹窗口中输入210后，触摸`[OK]`按钮或按下`[ENTER]`键。

2. 输入要使用的点焊枪号后，触摸`[OK]`按钮或按下`[ENTER]`键。

    ![](../_assets/tp630/pop-rcode-210_eng.png)

* 选定的点焊枪号将在${cont_model}教导挂件屏幕的右下角显示。
* 如果您更改点焊枪号，所指定的工具号将在相应的点焊枪工具号中自动更改。您可以在`[system - 4: Application Parameter - 1: Spot Welding - 2:Welding gun parameter] ([system  - 4: Application Parameter  - 1: Spot Welding  - 2:Welding gun parameter])`菜单中检查相应的点焊枪工具号。

{% hint style="info" %}
* R210代码无法在机器人启动期间使用。
* 点焊枪号只能在点焊环境中设置（`[system - 5: 初始化 - 3: Usage Setting] ([system  - 5: Initialize - 3: Usage Setting])`菜单中的`[Spot Welding]`项目设置为启用）。
* 您可以手动打开、关闭和夹紧选定的点焊枪。有关点焊功能的详细信息，请参阅"${cont_model}控制器点焊功能手册"。
{% endhint %}
[__SOURCE](8-r-code/6-r211.md)
# 8.6 R211 用于设置伺服枪挤压力

您可以在执行伺服枪挤压时手动设置挤压力。

1. 在收藏夹窗口输入211后，触摸`[OK]`按钮或按下`[ENTER]`键。

2. 输入挤压力后，触摸`[OK]`按钮或按下`[ENTER]`键。

    ![](../_assets/tp630/pop-rcode-211_eng.png)



* 焊接条件文件中的挤压力不会被更改。
* 如果输入的挤压力大于或小于伺服枪参数的电流/压力表的上限，将出现警告消息。



{% hint style="info" %}
* R211 代码在机器人启动期间无法使用。
* 
  点焊枪编号只能在点焊环境中设置（`[system - 5: 初始化 - 3: Usage Setting] ([system  - 5: Initialize - 3: Usage Setting])` 菜单中的 `[Spot Welding]` 项设置为启用）。

* 有关伺服枪挤压力手动设置的详细信息，请参阅 "[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/7-r212.md)
# 8.7 R212 用于预设伺服枪移动电极磨损量

您可以手动设置伺服枪移动电极的磨损量。

1. 在收藏夹窗口中输入 212 后，触摸 `[OK]` 按钮或按下 `[ENTER]` 键。

2. 输入移动电极磨损量后，触摸 `[OK]` 按钮或按下 `[ENTER]` 键。

    ![](../_assets/tp630/pop-rcode-212_eng.png)

{% hint style="warning" %}
需要注意的是，如果设置值大于或小于电极的实际磨损量，可能会导致夹紧力不匹配或与工件干涉。
{% endhint %}

{% hint style="info" %}
* R212 代码在机器人启动期间无法使用。
* 仅可以在点焊环境中设置点焊枪编号 \(`[Spot Welding]` 项在 `[system - 5: 初始化 - 3: Usage Setting] ([system  - 5: Initialize - 3: Usage Setting])` 菜单中设置为启用\)。
* 有关伺服枪移动电极磨损量的手动设置的详细信息，请参阅 "[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/8-r213.md)
# 8.8 R213用于预设伺服枪固定电极磨损量

您可以手动设置伺服枪固定电极的磨损量。

1. 在收藏夹窗口输入213后，触摸`[OK]`按钮或按下`[ENTER]`键。

2. 输入固定电极磨损量后，触摸`[OK]`按钮或按下`[ENTER]`键。

    ![](../_assets/tp630/pop-rcode-213_eng.png)

{% hint style="warning" %}
需要注意的是，如果设置的值大于或小于电极的实际磨损量，可能会导致夹紧力不匹配或与工件发生干涉。
{% endhint %}

{% hint style="info" %}
* R213代码在机器人的启动过程中无法使用。
* 点焊号只能在点焊环境中设置 \(`[Spot Welding]`项目在`[system - 5: 初始化 - 3: Usage Setting] ([system  - 5: Initialize - 3: Usage Setting])`菜单中设置为启用\)。
* 有关伺服枪固定电极磨损量的手动设置的详细信息，请参阅"[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/9-r214.md)
# 8.9 R214 同时选择焊接枪

您可以选择在焊接操作中同时使用的点焊枪（伺服枪或气动枪）的数量。

1. 在收藏夹窗口中输入 214 后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

2. 输入要同时使用的焊接枪的数量后，触摸 `[OK]` 按钮或按 `[ENTER]` 键。

    ![](../_assets/tp630/pop-rcode-214_eng.png)

* 选定的点枪编号将在 ${cont_model} 教学挂架屏幕的右下角显示。
* 如果您选择的点焊枪类型不同，将出现通知消息（“当前选择的枪类型设置不正确。”）。

<Br>

{% hint style="info" %}
* R214 代码在机器人启动期间无法使用。
* 点枪编号只能在点焊环境中设置（`[system - 5: 初始化 - 3: 使用设置]` 菜单中的 `[Spot Welding]` 项已设置为启用）。
* 您可以在 `[system - 4: 应用参数 - 1: 点焊 - 2: 焊枪参数]` 菜单中检查点焊枪的设置状态。
  * 当选择一把枪作为多同步枪时，所选枪的手动挤压/打开/关闭操作将与之前选择的枪同步进行。
  * 当选择一把枪作为多同步枪时，如果枪的 LED 状态为开启，则将以同步点格式记录 SPOT 命令。
* 选定的点焊枪可以手动操作。有关点焊功能的详细信息，请参阅 "[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/10-r215.md)
# 8.10 R215 在点焊条件中设置夹紧力

您可以在焊接条件表中设置伺服枪焊接所需的夹紧力。您也可以在`系统 - 4: 应用参数 - 1: 点焊 - 4: 焊接数据 (条件, 顺序) - 2: 焊接条件 (系统 - 4: 应用参数 - 1: 点焊 - 4: 焊接数据 (条件, 顺序) - 2: 焊接条件)`菜单中设置夹紧力。

1. 输入215后，触摸`[OK]`按钮或按下`[ENTER]`键。

2. 输入焊接条件编号后，触摸`[OK]`按钮或按下`[ENTER]`键。

    ![](../_assets/tp630/pop-rcode-215-1_eng.png)

3. 输入伺服枪夹紧力后，触摸`[OK]`按钮或按下`[ENTER]`键。

    ![](../_assets/tp630/pop-rcode-215-2_eng.png)
[__SOURCE](8-r-code/11-r220.md)
# 8.11 R220 用于设置面板厚度 \(Sv\)

您可以手动设置面板厚度，以记录伺服枪点焊步骤。

如果您在伺服枪固定电极仅与面板接触的状态下执行同时记录 MOVE 和 SPOT 语句的一键录制，那么移动电极的位置将根据面板厚度和磨损量自动记录在 MOVE 语句中。

1. 在收藏窗口输入 220 后，触摸 `[OK]` 按钮或按下 `[ENTER]` 键。

2. 输入面板厚度后，触摸 `[OK]` 按钮或按下 `[ENTER]` 键。

    ![](../_assets/tp630/pop-rcode-220_eng.png)



{% hint style="info" %}
有关面板厚度的手动设置的详细信息，请参阅 "[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/12-r314.md)
# 8.12 R314工程模式

在R代码窗口中，输入314，然后触摸`[OK]`按钮或按`[ENTER]`键。

![](../_assets/tp630/pop-rcode-314-1_eng.png)

完成后，以下显示会在屏幕的右上角闪烁。

![](../_assets/tp630/eng-mode.png)

在工程模式中可以设置以下功能。

* 轴原点（机器人参数）  
* 软极限（机器人参数）  
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

* 请注意，在工程模式中的不正确设置可能会导致机器人系统出现严重问题。{% endhint %}
[__SOURCE](8-r-code/13-r358.md)
# 8.13 R358 用于更换伺服工具

您可以在伺服工具更换系统中手动连接和断开伺服工具。

要在伺服工具更换系统中更换伺服工具，您需要使用物理自动工具更换 \(ATC\) 设备断开或连接电源和各种信号线。

当伺服工具是伺服枪时，如果您想手动执行更换工作，您需要在电机开启的情况下将机器人移动到可以连接或断开机器人的伺服枪支撑台，然后执行更换工作。如果伺服工具是其他类型，例如定位器，则在完成连接和断开工作的准备后可以执行更换工作。

R358 伺服工具更换参数及示例如下。

![](../_assets/image_546.png)

使用 R358 代码更换伺服工具的方法如下。

1. 在收藏窗口中输入 358，然后触摸 `[OK]` 按钮或按下 `[ENTER]` 键。

2. 在输入更换操作编号 \(0: 断开, 1: 连接, 2: 固定\) 后，触摸 `[OK]` 按钮或按下 `[ENTER]` 键。

    ![](../_assets/tp630/pop-rcode-358-1_eng.png)

3. 在输入要更换的焊接枪编号后，触摸 `[OK]` 按钮或按下 `[ENTER]` 键。所选焊接枪编号将在 ${cont_model} 教学挂件屏幕的右下角显示。

    ![](../_assets/tp630/pop-rcode-358-2_eng.png)

{% hint style="info" %}
* R358 代码不能在自动模式下使用。必须在手动模式下使用。
* 
  当点焊枪编号更改时，相应工具编号指定的工具编号将被自动更改。您可以在 `[system - 4: Application Parameter - 1: Spot Welding - 2:Welding gun parameter] ([system  - 4: Application Parameter  - 1: Spot Welding  - 2:Welding gun parameter])` 菜单中检查点焊枪相应工具编号。

* 
  只有在电机开启时才能进行伺服工具更换设置。

* 有关伺服工具更换的详细信息，请参阅 "[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](8-r-code/14-r359.md)
# 8.14 R359用于伺服工具编码器电源开启继电器

如果伺服枪在伺服工具更换系统中应用，当第一次安装伺服工具时，您需要执行此功能以重置伺服工具轴的编码器。

1. 在收藏夹窗口中输入359后，触摸`[OK]`按钮或按`[ENTER]`键。

2. 在输入1后，触摸`[OK]`按钮或按`[ENTER]`键。然后，电源将供应给编码器。

    ![](../_assets/tp630/pop-rcode-359_eng.png)



{% hint style="info" %}
* R359代码无法在自动模式下使用。必须在手动模式下使用。
* 
  要禁用伺服枪编码器的强制电源供应，您应该关闭控制器的电源，然后再重新开启。因此，当编码器重置完成后，请关闭控制器的电源并重新开启，然后进行手动连接。

* 伺服工具编码器电源设置功能是为工程师设计的，因此不支持一般用户。有关此功能的更多信息，请联系我们的工程师。
* 有关伺服工具编码器电源设置的详细信息，请参阅“[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)”。
{% endhint %}

{% hint style="warning" %}
在强制供应编码器电源时，切勿机械连接或断开伺服枪。
{% endhint %}
[__SOURCE](8-r-code/15-r360.md)
# 8.15 R360 手动设置 CONTPATH

它手动更改 CONTPATH（连续路径）模式。输入范围为 0, 1 和 2，每个数字的描述如下。（与 [5.7 contpath](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/5-moving-robot/7-contpath?cont_model=${cont_model}) 声明相同。）

<table>
  <thead>
    <tr>
      <th style="text-align:left">编号</th>
		<th style="text-align:left">含义</th>
      <th style="text-align:left">描述</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
		<td>不连续</td>
      <td style="text-align:left">
        如果步骤包含功能，当到达步骤位置时，机器人暂停时执行功能，然后移动到下一个步骤。
      </td>
	 </tr>
	 <tr>
		<td>1</td>
		<td>连续。<br>但是，输入信号是不连续的（默认）</td>
      <td style="text-align:left">
        在步骤运动期间，当机器人移动时，目标步骤中的功能被执行，然后通过目标步骤移动到下一个步骤。<br>
		但是，在输出功能的情况下，实际输出点在命令值达到准确范围内时输出。<br>
		此外，如果输入信号用于命令的参数，当机器人暂停时执行功能，然后移动到下一个步骤。
      </td>
	 </tr>
	 <tr>
		<td>2</td>
		<td>连续。<br>输入信号也是连续的</td>
      <td style="text-align:left">
        即使命令包含输入信号，它也会预先被解释并连续移动。
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
  1) 在不连续条件下的不连续操作：步骤 FWD，步骤 BWD，一步回放
  2) GUN1 或 GUN2 步骤。
  3) 如果 accu=0 且值为 0
  4) 如果工具编号改变

{% endhint %}

操作方法如下：

1. 按下 R 按钮，输入 360，触摸 `[OK]` 按钮，或按 <b>ENTER</b> 键。

2. 输入连续通过编号（0~2），触摸 `[OK]` 按钮，或按 <b>ENTER</b> 键。

![](../_assets/tp630/pop-rcode-360.png)

3. 可以通过标题栏中的 `CP0`、`CP1` 或 `CP2` 标志检查更改的模式。

![](../_assets/tp630/flag-cp.png)
[__SOURCE](8-r-code/16-r361.md)
# 8.16 R361 设置点动微进阶级别

R361 点动微进阶级别设置信息如下。

![](../_assets/image_538.png)

更改当前设定级别的微进阶距离的方法如下。

1. 在收藏夹窗口输入 361 后，触摸 `[OK]` 按钮或按下 `[ENTER]` 键。

2. 输入点动微进阶级别的单位 \(0: 距离. 1: 角度\)，然后触摸 `[OK]` 按钮或按下 `[ENTER]` 键。

    ![](../_assets/tp630/pop-rcode-361-1_eng.png)


3. 如果您输入 '1'，请输入微进阶角度并触摸 `[OK]` 按钮或按下 `[ENTER]` 键。

    ![](../_assets/tp630/pop-rcode-361-2_eng.png)

{% hint style="info" %}
* R361 代码不能在自动模式下使用。必须在手动模式下使用。
* 使用 R361 代码设置的微进阶距离将应用于当前设定的点动级别。因此，如果当前点动速度级别是 8，则将更改与 8 相对应的微进阶距离。
* 仅在点动微进阶键被激活 \(LED 开\) 时，才能进行点动微进阶。
{% endhint %}
[__SOURCE](8-r-code/17-r321.md)
# 8.17 R321 轴同步 jog 设置

这是一个将任意轴组合成一个同步组并通过单个 jog 键控制它们的功能。

![](../_assets/tp630/init-axis-sync-jog.png)

使用轴同步 jog 功能的方法如下。

1. 将您希望通过一个键移动的轴设置为相同的同步组，并按下 `[OK]` 按钮。
2. 使用 jog 键进行轴同步 jog。
3. 使用完轴同步 jog 功能后，将所有同步组设置为无效。

{% hint style="info" %}
* 此功能仅在 jog 时有效。同步功能在自动模式下不适用。
* 同步 jog 对在重启时不会初始化。
* 同步 jog 对在笛卡尔坐标系中的姿态值与实际机器人（简单 jog 功能）的姿态情况不匹配。
{% endhint %}
[__SOURCE](9-property/README.md)
# 9. 属性

当教授焊接操作的作业程序时，您应该设置弧焊特定的细节，例如编织、重试/重新开始和焊工的特性，以及焊接条件如电压和电流。此外，有些情况下您还应检查步骤或辅助点的位置。
[__SOURCE](9-property/1-use-property.md)
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
[__SOURCE](9-property/2-move-step-position/README.md)
# 9.2 移动步骤位置

您可以检查或修改当前在 JOB 程序中选择的行的步骤位置。
[__SOURCE](9-property/2-move-step-position/1-hidden-pose-move.md)
# 9.2.1 隐藏姿态移动语句

您可以检查或修改隐藏姿态移动语句中当前步骤的位置（由 `[REC]` 键记录的步骤，即不包含姿态变量的移动语句）。

1.	触摸作为隐藏姿态记录的移动命令（移动语句）中的 `[property]` 按钮。然后，当前步骤位置将出现。

2.	检查和修改当前步骤位置。

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
        <p>当前步骤的位置信息。您可以检查和设置名称、坐标值和坐标系统格式等。</p>
        <ul>
          <li><b>[名称]</b>: 当前步骤的编号。输入步骤编号后，按 <b>`[ENTER]` </b> 键以移动到相关步骤。</li>
          <li><b>坐标值</b>: 当前步骤的当前坐标值
            <ul>
              <li>使用光标键选择项目。</li>
              <li>在所需项目中输入值后，按 `[ENTER]` 键以反映更改。</li>
              <li>如果坐标系统格式设置为编码器，则坐标值将不会更改。</li>
            </ul>
          </li>
          <li><b>[坐标系统]</b>: 表示当前步骤位置的坐标系统格式</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>`[确认]`: 您可以保存更改。</li>
          <li><b>[上一个]/[下一个]</b>: 您可以显示前一个或下一个步骤的信息。</li>
          <li><b>[原始值]</b>: 您可以显示当前步骤的原始隐藏姿态值。</li>
          <li><b>[当前机器人姿态]</b>: 您可以显示机器人当前处于的姿态值。</li>
          <li><b>[移动]</b>: 触摸按钮将使机器人移动到记录的步骤位置（Jog）。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

3.	触摸 `[确认]` 按钮。然后，更改将被保存到作业程序中，操作将结束。

* 如果您通过按 `[ESC]` 键结束操作，则更改将不会被保存。 

{% hint style="info" %}
* 如果 `[机器人配置]` 设置为未指定，则机器人将指定与当前机器人位置最接近的配置。
* 
  有关根据机器人配置的指定，请参阅 "[2.3.2.2 基座和机器人录制坐标](../../2-operation/3-step/2-step-pose-modify/2-base-robot-crd-sys.md)"。
{% endhint %}
[__SOURCE](9-property/2-move-step-position/2-pose-rec-move.md)
# 9.2.2 位姿记录移动语句和位姿赋值语句

您可以在移动语句中编辑位姿变量值，包括位姿变量或位姿变量赋值语句。

1.	触摸记录为位姿变量的移动命令 \(移动语句\) 中的 `[property]` 按钮。然后，位姿变量设置屏幕将会出现。

2.	检查并修改当前位姿变量。

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
        <p>当前位姿变量信息。您可以查看并设置名称、坐标值、坐标系格式等。</p>
        <ul>
          <li><b>[名称]</b>: 当前位姿变量的名称</li>
          <li><b>坐标值</b>: 当前位姿变量的坐标值
            <ul>
              <li>使用光标键选择项目。</li>
              <li>在所需项目中输入值后，按下 <b>`[ENTER]`</b> 键以反映更改。</li>
              <li>如果坐标系格式设置为编码器，坐标值将不会改变。</li>
            </ul>
          </li>
          <li><b>[坐标系]</b>: 表示当前位姿变量位置的坐标系格式</li>
          <li><b>[配置]</b>: 当描述机器人位置时，由于设备特性存在多个解决方案，因此指定机器人配置以唯一描述配置。
            <ul>
              <li>此功能仅在坐标系类型设置为基座或机器人时可用。</li>
              <li>有关机器人配置的详细信息，请参见“<a href="../../operation/step/step-pose-modify/">2.3.2 记录和更改步骤位置</a><b>.</b> ”</li>
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
          <li><b>[上一个]/[下一个]</b>: 您可以显示上一个或下一个步骤的信息。</li>
          <li><b>[原始值]</b>: 您可以显示当前步骤的原始隐藏位姿值。</li>
          <li><b>[当前机器人位姿]</b>: 您可以显示机器人当前采取的位姿值。</li>
          <li><b>[移动]</b>: 触摸该按钮将使机器人移动到记录的步骤位置 (Jog)。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

3.	触摸 `[确定]` 按钮。然后，更改将保存在作业程序中，操作将结束。

* 如果您通过按 `[ESC]` 键结束操作，则更改不会被保存。
[__SOURCE](9-property/3-spot-welding-func.md)
# 9.3 点焊功能

在编写程序时，如果您在手动模式下将光标放置在点焊功能的位置，并触摸 `[property]` 按钮，则 `[1: 点焊]` 菜单将在应用程序参数设置菜单屏幕中高亮显示。使用点焊功能，您可以快速修改焊接条件的内容以及在进行点焊时的焊接顺序。

![Figure 76 Spot Welding Function](../_assets/tp630/app-spot-menu_eng.png)

{% hint style="info" %}
* 您可以通过触摸 `[system]` 按钮 - `[4: 应用程序参数 - 1: 点焊] ([4: Application Parameter  - 1: Spot Welding])` 来使用点焊功能。
* 
  有关点焊功能的详细信息，请参考 "[${cont_model} 控制器点焊功能手册](https://hrbook-hrc.web.app/#/view/doc-spot-weld/zh/README)"。
{% endhint %}
[__SOURCE](10-robot-language.md)
# 10. 机器人语言

有关机器人语言的详细信息，请参阅 "[${cont_model} 机器人控制器功能手册. - 机器人语言 HRScript](https://hrbook-hrc.web.app/#/view/doc-hrscript/zh/README?cont_model=${cont_model})"
[__SOURCE](11-etc/README.md)
# 11. 其他

本章解释之前未涵盖的其他信息。
[__SOURCE](11-etc/1-controller-files/README.md)
# 11.1 机器控制器中的主要文件夹和文件

各种配置、教学和日志文件存储在机器人控制器内。
在本节中，我们描述文件夹结构和各个文件的角色。
[__SOURCE](11-etc/1-controller-files/1-caution-ftp.md)
# 11.1.1 通过 FTP 加载到 project/ 文件夹时的注意事项

{% hint style="warning" %}
`[Warning]` TP 文件管理器或 FTP 服务允许您修改文件夹和文件。
然而，粗心的修改或删除文件可能会导致严重的问题，如启动失败、故障或数据丢失。
除非您完全理解其机制或在合格专家的指导下工作，否则不要修改这些文件。
{% endhint %}

您可以使用 HRWorkbench、文件管理器或备份功能备份和恢复项目文件夹中的配置和教学文件。

但是，在某些情况下，使用熟悉的 FTP 软件将文件备份到 PC 或将其恢复到机器人控制器可能更方便。
本节描述了在这样做时需要注意的重要预防措施。
(项目文件夹中每个文件的详细信息将在下一节中解释。)


#### 在修改 project/jobs/ 文件夹中的 .job 文件后应用更改

当您使用 FTP 软件在 `project/jobs/` 文件夹中添加或覆盖 .job 文件时，机器人控制器不会立即在内存中反映这些更改。
(使用 HRWorkbench 或文件管理器时，更改会立即被检测并自动加载到内存中。)

有两种方法可以将更新的文件应用到内存中：

- 在 HOME 屏幕上，单击控制台栏中的 ` (...)` 按钮，然后选择 `重新加载更新的Job (reload updated jobs)`。

  ![](../../_assets/tp630/etc/console_reload_job.png)

- 重启机器人控制器。


#### 在修改 project/vars/ 文件夹中的 .json 和 .csv 文件后应用更改

当您使用 FTP 软件在 `project/vars/` 文件夹中添加或覆盖全局变量文件时，机器人控制器不会立即在内存中反映这些更改。
(使用 HRWorkbench 或文件管理器时，更改会立即被检测并自动加载到内存中。)

要将更新的文件应用到内存中，请使用以下方法：

- 打开全局变量监控窗口，然后单击底部的 `Load All` (F-button)。

![](../../_assets/tp630/etc/gvar_load.png)

{% hint style="warning" %}
不要重启机器人控制器以应用更新的全局变量文件。
当控制器断电时，内存中当前的全局变量值会保存回文件，这将覆盖您刚刚更新的文件。
{% endhint %}
[__SOURCE](11-etc/1-controller-files/2-project.md)
<script id="page-config" type="application/json">
{
	"permittedStrs": ["Hi7"]
}
</script>

# 11.1.2 项目/

这是存储机器人配置、教学数据和状态最重要的文件夹。
在备份或恢复控制器系统时，此文件夹是核心组成部分。

#### 项目/

此文件夹包含各种配置文件，以及在控制器断电（关机）前立即保存的状态备份文件。
状态备份包括在关机时存储的信息，目的是：

    - 在控制器重新开机时恢复断电前正在运行的任务
      (注意：对于机器人应用或插件等复杂操作，可能无法恢复。)

    - 保存断电前的输出信号，并在通电后恢复它们


* arc_weld.json
  
  弧焊应用配置文件

* arc_weld_bkup.json
  
  在断电前保存的弧焊应用状态备份数据

* calibration.json

  机器人校准配置文件

* context.json

  包含所有任务的 .job 文件的执行上下文，包括指令指针位置、带参数的 .job 文件的调用历史、局部变量值等。

* dout.json

  在断电前保存的一般数字信号的输出状态

* force_control.json

  力控制配置文件

* hi6_proj.json

  主项目文件。大多数基本功能的配置存储在这里。

* kw.json
  
  在断电前保存的内置 PLC `kw` 继电器值

* maintenance.json

  各种维护和系统信息，包括机器人型号、轴数、运行时间、软件版本、剩余内存和存储、系统代码以及每线程执行时间

* motion_bkup.bin
  
  与机器人运动相关的在断电前保存的备份数据

* mw.json
  
  在断电前保存的内置 PLC `mw` 继电器值

* playback_bkup.bin

  与 .job 执行相关的在断电前保存的备份数据

* sealing.json

  密封应用配置文件

* sout.json

  在断电前保存的系统信号输出值

* spot_weld.json

  点焊应用配置文件

* spot_weld_bkup.json

  在断电前保存的点焊应用状态备份数据

* svtool_change.json

  伺服工具更换操作的附加轴配置文件

* version.json

  用于确定软件版本升级后第一次启动时是否需要数据更新的信息（当前版本号）
  

#### 项目/作业/
  
存储教学程序 (.job 文件) 的文件夹。


#### 项目/lads/
  
存储内置 PLC 梯形程序 (.lad 文件) 的文件夹。


#### 项目/安全/
  
(Hi7控制器) 存储功能安全配置文件的文件夹。

* safety_parameter.json

  功能安全配置文件

* safety_parameter.json.cert

  安全配置的认证文件。
  只有在使用正确密码保存配置时，才会发放有效的证书。如果无效，控制器将无法操作。


#### 项目/vars/

存储变量和别名的文件夹。

* aliases.json

  机器人语言别名文件

* *.csv

  顶层数组文件（以逗号分隔的值格式）

* vars.json

  全局变量文件
[__SOURCE](11-etc/1-controller-files/3-log.md)
# 11.1.3 log/


此文件夹存储各种日志文件。在下面的文件名中，? 表示一个数字；当达到最大数字时，文件将以循环方式从 0 开始覆盖，或者它可能表示格式为 YYYYMMDD_HHMMSS 的时间戳。

这些文件中：

事件日志可以在教导挂件日志窗口中查看，也可以通过 HRWorkbench 查看。

范围日志只能通过 HRWorkbench 查看。

其余的 .txt 文件可以使用任何标准文本编辑器打开。


* bootlog_?.txt

  存储控制器启动历史的日志文件。
  用于分析启动失败等问题。每次控制器启动时，会以循环方式创建一个新文件。

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

  存储机器人启动和停止事件的日志文件。

* pow_stage.txt

  存储电源开启、电源故障恢复和电源故障备份状态的文件。

* sclog_base_????????_??????.bin

  存储时间序列数据（如每个轴的位置、速度和加速度）的范围日志文件。  
  ????????_?????? 表示 YYYYMMDD_HHMMSS 格式的时间戳。  
  当检测到机器人震动或发生特定错误时生成。可以使用 HRWorkbench 中的范围日志功能查看。

* sclog_base_????????_??????.json

  描述对应 .bin 文件中存储的数据类型的模式文件。
  .bin 和 .json 文件必须成对存在才能打开日志。

* shutdownlog_?.txt

  存储控制器关机历史的日志文件。  
  用于分析电源故障备份操作是否正确执行。每次控制器关机时，会以循环方式创建一个新文件。

* updatesvclog_?.txt

  存储控制器软件版本升级历史的日志文件。
  用于分析版本升级是否成功。
[__SOURCE](11-etc/1-controller-files/4-backup.md)
# 11.1.4 backup/

此文件夹存储控制器的MAIN侧备份。  
文件夹名称以格式`bYYYYMMDD_HHMM`生成，包含子文件夹：project/, log/, cifX/, EC_LOG/, 和 EDR_LOG/。


#### backup/ev/

存储事件备份的文件夹。  
当发生特定错误时，备份会自动创建。


#### backup/ts/

存储定期备份的文件夹。  
备份会在预定时间自动创建。
[__SOURCE](11-etc/1-controller-files/5-etc.md)
# 11.1.5 其他文件夹

#### apps/

存放在 MAIN 端执行的插件应用的文件夹。


#### fbrr/

基于文件的机器人注册表文件夹。  
存储每个机器人机制模型的信息文件 (.fbr)。  
当添加新的模型信息文件时，可以在系统初始化期间通过选择模型来配置机器人系统。


#### gather/

存储时间序列数据收集功能的结果文件 (.GDT) 的文件夹。


#### help/

存储机器人语言 HRScript 的 HTML 帮助文件的文件夹。


#### roblang/

存放机器人语言 HRScript 的语法文件的文件夹。

* procs_?.json
  
  按类别的过程语法文件

* funcs_?.json

  按类别的函数语法文件

* svars_?.json
  
  按类别的系统变量语法文件
[__SOURCE](11-etc/2-keypad-mode.md)
# 11.2 数字键盘模式

此功能允许触摸屏上的 L、R 和 F（功能）按钮使用数字键盘操作。如果触摸屏 `故障` 或通过 `[F1: 服务] - 11: 示教器选项 ([F1: service] - 11: Teach pendant option)` `关闭`，您可以使用此功能操作按钮。

当数字键盘模式激活时，每个按钮对应的控制键将在按钮的顶部或底部显示。

### L, R 按钮条数字键盘模式
- 快捷键: `[CTRL]+[.]`
    - L 按钮条
        - `[R..]` : `[rec.cond]`
        - `[7]` : `[run to]`
        - `[4]` : `[jog inch.]`
        - `[1]` : `[property]]`
        - `[0]` : `[help]`
    - R 按钮条
        - `[ENTER]` : `[man.out]`
        - `[9]` : `[pane layout]`
        - `[6]` : `[soft kb.]`
        - `[3]` : `[user key]`
        - `[BS]` : `[prev/next]`

![](../_assets/tp630/keypad-mode-LR_eng.png)

### F 按钮条数字键盘模式
- 快捷键: `[CTRL]+[←(Backspace)]`
    - F 按钮条（映射到对应于数字键的 F 按钮）
        - 以下描述基于在最高级别屏幕上显示的按钮。
        - `[1]` : `[F1: 服务] ([F1: service])`
        - `[2]` : `[F2: 系统] ([F2: system])`
        - `[3]` : `[F3: 释放WAIT] ([F3: rel.WAIT])`
        - `[4]` : `[F4: 故障记录] ([F4: log])`
        - `[6]` : `[F6: 指令输入] ([F6: cmd.input])`
        - `[7]` : `[F7: 条件设置] ([F7: cond.set])`

![](../_assets/tp630/keypad-mode-F_eng.png)
[__SOURCE](appendices/README.md)
# 附录
[__SOURCE](appendices/rules-occupational-safety.md)
# 职业安全与健康标准法规及安全检查通知

工业机器人应根据《职业安全与健康标准法规》和《安全检查通知》的检查标准进行安装（如需检查）。

"[职业安全与健康标准法规](https://hrbook-hrc.web.app/#/view/rules-on-occupational-safety-and-health-standards/zh/README)"
[__SOURCE](quality-assurance.md)
# 质量保证

"[质量保证](https://hrbook-hrc.web.app/#/view/quality-assurance/zh/README)"