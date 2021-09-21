# 1.2.3 Hi6 티치 펜던트 화면

로봇의 동작을 제어하거나 로봇과 연동된 장치를 관리할 수 있습니다. Hi6 티치 펜던트 화면은 다음과 같이 구성됩니다.

![](../../.gitbook/assets/image%20%2834%29.png)

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
        <img src="../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">상태 표시줄입니다. 티치
        펜던트의 통신 상태와
        운전 모드, 로봇 시스템의
        상태와 메커니즘을 표시합니다.
        자세한 내용은 “1.2.3.1 상태
        표시줄”을 참조하십시오.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">기능 버튼을 이용해 설정값을
        확인하고 변경합니다.
        자세한 내용은 “1.2.3.3 기능
        버튼”을 참조하십시오.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c3.png" alt/>
      </td>
      <td style="text-align:left">작업 영역입니다. JOB 프로그램을
        편집하고 모니터링 정보를
        확인하는 등 다양한 작업을
        수행합니다. 여러 작업을
        동시에 수행할 수 있습니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c4.png" alt/>
      </td>
      <td style="text-align:left">메뉴 버튼을 이용해 메뉴의
        설정값을 확인 및 변경하고,
        다양한 기능을 실행합니다.
        자세한 내용은 “1.2.3.4 메뉴
        버튼”을 참조하십시오.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c5.png" alt/>
      </td>
      <td style="text-align:left">조그 막대입니다. [좌표계]
        버튼으로 선택한 조그
        수행의 기준 좌표계에
        따라 변경된 축의 이름이
        표시됩니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c6.png" alt/>
      </td>
      <td style="text-align:left">
        <p>이력 표시줄입니다. 자세한
          내용은 “1.2.3.2 이력 표시줄”을
          참조하십시오.</p>
        <ul>
          <li>현재 시간 정보와 티치
            펜던트의 메모리 사용
            현황이 표시됩니다. 또한
            에러 메시지 또는 경고
            메시지를 확인할 수 있습니다.</li>
          <li>화면에 소프트 키보드를
            표시하거나 숨깁니다.
            소프트 키보드 사용 중에는
            키보드의 위치를 화면의
            상단으로 이동할 수 있습니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### 

### 상태 표시줄

![그림 9 상태 표시줄](../../.gitbook/assets/image%20%281%29.png)

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
        <img src="../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">로봇 제어기 플랫폼의
        이름입니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">티치 펜던트와 로봇 제어기
        본체의 COM 모듈 간 이더넷
        통신의 상태를 표시합니다.
        (
        <img src="../../.gitbook/assets/flag-comm-ok.png" alt/>: 정상 /
        <img src="../../.gitbook/assets/flag-comm-ng.png"
        alt/>: 응답 없음)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <p>로봇의 운전 방식을 표시합니다.</p>
        <ul>
          <li><b>수동</b>: 조그로 로봇을
            제어하고, JOB 프로그램을
            작성하는 로봇 교시 모드입니다.</li>
          <li><b>자동</b>: JOB 프로그램을
            재생하여 로봇을 자동으로
            운전하는 모드입니다.</li>
          <li><b>원격수동</b>: 모드를 원격에서
            I/O신호로 결정하는 상태입니다.
            (현재 상태: 수동 모드)</li>
          <li><b>원격자동</b>: 모드를 원격에서
            I/O신호로 결정하는 상태입니다.
            (현재 상태: 자동 모드)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c4.png" alt/>
      </td>
      <td style="text-align:left">로봇 시스템의 다양한
        상태를 표시합니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c5.png" alt/>
      </td>
      <td style="text-align:left">로봇의 동작 상태를 표시합니다.
        (
        <img src="../../.gitbook/assets/flag-mot-on.png" alt/>: 모터 ON /
        <img src="../../.gitbook/assets/flag-start.png"
        alt/>: 로봇 재생 중 /
        <img src="../../.gitbook/assets/flag-stop.png"
        alt/>: 로봇 정지)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c6.png" alt/>
      </td>
      <td style="text-align:left">선택된 로봇 메커니즘의
        모델명을 표시합니다.</td>
    </tr>
  </tbody>
