# 7.3.10 Network Setting

You can set the information required for Network Setting for LAN ports.

1.	Touch the \[2: Control Parameter &gt; 9: Network &gt; 1: Environment setting \] menu.

2.	Set the parameters for each LAN(Public) port. Class C type IP Addressing supported.

3.	Public LAN ports can do portforwarding.

4.	Setting parameters will be adjusted when you reboot the system.

![](../../_assets/image_551.png)

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
      <td style="text-align:left">LAN Port Selection Tab. You can modify Public LAN Port. LAN1(Ethercat), LAN2(T/P-Main) are forbidden to change.
	  </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <br />Changing port setting. IP Address, Subnet Mask, Gateway can be modified.
          <li><b>IP Address : </b> You can set IP Address for the target port.</li>
          <li><b>Subnet Mask : </b> Subnet Mask setting for the target port. Usually subnet mask is 255.255.255.0</li>
          <li><b>Gateway : </b>You can set gateway address for the target port. 3rd  information and paste it to another port.
          </li>
        </ul>
      </td>
    </tr>
	<tr>
      <td style="text-align:left">
        <img src="../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>PortForwarding selection : </b> You can turn on portforwarding mode. portforwarding mode check box is only in LAN3 tab section. LAN1 does not support portforwarding.</li>
        </ul>
      </td>
    </tr>
	<tr>
      <td style="text-align:left">
        <img src="../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[OK]</b>: You can save the changes. After reboot the system all changes are adjusted.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}

Portforwarding means that redirect to other IP address of port through router. Hi6 controller has portforwarding function.

Ex) Device1(192.168.1.10 | 255.255.255.0 | 192.168.1.1) can connected to T/P(192.168.2.X | 255.255.255.0 | 192.168.2.X)

Refer to the following information when setting the usage of the Portforwarding.

* Supported IP : Class C type(192.168.XX.XX) devices can use portforwarding.
* Supported Subnet : Each port basically setted 3rd steps. For example LAN3(Public) can connected 192.168.1.X IP
* Basic Gateway: 192.168.X.1 is initial condition gateway.

{% endhint %}
