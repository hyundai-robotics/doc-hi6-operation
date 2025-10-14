# 7.3.3 Serial Port

You can set the information required for serial port communication.

1.	Touch the \[2: Control Parameter &gt; 3: Serial port\] menu.

2.	Set the parameters for each serial port.

    ![](../../_assets/tp630/ctrl-serial.png)



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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">Detailed information on the port selected from the serial port list. You
        can set the port name and parameter values.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><strong>Serial Port List</strong>: Select a port name to view and edit its detailed information.</li><li><strong>[OK]</strong>: Saves the changes.</li>
          <li><strong>[+]/[-]</strong>: Adds a new serial port or deletes an existing one.</li>
        </ul>
      </td>
    </tr>
        <tr>
      <td style="text-align:left">
        <img src="../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          Performs a loopback test. Connect the RX and TX pins of the serial port to check whether communication is functioning properly.
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
Refer to the following information when setting the usage of the serial port.

* Sensor: For receiving the shift data by accessing the vision sensor
* LVS: For connecting with the laser vision sensor for the weld line follow-up
* MODBUS: The MODBUS slave function of the Hi6 controller
{% endhint %}



