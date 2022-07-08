# 9.1 속성 기능 사용

Hi6 티치 펜던트 화면 우측의 \[속성\] 버튼을 이용하면 이러한 조건 설정과 위치 확인을 한 번의 버튼 조작으로 쉽고 빠르게 수행할 수 있습니다.

![그림 76 \[속성\] 버튼의 기능](../_assets/image_268.png)

예를 들어, Arc On 기능을 하는arcon 명령문에 커서가 있을 때 \[속성\] 버튼을 터치하면 용접 시작 조건 중 현재 명령문에서 사용하는 조건 번호의 내용이 표시됩니다. 화면에서 용접 시작 조건의 세부 내용을 확인하거나 변경할 수 있습니다. 또한 해당 조건 파일과 연관된 다른 조건 파일이 있을 경우 그곳으로 바로 이동할 수 있습니다. 즉, \[속성\] 버튼은 특정 명령문과 관련된 조건 파일이나 스텝 위치 등 세부 연관 내용을 쉽고 빠르게 확인하고 변경할 수 있게 해 줍니다.

\[속성\] 버튼을 이용하여 특정 명령문과 관련된 조건 파일 및 상세 내용을 확인하고 변경하는 방법은 다음과 같습니다.

1. 특정 명령문을 선택하여 커서를 두고 \[속성\] 버튼을 터치하십시오.
2. 다음 표의 내용을 참고하여 선택한 명령문과 관련된 파일이나 상세 내용을 확인 및 변경하십시오.

<table>
  <thead>
    <tr>
      <th style="text-align:left">명령문</th>
      <th style="text-align:left">파일 및 내용</th>
      <th style="text-align:left">설명</th>
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
        <p>스텝 위치
          <br />
        </p>
        <p>참조 위치</p>
      </td>
      <td style="text-align:left">
        <p>현재 스텝 위치 또는 전역
          포즈 변수</p>
        <p>X Y Z (㎜) Rx Ry Rz (deg) T1 ~ T10</p>
        <p>유닛, 좌표계, 로봇 Configuration</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">arcon asf=</td>
      <td style="text-align:left">
        <p>용접 시작 조건</p>
        <p>용접 보조 조건</p>
        <p>아크 용접기 조건</p>
      </td>
      <td style="text-align:left">
        <ul>
          <li>용접 시작 조건: 조건 번호,
            설명, 전압 확인, 재시도,
            동작 모드, 출력 전류, 출력
            전압, WCR 대기 시간, 로봇
            지연 시간 등</li>
          <li>용접 보조 조건
            <ul>
              <li>RETRY: 횟수, RETRACT시간/속도, 후퇴/용접선
                이동량, 쉬프트 이동량,
                속도, 전류, 전압</li>
              <li>RESTART: 횟수, 중첩량, 이동
                속도, 용접 전류, 전압,
                전류</li>
              <li>(용접 중)오버랩 조건 설정:
                아크, 가스, 와이어, 냉각수</li>
            </ul>
          </li>
          <li>아크 용접기 조건: 용접기
            번호, 명칭, 설명, 전원
            제어 모드, 와이어 직경,
            돌출 길이, 용착 검출 시간,
            ARC OFF 검출 시간 등
            <ul>
              <li>전류 특성: 극성, 지령치(V),
                측정치(A), 보정치</li>
              <li>전압 특성: 극성, 지령치(V),
                측정치(V), 보정치</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">arcon aef=</td>
      <td style="text-align:left">
        <p>용접 종료 조건</p>
        <p>용접 보조 조건</p>
      </td>
      <td style="text-align:left">
        <ul>
          <li>용접 종료 조건: 조건 번호,
            설명, 전압 확인, 출력 전류,
            출력 전압, 다운 슬로프,
            조건 유지 시간, 가스 후출</li>
          <li>용접 보조 조건: 자동 용착
            해제 횟수, 전류, 전압,
            지연시간</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">weavon wev=</td>
      <td style="text-align:left">위빙 조건</td>
      <td style="text-align:left">
        <ul>
          <li>위빙 조건: 건 번호, 위빙
            형태, 주파수, 기본 패턴,
            진행 각도, 경계 제한, 이동
            시간, 타이머</li>
          <li>아크 센싱 조건: 아크 센싱,
            좌우 센싱 시작 사이클,
            상하 센싱 시작 사이클,
            전압 계수, 샘플당 보정
            거리 등</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

1. \[기록\] 버튼을 터치하거나 &lt;esc&gt; 키를 눌러 작업을 종료하십시오.
2. \[기록\]: 변경 내용을 저장하고 작업을 종료합니다.
3. &lt;esc&gt;: 변경 내용을 취소하고 작업을 종료합니다

