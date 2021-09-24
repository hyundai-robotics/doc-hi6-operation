# 7.3.2.9 DIO Block Allocation

You can set the method of using the controller’s general input/output signals. This function can be used through connection to None, PLC, or Fieldbus item.

1.	Touch the \[2: Control Parameter &gt; 2: Input/Output Signal Setting &gt; 6: DIO Block Allocation\] menu.

2.	Set the connection with the DIO block of the selected FB address, and then touch the \[OK\] button.

![](../../../.gitbook/assets/image%20%28434%29.png)



* \[None\]: The DIO block of the selected FB address will not be assigned. If nothing is selected as the initial setting value of the controller, the None item will be set.
* 
  \[PLC\]: The DIO block of the selected FB address will be connected to PLC for the use. For the PLC operation, MULTPROG program will be used.

* \[Fieldbus\]: The DIO block of the selected FB address will be connected to the PCI communication board \(Fieldbus\) for the use. If the DIO block is connected to the PCI communication card, the PCI board selection window will be activated.



{% hint style="info" %}
When using \[PLC\] and \[Fieldbus\] at the same time, please be careful not to overlap the slot number of the multiprog program and \[Fieldbus\].
{% endhint %}



