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