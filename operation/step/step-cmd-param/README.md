# 2.3.1 스텝 명령문 인수

스텝 명령문 인수\(Parameter\)는 로봇 스텝의 이동에 필요한 이동 명령 move 이외의 이동 조건으로 로봇의 위치, 보간, 속도, Accuracy, 툴 번호 등이 있습니다.

스텝 명령문 인수에는 기본 인수와 선택 인수가 있습니다. 기본 인수는 스텝에 필수적인 인수이고 선택 인수는 필요에 따라 추가할 수 있는 인수입니다.

스텝 명령문은 다음과 같이 구성됩니다.

![](../../../_assets/image_77.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">번호</th>
      <th style="text-align:left">인수</th>
      <th style="text-align:left">설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">보간</td>
      <td style="text-align:left">
        <p>스텝과 스텝 사이의 보간된
          경로</p>
        <p>P (축보간), L (직선보간), C
          (원호보간), SP (정치툴보간
          Off), SL (정치툴 직선보간), SC
          (정치툴 원호보간)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">포즈</td>
      <td style="text-align:left">
        <p>위치를 기록하는 인수.
          이 인수가 생략되고 명령문
          뒤에 포즈가 지정될 수도
          있습니다(숨은 포즈).</p>
        <p>Target 포즈(X, Y, Z, Rx, Ry, Rz, Cfg){좌표계}
          + 시프트(X, Y, Z, Rx, Ry, Rz){좌표계}</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">속도</td>
      <td style="text-align:left">로봇의 운전 속도(단위:
        mm/sec, cm/min, %, sec)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">Accuracy</td>
      <td style="text-align:left">로봇이 목표 스텝으로
        이동할 때 발생하는 현재
        위치와 기록 위치의 허용
        오차값(0 ~ 7)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">툴 번호</td>
      <td style="text-align:left">사용하는 툴의 번호(0 ~
        31)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">정지 조건</td>
      <td style="text-align:left">로봇이 다음 명령(스텝
        또는 펑션)을 수행하기
        위해 이동을 정지하기
        위한 조건</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left">주석</td>
      <td style="text-align:left">스텝에 대한 설명</td>
    </tr>
  </tbody>
</table>

