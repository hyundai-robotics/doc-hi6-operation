# 7.3.9.2.4 Ethernet Communication Settings

Before performing Ethernet communication, you must first create and configure an Ethernet communication object.  
Up to eight Ethernet objects can be created and used, and the current communication status can be monitored in real-time.  

Currently, it is used to perform communication independently through HRScript or settings. 

![](../../../../_assets/tp630/image32.png)

You can forcibly close the socket of the corresponding Ethernet object using the [Close] button, or establish a communication connection using the [Connect] button.  
When the controller boots, it automatically attempts to establish a communication connection using the configured Ethernet objects.  

* **Name** 

    The name of the Ethernet communication object. Each name must be set between "enet0" and "enet7".

* **Protocol** 

    Select the communication protocol. (UDP, TCP client, TCP server)

* **IP Address** 

    Set the IP address of the target device.

* **Local Port** 

    Set the local port number.

* **Remote Port** 

    Set the remote port number.

* **Status** 

    Displays the current communication connection status. 
   