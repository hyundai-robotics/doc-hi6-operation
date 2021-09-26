# 7.7.1 축 원점 및 툴 길이 최적화

축 원점 및 툴 길이 최적화는 외부 측정센서를 사용하지 않고 로봇 각 축의 원점 및 툴 길이를 캘리브레이션하는 기능입니다.

뾰족한 팁 2 개를 준비하여 하나는 외부에 고정하고 다른 하나는 툴에 고정한 후 외부의 고정 팁을 기준으로 로봇의 툴 끝의 자세만 바꿔 여러 점을 로봇 프로그램으로 기록합니다. 이때 축 원점과 툴 길이를 모두 찾아내려면 7 점, 툴 길이만 찾아내려면 4 점 이상을 교시해야 합니다.

![&#xADF8;&#xB9BC; 68 &#xCD95; &#xC6D0;&#xC810; &#xBC0F; &#xD234; &#xAE38;&#xC774; &#xCD5C;&#xC801;&#xD654; &#xAE30;&#xB2A5; &#xAD50;&#xC2DC; &#xBC29;&#xBC95;](../../.gitbook/assets/image%20%28228%29.png)

축 원점 및 툴 길이 최적화 기능을 이용하면 CAD데이터가 없는 툴 길이 X, Y, Z뿐만 아니라 로봇 H, V, R2, B축의 원점을 최적화하여 찾아낼 수 있습니다.

{% hint style="warning" %}
축 원점 및 툴 길이 최적화 기능을 사용하면 엔코더 옵셋 및 툴 길이가 변경되어 기존에 교시된 프로그램의 작업 위치가 변경됩니다. 그러므로 축 원점 및 툴 길이 최적화는 반드시 교시 프로그램 작성 전에 수행하십시오.
{% endhint %}

{% hint style="info" %}
* 축 원점 및 툴 길이 최적화 기능에서 교시의 정확도는 최대 스텝 위치 오차 결과의 정확성과 비례합니다. 따라서 뾰족한 두 팁을 준비하여 이 두 팁을 가능한 한 정확히 일치하는 교시 작업이 요구됩니다. 툴 끝과 공간상의 고정점의 일치 정확도가 육안 확인 시 0.5 ㎜ 이내가 되도록 합니다.
* 스텝의 자세가 유사하지 않도록 스텝별로 가능한 한 30 deg 이상 차이를 둔 자세를 설정하여 티칭하십시오.
* 스텝의 손목 축\(R2, B, R1\)을 가능한 한 크게 동작시키고 스텝별 손목 축의 각도 차이를 충분히\(가능한 한 크게\) 두고 티칭하십시오.
{% endhint %}

축 원점 및 툴 길이 최적화 기능의 사용 방법은 다음과 같습니다.

1. \[6: 자동 캘리브레이션 &gt; 1: 축 원점 및 툴 길이 최적화\] 메뉴를 터치하십시오.
2. 최적화 대상을 선택하고 상세 옵션을 설정하십시오.

![](../../.gitbook/assets/image%20%28234%29.png)

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
        <p>&#xBD80;&#xAC00;&#xCD95;&#xC758; &#xC0C1;&#xC138; &#xD30C;&#xB77C;&#xBBF8;&#xD130;
          &#xC124;&#xC815; &#xC815;&#xBCF4;&#xC785;&#xB2C8;&#xB2E4;. &#xBD80;&#xAC00;&#xCD95;
          &#xC774;&#xB984;&#xACFC; &#xC0AC;&#xC591;, &#xAD6C;&#xC131; &#xB4F1;&#xC744;
          &#xD655;&#xC778;&#xD558;&#xACE0; &#xC124;&#xC815;&#xD560; &#xC218; &#xC788;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <ul>
          <li>[&#xCD5C;&#xC801;&#xD654; &#xC120;&#xD0DD;]: &#xCD5C;&#xC801;&#xD654;
            &#xB300;&#xC0C1;&#xC744; &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.
            <ul>
              <li>[&#xD234; &#xAE38;&#xC774;]: &#xB85C;&#xBD07;&#xC758; &#xD234; &#xAE38;&#xC774;
                &#xAC12;&#xC744; &#xBCF4;&#xC815;&#xD569;&#xB2C8;&#xB2E4;. &#xB85C;&#xBD07;
                &#xC6D0;&#xC810;&#xC774; &#xC815;&#xD655;&#xD788; &#xC124;&#xC815;&#xB41C;
                &#xACBD;&#xC6B0;&#xC5D0;&#xB294; &#xD234; &#xAE38;&#xC774;&#xB9CC; &#xBCF4;&#xC815;&#xD560;
                &#xC218; &#xC788;&#xC2B5;&#xB2C8;&#xB2E4;.</li>
              <li>[&#xCD95; &#xC6D0;&#xC810; &#xBC0F; &#xD234; &#xAE38;&#xC774;]: &#xB85C;&#xBD07;&#xC758;
                &#xC6D0;&#xC810;&#xACFC; &#xD234; &#xAE38;&#xC774; &#xAC12;&#xC744; &#xBAA8;&#xB450;
                &#xBCF4;&#xC815;&#xD569;&#xB2C8;&#xB2E4;. &#xD1B5;&#xC0C1;&#xC801;&#xC73C;&#xB85C;
                &#xB85C;&#xBD07;&#xC744; &#xC124;&#xCE58;&#xD558;&#xACE0; &#xCD5C;&#xCD08;&#xC5D0;
                &#xC815;&#xD655;&#xD55C; &#xC6D0;&#xC810;&#xC744; &#xC124;&#xC815;&#xD558;&#xACE0;&#xC790;
                &#xD560; &#xB54C; &#xC0AC;&#xC6A9;&#xD569;&#xB2C8;&#xB2E4;.</li>
            </ul>
          </li>
          <li>[&#xD504;&#xB85C;&#xADF8;&#xB7A8; &#xBC88;&#xD638;]: &#xB3D9;&#xC77C;&#xC810;&#xC744;
            &#xC5EC;&#xB7EC; &#xC790;&#xC138;&#xB85C; &#xAE30;&#xB85D;&#xD55C; &#xD504;&#xB85C;&#xADF8;&#xB7A8;&#xC758;
            &#xBC88;&#xD638;&#xB97C; &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>[&#xD234; &#xBC88;&#xD638;]: &#xC790;&#xB3D9; &#xC124;&#xC815;&#xD558;&#xB824;&#xB294;
            &#xD234;&#xC758; &#xBC88;&#xD638;&#xC785;&#xB2C8;&#xB2E4;. &#xC124;&#xC815;&#xC6A9;
            &#xD504;&#xB85C;&#xADF8;&#xB7A8;&#xC5D0; &#xAE30;&#xB85D;&#xB418;&#xC5B4;
            &#xC788;&#xB294; &#xD234; &#xBC88;&#xD638;&#xC640; &#xC77C;&#xCE58;&#xD574;&#xC57C;
            &#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>[&#xC2A4;&#xD15D;&#xC704;&#xCE58; &#xC624;&#xCC28; &#xD5C8;&#xC6A9;&#xBC94;&#xC704;]:
            &#xC790;&#xB3D9; &#xCE98;&#xB9AC;&#xBE0C;&#xB808;&#xC774;&#xC158; &#xACB0;&#xACFC;&#xC758;
            &#xC624;&#xCC28; &#xBC94;&#xC704;&#xB97C; &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;(&#xCD08;&#xAE30;
            &#xC124;&#xC815;&#xAC12; 0.6 &#x339C;). &#xC608;&#xC0C1; &#xC624;&#xCC28;&#xAC00;
            &#xC624;&#xCC28; &#xBC94;&#xC704; &#xB0B4;&#xC774;&#xBA74; &#xC790;&#xB3D9;&#xC73C;&#xB85C;
            &#xC815;&#xC218; &#xB370;&#xC774;&#xD130;&#xB97C; &#xAC31;&#xC2E0;&#xD558;&#xACE0;
            &#xC624;&#xCC28; &#xBC94;&#xC704;&#xB97C; &#xBC97;&#xC5B4;&#xB098;&#xBA74;
            &#xC815;&#xC218;&#xC758; &#xBC18;&#xC601; &#xC5EC;&#xBD80;&#xB97C; &#xC0AC;&#xC6A9;&#xC790;&#xC5D0;&#xAC8C;
            &#xC54C;&#xB824; &#xD655;&#xC778; &#xD6C4; &#xCC98;&#xB9AC;&#xD569;&#xB2C8;&#xB2E4;.</li>
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
          <li>[&#xC2E4;&#xD589;]: &#xC124;&#xC815; &#xC815;&#xBCF4;&#xB97C; &#xBC14;&#xD0D5;&#xC73C;&#xB85C;
            &#xCD5C;&#xC801;&#xD654;&#xB97C; &#xC2E4;&#xD589;&#xD569;&#xB2C8;&#xB2E4;.
            &#xCD5C;&#xC801;&#xD654; &#xACB0;&#xACFC;&#xB294; [&#xCD5C;&#xB300;&#xC2A4;&#xD15D;
            &#xC704;&#xCE58; &#xC624;&#xCC28;]&#xC5D0; &#xB098;&#xD0C0;&#xB0A9;&#xB2C8;&#xB2E4;.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
로봇의 원점과 툴 길이 값을 모두 보정하면 모든 로봇의 원점이 변경되어 기존에 작성된 프로그램의 위치가 변경되므로 주의하십시오.
{% endhint %}

{% hint style="info" %}
* 로봇 각 축의 원점 및 툴 길이는 설정 메뉴에서도 설정할 수 있습니다.
  * 툴 길이: \[설정 &gt; 3: 로봇 파라미터 &gt; 1: 툴 데이터\]
  * 각 축의 원점: \[설정 &gt; 3: 로봇 파라미터 &gt; 2: 축 원점\]
* 각도보정 기능\(\[설정 &gt; 3: 로봇 파라미터 &gt; 1: 툴 데이터\]\)을 이용해 툴 각도를 보정할 경우, 축 원점 및 툴 길이 최적화 기능을 먼저 실행한 후 각도 보정을 실행하십시오. 정확한 툴 데이터를 설정할 수 있습니다.
{% endhint %}

