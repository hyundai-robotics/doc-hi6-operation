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