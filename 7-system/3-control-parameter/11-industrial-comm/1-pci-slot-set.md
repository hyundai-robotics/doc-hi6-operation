# 7.3.11.1 PCI 插槽设置

您可以设置用于工业通信的 PCI 插槽。

1. 触摸 `[2: Control Parameter - 11: 工业通信 - 1: PCI 插槽设置 - 1 Channel] ([2: Control Parameter  - 11: Industrial Communication  - 1: PCI Slot Settings  - 1 Channel])` 菜单。然后，PCI 插槽设置屏幕将显示。

2. 选择所需的标签，然后设置通信方式 \(Master / Slave\) 和协议。之后，点击 `[OK]` 按钮。

    ![](../../../_assets/tp630/ctrl-industrial-channel_eng.png)

{% hint style="warning" %}
完成 PCI 插槽设置后，插槽 \#1 - \#4 中设置的 CONFIG 文件将全部删除。当您想要在使用过程中更改通信 PCI 插槽时，应该单独备份现有的 CONFIG 设置，并在恢复后使用它。
{% endhint %}

3. 关闭控制器的电源，然后重新打开它。

{% hint style="warning" %}
* 当您执行 PCI 插槽的设置以使用时，设置值将在您关闭控制器电源后重新打开时应用到系统。
{% endhint %}