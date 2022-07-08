# 1.2.1.1 모터 전원 투입 및 조작 가능 상태

티치 펜던트의 모드 스위치와 안전 플러그의 상태에 따라 모터 전원 투입 및 조작 가능 상태가 결정됩니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">안전 플러그</th>
      <th style="text-align:left">모드 스위치: 수동</th>
      <th style="text-align:left">모드 스위치: 자동</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">해제</td>
      <td style="text-align:left">
        <ul>
          <li>Motor ON 가능</li>
          <li>스텝 전후진 가능</li>
        </ul>
      </td>
      <td style="text-align:left">Emergency (Motor Off)</td>
    </tr>
    <tr>
      <td style="text-align:left">투입</td>
      <td style="text-align:left">
        <ul>
          <li>Motor ON 가능</li>
          <li>스텝 전후진 가능</li>
        </ul>
      </td>
      <td style="text-align:left">
        <ul>
          <li>Motor ON 가능</li>
          <li>정상 속도 운전</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
일반 산업용 로봇에는 안전 플러그를 사용합니다. 그러나 LCD 로봇에는 안전 플러그 대신 라이트 커튼을 사용합니다.
{% endhint %}

