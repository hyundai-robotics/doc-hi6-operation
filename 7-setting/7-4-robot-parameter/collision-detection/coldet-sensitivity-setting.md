# 7.4.8.1 충돌검지 민감도 설정

충돌검지 민감도는 JOB 프로그램에서 명령어로 조정할 수 있습니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">항목</th>
      <th style="text-align:left">내용</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">명령어</td>
      <td style="text-align:left">ColDet Sensitivity</td>
    </tr>
    <tr>
      <td style="text-align:left">설명</td>
      <td style="text-align:left">충돌검지 민감도 변경</td>
    </tr>
    <tr>
      <td style="text-align:left">입력 방법</td>
      <td style="text-align:left">command → MOTION → colsense</td>
    </tr>
    <tr>
      <td style="text-align:left">문법</td>
      <td style="text-align:left">ColDet Sensitivity=100</td>
    </tr>
    <tr>
      <td style="text-align:left">파라미터</td>
      <td style="text-align:left">0 ~ 200 (0: 기능 무효, 민감도
        값이 클수록 충격에 민감하게
        동작)</td>
    </tr>
    <tr>
      <td style="text-align:left">예</td>
      <td style="text-align:left">
        <p>[충돌검지] 메뉴에서 민감도를
          100%로 설정한 경우</p>
        <p>S1 ~ S2: 민감도 100%로 검지 / S3 ~
          S4: 민감도 50%로 검지</p>
        <p>
          <img src="../../../.gitbook/assets/coldet-sensitivity.png" alt/>
        </p>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
민감도를 너무 높게 설정하면 오검지가 발생할 수 있습니다. 또한 민감도를 너무 낮게 설정하면 충돌을 검지하지 못할 수 있습니다.
{% endhint %}

{% hint style="info" %}
* 명령어가 없을 경우 \[충돌검지\] 메뉴에서 설정한 기본 민감도로 충돌을 검지합니다.
* 명령어로 설정한 민감도는 다음의 경우에서 기본 민감도로 초기화됩니다.
  * 메인 프로그램의 END 명령어를 만남
  * 스텝/펑션 변경
  * 스텝 카운터 리셋
{% endhint %}

