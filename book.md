# Hi6 Robot Controller Operation Manual

{% hint style="warning" %}
The information presented in this manual is the property of Hyundai Robotics.

The manual may neither be copied, in part or in full, nor redistributed without prior written consent from Hyundai Robotics.

It may neither be provided to any third party nor used for any other purposes.



Hyundai Robotics reserves the right to modify this document without prior notification.



**Copyright ⓒ 2020 by Hyundai Robotics**
{% endhint %}
# About the Manual

This manual describes the basics and structure of Hyundai Robotics’ Hi6 controller as well as the common operation of industrial robots. Each chapter describes not only basic operation methods but also the methods to use various application functions.

This manual does not cover detailed application functions, such as direct teaching using a collaborative robot, methods of setting safety functions, spot welding, arc welding, positioner sync function, and sensor sync function. For details on relevant information, refer to the collaborative robot maintenance manual and individual application function manuals.

You must fully understand the contents of the manual before using the product. Moreover, keep the manual nearby so that you can refer to it whenever you need it.

This manual may be provided as reference material for customers who have purchased Hyundai Robotics products or may be used as internal training material.

This manual has been created based on standard specifications, so some contents may differ depending on the model of the product you have purchased. In addition, the contents and specifications of this manual are subject to change without prior notice to improve the performance of the product, and Hyundai Robotics is not responsible for situations that could be caused by inaccuracies or typos in the manual. For detailed information on the revision of the manual, you need to visit our internet website \(www.hyundai-robotics.com\).





# Copyrights

The product, as well as all programs, files, and contents covered in this manual, are protected by copyright laws and confidentiality agreements. Any activities, such as use, copying, disclosure, or distribution to third parties that are not expressly permitted by Hyundai Robotics, are strictly prohibited.

Copyright ⓒ 2021 HYUNDAI ROBOTICS. All rights reserved.



# Notation Convention

In this manual, the following notation conventions and safety instructions are used to help you understand the contents.

## Description of Figures

Figures are used to help you understand how to operate the product and illustrate what you can see on the screen. For the description of figures, numbers will be marked for the relevant parts, and the corresponding contents will be described as follows.

![](../_assets/image_1_en.png)

## GUI \(Graphical User Interface\)

On the GUI, menu names and button names are enclosed in square brackets \(\[ \]\) and displayed in bold. When you need to select multiple menus in order, mark them with the &gt; symbol between the names.

* Menu with a name: Touch the \[Menu\] button on the initial screen in manual or automatic mode.
* Multiple menus: Touch the \[Set Up\] button &gt; \[5: Initialize &gt; 7: Unit Setting\] menu on the initial screen in manual mode.



## Notation Method for Operation Keys

Keys that are to be pressed on the operation part of the teach pendant to operate functions will be enclosed in single arrow brackets \(&lt; &gt;\) and displayed in bold.

* If you press the &lt;Start&gt; key, the automatic operation of the program created in the robot will start.



## Cross Reference 

It provides shortcuts to relevant information within the manual. A cross-reference will be shown in double quotation marks \(??? ???\) in bold as follows.

* For details on how to change the date and time information, refer to ???[4.5 Setting of Date and Time.](../4-service/5-date-time-setting.md)???

## Note

In this section are some helpful tips or additional information that could be useful when you use the product as follows.

{% hint style="info" %}
When the ![](../_assets/eng-mode.png)icon blinks in the status bar, it means that you are in engineer mode.
{% endhint %}
# Safety Cautions

Before using the product, you must read the following safety cautions for proper use, user safety, and prevention of property damage.

### Danger

{% hint style="danger" %}
Imminent danger: Incompliance may cause the death of or serious injuries to the operator.
{% endhint %}

* Read the contents of the product installation in the manual and follow the instructions when installing the robot product and other devices.
* If a fatal error occurs in the software, stop using it immediately, and contact our customer support team.
* If there is a problem with the product, such as failure or damage, stop using it immediately and contact the customer support team for inquiry.



### Warning

{% hint style="warning" %}
Potential danger: Incompliance may cause injuries to the operator or damage to property, such as significant damage to the product.
{% endhint %}



* The safety equipment to be used after being connected to the controller must be connected to the safety contact terminal or to the configurable digital I/O set, which is to be set as the safety I/O, in double signals. When the equipment is connected to common contact terminals or in a single signal, the regulated safety level cannot be satisfied.
* Do not put your fingers or other body parts behind the controller’s inner bracket. There is a risk of electric shock or injury.
* 
  If you are a robot application system manufacturer or a robot user, you should fully understand the contents of the manual and complete the product operation training.

* For the safety of workers and users, you must prepare appropriate safety facilities, such as safety fences, before installing the product.
* Check the specification information and perform fastening by using appropriate fixing screws. Loosened screws may lead to separation of the robot, causing it to fall or suffer damage.
* Be careful not to let conductive foreign substances, such as liquid, dust, or metal powder, enter the connection sections \(power and cables\). Moreover, do not poke the connection parts with a pointed object or apply excessive force to them when connecting them. Corrosion or temporary short-circuiting of the connection terminals may cause the product to explode or suffer a fire.
* Check the wiring information and connect the devices using the appropriate terminals corresponding to the type of individual devices. In particular, if a safety device is connected to a general terminal, the safety function cannot be guaranteed, so you must connect it to the terminal designed for safety devices.
* Never use a damaged cable and do not disconnect the power while the product is in use. It may cause electric shock, fire, failure, or injury.
* 
  If the product is used for a long time, it may generate heat and cause injury, such as burns. If you need to touch the product, turn off the power and leave it for at least one hour to let it cool sufficiently before carrying out works.

* 
  Use the teach pendant while paying attention to the movement of the robot.

* If the teach pendant warns of a fatal error, stop the robot with the emergency stop switch immediately, identify the cause, and resolve the error. If the error cannot be resolved, please contact our customer support team for an inquiry.
* Never install, modify, disassemble, or repair the product without our permission. It may cause a failure or an accident. In addition, we are not responsible for any damage to or breaking of the product if you do not follow the instructions.



### Caution

{% hint style="warning" %}
Low-level danger factor: Incompliance may result in minor injury to the operator or damage to property, such as damage to the product.
{% endhint %}



* Do not install, modify, disassemble, or repair the product arbitrarily as it is prohibited for anyone other than our experts to arbitrarily modify the product or attach parts. If the product fails because of such acts, our free service and warranty service will be forfeited.
* A qualified installer should install the product in compliance with the related regulations and laws of the concerned country and region. When you want to install and repair the product, contact our customer support team, and ask an expert.
* Do not install and use the product in a dusty or dirty place. Dust or foreign substances may cause failure or abnormal performance of the product.
* Do not install and use the product in a place where magnetism exists or its influence reaches the product or there is electromagnetic interference. Magnetism may damage the product or cause abnormal performance.
* When operating the product, do not wear loose clothing or jewelry, and if the hair is long, take precautions to tie it back so that the hair does not get caught in the joints of the robot.
* Do not enter the operation range or touch the robot while the robot is in operation. Otherwise, there is a risk of injury.
* Prevent the product from being damaged by transporting it in a packaged state and by storing it in a dry place with low humidity. Otherwise, the moisture inside the packaging material may cause the product to get damaged or to fail.
* When it comes to storing the product, avoid places where temperature and humidity may change easily. Store the product in a clean, cool, and dry place.
* When transporting the product, maintain proper posture, and two or more people should work together. Otherwise, you may suffer injury to parts of your body, including waist, arms, and legs.
* If you use lifting equipment to transport the product, follow the safety regulations and equipment usage guidelines in the concerned country and region.
* When transporting the product, fully understand the transportation-related contents of the manual and comply with the instructions. We are not responsible for any damage to or breaking of the product because of transportation by the customer.





# 1. Robot System

# 1.1 Basic Configuration

Industrial robots are “machines that are equipped with manipulation and movement functions based on automatic control for them to perform various works by using programs at an industrial site.” The collaborative robot is a type of industrial robot.

The robot system consists of a manipulator and a controller that controls the manipulator. A teach pendant that is to be used for setting and manually operating the robot system is attached to the controller.

* Robot: Performs various works in industrial sites such as transporting objects, assembling parts, etc.
* Controller: Adjusts the robot’s operation according to the program setting values set through the teach pendant. It can be interoperated with various external equipment or devices through the input/output port of the controller. 
* Teach Pendant: A device that manages the entire robot system. It enables you to teach the robot a specific posture or setup and control the programs.

The following shows an example of the basic configuration of the robot system according to the robot type.

![Figure 1 Basic Configuration of the LCD Robot System](../../_assets/image_286.png)



![Figure 2 Basic Configuration of the Vertical Articulated Robot System ](../../_assets/image_285.png)

![Figure 3 Basic Configuration of the Collaborative Robot System ](../../_assets/image_292.png)

# 1.1.1 Controller

#### Vertical Articulated Robot Controller 

![Figure 4 Front \(Left\) / Back \(Right\) of the Controller](../../_assets/image_33.png)

| No. | Name | Description |
| :--- | :--- | :--- |
| ![](../../_assets/c1.png)  | Connection part | A passage for connecting instruments and the teach pendant to the controller or for connecting application devices to internal modules |
| ![](../../_assets/c2.png)  | Power switch | Turns on or off the power of the controller |
| ![](../../_assets/c3.png)  | Hook for storing the TP | Used for hanging the teach pendant or storing it |
| ![](../../_assets/c4.png)  | Emergency stop switch | Causes the robot to stop operating when pressed in case of an emergency |
| ![](../../_assets/c5.png)  | Cooling fan | A device that forcibly discharges the heated air inside the controller |

#### Collaborative Robot Controller

![Figure 5 Front \(Left\) / Back \(Right\) of the Controller](../../_assets/image_15.png)



| o. | Name | Description |
| :--- | :--- | :--- |
| ![](../../_assets/c1.png) | Robot cable connector | A connector that has built-in communication and power lines, making it possible to connect the controller to the equipment. |
| ![](../../_assets/c2.png) | Power connector | A connector that supplies power to the controller. |
| ![](../../_assets/c3.png) | Power circuit breaker | The main power of the controller can be turned on or off with the power switch. |
| ![](../../_assets/c4.png) | Vent | An air inflow passage for cooling the controller. |
| ![](../../_assets/c5.png) | Handle | It is mounted on the front and rear of the controller and used for transportation. |
| ![](../../_assets/c6.png) | Emergency stop switch | When an emergency situation occurs, the operation of the robot can be stopped by pressing the emergency stop switch. |
| ![](../../_assets/c7.png) | Application device connection hole | A passage to be used when an application device needs to be connected using a cable, with an internal module. |
| ![](../../_assets/c8.png) | Teach pendant connection hole | A passage for the connection of a teach pendant of direct-connection type. |
| ![](../../_assets/c9.png) | I/O connection block | This connects peripheral devices to the controller. |
| ![](../../_assets/c10.png) | Door | You can open the side of the controller by opening the door. |
| ![](../../_assets/c11.png) | Cooling fan | It is a device that forcibly discharges the heated air from inside the controller. |



# 1.1.2 Teach Pendant

TP600 and TP630 teach pendants are supported. This operation manual describes how to use a teach pendant based on the TP600 model.

TP600 is a model developed exclusively for the Hi6 controller and provides a large touch screen.



![Figure 5 Front \(Left\) / Back \(Right\) of TP600](../../_assets/image_16.png)



<table>
  <thead>
    <tr>
      <th style="text-align:left">No.</th>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">Operation key</td>
      <td style="text-align:left">Controls the robot&#x2019;s operation, inputs commands, or selects a menu</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">Display</td>
      <td style="text-align:left">The touch screen enables you to check and change the operation status
        and set the information of the robot.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">Mode switch</td>
      <td style="text-align:left">You can turn the mode switch to select the operation mode (
        <img src="../../_assets/sb-manual.png"
        alt/>manual,
        <img src="../../_assets/sb-auto.png" alt/>automatic,
        <img src="../../_assets/sb-remote.png" alt/>remote). If you remove the mode switch from the teach pendant, the selected
        operation mode will be locked.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">Emergency stop switch</td>
      <td style="text-align:left">Causes the robot to stop operating when pressed in case of an emergency</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">Jog dial</td>
      <td style="text-align:left">Can be used to set the menu</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">Mounting bracket</td>
      <td style="text-align:left">Holds or hangs the teach pendant to store it</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left">Enabling switch</td>
      <td style="text-align:left">
        <p>A switch that is to be used as a safety switch when operating the robot
          with the teach pendant in manual mode</p>
        <ul>
          <li>Stage 1, Stage 3: The robot operation will stop. In the case of Stage
            3, the switch will recover to Stage 1 without going through Stage 2.</li>
          <li>Stage 2: You can operate the robot.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c8.png" alt/>
      </td>
      <td style="text-align:left">Cable connection connector</td>
      <td style="text-align:left">A connector for connecting the cable to the controller</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c9.png" alt/>
      </td>
      <td style="text-align:left">USB connection port</td>
      <td style="text-align:left">Can be used to connect a device that can be accessed by USB communication
        such as a transportable storage device</td>
    </tr>
  </tbody>
</table>

TP630 is a model to which the same operation key usage environment as that of the existing Hi5a controller is applied, and it provides a screen with a layout similar to that of the TP600.

![Figure 6 Front \(Left\) / Back \(Right\) of TP630](../../_assets/image_31.png)

#### Operation Keys



<table>
  <thead>
    <tr>
      <th style="text-align:left">Operation Key</th>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-shift.png" alt/>
      </td>
      <td style="text-align:left">shift</td>
      <td style="text-align:left">
        <ul>
          <li>Pressing the <b>&lt;shift&gt;</b> key together with a specific key will
            switch the function of the specific key.</li>
          <li>You can switch the current screen in use by pressing this key together
            with the <b>&lt;&#x2191;/&#x2193;&gt; </b>key in the JOB editing window.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-ctrl.png" alt/>
      </td>
      <td style="text-align:left">ctrl</td>
      <td style="text-align:left">Pressing the <b>&lt;ctrl&gt;</b> key together with a specific key will execute
        the function defined for the specific key.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-up-dn.png" alt/>
      </td>
      <td style="text-align:left">up/down</td>
      <td style="text-align:left">Pressing the <b>&lt;&#x2193;/&#x2191;&gt; </b>key in manual mode will make
        it possible to move forward and backward in the unit of step.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-stop.png" alt/>
      </td>
      <td style="text-align:left">stop</td>
      <td style="text-align:left">
        <p>Pressing the <b>&lt;stop&gt;</b> key will temporarily stop the robot in
          automatic operation.</p>
        <ul>
          <li>When the robot stops, the stop lamp will be turned on, and the start lamp
            will be turned off.</li>
          <li>As the robot is stopped while executing the path of the created program,
            there is no risk of collision with peripheral devices.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-start.png" alt/>
      </td>
      <td style="text-align:left">start</td>
      <td style="text-align:left">Pressing the <b>&lt;start&gt;</b> key will start the automatic operation
        of the program created in the robot. When the robot starts operation in
        automatic mode, the start lamp will be turned on, and the stop lamp will
        be turned off.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-mot-on.png" alt/>
      </td>
      <td style="text-align:left">motor</td>
      <td style="text-align:left">
        <p>You can supply the servo power to the motor of each axis of the robot.</p>
        <ul>
          <li>Pressing the <b>&lt;motor&gt;</b> key in manual mode will make the motor
            lamp blink.</li>
          <li>Pressing the <b>&lt;motor&gt;</b> key in automatic mode will turn on the
            motor lamp.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-enter.png" alt/>
      </td>
      <td style="text-align:left">enter</td>
      <td style="text-align:left">
        <ul>
          <li>If you press the <b><<b>ENTER</b>></b> key when inputting a number, the input
            value will be applied to the setting.</li>
          <li>If you press the <b><<b>ENTER</b>></b> key for a response of Yes/No, Yes
            will be selected.</li>
          <li>When editing a statement in manual mode, if you press the <b><<b>ENTER</b>></b> key
            while in the statement cursor, the cursor will switch to the word cursor
            that enables you to edit the parameters of the statement.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-esc.png" alt/>
      </td>
      <td style="text-align:left">esc</td>
      <td style="text-align:left">
        <ul>
          <li>Allows you to cancel the key input or various functions in progress</li>
          <li>Pressing the <b>&lt;esc&gt;</b> key allows you to switch to a higher level
            without saving the changes.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-left-right.png" alt/>
      </td>
      <td style="text-align:left">left/right</td>
      <td style="text-align:left">
        <ul>
          <li>Allows you to move the cursor to previous or next when inputting texts</li>
          <li>If you press the <b>&lt;&#x2190;/&#x2192;&gt;</b> key in the word cursor
            status, you can move to the recorded step or other function parameters.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-num.png" alt/>
      </td>
      <td style="text-align:left">
        <p>number key</p>
        <p></p>
        <p></p>
        <p></p>
        <p></p>
        <p></p>
        <p></p>
        <p></p>
        <p></p>
        <p>jog key</p>
      </td>
      <td style="text-align:left">
        <ul>
          <li>You can input a number.</li>
          <li>If you press this key together with the <b>&lt;shift&gt; </b>key, you can
            input a sign (- / +) or comma (,), or delete a statement or parameter.</li>
          <li>
            <p>&lt;BS&gt;: Backspace allows you to erase the characters of the text one
              by one at the position of the cursor input. Moreover, if you select parameters
              when editing command and then press the <b>&lt;BS&gt;</b> key, you can delete
              the entire parameter values.</p>
            <p></p>
          </li>
        </ul>
        <p>While the motor is turned on in manual mode and the enabling switch is
          held, the &lt;enter /esc / &#x2190;/ &#x2192; &gt; keys and number keys
          will be operated as &#x201C;jog keys.&#x201D;</p>
        <ul>
          <li>The axis name designated to each key will be displayed on the right edge
            of the display.</li>
          <li>The &lt;&#x2192;&gt; key is for the direction of increase (+), and the
            &lt;&#x2190;&gt; key is for the direction of decrease (-).</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

# 1.2    Basic Use

# 1.2.1 Turning On the Power

{% hint style="info" %}
The method of turning on and off the power may differ depending on the type of controller.
{% endhint %}

#### Vertical Articulated Robot Controller

To start up the robot, power should be supplied to the robot controller. 

Turn the power switch on the left side of the robot controller to the ON direction to connect the main power of the controller. When the power is connected, the robot system will boot, and the display of the teach pendant will be turned on together with all the devices.

![](../../../_assets/image_12.png)

#### Collaborative Robot Controller

The power of the collaborative robot is supplied through the power connector of the controller.

Push upward the switch on the power breaker. When power is connected, the robot system will boot, the display of the teach pendant will be turned on, and the collaborative robot’s LED lamp will be turned on in white.



![](../../../_assets/image_23.png)

### 



# 1.2.1.1 Input of the Power to the Motor and the Operable Status

The status of the mode switch and safety plug of the teach pendant determines the input of power to the motor and the operable status.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Safety Plug</th>
      <th style="text-align:left">Mode Switch: Manual</th>
      <th style="text-align:left">Mode Switch: Automatic</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Released</td>
      <td style="text-align:left">
        <ul>
          <li>Motor ON enabled</li>
          <li>Step Forward/Backward enabled</li>
        </ul>
      </td>
      <td style="text-align:left">Emergency (Motor Off)</td>
    </tr>
    <tr>
      <td style="text-align:left">Inputted</td>
      <td style="text-align:left">
        <ul>
          <li>Motor ON enabled</li>
          <li>Step Forward/Backward enabled</li>
        </ul>
      </td>
      <td style="text-align:left">
        <ul>
          <li>Motor ON enabled</li>
          <li>Operation at normal speed</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
Safety plugs are used for general industrial robots, whereas a light curtain instead of a safety plug is used for LCD robots.
{% endhint %}

# 1.2.2 Turning Off the Power

It refers to all operations of stopping the robot and turning off the power button of the controller after performing all works.

{% hint style="warning" %}
* If the robot will not be in use for a long time, the encoder battery may be discharged, so move the robot to the reference position and then turn off the power.

* Be careful as the encoder data may be destroyed if the power is turned off while the encoder battery has a voltage drop alarm. 
{% endhint %}

#### Vertical Articulated Robot Controller

1.	Press the &lt;Stop&gt; key on the teach pendant. Then, the robot in operation will stop, and the stop lamp will be turned on.

2.	Press the emergency stop switch on the teach pendant. Then, the servo power to the robot motor will be cut off, and then the motor will be turned off.

![](../../_assets/image_36.png)



3.	Turn the power switch on the left side of the robot controller to the OFF direction. Then, the robot system will be powered off.

![](../../_assets/image_29.png)

#### Collaborative Robot Controller

1.	Press the &lt;Stop&gt; key on the teach pendant. The robot in operation will stop, and the stop lamp will be turned on.

2.	Press the emergency stop switch on the controller. The servo power to the robot motor will be cut off, and then the motor will be turned off.

![](../../_assets/image_11.png)



3.	Push downward the switch on the power circuit breaker. When the power is cut off, the robot system will be turned off, and the display of the teach pendant and the LED lamp of the collaborative robot will be turned off.

![](../../_assets/image_288.png)

# 1.2.3 Changing the language of the teach pendant screen

If you need to change the language of the teach pendant, you can change it with the following procedure. The following is an example of changing Korean to English mode.

1.	Click \[메뉴\] button\( \) on the right-button-bar.

![](../../_assets/image_291.png)

2.	Select \[9: TP 응용프로그램 종료\].\(  \)

![](../../_assets/image_293.png)

3.	Click the globe icon on the top-right corner.

![](../../_assets/image_289.png)

4.	Select \[English\] on pop-up menu.

![](../../_assets/image_282.png)

5.	Click \[run TP\] button on the bottom-right corner and wait for about 8 seconds.

![](../../_assets/image_294.png)



# 1.2.4 Screen of the Hi6 Teach Pendant

You can control the operation of the robot or manage devices that interoperate with the robot. The Hi6 teach pendant screen is configured as follows.

