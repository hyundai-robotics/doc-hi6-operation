# 7.3.5 원위치 등록

로봇의 임의 자세를 원위치로 등록하여 로봇이 이 위치에 들어왔을 때 원위치 신호를 출력 신호란에 출력할 수 있습니다. 원위치는 축별 자세로 지정하고 8 개까지 등록하여 사용할 수 있으며 축별 마진을 추가로 설정할 수 있습니다.

1.	\[2: 제어 파라미터 &gt; 5: 원위치 등록\] 메뉴를 터치하십시오.

2.	원위치 탭을 선택하고 사용 여부와 출력 신호, 축각도와 범위를 설정하십시오.

![](../../.gitbook/assets/image%20%2888%29.png)

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
        <p>&#xD0ED;&#xC5D0;&#xC11C; &#xC120;&#xD0DD;&#xD55C; &#xC6D0;&#xC704;&#xCE58;&#xC758;
          &#xC0C1;&#xC138; &#xC815;&#xBCF4;&#xC785;&#xB2C8;&#xB2E4;. &#xC0AC;&#xC6A9;
          &#xC5EC;&#xBD80;&#xC640; &#xCD9C;&#xB825; &#xC2E0;&#xD638;, &#xCD95;&#xAC01;&#xB3C4;&#xC640;
          &#xBC94;&#xC704;, &#xC124;&#xBA85;&#xC744; &#xC124;&#xC815;&#xD560; &#xC218;
          &#xC788;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <ul>
          <li>[&#xC0AC;&#xC6A9; &#xC5EC;&#xBD80;]: &#xC0AC;&#xC6A9; &#xC5EC;&#xBD80;&#xB97C;
            &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>[&#xCD9C;&#xB825; &#xC2E0;&#xD638;]: &#xCD9C;&#xB825; &#xC2E0;&#xD638;
            &#xBC88;&#xD638;&#xB97C; &#xC785;&#xB825;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>[&#xCD95;&#xAC01;&#xB3C4;]/[&#xBC94;&#xC704;]: &#xC6D0;&#xC704;&#xCE58;&#xC5D0;&#xC11C;
            &#xB85C;&#xBD07;&#xC758; &#xCD95;&#xAC01;&#xB3C4;&#xC640; &#xBC94;&#xC704;&#xB97C;
            &#xC785;&#xB825;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>&#xBC94;&#xC704;&#xAC00; 0&#xC73C;&#xB85C; &#xC124;&#xC815;&#xB41C; &#xACBD;&#xC6B0;,
            &#xD574;&#xB2F9; &#xCD95;&#xC5D0; &#xB300;&#xD574;&#xC11C;&#xB294; &#xC6D0;&#xC704;&#xCE58;
            &#xAC80;&#xC0AC;&#xB97C; &#xC218;&#xD589;&#xD558;&#xC9C0; &#xC54A;&#xC2B5;&#xB2C8;&#xB2E4;.</li>
          <li>&#xBC94;&#xC704;&#xB294; &#xC6D0;&#xC704;&#xCE58; &#xD3EC;&#xC778;&#xD2B8;&#xC758;
            + &#xBC29;&#xD5A5;&#xACFC; - &#xBC29;&#xD5A5;&#xC758; &#xBC94;&#xC704;&#xB85C;
            &#xC0AC;&#xC6A9;&#xD569;&#xB2C8;&#xB2E4;. &#xC608;&#xB97C; &#xB4E4;&#xC5B4;,
            &#xBC94;&#xC704;&#xB97C; 0.5&#xB85C; &#xC124;&#xC815;&#xD558;&#xBA74; &#xC6D0;&#xC704;&#xCE58;
            &#xC2E0;&#xD638;&#xC758; &#xCD9C;&#xB825; &#xBC94;&#xC704;&#xB294; 1&#xC774;
            &#xB429;&#xB2C8;&#xB2E4;.</li>
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
          <li>[&#xD604;&#xC7AC; &#xB85C;&#xBD07; &#xD3EC;&#xC988;]: &#xD604;&#xC7AC;
            &#xB85C;&#xBD07; &#xC790;&#xC138;&#xC758; &#xCD95;&#xAC01;&#xB3C4;&#xC640;
            &#xBC94;&#xC704;&#xAC00; &#xC790;&#xB3D9;&#xC73C;&#xB85C; &#xC785;&#xB825;&#xB429;&#xB2C8;&#xB2E4;.</li>
          <li>[&#xD504;&#xB85C;&#xADF8;&#xB7A8;/&#xC2A4;&#xD15D;]: &#xD504;&#xB85C;&#xADF8;&#xB7A8;&#xACFC;
            &#xC2A4;&#xD15D; &#xBC88;&#xD638;&#xB97C; &#xC785;&#xB825;&#xD558;&#xBA74;
            &#xD574;&#xB2F9; &#xC2A4;&#xD15D;&#xC758; &#xCD95;&#xAC01;&#xB3C4;&#xC640;
            &#xBC94;&#xC704;&#xAC00; &#xC790;&#xB3D9;&#xC73C;&#xB85C; &#xC785;&#xB825;&#xB429;&#xB2C8;&#xB2E4;.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

