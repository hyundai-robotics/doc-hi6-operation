# 9.1 Use of the property Function

If you use the \[property\] button on the right side of the Hi6 teach pendant screen, you can quickly and easily set the conditions and check the position simply by a single button operation.

![Figure 75 Function for the \[Attributes\] Button](../_assets/image_540.png)

For example, if you touch the \[property\] button while the cursor is on the arcon statement that is for the Arc On function, the contents of the condition number used in the current statement among the welding start conditions will be displayed. On the screen, you can check or change the details of the welding start conditions. Moreover, if there is another condition file associated with the concerned condition file, you can move directly to it. In other words, the \[property\] button allows you to check and change the details of the contents related to a specific statement such as condition file or step position quickly and easily. 



The following shows the method to check and change the condition file and details related to a specific command using the \[property\] button.

1.	Select a specific statement, place the cursor on it, and touch the \[property\] button.

2.	By referring to the following table, you can check and change the file or details related to the selected statement.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Statement</th>
      <th style="text-align:left">File and Contents</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>move</p>
        <p></p>
        <p>refp</p>
        <p></p>
      </td>
      <td style="text-align:left">
        <p>Step position</p>
        <p></p>
        <p>Reference position</p>
      </td>
      <td style="text-align:left">
        <p>Current step position or global pose variable</p>
        <p>X Y Z (mm) Rx Ry Rz (deg) T1&#x2013;T10</p>
        <p>The unit, coordinate system, and robot configuration</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">arcon asf=</td>
      <td style="text-align:left">
        <p>Welding start condition</p>
        <p>Welding auxiliary condition</p>
        <p>Arc welder condition</p>
      </td>
      <td style="text-align:left">
        <ul>
          <li>Welding start condition: Condition number, description, voltage check,
            retry, operation mode, output current, output voltage, WCR waiting time,
            robot delay time, etc.</li>
          <li>Welding auxiliary condition
            <ul>
              <li>Retry: Count, retract time/speed, back step/welding line movement amount,
                shift movement amount, speed, current, voltage</li>
              <li>Restart: Count, overlap amount, moving speed, welding current, voltage,
                current</li>
              <li>Overlap condition setting (in the middle of welding): Arc, gas, wire,
                and coolant</li>
            </ul>
          </li>
          <li>Arc welder condition: Welder number, title, description, power control
            mode, wire diameter, protruding distance, deposition detection time, ARC
            OFF detection time, etc.
            <ul>
              <li>Current properties: Polarity, command value (V), measurement value (A),
                and compensation value</li>
              <li>Voltage properties: Polarity, command value (V), measurement value (V),
                and compensation value</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">arcon aef=</td>
      <td style="text-align:left">
        <p>Welding end condition</p>
        <p>Welding auxiliary condition</p>
      </td>
      <td style="text-align:left">
        <ul>
          <li>Welding end condition: Condition number, description, voltage check, output
            current, output voltage, downslope, condition holding time, and gas postflow</li>
          <li>Welding auxiliary condition: Automatic deposition release: Count, current,
            voltage, delay time</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">weavon wev=</td>
      <td style="text-align:left">Weaving condition</td>
      <td style="text-align:left">
        <ul>
          <li>Weaving condition: Gun number, weaving type, frequency, basic pattern,
            progress angle, boundary limit, moving time, and timer</li>
          <li>Arc sensing condition: Arc sensing, left and right sensing start cycle,
            top and bottom sensing cycle, voltage factor, compensation distance per
            sample, etc.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

3.	Touch the \[Record\] button or press the &lt;esc&gt; key to end the operation.

* \[Record\]: You can save the changes and end the operation.
* &lt;esc&gt;: You can cancel the change and end the operation.





