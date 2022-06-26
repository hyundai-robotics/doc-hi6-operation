# 2.3.2.2 베이스 및 로봇 기록 좌표

로봇의 위치와 자세는 좌표계에 따라 다르게 나타낼 수 있습니다. 주행 축이 없는 경우, 일반적으로 베이스 좌표와 로봇 좌표가 동일합니다. 주행 축이 정의된 경우, 로봇 툴의 위치와 자세는 베이스 좌표와 로봇 좌표에 따라 다르게 나타납니다.

수동 모드에서 \[설정 &gt; 1: 사용자 환경\] 메뉴의 \[1: POSE 기록 형태\] 옵션이 베이스 또는 로봇으로 설정된 경우, move 명령문에서 \[속성\] 버튼을 터치하십시오. 속성창에서 로봇 툴의 위치와 자세를 확인할 수 있습니다.

{% hint style="info" %}
Pose 기록 형태를 변경하려면 고객지원팀에 문의하여 전문가에게 의뢰하거나 엔지니어에게 문의하십시오.
{% endhint %}

하나의 툴 끝 위치 및 방향에 대해서, 기구의 특성상 여러 자세가 있을 수 있으므로, 하나의 자세로 정의하려면 로봇 형태\(config.\)를 지정해야 합니다.

협동로봇의 경우, 기구학적 구조에 의해 소프트 리밋에 제한될 수 있습니다. 로봇이 동작하지 않을 때 소프트 리밋을 해제하거나 큰 값으로 설정하여 사용할 수 있습니다.

* auto \(자동\): 현재 로봇이 취하고 있는 자세에 대하여 이후의 항목들을 설정하지 않고 자동으로 결정합니다. 지정하지 않으면 아래의 항목들의 지정여부로 결정합니다.
* back \(뒤쪽\): 로봇의 툴 끝이 로봇 좌표계의 X축-방향인 뒤쪽입니다. 지정하지 않으면 + 방향인 앞쪽입니다.
* down \(하\): H축과 V축의 관계입니다. 지정하면 하, 지정하지 않으면 상입니다.

![그림 23 H축과 V축 자세: 상\(좌\), 하\(우\)](../../../_assets/image_58_1.png)

* flip \(플립\): B축의 좌표가 + 값인 플립입니다. 지정하지 않으면 - 값인 논플립\(non-flip\)입니다. 그림의 적색 화살표는 손목축의 상부 방향을 나타냅니다.

![그림 24 Flip \(좌\) / Non-flip \(우\) 자세](../../../_assets/image_75.png)

* S \(\|S\|&gt;=180\): S축 각도의 절대값이 180도 이상입니다. 지정하지 않으면 180도 미만입니다. 
* B \(\|B\|&gt;=180\): B축 각도의 절대값이 180도 이상입니다. 지정하지 않으면 180도 미만입니다.
* R2 \(\|R2\|&gt;=180\): R2축 각도의 절대값이 180도 이상입니다. 지정하지 않으면 180도 미만입니다.
* R1 \(\|R1\|&gt;=180\): R1축 각도의 절대값이 180도 이상입니다. 지정하지 않으면 180도 미만입니다.

좌표계는 \[포즈변수\].crd로 저장되며\(예: po32.crd\) 다음의 문자열 중 하나가 지정됩니다. 공문자열이면 기본값이 joint로 인식됩니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>베이스 좌표계 = &quot;base&quot;
          <br
          />
        </p>
        <p>로봇 좌표계 = &quot;robot&quot;
          <br />
        </p>
        <p>축 좌표계 = &quot;joint&quot;
          <br />
        </p>
        <p>엔코더 = &quot;encoder&quot;
          <br />
        </p>
        <p>사용자 좌표계 = &quot;u1&quot; ~ &quot;u10&quot;
          <br
          />
        </p>
      </td>
    </tr>
  </tbody>
</table>
