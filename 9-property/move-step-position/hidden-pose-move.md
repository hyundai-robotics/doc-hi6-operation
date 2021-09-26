# 9.2.1 Hidden Pose Move Statement

You can check or modify the position of the current step in the hidden pose move statement \(step recorded using the \[Record\] button, that is, a move statement that does not include a pose variable\).

1.	Touch the \[property\] button in the move command \(move statement\) recorded as a hidden pose. Then, the current step position will appear. 

2.	Check and modify the current step position.

![](../../.gitbook/assets/image%20%28544%29.png)



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
        <p>Position information of the current step. You can check and set the name,
          coordinate value and coordinate system format, etc.</p>
        <ul>
          <li>[Name]: Number of the current step. After inputting the step number, press
            the <b>&lt;enter&gt; </b>key to move to the concerned step.</li>
          <li>Coordinate Value: Current coordinate value of the current step
            <ul>
              <li>Select an item using the cursor key.</li>
              <li>After inputting a value in the desired item, press the &lt;enter&gt; key
                to reflect the change.</li>
              <li>If the coordinate system format is set as an encoder, the coordinate value
                will not be changed.</li>
            </ul>
          </li>
          <li>[Coord. System]: The coordinate system format to express the position
            of the current step</li>
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
          <li>[Current Robot Pose]: You can display the value of the posture the robot
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

{% hint style="info" %}
* If \[Robot Configuration\] is set as undesignated, the robot will designate a configuration the very closest to the current position of the robot.
* 
  For the designation according to the robot configuration, refer to “[2.3.2.2 Base and Robot Recording Coordinates](../../2-operation/2-3-step/step-pose-modify/base-robot-crd-sys.md).”
{% endhint %}

