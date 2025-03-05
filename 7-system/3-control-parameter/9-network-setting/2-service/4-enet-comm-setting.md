# 7.3.9.2.4 Ethernet communication setting
 
Before performing ethernet communication, you must first create and configure an Ethernet communication object.<br>
Up to five Ethernet objects can be created and used, and the current communication status can also be monitored. <br>

Currently used to perform Modbus master operations in HRScript. For more information on Modbus communication functions, please refer to the separate [Hi6 Robot Controller Function Manual - Modbus](https://hrbook-hrc.web.app/#/view/doc-modbus/english/README).

![](../../../../_assets/tp630/image32.png)

You can force close the socket of the corresponding Ethernet object with the [Close] button, and perform a communication connection with the [Connect] button. <br>
When the controller boots, it automatically establishes a communication connection with the configured Ethernet object. <br>


*   **Name**

    The name of the Ethernet communication object. Each name must be set to "enet0" ~ "enet4".


*   **Protocol**

    Select the communication protocol. 


*   **IP address**

    Sets the IP address used for communication. 


*   **Local port**

    Sets the local port number. 


*   **Remote port**

    Sets the remote port number. 


*   **State**

    Displays the status of the communication connection. 
