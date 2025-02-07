# 7.5.16.2 Jogging(open-api)

Please refer to the separate manual for open-api communication. <br>
Information about the url address and body used for robot jogging is as follows.

* url : POST /project/robot/joystick/joy
* body <br>
    axis : Composed of double type array. axis[0] corresponds to J1. A value of -1 means movement to the left, and a value of +1 means movement to the right. <br>


{% hint style="info" %}
If no data is received for 300ms, the jogging motion will stop.  
{% endhint %}
