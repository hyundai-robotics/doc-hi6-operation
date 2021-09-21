# 7.6.4 시리얼 엔코더 리셋

시리얼 엔코더는 내부 메모리에 엔코더 회전수 정보를 저장합니다. 모터의 에러 상태를 해제하거나 엔코더의 영점을 리셋하여 엔코더의 회전수를 0으로 클리어할 수 있습니다.

1. \[5: 초기화 &gt; 4: 시리얼 엔코더 리셋\] 메뉴를 터치하십시오.
2. 각 축의 엔코더 리셋 모드를 설정하고 상태를 확인한 후 리셋을 실행하십시오.

![](../../.gitbook/assets/image%20%28231%29.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#xBC88;&#xD638;</th>
      <th style="text-align:left">&#xC124;&#xBA85;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>&#xCD95;&#xBCC4;&#xB85C; &#xC5D4;&#xCF54;&#xB354; &#xB9AC;&#xC14B; &#xC0AC;&#xC6A9;
          &#xC5EC;&#xBD80;&#xC640; &#xBAA8;&#xB4DC;&#xB97C; &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</p>
        <ul>
          <li>[&#xBB34;&#xD6A8;]: &#xC2DC;&#xB9AC;&#xC5BC; &#xC5D4;&#xCF54;&#xB354;
            &#xB9AC;&#xC14B;&#xC744; &#xC2E4;&#xD589;&#xD558;&#xC9C0; &#xC54A;&#xC2B5;&#xB2C8;&#xB2E4;.</li>
          <li>[&#xC5D0;&#xB7EC;&#xD574;&#xC81C;]: &#xC5D4;&#xCF54;&#xB354; &#xD68C;&#xC804;&#xC218;&#xB97C;
            &#xD074;&#xB9AC;&#xC5B4;&#xD558;&#xC9C0; &#xC54A;&#xACE0; &#xBAA8;&#xD130;&#xC758;
            &#xC5D4;&#xCF54;&#xB354; &#xAD00;&#xB828; &#xC5D0;&#xB7EC;&#xB9CC; &#xD574;&#xC81C;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>[&#xC5D4;&#xCF54;&#xB354; &#xB9AC;&#xC14B;]: &#xBAA8;&#xD130;&#xC758;
            &#xC5D4;&#xCF54;&#xB354; &#xAD00;&#xB828; &#xC5D0;&#xB7EC;&#xB97C; &#xD574;&#xC81C;&#xD558;&#xACE0;
            &#xC5D4;&#xCF54;&#xB354;&#xC758; &#xC601;&#xC810;&#xC744; &#xB9AC;&#xC14B;&#xD558;&#xC5EC;
            &#xD68C;&#xC804;&#xC218;&#xB97C; &#xD074;&#xB9AC;&#xC5B4;&#xD569;&#xB2C8;&#xB2E4;.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[&#xC2E4;&#xD589;]: &#xC2DC;&#xB9AC;&#xC5BC; &#xC5D4;&#xCF54;&#xB354;
            &#xB9AC;&#xC14B;&#xC744; &#xC2E4;&#xD589;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>[&#xC804;&#xCD95;&#xC120;&#xD0DD;]: &#xBAA8;&#xB4E0; &#xCD95;&#xC744;
            &#xD55C; &#xBC88;&#xC5D0; &#xC120;&#xD0DD;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>[&#xC804;&#xCD95;&#xD574;&#xC81C;]: &#xBAA8;&#xB4E0; &#xCD95;&#xC758;
            &#xC120;&#xD0DD;&#xC744; &#xD55C; &#xBC88;&#xC5D0; &#xD574;&#xC81C;&#xD569;&#xB2C8;&#xB2E4;.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
* 로봇 시스템의 초기화 설정 수행 시에 엔코더 리셋을 수행하고 로봇이 정상 동작 중에는 절대 엔코더 리셋을 수행해서는 안 됩니다. 다만, 통신 이상 등의 엔코더 관련 에러가 발생하거나 엔코더 배터리가 소실된 경우에는 엔코더 리셋을 수행할 수 있습니다. 이때에는 기존의 로봇 원점 위치와 달라지지 않도록 로봇 프로그램의 실제 위치를 확인하여 작업하십시오.
* 제어기와 엔코더에 전원이 공급되지 않으면 엔코더의 위치 정보가 손실되어 로봇 작업 프로그램 사용에 문제가 발생할 수 있습니다. 이를 해결하기 위해 시리얼 엔코더에 전용 배터리를 부착하여 제어기의 전원 상태에 관계없이 위치 정보를 기록합니다. 엔코더 배터리에 전압 에러가 발생하면 반드시 제어기의 전원이 켜져 있는 상태에서 배터리를 교체하여 위치 정보의 손실을 예방하십시오.
{% endhint %}