</table>

### 

### 이력 표시줄

![그림 10 이력 표시줄](../../.gitbook/assets/image%20%2822%29.png)

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
        <img src="../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">날짜와 시간 정보가 표시됩니다.
        [메뉴] 버튼 &gt; [08: 날짜, 시간
        설정] 메뉴를 터치하면
        날짜와 시간 정보를 변경할
        수 있습니다. 날짜와 시간
        정보 변경에 대한 자세한
        내용은 “4.5 날짜 및 시간
        설정”을 참조하십시오.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>티치 펜던트의 메모리(RAM)
            사용 현황이 표시됩니다.
            메모리의 전체 용량 대비
            사용 및 잔여 용량이 막대그래프에
            나타나고 잔여 용량(MByte)은
            수치로도 확인할 수 있습니다.</li>
          <li>에러 또는 경고 상황이
            발생하면 메모리 사용
            현황 대신 알림 메시지가
            나타나 약 1분 동안 깜빡인
            후 멈춥니다.</li>
          <li>알림 메시지 우측에서
            에러 및 경고 발생 시점을
            확인할 수 있습니다. 또한
            알림 메시지를 터치하면
            새 창에서 에러 및 경고
            발생 이력을 확인할 수
            있습니다.</li>
          <li>알림 메시지에 대한 자세한
            내용은 “2.5 에러 정보”를
            참조하십시오.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <p>화면에 소프트 키보드를
          표시합니다. 소프트 키보드의
          사용 방법에 대한 자세한
          내용은 “3.2.4.4 소프트 키보드”를
          참조하십시오.</p>
        <ul>
          <li>소프트 키보드 사용 중에
            [
            <img src="../../.gitbook/assets/bt-dock-softkb.png" alt/>] 버튼을 터치하면 키보드의
            위치를 화면 상단으로
            이동할 수 있습니다.</li>
          <li>소프트 키보드를 숨기려면,
            [
            <img src="../../.gitbook/assets/bt-softkb.png" alt/>] 버튼을 터치하십시오.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### 

