# 7.4.1.1 툴 데이터 설정

수동으로 로봇의 R1축 플랜지를 기준으로 TCP \(Tool Center Point\)의 거리와 각도를 설정하고, 툴의 중량, 무게 중심과 이너셔를 등록하는 방법은 다음과 같습니다.

1.	\[3: 로봇 파라미터 &gt; 1: 툴 데이터\] 메뉴를 터치하십시오.

2.	툴 데이터의 이름과 중량, 축별 상세 조건, 허용 비율을 설정하십시오.

![](../../../.gitbook/assets/image%20%28223%29.png)



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
        <img src="../../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">툴 데이터 목록에서 선택한
        툴 데이터의 상세 정보입니다.
        툴 데이터 이름과 설명,
        중량, 축별 상세 조건, 허용
        비율을 설정할 수 있습니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[자동보정]: 새로운 툴
            데이터를 생성하거나
            기존의 프로그램을 활용하여
            툴 데이터를 간단히 생성합니다.
            <br
            />기존에 티칭되어 있는
            스텝 위치에 새로 설정하려면
            툴을 위치시킨 후 자동
            보정 기능을 실행하면
            새로운 툴의 길이와 각도가
            생성됩니다.
            <br />
            <img src="../../../.gitbook/assets/tool-data-auto-calib.png" alt/>
            <br />
            <ul>
              <li>[기존 프로그램 번호]:
                툴 변형이 일어나기 전
                티칭되어 있는 프로그램
                번호를 입력합니다.</li>
              <li>[기존 스텝 번호]: 툴 데이터
                자동 보정을 시행할 스텝
                번호를 입력합니다.</li>
              <li>[설정할 툴 번호]: 새로
                설정할 툴의 번호를 입력합니다.
                <br
                />
              </li>
            </ul>
          </li>
          <li>[각도보정]: 툴의 각도를
            보정합니다.
            <br />
            <img src="../../../.gitbook/assets/tool-angle-auto-calib.png" alt/>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: 변경 내용을 저장합니다.</li>
          <li>[+]/[-]: 새로운 툴 데이터를
            추가하거나 툴 데이터를
            삭제합니다.</li>
          <li>툴 데이터 목록입니다.
            툴 데이터 이름을 선택하면
            상세 정보를 확인 및 편집할
            수 있습니다.</li>
          <li>[페이지 복사]/[페이지
            붙여넣기]: 툴 데이터 정보를
            복사하여 다른 툴 데이터에
            붙여 넣습니다.
            <br />목록에서 복사할 툴 데이터
            정보의 이름을 선택하고
            [페이지 복사] 버튼을 터치한
            후 값을 적용할 툴 데이터의
            이름을 선택하고 [페이지
            붙여넣기] 버튼을 터치하십시오.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* 툴 데이터 목록에서, 부하 추정이 되지 않는 툴 데이터는 이름의 우측에 \(X\) 표시가 나타납니다.
* 반드시 부하 추정을 실행한 후에 툴을 사용하십시오. 부하 추정이 되지 않은 툴을 사용하면 로봇의 속도 및 내구성에 문제가 발생할 수 있습니다.
* 툴 데이터를 복사하면 부하 추정 데이터가 함께 복사됩니다. 툴 데이터 복사 및 붙여넣기 기능은 부하 추정이 수행된 툴 번호 탭에서만 실행할 수 있습니다.
{% endhint %}

