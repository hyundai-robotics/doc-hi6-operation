# 6.7 Public Output

Touch \[public Output\] in the panel selection window. Then, the public output signal window will appear. 

You can check the status of public output signals that are outputted through the CNOUT connector of the I/O board in the controller.

![Figure 40 Public Output Signal &#x2013; ON/OFF Status \(Left\) / Value Status \(Right\)](../_assets/image%20%28444%29.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">No.</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Displays the status of general output signals</p>
        <ul>
          <li>General output signals designated as the system&#x2019;s basic specifications
            or assigned by the user will be displayed <b>in bold</b>.</li>
          <li>The signals currently being outputted will be displayed in yellow.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[FB0]: You can select the FB block to monitor by touching the drop-down
            menu (FB0 - FB15). You can configure up to 16 I/O blocks, and 960 points
            of signals can be monitored using one block.</li>
          <li>[Manual Output]: You can force the selected signal to be outputted.</li>
          <li><b>[ATTR.-APPLIED]</b>: You can check the checkbox to perform the setting
            in a way that the physical input values are to be displayed before passing
            through the positive/negative logic attributes. The basic setting (unchecked)
            is that the input logic value after passing through the positive/negative
            logic attributes will be displayed.</li>
          <li>[ON/OFF]/[Value]: You can change the signal display mode by touching the
            radio button.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* In the case of using signals, such as fieldbus signals, by mapping them using an embedded PLC, the On/Off status of the output signals may appear differently. 
* 
  The flow of the output signals is as follows.
{% endhint %}

![](../_assets/image%20%28409%29.png)

#### 

#### Manual Output

You can select the desired signal and force it to be outputted.

1.	You can set the display mode to the ON/OFF status by touching the \[ON/OFF\] radio button on the right side of the general output signal window. 

2.	Touch a signal to select it in the signal window, and then touch the \[Manual Output\] button.

![](../_assets/image%20%28437%29.png)


3.	After checking the output conditions in the manual output confirmation window, touch the \[ENTER\] button.
_assets
![](../_assets/image%20%28463%29.png)

| FbN | doN | =1/0 |
| :---: | :---: | :---: |
| N: Number of the FB block to monitor | N: Number of the signal to output | Output status \(1: Output, 0: No output\) |

4.	Check the output status of the selected signal. The selected signal will be switched to the output status and displayed in yellow in the signal window.
_assets
![](../_assets/image%20%28426%29.png)