### 기능 버튼

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">번호</th>
      <th style="text-align:left">설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>[기록조건] 버튼: move 문 기록
          조건의 기본값을 설정합니다.</p>
        <p>[기록조건] 버튼을 터치한
          후 설정창에서 보간, 이동
          속도와 단위, Accuracy, 툴 번호를
          입력하고 [확인] 버튼(
          <img
          src="../../.gitbook/assets/icon-ok.png" alt/>)을 터치하십시오.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/lbt-bar.png" alt/>
      </td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>[실행단위] 버튼: 수동
          또는 자동 모드에서의
          프로그램 실행 단위를
          설정합니다.</p>
        <p></p>
        <p>수동 모드: 원하는 옵션이
          나타날 때까지 [실행단위]
          버튼을 반복해서 터치하십시오.</p>
        <ul>
          <li>
            <img src="../../.gitbook/assets/bt-runto-cmd.png" alt/>[cmd]: 명령어 한 행씩 실행합니다.</li>
          <li>
            <img src="../../.gitbook/assets/bt-runto-step.png" alt/>[step]: 한 스텝씩 실행합니다.</li>
          <li>
            <img src="../../.gitbook/assets/bt-runto-end.png" alt/>[end]: end 명령문까지 실행합니다.</li>
        </ul>
        <p></p>
        <ul>
          <li>자동 모드: [실행단위]
            버튼을 터치한 후 설정창에서
            옵션을 설정하십시오.</li>
          <li>
            <img src="../../.gitbook/assets/bt-spd_manual (3) (3) (3).png" alt/>[1cycle]: end 명령문까지 실행
            후 정지합니다.</li>
          <li>
            <img src="../../.gitbook/assets/bt-runto-cont.png" alt/>[cont]: end 명령문까지 실행
            후 스텝 0부터 다시 실행합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <p>[속도조절] 버튼: 사용자의
          안전을 위해 스텝 속도를
          설정합니다.</p>
        <p>[속도조절] 버튼을 터치한
          후 설정창에서 스텝 전후진
          최고 속도와 자동 운전
          속도 비율을 설정하십시오.</p>
        <p></p>
        <ul>
          <li>
            <img src="../../.gitbook/assets/bt-spd_manual (3) (3) (2).png" alt/>수동 모드: 스텝 FWD/BWD 제한
            속도(㎜/sec)를 표시합니다.</li>
          <li>
            <img src="../../.gitbook/assets/bt-spd_manual (3) (3) (1).png" alt/>자동 모드: 재생 속도(%)를
            표시합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p>[조그 속도 레벨/조그 인칭]
          버튼: 축별 또는 직교 조그의
          속도 레벨과 조그키의
          사용 모드를 설정합니다.</p>
        <ul>
          <li>
            <p>[
              <img src="../../.gitbook/assets/bt-spd-up.png" alt/>/
              <img src="../../.gitbook/assets/bt-spd-dn.png" alt/>]: 원하는 축별 또는 직교
              조그의 속도 레벨(1: 저속
              ~ 8: 고속)이 나타날 때까지
              버튼을 반복하여 터치하십시오.
              버튼을 길게 터치하면
              최저 또는 최고 레벨을
              한 번에 설정할 수 있습니다.</p>
            <p></p>
          </li>
          <li>
            <img src="../../.gitbook/assets/bt-jog-1.png" alt/>
            <img src="../../.gitbook/assets/bt-jog-inch.png" alt/>[1]: 레벨 값을 터치하면
            레벨 값의 좌측 상단에
            inch 표시가 나타나고 인칭
            모드로 전환됩니다. 일반
            모드로 돌아가려면 레벨
            값을 터치하십시오. inch
            표시가 사라집니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c5.png" alt/>
      </td>
      <td style="text-align:left">
        <p>[툴] 버튼: 선택된 툴 번호를
          확인하고 설정합니다.</p>
        <p>[툴] 버튼을 터치한 후
          설정창에서 툴 번호를
          입력하고 [확인] 버튼을
          터치하십시오.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c6.png" alt/>
      </td>
      <td style="text-align:left">
        <p>
          <img src="../../.gitbook/assets/bt-gun-off.png" alt/>
          <img src="../../.gitbook/assets/bt-gun-on.png" alt/>[건] 버튼: 선택된 건 번호를
          확인하고 건의 ON/OFF 상태를
          설정합니다.</p>
        <p>건 번호를 확인하고 [건]
          버튼을 터치하십시오.
          건의 상태가 ON 또는 OFF로
          전환되고 버튼의 색이
          변경됩니다.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c7.png" alt/>
      </td>
      <td style="text-align:left">[도움말] 버튼: 선택된
        명령문이나 에러 메시지
        또는 경고 메시지에 대한
        상세 정보가 나타납니다.</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
조그 인칭 모드

일반 모드에서는 조그키를 누르고 있는 동안 로봇이 계속 움직이지만, 인칭 모드에서는 각 인칭 레벨의 설정 값만큼만 이동한 후 정지하므로 세밀하게 조작할 수 있습니다.
{% endhint %}

{% hint style="info" %}
건\(GUN\)

* 스폿용접을 사용할 때, 스텝 기록 시 GUN 가압 동작의 기록 여부를 결정합니다. &lt;shift&gt; 키와 함께 누르면 GUN 신호가 수동 출력됩니다.
* 아크용접을 사용할 때, 자동 운전 시에 램프가 켜져 있으면 실제로 아크 용접을 진행하고, 램프가 꺼져 있으면 아크용접을 진행하지 않고 티칭된 궤적만을 확인합니다.
{% endhint %}



### 메뉴 버튼



