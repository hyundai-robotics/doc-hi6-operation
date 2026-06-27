# 7.5.16.2 Jogging(open-api)

请参阅单独的手册以获取 open-api 通信信息。 <br>
机器人驳接的 url 地址和使用的 body 信息如下。

* url : POST /project/robot/joystick/joy
* body <br>
    axis : 由 double 类型数组组成。 axis[0] 对应于 J1。值为 -1 表示向左移动，值为 +1 表示向右移动。 <br>


{% hint style="info" %}
如果在 300ms 内未收到数据，驳接动作将停止。  
{% endhint %}