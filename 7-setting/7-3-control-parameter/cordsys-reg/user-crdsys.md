# 7.3.6.1 사용자 좌표계

사용자 좌표계는 사용자\(User\)가 지정하는 위치에 설정하는 좌표계입니다. 사용자 좌표계를 사용하기 위해 먼저 사용자 좌표계 정의를 위한 3개의 기준 스텝을 티칭한 후 티칭된 프로그램 번호와 사용자 좌표계 번호를 지정하여 사용자 좌표계를 등록합니다.

다음 절차에 따라 3개의 기준 스텝을 티칭하십시오.



![&#xADF8;&#xB9BC; 57 &#xC0AC;&#xC6A9;&#xC790; &#xC88C;&#xD45C;&#xACC4; &#xC815;&#xC758;&#xB97C; &#xC704;&#xD55C; 3&#xAC1C;&#xC758; &#xAE30;&#xC900; &#xC2A4;&#xD15D; &#xD2F0;&#xCE6D; &#xBC29;&#xBC95;](../../../.gitbook/assets/image%20%28194%29.png)

1.	사용자 좌표계의 원점 정의: 임의의 한 점을 티칭하십시오.

2.	사용자 좌표계의 X축 정의: 가능한 한 원점과의 거리가 200 ㎜ 이상 떨어진 지점의 X축 선상에 임의의 한 점을 티칭하십시오.

3.	사용자 좌표계의 XY 평면 정의\(Y축과 Z축 방향 결정\): 가능한 한 원점과의 거리가 200 ㎜ 이상 떨어진 지점의 X축과 Y축으로 이루어지는 평면상에 임의의 한 점을 티칭하십시오.

{% hint style="info" %}
* 사용자 좌표계 설정용 프로그램을 티칭할 때 TCP \(Tool Center Point\)는 정확한 값으로 설정되어 있어야 합니다. 현재 선택된 툴의 툴 데이터가 정확한 값으로 입력되었는지 확인하십시오.
* 사용자 좌표계는 총 10개까지 등록할 수 있습니다.
{% endhint %}

{% hint style="warning" %}
좌표계 정의를 위한 기준점 기록 시 주의 사항은 다음과 같습니다.

* 기준 3점이 동일 직선상에 존재하지 않아야 합니다.
* 기준 3점 간의 거리가 지나치게 가깝지 않아야 합니다.
* 사용자 좌표계의 XY 평면을 정의한 이후의 이후의 스텝은 좌표계 등록에 아무런 영향을 미치지 않습니다.
{% endhint %}

티칭된 프로그램 번호와 사용자 좌표계 번호를 지정하여 사용자 좌표계를 등록하는 방법은 다음과 같습니다.

1.	\[2: 제어 파라미터 &gt; 6: 좌표계 등록 &gt; 1: 사용자 좌표계\] 메뉴를 터치하십시오.

2.	사용자 좌표계 이름과 프로그램 번호, 축별 원점과의 거리 및 각도를 설정하십시오.

![](../../../.gitbook/assets/image%20%28140%29.png)



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
        <img src="../../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">&#xC0AC;&#xC6A9;&#xC790; &#xC88C;&#xD45C;&#xACC4; &#xBAA9;&#xB85D;&#xC5D0;&#xC11C;
        &#xC120;&#xD0DD;&#xD55C; &#xC88C;&#xD45C;&#xACC4;&#xC758; &#xC0C1;&#xC138;
        &#xC815;&#xBCF4;&#xC785;&#xB2C8;&#xB2E4;. &#xC88C;&#xD45C;&#xACC4; &#xC774;&#xB984;&#xACFC;
        &#xC124;&#xBA85;, &#xD2F0;&#xCE6D;&#xB41C; &#xD504;&#xB85C;&#xADF8;&#xB7A8;
        &#xBC88;&#xD638;, &#xCD95;&#xBCC4; &#xC6D0;&#xC810;&#xACFC;&#xC758; &#xAC70;&#xB9AC;
        &#xBC0F; &#xAC01;&#xB3C4;&#xB97C; &#xC124;&#xC815;&#xD560; &#xC218; &#xC788;&#xC2B5;&#xB2C8;&#xB2E4;.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: &#xBCC0;&#xACBD; &#xB0B4;&#xC6A9;&#xC744; &#xC800;&#xC7A5;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>[+]/[-]: &#xC0C8;&#xB85C;&#xC6B4; &#xC0AC;&#xC6A9;&#xC790; &#xC88C;&#xD45C;&#xACC4;&#xB97C;
            &#xCD94;&#xAC00;&#xD558;&#xAC70;&#xB098; &#xC0AC;&#xC6A9;&#xC790; &#xC88C;&#xD45C;&#xACC4;&#xB97C;
            &#xC0AD;&#xC81C;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>&#xC0AC;&#xC6A9;&#xC790; &#xC88C;&#xD45C;&#xACC4; &#xBAA9;&#xB85D;&#xC785;&#xB2C8;&#xB2E4;.
            &#xC88C;&#xD45C;&#xACC4; &#xC774;&#xB984;&#xC744; &#xC120;&#xD0DD;&#xD558;&#xBA74;
            &#xC0C1;&#xC138; &#xC815;&#xBCF4;&#xB97C; &#xD655;&#xC778; &#xBC0F; &#xD3B8;&#xC9D1;&#xD560;
            &#xC218; &#xC788;&#xC2B5;&#xB2C8;&#xB2E4;.</li>
          <li>[&#xD398;&#xC774;&#xC9C0; &#xBCF5;&#xC0AC;]/[&#xD398;&#xC774;&#xC9C0;
            &#xBD99;&#xC5EC;&#xB123;&#xAE30;]: &#xC0AC;&#xC6A9;&#xC790; &#xC88C;&#xD45C;&#xACC4;
            &#xC815;&#xBCF4;&#xB97C; &#xBCF5;&#xC0AC;&#xD558;&#xC5EC; &#xB2E4;&#xB978;
            &#xC88C;&#xD45C;&#xACC4;&#xC5D0; &#xBD99;&#xC5EC; &#xB123;&#xC2B5;&#xB2C8;&#xB2E4;.
            <br
            />&#xBAA9;&#xB85D;&#xC5D0;&#xC11C; &#xBCF5;&#xC0AC;&#xD560; &#xC88C;&#xD45C;&#xACC4;
            &#xC815;&#xBCF4;&#xC758; &#xC774;&#xB984;&#xC744; &#xC120;&#xD0DD;&#xD558;&#xACE0;
            [&#xD398;&#xC774;&#xC9C0; &#xBCF5;&#xC0AC;] &#xBC84;&#xD2BC;&#xC744; &#xD130;&#xCE58;&#xD55C;
            &#xD6C4; &#xAC12;&#xC744; &#xC801;&#xC6A9;&#xD560; &#xC88C;&#xD45C;&#xACC4;&#xC758;
            &#xC774;&#xB984;&#xC744; &#xC120;&#xD0DD;&#xD558;&#xACE0; [&#xD398;&#xC774;&#xC9C0;
            &#xBD99;&#xC5EC;&#xB123;&#xAE30;] &#xBC84;&#xD2BC;&#xC744; &#xD130;&#xCE58;&#xD558;&#xC2ED;&#xC2DC;&#xC624;.</li>
          <li>[JOB &#xACC4;&#xC0B0;]: &#xC0AC;&#xC6A9;&#xC790; &#xC88C;&#xD45C;&#xACC4;&#xB97C;
            &#xC815;&#xC758;&#xD558;&#xAE30; &#xC704;&#xD574; &#xD2F0;&#xCE6D;&#xD55C;
            &#xD504;&#xB85C;&#xADF8;&#xB7A8;&#xC744; &#xAE30;&#xBC18;&#xC73C;&#xB85C;
            &#xC0AC;&#xC6A9;&#xC790; &#xC88C;&#xD45C;&#xACC4;&#xB97C; &#xACC4;&#xC0B0;&#xD569;&#xB2C8;&#xB2E4;.
            <br
            />[&#xB4F1;&#xB85D;&#xC744; &#xC704;&#xD55C; &#xD504;&#xB85C;&#xADF8;&#xB7A8;
            &#xBC88;&#xD638;] &#xC635;&#xC158;&#xC5D0; &#xD2F0;&#xCE6D;&#xD55C; &#xD504;&#xB85C;&#xADF8;&#xB7A8;&#xC758;
            &#xBC88;&#xD638;&#xB97C; &#xC785;&#xB825;&#xD55C; &#xD6C4; [JOB &#xACC4;&#xC0B0;]
            &#xBC84;&#xD2BC;&#xC744; &#xD130;&#xCE58;&#xD558;&#xBA74; &#xC0AC;&#xC6A9;&#xC790;
            &#xC88C;&#xD45C;&#xACC4;&#xC758; &#xC6D0;&#xC810;&#xACFC; &#xAC01;&#xB3C4;&#xAC00;
            &#xACC4;&#xC0B0;&#xB429;&#xB2C8;&#xB2E4;.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

