# 7.4.8.1 Collision Detection Sensitivity Setting

The collision detection sensitivity can be adjusted using the command in the JOB program.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Item</th>
      <th style="text-align:left">Contents</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Command</td>
      <td style="text-align:left">ColDet Sensitivity</td>
    </tr>
    <tr>
      <td style="text-align:left">Description</td>
      <td style="text-align:left">Changing the collision detection sensitivity</td>
    </tr>
    <tr>
      <td style="text-align:left">How to input</td>
      <td style="text-align:left">command &#x2192; MOTION &#x2192; colsense</td>
    </tr>
    <tr>
      <td style="text-align:left">Syntax</td>
      <td style="text-align:left">ColDet Sensitivity=100</td>
    </tr>
    <tr>
      <td style="text-align:left">Parameter</td>
      <td style="text-align:left">0&#x2013;200 (0: Function disabled. The larger the sensitivity value,
        the more sensitive it is to impact.)</td>
    </tr>
    <tr>
      <td style="text-align:left">Example</td>
      <td style="text-align:left">
        <p>[Impact Detection] When the sensitivity is set to 100% in the menu</p>
        <p>S1 - S2: Detection based on the sensitivity of 100% S3&#x2013;S4: Detection
          based on a sensitivity of 50%</p>
        <p>
          <img src="../../../.gitbook/assets/coldet-sensitivity.png" alt/>
        </p>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
If the sensitivity is set too high, false detection may occur. Moreover, if the sensitivity is set too low, collisions detection may not be performed.
{% endhint %}

{% hint style="info" %}
* If there is no command, collision will be detected based on the basic sensitivity set in the \[Impact Detection\] menu.
* The sensitivity set by the command will be initialized to the basic sensitivity in the following cases.
  * When encountering the END command of the main program
  * When changing the step/function
  * When resetting the step counter
{% endhint %}

