# 6.7 Public Output

Touch \[public Output\] in the panel selection window. Then, the public output signal window will appear. 

You can check the status of public output signals that are outputted through the CNOUT connector of the I/O board in the controller.

![Figure 40 Public Output Signal &#x2013; ON/OFF Status \(Left\) / Value Status \(Right\)](../.gitbook/assets/image%20%28405%29.png)

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
        <img src="../.gitbook/assets/c1.png" alt/>
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
        <img src="../.gitbook/assets/c2.png" alt/>
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

![](../.gitbook/assets/image%20%28401%29.png)

#### 

#### Manual Output

원하는 신호를 선택하여 강제로 출력할 수 있습니다.

1.	범용 출력 신호창 우측의 \[ON/OFF\] 라디오 버튼을 터치하여 표시 방식을 ON/OFF 상태로 설정하십시오.

2.	신호창에서 신호를 터치하여 선택한 후 \[수동 출력\] 버튼을 터치하십시오.

![](../.gitbook/assets/image%20%28157%29.png)



3.	수동 출력 확인창에서 출력 조건을 확인한 후 \[확인\] 버튼을 터치하십시오.

![](../.gitbook/assets/image%20%28147%29.png)

| FbN | doN | =1/0 |
| :---: | :---: | :---: |
| N: 모니터링할 FB 블록의 번호 | N: 출력할 신호의 번호 | 출력 상태\(1: 출력, 0: 미출력\) |

4.	선택한 신호의 출력 상태를 확인하십시오. 선택한 신호가 출력 상태로 전환되어 신호창에 노란색으로 표시됩니다.

![](../.gitbook/assets/image%20%28165%29.png)