![Figure 7 Configuration of the Hi6 Teach Pendant](../../../_assets/image_283.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">The status bar displays the communication status and operation mode of
        the teach pendant and the status and mechanism of the robot system. For
        details, refer to &#x201C;<a href="status-bar.md"><b>1.2.4.1 Status Bar</b></a>&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">You can check and change the setting values using the function buttons.
        For details, refer to &#x201C;<a href="function-buttons.md"><b>1.2.4.3 Function</b> <b>Buttons</b></a>&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">Work area. You can perform various tasks such as editing the JOB program
        and checking the monitoring information. You can perform multiple tasks
        simultaneously.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">You can check and change the setting values of the menus and execute various
        functions using the menu buttons. For details, refer to &#x201C;<a href="menu-buttons.md"><b>1.2.4.4 Menu Buttons</b></a>&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">The jog bar displays the name of the axis newly selected according to
        the reference coordinate system of the jog execution selected using the <b>[Crd. Sys]</b> button.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Taskbar. For details, refer to &#x201C;<a href="log-bar.md"><b>1.2.4.2 Log bar</b></a>&#x201D;</p>
        <ul>
          <li>It displays the current time information and the memory usage status of
            the teach pendant. You can also check error messages or warning messages.</li>
          <li>You can display the keyboard on the screen or hide it. While using the
            soft keyboard, you can move the keyboard to the top of the screen.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### 

# 1.2.4.1 Status Bar

![Figure 8 Status Bar](../../../_assets/image_284.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">The name of the robot controller platform</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">Displays the status of Ethernet communication between the teach pendant
        and the COM module of the main body of the robot controller (
        <img src="../../../_assets/flag-comm-ok.png"
        alt/>: Normal /
        <img src="../../../_assets/flag-comm-ng.png" alt/>: No response)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Displays the operation mode of the robot</p>
        <ul>
          <li><b>Manual</b>: This is a robot teaching mode that enables you to control
            the robot with a jog and create a JOB program.</li>
          <li><b>Auto</b>: This mode allows the robot to automatically operate through
            the playback of a JOB program.</li>
          <li><b>Remote Manual</b>: This is a state in which the mode is determined
            by a remote I/O signal. (Current status: Manual mode)</li>
          <li><b>Remote Auto</b>: It is a state in which the mode is determined by a
            remote I/O signal. (Current status: Auto mode)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">Displays the various states of the robot system</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">Displays the operation status of the robot (
        <img src="../../../_assets/flag-mot-on.png"
        alt/>: Motor ON /
        <img src="../../../_assets/flag-start.png" alt/>: Robot is playing back /
        <img src="../../../_assets/flag-stop.png"
        alt/>: Robot has stopped)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">Displays the model name of the selected robot mechanism</td>
    </tr>
  </tbody>
</table>

# 1.2.4.2 Log Bar

![Figure 9 Log Bar](../../../_assets/image_287.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">Displays the date and time information. If you touch the <b>[Menu]</b> button
        &gt; <b>[08: Setting of Date and Time]</b> menu, you can change the date
        and time information. For details on changing the date and time information,
        refer to &#x201C;<b>4.5</b>  <b>Setting of Date and Time.</b>&#x201D;</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>Displays the memory (RAM) usage status of the teach pendant. Displays
            the used and residual capacity compared to the total capacity of the memory
            in a bar graph and helps check the residual capacity (MByte) numerically.</li>
          <li>If an error or warning occurs, a notification message will appear instead
            of the memory usage status and will blink for about one minute and then
            stop.</li>
          <li>You can check the occurrence timing of errors and warnings on the right
            side of the notification message. Moreover, if you touch the notification
            message, you can check the history of errors and warnings in a new window.</li>
          <li>For details on the notification message, refer to &#x201C;<b>2.5 Error Information.</b>&#x201D;</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Displays a soft keyboard on the screen. For details on how to use the
          soft keyboard, refer to &#x201C;<b>3.2.4.4 Soft Keyboard.</b>&#x201D;</p>
        <ul>
          <li>If you touch the <b>[</b>
            <img src="../../../_assets/bt-dock-softkb.png"
            alt/><b>]</b> button while using the soft keyboard, you can move the keyboard
            to the top of the screen.</li>
          <li>To hide the soft keyboard, touch the <b>[</b>
            <img src="../../../_assets/bt-softkb.png"
            alt/><b>]</b> button.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

# 1.2.4.3 Function Buttons

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">No.</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p><b>[Recording Condition]</b> button: You can set the basic value of the
          recording condition for the move statement.</p>
        <p>After touching the <b>[Recording Condition]</b> button, you need to input
          data related to the interpolation, moving speed and unit, accuracy, and
          tool number in the setting window, and then touch the [<b>OK] </b>button
          (
          <img src="../../../_assets/icon-ok (1).png" alt/>).</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/lbt-bar-en.png" alt/>
      </td>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p><b>[Execution Unit]</b> button: You can set the program execution unit
          in manual or automatic mode.</p>
        <p></p>
        <p>Manual mode: Touch the [run to] button repeatedly until the desired option
          appears.</p>
        <ul>
          <li>
            <img src="../../../_assets/bt-runto-cmd-en.png" alt/>[cmd]: Will execute the command line by line</li>
          <li>
            <img src="../../../_assets/bt-runto-step-en.png" alt/>[step]: Wil execute step by step</li>
          <li>
            <img src="../../../_assets/bt-runto-end-en.png" alt/>[end]: Will execute up to the end statement</li>
        </ul>
        <p></p>
        <p>Automatic mode: After touching the [run to] button, set the option in
          the setting window.</p>
        <ul>
          <li>
            <img src="../../../_assets/bt-runto-1-cycle-en.png" alt/>[1 cycle]: Will execute up to the end statement before stopping</li>
          <li>
            <img src="../../../_assets/bt-runto-cont-en.png" alt/>[cont]: Will execute up to the end statement and then execute again starting
            from Step 0</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <p><b>[Speed Adjustment]</b> button: You can set the step speed for user safety.</p>
        <p>After touching the <b>[Speed Adjustment]</b> button, set the maximum step
          forward/backward speed and the automatic operation speed ratio in the setting
          window.</p>
        <ul>
          <li>
            <img src="../../../_assets/bt-spd_manual-en.png" alt/>Manual mode: Displays the speed limit of a step forward/backward (mm/sec)</li>
          <li>
            <img src="../../../_assets/bt-spd_auto-en.png" alt/>Automatic mode: Displays the playback speed (%)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p><b>[Jog Speed Level / Jog Inching]</b> button: You can set the speed level
          of each axis or of the cartesian jog and the use mode of the jog key.</p>
        <ul>
          <li>[
            <img src="../../../_assets/bt-spd-up.png" alt/>/
            <img src="../../../_assets/bt-spd-dn.png" alt/>]: Touch the button repeatedly until the desired speed level of each axis
            or of the cartesian jog (1: Low speed &#x2013; 8: High speed) appears.
            With a long touch of the button, you can set the lowest or highest level
            at once.</li>
          <li>
            <img src="../../../_assets/bt-jog-1.png" alt/>
            <img src="../../../_assets/bt-jog-inch.png" alt/>[1]: Touching the level value will display an inch mark on the top left
            of the level value, and the mode will switch to the inching mode. Touch
            the level value to return to normal mode. Then, the inch mark will disappear.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">
        <p><b>[Tool]</b> button: You can check and set the selected tool number.</p>
        <p>After touching the <b>[Tool]</b> button, input the tool number in the setting
          window and then touch the <b>[OK]</b> button.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">
        <img src="../../../_assets/bt-gun-off-en.png" alt/>
        <img src="../../../_assets/bt-gun-on-en.png" alt/><b>[Gun] </b>button: You can check the selected gun number and set the
        gun to an ON/OFF state. Check the gun number and touch the <b>[Gun]</b> button.
        Then, the gun will switch to an ON or OFF state, and the color of the button
        will change.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left">[Help] button: Displays detailed information about the selected statement
        or an error message or a warning message</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* Jog inching mode: In normal mode, the robot keeps moving while you are pressing the jog key, but in inching mode, the robot moves only as much as the set value of each inching level and then stops, so you can operate the robot in detail.
* Gun
* It will determine whether to record the gun squeeze operation during the step recording process when you use spot welding. When this button is pressed together with the &lt;shift&gt; key, the GUN signal will be outputted manually.
* When you use arc welding, if the lamp is on during automatic operation, arc welding will be progressed. If the lamp is off, arc welding will not be progressed, but only the taught trajectory will be checked.
{% endhint %}

# 1.2.4.4 Menu Buttons



<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">No.</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c1.png" alt/>
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
        <img src="../../../_assets/rbt-bar-en.png" alt/>
      </td>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Coordinate System: You can check and set the reference coordinate system
          for the jog execution.</p>
        <p>Touch the <b>[Crd. Sys]</b> button repeatedly until the desired coordinate
          system mode appears. The name of the axis newly selected according to the
          selected reference coordinate system will be displayed on the jog bar on
          the right side of the screen.</p>
        <ul>
          <li>
            <img src="../../../_assets/bt-crd-joint-en.png" alt/>Joint Coordinate System: The name of each joint will be displayed on the
            jog bar. If you touch the [-/+] button on the right side of the joint name,
            you can move the corresponding joint.</li>
          <li>
            <img src="../../../_assets/bt-crd-robot-en.png" alt/>Robot Coordinate System: X, Y, Z, RX, RY, RZ, and additional axes will
            be displayed on the jog bar. Based on the robot coordinate system, the
            tooltip (TCP, Tool Center Point) of the robot can be moved or rotated.</li>
          <li>
            <img src="../../../_assets/bt-crd-user.png" alt/>User Coordinate System: X, Y, Z, RX, RY, RZ, and additional axes will
            be displayed on the jog bar. The tooltip of the robot can be moved and
            rotated based on the user coordinate system.</li>
          <li>
            <img src="../../../_assets/bt-crd2-tool-en.png" alt/>Tool Coordinate System: X, Y, Z, RX, RY, RZ, and additional axes will
            be displayed on the jog bar. The tooltip of the robot can be moved and
            rotated based on the tool coordinate system.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
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
        <p>
          <img src="../../../_assets/bt-pos-mod-en.png" alt/>(In combination with the &lt;shift&gt; key) Position Correction: Apply
          the robot&#x2019;s current posture as the target pose of the step in the
          JOB program.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Command Inputting: Input the desired command.</p>
        <p>After touching the <b>[Command]</b> button, touch the command in the command
          inputting window. Then, the statement will be inputted right below the
          current cursor position. For details on inputting the commands, refer to
          &#x201C;<b>3.2.2 Statement Inputting.</b>&#x201D;</p>
        <p>
          <img src="../../../_assets/bt-delete-en.png" alt/>(In combination with the &lt;shift&gt; key)</p>
        <p>Deletion: You can delete the statement in the JOB program.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Attribute: You can check the attributes of a statement.</p>
        <p>After selecting a statement by touching it, touch the <b>[Attribute</b>]
          button. Then, the attribute window for the statement will appear.</p>
        <p>
          <img src="../../../_assets/bt-block-edit-en.png" alt/>(In combination with the &lt;shift&gt; key) Block Editing: You can enter
          the block editing mode where you can perform copying, cutting, and pasting
          in the JOB program. For details on block editing, refer to &#x201C;3.2.4.5
          Block Editing Mode.&#x201D;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">[Menu]: You can use the service function menus in the program.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left">[system]: You can set the user environment using the system menu of the
        program.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c8.png" alt/>
      </td>
      <td style="text-align:left">Favorites: You can quickly execute predesignated functions using code
        numbers. Touch the <b>[Favorites]</b> button, input the code number, and
        touch the <b>[OK] </b>button. Then, the designated function will be executed.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c9.png" alt/>
      </td>
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

# 1.2.4.5 Work area

The work area is an area where you can perform various tasks, such as editing JOB programs and checking the monitoring information.

![Figure 10 Layout of the Work Area](../../../_assets/image_309.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>The work area consists of two-panel stacks: top and bottom.</p>
        <ul>
          <li>You can perform multiple tasks simultaneously by adding a panel window
            to each panel stack.</li>
          <li>You can add a new panel stack at the top and bottom of an existing panel
            stack or between panel stacks</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Panel stack. The names of all currently open panels are displayed, and
          the selected panel window appears at the bottom.</p>
        <ul>
          <li>You can change the order on the panel window by selecting a panel name
            by touching it and then dragging it to the desired location.</li>
          <li>If you select a panel name by touching it and dragging it to another panel
            stack, you can move the location of the panel window to another panel stack.</li>
          <li>If you select a panel name by touching it and dragging it to a location
            other than the existing panel stack, a new panel stack will be added, and
            then the panel window will open in the new panel stack.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[+]: You can open a new panel window by selecting the desired monitoring
            item from the panel selection window. Panel windows will be added as tabs
            to the panel stack.</li>
          <li>[X]: You can close the selected panel window. If there is only one panel
            window in the panel stack, the panel window cannot be closed.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

# 2. Operation

Operation refers to the act of instructing the contents of the work to the robot and checking the contents. In general, when it comes to industrial robots, manual and automatic modes are used. Manual operation refers to the act of directly instructing the contents of the work to the robot, and the automatic operation refers to the act of making the robot repeatedly execute the contents of the instructed work.

# 2.1 Manual Operation

Manual operation is an operation method of directly teaching and checking the robot at a safe speed.

# 2.1.1 Operation Method

The method of instructing the contents of the work to the robot using the jog key and checking the contents of the instructed work are as follows.

1.	Check whether there are people or obstacles within the safety fence and the operation range of the robot.

2.	Set the operation mode to manual mode by turning the mode switch of the teach pendant.





![](../../_assets/image_40.png)

3.	In the status bar of the Hi6 teach pendant screen, check whether the operation mode is set to manual mode.

![](../../_assets/image_325.png)

* If it is set to automatic mode, set the operation mode to manual mode by turning the mode switch of the teach pendant.

4.	Touch the \[Program\] button in the JOB program window. Then, the program selection window will appear.

![](../../_assets/image_329.png)



5.	Select a program from the list in the program selection window or input the program number and then touch the \[OK\] button.

![](../../_assets/image_317.png)

6.	Press the &lt;motor&gt; key on the teach pendant. Then, the motor lamp will blink, and the servo power will be ready to be supplied to the motor of each axis of the robot.

7.	Press the enabling switch on the back of the teach pendant. Then, the motor lamp will be turned on, and the motor brake will be released, allowing the servo power to be supplied. The robot will be ready to move.

8.	Operate the robot according to the speed level or movement conditions of the coordinate system using the jog key.

* To save the robot’s location, touch the \[Record\] button at the desired location. Then the step will be recorded.
* To record the function required for the step, touch the \[Command Inputting\] button.
* To check the robot’s location while manually moving it forward or backward, press the &lt; ↓ / ↑ &gt; key. While you are pressing the &lt; ↓ / ↑ &gt; key, the robot will move in the unit of step. When the robot reaches the target step, the execution completion mark \( . \) will appear in front of the command, and then the robot will stop.





# 2.1.2 Operation Speed Adjustment

In manual mode, you can operate the robot using the step forward/backward operation and manual jog operation. With the function button on the left side of the Hi6 teach pendant screen, you can check and adjust the step forward/backward speed limit \(![](../../_assets/c1.png)\) and the jog’s speed level \(![](../../_assets/c2.png)\).

![](../../_assets/lbt-spd-bar-en.png)

To set the step speed limit, touch the \[Speed Adjustment\] button and then input the speed value in the setting window. The step forward/backward speed limit will be displayed in numbers along with the unit \(mm/sec\) on the \[Speed Adjustment\] button. The maximum speed of the robot tool and link will be limited below the speed limit.

![](../../_assets/cond-set-step-fwd-bwd-spd-en.png)

For example, if the speed limit in manual mode is set to 250 mm/s and the recorded step speed is 1,000 mm/s, the moving speed of the step will be limited to 250 mm/s during the step forward/backward operation. When the recorded speed is 100 mm/s, the robot will move at 100 mm/s because the recorded speed does not exceed the speed limit.

{% hint style="info" %}
In automatic mode, the \[Speed Adjustment\] button will display the playback speed \(%\) instead of the step speed limit \(mm/sec\).
{% endhint %}

To set the jog speed level \(1: Low to 8: High\), touch the \[ / \] button repeatedly until the desired speed level appears. The jog speed level will be displayed in numbers between the \[ / \] buttons. Even in this case, the maximum speed of the robot tool and link will be limited below the speed limit.

![](../../_assets/lbt-spd-bar2.png)

{% hint style="warning" %}
If the length and angle in the tool data are set differently from the actual values, the tool may operate too fast in manual mode. Before operating the robot, you must make sure that the tool data is set correctly.
{% endhint %}



# 2.1.3 Step Forward/Backward

The step forward/backward is one of the methods of operating the robot in manual mode and refers to the act of playing back a recorded program. By manipulating the robot in the step forward/backward operation, you can check the recorded program path and mutual interlock relationship at a range of safe speed.

The execution unit for the step forward/backward operation can be checked and set from the \[run to\] button on the left side of the Hi6 teach pendant screen.

![](../../_assets/image_318.png)

To set the execution unit for the step forward/backward operation, touch the \[run to\] button repeatedly until the desired option appears.

![](../../_assets/image_303.png)

* **\[cmd\]:** Will execute the command line by line
* **\[step\]:** Will execute step by step
  ****
* **\[end\]:** Will execute up to the end statement
  ****



When the execution unit is set as cmd or step, the robot will ignore the set accuracy area and reach the recorded step. If it is set as end, the robot will operate on the same path as the one for playing b/n automatic mode.

When you set the execution unit as cmd or step and perform the step forward/backward operation, the robot will operate on a path without cornering. For details on cornering, refer to ???[2.3.1.4 Accuracy](../3-step/1-step-cmd-param/4-accuracy.md).???

![Figure 11 Playback Forward/Backward Path When cmd/step Setting is Performed](../../_assets/path-cmd-step-pback-fwd-bwd-en.png)

If you set the execution unit as end and then perform the step forward/backward operation, the path of the robot will change according to the stop position. In other words, if the robot stops at a place other than at cornering and then executes the forward operation, the robot will recover the original cornering path, but if the robot executes the backward operation, the robot will move to the recorded step, and at this time, the robot will stop at the recorded step and then move immediately to the previous step. When the robot stops at cornering, the robot will maintain its previous cornering path both when moving forward and when moving backward.

![Figure 12 Playback Forward/Backward Path When End Setting is Performed](../../_assets/path-end-pback-fwd-bwd-en.png)

When the robot stops at cornering and then executes the forward operation, the robot will operate on the original cornering path. Here, if the robot executes the backward operation and then, without reaching the previous step completely, executes the forward operation again, the robot may not be able to create the original cornering path in some cases. In other words, if the distance of the step becomes shorter than the original distance, making it impossible to meet the existing accuracy condition, a smaller cornering path than the original one will be created.

![Figure 13 Example of the Robot Path Change During Step Forward/Backward Operation](../../_assets/path-step-bwd-then-fwd-en.png)


You can set the maximum speed for the step forward/backward operation and set whether to execute functions as well. After touching the \[run to\] button on the left side of the Hi6 teach pendant screen, set the speed value and function execution option in the setting window.



![](../../_assets/cond-set-step-fwd-bwd-spd-en.png)

* \[2: Step FWD/BWD maximum speed\]: Same as the value set for the speed in manual operation
* \[3: Function execution during step FWD\]: You can select the function execution option.
  * Off: The function will not be executed for the step forward/backward operation. Regardless of the conditions of the external I/O, you can check only the robot path. Be careful as the interlock with the external system will not work.
  * On: You can execute all functions. Should be used after the external interlock is completed.
  * I On: You can execute only the input wait function. It should be used when it is necessary to check the safety through the external interlock.





# 2.2 Automatic Operation

Automatic operation is an operation method of teaching the robot the contents of the work that it should execute and then making the robot perform the work.

# 2.2.1 Operation Method

It is the method to teach the robot the contents of the work and then make it perform the work is as follows.

1.	Check whether there are people or obstacles within the safety fence and the operation range of the robot.

2.	Set the operation mode to automatic mode by turning the mode switch of the teach pendant.



![](../../_assets/mode-sw-auto.png)

3.	On the status bar of the Hi6 teach pendant screen, check whether the operation mode is set to automatic mode.



![](../../_assets/image_301.png)

* If it is set to manual mode, turn the mode switch of the teach pendant to set the operation mode to automatic mode.

4.	Touch the \[Recording Condition\] button on the left side of the initial screen. Then, the condition setting window will appear.

![](../../_assets/image_332.png)



5.	Set the program repetition option and robot operation speed.

![](../../_assets/image_305.png)

* **\[1: Operation Cycle type\]:** You can set whether to repeat the program that will be executed during automatic operation.
* **\[6: Playback speed rate\]:** You can set the operation speed \(%\) of the robot when a program is played back in automatic mode.  
  For example, if the operation speed is set to 100, the robot will move at the recorded speed of the step, and if it is set to 50, the robot will move at the ratio of 50% of the recorded speed.
  ****



6.	Press the &lt;start&gt; key on the teach pendant. The start lamp will be turned on, and the robot will perform the work according to the created program.



# 2.2.2 Operation Speed Adjustment

In automatic operation, the \[Speed Adjustment\] button on the left side of the Hi6 teach pendant screen will display the robot's operation speed \(%\) while the program is being played back. The displayed operation speed is the ratio of the robot’s moving speed to the speed recorded in the step.

![](../../_assets/lbt-auto-spd_en.png)

{% hint style="info" %}
In manual mode, the \[Speed Adjustment\] button will display the step speed limit, instead of the playback speed \(%\).
{% endhint %}

In automatic mode, you can adjust the operation speed of the robot, without modifying the program, by changing the value of the automatic operation speed ratio in the condition setting. After touching the \[Speed Adjustment\] button on the left side of the Hi6 teach pendant screen, set the option values of the \[2: Step FWD/BWD maximum speed\] and \[6: Playback speed rate\] in the setting window.

![](../../_assets/cond-set-step-fwd-bwd-spd-auto-spd_en.png)

# 2.3 Step

A step refers to a specific posture \(the position of each axis or the position of the tooltip\) that is to be recorded in the job program and taken by the robot. In other words, a step is one position that the robot will reach through a movement.

The robot performs various functions while moving from one step to another. For movement from one step to another, a movement condition such as a move, which is a movement command, is required.

* It is the basic unit of robot programming. This is a command for the manipulator to move. It consists of minimum information that is necessary for the operation of the robot. 
* Movement conditions: These are the step statement parameters such as robot position, interpolation, speed, accuracy, and tool number.





# 2.3.1 Step Statement Parameters

The step statement parameters are the movement conditions required for the step movement of the robot, such as the robot position, interpolation, speed, accuracy, and tool number of the robot, in addition to move, a movement command.

Parameters of the step statement are divided into default parameters and optional parameters. The default parameters are the essential ones for a step, and the optional parameters are the ones that can be added when necessary. 

The step statement is configured as follows.



![](../../../_assets/image_77.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">No.</th>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">Interpolation</td>
      <td style="text-align:left">
        <p>Interpolated path between steps</p>
        <p>P (Joint interpolation), L (Linear interpolation), C (Circular interpolation),
          SP (Stationary tool interpolation off), SL (Stationary tool linear interpolation),
          SC (Stationary tool circular interpolation)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">Pose</td>
      <td style="text-align:left">
        <p>A parameter to record a position. This parameter may be omitted, and a
          pose may be designated after the statement (hidden pose).</p>
        <p>Target pose (X, Y, Z, Rx, Ry, Rz, Cfg) {Coordinate system} + Shift (X,
          Y, Z, Rx, Ry, Rz) {Coordinate system}</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">Speed</td>
      <td style="text-align:left">Operation speed of the robot (Unit: mm/sec, cm/min, %, sec)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">Accuracy</td>
      <td style="text-align:left">A value of the allowable error (0&#x2013;7) between the current position
        and the recorded position that occurs when the robot moves to the target
        step</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">Tool number</td>
      <td style="text-align:left">Number of the tool in use (0&#x2013;31)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">Stop condition</td>
      <td style="text-align:left">A condition for the robot to stop moving to execute the next command (step
        or function)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left">Comment</td>
      <td style="text-align:left">Description of the step</td>
    </tr>
  </tbody>
</table>

# 2.3.1.1 Interpolation

Interpolation refers to the interpolated path between steps, and the interpolation method for the \[Step N\] determines the form of the path between \[Step N-1\] and \[Step N\].

* P-PTP \(Point-to-Point\) It is the fastest of the general interpolation modes as it interpolates the path between two steps based on individual axes, not the tooltip. Considering the characteristics of industrial robots that consist of rotation joints, the path of the tooltip is usually shaped in a C form.





![Figure 14 Example of the Tooltip Path in P-PTP Interpolation](../../../_assets/image_73.png)

* L-Linear interpolation It moves in a linear line between two steps in Cartesian space. It is used for a case in which a linear path is needed, such as an arc welding section. The movement will take place while the wrist posture changes automatically as follows.

![Figure 15 Example of L-Linear Interpolation](../../../_assets/image_48.png)

During the linear interpolation, under certain conditions, the robot cannot automatically change the wrist posture, and such a condition is called the singular posture.



{% hint style="info" %}
Singular postures in which the posture interpolation cannot be performed are as follows.

* If the B-axis is near the dead zone: For details on the dead zone setting, refer to ???[7.4.5 B-axis Deadzone](../../../7-system/4-robot-parameter/5-b-axis-deadzone.md).???
* When the sign of the B-axis changes: When the sign of the B-axis angle switches \( - ?�� + \) or \( + ?�� - \)
* When the angle variation of the R2 and R1 axes exceeds 180 degrees
* When the center of the B-axis \(axis 5\) or the tooltip passes the center of rotation of the S-axis \(axis 1\): There may be an error in the trajectory as well as in the posture.
* When the angle variation of the S-axis exceeds 180 degrees
{% endhint %}

* C-Circular interpolation

  It moves in a circular path created between two steps. There should be three points to determine the circle, and the references for selecting them are as follows.



  * At the time of moving from \[Step n\] to \[Step n+1\], if the interpolation method of \[Step n+1\] is C-circular interpolation, it is required to refer to the next step \[Step n+2\].

  * If the interpolation method of \[Step n+2\] is C-circular interpolation, it is required to determine the circle based on \[Step n\], \[Step n+1\], and \[Step n+2\], and among them, movement should take place along the arc of the section of \[Step n\] - \[Step n+1\].

  * If the interpolation method of \[Step n+2\] is not a circular interpolation, it is required to refer to the previous step \[Step n-1\] and determine the circle based on \[Step n-1\], \[Step n\], and \[Step n+1\], and among them, movement should take place along the arc of the section of \[Step n\] - \[Step n+1\].



![Figure 16 Example 1 of C-Circular Interpolation](../../../_assets/image_338.png)

If you use the criteria of selecting three points required for determining the circle, you can create a program through the double registration of the same point, even in the case of a continuous arc.

In this way, by determining the interpolation method of the step in consideration of the path to move along and using the same point dual registration function, you can create a program as desired.

![Figure 17 Example 2 of C-Circular Interpolation](../../../_assets/image_302.png)

* Stationary tool interpolation

  This method will be used when the robot owns the workpiece and perform the work using an externally fixed tool. In this case, the interpolation will be performed based on the workpiece owned by the robot.

  For details on the types of interpolation for stationary tools, refer to ???[7.3.6.2 Stationary Tool Coordinate System](../../../7-system/3-control-parameter/6-cordsys-reg/2-stationary-tool-crdsys.md).???





# 2.3.1.2 Pose

A pose is a parameter to record the position. If you input a move, the movement command, by using the \[Command\] button, you should designate the pose expression in the tg \(target\) parameter. When the move statement is inputted using the \[Record\] button, the tg parameter will not appear. At the moment of touching the \[Record\] button, the position and posture of the manipulator will be recorded, but they will not be displayed on the JOB editing screen, which is why they are called a hidden pose.

The method to input a pose using the menu button on the right side of the Hi6 teach pendant screen is as follows.

* After touching the \[Command\] button, select \[Motion\] and then input the statement.

![](../../../_assets/image_306.png)

* After touching the \[property\] button, set the attributes of the current robot pose and then touch the \[Apply\] button.

![](../../../_assets/image_328.png)

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



# 2.3.1.3 Speed

The operation speed of the robot can be displayed using the following four types of units. They can be used in all interpolation methods.

* ㎜/sec, ㎝/min: Sets the maximum speed of the TCP \(Tool Center Point\) of the robot.   The maximum speed of the robot will be automatically calculated by the controller based on the position and acceleration/deceleration parameters. If the setting value is larger than the maximum speed limit of the performance of the robot, the robot will operate only at the maximum speed limit.



* sec: Sets the robot moving time.  The shortest robot moving time will be automatically calculated by the controller based on the position and acceleration/deceleration parameters. If the setting value is shorter than the shortest time limit of the performance of the robot, the robot will operate only at the shortest time limit.



* %: Sets the ratio of the robot moving speed to the maximum speed at which the robot can operate.  When this is set to 100%, the robot will operate at the maximum speed within the allowable range.





# 2.3.1.4 Accuracy

It will determine the accuracy \(the degree of approach to the recorded position\) at which the robot passes through the step when progressing the target step. When the robot moves to the target step, if the error between the current position and the recorded position that occurs when the robot moves to the target step is less than a certain value, the robot will move to the next step. The value of the allowable error at this time is called accuracy.

A path that is newly created within the accuracy range \(0???7\) according to the accuracy is called a cornering path. In general, the higher the accuracy, the faster the cornering speed, which is advantageous in terms of moving time.



![Figure 18 Change of the Path P2 Because of Accuracy](../../../_assets/image_53.png)

Accuracy 0 has the highest accuracy, and Accuracy 7 has the greatest error. Accuracy will be applied in a way that it cannot be greater than 1/2 of the length of the shorter trajectory of both trajectories of the target step. In other words, you can apply the expression ??�Accuracy ?�� min \(P1-P2, P2-P3\) / 2??? in the example above. In this expression, the TCP distance is used for explanation, but the same concept can be applied to the angle.

In the case of a robot, the value of the applicable accuracy level will be defined based on the tooltip distance and posture angle of the robot. When it comes to additional axes, the value in the case of the linear axis will be defined based on the length, and the value in the case of the rotation axis will be defined based on the angle. You can directly change the values in the \[system&gt; 3: Robot Parameter&gt; 6: Accuracy\] menu. For details on the value of the accuracy level, refer to ???[7.4.6 Accuracy](../../../7-system/4-robot-parameter/6-accuracy.md).???



The figure below shows how the cornering path is created according to the value of the accuracy level. If there is a general 6-axis articulated robot and an additional axis, the value of accuracy level can be set individually for TCP \(tooltip distance\), ORN \(position angle\), and AUX \(additional axis distance\). Because all the values of relevant accuracy levels should be satisfied, the cornering path will be created based on the smallest value among TCP, ORN, and AUX. The cornering path will be created in a constant curve, regardless of the speed variation, while satisfying the convex hull property. However, errors of several millimeters \(mm\) may occur at low speed and high speed because of servo delay.

![Figure 19 Creation of the Cornering Path According to the Value of Accuracy Level](../../../_assets/image_79.png)

{% hint style="info" %}
The mode of creating the cornering path according to the value of accuracy level will be applied to all types of interpolation in the same manner. In the case of P interpolation, the TCP distance accuracy will be applied, but errors may occur.
{% endhint %}

The cornering path will not exceed the convex polygon area because of the convex hull property, as shown below.

![Figure 20 All Points on the Cornering Path within the Convex Polygon Area](../../../_assets/image_87.png)

# 2.3.1.5 Tool Number

The robot position will be determined by the position and posture of the tooltip. You can designate the tool number \(0–31\) that will be used.

# 2.3.1.6 Stop Condition

When the conditional expression “after until” is satisfied, the robot stops moving and executes the next command \(step or function\).

The value of the conditional expression “after until” can be checked through the return value of the result \(\) function. You can check whether the move operation is terminated by a conditional expression.

![Figure 21 Example of Stop Conditions](../../../_assets/image_46_1.png)

{% hint style="info" %}
For details on the robot language, refer to the "[Robot Language Function Manual](https://hrbook-hrc.web.app/#/view/doc-hrscript/english/README)."
{% endhint %}
# 2.3.1.7 Comment

You can input a comment for the description of a step. You can input the contents of comments conveniently by using the soft keyboard.

# 2.3.2 Recording and Changing a Step Position

You can record or change the robot position and posture of the recorded step using the \[Record\] button.

# 2.3.2.1 Axis Angle Recording Coordinate

In manual mode, if the \[1: Pose Recording Form\] option in the \[system&gt; 1: User Environment\] menu is set to axis angle, touch the \[property\] button in the move statement. The following attributes window will appear. The position of the robot recorded by the encoder can only be checked, and the position data cannot be modified.

![](../../../_assets/image_336.png)



# 2.3.2.2 Base and Robot Recording Coordinates

The position and posture of the robot can be displayed differently depending on the coordinate system. If there is no travel axis, the base coordinate and the robot coordinate will generally be the same. If the travel axis is defined, the position and posture of the robot tool will be displayed differently depending on whether it is the base coordinate and the robot coordinate.

In manual mode, if the \[1: Pose Recording Form\] option in the \[system&gt; 1: User Environment\] menu is set to base or robot, touch the \[property\] button in the move statement. You can check the position and posture of the robot tool in the attributes window.

{% hint style="info" %}
If you would like to change the pose recording form, please contact our customer support team to ask an expert or an engineer.
{% endhint %}

For one tooltip position and its orientation, there may be multiple postures because of the characteristics of the instrument, so to define one posture, the robot form \(config.\) should be designated.

Collaborative robots can be restricted by the soft limit because of their mechanical structures. When the robot is not in operation, you can release the soft limit or set it to a large value.

* auto: Regarding the current posture of the robot, the items that come later will be automatically determined. If this mode is not set, a determination will be performed based on whether the items below are designated or not.
* back: The tooltip of the robot is in the – direction on the X-axis of the robot coordinate system, meaning the rear. If this is not designated, the tooltip will be in the + direction, meaning the front. 
* down: Relationship between the H-axis and V-axis. If this is designated, the result will be the bottom. If this is not designated, the result will be top.

![Figure 22 Posture of the H and V Axes: Up \(Left\), Down \(Right\)](../../../_assets/image_58_1.png)



* flip: Flip with the B-axis coordinate being a + value. If this is not designated, the result will be non-flip with a - value. The red arrow in the figure shows the direction of the top of the wrist axis.

![Figure 23 Flip \(Left\) / Non-flip \(Right\) Posture](../../../_assets/image_75.png)

* S \(\|S\|&gt;=180\): The absolute value of the S-axis angle is more than 180 degrees. If not designated, it will be less than 180 degrees.
* 
  B \(\|B\|&gt;=180\): The absolute value of the B-axis angle is more than 180 degrees. If not designated, it will be less than 180 degrees.

* 
  R2 \(\|R2\|&gt;=180\): The absolute value of the R2-axis angle is more than 180 degrees. If not designated, it will be less than 180 degrees.

* R1 \(\|R1\|&gt;=180\): The absolute value of the R1-axis angle is more than 180 degrees. If not designated, it will be less than 180 degrees.



The coordinate system will be saved as \[Pose Variable\].crd \(Example: po32.crd\), and one of the following strings will be designated. If it is an empty string, the basic value will be recognized as joint.

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>Base coordinate system = &quot;base&quot;
          <br />
        </p>
        <p>Robot coordinate system = &quot;robot&quot;
          <br />
        </p>
        <p>Joint coordinate system = &quot;joint&quot;
          <br />
        </p>
        <p>Encoder = &quot;encoder&quot;
          <br />
        </p>
        <p>User coordinate system = &quot;u1&quot; &#x2013; &quot;u10&quot;
          <br />
        </p>
        <p>
          <br />
        </p>
      </td>
    </tr>
  </tbody>
</table>



# 2.4 R Codes

R codes are unique code numbers assigned to specific functions. Assigning unique code numbers to frequently used functions can help you use those functions quickly. For details on R codes, refer to “[8 R codes](../r-code/).”

After touching the \[Favorites\] button on the right side of the Hi6 teach pendant screen, input the code number and touch the \[OK\] button. Then the predefined function will be executed.

![](../_assets/image_313.png)





# 2.5 Error Information

When a problem occurs, a notification will appear on the taskbar at the bottom of the Hi6 teach pendant screen and will blink for about one minute. You can check the error code, notification message, and the time of error occurrence.

![](../../_assets/image_304_1.png)

# 2.5.1 Error Type

Troubles in the robot system are divided into errors and warnings.

* Error: It is trouble serious enough to stop the robot operation, and the code number in the notification message starts with E.

![](../../_assets/image_295.png)



* Warning: The robot will continue to operate, but a warning is a trouble that requires you to check whether or not a response action has been taken. The code number in the notification message starts with W.

![](../../_assets/image_296.png)



# 2.5.2 Error Handling

The following shows how to check and deal with various system troubles, such as system failures or operational errors.

* Check the notification on the taskbar. An error code, notification message, and time of error occurrence will appear.

![](../../_assets/image_304_1.png)

* Touch the notification on the taskbar. Then, the error and warning history will appear in a new window. 

![](../../_assets/image_327.png)

* You can also open the error and warning history window by touching the \[+\] button at the top right of the task panel stack and selecting \[log\].
* 
  The error and warning history will be displayed in chronological order, and the most recent troubles will be highlighted.

* 
  Touch the \[Help\] button on the left side of the Hi6 teach pendant screen. You can check the error code, the notification message, the cause of the trouble, and how to take action for it.

![](../../_assets/image_326.png)





# 2.6 User Buttons

By assigning the desired functions to the buttons in the user button area on the right side of the Hi6 teach pendant screen, you can conveniently use them when teaching a robot.

# 2.6.1 Switching of the User Button Area

Touch the \[User buttons\] button on the right side of the Hi6 teach pendant screen until the desired area appears. Then, the menu button area will be switched to the user button area. In the user key area, the key signal output function and the spot application function are assigned and provided by default.

![](../../_assets/image_337.png)

* If you press the \[User buttons\] button while pressing the &lt;shift&gt; key, you can switch the area in the opposite direction.
* In the user button area, the key signal output function and the spot application function are assigned.
  * 
    The key signal output function area will stay empty as the initial state in which no button is registered.

  * 
    The spot application function area will have buttons registered, which can be used for teaching the robot.





# 2.6.2 Button Registration for Each Area

You can register the desired function in the user key area with a button. Up to eight functions can be registered.



# 2.6.2.1 Key Signal Output Function Area

You can simply turn on/off the desired output signal by registering it with a button.

1.	Touch the \[User Buttons\] button repeatedly until the key signal output function area appears.

2.	While pressing the &lt;ctrl&gt; key, touch the \[User Buttons\] button. The key signal output setting window will appear.

3.	After setting the function name and option to display on the button, touch the \[OK\] button.

![](../../../_assets/image_310.png)



* \[Title\]: This is the function name to be displayed on the button.
* \[on-var.\]: This is the name of the signal output variable or of the number type variable. This is the name of the variable whose value will be turned ON \(assign 1\) when the button is turned ON.
* \[off-var.\]: This is the name of the signal output variable or the number type variable. This is the name of the variable whose value will be turned ON \(assign 1\) when the button is turned OFF.
* \[Toggle\]: This helps you perform the setting in a way that the functions registered with the buttons can be activated or deactivated whenever you touch the buttons. If the toggle function is not used, the functions registered with the button will be activated only while the button is being touched.
* \[Permit on Auto Mode\]: This allows the variable value output function even in automatic mode.
* \[Off on Auto Mode\]: This turns off all variable values \(assign 0\) in automatic mode.



{% hint style="info" %}
You can easily input the signal output variable value using the \[fb\] button and the \[do\] button. For example, input 2.9 and press the <<b>ENTER</b>> key. It will be converted to and displayed as fb2.do9. If you input 9 without decimal point and press the <<b>ENTER</b>> key, it will be converted to do9.
{% endhint %}

4.	Check the buttons in the key signal output function area, and touch each button to make sure that the set value is properly applied.

![](../../../_assets/image_331.png)

{% hint style="info" %}
You can also assign the desired output signals to the buttons in the key signal output function area in the \[Set Up&gt; Control Parameter&gt; Input/Output Signal Setting&gt; Key Signal Output\] menu. For details, refer to ???[7.3.2.8 Key Signal Output](../../../7-system/3-control-parameter/2-io-signal-setting/8-key-signal-output.md).???
{% endhint %}



# 2.6.2.2 Spot Application Function Area

For details on the spot application function, refer to the “Hi6 Controller Spot Welding Function Manual.”

# 2.7 Coordinate System

Coordinates in space are used to determine the direction of the robot’s movement. Hi6 controller has the joint coordinate system, robot coordinate system, user coordinate system, and tool coordinate system.

* Joint coordinate system: You can move the corresponding joint when touching the \[-/+\] button on the right side of the joint name The buttons on the right are for the + direction, and the buttons on the left are for the - direction. For example, when you move the first joint in the joint coordinate system, the &lt;esc&gt; key will be for the + direction, and the <<b>ENTER</b>> key will be for the – direction. When you move the second joint, the &lt;→&gt; key will be for the + direction, and the &lt;←&gt; key will be for the – direction.



* Robot/User/Tool Coordinate System: The tooltip \(TCP, Tool Center Point\) of the robot can be moved and rotated based on each coordinate system.





# 2.7.1 Jog Keys

It will be used in manual mode. When you are holding the enabling switch while the motor is turned on, the <<b>ENTER</b>>, &lt;esc&gt;, and &lt;←/→&gt; keys and number keys on the teach pendant will operate as “jog keys.”

![Figure 25 Jog Keys on the Teach Pendant](../../_assets/image_95.png)

* The name of the axis assigned to each key will be displayed in the jog bar at the right edge of the display.
* The operation keys on the right are for the direction of increase \(+\), and the operation keys on the left are for the direction of decrease \(-\).

Only in the case in which the selected mechanism is mechanism \[0\] robot selected during jogging, if the total number of axes of the next mechanism \[1\] is less than two, they will be assigned according to the order of the registered additional axes. At this time, if unassigned keys remain in the mechanism \[1\] and the next mechanism has room, in terms of the number of axes to which the remaining axes can be assigned, they will be sequentially assigned.

For example, whether to perform an assignment for the axes J7 and J8 according to the number of axes of the mechanisms for the additional axes will be as follows.

| Mechanism \[0\] | Mechanism \[1\] | Mechanism \[2\] | Whether to assign for J7 axis / J8 axis |
| :--- | :--- | :--- | :--- |
| 6-axis robot | Travel axis, Axis 1 | Positioner, Axis 1 | J7: Travel axis / J8: Positioner |
| 6-axis robot | Travel axis, Axis 1 | Positioner, Axis 2 | J7: Travel axis / J8: Not assigned |
| 6-axis robot | Travel axis, Axis 2 | Positioner, Axis 2 | J7: Travel axis 1 / J8: Travel axis 2 |
| 6-axis robot | Travel axis, Axis 3 | Positioner, Axis 1 | J7: Not assigned / J8: Not assigned |







# 2.7.2 Joint Coordinate System

| **Joint Coordinate System** | Robot Coordinate System | User Coordinate System | Tool Coordinate System |
| :---: | :---: | :---: | :---: |
|  ![](../../_assets/bt-crd2-joint-en.png)  | ![](../../_assets/bt-crd2-robot-en.png)  | ![](../../_assets/bt-crd2-user-en.png)  | ![](../../_assets/bt-crd2-tool-en.png)  |

1.	Turn on the motor in manual mode and hold the enabling switch on the back of the teach pendant.

2.	Select the joint coordinate system by repeatedly touching the \[Crd. Sys\] button on the right side of the Hi6 teach pendant screen. Then, the jog bar will display the name of each joint.

3.	Operate the robot with the jog keys. Each joint of the robot moves independently.



![](../../_assets/image_85.png)

{% hint style="info" %}
For details on the robot’s progress direction in relation to the jog keys, refer to “[2.7.1 Jog Keys](jog-key.md).” 
{% endhint %}

# 2.7.3 Robot Coordinate System

| Joint Coordinate System | **Robot Coordinate System** | User Coordinate System | Tool Coordinate System |
| :---: | :---: | :---: | :---: |
|  ![](../../_assets/bt-crd2-joint-en.png)  | ![](../../_assets/bt-crd2-robot-en.png)  | ![](../../_assets/bt-crd2-user-en.png)  | ![](../../_assets/bt-crd2-tool-en.png)  |

1.	Turn on the motor in manual mode and hold the enabling switch on the back of the teach pendant.

2.	Select the robot coordinate system by repeatedly touching the \[Crd. Sys\] button on the right side of the Hi6 teach pendant screen. Then, the jog bar will display X, Y, Z, RX, RY, RZ, and additional axes.

3.	Operate the robot with the jog keys. The robot will move as follows.



![](../../_assets/image_62.png)

{% hint style="info" %}
* For details on the robot’s progress direction in relation to the jog keys, refer to “[2.7.1 Jog Keys](1-jog-key.md).” 
* 
  If you use your right hand, you can easily understand the operation of the robot in the robot coordinate system.

![](../../_assets/crd-direction.png) 

Figure 26 Coordinate System Direction \(Left\) / Rotation Direction \(Right\)

* If you put the progress direction of the right index finger in the X direction of the robot coordinate system, while you stand on the back of the robot, the progress direction of the thumb becomes the Z direction, and the progress direction of the middle finger becomes the Y direction.
* If you put the thumb of the right hand in the direction of the central axis of rotation, the direction of the other folded fingers becomes the + direction of the rotation direction.
{% endhint %}



# 2.7.4 User Coordinate System

| Joint Coordinate System | Robot Coordinate System | **User Coordinate System** | Tool Coordinate System |
| :---: | :---: | :---: | :---: |
|  ![](../../_assets/bt-crd2-joint-en.png)  | ![](../../_assets/bt-crd2-robot-en.png)  | ![](../../_assets/bt-crd2-user-en.png)  | ![](../../_assets/bt-crd2-tool-en.png)  |

1.	On the right side of the initial screen, touch the \[system\] button &gt; \[2: Control Parameter&gt; 7: Coordinate System Registration&gt; 1: User Coordinate System\] menu and then register the user coordinate system.

{% hint style="info" %}
For details on how to register the user coordinate system, refer to “[7.3.6.1 User Coordinate System](../../7-system/3-control-parameter/6-cordsys-reg/1-user-crdsys.md).”
{% endhint %}

2.	Touch the \[Speed Adjustment\] button at the top left of the initial screen and then set the coordinate system in the \[9: Select user coordinate\] option. You can choose the user coordinate system instead of the Cartesian coordinate system.

![](../../_assets/image_299.png)

3.	Operate the robot with the jog keys. The robot will move as follows.

![](../../_assets/image_103.png)

{% hint style="info" %}
For details on the robot’s progress direction in relation to the jog keys, refer to “[2.7.1 Jog Keys](1-jog-key.md).” 
{% endhint %}

# 2.7.5 Tool Coordinate System

| Joint Coordinate System | Robot Coordinate System | User Coordinate System | **Tool Coordinate System** |
| :---: | :---: | :---: | :---: |
|  ![](../../_assets/bt-crd2-joint-en.png)  | ![](../../_assets/bt-crd2-robot-en.png)  | ![](../../_assets/bt-crd2-user-en.png)  | ![](../../_assets/bt-crd2-tool-en.png)  |

1.	Turn on the motor in manual mode and hold the enabling switch on the back of the teach pendant.

2.	Select the tool coordinate system by repeatedly touching the \[Crd. Sys\] button on the right side of the Hi6 teach pendant screen. Then, the jog bar will display X, Y, Z, RX, RY, RZ, and additional axes.

3.	Operate the robot with the jog keys. The robot will move as follows.

* If a torch is attached to the robot

![](../../_assets/image_68.png)



* If no torch is attached to the robot

![](../../_assets/image_92.png)

{% hint style="info" %}
For details on the robot’s progress direction in relation to the jog keys, refer to “[2.7.1 Jog Keys](1-jog-key.md).”
{% endhint %}

# 2.8 Optimization of the Axis Origin and Tool Length

You can make it possible for the axis integer and tool length to be automatically set to improve the accuracy of the linear interpolation trajectory and coordinate shifting.

* You can make it possible for the distance to the tooltip, which is difficult to measure in 3D, to be automatically set. The parameters to be calibrated are the axis origins of the H, V, R2, and B axes and the tool length in the X, Y, and Z directions.
* You can perform “optimization of axis origin and tool length” and of “tool length.”

{% hint style="warning" %}
You should optimize the “axis origin and tool length” before teaching the robot program. If the “axis origin and tool length” is optimized while a robot program has been created already, the position in the existing program may change.
{% endhint %}

The following shows how to set the optimization of the axis origin and tool length:

1.	Set the operation mode to manual mode using the mode switch on the teach pendant.

2.	After touching the \[Prog\] button in the JOB program window, input the program number, and then touch the \[OK\] button.



![](../_assets/image_314.png)


3.	Press the &lt;motor&gt; key on the teach pendant, and then the motor lamp will blink.

* If the motor is not turned on, check the error message on the log bar and resolve the trouble.

4.	Operate the robot using the jog key while holding the enabling switch on the back of the teach pendant.

5.	Place a pointed needle at an arbitrary location within the operation range of the robot, and then match the tooltip of the robot to it. The distance from the front end of the robot to the matched tooltip will be optimized.

6.	Record the step by touching the \[Record\] button on the right side of the Hi6 teach pendant screen.

![](../_assets/image_316.png)


7.	Change the robot’s posture and repeat the above steps 5–6 more than four times.

* Change the robot’s posture using all six axes as much as possible. Moreover, change the axis angle by at least 30 degrees.

8.	Touch the \[system\] button &gt; \[6: Auto Calibration &gt; 1: Optimize axis origin and tool length\] menu.

![](../_assets/image_324.png)


9.	Set the program number, tool number, and step position error allowable range created for the automatic calibration, and then touch the \[Execute\] button. Then the selected axis origin and tool length will be set.

![](../_assets/image_330.png)

* You should select Tool Length in the \[Optimization Selection\] option, starting from the au/atic ca/tion of the second tool, when you use multiple tools. If you select Axis Origin and Tool Length, the previously set tool information will not match.

{% hint style="info" %}
For details on this function, refer to “[7.7.1 Optimization of Axis Origin and Tool Length](../7-system/7-auto-calibration/1-axis-origin-tool-length-optimization.md).”
{% endhint %}

# 2.9 Tool Data Automatic Calibration

After determining the axis origin and tool length through automatic calibration, etc., if the tool is deformed, you can simply determine new tool data. At this time, the axis origin should have been determined and maintained. In addition, a fixed reference point should be taught after the tool length is determined and the angle calibration is completed. If tool deformation occurs, place the tool in the same position at the reference point designated prior to the deformation, and then perform automatic tool data calibration.

1.	Touch the \[system\] button &gt; \[3: Robot Parameter&gt; 1: Tool Data\] menu.

![](../_assets/image_340.png)

2.	After touching the \[Auto Calibration\] button, move the tooltip to the original position using the jog key.

![](../_assets/image_341.png)

3.	 After checking the program number of the predetermined reference point, the step number, and the tool number, touch the \[Execute\] button.

![](../_assets/image_322.png)

{% hint style="info" %}
For details on this function, refer to “[7.4.1 Tool Data](../setting/robot-parameter/tool-data/).”
{% endhint %}

# 3. Program Writing

You can write and manage programs so that the robot can perform works and achieve the desired results.

# 3.1 Program Management

While the robot is stopped, you can create, modify, and delete programs.

1.	In the JOB program window, touch the \[Prog\] button. Then, the program selection window will appear.

![](../_assets/image_344.png)



2.	You can create, modify, and delete programs.

* To add a new program, touch the \[+\] button and then input the relevant contents by referring to “3.2 Program Writing.”

![](../_assets/image_353.png)

* To open a program to check and modify its contents, input the program number, or select a program from the list and then touch the \[OK\] button. Then, the selected program will be opened in the JOB program window.

![](../_assets/image_346.png)

* To delete a program, select the program from the list and touch the \[-\] button.

![](../_assets/image_357.png)

* You can delete a program from the file list \(\[Menu&gt; 5: File Management\]\). For details, refer to “[4.2 File Management](../menu/file-manager/).”
* You can quickly delete a program using the R code \(R117\). For details, refer to “[8.4 R117 for Deleting a Program](../8-r-code/4-r117.md).”





# 3.2 Program Writing

To get the desired result, you can write and edit a program consisting of various statements that instruct the robot to operate. You can write programs in manual mode.



# 3.2.1 Statements

A general program consists of a step command that instructs the robot to move and a function command that instructs the robot to carry out work after the movement.

A statement is largely divided into a command and a parameter, which is an additional item. The parameters are divided into default parameters essential for a statement and optional parameters that can be omitted.

![](../../_assets/image_82.png)



| No. | Description | No. | Description |
| :--- | :--- | :--- | :--- |
| ![](../../_assets/c1.png)  | Step number | ![](../../_assets/c3.png)  | Parameter |
| ![](../../_assets/c2.png)  | Command | ![](../../_assets/c4.png)  | Comment |

{% hint style="info" %}
For details on parameters, refer to “[2.3.1 Step Statement Parameters](../../operation/step/step-cmd-param/).”
{% endhint %}

When you input a statement, basic setting values will be automatically inputted into the default parameters and can be changed. Optional parameters are marked with a symbol \( \_ \), and you can input the parameter values by selecting the parameters. Moreover, parameters that can be inputted will be displayed as buttons on the right side of the screen.

![Figure 27 Editing a Command &#x2013; Inputting Parameter Values](../../_assets/image_355.png)

When editing the command parameters, you can edit variables, expressions, and strings by using the operation keys on the teach pendant and the menu buttons on the right side of the screen, or by using the soft keyboard.

# 3.2.2 Statement Inputting

# 3.2.2.1 General Statement Inputting

1.	In manual mode, touch the \[Command\] button on the right side of the initial screen. Then, the command inputting window will appear.

![](../../../_assets/image_349.png)

2.	Touch a statement group or input command and then select the command from the list. The statement will be inputted immediately below the current cursor position.

![](../../../_assets/image_358.png)

* In the case of command with multiple parameter forms, a check mark \(![](../../../_assets/icon-ok.png)\) will appear on the right. You can check and select the parameter form by touching the command in the list. 
* 
  For details on each statement, refer to the “[Hi6 Robot Language Function Manual](https://hrbook-hrc.web.app/#/view/doc-hrscript/english/README).”
# 3.2.2.2 Inputting of a Step Statement with a Hidden Pose

To input the current posture of the robot as a move command, touch the \[Record\] button on the right side of the Hi6 teach pendant screen.



![](../../../_assets/image_350.png)

When you input a command using the \[Record\] button, the pose variable will not appear in the step, unlike the general command inputting mode, so it is called a hidden pose.



# 3.2.2.3 Recording Condition

When a statement is inputted using the \[Record\] button, the current posture of the robot will be recorded as the target pose, and the value set in advance using the \[Rec.cond.\] button will be applied to the move command \(move\) parameter. The following shows the method of setting the recording condition of a statement.

1.	Touch the \[Rec.cond.\] button on the left side of the Hi6 teach pendant screen. Then, the recording condition setting window will appear.

![](../../../_assets/image_56.png)

2.	After setting the interpolation, moving speed and unit, accuracy, and tool number, touch the \[OK\] button \(![](../../../_assets/icon-ok.png)\).

![](../../../_assets/image_348.png)

* When position recording is performed, the move statement will be recorded based on the condition set in the recording condition.
* In the mechanism set, you can designate the configuration of the mechanism to be stored when position recording is performed.

If you briefly touch the \[mechsets\] button, the predefined mechanism set numbers will appear in sequence.

If you touch and hold the \[mechsets\] button, you can modify the existing set configuration in the Mechanism Set setting window, or add or delete a mechanism set by using the \[+\] or \[-\] button.

![](../../../_assets/image_351.png)





# 3.2.3 Statement Configuration

A statement consists of an address area and a statement area. 

![Figure 28 Areas Comprising a Statement](../../_assets/image_106.png)

| No. | Area | Description |
| :--- | :--- | :--- |
| ![](../../_assets/c1.png) | Address area | Displays the line number \(1 to 9999\) and step number \(S1 to S999\) |
| ![](../../_assets/c2.png) | Statement area | Displays a statement |

You can move the cursor position between the address area and the statement area by pressing the &lt;←/→&gt; key on the teach pendant. Pressing the &lt;↓/↑&gt; key will allow you to move the cursor up and down between the lines within the selected area.

![Figure 29 Moving the Cursor Between Areas \(Left: Address Area. Right: Statement Area\)](../../_assets/image_86.png)



# 3.2.4 Statement Editing

You can edit the statement in the JOB program window using the operation keys on the teach pendant and the menu buttons on the right side of the screen. Using the soft keyboard, you can edit variables, expressions, and strings.

In the statement area, you can check and edit statements by switching the status of the cursor according to the selected object.

* Statement cursor Status: You can check a statement while the entire line of the statement is selected.

![](../../../_assets/image_41.png)

* Word cursor Status: You can check and edit a statement while the individual parameters of the statement are selected.

![](../../../_assets/image_64.png)





# 3.2.4.1 Statement Editing Method

The following shows how to edit a statement.

1.	In the JOB program window, select the statement area by pressing the &lt;←/→&gt; key on the teach pendant. The statement area will be selected while in the statement cursor status.

2.	Press the <<b>ENTER</b>> key on the teach pendant while in the statement cursor status. Then, switching to the statement cursor status will occur and a parameter will be selected, and the selected parameter value will appear in the input area at the bottom.

3.	Edit the parameter value using the operation keys on the teach pendant and the menu buttons on the right side of the screen.

* Pressing the &lt;←/→&gt; key will allow you to move the cursor in the left or right direction between parameters
* Parameters that can be inputted will be displayed as buttons on the right side of the screen. You can easily input parameters by selecting the desired buttons.
* You can edit variables, expressions, and strings using the soft keyboard. 

4.	Press the <<b>ENTER</b>> key. Then, the contents of the change will be applied, allowing the parameter value of the statement to be changed and the cursor to move to the next parameter.

* To cancel the change, press the &lt;esc&gt; key.

5.	You can edit another parameter by repeating the above steps 2–3.

6.	Press the <<b>ENTER</b>> key to complete the editing. The changes will be saved in the JOB program, and the cursor will return to the statement cursor status.





# 3.2.4.2 Example of Statement Editing

With an example of changing the interpolation parameter from P \(joint interpolation\) to L \(linear interpolation\), the following describes how to edit a statement.

1.	Press the <<b>ENTER</b>> key on the teach pendant while in the statement cursor status. Then, the statement cursor will change to the word cursor status, allowing the P \(joint interpolation\), which is the interpolation parameter of the move statement, to be selected. In the input area, P, which is the current setting value of interpolation, will be displayed and the interpolation parameter that can be inputted will be displayed as buttons on the right side of the screen.

![](../../../_assets/image_51.png)

2.	Touch the \[L\] button among the buttons on the right side of the screen. Then, L \(linear interpolation\) will be displayed in the input area.

![](../../../_assets/image_59.png)

3.	Press the <<b>ENTER</b>> key. The interpolation parameter of the statement will change to L, and then the cursor will move to the next parameter, allowing the moving speed to be selected.

![](../../../_assets/image_69.png)

4.	Press the <<b>ENTER</b>> key to complete editing. The contents of the change will be saved in the JOB program, and then the cursor will return to the statement cursor status.



# 3.2.4.3 Line Number Editing Method

The line number can be set to any number between 1 and 9999.

1.	In the JOB program window, select the address area by pressing the &lt;←/→&gt; key on the teach pendant. Then, the address area will be selected.

* If the cursor is in the statement cursor status while in the statement area, press the &lt;←&gt; key to move the cursor to the address area.



![](../../../_assets/image_352.png)

2.	In the address area, select a line by pressing the &lt;↓/↑&gt; key and then edit the line number.

* To input a line number, input the line number in the input area using the number keys.



![](../../../_assets/image_356.png)

* To delete a line number, press the &lt;BS&gt; key. Then, the address value of the line number will be removed from the input area.


3.	Press the <<b>ENTER</b>> key to complete the editing. The contents of the change will be saved in the JOB program.
_assets
![](../../../_assets/image_67.png)



# 3.2.4.4 Soft Keyboard

You can easily input variables, expressions, and strings using the soft keyboard on the Hi6 teach pendant screen.

1.	Touch the \[ \] button on the log bar of the Hi6 teach pendant screen. Then, a soft keyboard will appear at the bottom of the screen.

2.	You can input variables, expressions, and strings in the input area using the soft keyboard. The existing parameter values will be removed, and the inputted texts will be displayed.

![](../../../_assets/image_78.png)

* If you touch the \[ / \] button on the left side of the input area, you can move the cursor position, allowing you to insert the text at the desired position.
* You can input numbers and special characters by touching the \[![](../../../_assets/bt-123.png)/![](../../../_assets/bt-symbol.png)\] button.
* 
  You can change the input language by touching the \[![](../../../_assets/bt-lang.png)\] button.

* 
  You can input a capital letter or a symbol by touching the key while pressing the &lt;shift&gt; key on the teach pendant.

* 
  You can move the keyboard to the top of the screen by touching the \[![](../../../_assets/bt-dock-softkb.png)\] button.

3.	When you have finished editing the text, you can hide the soft keyboard by touching the \[![](../../../_assets/bt-softkb.png)\] button at the bottom right of the soft keyboard.





# 3.2.4.5 Block Editing Mode

You can copy, move, and delete a line or multiple lines of the program by designating it or them as a block.

1.	While pressing the &lt;shift&gt; key on the teach pendant, touch the \[Block Editing\] button on the right side of the JOB program window. Then, the block editing mode will be activated.

2.	Place the cursor on the desired line using the &lt;↓/↑&gt; keys on the teach pendant and then press the <<b>ENTER</b>> key. Then, the line on which the cursor is placed will be selected as the start line of the block.

![](../../../_assets/image_354.png)



3.	Move the cursor by turning the jog dial on the teach pendant. Then, the section from the start line to the line to which the cursor is moved to will be selected as a block.

![](../../../_assets/image_343.png)

4.	You can edit the statement in the area that is selected as a block using the function buttons on the right side of the screen.

![](../../../_assets/image_345.png)

* \[Cut\]: You can cut the area selected as a block and save it in the clipboard so that it can be pasted to another location.
* \[Copy\]: You can copy the area selected as a block and save it in the clipboard so that it can be pasted to another location.
* \[Paste\]: Paste the area saved in the clipboard to the desired location.

  To paste the statement saved in the clipboard, you should select the cursor position using the jog dial and then touch the \[Paste\] button. Then, the statement will be inputted into the line right below the current cursor position.

* 
  \[Delete\]: You can delete the selected area.

5.	When you complete editing a block, press the &lt;esc&gt; key on the teach pendant or touch the \[Close\] button on the right side of the screen to exit the block editing mode.





# 4. Menu

You can use the program’s various service function menus such as variable and file management.

# 4.1 Use of Menus

1.	In manual or automatic mode, touch the \[Menu\] button on the right side of the initial screen. Various service menus of the program will be displayed.

2.	Selecting the desired menu will enable you to manage files, programs, teach pendants, or to check the status of the robot system.

![](../_assets/image_394.png)



* \[5: File Manager\]: You can manage files in the main board’s internal memory, teach pendant, or removable storage device.
* \[6: Program Conversion\]: You can convert the data, such as the condition and location of the created program, by batch or individually.
* 
  \[7: System Diagnosis\]: You can check the status of the robot and controller and update the system version.

* 
  \[8: Date, time setting\]: You can set the date and time of the controller.





# 4.2 File Management


You can manage files in the main board’s internal memory, teach pendant, or removable storage device.

1.	Touch the \[5: File Manager\] menu. Then, a list of folders of each device and a list of files saved in the selected folder will appear.

2.	Check and manage the folder structure and saved files by device.
_assets
![](../../_assets/image_372.png)



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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>This is a list of folders in the main board&#x2019;s internal memory,
          teach pendant, and removable storage devices. You can check the folder
          structure.</p>
        <ul>
          <li>[_assets
            <img src="../../_assets/icon-mb.png" alt/>MAIN]: The files saved in the mainboard (M/B) will be used for the actual
            robot operation.</li>
          <li>[_assets
            <img src="../../_assets/icon-tp.png" alt/>TP] / [
            <img src="../../_assets/icon-usb.png" alt/>USB]: The teach pendant (T/P) and a removable storage device (USB) will
            be used for data_assets>[</b>
            <img src="../../_assets/icon-usb.png"
            alt/><b>USB]</b> folder will appear only when a removable storage device is
            connected to the teach pendant.</li>
          <li>You can move the cursor in the folder list by turning the jog dial on
            the teach pendant.</li>
          <li>If you select _assets
            <img src="../../_assets/icon-gt.png" alt/>] or [
            <img src="../../_assets/icon-wedge.png" alt/>] in the folder list and press the <b><<b>ENTER</b>></b> key, you can show
            or hide subfolders.</li>
          <li>When you select a folder, you can check the list of files saved in the
            folder.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">Shows the list of the files saved in the selected folder. You can check
        the name, size, last modified date, protected status, and additional information
        of each file.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">You can manage files and folders using the function buttons.</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* It is the same function as “R17 File Management” of R codes._assets
* When a removable storage device is connected to the teach pendant, the \[USB\] icon \(![](../../_assets/icon-usb2.png)\) will appear on the status bar of the Hi6 teach pendant screen.
{% endhint %}

{% hint style="warning" %}
Never remove the removable storage device from the teach pendant while performing operations such as copying or deleting files. Data may be corrupted.
{% endhint %}

# 4.2.1 File Management

Select one or multiple files to copy, move, or delete.

1.	Select a folder in the folder list using the jog dial on the teach pendant. A list of files saved in the selected folder will appear.

![](../../_assets/image_366.png)

2.	Select the desired file in the file list by touching it.

![](../../_assets/image_377.png)

* You can select multiple files one by one by touching each file while pressing the &lt;ctrl&gt; key.
* If you touch two files while pressing the &lt;shift&gt; key, you can select all files between the two files at once.
* If you touch the \[Select All\] button on the right side of the screen, you can select all files at once.

  Press the &lt;esc&gt; key to cancel the file selection.

3.	You can copy, move, or delete the selected file using the function buttons on the right side of the screen.

* \[Copy\]: Copy the selected file and save it in a temporary folder so that it can be pasted into another folder.
* \[Paste\]: You can paste the file saved in the clipboard to the desired folder. 
* \[Cut\]: You can cut the selected file and save it in a temporary folder so that it can be pasted into another folder. 
* \[Delete\]: You can delete the selected file. A protected file \(with the protection mark \(W\_\) in the attributes\) cannot be deleted.

4.	To paste a file into a folder, select the folder using the jog dial and then touch the \[Paste\] button. Then, the file will be pasted to the selected folder.

![](../../_assets/image_370.png)


If the selected folder has a file with a duplicate name, a duplication notification window will appear. Handle it by setting whether to overwrite it.
_assets
![](../../_assets/image_376.png)

* To delete a file, touch the \[Delete\] button, and then touch the \[ENTER\] button in the confirmation window.
_assets
![](../../_assets/image_395.png)

# 4.2.2 Renaming of a File and Folder

You can rename a file or folder. You can also rename multiple files or folders at once.

1.	Touch the desired file \(or folder\) in the file \(or folder\) list to select it, and then touch the \[Rename\] button on the right side of the screen.

_assets
![](../../_assets/image_81.png)

2.	Input the file \(or folder\) name in the input area.
_assets
![](../../_assets/image_393.png)

* You can input the number simply by using the operation keys on the teach pendant. \(&lt;←/→&gt; keys: For moving the cursor. Number keys: For inputting a number\)
* _assets
  To input a text including numbers, touch the \[ ![](../../_assets/bt-dock-softkb.png) \] button on the log bar to use the soft keyboard.

3.	Press the <<b>ENTER</b>> key. Then, the new name you inputted in the list will appear.

{% hint style="info" %}
* You can also rename a protected file.
* 
  Even if a file is renamed, the information such as size, modified date, and attributes will remain the same as before.

* 
  It is the same function as “R116 Program Number Change” of R codes.


{% endhint %}



# 4.2.3 Folder Management

You can delete a folder or add a new one.

# 4.2.3.1 Folder Deletion

1.	Select a folder in the folder list using the jog dial on the teach pendant and then touch the \[Delete\] button on the right side of the screen.

![](../../../_assets/image_373.png)

2.	In the confirmation window, touch the \[ENTER\] button. The selected folder and all files saved in it will be deleted.

![](../../../_assets/image_386.png)



# 4.2.3.2 Folder Creation

1.	Select a folder in the folder list using the jog dial of the teach pendant and then touch the \[New Folder\] button on the right side of the screen. Then, a new folder will be added under the selected folder.

![](../../../_assets/image_362.png)

2.	Input the name of the new folder and then press the <<b>ENTER</b>> key.

![](../../../_assets/image_304.png)

# 4.2.4 File Protection

Protect your important files by performing a setting that can make it impossible to change or delete a program.

1.	Select the file and touch the \[property\] button. Then, the attribute setting window will appear.

![](../../_assets/image_380.png)

2.	Check the file name and touch the \[Read Only\] checkbox to select it and then touch the \[OK\] button. A protection mark \(W\_\) will appear in the attributes of the file list.

![](../../_assets/image_238.png)



# 4.2.5 Data Backup

You can save the history of the memory buffer as a file, and back up the project \(project/\) and history \(log/\) folders.

1.	By using the jog dial on the teach pendant, select the folder where you want to save the backup data in the teach pendant \(T/P\) or removable storage device \(USB\) folder in the folder list.

![](../../_assets/image_388.png)

2.	While pressing the &lt;shift&gt; key, touch the \[Select all\] button at the right side of the screen. The data backup will start.

![](../../_assets/image_391.png)

3.	When data backup \(it will take about 30 seconds\) is completed, check the backup result in the notification window.

![](../../_assets/image_290.png)

# 4.2.6 Data Restoration

This function helps restore the project \(project/\) and history \(log/\) that are previously backed up.

1.	By using the teach pendant’s jog dial, select the project \(project/\) folder backed up in the teach pendant \(T/P\) or removable storage device \(USB\), and then touch the \[Copy\] button.



![](../../_assets/image_385.png)

2.	By using the teach pendant’s jog dial, select the \[MAIN\] folder in the folder list, and then touch the \[Paste\] button.

![](../../_assets/image_381.png)



3.	In the duplicate notification window, touch the checkbox for \[All\] to select it, and then touch the \[OK\] button. The backup data will be restored on the main board.

![](../../_assets/image_360.png)

4.	Turn the power of the controller back on.

# 4.3 Program Conversion

You can write a new program by modifying the conditions and location of the created program by batches or individually, or by shifting coordinates.

1.	Touch the \[6: Program Conversion\] menu. Then, the program conversion menu will appear. 

2.	Select the desired menu and then modify the program conditions and location, or write a new program.

![](../../_assets/image_359.png)

{% hint style="info" %}
During the startup of the robot, the use of the menus \[4: The reference coordinate system\], \[5: Coordinate transformation\], \[6: Mirror Image\], and \[7: Step Copy\] will be restricted.
{% endhint %}



# 4.3.1 Recording Condition

You can change and set the recording condition for a specific step of the program and then apply it to the existing program, or write a new program.

1.	Touch the \[6: Program Conversion &gt; 1: Record condition conversion\] menu. Then, the recording condition conversion setting window will appear.

2.	After setting the recording condition option, touch the \[OK\] button.

![](../../_assets/image_389.png)

* \[Source program\]/\[Target program\]: You can input the number of the original program \(Initial setting value: The currently selected program\) whose recording conditions you want to change and the number of the new program you want to save after the change of recording conditions. If you set the number of the target program to match the same number as that of the original program, the original program will be overwritten by and replaced with a new program.
* \[Start Step\]/\[End Step\]: You can set the range of the steps \(Initial setting value: 1/last step\) to which you will apply the change of recording conditions.
* \[Accuracy\], \[Tool\]: You can change the recording conditions.



# 4.3.2 Recording Speed Conversion

You can change the recording speed for a specific step of the program and apply it to the existing program, or create a new program.

1.	Touch the \[6: Program Conversion &gt; 2: Record speed conversion\] menu. Then, the recording speed conversion setting window will appear.

2.	After setting the recording speed option, touch the \[OK\] button.

![](../../_assets/image_398.png)

* \[Source program\]/\[Target program\]: You can input the number of the original program \(Initial setting value: The currently selected program\) whose recording speed you want to change and the number of the new program you want to save after the change of recording speed. If you set the number of the target program to match the same number as that of the original program, the original program will be overwritten by and replaced with a new program.
* \[Start Step\]/\[End Step\]: You can set the range of the steps \(Initial setting value: 1/last step\) to which you will apply the change of the recording speed.
* \[Method\]: You can set the method of designating the speed.
  * \[specify Speed\]: You can convert the recorded speeds by batch.
  * \[specify ratio\]: If the unit of the recorded speed and the unit of speed selected in the \[Unit\] option match with each other, the speed can be converted to a ratio against the recorded speed.
  * \[change unit\]: You can convert the unit of the recorded speed.
* \[Range\]: You can set the application section within the range of the steps of which recording speed you want to change.
* \[Unit\]: You can set the unit of speed. When the speed designation method is selected as \[specify ratio\], only those that match the unit of the speed recorded in the step will be converted to the percentage of the ratio.
* \[Speed\]: This will mean the ratio value if you select the \[specify ratio\] as the speed designation method.



# 4.3.3 Recording Position

You can change and set the coordinate system of the step position recorded as a hidden pose in a specific step of the program and apply it to the existing program or create a new program.

1.	Touch the \[6: Program Conversion &gt; 3: Record Pose conversion\] menu. Then the recording position conversion setting window will appear.

2.	After setting the recording position option, touch the \[OK\] button.

![](../../_assets/image_320.png)

* \[source program\]/\[Target program\]: You can input the number of the original program \(Initial setting value: The currently selected program\) of which recording position you want to change and the number of the new program you want to save after the change of recording position. If you set the number of the target program to match the same number as that of the original program, the original program will be overwritten by and replaced with a new program.
* \[Start Step\]/\[End Step\]: You can set the range of the steps \(Initial setting value: 1/last step\) to which you will apply the change of the recording position.
* \[Coord. System Format\]: You can select the coordinate system to shift the position data recorded in the step. If you select base, robot, tool, or user, the position data will be converted to Cartesian coordinate values, and if you select joint, the position data will be converted to axis angles.



# 4.3.4 Recording Coordinate System

You can change the coordinate system of the step position recorded as a hidden pose. You can check the coordinate system you have changed to by pressing the quick open button at the concerned step. During the startup of the robot, the use of the \[4: Transformation of the reference coordinate system\] menu will be restricted.

1.	Touch the \[6: Program Conversion &gt; 4: Transformation of the reference coordinate system\] menu. Then, the recording coordinate system shifting setting window will appear.

2.	After setting the recording coordinate system option, touch the \[OK\] button.

![](../../_assets/image_323.png)

* \[Source program\]/\[Target program\]: You can input the number of the original program \(Initial setting value: The currently selected program\) of which recording coordinate system you want to change and the number of the new program you want to save after the change of recording coordinate system. If you set the number of the target program to match the same number as that of the original program, the original program will be overwritten by and replaced with a new program.
* \[Start Step\]/\[End Step\]: You can set the range of the steps \(Initial setting value: 1/last step\) to which you will apply the change of the recording coordinate system.
* \[Coordinate System Format\]: You can select a coordinate system that you want to designate newly.



# 4.3.5 Coordinate Shifting

The coordinate shifting function is a function that enables you to create a program without additional teaching even if a workpiece of the same shape, as shown in Image 2, is placed at a different location after a program taught on the workpiece \(Image 1\).

![Figure 30 Coordinate Shifting](../../_assets/image_369.png)

It is required to have three reference points to use the coordinate shifting function. You can create Program A by marking three reference points on the workpiece at the initial position. After moving the position of the workpiece, write Program B using the previously marked three reference points.

![Figure 31 Coordinate Shifting Program](../../_assets/image_368.png)

{% hint style="info" %}
* The accuracy of the coordinate shifting program will be affected by the accuracy of teaching the three reference points in coordinate shifting. Perform teaching as accurately as possible for the three reference points.
* Set the distance between the three reference points as far as possible in coordinate shifting.
{% endhint %}

You can shift the existing program \(Program 1\) to a new program \(Program 2\) by calculating the coordinate shifting amount in three steps that are the basis of Program A and Program B.

![](../../_assets/image_315.png)



# 4.3.6 Mirror Image

You can write a program in which the position of the S axis and the posture of the wrist axis are symmetrical based on the Y-Z plane at the 0° position of the S axis of the robot.

This function is useful when instructing two robots on the left and right to perform the same operation, such as welding the body of a vehicle. First, teach an operation to one robot and then open the program of the taught operation and convert it into a mirror image. Then, a program symmetrical to the S axis will be written.

![Figure 32 Original Program \(Left\) / Program Converted Through Mirror Image \(Right\)](../../_assets/image_379.png)

{% hint style="info" %}
The mirror image function is not supported for collaborative robots.
{% endhint %}

The use of the \[6: Mirror Image\] menu will be restricted during the startup of the robot. The method to use the mirror image function is as follows.

1.	Touch the \[6: Program Conversion &gt; 6: Mirror Image\] menu. Then, the mirror image setting window will appear.

2.	After setting the mirror image conversion option, touch the \[OK\] button.

* \[Source program\]/\[Target program\]: You can set the number of the existing program and the number of the new program that is to be created through conversion using a mirror image.

![](../../_assets/image_194.png)



# 4.3.7 Step Copy

You can copy part of a program to another program or the same program. The functions recorded in the step will also be copied. During the startup of the robot, the use of the \[7: Step Copy\] menu will be restricted.

1.	Touch the \[6: Program Conversion &gt; 7: Step Copy\] menu. The step copying setting window will appear.

2.	After setting the step copying option, touch the \[OK\] button.

![](../../../_assets/image_221.png)

* \[Source program\]/\[Target program\]: You can set the number of the original program of which you want to copy the step and the number of the new program that you want to create by pasting the copied step. If you set the target program number as the same number as the original program number, the original program will be overwritten by and replaced with the new program.
* \[Start Step\]/\[End Step\]: You can set the range of steps that you want to copy \(Initial setting value: 1/last step\).
* \[Insert Step\]: You can set the reference step to which you want to paste the copied step. The copied step will be pasted right after the reference step.
* \[Copy Method\]: You can select the progress direction of the copied step.
  * \[Forward/Inverse\]: You can paste the copied steps in the same order as the original program or the reverse order of the original program.

{% hint style="info" %}
* You cannot copy a protected program.
* If the END function is recorded in the copied step, the function will be copied together. Delete the function when necessary.
* If a function that makes it possible to jump \(GOTO, GOSUB\) to a step outside the copied range is recorded in the copied step, the function will be copied, but the number will not be changed automatically. Please change the number after copying.
{% endhint %}



# 4.3.7.1 Example of Step Copy

You can copy the steps 2–5 of the program 1 to step 2 of the program 2 \(set as the input step\) in the right and reverse directions.

The steps 2–5 of the original program \(program 1\) will be inserted right after the input step \(step 2\) of the target program \(program 2\) in the right direction \(same order as the original program\) or in the reverse direction \(reverse order of the original program\).

![](../../../_assets/image_321.png)



# 4.4 System Diagnosis

You can inspect and manage the state of the robot and controller. You can check and update the version of each module of the controller.

# 4.4.1 System Version

1.	Touch the \[7: System Diagnosis &gt; 1: System version\] menu. Then, the system environment setting window will appear.

2.	Check and manage the system environment \(software version\) information of the robot and controller.

![](../../../_assets/image_390.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">System environment (software version) information of the robot and controller</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Edit and manage the system environment using the function buttons.</p>
        <ul>
          <li>[OK]: You can save the contents of the change.</li>
          <li>[Ver. Up]: You can update the version of each module of the controller.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>



# 4.4.1.1 Controller System Updating

You can update the version of each module of the controller using the integrated compressed file.

1.	Connect the removable storage device containing the integrated compressed file to the USB slot of the teach pendant. When the removable storage device is connected to the teach pendant, the \[USB\] icon \(![](../../../_assets/icon-usb2.png)\) will appear in the status bar.

2.	Touch the \[Ver. Up\] button on the right side of the system environment setting window. Then, the version upgrade program execution window will appear.

3.	Select the \[Version Up\] mode by touching the drop-down menu, select the integrated compressed file using the \[Open\] button, and then touch the \[OK\] button.

![](../../../_assets/image_311.png)



4.	After selecting the module that you want to update, touch the \[OK\] button. Then, the update will start.

![](../../../_assets/image_255.png)

5.	When the update is completed, touch the \[OK\] button. Then, the version upgrade program execution window will be closed, and the controller will automatically restart.

![](../../../_assets/image_367.png)

# 4.5 Setting of Date and Time

You can set the date and time of the controller.

1.	Touch the \[8: Date, time setting\] menu. The date and time setting window will appear.

2.	After setting the date and time information, touch the \[OK\] button.

![](../_assets/image_361.png)



* You can perform setting by inputting the date and time by using the operation keys on the teach pendant.
  * 
    If you press the arrow keys, the cursor will move between the date and time items \(year/month/day/hour/minute/second/a.m./p.m.\).

  * 
    You can input a number by pressing the number keys. You can also adjust the value using the &lt;shift+↑/↓&gt; keys.
* Set the date on the calendar. Touch the \[◁/▷\] button to select the year and month and then touch the date.





# 5. Condition Setting

You can simply change the operation conditions without modifying the program. The changed setting values will remain the same even if the controller is restarted.

# 5.1 Operation Condition Setting

1.	Touch the \[Speed Adjustment\] button on the upper left on the initial screen. Then, the operation conditions setting window will appear.

![](../_assets/image_365.png)

{% hint style="info" %}
On the \[Speed Adjustment\] button, the speed limit \(mm/sec\) will be displayed while in manual mode, and the playback speed \(%\) will be displayed in automatic mode.
{% endhint %}



2.	Change the operation condition setting values by repeating the following procedure, and then touch the \[OK\] button.

![](../_assets/image_371.png)

a.	Turn the jog dial on the teach pendant. Then, the cursor will move.

b.	Turn the jog dial to select the desired option, or press the numeric keys to input a number.

c.	Press the <<b>ENTER</b>> key. Then, the contents of the change will be applied, causing the setting value to be changed, and then the cursor will move to the next item.



# 5.2 Information of Operation Conditions Setting



* \[1: Operation cycle type\]: You can set whether to repeat the program that will be executed during automatic operation. It can also be set while the robot is starting up, and the setting value will not be applied during manual operation.
  * 
    1 Cycle: The job program will operate once and then stop. When the program END is reached, the robot will stop.

  * Continuous: The job program will operate continuously and repeatedly. If there is an external stop operation, the robot will stop.
* 
  \[2: Step FWD/BWD maximum speed\]: You can set the speed limit for a step forward/backward. For details on this option, refer to ???[2.1 Manual Operation](../operation/manual-operation/).???

* 
  \[3: Function execution during Step FWD\]: You can set the execution option \(mode\) of the function recorded in the job program while in the step forward operation.

  * 
    Off: Only END recorded in the job program will be executed. All other functions except for END will not be executed.

  * 
    On: All functions recorded in the job program will be executed.

  * 
    1 On: Only the input signal wait function and program END function will be executed.



{% hint style="warning" %}
While in the step backward operation, only the input wait signal function will be executed, and all other functions will not be executed.
{% endhint %}

* \[4: Re-execution of the function after step backward and forward\]: You can perform setting in a way that the previously executed functions among the functions recorded in the job program can be executed again when in the step forward operation again after the step backward operation.
* 
  \[5: Path recovery during step FWD/BWD\]: You can set the mode of executing path recovery when in the step forward/backward operation.

  * Disable: Will not execute path recovery
  * Enable: Will execute path recovery without confirming with the user whether to execute path recovery

* 
  \[6: Playback speed rate\]: You can set the operation speed \(%\) of the robot for playback of a program in automatic mode. It does not refer to changing the speed recorded in the step of the job program, but it refers to changing the ratio, ranging from 1% to 100% of the robot??�s moving speed against the speed recorded in the step in batch.




{% hint style="info" %}
If a low-speed command is inputted through an external input during automatic operation, the automatic operation speed ratio will not be applied, but the manual maximum speed \(250 mm/s\) will be applied.
{% endhint %}

* \[7: Robot Lock\]: You can set the job program in a way that automatic operation is possible, without moving the robot. You can check the status of I/O with the peripheral devices, the soft limit, the cycle time, etc.
* \[8: Interpolation base\]: You can set a tool that will be the reference during the manual jogging of the robot. In general, a robot tool is used as an interpolation reference.
  * Robot Tool: Interpolation operation will be executed based on the tool attached to the front end of the robot.
  * 
    Stationary Tool: Interpolation will be executed based on the front end of the tool fixed to, for example, to the floor. If a stationary tool is selected as the interpolation reference, the tool number on the left side of the initial screen will be marked with ST0 \(![](../_assets/bt-st0s.png)\).




{% hint style="info" %}
If you select the stationary tool as the interpolation reference, you must set the stationary tool coordinate system. For details, refer to ???[7.3.6.2 Stationary Tool Coordinate System](../7-system/3-control-parameter/6-cordsys-reg/2-stationary-tool-crdsys.md).???
{% endhint %}

* \[9: Select user Coordinate System Designation\]: You can set the user coordinate system number \(0???10\) for Cartesian operation during manual jog operation. Then, the robot will operate based on the Cartesian coordinate system in the directions of X, Y, and Z axes of the designated user coordinate system, and the coordinate values of the user coordinate system selected during the monitoring of the pose will be displayed as X, Y, and Z coordinate values of the front end of the tool.



* 
  If 0 is set, the robot coordinate system icon \(![](../_assets/icon-crd-rob.png)\) will be displayed on the \[Coordinate System\] button on the right side of the screen. The operation based on the user coordinate system will be deactivated, and the operation and monitoring based on the Cartesian coordinates will be performed.

![](../_assets/image_126_en.png)

* If a number between 1 and 10 is set, the user coordinate system icon \(![](../_assets/icon-crd-user.png)\) will be displayed on the \[Coordinate System\] button. The coordinate values that are changed by using the &lt;Axis Operation&gt; key will be based on the user coordinate system.

![](../_assets/image_134_en.png)



{% hint style="info" %}
You can register the user coordinate system number in the \[system &gt; 2: Control Parameter &gt; 7: Coordinate System Registration &gt;1: User Coordinate System\].
{% endhint %}







# 6. Monitoring

You can check the status of the robot system and various data of the controller.

# 6.1 Use of the Monitoring Function

1.	Touch the \[+\] button at the top right of the panel stack in the work area. The panel selection window will appear.

![](../_assets/image_384.png)

2.	?��?�� ?��?��창에?�� ?��?��?�� 모니?���? ?��목을 ?��?��?��?�� 로봇 ?��?��?��?�� ?��?��??? ?��?��기의 각종 ?��?��?���? ?��?��?��?��?��?��.

![](../_assets/image_383.png)

{% hint style="info" %}
* All items that can be monitored will be displayed on the panel selection window.
* 
  The items that can be monitored will be displayed differently depending on the setting of the controller.

* 
  For details on how to use the panel stack and window of the work area, refer to ???[1.2.4.5 Work area](../1-robot-system/2-basic-usage/4-screen-of-the-hi6-tp/5-work-area.md).???
{% endhint %}







# 6.2 job

Touch \[JOB\] in the panel selection window. Then, the JOB program window will appear. You can check a program, and then edit or delete it or create one.

![Figure 33 JOB Program](../_assets/image_397.png)



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
      <td style="text-align:left">Displays the basic information and statement of a program. You can check
        and edit the details of the statement.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[Program]</b>: You can select or delete a program from the created
            program list.
            <br /><b>[&#x2026;]</b>: If the automatic indentation is applied incorrectly,
            the automatic indentation in the JOB program can be performed again.</li>
          <li>When a program is written, the parameter value of the selected statement
            will be displayed in the input area.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
For details on how to manage and write programs, refer to “[3 Program Writing](../programming/).”
{% endhint %}



# 6.3 Pose

Touch \[Pose\] in the panel selection window. Then, the robot pose information window will appear. You can check the current angle of each axis of the robot, the coordinate value of the tool center point \(TCP\), and the current value and command value of the encoder.

![Figure 34 Pose](../_assets/image_392.png)

# 6.4 System Input

In the panel selection window, touch \[System Input\]. Then, the input signal window will appear. 

You can check the status of signals related to the robot operation and the status of the input signals preassigned to detect any abnormality that occurs to the robot and the controller.

![Figure 35 System Input - ON/OFF Status \(Left\) / Value Status \(Right\)](../_assets/image_387.png)

![Figure 36 System Input &#x2013; Sequence Status](../_assets/image_396.png)



* In the ON/OFF status and sequence status, the signals currently being inputted will be displayed in yellow.
* 
  In the sequence status, only the status of the controller sequence signals will be displayed.

* 
  \[ON/OFF\]/\[Value\]/\[Sequence\]: You can change the display mode of the input signal window by touching the radio button.





# 6.5    System Output

Touch \[System Output\] in the panel selection window. Then, the output signal window will appear.

You can check the signals related to the robot operation and check the status of brake control.



![Figure 37 System Output - ON/OFF Status \(Left\) / Value Status \(Right\)](../_assets/image_451.png)

![Figure 38 System Output &#x2013; Sequence Status](../_assets/image_416.png)

* In the ON/OFF status and sequence status, the signals currently being outputted will be displayed in yellow.
* In the sequence status, only the status of the controller sequence signals will be displayed.
* \[ON/OFF\]/\[Value\]/\[Sequence\]: You can change the display mode of the output signal window by touching the radio button.
* \[Manual output\]: You can force the output of the selected signals while in the ON/OFF and sequence status.



#### Manual Output

You can select the desired signal and force it to be outputted.

1.	You can set the display mode to the ON/OFF status or sequence status by touching the \[ON/OFF\] or \[Sequence\] radio button on the right side of the system output signal window. 

2.	Touch a signal to select it in the signal window, and then touch the \[Manual Output\] button.

![](../_assets/image_446.png)

3.	After checking the output conditions in the manual output confirmation window, touch the \[ENTER\] button.

![](../_assets/image_406.png)

| soN | =1/0 |
| :---: | :---: |
| N: Number of the signal to be outputted | Output status \(1: Output, 0: No output\) |


4.	Check the output status of the selected signal. The selected signal will be switched to the output status and displayed in yellow in the signal window.
_assets
![](../_assets/image_405.png)

# 6.6 Public Input

Touch \[public Input\] in the panel selection window. Then, the public input signal window will appear. 

You can check the status of public input signals that are inputted through the CNIN connector of the I/O board in the controller.

![Figure 39 Public Input Signal &#x2013; ON/OFF Status \(Left\) / Value Status \(Right\)](../_assets/image_411.png)

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
        <p>Displays the status of general input signals</p>
        <ul>
          <li>General input signals designated as the system&#x2019;s basic specifications
            or assigned by the user will be displayed <b>in bold</b>.</li>
          <li>The signals currently being inputted will be displayed in yellow.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[FB0]: You can select the FB block to monitor by touching the drop-down
            menu (FB0 - FB15). You can configure up to 16 I/O blocks, and 960 points
            of signals can be monitored in</li>
          <li><b>[ATTR.-APPLIED]</b>: You can check the checkbox to perform the setting
            in a way that the physical input values are to be displayed before passing
            through the positive/negative logic attributes. The basic setting (unchecked)
            is that the input logic value after passing through the positive/negative
            logic attributes will be displayed.</li>
          <li>[ON/OFF]/[Value]: You can change the signal display mode by touching the
            radio button.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* In the case of using signals, such as fieldbus signals, by mapping them using an embedded PLC, the On/Off status of the input signals may appear differently. 
* 
  The flow of the input signals is as follows.
{% endhint %}

![](../_assets/user-input-flow_en.png)

# 6.7 Public Output

Touch \[public Output\] in the panel selection window. Then, the public output signal window will appear. 

You can check the status of public output signals that are outputted through the CNOUT connector of the I/O board in the controller.

![Figure 40 Public Output Signal &#x2013; ON/OFF Status \(Left\) / Value Status \(Right\)](../_assets/image_444.png)

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
        <p>Displays the status of general output signals</p>
        <ul>
          <li>General output signals designated as the system&#x2019;s basic specifications
            or assigned by the user will be displayed <b>in bold</b>.</li>
          <li>The signals currently being outputted will be displayed in yellow.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[FB0]: You can select the FB block to monitor by touching the drop-down
            menu (FB0 - FB15). You can configure up to 16 I/O blocks, and 960 points
            of signals can be monitored using one block.</li>
          <li>[Manual Output]: You can force the selected signal to be outputted.</li>
          <li><b>[ATTR.-APPLIED]</b>: You can check the checkbox to perform the setting
            in a way that the physical input values are to be displayed before passing
            through the positive/negative logic attributes. The basic setting (unchecked)
            is that the input logic value after passing through the positive/negative
            logic attributes will be displayed.</li>
          <li>[ON/OFF]/[Value]: You can change the signal display mode by touching the
            radio button.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* In the case of using signals, such as fieldbus signals, by mapping them using an embedded PLC, the On/Off status of the output signals may appear differently. 
* 
  The flow of the output signals is as follows.
{% endhint %}

![](../_assets/user-input-flow_en.png)

#### 

#### Manual Output

You can select the desired signal and force it to be outputted.

1.	You can set the display mode to the ON/OFF status by touching the \[ON/OFF\] radio button on the right side of the general output signal window. 

2.	Touch a signal to select it in the signal window, and then touch the \[Manual Output\] button.

![](../_assets/image_437.png)


3.	After checking the output conditions in the manual output confirmation window, touch the \[ENTER\] button.
_assets
![](../_assets/image_463.png)

| FbN | doN | =1/0 |
| :---: | :---: | :---: |
| N: Number of the FB block to monitor | N: Number of the signal to output | Output status \(1: Output, 0: No output\) |

4.	Check the output status of the selected signal. The selected signal will be switched to the output status and displayed in yellow in the signal window.
_assets
![](../_assets/image_426.png)

# 6.8 Global Variables

You can check the global variables defined as global in the JOB program. You can also select and change a variable value.

1.	Execute the program that includes the global variables defined as global, and then touch the \[+\] button at the top right of the panel stack in the work area.

![](../_assets/image_455.png)

2.	In the panel selection window, touch \[Global Variable\]. Then, a list of global variables included in the program will appear in a new window.

![](../_assets/image_470.png)

3.	You can check the name, type, and value of a variable. You can also select and change the value of a variable.

![](../_assets/image_462.png)

# 6.9 Local Variables

You can check the local variables defined as var in the JOB program. You can also select and change a variable value.

1.	Execute the program that includes the local variables defined as var, and then touch the \[+\] button at the top right of the panel stack in the work area.

![](../_assets/image_453.png)

2.	In the panel selection window, touch \[Local Variable\]. Then, a list of local variables included in the program will appear in a new window.

![](../_assets/image_445.png)

3.	You can check the name, type, and value of a variable. You can also select and change the value of a variable.

![](../_assets/image_461.png)



# 6.10 Operation time

In the panel selection window, touch \[Operation time\]. Then, the controller’s operation information window will appear.

You can check the accumulated time and number of cycles for each operation of the controller created immediately after system initialization, power input, and the start of the recent cycle. You can initialize the operation information by touching the \[Clear\] button for each item at the bottom of the information.

![Figure 41 Operation information](../_assets/image_460.png)



The fol_assetse timing of reflection in accordance with the conditions of individual items.

![](../_assets/image_449.png)

# 6.11 Log

Touch \[Log\] in the panel selection window. Then, the log window will appear. 

You can check the logs of errors, warnings, notification, operations, operations by the user, I/O, and executions.

![Figure 42 Log](../_assets/image_458.png)

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
        <p>You can set the type of log to be displayed in the list. If you touch
          the button of the desired type, only the logs that match the type will
          appear in the list.</p>
        <ul>
          <li>[All]: You can check all types of logs.</li>
          <li>[+E]/[+W]: You can check the logs of errors or warnings.
            <br />When a trouble occurs in the robot system, you can check and record the
            contents of the trouble, the time of trouble occurrence, as well as the
            program number, step number, axis data, and input/output status at the
            time of the trouble occurrence, and then manage the log of troubles. This
            makes it possible to analyze the cause of trouble or refer to the log of
            troubles that occurred prior to system recovery.</li>
          <li>[+N]: You can check the log of notifications.</li>
          <li>[+ST]: You can check the log of robot operations.
            <br />When signals related to operation such as startup, stop, and mode change
            of the robot are inputted, the contents and time, as well as the program
            number, step number, axis data, and input/output status at the time of
            input, will be recorded. When the robot is repaired, you can refer to the
            log of the robot operation.</li>
          <li>[+P]: You can check the log of the status that will be periodically recorded.</li>
          <li>[+OP]: You can check the log of operation.</li>
          <li>[+IO]: You can check the log of the variation of the input and output
            signals.</li>
          <li>[+H]: You can check the log of the execution of the JOB program.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[num.]: You can adjust the number of logs (30, 100, 200, 500, or 1000)
            to be displayed in the list by touching the drop-down menu. If you select
            the number of logs, the latest logs as many as that number will be recalled
            and displayed on the screen.</li>
          <li>[
            <img src="../_assets/bt-menu.png" alt/>]: You can open the pop-up menu.</li>
          <li>Save as log file: You can save the latest logs of the memory buffer as
            a file.</li>
          <li>Clear log file: You can clear the logs in memory buffer and delete all
            the log files. (Deleted files cannot be restored.)</li>
          <li>[
            <img src="../_assets/bt-lock.png" alt/>]: You can turn off the notification for a new log. The log will not be
            updated, and the current status will be maintained until the lock icon
            is turned off.</li>
          <li>[
            <img src="../_assets/bt-trash.png" alt/>]: You can delete the log displayed on the screen.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">A list of the logs of selected types. You can check the detailed information
        of the logs for individual types.</td>
    </tr>
  </tbody>
</table>



# 6.12 History

In the panel selection window, touch \[History\]. The history window will appear. 

You can check the history as the execution history and time stamps of the job program will be outputted.



![Figure 43 History](../_assets/image_439.png)

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
        <ul>
          <li>[
            <img src="../_assets/bt-refresh.png" alt/>]: You can refresh the execution history.</li>
          <li>[
            <img src="../_assets/bt-lock.png" alt/>]: You can turn off the notification for a new history. The history will
            not be updated, and the current status will be maintained until the lock
            icon is turned off.</li>
          <li>[
            <img src="../_assets/bt-trash.png" alt/>]: You can clear the history displayed on the screen.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">This shows the execution history and time stamp of the job program. You
        can check the history of the executed job programs.</td>
    </tr>
  </tbody>
</table>

# 6.13 System Character

In the panel selection window, touch \[System character\]. Then, the system character window will appear. 

You can check all the various data of the robot system or only the data of a specific type of information.

![Figure 44 System character](../_assets/image_441.png)

| No. | Description |
| :--- | :--- |
| ![](../_assets/c1.png) | Displays the data of the robot system. You can check the detailed data of a specific type by selecting individual types of information shown above. |
| ![](../_assets/c2.png) | **\[Clear\]**: For the rest of the items except for the motion of each axis, you can initialize the maximum value of the system data by type. |

{% hint style="info" %}
System character monitoring function is only available in engineer mode.
{% endhint %}

{% hint style="warning" %}
* In Engineer Mode, the Engineer Mode icon \(![](../_assets/eng-mode.png)\) will blink on the status bar.
* Use caution as a serious problem may occur in the robot system if the setting is performed incorrectly.
{% endhint %}

### 

#### Initialization

You can initialize the maximum value of the data by selecting the type of information you want.

1.	Touch the \[Clear\] button at the bottom of the system properties window.

![](../_assets/image_420.png)

2.	Touch the type of information you want to initialize. Then, the maximum value of the selected item will be initialized.

![](../_assets/image_421.png)

# 6.14 Task monitor

In the panel selection window, touch \[Task monitor\]. Then, the task window will appear.

You can check the operation cycle and execution time information for each task.

![Figure 45 Task monitor](../_assets/image_422.png)

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
        <ul>
          <li><b>[Cycle Time]/[Execution Time]</b>: You can change the information type
            for each task.</li>
          <li><b>[Initialization]</b>: You can initialize the displayed information.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">Displays the operation cycle and execution time information for each task</td>
    </tr>
  </tbody>
</table>





# 6.15 Soft Keyboard

In the panel selection window, touch \[Soft Keyboard\]. Then, a soft keyboard window will appear. 

You can input variables, expressions, and strings, which include numbers, characters, symbols, and special symbols. For details on how to use the soft keyboard, refer to ???[3.2.4.4 Soft Keyboard](../3-programming/2-prog-edit/4-statement-edit/4-softkeyboard.md).???

![Figure 46 Soft Keyboard](../_assets/image_435.png)

# 6.16 workcell

In the panel selection window, touch \[Work Cell\]. Then, the robot’s current posture will appear on the 3D screen.

By setting the safety function of the collaborative robot, you can check the setting status of the operation area \(![](../_assets/c1.png)\), tool area \(![](../_assets/c2.png)\), tool direction restriction \(![](../_assets/c3.png)\), robot elbow area \(![](../_assets/c4.png)\), prohibited area \(![](../_assets/c5.png)\).



![Figure 47 Work Cell Monitoring](../_assets/image_430.png)

* Select the \[Upscale/Downscale\] icon \(![](../_assets/wc-zoom.png)\), \[Move\] icon \(![](../_assets/wc-pan.png)\), or \[Rotate\] icon \(![](../_assets/wc-rotate.png)\) at the bottom right of the 3D screen, and then drag the screen. Then, the camera will be adjusted.
* If the setting is changed, you can apply the new settings only after closing and reopening the workcell window.





# 6.17 Help

In the panel selection window, touch \[Help\]. Then, you can check the usage information of the Hi6 controller in the help window of the controller.

![Figure 48 Help](../_assets/image_448.png)

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
        <p>List of help provided in the controller</p>
        <ul>
          <li>[
            <img src="../_assets/icon-gt.png" alt/>]/[
            <img src="../_assets/icon-wedge.png" alt/>]: You can hide or display the subitems.</li>
          <li>[
            <img src="../_assets/icon-file.png" alt/>]: You can display the details of the selected item at the bottom.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">Displays the details of the item selected in the above list of help</td>
    </tr>
  </tbody>
</table>

# 6.18 Sensor Sync

Touch \[Sensor Sync\] in the panel selection window. Then, the sensor sync window will appear.

You can check the information related to the conveyor and press sync functions. The sensor sync function can be activated by setting the sync status as conveyor or press in the \[system&gt; 4: Application Parameter &gt; 4: Sensor Sync\] menu.

![Figure 49 Sensor Sync Monitoring](../_assets/image_418.png)

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
      <td style="text-align:left">Displays the information related to the conveyor and press sync functions
        of the selected sensor</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[Sensor #1]</b>: You can select a sensor to monitor by touching the
            drop-down menu.</li>
          <li><b>[Manual reset]</b>: You can manually delete various sensor-related
            data (encoder pulse, sensor position, sensor speed, workpiece entry count,
            sync playback status, etc.).</li>
          <li><b>[Limit Switch Operate]</b>: You can use this function when you input
            the l</li>
          <li><b>[Work Position Input]</b>: You can manually input the sensor position
            value (Linear: mm. Circular: deg).</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>



{% hint style="info" %}
For details on the sensor sync function, refer to the “Hi6 Sensor Sync Function Manual.”
{% endhint %}

# 6.19 Program reserve

In the panel selection window, touch \[Program reserve\]. Then, the scheduled program execution window will appear. 

When programs are scheduled through external signals and executed in the scheduled order, you can check and change the status in the list of scheduled programs.

![Figure 50 Program reserve](../_assets/image_433.png)

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
* The \[Program reserve\] item will not be activated if the \[Applied Register Count\] option in the \[Set Up &gt; 2: Control Parameter &gt; 8: Program reserve\] menu is set as disable.
* For details on the scheduled program execution, refer to the “Hi6 Controller Scheduled Program Execution Function Manual.”
{% endhint %}

# 7. Set Up

In the settings item, you can check and set the user information and various parameter information.

# 7.1 Use of the Menus in Settings

1.	In manual or automatic mode, touch the \[system\] button on the right side of the initial screen. Then, the program’s settings menus will be displayed.

![](../_assets/bt-setup-en.png)

2.	You can check and set the user information and various parameter information by selecting the desired menus.

![](../_assets/image_410.png)

* \[1: User Environment\]: You can check and set various user conditions.
* 
  \[2: Control Parameter\]: You can set various conditions of the controller and the input/output signals, communication information, robot ready OK signal condition, home position signal, and coordinate system.

* 
  \[3: Robot Parameter\]: You can set various data related to robot operation and information such as the origin of each axis and operation range.

* \[4: Application Parameter\]: You can check and set various parameters for using the robot’s application functions.
* 
  \[5: Initialize\]: You can perform the initial setting of the robot system. You can also initialize the serial encoder.

* 
  \[6: Auto Calibration\]: You can calibrate the robot’s axis origin, tool length, load mass, and base axis direction, etc. using the programs taught to use the robot correctly and also by using the movement that will automatically operate.





# 7.2 User Environment

You can check and set various user conditions. 

1.	Touch the \[1: User Environment\] menu. Then, the user environment setting window will appear.

2.	After setting the user environment, touch the \[OK\] button.

![](../_assets/image_459.png)

* \[1: Pose Record Type\]: You can set the type of the position recording of the step to be recorded as a hidden pose.
  * 
    \[Base\]/\[Robot\]/\[Axis Angle\]: You can record the position of the step based on the base coordinate, robot, and axis angle values.

  * 
    \[U\]: You can record the position in the user coordinate system.
* 
  \[Confirm Delete  Command\] You can set whether to expose the deletion confirmation window when deleting a statement in manual mode.

* \[3: WAIT\(DI/WI\) release\]: While in the input signal wait or welding complete signal wait status, you can set whether to force the signal wait status to be deactivated using the &lt;shift+F3: Wait Deactivation &gt; keys.
* 
  \[4: Program Strobe Signal Use\]: When selecting an external program by receiving an external digital signal, you can set the time when the external program is to be selected.

  * 
    \[Disable\]: Makes it possible to select an external program by reading only the external program selection signal

  * 
    \[Enable\]: Makes it possible to select an external program by reading the external program selection signal at the time when the program strobe sognal is inputted

* 
  \[5: Ext. Update of Playback Prog.\]: You can set whether to allow the process of externally \(PC\) modifying the program that is being played back, and then to allow the process of downloading it to the controller \(With regard to the number of the program being played back, the downloaded program will be applied from the next cycle\).



{% hint style="warning" %}
If the program being played back is modified externally \(PC\) and downloaded to the controller, it could cause a failure of or abnormality with the product. Contact our customer support team to ask an expert or an engineer.
{% endhint %}

* \[6: Collision Sensor\]: You can set a method of stopping the robot when the collision sensor is operating.
  * 
    \[\(1\) Sensor\]: When the collision sensor is operating, this function will switch the robot into the emergency stop ready off \(motor off\) status or stop the robot \(operation ready on \(motor on\) status\).

  * 
    \[\(2\) Signal Logic\]: You can set the input signal logic of the collision sensor as positive logic or negative logic.



{% hint style="info" %}
* If you enter the \[system\] menu while the motor is turned off because of the operation of the collision sensor, the motor ON and jog operations can be performed. This function can be used to move the robot that suffered a collision.
* If the collision sensor operates while \[Sensor\] is set as stop, the robot can perform only jogging.
{% endhint %}

* \[7: cpo\( \) coordinate System\]: You can set the reference of the coordinate system of the pose that is to be acquired when the pose expression \(cpo\(\)\) that makes it possible to acquire the current robot pose in the job program is used.
* 
  \[8:cpo\( \) Selection\]: You can set the type of the current position value that is to be acquired when a pose expression \(cpo\(\)\) that makes it possible to acquire the current position of the robot based on the coordinate system \(U/Base/Joint\) designated in the job program. You can select the command value \(robot’s command value \(cmd\)\) or the current value \(robot’s current value \(cur\)\).

{% hint style="warning" %}
There may be an error between the robot’s current value and the robot’s command value because of servo delay. Set the type of the current position value according to the environment and purpose of the use.
{% endhint %}

* \[9: Manual Oper. for Stop Signal Input\]: You can set whether to enable jog operation when an external stop signal is inputted.

# 7.3 Control Parameter

You can set various conditions of the controller and set the input/output signal, communication information, robot ready OK signal condition, home position signal, and the coordinate system.

1.	Touch the \[2: Control Parameter\] menu. Then, the control parameter menu will appear. 

2.	Select the desired menu and check and set various conditions of the controller.

![](../../_assets/image_447.png)

# 7.3.1 Control Environment Setting

You can set various conditions of the controller and perform necessary operations.

1.	Touch the \[2: Control Parameter &gt; 1: Control Environment Setting\] menu.

2.	After setting the control environment conditions of the controller, touch the \[OK\] button.

![](../../_assets/image_471.png)

* \[1: Power Saving Function\]: You can set whether to use the power saving function and set the wait time.

While the power saving function is used, if the robot is in operation stop status while in the auto mode for a long period, such as waiting for startup or waiting for an input signal, the power supply to the motor will be cut off when the wait time has expired, helping save power consumption. When an operation command is inputted in the robot, the power saving function will be automatically deactivated, allowing the power to be supplied to the motor and the robot to operate.



{% hint style="info" %}
Delays may occur in the process of activating/deactivating the power-saving function. When operating while expecting the speed of the robot, you should set the power saving function as disable.
{% endhint %}

* \[2: Path Recovery on Auto Mode\]: You can set the allowable distance and allowable angle for path recovery in automatic mode.

  During path recovery, an error will be detected if the distance and angle exceed the set allowable range. If the allowable distance is set to 1, no path recovery will take place.





# 7.3.2 Input/Output Signal Setting

1.	Touch the \[2: Control Parameter &gt; 2: Input/Output Signal Setting\] menu. Then, the input/output signal setting menu will appear.

2.	Select the desired menu and set the input/output signal attributes and signal assignment, etc.

![](../../../_assets/image_443.png)

# 7.3.2.1 Input Signal Attribute

You can set the logic and name for a general input signal.

1.	Touch the \[2: Control Parameter &gt; 2: Input/Output Signal Setting &gt; 1: Input Signal Attribute\] menu. 

2.	Check and set the general input signal list, and then touch the \[OK\] button.

![](../../../_assets/image_425.png)

* \[Append\]: You can add a new general input signal to the list. 
* \[Delete\]: You can delete the general input signal from the list.





# 7.3.2.2 Output Signal Attribute

You can set the logic, pulse, and name for a general input signal.

1.	Touch the \[2: Control Parameter &gt; 2: Input/Output Signal Setting &gt; 1: Output Signal Attribute\] menu. 

2.	Check and set the general input signal list, and then touch the \[OK\] button.

![](../../../_assets/image_440.png)

* \[Append\]: You can add a new general output signal to the list.
* \[Delete\]: You can delete the general output signal from the list.





# 7.3.2.3 Input/Output Signal Setting Information

* \[Signal\]: The signal to apply the attribute to. The fb block signal can be designated by inputting the block number, decimal point, and signal number in sequence.

  For example, if you want to designate the signal 35 of the block fb1, you can set it by inputting 1.35.

* 
  \[Negative Logic\]: The positive logic and negative logic of the general input/output signal are as follows.

![](../../../_assets/image_457.png)

* \[Pulse Count\]: Pulse count. This is the count of pulses. If it is set to a value between 1 and 100, pulse output will occur, and if set to 0, a delayed output will occur.
* 
  \[Pulse On\]/\[Pulse Off\]: This is the On status time and Off status time of the output signal when pulse output or delayed output occurs.

  The example of the pulse output according to the pulse attribute value is as follows.

* 
  Pulse output: Count: 3. On status time: 1 second. Off status time: 0.2 seconds

![](../../../_assets/image_468.png)



* Delayed output: Count: 0. On status time: 1 second. Off status time: 0.5 seconds

![](../../../_assets/image_464.png)

* \[Name\]: Name of the general input/output signal



# 7.3.2.4 Input Signal Assignment

You can remotely control the controller’s state or operation using the controller input signal. The method of assigning the input signal number in the remote-control item is as follows.

1.	Touch the \[2: Control Parameter &gt; 2: Input/Output Signal Setting &gt; 3: Input Signal Assign\] menu. 

2.	After inputting the input signal number in the remote control item, touch the \[OK\] button.

![](../../../_assets/image_408.png)

* \[Reset All\]: You can reset the numbers of the input signals assigned to all remote control items. 
* 
  \[Reset One\]: You can reset the number of the input signal assigned to the selected remote control item. 

* 
  \[Reset Channel\]: You can initialize the input channel for the set input signal. The channel consists of fb0 to fb9, and fb0 will be omitted in the display in the case of fb0.

* 
  \[S\]: You can designate the system signal when using the remote control as a system input signal. The system signal consists of “s+number,” which combines the letter s with the signal number. For example, you can set the system signal 49 as s49.





# 7.3.2.5 Input Signal Setting Information

#### Remote mode

When the mode switch of the teach pendant is selected to remote \(![](../../../_assets/sb-remote.png)\), the corresponding signal should be turned on for the remote mode to be selected. If the corresponding signal is turned off, the internal mode will be selected. In general, if the mode switch of the teach pendant is selected to be remote \(![](../../../_assets/sb-remote.png)\), the user wants to select the remote mode, which is why the basic value is set to 254, and the corresponding signal will be designated as negative logic in the input signal attribute.



#### Manual \(Teach\) mode

While the remote mode is selected, if the corresponding signal is turned on, you will be in a state in which the robot will be operated manually in remote mode. However, in general, there is no case of operating the robot in this state, and this mode is rarely used. 



#### Auto \(Playback\) mode 

While the remote mode is selected, if the corresponding signal is turned on, you will be in a state in which the robot will be operated automatically in remote mode. However, in general, if the mode switch of the teach pendant is selected to remote \(![](../../../_assets/sb-remote.png)\), the user wants to operate the robot automatically in remote mode, which is why the basic value is set to 255, and the corresponding signal will be designated as negative logic in the signal attribute.



#### External start

This is used to start the robot in remote auto mode.



#### External stop 

This is used to stop the robot in remote auto mode.



#### Selection of an external program 

When the robot is externally started up, the timing of reading the program selection bit and determining it as an external program depends on whether to use the strobe signal.

* When the program strobe signal use is set as enable: If the program strobe signal is on while there is an external startup input, the program selection bit will be read, and the read value will be determined as the program number.

![Figure 51 Diagram of the Selection of an External Program When the Program Strobe Signal is Set as &amp;lt;Enable&amp;gt;](../../../_assets/image_438.png)

* When the program strobe signal use is set as disable: After there is an external startup input, the program selection bit will be read, and if this value does not change for 90 ms, it will be determined as the program number.

![](../../../_assets/image_465.png)

#### 

#### Program selection bit and binary/discrete \(off ?�� binary\)

The program selection bit is a combination of signals to select a program to execute when an external start signal is inputted. It is applied only when a step is pointed in Header or in the End currently in the TP. When a program is being executed, the program will be executed to the end.

Binary/Discrete signal is an option that determines the interpretation of the program selection bit, and if it is 0, it will be recognized as binary, and if it is 1, it will be recognized as discrete.

For example, if the program selection bit is set as follows, an example of JOB to execute according to the input is as follows.

![](../../../_assets/image_436.png)

#### 

#### External reset

This function is used to perform the same operation as executing the R0 step counter reset function from the teach pendant by an external signal. When the robot is starting up, this function will not operate. If this function operates normally, the execution position will move to the beginning of the program, and the occurrence status of various errors or warnings will be cleared. Refer to ???[8.2 R0 for Resetting the Step Counter](../../../8-r-code/2-r0.md)??? for information on this function.

#### 

#### Low speed command

This function is used to limit the robot??�s moving speed to within the safe speed \(250 mm/s\) by an external signal.



#### Collision sensor

This function is used to detect the collision of the robot and stop the robot. In conjunction with the settings in the \[System&gt; 1: User Environment&gt; 6: Collision Sensor\] menu, conditions and signal logic for stopping the robot will be determined.



#### Error/Warning signal clearing

This function is used to clear the occurrence status of various errors and warnings by an external signal. 

#### 

#### Joystick mode

This function is used to manually jog the robot. It is generally used in LCD macro inspection equipment. Refer to a separate function manual for using the function.



#### Door switch

This function is used to stop the robot in movement when the door of the safety fence is opened.



#### Screen saver deactivation

If the teach pendant is not operated, the teach pendant will switch to the screen saver state when the screen off time set in the \[Menu&gt; 11: Teach Pendant Option\] menu has elapsed. This function is used to turn on the screen of the teach pendant by an external signal.



#### External motor on

This function is used to turn on the motor from an external operation panel.



#### External motor off

This function is used to turn off the motor from an external operation panel.

# 7.3.2.6 Output Signal Assignment

Event information or status information that occurred in the controller can be transmitted to the outside through the controller output signal. The method of assigning output signals to the information to be transmitted to the outside is as follows.

1.	Touch the \[2: Control Parameter &gt; 2: Input/Output Signal Setting &gt; 4: Output Signal Assign-Main task\] menu. 

2.	After inputting the output signal number in the information item, touch the \[OK\] button.

![](../../../_assets/image_432.png)



* \[Reset All\]: You can reset the numbers of the output signals assigned to all information items.
*  \[Reset One\]: You can reset the number of the output signal assigned to the selected information item. 
* 
  \[Reset Channel\]: You can reset the input channel of the output signal assigned to the information item \(0–16: digital signal\)

* 
  \[Previous Task\]/\[Next Task\]: You can move to the previous or next task screen.

* 
  \[S\]: You can designate a system signal when using the remote control through a system input signal. The system signal is in the form of “s+number,” which combines the letter s with the signal number. For example, you can set the system signal 49 as s49.





# 7.3.2.7 Output Signal Setting Information

#### Remote mode

With the mode switch of the teach pendant selected to remote \(![](../../../_assets/sb-remote.png)\), the signal set in the input signal assign section should be inputted in the state of on in order to activate the remote state. This function is used to output the state to the outside. 



#### Manual \(Teach\) mode

This function is used to output the state to the outside that the operation mode of the controller is manual.



#### Auto \(Playback\) mode

This function is used to output the state to the outside that the operation mode of the controller is automatic.



#### Motor on 

When power is supplied to each motor by the input of the motor on signal and the driving is ready, this function is used to output the state to the outside.



#### Robot ready OK

When the current controller status satisfies all conditions set in the \[Set Up&gt; 2: Control Parameter&gt; 4: Robot Ready Condition\] menu, this function is used to output the state to the outside. 



#### Robot starting

When the robot is started by the step forward/backward operation in manual mode or by the input of the start signal in automatic mode, this function is used to output this state to the outside.



#### Robot moving

When the robot is moving, this function is used to output this state to the outside.



#### Robot stop \(Hold\)

When the robot is stopped, contrary to the output of the start signal, this function is used to output this state to the outside.



#### Emergency stop

When there is an input signal from the emergency stop button mounted on the front of the teach pendant or of the controller is inputted, this function is used to output the state to the outside.



#### Emergency stop \(External\)

This function is used to output to the outside the signal from an external emergency stop device connected to the system board. 



#### Low speed mode 

When the signal set for the low speed command in the input signal assign section is turned on or when the robot operates at a safe speed in manual mode, this function is used to output this state to the outside.



#### Program end 

When the end cycle is performed in the job program, this function is used to output this state to the outside.



#### Overall error

Errors occurring in the controller are divided into the errors caused by system errors and the errors caused by the user’s mistakes in operation. When an error occurs because of a system error, this function is used to output this state to the outside. The errors caused by system errors range from 1 to 999 and 2000 to 7999.



#### Operation error

Errors occurring in the controller are divided into the errors caused by system errors and the errors caused by the user’s mistakes in operation. When an error occurs because of the user’s mistakes in operation, this function is used to output this state to the outside. For information, the errors caused by system errors range from 1 to 999 and 2000 to 7999.



#### Warning

When a warning occurs in the controller, this function is used to output this state to the outside.



#### Collision sensor 

When the input of the collision sensor signal set in the input signal assign section is turned on and it is confirmed that a collision has occurred in the robot, this function is used to output this state to the outside.



#### Step set warning 

In automatic mode, it can be dangerous if the currently selected position of the cursor is different from the position in which the execution was performed previously. This function is used to output this state to the outside.



#### Interlock abnormal warning

When the waiting time in the wait statement of the job program exceeds the time set in the \[Interlock Abnormal Time\] option in the \[System&gt; 2: Control Parameter&gt; 1: Control Environment Setting\] menu, this function is used to output this state to the outside.

Error/Warning output bit, Error/Warning output selection and Error/Warning output strobe

For the error/warning output bit, error/warning output strobe, overall abnormality, operation error, and warning occurrence signals, refer to the following sequence.

![Figure 53 16Bit Output](../../../_assets/image_456.png)

#### External reset ack

When the external reset signal set in the input signal assign section is turned on, this function is used to output this state to the outside. This signal will be turned on for 200 ms and then turned off automatically.



#### Program echo bit 

When a program is selected by the program selection bit set in the input signal assign section, this function is used to output the selected program number to the outside. 



#### Program ack 

When the robot is started by an input of the external startup signal in remote mode, this function is used to output the state to the outside. The signal will be turned on for 200 ms and then turned off automatically.



#### Arc welding abnormal

When an error related to arc welding occurs, this function is used to output this status to the outside.



#### Arc deposition warning

When welding deposition occurs during arc welding, this function is used to output this state to the outside. This signal will be turned on for 200ms and then turned off automatically.



#### Robot lock state \(Valid=ON\)

This function is used to output to the outside the robot lock setting status in \[Condition Setting\].



#### Field bus abnormal, and field bus idle

When a fieldbus communication board such as CC-LINK and DeviceNet is used, this function is used to output the communication state to the outside.



#### Battery \(backup, encoder\) voltage drop

When there is a voltage drop in the backup battery to maintain the state of the SRAM installed on the main board or a voltage drop in the encoder battery to maintain the value of the encoder installed on each motor, this function is used to output to the outside.



#### Torque monitoring

This function is used to output to the outside the torque value that is applied to the six axes of the robot. The torque value that will be outputted to the outside is a % value in the multiplier of 1/2.



#### Grease injection alarm

This function is used to output to the outside the condition that requires grease injection.



#### Average load factor abnormality alarm 

This function is used to output to the outside the status regarding whether the robot has exceeded the average load factor during operation.





# 7.3.2.8 Key Signal Output

By assigning the output signal of the controller to the signal keys \(&lt;shift+F1 - F8&gt;\) of the teach pendant, you can perform setting in a way to turn on or output signal.

1.	Touch the \[2: Control Parameter &gt; 2: Input/Output Signal Setting &gt; 5: Key Signal Output\] menu. 

2.	Set the label, signal, and function to the manual output keys \(&lt;F1 - F8&gt;\) of the teach pendant, and then touch the \[OK\] button.

![](../../../_assets/image_469.png)



* \[fb\]/\[do\]: You can easily input the signal output variable value by using numbers and decimal point only.



For example, input 2.9 and press the <<b>ENTER</b>> key. Then, it will be converted to and displayed as fb2.do9. If you input 9 without decimal point and press the <<b>ENTER</b>> key, it will be converted to do9.

{% hint style="info" %}
You can register the desired output signal with a button in the user key area of Hi6 teach pendant. For details, refer to ???[2.6.2.1 Key Signal Output Function Area](../../../2-operation/7-user-key/2-button-registration/1-key-signal-output.md).???
{% endhint %}

# 7.3.2.9 DIO Block Allocation

You can set the method of using the controller’s general input/output signals. This function can be used through connection to None, PLC, or Fieldbus item.

1.	Touch the \[2: Control Parameter &gt; 2: Input/Output Signal Setting &gt; 6: DIO Block Allocation\] menu.

2.	Set the connection with the DIO block of the selected FB address, and then touch the \[OK\] button.

![](../../../_assets/image_434.png)



* \[None\]: The DIO block of the selected FB address will not be assigned. If nothing is selected as the initial setting value of the controller, the None item will be set.
* 
  \[PLC\]: The DIO block of the selected FB address will be connected to PLC for the use. For the PLC operation, MULTPROG program will be used.

* \[Fieldbus\]: The DIO block of the selected FB address will be connected to the PCI communication board \(Fieldbus\) for the use. If the DIO block is connected to the PCI communication card, the PCI board selection window will be activated.



{% hint style="info" %}
When using \[PLC\] and \[Fieldbus\] at the same time, please be careful not to overlap the slot number of the multiprog program and \[Fieldbus\].
{% endhint %}



# 7.3.2.10 Multiple Signal Output

Output signals \(up to 16 signals\) can be created as a group, and data can be outputted through individual signals.

The data is in binary format and determines whether the output will be on or off. For example, the data to print do41 and do43 on the screen shown below is 0101 in binary \(5 in decimal\).

1.	Touch the \[2: Control Parameter &gt; 2: Input/Output Signal Setting &gt;7: Multiple Signal Output\] menu

2.	Set the name, signals, and strobe of the output signal group. 

![](../../../_assets/image_452.png)





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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Detailed information on the group selected from the output signal group
          list. You can set the name, description, signal and strobe of the group.</p>
        <ul>
          <li><b>[Reset All]/[Reset One]:</b> You can reset the set value of all signals
            or of a selected signal to -1.</li>
          <li><b>[Reset Channel]:</b> You can reset the output channel of the set signal
            (0&#x2013;9: digital signals)</li>
          <li><b>[Set Range]</b>: You can quickly set the signal by designating the
            start and end signals.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[OK]:</b> You can save the edited content.</li>
          <li><b>[+]/[-]:</b> You can add a new output signal group or delete an output
            signal group.</li>
          <li>This shows a list of output signal groups. Selecting a group name allows
            you to view and edit details.</li>
          <li><b>[Copy Page/Paste Page]:</b> You can copy the output signal group information
            and paste it to another group.</li>
          <li>Select the name of the group to be copied from the list, touch the <b>[Copy Page]</b> button,
            select the name of the group to which the value is to be applied, and touch
            the <b>[Paste Page]</b> button.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

For example, when a job program configured as the setting in the screen above is executed, the operation will be as follows.

![Figure 54 Example of Job Program Execution](../../../_assets/image_429.png)

When the robot starts from S1 toward S2 and the accuracy of S2 is OK, the strobe signal will be outputted together with the signal of the designated group. The strobe signal will be turned off after 200 ms. \(The strobe signal is a pulse signal of 200 ms.\)

# 7.3.2.11 Multiple Signals Input

Input signals \(up to 16 signals\) can be created as a group, and data can be acquired through individual signals.

The data is in binary format and will be determined by the input on or off. For example, if di41 and di43 are on and all other signals are off, the data will be 0101 \(5 in decimal\).

1.	Touch the \[2: Control Parameter &gt; 2: Input/Output Signal Setting &gt; 8: Multiple Signal Input\] menu.

2.	Set the name, signals, and strobe of the input signal group.

![](../../../_assets/image_414.png)





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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Detailed information on the group selected from the input signal group
          list. You can set the name, description and signal of the group.</p>
        <ul>
          <li><b>[Reset All]</b>/<b>[Reset One]</b>: You can reset the set value of
            all signals or of a selected signal to -1.</li>
          <li><b>[Reset Channel]</b>: You can reset the input channel of the set signal
            (0&#x2013;9: digital signals)</li>
          <li><b>[Set Range]</b>: You can quickly set the signal by designating the
            start and end signals.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: You can save the edited content.</li>
          <li>[+]/[-]:You can add a new input signal group or delete an input signal
            group.</li>
          <li>This shows a list of input signal groups. Selecting a group name allows
            you to check and edit details.</li>
          <li><b>[Copy Page]</b>/<b>[Paste Page]: </b>You can copy the input signal
            group information and paste it to another group.
            <br />Select the name of the group to be copied from the list, touch the <b>[Copy Page]</b> button,
            select the name of the group to which the value is to be applied, and touch
            the <b>[Paste Page] </b>button.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

For example, when a job program configured as the setting in the screen above is executed, the operation will be as follows.

![Figure 55 Example of Job Program Execution](../../../_assets/image_407.png)

After starting from S1 toward S2, the robot executes the wait statement. If the wait condition is satisfied before the accuracy of S2 is ok, the robot will move to the path in red. If this is not the case, the robot will wait until the wait condition is satisfied.

# 7.3.3 Serial Port

You can set the information required for serial port communication.

1.	Touch the \[2: Control Parameter &gt; 3: Serial port\] menu.

2.	Set the parameters for each serial port.

![](../../_assets/image_412.png)



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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">Detailed information on the port selected from the serial port list. You
        can set the port name and parameter values.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[OK]</b>: You can save the changes.</li>
          <li><b>[+]/[-]</b>: You can add a new serial port or delete a serial port.</li>
          <li>A list of serial ports. Selecting a port name allows you to check and
            edit details.</li>
          <li><b>[Copy page]</b>/<b>[Paste page]: </b>You can copy the serial port information
            and paste it to another port.
            <br />Select the name of the port information to be copied from the list, touch
            the <b>[Copy page]</b> button, select the name of the port to which the value
            is to be applied, and touch the <b>[Paste page] </b>button.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
Refer to the following information when setting the usage of the serial port.

* Sensor: For receiving the shift data by accessing the vision sensor
* LVS: For connecting with the laser vision sensor for the weld line follow-up
* MODBUS: The MODBUS slave function of the Hi6 controller
{% endhint %}



# 7.3.4 Robot Ready Condition

When the robot ready is completed, set the conditions for signal output in the \[Robot Ready OK\] item of the \[system&gt; 2: Control Parameter &gt; 2: Input/Output Signal Setting &gt; 4: Output Signal Assign\] menu.

1.	Touch the \[2: Control Parameter &gt; 4: Robot Ready Condition\] menu. 

2.	After setting the robot ready condition, touch the \[OK\] button.

![](../../_assets/image_467.png)



# 7.3.5 Home Position Registration

By registering the robot’s arbitrary posture as the home position, you can allow the home position signal to be outputted to the output signal field when the robot enters this position. The home position can be designated based on the posture of each axis, and up to eight postures can be registered and used, and the margin for each axis can be additionally set.

1.	Touch the \[2: Control Parameter &gt; 5: Registration of Home Position\] menu.

2.	Select the home position tab, and then set the use, output signal, axis angle, and range.

![](../../_assets/image_466.png)



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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Detailed information on the home position selected in the tab. You can
          set the use, output signal, axis angle and range, and description.</p>
        <ul>
          <li>[Use]: You can set whether to use.</li>
          <li>[Output Signal]: You can input the output signal number.</li>
          <li>[Axis Angle]/[Range]: You can input the axis angle and range of the robot
            at the home position.</li>
          <li>If the range is set to 0, home position inspection will not be performed
            for the axis.</li>
          <li>The range refers to a range that covers the + direction and - direction
            of the home point. For example, if the range is set to 0.5, the output
            range of the home position signal will be 1.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[OK]</b>: You can save the changes.</li>
          <li><b>[Current Robot Pose]</b>: The axis angle and range of the current robot
            posture will be automatically inputted.</li>
          <li><b>[Program/Step]</b>: If you input the program and step number, the axis
            angle and range of the relevant step will be automatically inputted.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

# 7.3.6 Coordinate System Registration

1.	Touch the \[2: Control Parameter &gt; 6: Coordinate Registration\] menu. Then, the coordinate system registration menu will appear. 

2.	By selecting the desired menu, you can set the coordinate system with respect to the user coordinate system or the stationary tool coordinate system.

![](../../../_assets/image_401.png)



# 7.3.6.1 User Coordinate System

The user coordinate system is a coordinate system that is to be set at a position designated by the user. To use the user coordinate system, first, teach three reference steps that are needed to define the user coordinate system, and then register the user coordinate system by designating the taught program number and user coordinate system number.

Teach three reference steps by following the procedures below.

![Figure 56 Method of Teaching Three Reference Steps for Defining the User Coordinate System](../../../_assets/image_427.png)


1.	Define the origin of the user coordinate system: Teach an arbitrary point.

2.	Define the X axis in the user coordinate system: Teach an arbitrary point on the X-axis line in a way that the arbitrary point can be 200 mm as distant as possible from the origin.

3.	Define the XY plane in the user coordinate system \(determine the Y-axis and Z-axis directions\): Teach an arbitrary point on the plane consisting of the X axis and Y axis at the point where the distance from the origin is 200 mm or more as possible.

{% hint style="info" %}
* When the teaching of the user coordinate system setting program is performed, the TCP should be set to the correct values. Check whether the tool data of the currently selected tool is inputted correctly. 
* You can register up to 10 user coordinate systems.


{% endhint %}

{% hint style="warning" %}
The cautions in recording the reference points for defining the coordinate system are as follows.

* The reference 3 points should not exist on the same linear line.
* The distance between the reference 3 points should not be too close to each other.
* Subsequent steps after the XY plane in the user coordinate system is once defined will not have any effect on the coordinate system registration.
{% endhint %}

The method to register the user coordinate system by designating the taught program number and user coordinate system number is as follows.

1.	Touch the \[2: Control Parameter &gt; 6: Coordinate System Registration &gt; 1: User Coordinate System\] menu.

2.	Set the user coordinate system name and program number, and the distance and angle from each axis origin.
_assets
![](../../../_assets/image_442.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">No.</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align_assets
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">Detailed information on the coordinate system selected from the user coordinate
        system list. You can set the coordinate system name and description, the
        taught program number, and the distance and angle from each axis origin.</td>
    </tr>
    <tr>
      <td style="text-align_assets
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[OK]</b>: You can save the changes.</li>
          <li><b>[+]/[-]</b>: You can add a new user coordinate system or delete a user
            coordinate system.</li>
          <li>A list of user coordinate systems. Selecting the coordinate system name
            allows you to check and edit details.</li>
          <li><b>[Copy Page]/[Paste Page]</b>: You can copy the user coordinate system
            information and paste it into another coordinate system.
            <br />After selecting the name of the coordinate system information to be copied
            from the list, and then touching the <b>[Copy Page] </b>button, select the
            name of the coordinate system to which the value is to be applied, and
            then touch the <b>[Paste Page]</b> button.</li>
          <li><b>[Calc.from job]</b>: You can calculate the user coordinate system based
            on the taught program to define the user coordinate system.
            <br />If you touch the <b>[Calc. from job]</b> button after inputting the taught
            program number in the<b> [Job no.]</b> option, the origin and angle of the
            user coordinate system will be calculated.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

# 7.3.6.2 Stationary Tool Coordinate System

A robot tool is a tool attached to the front end of the robot. In general, robots perform operations using tools attached to the robot. A typical example is arc welding. The arc welding tool is usually attached to the front end of the robot and is used to perform welding on the externally fixed workpiece.

On the other hand, in the case of a stationary tool, the tool is attached to the outside, not the robot. In this case, the robot handles the workpiece and places it on an externally fixed tool to operate. A typical operation using a stationary tool is the sealing operation. Normally, in the sealing operation, when the external tool discharges a certain amount of solvent required for sealing, the robot holds the workpiece and creates the required trajectory to operate.

![Figure 57 Example of a Sealing Operation](../../../_assets/image_399.png)

To create the required trajectory, the robot performs linear \(L\) and circular \(C\) interpolations based on the externally attached tool, not based on the tool attached to itself. At this time, the stationary tool interpolation function will be used.

When the stationary tool interpolation function is used, even if the posture of the workpiece held by the robot is changed, the moving path of the stationary tool on the workpiece can maintain the linear lines and arcs. As such, the stationary tool interpolation function must always be used for an operation for which the moving path of the external tool is important.

To use the stationary tool interpolation function, you must set the stationary tool coordinate system. 

The method to set the stationary tool coordinate system is as follows.

1.	Touch the \[2: Control Parameter &gt; 6: Coordinate Registration 2: Stationary Tool Coordinate System\] menu.

2.	Select the desired tab and register the position of the stationary tool coordinate system. 

![](../../../_assets/image_402.png)



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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">You can set a total of four stationary tool coordinate systems (tool 0
        - tool 3) by selecting a tab.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: You can save the changes.</li>
          <li>[Auto Setting]: You can set the current TCP position as the position of
            the stationary tool coordinate system.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>



#### Setting the Current TCP Position as the Position of the Stationary Tool Coordinate System

After accurately finding the TCP based on the robot base coordinate system, you should match the stationary tool and the robot tool, as shown in the figure below, and then execute the automatic setting function using the \[Auto Setting\] button. Then, the current TCP position will be registered.

![Figure 58 Method of Teaching Using the \[Auto Setting\] Button](../../../_assets/image_415.png)



#### Writing a Program Using the Stationary Tool Coordinate System

To perform the recording for the stationary tool interpolation step, you should record the step as SL or SC. Using the \[Recording Condition\] button on the upper left of the Hi6 teach pendant screen, you can change the recording condition to SL \(stationary tool linear interpolation\) or SC \(stationary tool circular interpolation\).

For example, if you register and use the stationary tool coordinate system No. 1, you can create a program as follows.

![Figure 59 Example of Writing a Program When Using the Stationary Tool Coordinate System \#1](../../../_assets/image_404.png)

{% hint style="info" %}
In the case of using the stationary servo gun, the stationary tool interpolation function is not required. This is because, in the servo gun welding, the moving path of the workpiece for the stationary servo gun does not need to be formed in a linear line or arc while only the welding point is important.
{% endhint %}

# 7.3.7 Scheduled Program Execution

For details on how to execute scheduled programs, refer to the “Hi6 Controller Scheduled Program Execution Function Manual.”

# 7.3.8 Automatic Backup and Recovery

For details on how to automatically back up and recover the controller’s data, refer to the “Hi6 Controller Automatic Backup Function Manual.”

# 7.3.9 Industrial Communication \(fieldbus\)

You can perform the setting of the industrial communication \(fieldbus\) to use it.

1.	Depending on the type of the communication to use, you need to install a PCI card and then set the slot number \(1 to 4\) by referring to the “Hi6 Controller Maintenance Manual”.

2.	Set the industrial communication firmware by referring to “7.3.9.1 Firmware Setting”.

3.	Turn off the power of the controller, and then turn it back on.

4.	If necessary, carry out additional setting by referring to “7.3.9.2 Industrial Communication Setting”.





# 7.3.9.1 Firmware Setting

You can set the firmware to be used for the industrial communication.

1.	Touch the \[2: Control Parameter &gt; 11: Industrial Communication &gt; 1: Firmware Setting &gt; 1 Channel\] menu. Then, the firmware setting screen will appear.

2.	Select the desired tab and then set the communication method \(Master / Slave\) and protocol. After that, tap the \[OK\] button.

![](../../../_assets/image_419.png)



{% hint style="warning" %}
When the firmware setting is completed, the CONFIG files set in the slot \#1 - \#4 will be all deleted. When you want to change the communication firmware in the middle of using it, you should back up the existing CONFIG setting separately and use it after restoring it. 
{% endhint %}

3.	Turn off the power of the controller, and then turn it back on.

{% hint style="warning" %}
* When you perform the setting of the firmware to use it, the setting value will be applied to the system only after you turn off the power of the controller and then turn it back on.
{% endhint %}



# 7.3.9.2 Industrial Communication Setting

\(The function to be provided later\) If you set the communication method to CC-Link slave, you can set the detailed information for each type of communication inside the controller.

{% hint style="info" %}
You can set the communication information by using the “Sycon.net” program on the Hyundai Robotics internet website \(www.hyundai-robotics.com\).
{% endhint %}

# 7.3.9.3 Monitoring

You can monitor the setting information and operation status of the firmware and communication the use of which you have set in the industrial communication menu.

1.	Touch \[Menu\] button &gt; \[19: Industrial Communication Monitoring\] menu. Then the screen for monitoring the industrial communication of each board will appear.

2.	By selecting the desired tab, you can check the detailed information of the firmware, communication devices and communication configuration. 

![](../../../_assets/image_450.png)

{% hint style="info" %}
You can restart the industrial communication of the PCI communication card by using the \[Restart\] button.
{% endhint %}

# 7.4 Robot Parameters

You can set various data related to robot operation as well as information such as the origin and operation range of each axis.

1.	Touch the \[3: Robot Parameter\] menu. Then, the robot parameter menu will appear. 

2.	You can check and set various parameters of the manipulator by selecting the desired menu.

![](../../_assets/image_477.png)



# 7.4.1    Tool Data

You can set the distance and angle of the TCP based on the robot’s R1-axis flange and register the tool’s weight, center of gravity, and inertia. You can perform registration manually using the \[1: Tool data\] menu.

In another way, the tool length can be set using the automatic calibration function, and the tool’s weight, center of gravity, and inertia can be registered using the load estimation function.

In the case of interpolation operation such as linear or circular interpolation, the trajectory will be created based on the TCP, so the length and angle of the tool should be accurately set before the teaching.

The Hi6 controller performs control based on the dynamics of the robot. The robot can operate quickly and safely only when the weight, center, and inertia of the tool are correctly set. If the weight, center, and inertia values of the tool are incorrect or wrong, serious problems may occur in the performance and service life of the robot.

In particular, in the case of using the tool change function, all tool information related to tool change, not only the information about each tool, but also separate numbers assigned to disconnected tools, should be inputted for the use. Moreover, even during the handling operation, the attachment/detachment status of the workpiece should be assigned to each tool number for the use.

The length of the tool is the length in each direction in the flange coordinate system. \(Length in X-axis direction: Xt / Length in Y-axis direction: Yt / Length in Z-axis direction: Zt\)



![Figure 60 Flange Coordinate System for Each Robot Type](../../../_assets/image_213.png)

The angle of the tool is the posture conversion amount in each direction in the flange coordinate system. \(Angle in X-axis direction: Rx / Angle in Y-axis direction: Ry / Angle in Z-axis direction: Rz\)

![Figure 61 Tool Angle: Rotating Rx \(Left\) / Rotating Ry \(Middle\) / Rotating Rz \(Right\)](../../../_assets/image_211.png)

The length and angle of the tool will be set based on the flange coordinate system. The tool length can be set as the distance from the center of the flange coordinate system to the TCP.

The tool posture is a value acquired by performing rotation sequentially in the X, Y, and Z directions based on the tool flange coordinate system according to the tool angle set as above.

Rxyz = Rot\(z, Rz\)Rot\(y, Ry\)Rot\(x, Rx\)

* Rxyz: Tool posture rotation matrix based on the tool flange
* Rot\(z, Rz\): Rotation matrix that rotation occurs as much as Rz in the Z-axis direction of the flange coordinate system 
* Rot\(y, Ry\): Rotation matrix that rotation occurs as much as Ry in the Y-axis direction of the flange coordinate system
* Rot\(x, Rx\): Rotation matrix that rotation occurs as much as Rx in the X-axis direction of the flange coordinate system





# 7.4.1.1 Tool Data Setting


The manual method of setting the distance and angle of TCP based on the robot’s R1-axis flange and registering the tool’s weight, center of gravity, and inertia is as follows.

1.	Touch the \[3: Robot Parameter &gt; 1: Tool Data\] menu.

2.	Set the tool data name, weight, detailed conditions of each axis, and allowable ratio.
_assets
![](../../../_assets/image_480.png)





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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">Detailed information on the tool data selected from the tool data list.
        You can set the tool data name and description, weight, detailed conditions
        of each axis, and allowable ratio.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[Auto Calibration]</b>: You can create new tool data or can create
            tool data simply by using an existing program. If you want to perform setting
            newly at the previously taught step position, you should first place the
            tool, and then execute the automatic calibration function to create tool
            length and angle newly.
            <br />
            <img src="../../../_assets/tool-data-auto-calib-en.png" alt/>
            <br />
          </li>
          <li>[Previous Program Number]: You can input the program number taught before
            tool deformation occurs.</li>
          <li>[Previous Step Number]: You can input the step number for which automatic
            tool data calibration will be performed.</li>
          <li>[Tool Number to Set]: You can input the tool number to be newly set.</li>
          <li>
            <p>[Angle Calibration]: You can calibrate the angle of the tool.</p>
            <p>
              <img src="../../../_assets/tool-angle-auto-calib-en.png" alt/>
            </p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: You can save the changes.</li>
          <li>[+]/[-]: You can add new tool data or delete tool data.</li>
          <li>Tool data list. Selecting a tool data name will allow you to check and
            edit detailed information.</li>
          <li>[Copy page]/[Paste page]: You can copy the tool data information and then
            paste it to another tool data.
            <br />After selecting the name of the tool data information to be copied from
            the list and touching the<b> [Copy page] </b>button, select the name of
            the tool data to which the value is to be applied, and then touch the <b>[Paste page]</b> button.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* In the tool data list, tool data for which load estimation is not performed will be marked with \(X\) to the right side of the name.
* You must perform load estimation first before using the tool. The use of tools for which load estimation is not performed could cause trouble with the speed and durability of the robot.
* 
  When tool data is copied, the load estimation data will also be copied. The tool data copying and pasting functions can only be executed on the tab of the tool number for which load estimation has been performed.
{% endhint %}

# 7.4.1.2 Tool Data Setting Information

* \[Weight\]: Weight of the tool \(kg\)
* \[Length\]: Length of the tool \(mm\). You can set it using the automatic calibration function or the auto calibration.
* \[Angle\]: Angle of the tool \(deg\). You can set it using the automatic calibration function or the angle calibration function.
* \[Center\]: Position of the center of gravity of the tool based on the center of the flange \(mm\). You can set it using the load estimation function.
* \[Inertia\]: The moment of inertia \(kg/m2\) of the tool with respect to the tool coordinate. You can set it using the load estimation function.
* Allowable Ratio: \(Only for the robot models to which high-load mode is applied\) This is the ratio of the current setting against the allowable reference value. The robot operation, according to the allowable ratio, is as follows.

| Classification | Normal | High-load mode | Exception allowable mode | Playback impossible \(Large size\) |
| :--- | :--- | :--- | :--- | :--- |
| Weight ratio \(%\) | - 100 | 100–120 | 100–120 | 120 - |
| Moment ratio \(%\) | - 100 | 100–110 | 100–115 \(150\) | 115 \(150\) - |
| Inertia ratio \(%\) | - 100 | 100–130 | 100–150 \(600\) | 150 \(600\) - |

{% hint style="info" %}
The allowable ratio can be changed depending on the robot model and controller software version.
{% endhint %}



# 7.4.2 Axis Origin

You can register the mechanical origin position of each axis.

1.	Touch the \[3: Robot Parameter &gt; 2: Axis Origin\] menu.

2.	Register the mechanical origin position of each axis.

![](../../_assets/image_478.png)





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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Detailed information on the mechanical origin position of each axis. You
          can set the encoder and position of the axis.</p>
        <ul>
          <li>S-axis: You can change the S-axis origin depending on the installation
            situation of the robot and surrounding jig.</li>
          <li>R1-axis: You can change the origin of the R1- axis origin according to
            the tool attachment direction.</li>
          <li>H, V, R2, and B axes: Can be set automatically through the automatic calibration
            function</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: You can save the changes.</li>
          <li>[Apply One]: You can apply the selected origin position to the selected
            axis information.</li>
          <li>[Apply All]: You can apply the selected origin position to all axis information.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
* The axis origin setting affects the accuracy of the robot’s cartesian operation. Change it to the exact value as much as possible.
* 
  If the axis origin setting is changed, the position of the previously created program will be changed. Therefore, the axis origin setting must be executed only at the initial installation stage.

* 
  If the encoder offset setting is changed, the axis origin should be newly set. Therefore, the encoder offset setting must be completed before the setting of the axis origin.
{% endhint %}

{% hint style="info" %}
At the time of the shipping from the factory, the mechanical origin position of each axis is set at the standard value \(0X400000\).
{% endhint %}

# 7.4.3 Soft Limit

You can adjust the operation range of each axis according to the robot’s use environment.

1.	Touch the \[3: Robot Parameter &gt; 3. Soft Limit\] menu.

2.	Set the operation range of each axis.

![](../../_assets/image_486.png)



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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">Detailed information on the operation range of each axis. You can set
        the minimum and maximum operation ranges of an axis and the current axis
        position.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: You can save the changes.</li>
          <li>[Cur. Value]: You can set the operation range of each axis based on the
            current robot position.</li>
          <li>[Reset All]: You can initialize the operation range of all axes.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
At the time of the shipping from the factory, the operation range of each axis of the robot is set to a maximum. 
{% endhint %}

# 7.4.4 Encoder Offset

The current encoder position can be set as the encoder origin position \(position 0X400000\). You can determine the encoder origin at the reference position of each axis of the robot \(the position where the scale of each axis is attached\).

1.	Touch the \[3: Robot Parameter &gt; 4: Encoder Offset\] menu.

2.	Set the encoder offset value by adjusting the position of each axis. The encoder offset value will be recorded as a hex value \(a hexadecimal number\).

![](../../../_assets/image_472.png)



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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">Detailed information on the encoder offset value of each axis. You can
        set the calibrated encoder value, current encoder value, and current position
        of an axis.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: You can save the changes.</li>
          <li>[Reset One]/[Reset All]: You can initialize the encoder offset value of
            the selected or every axis.</li>
          <li>[Calculate Correction Value]: You can calibrate the encoder offset value
            of the selected axis.</li>
          <li>[Previous Correction Value]: You can retrieve the encoder offset value
            that existed prior to the calibration of the selected axis.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
The encoder offset value is set at the time of the shipping from the factory. Resetting the encoder offset value should be performed only when necessary, such as replacing the motor or encoder.
{% endhint %}

# 7.4.4.1 Encoder Offset Value Utilization

To continue using the existing program even after the current job program is backed up and the system is initialized \(\[system &gt; 5: Initialize&gt; 1: System Initialization\]\), the robot should maintain the reference position information that existed before initialization. If you record the encoder offset value, the previous position information of the robot can be retrieved.

After system initialization, directly input the encoder offset value as a hex value. It will be easy to input the value if you use the soft keyboard.

If the encoder offset value is recorded as the axis position value \(mm or degree\), you need to input the axis position value into the input window that will appear when you touch the \[Reset One\] button while pressing the &lt;Shift&gt; key.

![](../../../_assets/image_485.png)



{% hint style="info" %}
The basic setting value in the axis position input window is the reference position value. If you save without inputting the axis position value, the current encoder position will be set as the origin position \(0X400000\).
{% endhint %}

# 7.4.5 B-Axis Deadzone

Around 0 degree of the B-axis, the rotational center of the R1 axis and the rotational center axis of the R2 axis will be almost in parallel. When the TCP of the robot performs interpolation such as linear interpolation or circular interpolation, the wrist axis will move rapidly even in small movements.

Set the B-axis no-use area.

1.	Touch the \[3: Robot Parameter &gt; 5: B-axis Deadzone\] menu.

2.	After setting the angle for determining the no-use area and setting the interpolation handling mode, touch the \[OK\] button.

![](../../_assets/image_482.png)



* \[Setting Value\]: You can input the angle for determining the B-axis no-use area.
* 
  \[Dead zone interpolation\]: When the trajectory of the robot has to pass through the B-axis no-use area in interpolation operation, you can perform the setting regarding the handling of errors and stopping of the robot. 





# 7.4.6 Accuracy

You can set the detailed conditions of the accuracy level, which refers to the accuracy of passing through the step when the robot progresses the target step.

1.	Touch the \[3: Robot Parameter &gt; 6: Accuracy\] menu.

2.	Set the tooltip position \(TCP\) and posture for each accuracy level.

![](../../_assets/image_479.png)



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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Detailed information for each level. You can set the tooltip position
          (TCP) and posture for each accuracy level.</p>
        <ul>
          <li>The accuracy level can be set to a value from 0 to 7, and the accuracy
            level will be recorded as one of the step statement parameters.</li>
          <li>Accuracy level 0&#x2013;6: Input the TCP distance and posture, as well
            as the distance and angle of the additional axis, for each level.
            <br />For the robots that do not support linear or circular interpolation, such
            as LCD robots, the same method as for additional axes will be applied.</li>
          <li>Accuracy level 7: The value will be automatically calculated and displayed
            in the controller, so you do not need to input the value directly.
            <br />When the accuracy level 7 is applied, the maximum cornering path that
            satisfies the condition of 1/2 of the step distance will be created. Accuracy
            level 7 is useful when it is required to make the robot move as smoothly
            and quickly as possible, such as the act of LDC hand entering and exiting.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: You can save the changes.</li>
          <li>[Reset All]: You can initialize the TCP distance and posture for all accuracy
            levels.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* If you approach the accuracy level based on your understanding of the contents of “2.3 Step,” you can use it more easily.
* In the welding step that uses a servo gun or an equalizerless gun, the controller will automatically perform restriction regardless of the set accuracy level. 


{% endhint %}



# 7.4.7 Additional Weight of Each Axis

You can register information on a transformer or wiring support mounted on the basic axis of the robot.

1.	Touch the \[3: Robot Parameter &gt; 7: Additional Weight on Each Axis\] menu.

2.	Select the basic axis tab, set the information of the mounted additional weight, and then touch the \[OK\] button. 

![](../../../_assets/image_475.png)



{% hint style="warning" %}
If the robot has an additional weight because a transformer or wiring support is mounted onto it, you must register the information on the additional weight of each axis. If the additional weight is not correctly registered, the error may get large when the tool load estimation is performed.
{% endhint %}

# 7.4.7.1 Coordinate System Origin of Each Axis

The X, Y, and Z directions of each axis are set in the same direction as the robot coordinate system. Refer to the following about the coordinate system origin of each axis.

![Figure 62 Coordinate System Origin of Each Axis for Each Robot Configuration ](../../../_assets/image_476.png)

# 7.4.8 Collision Detection \(Function to Be Available Later\)

The Hi6 controller has the error detection function for overcurrent, overload, overspeed, position deviation, as well as the collision detection function, as safety functions in preparation for a case in which the robot operates under abnormal conditions or operates abnormally. These two functions will work with each other to enhance the safety of the robot.

In the Hi6 controller, a model-based collision detection function is provided. The model-based collision detection function detects a collision by calculating the difference between the torque that should be normally applied during the robot’s operation and the measured torque based on the dynamics model of the robot. By setting the sensitivity, you can adjust the responsiveness to the collision and make it possible to detect any contact with the outside that occurs when the robot moves at low speed.

However, the collision detection function detects the collision on the robot axis, so if the impact is not transmitted to the robot, the collision will not be detected. Moreover, the following are the points that require you to exercise precautions when using the collision detection function.

* The collision detection function will work only when the motor is turned on.
* You must execute load estimation before using the collision detection function.
* If the tool weight and the additional weight of each axis are different from the actual data, false detection may occur.
* When load estimation and sensor-based/sensorless force control functions are performed, the collision will not be detected.
* Collisions on the positioners, stationary guns, and jigs that are not attached to the robot cannot be detected.
* Special-order robots do not support the model-based collision detection function.

 

The following shows how to set the collision detection function.

1.	Touch the \[3: Robot Parameter &gt; 14: Impact Detection\] menu.

2.	Set whether to use the collision detection function, and set the sensitivity, etc.

![](../../../_assets/image_481.png)



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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>This is information on the use options of the collision detection function.
          You can set whether to use this function and set the sensitivity and whether
          to use the low-speed collision detection function.</p>
        <ul>
          <li>[Function to be Used]: You can set whether to use the collision detection
            function.</li>
          <li>[Sensitivity]: You can set the collision detection sensitivity. The larger
            the value, the more sensitive it is to impact (basic setting value: 100%).</li>
          <li>[Low-Speed Impact Detection]: You can set whether to use the low-speed
            collision detection function.</li>
          <li>[Reference Time]: You can set the reference time for determining a collision.
            If an impact force occurs during the reference time, it will be determined
            as a collision.</li>
          <li>[Link Speed]: You can set the reference speed for determining a low speed.
            Slow-speed collision will be inspected only below the reference link speed.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: You can save the changes.</li>
          <li>[Reset All]: You can initialize the setting values of all the use options.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

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
          <img src="../../../_assets/coldet-sensitivity.png" alt/>
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

# 7.4.9 Jog Inching Level Setting

You can limit the operation by designating the moving distance. This is useful when you want to move the robot as much as the desired distance with the jog key in manual mode.

1.	Touch the \[3: Robot Parameter &gt; 11: Set the Jog Inching Level\] menu.

2.	After setting the distance and angle for each jog inching level, touch the \[OK\] button.

![](../../../_assets/image_487.png)



# 7.4.9.1 Main Functions of the Jog Inching Function

* Inching applicable coordinate systems
  * 
    Inching in the joint coordinate system: Movement will take place as much as the distance \(mm\) and angle \(deg\) designated for each joint.

  * Inching in the Cartesian coordinate system
  * Inching in the tool coordinate system 
  * Inching in the user coordinate system: Movement will take place as much as the amount designated for the X, Y, and Z positions \(mm\) and Rx, Ry, and Rz postures\(deg\).
* Inching level 

  You can set the inching distance at the same level as the existing jog speed, so you can select eight levels of speed, and you can set the inching distance for each level.





# 7.4.9.2 Inching Jog Operation

The inching function is a function that does not allow the movement to take place beyond the maximum moving distance per one push of the jog key. 

Even after reaching the inching distance, if you keep pressing the jog key and then release your hand, the robot will decelerate to the inching distance, and then stop.

![Figure 63 When Releasing the Key After Reaching the Inching Distance](../../../_assets/image_488.png)



If you release the jog key before reaching the inching distance, the robot will decelerate, starting from the time you release the jog key, and then stop. At this time, the mode will be the same as the general jog mode.

![Figure 64 When Releasing the Hand Before Reaching the Inching Distance](../../../_assets/image_473.png)

{% hint style="info" %}
In the joint coordinate system, the speed level 1 is fixed to a mode that the robot will move by 1 bit of the encoder.
{% endhint %}

# 7.5 Application Parameters

1.	Touch the \[4: Application Parameter\] menu. Then, the application parameter menu will appear.

2.	Select the desired menu, and then check and set various parameters for the use of the application functions of the robot.

![](../_assets/image_483.png)



{% hint style="info" %}
For details on how to use each menu, refer to the “Function Manual” for each application function.
{% endhint %}

# 7.6 Initialize

If the robot controller does not operate normally, initialize the system. The system initialization must be performed by an engineer who has experience in initial setting of the robots of Hyundai Robotics.



1.	Touch the \[5: Initialize\] menu. Then, the menu for initialization will appear.

2.	Select the desired menu, and then perform the initial setting of the robot system, and then initialize the serial encoder.

![](../../_assets/image_493.png)



{% hint style="info" %}
Some items in the \[Initialize\] menu will be supported only when a specific type of an additional axis is selected.
{% endhint %}

{% hint style="info" %}
* To initialize the system, you should contact the customer support team and ask for an expert or a qualified engineer to prevent false operation.
* 
  When the system is initialized, all data and programs saved in the controller will be deleted. Before initializing the system, you should back up your data and programs and restore them if necessary.

  For details on Data Backup and Restoration, refer to ???[4.2.5 Data Backup](../../4-service/2-file-manager/5-data-backup.md)??? and ???[4.2.6 Data Restoration](../../4-service/2-file-manager/6-data-restore.md)???.
{% endhint %}



# 7.6.1 System Format

1.	On the status bar of the Hi6 teach pendant screen, check if the operation mode is set to manual mode.

![](../../_assets/image_514.png)

* If it is set to automatic mode, turn the mode switch of the teach pendant to set it to manual mode.

![](../../_assets/image_230.png)

2.	Touch the \[Set Up\] button &gt; \[5: Initialize &gt; 1: System format\] menu.

![](../../_assets/image_535.png)

3.	After checking the saved data, touch the \[Initialize\] button. All data and programs including control parameter files and machine parameter files will be deleted, and the initial setting values will be restored.

![](../../_assets/image_534.png)

# 7.6.2 Robot Type Selection

1.	Touch the \[5: Initialize &gt; 2: Robot Type Selection\] menu. Or touch the \[Mechanism\] button at the top right of the Hi6 teach pendant screen.

2.	Select a robot in the robot model selection window, and then touch the \[OK\] button.

![](../../_assets/image_506.png)



* You can scroll through the robot model list to check the model name, or you can input the model name to search.
* If you touch the robot usage button, only the robots belonging to the usage can be checked on the list.
* 
  If you select a new robot model, the machine parameter file \(hi6\_porj.json\) will be restored to the initial setting values, and various history files will also be initialized.

* 
  If you select a system that includes additional axes such as a travel axis or a servo gun, you should set the number of additional axes. If a system consists of only robot axes without additional axes, input 0. 



![](../../_assets/image_508.png)

{% hint style="warning" %}
* The manipulator and controller are shipped as one system. For this reason, the robot controller is equipped with a drive suitable for the drive capacity of the robot that is part of the system.
* When resetting the system by initializing it, you must check the model of the robot that was set to the initial setting values when shipped from the factory, and then set the correct model.


{% endhint %}

3.	After touching the \[Favorites\] button at the bottom right of the Hi6 teach pendant screen, input 314 in the input area of the favorites window, and then touch the \[OK\] button.

![](../../_assets/image_498.png)

{% hint style="warning" %}
* In Engineer Mode, the Engineer Mode icon \(![](../../_assets/eng-mode.png)\) will blink on the status bar.
* Use caution as a serious problem may occur in the robot system if the setting is performed incorrectly.
{% endhint %}

4.	Touch the \[Set Up\] button &gt; \[3: Robot Parameter &gt; 4: Encoder Offset\] menu.

![](../../_assets/image_533.png)

5.	Perform encoder offset calibration. To turn on the motor, you should set the encoder offset temporarily even if the robot position is not the reference position.

![](../../_assets/image_490.png)

{% hint style="info" %}
* You should perform an encoder offset setting normally after moving the robot to the reference position.
* For the initial setting, you should perform the encoder offset setting even if the robot position is not the reference position. Otherwise, the motor will not be turned on, making it impossible to drive the robot.


{% endhint %}

6.	Turn off and on the power of the controller and then supply power to the motor.

7.	In manual mode, move the robot safely to the reference position at low speed and then perform the encoder offset calibration again by referring to steps 7–8.

* In the encoder offset setting item, the current encoder position will be set to 0X400000 \(hexadecimal\).
* When a motor is replaced because of failure, if the encoder offset setting is performed at the same location, the recorded program can be used identically.

8.	Press the &lt;Program&gt; key on the teach pendant, and select the program 9999 and then record one step. You can move the robot to the reference position easily. 

{% hint style="warning" %}
* To initialize the system, contact the customer support team and ask an expert.
* 
  For initialization of a collaborative root, refer to the collaborative robot safety functions manual.

* 
  When the system is initialized, all data and programs, including control parameter files and machine parameter files, will be deleted. If you back up your data before initializing the system, it can be restored and used when necessary.
{% endhint %}



# 7.6.3 Usage Setting

You can select the operation usage and initialize the user key and input/output assignment signals according to the operation usage.

1.	Touch the \[5: Initialize &gt; 3: Usage Setting\] menu.

2.	After selecting the operation usage and setting the environment conditions according to the usage, touch the \[OK\] button. Then, you can use commands related to the selected operation usage and access the relevant menus.





# 7.6.3.1 Spot Welding

If you select the operation usage as spot welding, you can use the commands related to spot welding and access the menu related to spot welding.

![Figure 65 Operation Usage &#x2013; Spot Welding](../../../_assets/image_492.png)

1.	Set \[Spot Welding\] as enable. Then, other usages will be handled as disable.

2.	Click the \[User Key Initialization\] drop-down menu and the \[Input/Output Assign Initialization\] drop-down menu, respectively, and select spot.





# 7.6.3.2 Arc Welding

If you select the operation usage as Arc welding, you can use commands related to arc welding and access the menus related to arc welding.

![Figure 66 Operation Usage &#x2013; Arc Welding](../../../_assets/image_509.png)

1.	Set the welding machine type \(analog or digital\) in \[Arc Welding\]. Other usages will be handled as disable, and a list of welders supported by the system will appear at the bottom of the screen.

2.	After checking the welder list, set the welder number.

3.	Click the \[User Key Initialization\] drop-down menu and the \[Input/Output Assign Initialization\] drop-down menu, respectively, and select arc.





# 7.6.4 Serial Encoder Reset

The serial encoder stores the encoder rotation speed information in the internal memory. The encoder rotation speed can be cleared to zero by resolving the motor error state or by resetting the zero point of the encoder.

1.	Touch the \[5: Initialize &gt; 4: Serial Encoder Reset\] menu.

2.	Set the encoder resetting mode for each axis and check the status, and then execute the resetting.

![](../../_assets/image_504.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>You can set whether to use the encoder reset function for each axis and
          set a mode for each axis.</p>
        <ul>
          <li>[Disable]: Serial encoder resetting will not be executed.</li>
          <li>[Error release]: You can clear only the errors related to the motor encoder
            without clearing the encoder rotation speed.</li>
          <li>[Reset]: You can clear the rotation speed by resolving the errors related
            to the motor encoder and then by resetting the zero point of the encoder.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[Execute]: You can execute the serial encoder resetting.</li>
          <li>[All select]: You can select all axes at once.</li>
          <li>[All cancel]: You can deselect all axes at once</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
* You can perform the encoder resetting when performing the initial setting of the robot system, but never perform the encoder resetting while the robot is operating normally. However, if an encoder-related error such as a communication error occurs or the encoder battery is lost, you can perform the encoder resetting. In this case, check the actual position in the robot program so that it does not differ from the existing robot origin position.
* If the power is not supplied to the controller and encoder, the position information of the encoder may be lost, possibly causing trouble in using the job program of the robot. To solve this problem, a dedicated battery is attached to the serial encoder, making it possible to record the position information regardless of the power status of the controller. If a voltage error occurs in the encoder battery, the battery must be replaced while the controller is still powered on to prevent loss of the position information.
{% endhint %}



# 7.6.5 Additional Axis Parameter Setting

Additional axes that can be used in addition to the robot itself include the robot’s base axis \(travel axis\), servo gun axis, positioner axis, and jig axis. For details on the specification of each additional axis, refer to the “Additional Axis Function Manual.”

The method to set parameters such as the specification and configuration of the additional axes that are being used is as follows.

1.	Touch the \[5: Initialize &gt; 5: Additional Axis Parameter Setting\] menu.

2.	Set the parameters such as the specification and configuration of the additional axes.

![](../../_assets/image_499.png)





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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Detailed parameter setting information of the additional axis. You can
          check and set the name, specification, and configuration, etc. of the additional
          axis.</p>
        <ul>
          <li>[Name]: Name of the additional axis in use</li>
          <li>[Axis Specification]: Specification of the additional axis. You can use
            individual functions separately developed for each usage of the additional
            axis according to the specifications.</li>
          <li>[Axis structure]: Mechanism type of the additional axis. In the case of
            the specifications of some axes, you can designate the mechanism type that
            was registered in advance. As an exemplary case, you can select the standard
            positioner model in case of the position.</li>
          <li>[Axis position]: This is the position where the axis is connected to the
            DSP board. You can designate the BD number, DSP number, axis number, and
            brake number sequentially according to the wiring specifications.</li>
          <li>[Reduction ratio]: Information of the deceleration ratio that involves
            the motor and link of the additional axis
            <ul>
              <li>The deceleration ratio sign can be set according to the rotation direction
                of the motor shaft when the additional axis link moves in the (+) direction.
                When viewed from the front, if the shaft is rotating counterclockwise,
                the sign will be (+), and if it is rotating clockwise, the sign will be
                (-).</li>
              <li>The parameter of the numerator of the deceleration ratio is the moving
                distance (mm or deg) of the link, and the parameter corresponding to the
                denominator is the motor rotation speed corresponding to the moving distance
                of the link. The parameters of the setting items will be defined in integer
                form. For parameters that will be displayed with decimals, set the deceleration
                ratio as an integer by multiplying the numerator and denominator by a certain
                multiple.</li>
            </ul>
          </li>
          <li>[Soft limit]: The minimum and maximum operating range of the additional
            axis</li>
          <li>[AMP Specification]: The amplifier specification of the additional axis</li>
          <li>[Motor Specification]: Model name of the motor connected to the additional
            axis</li>
          <li>[Accel/Decel Parameter]: The maximum speed and acceleration time of the
            additional axis</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: You can save the changes.</li>
          <li>[+]/[-]: You can add a new additional axis or delete an additional axis.</li>
          <li>A list of additional axes. If you select the additional axis name, you
            can check and edit detailed parameters.</li>
          <li>[Copy page]/[Paste page]:
            <br />You can copy the information of the additional axis and paste it into
            the data of another additional axis.
            <br />After selecting the information name of the additional axis to be copied
            from the list and then touching the <b>[Copy page]</b> button, select the
            name of the additional axis to which the value is to be applied, and then
            touch the <b>[Paste page]</b> button.</li>
          <li>[Rotation Radius]: If the additional axis is a rotation axis, you can
            set the rotation radius to limit the linear speed when jogging.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

# 7.6.6 Mechanism Setting

Mechanism will be used as a group during the jog operation which the jog keys are to be assigned to. In addition, mechanism is also a set of units, each of which is to be differentiated in the process of recording or editing the position of a step. When the mechanisms are set, mechanism numbers \(M\#\) will be assigned for individual groups of axes.

The method to set the use of the endless function and set the position group is as follows.

1.	Touch the \[5: Initialize &gt; 6: Mechanism Setting\] menu.

2.	After setting the mechanism number, positioner group number, and the use of the endless function for each axis, touch the \[OK\] button.

![](../../_assets/image_524.png)



* \[Mech\]: By touching the drop-down menu, you can set the mechanism number of the axis.
  * If the axis specification is a robot, the mechanism number will be fixed as M0.
  * 
    Starting with the additional axis, you can designate the mechanism number to a value ranging between M1 and M7.

  * 
    The axes set with the same mechanism number will be managed as the same group.

  * 
    To jog the additional axis, you can switch between mechanisms using the \[Mech\] button. At this time, if you press the jog key, jogging will take place in the order of the axes of the relevant mechanism.
* 
  \[Positioner Group\]: You can set the positioner group number. The position group number can be set only for the axes whose specification is set as positioner.

* 
  \[Endless\]: You can set whether to use the endless function on the axis.



{% hint style="info" %}
A set mechanism unit is the minimum unit that can be assigned to each task and can be driven. To each task, a complex combination of mechanisms can be assigned to individual tasks.
{% endhint %}

#### 

#### Position Group Designation Rules

* Designate the group in order starting with the lower axis.
* 
  Designate the group not in sync as disable.

* 
  In the case of the positioner, only up to axis 2 will be supported for the same group. Do not designate axis 3 as the same group.

* 
  Redefining the group setting will disable the previously designated positioner calibration data, so you should execute the positioner calibration again.



#### Mechanism Jog Rules 

* The Hi6 controller provides eight jog keys in total.
* 
  Mechanisms will be utilized as one group during the jog operation.

* 
  If you select the mechanism number as \[M0\], the jog keys for the axes 7 and 8 will be operating as an exceptional case, and it is possible to operate M1 and M2 within a range in which the total number of axes including the next mechanism is eight or less. Even in this case, if you set the mechanism number as \[M1\], you can perform the jog operation for the configuration elements of M1. 

* 
  The following shows the example of the usage.

  Example 1\) M0: Robot \(Axes 1–6\). M1: Travel axis \(Axis 7\). M2: Servo gun \(Axis 8\)

  * Select \[M0\] ⇒ Jog key for axes 1–6: M0. Jog key for axis 7: M1. Jog key for axis 8: M2
  * Select \[M1\] ⇒ Jog key for axis 1: M1
  * Select \[M2\] ⇒ Jog key for axis 1: M2

  Example 2\) M0: Robot \(Axes 1–6\). M1: Travel axis \(Axis 7\). M2: Servo gun \(Axes 8–9\)

  * Select \[M0\] ⇒ Jog key for axes 1–6: M0. Jog key for axis 7: M1
  * Select \[M1\] ⇒ Jog key for axis 1: M1
  * Select \[M2\] ⇒ Jog key for axes 1–2: M2

  Example 3\) M0: Robot \(Axes 1–7\). M1: Travel axis \(Axis 8\). M2: Servo gun \(Axes 9–10\)

  * Select \[M0\] ⇒ Jog key for axes 1–7: M0. Jog key for axis 8: M1
  * Select \[M1\] ⇒ Jog key for axis 1: M1
  * Select \[M2\] ⇒ Jog key for axis 1: M2





# 7.7 Auto Calibration

To use the robot correctly, the robot’s axis origin, tool length, load mass, and base axis direction can be found using the taught programs and using the movements that will be executed automatically. Those calibrated values will be automatically reflected in the robot.

1.	Touch the \[6: Auto Calibration\] menu. Then, the automatic calibration menu will appear.

2.	Calibrate the robot’s axis origin, tool length, load mass, base axis direction, etc. by selecting the desired menu,

![](../../_assets/image_494.png)

# 7.7.1 Optimize Axis Origin and Tool Length

The optimization of axis origin and tool length is a function to calibrate the origin and tool length of each axis of the robot without using an external measuring sensor.

Prepare two pointed tips. Fix one on the outside and the other on the tool. Then, while changing only the posture of the tooltip of the robot based on the outside fixed tip, you need to record several points using the robot program. At this time, you need to teach seven points to find the axis origin and tool length, and four points or more to find only the tool length.

![Figure 67 Method of Teaching for the Axis Origin and Tool Length Optimization Function](../../_assets/image_228.png)

Using the axis origin and tool length optimization function, you can find the optimized tool lengths X, Y, and Z and the optimized origin of the robot H, V, R2, and B axes as well, even when no CAD data is available for them.

{% hint style="warning" %}
When the axis origin and tool length optimization function is used, the encoder offset and tool length will be changed, thus also changing the operation position of the previously taught program. Therefore, you should perform the optimization of axis origin and tool length before writing the teaching program.
{% endhint %}

{% hint style="info" %}
* In using the axis origin and tool length optimization function, the accuracy of the teaching is proportional to the accuracy of the maximum step position error result. Therefore, you should prepare two pointed tips and perform the teaching for the tooltip to match the two tips as accurately as possible. Make sure that the accuracy of the matching between the tooltip and the fixed points in space is within 0.5 mm when visually checked.
* Teach by setting a posture, with a difference of 30 deg or more, for each step so that the postures of the steps are not similar.
* Operate the wrist axes \(R2, B, R1\) as large as possible in a step and perform teaching while keeping a sufficient \(as large as possible\) angle difference of the wrist axes for individual steps.
{% endhint %}

The method to use the axis origin and tool length optimization function is as follows.

1.	Touch the \[6: Auto Calibration &gt; 1: Optimize Axis Origin and Tool Length\] menu.

2.	Select an optimization target and set detailed options.

![](../../_assets/image_529.png)



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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Detailed parameter setting information of the additional axis. You can
          check and set the name, specification, and configuration of the additional
          axis.</p>
        <ul>
          <li>[Optimization Selection]: You can select an optimization target.
            <ul>
              <li>[Tool Length]: You can calibrate the robot&#x2019;s tool length value.
                If the robot origin is correctly set, you can calibrate only the tool length.</li>
              <li>[Axis Origin &amp; Tool Length]: You can calibrate both the robot&#x2019;s
                origin and tool length values.
                <br />Normally, this function can be used when installing a robot and then initially
                setting the correct origin.</li>
            </ul>
          </li>
          <li>[Program Number]: You can set the number of the program in which the same
            point is recorded in multiple postures.</li>
          <li>[Tool Number]: This is the number of the tool to be set automatically.
            This should match the tool number recorded in the setting program.</li>
          <li>[Step location Error tolerance]: You can set the error range of the automatic
            calibration result (the initial setting value is 0.6 mm). If the expected
            error is within the error range, the integer data will be automatically
            updated, and if the error is out of the error range, whether to reflect
            the integer will be notified to and confirmed with the user, and then the
            necessary handling will be performed.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: You can save the changes.</li>
          <li>[Execute]: You can execute optimization based on the set information.
            The optimization result will appear in [Max Step Position Error].</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
It requires your attention that if you calibrate both the robot origin and tool length values, all origins of the robot will change, consequently changing the position of the previously created program.
{% endhint %}

{% hint style="info" %}
* You can also set the origin of each axis and tool length of the robot in the settings menu.
  * Tool Length: \[Set Up &gt; 3: Robot Parameter &gt; 1: Tool Data\]
  * Origin of each axis: \[Set Up &gt; 3: Robot Parameter &gt; 2: Axis Origin\]
* If you calibrate the tool angle using the angle calibration function \(\[Set Up &gt; 3: Robot Parameter &gt; 1: Tool Data\]\), you should execute the origin axis and tool length optimization function first, and then execute the angle calibration. In this way, the tool data can be set correctly.
{% endhint %}

# 7.7.2 Positioner Calibration

Positioner calibration is a function that enables the robot to perform a synchronized follow-up with the operation of a jig device installed outside the robot or to perform a linear or circular operation relative to the jig device. The external jig device in which the positioner calibration function will be applied to is called a positioner or station.

Using the positioner calibration function makes it possible to compensate for the operational difficulties because of the limitation of the robot operation area. In other words, even if the positioner moves while the workpiece is fixed onto it, the robot can still perform a linear or circular operation on the workpiece by following up with the movement of the positioner.

You can simply set the positioner’s coordinate system by performing the positioner calibration by teaching three points for a 1-axis positioner and five points for a 2-axis positioning.

![Figure 68 1-Axis Positioner \(Left\) / 2-Axis Positioner \(Right\)](../../_assets/image_244.png)

The information on the main functions of the positioner calibration is as follows.

| Main Functions | Description |
| :--- | :--- |
| Positioner group | 1–4 groups are supported |
| Positioner axis count | 1-axis positioner and 2-axis positioner are supported \(rotation axis\) |
| Interpolation mode | Linear interpolation and circular interpolation are supported |

{% hint style="info" %}
* The positioner calibration function can be used while the positioner group is set.
* For more details, refer to the “Hi6 Controller Positioner Sync Function Manual.”
{% endhint %}

# 7.7.3 Load Estimation Function

Load estimation is a function that automatically calculates the physical properties \(mass, center position, inertia\) of the tool attached to the front end of the robot through a certain operation.

The manipulator information \(mass, center of mass, inertia of each link\) is registered in the controller. However, as a tool will be used after being attached to the front end of the robot when necessary, the tool information should be inputted. The information on the tool physical properties includes tool mass \(kg\), center position, and inertia that are necessary to safely use the robot.

If the CAD data contains the physical properties information of the tool, you can directly input the tool mass, center position, and inertia by touching the \[Set Up\] button &gt; \[3: Robot Parameter &gt; 1: Tool Data\] menu of the job program.

![](../../_assets/image_491.png)



The tool data setting information is as follows.

![Figure 70 Tool Data](../../_assets/image_505.png)

* \[Weight\]: The total weight \(kg\) of the tool installed at the front end of the robot
* \[Center\]: The distance \(mm\) in the x, y, z directions from the center of the robot flange face to the position of the center of gravity of the tool
* \[Inertia\]: The moment of inertia of the tool with respect to the tool coordinate \(kg/m2\). The moment of inertia will be determined by the mass distribution around the x, y, and z axes based on the center of gravity, and will increase as the load mass is distributed farther from the rotation axis.
* Tool data coordinate system: Inertia and center will be expressed as values with respect to the x-, y-, and z-axis directions.



However, in many cases, it is difficult to determine the physical properties of the tool such as mass, inertia, and center of gravity of the tool from CAD data. At this time, you can check the physical properties of the tool using the load estimation function in the robot controller.

![Figure 71 Load Estimation Function](../../_assets/image_527.png)

1.	Touch the \[6: Auto Calibration &gt; 4: Load Estimation Function\] menu.

2.	After touching the \[Add. Weight on Each Axis\] button, input the information of the additional weight of each axis.

If the load estimation function is performed while there is additional weight, it will be determined that all the weight objects mounted onto the robot are at the front end. For accurate load estimation, the information on the additional weight of each axis should be inputted.

3.	After moving the robot to a safe area by moving the main axis of the robot, touch the \[Set pose\] button.

4.	After touching the \[Wrist Axis Operation Area\] button, designate the operation area of the wrist axis to be used in the load estimation operation. Load estimation can be performed in an operation area that there is no interference not only with nearby facilities but also with the manipulator.

If the \[Wrist Axis Operation Area\] button is not supported, skip this step, and perform the next step.

5.	Touch the \[Play check\] button. Then, while the robot is operating at a low speed, you can check for any interference with nearby facilities or the manipulator.

6.	After inputting the number of the tool mounted onto the robot, touch the \[Play Normal\] button. Then, load estimation will be performed, allowing the physical properties of the tool to be calculated.

7.	After checking the load estimation result, touch the \[End\] button. Then, the calculated physical properties of the tool will be registered in the tool number.

{% hint style="info" %}
* Additional weight is the overall weight of all devices that the user attaches to the robot, such as a welding dressing device and welding signal line relay box, except for the tool mounted at the front end of the robot.
* 
  The wrist axis operation area function will not be supported in some robots.

* It requires your attention that the load estimation function may not be executed depending on the setting values of the wrist axis operation area function.
* For details on the load estimation function, refer to the “Load Estimation Function Manual.”
{% endhint %}



# 7.7.4 Base Axis Calibration

Base axis calibration is a function to calibrate the installation direction of the axis.

It is almost impossible to install the base axis to exactly match one direction \(X, Y, or Z\) of the robot coordinate system. When you calculate the direction of the base axis in the controller using the base axis calibration function, you can improve the performance of the linear interpolation trajectory of the system including the base axis.

After the robot is installed on the base axis, this function makes it possible to perform position interpolation by finding the direction vector of any base axis on which the robot is installed.

![Figure 72 Base Axis Calibration](../../../_assets/image_497.png)


In general, the base axis is used to move the robot to the operation position. In special cases, the base axis can also be used in a case in which a linear trajectory should be guaranteed while the robot is moving on the base axis.

* When two robots with the base axis calibrated deliver the workpiece \(multi-robots will be supported in the future\)
* When you need to perform interpolation while operating the base axis





# 7.7.4.1 Base Axis Initial Setting

1.	In manual mode, touch the \[system\] button &gt; \[5: Initialize&gt; 5: Additional Axis Parameter Setting\] menu on the right side of the initial screen.

2.	After setting the parameters such as the specifications and configuration of the additional axis, touch the \[OK\] button.

* \[Axis Specification\]: You can select the specification of the additional axis as base.
* \[Axis Configuration\]: You can select the mechanism of the additional axis as any.
* Other parameters: You can set other parameters according to the instrumental design value and controller configuration specifications.



{% hint style="info" %}
* When the system is initialized, the additional axis setting menu will appear, allowing you to perform the initial setting of the base axis.
* 
  The additional axis parameter setting menu is a function for engineers, so it will not be supported for general users. For details on the additional axis parameter setting menu, contact the engineer for inquiry.
{% endhint %}

{% hint style="warning" %}
You can use the calibration function only for the first base axis, and you can set the axis configuration as any when setting the additional axis parameter. Do not set the axis configuration as any for the other base axes except for the first base axis.
{% endhint %}

# 7.7.4.2 Base Axis Calibration Program Teaching

1.	Make a reference point in space, and then record the first reference point.

2.	Move the base axis more than 200 mm and record the same point as the second step.

3.	While moving 200 mm or more in the same direction as the direction you moved in step 2, record the same point as the third and fourth steps.

![](../../../_assets/image_526.png)



{% hint style="warning" %}
* Teach the travel axis calibration program using a tool for which robot calibration \(optimization of the axis origin and tool length\) has been completed.
* 
  When recording a step, record it using a tool number for base axis calibration.

* 
  Record the position by setting the moving distance of the base axis between recording steps as far as possible.
{% endhint %}

# 7.7.4.3 Base Axis Calibration Execution

1.	Touch the \[6: Auto Calibration &gt; 6: Base Axis Calibration\] menu.

2.	After inputting the program number for the base axis calibration, touch the \[Auto Setting\] button.

![](../../../_assets/image_496.png)

3.	After checking the installation direction vector value of the base axis, touch the \[OK\] button.

# 7.7.4.4 Operation After Base Axis Calibration

If you jog the base axis after performing base axis calibration, the distance traveled in the created direction vector of the base axis will be converted into the current coordinate value.

![Figure 73 Operation After Calibration of the Base Axis](../../../_assets/image_528.png)

1.	Touch the \[+\] button at the top right of the panel stack in the work area, and then touch \[Pose\] in the panel selection window.

2.	Jog the base axis. The distance traveled in the direction of the base axis will be converted into X, Y, and Z values and displayed in the pose information window.

3.	Record and play back the steps in the usual way.

{% hint style="warning" %}
Set the jog coordinate system as the tool coordinate system and jog the base axis to check whether the base axis is properly calibrated. If the tooltip fixing operation is executed, it means that the base axis has been properly calibrated.
{% endhint %}

# 7.7.5 Gravity Direction Auto Setting

The Hi6 controller is based on dynamics, so it is important to set the gravity direction.

In general, the robot installation direction is perpendicular to the gravity direction as follows. If the robot is installed obliquely to the ground, the gravity direction should be set in the robot controller. At this time, you can use the automatic gravity direction setting function.

![Figure 74 Gravity Direction of the Robot Placed on a Floor \(Left\) / Gravity Direction of the Robot Placed on a Slope \(Right\)](../../_assets/image_507.png)



How to set the gravity direction is as follows.

1.	Attach a weight to the outside to indicate the gravity direction, and then teach two points \(Step 1, Step 2\) in the direction of the gravitational action.

2.	Touch the \[6: Auto Calibration &gt; 8: Automatic setting of gravity direction\] menu.

3.	After inputting the program number, touch the \[Execute\] button. Then, the direction vector will be calculated and displayed.

![](../../_assets/image_510.png)



4.	After checking the direction vector value, touch the \[OK\] button. Then, the direction will be set as the gravity direction.

# 7.7.6 Calibration of the Robot and Tool

The robot and tool calibration function will be used in an environment where the position of the robot can be measured with a 3D measuring device.

1.	After selecting the position to be measured at the tooltip of the robot, measure the position of more than 15 points while moving the position and posture of the robot in various ways, and record the robot positions as a program.

![](../../_assets/image_245.png)

2.	Organize the measured robot’s position data \(measuring point data\) in X, Y, and Z formats, and then create a file \(Format: ASCII Extension: MSR\). 

![](../../_assets/image_518.png)

3.	After saving the position data file into a removable storage device, connect the removable storage device to the teach pendant. The \[USB\] icon \( \) will appear in the status bar of the Hi6 teach pendant screen.

4.	Touch the \[6: Auto Calibration &gt; 9: Robot and Tool calibration condition\] menu.

5.	Touch the \[Explorer\] button to select a position data file and set the robot program used for the measurement.

![](../../_assets/image_536.png)



6.	Touch the \[OK\] button. Then, the screen will switch to the robot and tool calibration screen. 

7.	Touch the \[Execute\] button on the robot and tool calibration execution screen. Then, the calibration results will appear.

![](../../_assets/image_522.png)



8.	After checking the calibration result, touch the \[OK\] button. Then, the calibration result will be automatically applied to the axis origin and tool integer. 

9.	Touch the \[3: Robot Parameter &gt; 1: Tool Data\] menu. Then, you can check the robot calibration execution result.

![](../../_assets/image_495.png)

{% hint style="info" %}
The axis origin and tool length X, Y, and Z values of the axes 2–5 \(H, V, R2, and B axes\) of the calibration parameter are selected. To calibrate the tool only, perform execution after deselecting the value of each axis.
{% endhint %}





# 8. R Codes

When it comes to the operating procedures for frequently used functions, such as modifying the contents of a program or changing the setting status of a controller, you can use them easily by designating specific service codes \(R codes\). 

R codes are configured in the “R+No.” format, which combines R, representing Reset and Rapid, with a number.





# 8.1 Use of R Codes

The method to execute a specified function using an R code is as follows.

1.	Touch the \[Favorites\] button on the right side of the Hi6 teach pendant screen. Then, the favorites window will appear.

![](../_assets/image_516.png)



2.	Select a code number from the list or input the code number in the input area, and then touch the \[OK\] button or press the <<b>ENTER</b>> key. Then, the function designated to the selected R code will be executed.

![](../_assets/image_523.png)





# 8.2 R0 for Resetting the Step Counter

After inputting 0 in the favorites window, touch the \[OK\] button or press the <<b>ENTER</b>> key.

![](../_assets/image_511.png)

You can initialize the step counter to move to STEP0. You can also perform the following functions.

* Clearing the playback execution status
* Turning off the overall abnormality signal and lamp
* Turning off the alarm signal
* Clearing the wait status
* Clearing the status and signals of various application functions



{% hint style="info" %}
R0 code cannot be used during the startup of the robot.
{% endhint %}

# 8.3 R115 for Copying a Program

You can copy the JOB program on the mainboard to another program on the mainboard. After inputting the number of the program that you want to copy, input the program number to which you want to copy the copied program.

1.	After inputting 115 in the favorites window, touch the \[OK\] button or press the <<b>ENTER</b>> key.

2.	After inputting the number of the program \(original\) that you want to copy and also the number of the program \(target\) to which you want to copy the copied program, touch the \[OK\] button or press the <<b>ENTER</b>> key. Then, the program will be copied.

![](../_assets/image_531.png)

* If a program with the same number as the program to which you want to copy the copied program exists already, you should select whether to overwrite the file.
* 
  If there is no original file to copy, a notification message \(“No Original File Exists.”\) will appear.



{% hint style="info" %}
Code R115 cannot be used in automatic mode. It must be used in manual mode.
{% endhint %}



# 8.4 R117 for Deleting a Program

You can individually delete the programs in the internal memory.

1.	After inputting 117 in the favorites window, touch the \[OK\] button or press the <<b>ENTER</b>> key.

2.	After inputting the number of the program that you want to delete, touch the \[OK\] button or press the <<b>ENTER</b>> key. Then, the deletion confirmation window will appear.

![](../_assets/image_517.png)

* If there is no file to delete, a notification message \(“No File Exists.”\) will appear. 
* If you want to delete a protected program, a notification message \(“A Protected File.”\) will appear.

3.	In the deletion confirmation window, touch the \[OK\] button or press the <<b>ENTER</b>> key. Then, the selected program will be deleted.

{% hint style="info" %}
The R117 code cannot be used in automatic mode. It must be used in manual mode.
{% endhint %}

# 8.5 R210 for Selecting a Spot Gun Number

You can select the spot guns to use when using multiple spot welding guns \(servo guns or pneumatic guns\).

1.	After inputting 210 in the favorites window, touch the \[OK\] button or press the <<b>ENTER</b>> key.

2.	After inputting the number of the spot gun to use, touch the \[OK\] button or press the <<b>ENTER</b>> key.

![](../_assets/image_512.png)

* The selected spot gun number will be displayed on the \[Gun\] button on the left side of the Hi6 teach pendant screen.
* If you change the spot gun number, the tool number designated in the spot gun corresponding tool number will be automatically changed. You can check the spot gun corresponding tool number in the \[Set Up &gt; 4: Application Parameter &gt; 1: Spot Welding &gt; 1: Gun Number Corresponding Tool Number and Gun Type Setting\] menu.



{% hint style="info" %}
* R210 code cannot be used during the startup of the robot.
* The spot gun number can be set only in the spot welding environment \(\[Spot Welding\] item in the \[Set Up &gt; 5: Initialize&gt; 3: Usage Setting\] menu is set as enable\).
* You can manually open, close, and squeeze the selected spot welding gun. For details on the spot welding function, refer to the “Hi6 Controller Spot Welding Function Manual.”
{% endhint %}

# 8.6 R211 for Setting the Servo Gun Squeeze Force

You can manually set the squeeze force when executing the servo gun squeeze. 

1.	After inputting 211 in the favorites window, touch the \[OK\] button or press the <<b>ENTER</b>> key.

2.	After inputting the squeeze force, touch the \[OK\] button or press the <<b>ENTER</b>> key.

![](../_assets/image_525.png)



* The squeeze force in the welding condition file will not be changed.
* If the inputted squeeze force is greater than or smaller than the upper limit of the current/pressure table of the servo gun parameters, a warning message will appear.



{% hint style="info" %}
* R211 code cannot be used during the startup of the robot. 
* 
  The spot gun number can be set only in the spot welding environment \(\[Spot Welding\] item in the \[Set Up &gt; 5: Initialize&gt; 3: Usage Setting\] menu is set as enable\). 

* For details on the manual setting of the servo gun squeeze force, refer to the “Hi6 Controller Spot Welding Function Manual.”
{% endhint %}

# 8.7 R212 for Presetting the Servo Gun Moving Electrode Wear Volume

You can manually set the servo gun moving electrode wear volume.

1.	After inputting 212 in the favorites window, touch the \[OK\] button or press the <<b>ENTER</b>> key. 

2.	After inputting the moving electrode wear volume, touch the \[OK\] button or press the <<b>ENTER</b>> key.

![](../_assets/image_530.png)

{% hint style="warning" %}
It requires your attention that if the setting value is set larger or smaller than the actual wear volume of the electrode, it may cause mismatching of the squeeze force or interference with the workpiece.
{% endhint %}

{% hint style="info" %}
* R212 code cannot be used during the startup of the robot.
* The spot gun number can be set only in the spot welding environment \(\[Spot Welding\] item in the \[Set Up &gt; 5: Initialize&gt; 3: Usage Setting\] menu is set as enable\).
* For details on the manual setting of the servo gun moving electrode wear volume, refer to the “Hi6 Controller Spot Welding Function Manual.”
{% endhint %}

# 8.8 R213 for Presetting the Servo Gun Fixed Electrode Wear Volume

You can manually set the servo gun fixed electrode wear volume. 

1.	After inputting 213 in the favorites window, touch the \[OK\] button or press the <<b>ENTER</b>> key. 

2.	After inputting the fixed electrode wear volume, touch the \[OK\] button or press the <<b>ENTER</b>> key.

![](../_assets/image_532.png)

{% hint style="warning" %}
It requires your attention that if the setting value is set larger or smaller than the actual wear volume of the electrode, it may cause mismatching of the squeeze force or interference with the workpiece.
{% endhint %}

{% hint style="info" %}
* R213 code cannot be used during the startup of the robot. 
* The spot gun number can only be set in the spot welding environment \(\[Spot Welding\] item in the \[Set Up &gt; 5: Initialize&gt; 3: Usage Setting\] menu is set as enable\).
* For details on the manual setting of the servo gun fixed electrode wear volume, refer to the “Hi6 Controller Spot Welding Function Manual.”
{% endhint %}

# 8.9 R214 for Selecting Welding Guns Simultaneously

You can select the numbers of spot welding guns \(servo guns or pneumatic guns\) that are to be used in a welding operation in which multiple spot welding guns will be used at the same time.

1.	After inputting 214 in the favorites window, touch the \[OK\] button or press the <<b>ENTER</b>> key. 

2.	After inputting the numbers of the welding guns to use simultaneously, touch the \[OK\] button or press the <<b>ENTER</b>> key.

![](../_assets/image_489.png)

* The selected spot gun number will be displayed on the \[Gun\] button on the left side of the Hi6 teach pendant screen.
* If you select spot welding guns that are different in type from each other, a notification message \(“The Gun Type of the Currently Selected Gun is Set Incorrectly.”\) will appear.



{% hint style="info" %}
* R214 code cannot be used during the startup of the robot.
* The spot gun number can only be set in the spot welding environment \(\[Spot Welding\] item in the \[Set Up &gt; 5: Initialize &gt; 3: Usage Setting\] menu is set as enable.
* You can check the setting status of the spot welding gun in the \[Set Up &gt; 4: Application Parameter &gt; 1: Spot Welding &gt; 1: Gun Number Corresponding Tool Number and Gun Type Setting\] menu.
  * When a gun is selected as a multisync gun, the manual squeeze/open/close operations of the selected gun will be simultaneously in sync with the previously selected guns.
  * When a gun is selected as a multisync gun, if the gun LED is in the ON status, the SPOT command will be recorded in the sync spot format.
* The selected spot welding gun can be operated manually. For details on the spot welding function, refer to the “Hi6 Controller Spot Welding Function Manual.”
{% endhint %}



# 8.10 R215 for Setting the Squeeze Force in the Spot Welding Condition

You can set the squeeze force required for servo gun welding in the welding condition table. You can also set the squeeze force in the \[Set Up &gt; 4: Application Parameter &gt; 1: Spot Welding &gt; 4: Welding Data \(Condition, Sequence\) &gt; 2: Welding Condition\] menu.

1.	After inputting 215 in the favorites window, touch the \[OK\] button or press the <<b>ENTER</b>> key. 

2.	After inputting the welding condition number, touch the \[OK\] button or press the <<b>ENTER</b>> key.

![](../_assets/image_515.png)



3.	After inputting the servo gun squeeze force, touch the \[OK\] button or press the <<b>ENTER</b>> key.

![](../_assets/image_500.png)

# 8.11 R220 for Setting the Panel Thickness \(Sv\)

You can manually set the panel thickness to record the servo gun spot welding step.

If you execute the one-touch recording in which the MOVE and SPOT statements are to be simultaneously recorded while only the servo gun fixed electrode is in the state of being in contact with the panel, the position of the moving electrode will be automatically recorded in the MOVE statement in consideration of the panel thickness and wear volume.

1.	After inputting 220 in the favorites window, touch the \[OK\] button or press the <<b>ENTER</b>> key. 

2.	After inputting the panel thickness, touch the \[OK\] button or press the <<b>ENTER</b>> key.

![](../_assets/image_542.png)



{% hint style="info" %}
For details on the manual setting of the panel thickness, refer to the “Hi6 Controller Spot Welding Function Manual.”
{% endhint %}

# 8.12 R358 for Changing the Servo Tool

You can manually connect and disconnect the servo tool in the servo tool change system. 

To change the servo tool in the servo tool change system, you need to disconnect or connect the power and various signal lines using a physical automatic tool change \(ATC\) device.

When the servo tool is a servo gun, if you want to manually perform the change work, you need to move the robot, while the motor is turned on, to the servo gun support table where you can connect or disconnect the robot, and then perform the change work. If the servo tool is a different type, such as a positioner, you can perform the change work when the preparation for connection and disconnection work is completed.

R358 servo tool change parameters and the examples are as follows.

![](../_assets/image_546.png)

The method to change the servo tool using the R358 code is as follows.

1.	After inputting 358 in the favorites window, touch the \[OK\] button or press the <<b>ENTER</b>> key.

2.	After inputting the change operation number \(0: Disconnect, 1: Connect, 2: Fix\), touch the \[OK\] button or press the <<b>ENTER</b>> key.

![](../_assets/image_545.png)


3.	After inputting the number of the welding gun to change, touch the \[OK\] button or press the <<b>ENTER</b>> key. The selected weld gun number will be displayed on the \[Gun\] button on the left side of the Hi6 teach pendant screen.
_assets
![](../_assets/image_537.png)

{% hint style="info" %}
* R358 code cannot be used in automatic mode. It must be used in manual mode.
* 
  When the spot gun number is changed, the tool number designated in the spot gun corresponding tool number will be automatically changed. You can check the spot gun corresponding tool number in the \[Set Up &gt; 4: Application Parameter &gt; 1: Spot Welding &gt; 1: Gun Number Corresponding Tool Number and Gun Type Setting\] menu.

* 
  The servo tool change setting can be performed only when the motor is turned on.

* For details on the servo tool change, refer to the “Hi6 Controller Spot Welding Function Manual.”
{% endhint %}

# 8.13 R359 for Servo Tool Encoder Power On Relay

If the servo gun is applied in the servo tool change system, you need to execute this function to reset the encoder of the servo tool axis when installing the servo tool for the first time.

1.	After inputting 359 in the favorites window, touch the \[OK\] button or press the <<b>ENTER</b>> key.

2.	After inputting 1, touch the \[OK\] button or press the <<b>ENTER</b>> key. Then, the power will be supplied to the encoder.

![](../_assets/image_549.png)



{% hint style="info" %}
* R359 code cannot be used in automatic mode. It must be used in manual mode.
* 
  To disable the forced power supply to the servo gun encoder, you should turn off the power of the controller and then turn it back on. Therefore, when the encoder reset is completed, turn off the power of the controller and turn it back on, and then progress the manual connection.

* The servo tool encoder power setting function is a function for engineers, so it is not supported for general users. Please contact our engineer for more information on this feature.
* For details on the servo tool encoder power setting, refer to the “Hi6 Controller Spot Welding Function Manual.”
{% endhint %}

{% hint style="warning" %}
Never mechanically connect or disconnect the servo gun while the encoder power is forcibly supplied.
{% endhint %}

# 8.14 R361 for Setting the Jog Inching Level

R361 jog inching level setting information is as follows.

![](../_assets/image_538.png)

The method to change the inching distance of the currently set level is as follows.

1.	After inputting 361 in the favorites window, touch the \[OK\] button or press the <<b>ENTER</b>> key.

2.	After inputting the unit of the jog inching level \(0: Distance. 1: Angle\), touch the \[OK\] button or press the <<b>ENTER</b>> key.

![](../_assets/image_539.png)


3.	1을 입력한 경우, 인칭 각도를 입력한 후 \[확인\] 버튼을 터치하거나 <<b>ENTER</b>> 키를 누르십시오.
_assets
![](../_assets/image_548.png)

{% hint style="info" %}
* R361 code cannot be used in automatic mode. It must be used in manual mode.
* The inching distance set using the R361 code will be set for the currently set jog level. Therefore, if the current jog speed level is 8, the inching distance corresponding to 8 will be changed.
* Jog inching is possible only when the jog inching key is activated \(LED On\). 
* The jog inching level setting function is for engineers, so it is not supported for general users. Please contact our engineer for details on this function.
{% endhint %}

# 9. Property

When teaching a job program for a welding operation, you should set the arc welding-specific details, such as weaving, retry/restart, and characteristics of the welder, in addition to welding conditions such as voltage and current. Moreover, there are cases in which you should check the position of a step or an auxiliary point.



# 9.1 Use of the property Function

If you use the \[property\] button on the right side of the Hi6 teach pendant screen, you can quickly and easily set the conditions and check the position simply by a single button operation.

![Figure 75 Function for the \[Attributes\] Button](../_assets/image_540.png)

For example, if you touch the \[property\] button while the cursor is on the arcon statement that is for the Arc On function, the contents of the condition number used in the current statement among the welding start conditions will be displayed. On the screen, you can check or change the details of the welding start conditions. Moreover, if there is another condition file associated with the concerned condition file, you can move directly to it. In other words, the \[property\] button allows you to check and change the details of the contents related to a specific statement such as condition file or step position quickly and easily. 



The following shows the method to check and change the condition file and details related to a specific command using the \[property\] button.

1.	Select a specific statement, place the cursor on it, and touch the \[property\] button.

2.	By referring to the following table, you can check and change the file or details related to the selected statement.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Statement</th>
      <th style="text-align:left">File and Contents</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>move</p>
        <p></p>
        <p>refp</p>
        <p></p>
      </td>
      <td style="text-align:left">
        <p>Step position</p>
        <p></p>
        <p>Reference position</p>
      </td>
      <td style="text-align:left">
        <p>Current step position or global pose variable</p>
        <p>X Y Z (mm) Rx Ry Rz (deg) T1&#x2013;T10</p>
        <p>The unit, coordinate system, and robot configuration</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">arcon asf=</td>
      <td style="text-align:left">
        <p>Welding start condition</p>
        <p>Welding auxiliary condition</p>
        <p>Arc welder condition</p>
      </td>
      <td style="text-align:left">
        <ul>
          <li>Welding start condition: Condition number, description, voltage check,
            retry, operation mode, output current, output voltage, WCR waiting time,
            robot delay time, etc.</li>
          <li>Welding auxiliary condition
            <ul>
              <li>Retry: Count, retract time/speed, back step/welding line movement amount,
                shift movement amount, speed, current, voltage</li>
              <li>Restart: Count, overlap amount, moving speed, welding current, voltage,
                current</li>
              <li>Overlap condition setting (in the middle of welding): Arc, gas, wire,
                and coolant</li>
            </ul>
          </li>
          <li>Arc welder condition: Welder number, title, description, power control
            mode, wire diameter, protruding distance, deposition detection time, ARC
            OFF detection time, etc.
            <ul>
              <li>Current properties: Polarity, command value (V), measurement value (A),
                and compensation value</li>
              <li>Voltage properties: Polarity, command value (V), measurement value (V),
                and compensation value</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">arcon aef=</td>
      <td style="text-align:left">
        <p>Welding end condition</p>
        <p>Welding auxiliary condition</p>
      </td>
      <td style="text-align:left">
        <ul>
          <li>Welding end condition: Condition number, description, voltage check, output
            current, output voltage, downslope, condition holding time, and gas postflow</li>
          <li>Welding auxiliary condition: Automatic deposition release: Count, current,
            voltage, delay time</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">weavon wev=</td>
      <td style="text-align:left">Weaving condition</td>
      <td style="text-align:left">
        <ul>
          <li>Weaving condition: Gun number, weaving type, frequency, basic pattern,
            progress angle, boundary limit, moving time, and timer</li>
          <li>Arc sensing condition: Arc sensing, left and right sensing start cycle,
            top and bottom sensing cycle, voltage factor, compensation distance per
            sample, etc.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

3.	Touch the \[Record\] button or press the &lt;esc&gt; key to end the operation.

* \[Record\]: You can save the changes and end the operation.
* &lt;esc&gt;: You can cancel the change and end the operation.





# 9.2 Move-Step Position

You can check or modify the position of the step in the currently selected line in the JOB program.

# 9.2.1 Hidden Pose Move Statement

You can check or modify the position of the current step in the hidden pose move statement \(step recorded using the \[Record\] button, that is, a move statement that does not include a pose variable\).

1.	Touch the \[property\] button in the move command \(move statement\) recorded as a hidden pose. Then, the current step position will appear. 

2.	Check and modify the current step position.

![](../../_assets/image_544.png)



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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Position information of the current step. You can check and set the name,
          coordinate value and coordinate system format, etc.</p>
        <ul>
          <li>[Name]: Number of the current step. After inputting the step number, press
            the <b><<b>ENTER</b>> </b>key to move to the concerned step.</li>
          <li>Coordinate Value: Current coordinate value of the current step
            <ul>
              <li>Select an item using the cursor key.</li>
              <li>After inputting a value in the desired item, press the <<b>ENTER</b>> key
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
        <img src="../../_assets/c2.png" alt/>
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
  For the designation according to the robot configuration, refer to ???[2.3.2.2 Base and Robot Recording Coordinates](../../2-operation/3-step/2-step-pose-modify/2-base-robot-crd-sys.md).???
{% endhint %}

# 9.2.2 Pose Recording Move Statement and Pose Assign Statement

You can edit the pose variable value in the move statement, including the pose variable or the pose variable assign statement.

1.	Touch the \[property\] button in the move command \(move statement\) recorded as a pose variable. Then, the pose variable setting screen will appear.

2.	Check and modify the current pose variable.

![](../../_assets/image_547.png)





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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Current pose variable information. You can check and set the name, coordinate
          value, coordinate system format, etc.</p>
        <ul>
          <li>[Name]: Name of the current pose variable</li>
          <li>Coordinate value: The coordinate value of the current pose variable
            <ul>
              <li>Select an item using the cursor key.</li>
              <li>After inputting a value in the desired item, press the <b><<b>ENTER</b>></b> key
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
              <li>For details on the robot configuration, refer to &#x201C;<a href="../../operation/step/step-pose-modify/">2.3.2 Recording and Changing a Step Position</a><b>.</b>&#x201D;</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
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

* If you end the operation by pressing the <**ESC**> key, the change will not be saved. 





# 9.3 Spot Welding Function

When writing the SPOT command while writing the program, if you place the cursor on the spot welding function position in manual mode and touch the \[property\] button, then the \[1: Spot Welding\] menu will be highlighted in the application parameter setting menu screen. Using the spot welding function, you can quickly modify the contents of the welding conditions and also of the welding sequence when performing spot welding.

![Figure 76 Spot Welding Function](../_assets/image_543.png)

{% hint style="info" %}
* You can use the spot welding function by touching the \[Set Up\] button &gt; \[4: Application Parameter &gt; 1: Spot Welding\].
* 
  For details on the spot welding function, refer to the “Hi6 Controller Spot Welding Function Manual.”
{% endhint %}

# 10. Robot Language

For details on the robot language, refer to the "[Hi6 Robot Controller Function Manual. - Robot Language HRScript](https://hrbook-hrc.web.app/#/view/doc-hrscript/english/README)"
# Appendices

  


# Rules on Occupational Safety and Health Standards, and Notice for Safety Inspection

The industrial robot should be installed in consideration of the inspection standards both of the Rules on Occupational Safety and Health Standards and of the Notice for Safety Inspection \(if subject to inspection\).

"[Rules on Occupational Safety and Health Standards](https://hrbook-hrc.web.app/#/view/rules-on-occupational-safety-and-health-standards/english/README)"
# Quality Assurance

"[Quality Assurance](https://hrbook-hrc.web.app/#/view/quality-assurance/english/README)"
