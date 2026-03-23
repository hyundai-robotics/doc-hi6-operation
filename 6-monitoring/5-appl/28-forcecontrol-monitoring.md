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