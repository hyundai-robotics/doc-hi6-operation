# 6.7 범용 출력

패널 선택창에서 \[범용 출력\]을 터치하십시오. 범용 출력 신호창이 나타납니다.

제어기 내 I/O 보드의 CNOUT커넥터를 통해 입력하는 신호인 범용 출력 신호의 상태를 확인할 수 있습니다.

![그림 41 범용 출력 신호 - ON/OFF 상태\(좌\) / 값 상태\(우\)](../_assets/tp630/pane-univoutsig-mode.png)

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
        <img src="../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>범용 출력 신호의 상태를
          표시합니다.</p>
        <ul>
          <li>시스템의 기본 사양으로
            지정되거나 사용자에
            의해 할당된 범용 출력
            신호는 굵은 글씨로 표시됩니다.</li>
          <li>현재 출력 중인 신호는
            초록색으로 표시됩니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[속성적용]: 정/부논리
            속성을 입력 상태값에 적용할지 여부를
            설정할 수 있습니다. </li>
          <li>[모드]: 해당 주소의 상태를 비트, 바이트, 워드 단위로 표시합니다.</li>
          <li>[수동 출력]: 선택한 신호를
            강제로 출력할 수 있습니다.</li>
          <li>[do/y]: 제어기의 논리적인 입력 상태와 PLC에 의한 매핑 상태를 구분하여 표시합니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 내장 PLC로 필드버스 신호 등을 매핑하여 사용하는 경우에는 출력 신호의 On/Off 상태가 다르게 나타날 수 있습니다.
* 출력 신호의 흐름은 다음과 같습니다.
{% endhint %}

![](../_assets/user-input-flow.png)

## 수동 출력

원하는 신호를 선택하여 강제로 출력할 수 있습니다.

1. 범용 출력 신호창 우측의 \[ON/OFF\] 라디오 버튼을 터치하여 표시 방식을 ON/OFF 상태로 설정하십시오.
2. 신호창에서 신호를 터치하여 선택한 후 \[수동 출력\] 버튼을 터치하십시오.

![](../_assets/tp630/pane-univoutsig.png)

3. 수동 출력 확인창에서 출력 조건을 확인한 후 \[**확인**\] 버튼을 터치하십시오.

![](../_assets/tp630/pane-univoutsig-manual.png)

| FbN | doN | =1/0 |
| :---: | :---: | :---: |
| N: 모니터링할 FB 블록의 번호 | N: 출력할 신호의 번호 | 출력 상태\(1: 출력, 0: 미출력\) |

4. 선택한 신호의 출력 상태를 확인하십시오. 선택한 신호가 출력 상태로 전환되어 신호창에 노란색으로 표시됩니다.

![](../_assets/tp630/pane-univoutsig-onoff.png)

