# 7.4.9.2 微调操作

微调功能是一种功能，它不允许运动超过每次按下微调键的最大移动距离。

即使达到微调距离，如果您继续按住微调键然后松手，机器人将减速至微调距离，然后停止。

![Figure 63 When Releasing the Key After Reaching the Inching Distance](../../../_assets/image_488.png)

如果您在达到微调距离之前释放微调键，机器人将从您释放微调键的时刻开始减速，然后停止。此时，模式将与普通微调模式相同。

![Figure 64 When Releasing the Hand Before Reaching the Inching Distance](../../../_assets/image_473.png)

{% hint style="info" %}
在关节坐标系中，速度等级1固定为机器人将按编码器的1位移动的模式。
{% endhint %}