# 2.3.1.2 포즈

포즈는 위치를 기록하는 인수입니다. \[명령입력\] 버튼을 이용하여 이동 명령 move를 입력한 경우는 tg\(target\) 인수에 포즈식을 지정해야 합니다. \[기록\] 버튼을 이용해 move문을 입력한 경우에는 tg 인수가 나타나지 않습니다. \[기록\] 버튼을 터치하는 순간의 로봇 본체의 위치와 자세가 기록되는데 JOB 편집 화면에는 표시되지 않으므로 이것을 숨은 포즈라고 합니다.

Hi6 티치 펜던트 화면 우측의 메뉴 버튼을 이용하여 포즈를 입력하는 방법은 다음과 같습니다.

* \[명령입력\] 버튼을 터치한 후 \[MOTION\]을 선택하고 명령문 입력하십시오.



![](../../../.gitbook/assets/image%20%2848%29.png)

* \[속성\] 버튼을 터치한 후 현재의 로봇 포즈 속성을 설정하고 \[OK\] 버튼 터치하십시오.

![](../../../.gitbook/assets/image%20%2842%29.png)

포즈 변수와 쉬프트 변수는 다음의 형식으로 저장됩니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#xD3EC;&#xC988; &#xBCC0;&#xC218;</th>
      <th style="text-align:left">&#xC26C;&#xD504;&#xD2B8; &#xBCC0;&#xC218;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">(X, Y, Z, Rx, Ry, Rz, {&#xC88C;&#xD45C;&#xACC4;}, {config.})</td>
      <td style="text-align:left">(X, Y, Z, Rx, Ry, Rz, {&#xC88C;&#xD45C;&#xACC4;})</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>{&#xC88C;&#xD45C;&#xACC4;}:
          <br />&quot;base&quot; = &#xBCA0;&#xC774;&#xC2A4; &#xC88C;&#xD45C;&#xACC4;
          <br
          />
        </p>
        <p>&quot;robot&quot; = &#xB85C;&#xBD07; &#xC88C;&#xD45C;&#xACC4;
          <br />
        </p>
        <p>&quot;user{n}&quot; = &#xC0AC;&#xC6A9;&#xC790; &#xC88C;&#xD45C;&#xACC4;(n&#xC740;
          &#xBC88;&#xD638;)
          <br />
        </p>
        <p>&quot;joint&quot; = &#xCD95; &#xC88C;&#xD45C;&#xACC4;
          <br />
        </p>
        <p>&quot;encoder&quot;= &#xC5D4;&#xCF54;&#xB354;</p>
      </td>
      <td style="text-align:left">
        <p>{&#xC88C;&#xD45C;&#xACC4;}:</p>
        <p>&quot;base&quot; = &#xBCA0;&#xC774;&#xC2A4; &#xC88C;&#xD45C;&#xACC4;
          <br
          />
        </p>
        <p>&quot;robot&quot; = &#xB85C;&#xBD07; &#xC88C;&#xD45C;&#xACC4;
          <br />
        </p>
        <p>&quot;user{n}&quot; = &#xC0AC;&#xC6A9;&#xC790; &#xC88C;&#xD45C;&#xACC4;(n&#xC740;
          &#xBC88;&#xD638;)
          <br />
        </p>
        <p>&quot;joint&quot; = &#xCD95; &#xC88C;&#xD45C;&#xACC4;</p>
        <p></p>
      </td>
    </tr>
  </tbody>
</table>



