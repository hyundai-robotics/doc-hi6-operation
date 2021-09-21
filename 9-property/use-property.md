# 9.1 속성 기능 사용

Hi6 티치 펜던트 화면 우측의 \[속성\] 버튼을 이용하면 이러한 조건 설정과 위치 확인을 한 번의 버튼 조작으로 쉽고 빠르게 수행할 수 있습니다.

![&#xADF8;&#xB9BC; 76 \[&#xC18D;&#xC131;\] &#xBC84;&#xD2BC;&#xC758; &#xAE30;&#xB2A5;](../.gitbook/assets/image%20%28268%29.png)

예를 들어, Arc On 기능을 하는arcon 명령문에 커서가 있을 때 \[속성\] 버튼을 터치하면 용접 시작 조건 중 현재 명령문에서 사용하는 조건 번호의 내용이 표시됩니다. 화면에서 용접 시작 조건의 세부 내용을 확인하거나 변경할 수 있습니다. 또한 해당 조건 파일과 연관된 다른 조건 파일이 있을 경우 그곳으로 바로 이동할 수 있습니다. 즉, \[속성\] 버튼은 특정 명령문과 관련된 조건 파일이나 스텝 위치 등 세부 연관 내용을 쉽고 빠르게 확인하고 변경할 수 있게 해 줍니다.

\[속성\] 버튼을 이용하여 특정 명령문과 관련된 조건 파일 및 상세 내용을 확인하고 변경하는 방법은 다음과 같습니다.

1. 특정 명령문을 선택하여 커서를 두고 \[속성\] 버튼을 터치하십시오.
2. 다음 표의 내용을 참고하여 선택한 명령문과 관련된 파일이나 상세 내용을 확인 및 변경하십시오.

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#xBA85;&#xB839;&#xBB38;</th>
      <th style="text-align:left">&#xD30C;&#xC77C; &#xBC0F; &#xB0B4;&#xC6A9;</th>
      <th style="text-align:left">&#xC124;&#xBA85;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>move
          <br />
        </p>
        <p>refp</p>
      </td>
      <td style="text-align:left">
        <p>&#xC2A4;&#xD15D; &#xC704;&#xCE58;
          <br />
        </p>
        <p>&#xCC38;&#xC870; &#xC704;&#xCE58;</p>
      </td>
      <td style="text-align:left">
        <p>&#xD604;&#xC7AC; &#xC2A4;&#xD15D; &#xC704;&#xCE58; &#xB610;&#xB294; &#xC804;&#xC5ED;
          &#xD3EC;&#xC988; &#xBCC0;&#xC218;</p>
        <p>X Y Z (&#x339C;) Rx Ry Rz (deg) T1 ~ T10</p>
        <p>&#xC720;&#xB2DB;, &#xC88C;&#xD45C;&#xACC4;, &#xB85C;&#xBD07; Configuration</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">arcon asf=</td>
      <td style="text-align:left">
        <p>&#xC6A9;&#xC811; &#xC2DC;&#xC791; &#xC870;&#xAC74;</p>
        <p>&#xC6A9;&#xC811; &#xBCF4;&#xC870; &#xC870;&#xAC74;</p>
        <p>&#xC544;&#xD06C; &#xC6A9;&#xC811;&#xAE30; &#xC870;&#xAC74;</p>
      </td>
      <td style="text-align:left">
        <ul>
          <li>&#xC6A9;&#xC811; &#xC2DC;&#xC791; &#xC870;&#xAC74;: &#xC870;&#xAC74; &#xBC88;&#xD638;,
            &#xC124;&#xBA85;, &#xC804;&#xC555; &#xD655;&#xC778;, &#xC7AC;&#xC2DC;&#xB3C4;,
            &#xB3D9;&#xC791; &#xBAA8;&#xB4DC;, &#xCD9C;&#xB825; &#xC804;&#xB958;, &#xCD9C;&#xB825;
            &#xC804;&#xC555;, WCR &#xB300;&#xAE30; &#xC2DC;&#xAC04;, &#xB85C;&#xBD07;
            &#xC9C0;&#xC5F0; &#xC2DC;&#xAC04; &#xB4F1;</li>
          <li>&#xC6A9;&#xC811; &#xBCF4;&#xC870; &#xC870;&#xAC74;
            <ul>
              <li>RETRY: &#xD69F;&#xC218;, RETRACT&#xC2DC;&#xAC04;/&#xC18D;&#xB3C4;, &#xD6C4;&#xD1F4;/&#xC6A9;&#xC811;&#xC120;
                &#xC774;&#xB3D9;&#xB7C9;, &#xC26C;&#xD504;&#xD2B8; &#xC774;&#xB3D9;&#xB7C9;,
                &#xC18D;&#xB3C4;, &#xC804;&#xB958;, &#xC804;&#xC555;</li>
              <li>RESTART: &#xD69F;&#xC218;, &#xC911;&#xCCA9;&#xB7C9;, &#xC774;&#xB3D9;
                &#xC18D;&#xB3C4;, &#xC6A9;&#xC811; &#xC804;&#xB958;, &#xC804;&#xC555;,
                &#xC804;&#xB958;</li>
              <li>(&#xC6A9;&#xC811; &#xC911;)&#xC624;&#xBC84;&#xB7A9; &#xC870;&#xAC74; &#xC124;&#xC815;:
                &#xC544;&#xD06C;, &#xAC00;&#xC2A4;, &#xC640;&#xC774;&#xC5B4;, &#xB0C9;&#xAC01;&#xC218;</li>
            </ul>
          </li>
          <li>&#xC544;&#xD06C; &#xC6A9;&#xC811;&#xAE30; &#xC870;&#xAC74;: &#xC6A9;&#xC811;&#xAE30;
            &#xBC88;&#xD638;, &#xBA85;&#xCE6D;, &#xC124;&#xBA85;, &#xC804;&#xC6D0;
            &#xC81C;&#xC5B4; &#xBAA8;&#xB4DC;, &#xC640;&#xC774;&#xC5B4; &#xC9C1;&#xACBD;,
            &#xB3CC;&#xCD9C; &#xAE38;&#xC774;, &#xC6A9;&#xCC29; &#xAC80;&#xCD9C; &#xC2DC;&#xAC04;,
            ARC OFF &#xAC80;&#xCD9C; &#xC2DC;&#xAC04; &#xB4F1;
            <ul>
              <li>&#xC804;&#xB958; &#xD2B9;&#xC131;: &#xADF9;&#xC131;, &#xC9C0;&#xB839;&#xCE58;(V),
                &#xCE21;&#xC815;&#xCE58;(A), &#xBCF4;&#xC815;&#xCE58;</li>
              <li>&#xC804;&#xC555; &#xD2B9;&#xC131;: &#xADF9;&#xC131;, &#xC9C0;&#xB839;&#xCE58;(V),
                &#xCE21;&#xC815;&#xCE58;(V), &#xBCF4;&#xC815;&#xCE58;</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">arcon aef=</td>
      <td style="text-align:left">
        <p>&#xC6A9;&#xC811; &#xC885;&#xB8CC; &#xC870;&#xAC74;</p>
        <p>&#xC6A9;&#xC811; &#xBCF4;&#xC870; &#xC870;&#xAC74;</p>
      </td>
      <td style="text-align:left">
        <ul>
          <li>&#xC6A9;&#xC811; &#xC885;&#xB8CC; &#xC870;&#xAC74;: &#xC870;&#xAC74; &#xBC88;&#xD638;,
            &#xC124;&#xBA85;, &#xC804;&#xC555; &#xD655;&#xC778;, &#xCD9C;&#xB825; &#xC804;&#xB958;,
            &#xCD9C;&#xB825; &#xC804;&#xC555;, &#xB2E4;&#xC6B4; &#xC2AC;&#xB85C;&#xD504;,
            &#xC870;&#xAC74; &#xC720;&#xC9C0; &#xC2DC;&#xAC04;, &#xAC00;&#xC2A4; &#xD6C4;&#xCD9C;</li>
          <li>&#xC6A9;&#xC811; &#xBCF4;&#xC870; &#xC870;&#xAC74;: &#xC790;&#xB3D9; &#xC6A9;&#xCC29;
            &#xD574;&#xC81C; &#xD69F;&#xC218;, &#xC804;&#xB958;, &#xC804;&#xC555;,
            &#xC9C0;&#xC5F0;&#xC2DC;&#xAC04;</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">weavon wev=</td>
      <td style="text-align:left">&#xC704;&#xBE59; &#xC870;&#xAC74;</td>
      <td style="text-align:left">
        <ul>
          <li>&#xC704;&#xBE59; &#xC870;&#xAC74;: &#xAC74; &#xBC88;&#xD638;, &#xC704;&#xBE59;
            &#xD615;&#xD0DC;, &#xC8FC;&#xD30C;&#xC218;, &#xAE30;&#xBCF8; &#xD328;&#xD134;,
            &#xC9C4;&#xD589; &#xAC01;&#xB3C4;, &#xACBD;&#xACC4; &#xC81C;&#xD55C;, &#xC774;&#xB3D9;
            &#xC2DC;&#xAC04;, &#xD0C0;&#xC774;&#xBA38;</li>
          <li>&#xC544;&#xD06C; &#xC13C;&#xC2F1; &#xC870;&#xAC74;: &#xC544;&#xD06C; &#xC13C;&#xC2F1;,
            &#xC88C;&#xC6B0; &#xC13C;&#xC2F1; &#xC2DC;&#xC791; &#xC0AC;&#xC774;&#xD074;,
            &#xC0C1;&#xD558; &#xC13C;&#xC2F1; &#xC2DC;&#xC791; &#xC0AC;&#xC774;&#xD074;,
            &#xC804;&#xC555; &#xACC4;&#xC218;, &#xC0D8;&#xD50C;&#xB2F9; &#xBCF4;&#xC815;
            &#xAC70;&#xB9AC; &#xB4F1;</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

1. \[기록\] 버튼을 터치하거나 &lt;esc&gt; 키를 눌러 작업을 종료하십시오.
2. \[기록\]: 변경 내용을 저장하고 작업을 종료합니다.
3. &lt;esc&gt;: 변경 내용을 취소하고 작업을 종료합니다

