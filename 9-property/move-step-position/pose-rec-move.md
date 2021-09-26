# 9.2.2 Pose Recording Move Statement and Pose Assign Statement

You can edit the pose variable value in the move statement, including the pose variable or the pose variable assign statement.

1.	Touch the \[property\] button in the move command \(move statement\) recorded as a pose variable. Then, the pose variable setting screen will appear.

2.	Check and modify the current pose variable.

![](../../.gitbook/assets/image%20%28547%29.png)





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
        <img src="../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Current pose variable information. You can check and set the name, coordinate
          value, coordinate system format, etc.</p>
        <ul>
          <li>[Name]: Name of the current pose variable</li>
          <li>Coordinate value: The coordinate value of the current pose variable
            <ul>
              <li>Select an item using the cursor key.</li>
              <li>After inputting a value in the desired item, press the <b>&lt;enter&gt;</b> key
                to reflect the change.</li>
              <li>If the coordinate system format is set as an encoder, the coordinate value
                will not be changed.</li>
            </ul>
          </li>
          <li>[Coord. System]: The coordinate system format to express the position
            of the current pose variable</li>
          <li>[Configuration]: When describing the position of the robot, there are
            multiple solutions because of the characteristics of the device, so the
            robot configuration is designated to uniquely describe the configuration.
            <ul>
              <li>This function can only be used when the coordinate system type is set
                as a base or robot.</li>
              <li>For details on the robot configuration, refer to &#x201C;<a href="../../2-operation/2-3-step/step-pose-modify/">2.3.2 Recording and Changing a Step Position</a><b>.</b>&#x201D;</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: You can save the changes.</li>
          <li>[Previous]/[Next]: You can display the information of the previous or
            next step.</li>
          <li>[Original Value]: You can display the original hidden pose value of the
            current step.</li>
          <li>[Current Robot Pose]: You can display the value of the pose the robot
            is currently taking.</li>
          <li>[Moving]: Touching the <b>[Moving]</b> button will move the robot to the
            recorded step position (Jog).</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

3.	Touch the \[Record\] button. Then, the change will be saved in the job program, and the operation will end.

* If you end the operation by pressing the &lt;esc&gt; key, the change will not be saved. 