<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">번호</th>
      <th style="text-align:left">설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>메커니즘(mechanism): 선택된
          메커니즘을 확인하고
          설정합니다.</p>
        <p>원하는 메커니즘 그룹이
          나타날 때까지 <b>[메커니즘]</b> 버튼을
          반복해서 터치하십시오.
          초기 설정에서 로봇 모델이
          선택되지 않은 경우, 메커니즘
          그룹이 표시되지 않고
          미초기화 표시가 나타납니다.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/rbt-bar.png" alt/>
      </td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>좌표계(coordinate system): 조그 수행의
          기준 좌표계를 확인하고
          설정합니다.</p>
        <p>원하는 좌표계 방식이
          나타날 때까지 <b>[좌표계]</b> 버튼을
          반복해서 터치하십시오.
          선택한 기준 좌표계에
          따라 변경된 축의 이름이
          화면 우측 조그 막대에
          나타납니다.</p>
        <p></p>
        <ul>
          <li>
            <img src="../../.gitbook/assets/bt-crd-joint.png" alt/>축(Joint) 좌표계: 조그 막대에
            각 축의 이름이 표시됩니다.
            축 이름 우측의<b> [-/+]</b> 버튼을
            터치하면 해당하는 축을
            움직일 수 있습니다.</li>
          <li>
            <img src="../../.gitbook/assets/bt-crd-robot.png" alt/>로봇(Robot) 좌표계: 조그 막대에
            X, Y, Z, RX, RY, RZ와 부가축이 표시됩니다.
            로봇 좌표계를 기준으로
            로봇의 툴 끝(TCP, Tool Center Point)을
            이동 및 회전할 수 있습니다.</li>
          <li>
            <img src="../../.gitbook/assets/bt-crd-user.png" alt/>사용자(User) 좌표계: 조그
            막대에 X, Y, Z, RX, RY, RZ와 부가축이
            표시됩니다. 사용자 좌표계를
            기준으로 로봇의 툴 끝(TCP)을
            이동 및 회전할 수 있습니다.</li>
          <li>
            <img src="../../.gitbook/assets/bt-crd-tool.png" alt/>툴(Tool) 좌표계: 조그 막대에
            X, Y, Z, RX, RY, RZ와 부가축이 표시됩니다.
            툴 좌표계를 기준으로
            로봇의 툴 끝(TCP)을 이동
            및 회전할 수 있습니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <p>기록(RECord): JOB 프로그램에서
          move 문을 입력합니다.</p>
        <p><b>[기록]</b> 버튼을 터치하십시오.
          현재 커서 위치의 바로
          아래에 move 문이 입력됩니다.</p>
        <ul>
          <li>로봇의 현재 자세가 타겟
            포즈로 기록되고 move 문의
            보간, 이동 속도와 단위,
            정밀도, 툴 번호, 메커니즘
            세트는 <b>[기록조건]</b> 버튼으로
            설정한 값이 적용됩니다.</li>
          <li>타겟 포즈와 move 문 기록
            조건값은 추후에 편집할
            수 있습니다.</li>
        </ul>
        <p>
          <img src="../../.gitbook/assets/bt-pos-mod.png" alt/>(<b>&lt;shift&gt;</b> 키 조합 시) 위치
          수정: JOB 프로그램에서
          로봇의 현재 자세를 스텝의
          타겟 포즈로 적용합니다.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p>명령 입력: 원하는 명령어를
          입력합니다.</p>
        <p><b>[명령입력]</b> 버튼을 터치한
          후 명령 입력창에서 명령어를
          터치하십시오. 현재 커서
          위치의 바로 아래에 명령문이
          입력됩니다. 명령 입력에
          대한 자세한 내용은 “3.2.2
          명령문 입력”을 참조하십시오.</p>
        <p></p>
        <p>
          <img src="../../.gitbook/assets/bt-delete.png" alt/>(<b>&lt;shift&gt;</b> 키 조합 시) 위치
          수정: JOB 프로그램에서
          로봇의 현재 자세를 스텝의
          타겟 포즈로 적용합니다.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c5.png" alt/>
      </td>
      <td style="text-align:left">
        <p>속성: 명령문의 속성을
          확인합니다.</p>
        <p>명령문을 터치하여 선택한
          후<b> [속성]</b> 버튼을 터치하십시오.
          명령문의 속성창이 나타납니다.</p>
        <p></p>
        <p>
          <img src="../../.gitbook/assets/bt-block-edit.png" alt/>(<b>&lt;shift&gt;</b> 키 조합 시) 블록
          편집: JOB 프로그램에서
          복사하기, 잘라내기, 붙여넣기를
          수행할 수 있는 블록 편집
          모드로 진입합니다. 블록
          편집에 대한 자세한 내용은
          “3.2.4.5 블록 편집 모드”를
          참조하십시오.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c6.png" alt/>
      </td>
      <td style="text-align:left"><b>[메뉴]</b>: 프로그램의 서비스
        기능 메뉴를 사용합니다.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c7.png" alt/>
      </td>
      <td style="text-align:left"><b>[설정]</b>: 프로그램의 시스템
        메뉴를 이용해 사용 환경을
        설정합니다.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c8.png" alt/>
      </td>
      <td style="text-align:left">
        <p>즐겨찾기: 코드 번호를
          이용해 미리 지정한 기능을
          빠르게 실행합니다.</p>
        <p><b>[즐겨찾기] </b>버튼을 터치한
          후 코드 번호를 입력하고<b> [확인]</b> 버튼을
          터치하십시오. 지정된
          기능이 실행됩니다.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c9.png" alt/>
      </td>
      <td style="text-align:left">
        <p>사용자키: 사용자키 영역에
          버튼으로 할당한 기능을
          로봇 티칭 시 사용합니다.</p>
        <p><b>[사용자키]</b> 버튼을 터치하십시오.
          메뉴 버튼 영역이 사용자키
          영역으로 전환되어 미리
          버튼으로 할당한 기능을
          사용할 수 있습니다. 메뉴
          버튼 영역으로 돌아가려면, <b>[사용자키]</b> 버튼을
          터치하거나 <b>&lt;esc&gt;</b> 키를
          누르십시오.</p>
      </td>
    </tr>
  </tbody>
