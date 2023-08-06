# 6.2.6 Forced IO

You can register IO relay variables in the Force IO panel to force some changed IO values.

{% hint style="warning" %}
* This function is only for testing or problem analysis.
* Misoperation of forced IO function can cause serious accidents such as collisions, drops, and casualties. Use with caution only if you fully understand the system's IO connections and clearly predict the consequences of the forced value change.
* After testing and problem analysis, be sure to clear the forced IO completely and restore it to a normal IO state.

{% endhint %}

## Opening forced IO panel

1. Split the screen and press the [Select] button on the bottom left.

![](../../_assets/tp630/panel-split.png)
&nbsp;
![](../../_assets/tp630/panel-sel.png)

2. Double-click `forced io` in the panel selection window. Forced I/O panel opens.

![](../../_assets/tp630/panel-forced-io/panel-forced-io.png)

![](../../_assets/tp630/panel-forced-io/panel-forced-io-mon.png)


## How to use

Select the `Name` column, type the desired IO Relay variable name, and press the `ENTER` key to register the variable in the table.  
(You can modify the variable name you entered by clicking the Name column once more.)

![](../../_assets/tp630/panel-forced-io/panel-forced-io-name.png)

Select the `Value` column, type the new IO value you want to apply, and press the `ENTER` key.

![](../../_assets/tp630/panel-forced-io/panel-forced-io-val.png)

If you have more forced IO entries to apply, enter them in the same way. You can enter up to 100 entries.

![](../../_assets/tp630/panel-forced-io/panel-forced-io-multi.png)

The * mark on the panel title bar means that the table has been modified and this modification has not yet been applied.
Press the [F7: Apply] button to apply the forced IO.
The moment you press the `OK` button in the warning message box, all forced I/O entries are applied.

![](../../_assets/tp630/panel-forced-io/panel-forced-io-apply.png)

The * mark on the panel title bar disappears, and you can see that the forced IO value is applied.
A red F mark flashes on the title bar. It is a warning that forced IO is being applied.

![](../../_assets/tp630/panel-forced-io/panel-forced-io-result.png)


* Press `SHIFT+DEL` to delete an item during editing.
* You can change the order of the items by pressing the [F5: Swap Up], [F6: Swap Down] buttons.
* If you click [F3: Cancel edit] while editing a table, it will reload the last applied state.

After completing the test and problem analysis, be sure to press the [F2: Clear] button to fully clear the forced IO.

![](../../_assets/tp630/panel-forced-io/panel-forced-io-clear.png)

{% hint style="warning" %}
* If multiple entries force conflicting values for the same relay (or overlaid bits), they are forced to the value of the lower item of the table.
* When the Hi6 controller is powered off, all contents registered as forced IO are cleared.

{% endhint %}
