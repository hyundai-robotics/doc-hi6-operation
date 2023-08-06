# 6.3.8 Program reservation execution

For this monitoring, pre-setting is required. You have to select the register number as 20EA or 1EA in the page of [system > 2:Control parameter > 7:Program reservation execution]'.

![](../_assets/tp630/ctrl-prog-reserve_eng.png)

In the panel selection window, touch \[program reserve\]. Then, the scheduled program execution window will appear. 

When programs are scheduled through external signals and executed in the scheduled order, you can check and change the status in the list of scheduled programs.

![Figure 50 Program reserve](../_assets/tp630/pane-prog-reserv_eng.png)

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
        <img src="../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>A list of scheduled programs. You can schedule 1&#x2013;20 programs.</p>
        <ul>
          <li>When a program being executed in remote mode is terminated, programs will
            be automatically executed according to the scheduled order.</li>
          <li>When the execution of scheduled programs is completed, those programs
            will be deleted from the list.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[Edit]</b>: You can edit the list of scheduled programs.</li>
          <li><b>[Insert]</b>: You can add a program that will be executed on a schedule
            to the list of scheduled programs.</li>
          <li><b>[Delete]</b>: You can delete a scheduled program from the list of scheduled
            programs.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>



{% hint style="info" %}
* The \[Program reserve\] item will be activated only when the sync status of the sensor sync function among the application functions is set as conveyor or press.
* The \[Program reserve\] item will not be activated if the \[Applied Register Count\] option in the \[system &gt; 2: Control Parameter &gt; 8: Program reserve\] menu is set as disable.
* For details on the scheduled program execution, refer to the “Hi6 Controller Scheduled Program Execution Function Manual.”
{% endhint %}

