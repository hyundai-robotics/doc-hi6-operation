# 7.5.16.2 Jogging(open-api)

请参阅关于open-api通信的单独手册。 <br>
有关机器人操纵的url地址和请求体的信息如下。

* url : POST /project/robot/joystick/joy
* body <br>
    axis : 由双精度类型数组组成。 axis[0] 对应于 J1。 值为 -1 表示向左移动，值为 +1 表示向右移动。 <br>


{% hint style="info" %}
如果在300ms内未收到数据，操纵运动将停止。  
{% endhint %}