# 1.2.4.4 Menu Buttons



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
        <img src="../../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Mechanism: You can check and set the selected mechanism.</p>
        <p>Touch the <b>[Mechanism] </b>button repeatedly until the desired mechanism
          group appears. If the robot model is not selected during the initial setting
          process, the mechanism group will not be displayed, but only the <b>Not Initialized</b> mark
          will be displayed.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Coordinate System: You can check and set the reference coordinate system
          for the jog execution.</p>
        <p>Touch the <b>[Crd. Sys]</b> button repeatedly until the desired coordinate
          system mode appears. The name of the axis newly selected according to the
          selected reference coordinate system will be displayed on the jog bar on
          the right side of the screen.</p>
        <p></p>
        <ul>
          <li>Joint Coordinate System: The name of each joint will be displayed on the
            jog bar. If you touch the [-/+] button on the right side of the joint name,
            you can move the corresponding joint.</li>
          <li>Robot Coordinate System: X, Y, Z, RX, RY, RZ, and additional axes will
            be displayed on the jog bar. Based on the robot coordinate system, the
            tooltip (TCP, Tool Center Point) of the robot can be moved or rotated.</li>
          <li>User Coordinate System: X, Y, Z, RX, RY, RZ, and additional axes will
            be displayed on the jog bar. The tooltip of the robot can be moved and
            rotated based on the user coordinate system.</li>
          <li>Tool Coordinate System: X, Y, Z, RX, RY, RZ, and additional axes will
            be displayed on the jog bar. The tooltip of the robot can be moved and
            rotated based on the tool coordinate system.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>Record: You can input the move statement in the JOB program.</p>
        <p>Touch the [Record] button. Then, the move statement will be inputted right
          below the current cursor position.</p>
        <ul>
          <li>The current posture of the robot will be recorded as the target pose,
            and when it comes to the interpolation, moving speed and unit, accuracy,
            and tool number in the move statement, the values set using the <b>[Recording Condition]</b> button
            will be applied.</li>
          <li>The target pose and the values of the recording condition of the move
            statement can be edited later.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">(In combination with the <b>&lt;shift&gt;</b> key) Position Correction:
        Apply the robot&#x2019;s current posture as the target pose of the step
        in the JOB program.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>Command Inputting: Input the desired command.</p>
        <p>After touching the <b>[Command]</b> button, touch the command in the command
          inputting window. Then, the statement will be inputted right below the
          current cursor position. For details on inputting the commands, refer to
          &#x201C;<b>3.2.2 Statement Inputting.</b>&#x201D;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">(In combination with the <b>&lt;shift&gt;</b> key)
        <br />Deletion: You can delete the statement in the JOB program.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>Attribute: You can check the attributes of a statement.</p>
        <p>After selecting a statement by touching it, touch the <b>[Attribute</b>]
          button. Then, the attribute window for the statement will appear.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">(In combination with the &lt;shift&gt; key) Block Editing: You can enter
        the block editing mode where you can perform copying, cutting, and pasting
        in the JOB program. For details on block editing, refer to &#x201C;<b>3.2.4.5 Block Editing Mode.</b>&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">[Menu]: You can use the service function menus in the program.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">[Set up]: You can set the user environment using the system menu of the
        program.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Favorites: You can quickly execute predesignated functions using code
        numbers. Touch the <b>[Favorites]</b> button, input the code number, and
        touch the <b>[OK] </b>button. Then, the designated function will be executed.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>User Key: You can use the function assigned, as a button, to the user
          key area when teaching the robot.</p>
        <p>Touch the <b>[User buttons]</b> button. Then, the menu button area will
          be switched to the user key area, so you can use the function preassigned
          as a button. To return to the menu button area, touch the <b>[User buttons]</b> button
          or press the <b>&lt;esc&gt; </b>key.</p>
      </td>
    </tr>
  </tbody>
</table>

