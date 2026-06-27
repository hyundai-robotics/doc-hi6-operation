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