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