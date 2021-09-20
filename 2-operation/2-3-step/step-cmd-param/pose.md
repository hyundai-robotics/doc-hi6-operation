# 2.3.1.2 Pose

A pose is a parameter to record the position. If you input a move, the movement command, by using the \[Command\] button, you should designate the pose expression in the tg \(target\) parameter. When the move statement is inputted using the \[Record\] button, the tg parameter will not appear. At the moment of touching the \[Record\] button, the position and posture of the manipulator will be recorded, but they will not be displayed on the JOB editing screen, which is why they are called a hidden pose.

The method to input a pose using the menu button on the right side of the Hi6 teach pendant screen is as follows.

* After touching the \[Command\] button, select \[Motion\] and then input the statement.

![](../../../.gitbook/assets/image%20%28306%29.png)

* After touching the \[property\] button, set the attributes of the current robot pose and then touch the \[Apply\] button.

![](../../../.gitbook/assets/image%20%28326%29.png)

The pose variable and shift variable will be saved in the following formats.

<table>
  <thead>
    <tr>
      <th style="text-align:center">Pose Variable</th>
      <th style="text-align:center">Shift Variable</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center">(X, Y, Z, Rx, Ry, Rz, {Coordinate system}, {config.})</td>
      <td style="text-align:center">(X, Y, Z, Rx, Ry, Rz, {Coordinate system})</td>
    </tr>
    <tr>
      <td style="text-align:center">
        <p>{Coordinate system}:</p>
        <p>&quot;base&quot; = Base coordinate system
          <br />&quot;robot&quot; = Robot coordinate system
          <br />&quot;user{n}&quot; = User coordinate system (n refers to a number)
          <br
          />&quot;joint&quot; = Joint coordinate system
          <br />&quot;encoder&quot;= Encoder</p>
      </td>
      <td style="text-align:center">
        <p>{Coordinate system}:</p>
        <p>&quot;base&quot; = Base coordinate system
          <br />&quot;robot&quot; = Robot coordinate system
          <br />&quot;user{n}&quot; = User coordinate system (n refers to a number)
          <br
          />&quot;joint&quot; = Joint coordinate system</p>
      </td>
    </tr>
  </tbody>
</table>



