# 7.4.2 축 원점

각 축의 기구학적 원점 위치를 등록할 수 있습니다.

1. \[3: 로봇 파라미터 &gt; 2: 축 원점\] 메뉴를 터치하십시오.
2. 각 축의 기구학적 원점 위치를 설정하십시오.

![](../../.gitbook/assets/image%20%28212%29.png)

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
        <p>&#xAC01; &#xCD95;&#xC758; &#xAE30;&#xAD6C;&#xD559;&#xC801; &#xC6D0;&#xC810;
          &#xC704;&#xCE58;&#xC758; &#xC0C1;&#xC138; &#xC815;&#xBCF4;&#xC785;&#xB2C8;&#xB2E4;.
          &#xCD95;&#xC758; &#xC5D4;&#xCF54;&#xB354;&#xC640; &#xC704;&#xCE58;&#xB97C;
          &#xC124;&#xC815;&#xD560; &#xC218; &#xC788;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <ul>
          <li>S&#xCD95;: &#xB85C;&#xBD07;&#xACFC; &#xC8FC;&#xBCC0; &#xC9C0;&#xADF8;&#xC758;
            &#xC124;&#xCE58; &#xC0C1;&#xD669;&#xC5D0; &#xB530;&#xB77C; S&#xCD95; &#xC6D0;&#xC810;&#xC744;
            &#xBCC0;&#xACBD;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>R1&#xCD95;: &#xD234;&#xC758; &#xBD80;&#xCC29; &#xBC29;&#xD5A5;&#xC5D0;
            &#xB530;&#xB77C; R1&#xCD95; &#xC6D0;&#xC810;&#xC744; &#xBCC0;&#xACBD;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>H, V, R2, B&#xCD95;: &#xC790;&#xB3D9; &#xCE98;&#xB9AC;&#xBE0C;&#xB808;&#xC774;&#xC158;
            &#xAE30;&#xB2A5;&#xC744; &#xC774;&#xC6A9;&#xD558;&#xC5EC; &#xC790;&#xB3D9;&#xC73C;&#xB85C;
            &#xC124;&#xC815;&#xD560; &#xC218; &#xC788;&#xC2B5;&#xB2C8;&#xB2E4;.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: &#xBCC0;&#xACBD; &#xB0B4;&#xC6A9;&#xC744; &#xC800;&#xC7A5;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>[&#xC801;&#xC6A9;]: &#xC120;&#xD0DD;&#xB41C; &#xCD95; &#xC815;&#xBCF4;&#xC5D0;
            &#xC120;&#xD0DD;&#xD55C; &#xC6D0;&#xC810; &#xC704;&#xCE58;&#xB97C; &#xC801;&#xC6A9;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>[&#xC804;&#xCCB4;&#xC801;&#xC6A9;]: &#xBAA8;&#xB4E0; &#xCD95; &#xC815;&#xBCF4;&#xC5D0;
            &#xC120;&#xD0DD;&#xD55C; &#xC6D0;&#xC810; &#xC704;&#xCE58;&#xB97C; &#xC801;&#xC6A9;&#xD569;&#xB2C8;&#xB2E4;.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
* 축 원점 설정은 로봇의 직교 동작 정확도에 영향을 미칩니다. 가능한 한 정확한 값으로 변경하십시오.
* 축 원점 설정이 변경되면 기존에 작성된 프로그램의 위치가 변경되므로 축 원점 설정은 반드시 초기 설치 단계에서만 실행하십시오.
* 엔코더 옵셋 설정이 변경되면 축 원점을 새로 설정해야 하므로 반드시 엔코더 옵셋 설정을 완료한 후에 축 원점을 설정하십시오.
{% endhint %}

{% hint style="info" %}
공장 출하 시에는 각 축의 기구학적 원점 위치가 표준값\(0X400000\)으로 설정되어 있습니다.
{% endhint %}

