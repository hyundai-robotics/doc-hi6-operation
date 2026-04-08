# 7.5.23 S-curve Condition

The S-curve refers to motion-trajectory planning that adjusts path accuracy and residual vibration according to the task, enabling the design of an optimal process

![](../../../_assets/tp630/s-curve_velocity_comparison.png)

The image compares the default velocity-profiling method with the S-curve velocity-profiling method.

Default (blue solid line): Acceleration starts and ends with abrupt changes in acceleration, which can cause vibration.
S-curve (red dashed line): The speed change during acceleration and deceleration is performed more smoothly. This minimizes robot vibration and reduces path error even when the motion speed changes.

{% hint style="warning" %}
* If continuous motion generation fails, the motion will run as a discontinuous (broken) motion. In that region, adjust the parameters or switch back to the default motion (Default) for reliable operation.
* History logs can be used to view records of continuous-motion failures.
{% endhint %}

{% hint style="info" %}
* This feature is supported from version V70.00-00 onward.
* Refer to the command syntax in the ${cont_model} controller manual "[5.22 scurve](https://hrbook-hrc.web.app/#/view/doc-hrscript/en/5-moving-robot/22-s-curve?cont_model=${cont_model})"
{% endhint %}
