# 7.3.9.1 Environment setting

You can set the information required for Network Setting for LAN ports.

1.	Touch the \[ System &gt; 2: Control Parameter &gt; 9: Network &gt; 1: Environment setting \] menu.

2.	Set the parameters for each LAN(Public) port. Class C type IP Addressing supported.

3.	Setting parameters will be adjusted when you reboot the system.

<img src ="../../../_assets/image_551.png">

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">In the LAN Port Selection tab, only the Public LAN Port can be modified. EtherCAT and T/P-Main ports are fixed and cannot be changed.
	  </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          Changing port setting. IP Address, Subnet Mask, Gateway can be modified.
          <li><b>IP Address : </b> You can set IP Address for the target port.</li>
          <li><b>Subnet Mask : </b> Subnet Mask setting for the target port. Usually subnet mask is 255.255.255.0</li>
          <li><b>Gateway : </b>You can set gateway address for the target port. 3rd  information and paste it to another port.
          </li>
          <li><b>MAC : </b>Displays the controller's MAC address.
          </li>
        </ul>
      </td>
    </tr>
	<tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[OK]</b>: You can save the changes. After reboot the system all changes are adjusted.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
