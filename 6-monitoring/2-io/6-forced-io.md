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