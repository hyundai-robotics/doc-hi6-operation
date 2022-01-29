# 6.6 범용 입력

패널 선택창에서 \[범용 입력\]을 터치하십시오. 범용 입력 신호창이 나타납니다.

제어기 내 I/O 보드의 CNIN 커넥터를 통해 입력되는 신호인 범용 입력 신호의 상태를 확인할 수 있습니다.

![그림 40 범용 입력 신호 - ON/OFF 상태\(좌\) / 값 상태\(우\)](../.gitbook/assets/image%20%28166%29.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">번호</th>
      <th style="text-align:left">설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>범용 입력 신호의 상태를
          표시합니다.</p>
        <ul>
          <li>시스템의 기본 사양으로
            지정되거나 사용자에
            의해 할당된 범용 입력
            신호는 굵은 글씨로 표시됩니다.</li>
          <li>현재 입력 중인 신호는
            노란색으로 표시됩니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[FB0]: 드롭다운 메뉴를 터치하여
            모니터링할 FB 블록을 선택할
            수 있습니다(FB0 ~ FB15). 최대
            16 개의 I/O 블록을 구성할
            수 있으며 블록은 960 점의
            신호를 모니터링합니다.</li>
          <li>[속성적용]: 체크박스에
            체크 표시하여 정/부논리
            속성을 거치기 전의 입력
            물리값을 표시하도록
            설정할 수 있습니다. 정/부논리
            속성을 거친 후의 입력
            논리값이 표시되도록
            기본 설정(체크 해제)되어
            있습니다.</li>
          <li>[ON/OFF]/[값]: 라디오 버튼을
            터치하여 신호의 표시
            방식을 변경할 수 있습니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 내장 PLC로 필드버스 신호 등을 매핑하여 사용하는 경우에는 입력 신호의 On/Off 상태가 다르게 나타날 수 있습니다.
* 입력 신호의 흐름은 다음과 같습니다. 
{% endhint %}

![](../.gitbook/assets/user-input-flow%20%281%29.png)