</table>

### 

### 작업 영역

JOB 프로그램을 편집하고 모니터링 정보를 확인하는 등 다양한 작업을 수행하는 작업 영역입니다.

![그림 11 작업 영역 구성](../../.gitbook/assets/image%20%2824%29.png)

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
        <img src="../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>작업 영역은 상하, 두 개의
          패널 스택으로 기본 구성됩니다.</p>
        <ul>
          <li>각 패널 스택에 패널창을
            추가하여 여러 작업을
            동시에 수행할 수 있습니다.</li>
          <li>기존 패널 스택의 상단과
            하단에 또는 패널 스택
            사이에 새 패널 스택을
            추가할 수 있습니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>패널 스택입니다. 현재
          열려 있는 모든 패널의
          이름이 표시되며 선택된
          패널창이 하단에 나타납니다.</p>
        <ul>
          <li>패널명을 터치하여 선택한
            후 원하는 위치로 끌어
            놓으면 패널창의 순서를
            바꿀 수 있습니다.</li>
          <li>패널명을 터치하여 선택한
            후 다른 패널 스택으로
            끌어 놓으면 패널창의
            위치를 다른 패널 스택으로
            이동할 수 있습니다.</li>
          <li>패널명을 터치하여 선택한
            후 기존의 패널 스택 외
            다른 위치로 끌어 놓으면
            새 패널 스택이 추가되고
            패널창이 새 패널 스택에서
            열립니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[+]: 패널 선택창에서 원하는
            모니터링 항목을 선택하여
            새 패널창으로 엽니다.
            패널창은 패널 스택에
            탭으로 추가됩니다.</li>
          <li>[X]: 선택한 패널창을 닫습니다.
            패널 스택에 패널창이
            하나만 있을 경우에는
            해당 패널창을 닫을 수
            없습니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

