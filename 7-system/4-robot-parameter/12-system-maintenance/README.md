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