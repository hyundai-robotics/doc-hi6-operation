# 2.3.1 스텝 명령문 인수

스텝 명령문 인수\(Parameter\)는 로봇 스텝의 이동에 필요한 이동 명령 move 이외의 이동 조건으로 로봇의 위치, 보간, 속도, Accuracy, 툴 번호 등이 있습니다.

스텝 명령문 인수에는 기본 인수와 선택 인수가 있습니다. 기본 인수는 스텝에 필수적인 인수이고 선택 인수는 필요에 따라 추가할 수 있는 인수입니다.

스텝 명령문은 다음과 같이 구성됩니다.

![](../../../.gitbook/assets/image%20%2856%29.png)



<table>
  <thead>
    <tr>
      <th style="text-align:left">&#xBC88;&#xD638;</th>
      <th style="text-align:left">&#xC778;&#xC218;</th>
      <th style="text-align:left">&#xC124;&#xBA85;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">&#xBCF4;&#xAC04;</td>
      <td style="text-align:left">
        <p>&#xC2A4;&#xD15D;&#xACFC; &#xC2A4;&#xD15D; &#xC0AC;&#xC774;&#xC758; &#xBCF4;&#xAC04;&#xB41C;
          &#xACBD;&#xB85C;</p>
        <p>P (&#xCD95;&#xBCF4;&#xAC04;), L (&#xC9C1;&#xC120;&#xBCF4;&#xAC04;), C
          (&#xC6D0;&#xD638;&#xBCF4;&#xAC04;), SP (&#xC815;&#xCE58;&#xD234;&#xBCF4;&#xAC04;
          Off), SL (&#xC815;&#xCE58;&#xD234; &#xC9C1;&#xC120;&#xBCF4;&#xAC04;), SC
          (&#xC815;&#xCE58;&#xD234; &#xC6D0;&#xD638;&#xBCF4;&#xAC04;)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">&#xD3EC;&#xC988;</td>
      <td style="text-align:left">
        <p>&#xC704;&#xCE58;&#xB97C; &#xAE30;&#xB85D;&#xD558;&#xB294; &#xC778;&#xC218;.
          &#xC774; &#xC778;&#xC218;&#xAC00; &#xC0DD;&#xB7B5;&#xB418;&#xACE0; &#xBA85;&#xB839;&#xBB38;
          &#xB4A4;&#xC5D0; &#xD3EC;&#xC988;&#xAC00; &#xC9C0;&#xC815;&#xB420; &#xC218;&#xB3C4;
          &#xC788;&#xC2B5;&#xB2C8;&#xB2E4;(&#xC228;&#xC740; &#xD3EC;&#xC988;).</p>
        <p>Target &#xD3EC;&#xC988;(X, Y, Z, Rx, Ry, Rz, Cfg){&#xC88C;&#xD45C;&#xACC4;}
          + &#xC2DC;&#xD504;&#xD2B8;(X, Y, Z, Rx, Ry, Rz){&#xC88C;&#xD45C;&#xACC4;}</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c3.png" alt/>
      </td>
      <td style="text-align:left">&#xC18D;&#xB3C4;</td>
      <td style="text-align:left">&#xB85C;&#xBD07;&#xC758; &#xC6B4;&#xC804; &#xC18D;&#xB3C4;(&#xB2E8;&#xC704;:
        mm/sec, cm/min, %, sec)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c4.png" alt/>
      </td>
      <td style="text-align:left">Accuracy</td>
      <td style="text-align:left">&#xB85C;&#xBD07;&#xC774; &#xBAA9;&#xD45C; &#xC2A4;&#xD15D;&#xC73C;&#xB85C;
        &#xC774;&#xB3D9;&#xD560; &#xB54C; &#xBC1C;&#xC0DD;&#xD558;&#xB294; &#xD604;&#xC7AC;
        &#xC704;&#xCE58;&#xC640; &#xAE30;&#xB85D; &#xC704;&#xCE58;&#xC758; &#xD5C8;&#xC6A9;
        &#xC624;&#xCC28;&#xAC12;(0 ~ 7)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c5.png" alt/>
      </td>
      <td style="text-align:left">&#xD234; &#xBC88;&#xD638;</td>
      <td style="text-align:left">&#xC0AC;&#xC6A9;&#xD558;&#xB294; &#xD234;&#xC758; &#xBC88;&#xD638;(0 ~
        31)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c6.png" alt/>
      </td>
      <td style="text-align:left">&#xC815;&#xC9C0; &#xC870;&#xAC74;</td>
      <td style="text-align:left">&#xB85C;&#xBD07;&#xC774; &#xB2E4;&#xC74C; &#xBA85;&#xB839;(&#xC2A4;&#xD15D;
        &#xB610;&#xB294; &#xD391;&#xC158;)&#xC744; &#xC218;&#xD589;&#xD558;&#xAE30;
        &#xC704;&#xD574; &#xC774;&#xB3D9;&#xC744; &#xC815;&#xC9C0;&#xD558;&#xAE30;
        &#xC704;&#xD55C; &#xC870;&#xAC74;</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c7.png" alt/>
      </td>
      <td style="text-align:left">&#xC8FC;&#xC11D;</td>
      <td style="text-align:left">&#xC2A4;&#xD15D;&#xC5D0; &#xB300;&#xD55C; &#xC124;&#xBA85;</td>
    </tr>
  </tbody>
</table>

