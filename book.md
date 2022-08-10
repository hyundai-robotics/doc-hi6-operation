# Hi6 로봇제어기 조작설명서



# 이 설명서에 대하여

이 설명서는 현대로보틱스 Hi6 제어기의 기본 사항과 구조 및 산업용 로봇의 공통 조작에 대해 설명합니다. 각 장에서는 기본 조작 방법뿐만 아니라 여러 응용 기능의 사용 방법에 대해 설명합니다.

이 설명서에서는 협동로봇을 이용한 직접 교시와 안전 기능 설정 방법, 스폿 용접 기능, 아크 용접 기능, 포지셔너 동기 기능, 센서 동기 기능 등의 응용 기능에 대해서는 자세히 다루지 않습니다. 관련 정보에 대한 자세한 내용은 협동로봇 보수 설명서와 응용 기능별 설명서를 참조하십시오.

제품을 사용하기 전에 반드시 설명서의 내용을 충분히 숙지하시기 바랍니다. 또한 필요할 때 언제든 볼 수 있도록 설명서를 가까운 장소에 보관하십시오.

이 설명서는 현대로보틱스 제품을 구매한 고객에게 참조용으로 제공되거나 교육을 위한 내부 교육 자료로 제공되어 사용될 수 있습니다.

이 설명서는 표준 사양을 기준으로 작성되었으므로 구입하신 제품의 모델에 따라 일부 내용이 다를 수 있습니다. 또한 이 설명서의 내용과 사양은 제품의 성능 향상을 위해 예고 없이 변경될 수 있으며 부정확한 내용이나 오탈자로 인해 발생하는 상황에 대해서 현대로보틱스는 책임이 없습니다. 개정에 관한 상세한 정보는 당사의 인터넷 웹사이트\(www.hyundai-robotics.com\)를 방문하여 확인하시기 바랍니다.



# 저작권

이 제품과 설명서에서 다루고 있는 모든 프로그램과 파일, 콘텐츠는 저작권 법과 비밀 유지 계약에 의하여 보호받고 있습니다. 현대로보틱스가 명시적으로 허용하지 않은 사용, 복사, 제 3자에의 공개 및 배포 등의 행위는 엄격히 금지됩니다.



Copyright ⓒ 2020 HYUNDAI ROBOTICS. All rights reserved.

# 표기 규약

이 설명서에서는 내용의 이해를 돕기 위해 다음의 표기 규약과 안전 지시를 사용합니다.

## 그림설명

그림은 제품 조작 방법의 이해를 돕고 화면을 설명하는데 사용합니다. 그림을 설명할 때에는 다음과 같이 해당 부분에 숫자를 표기하고 그에 대응하는 내용을 설명합니다.

![](../_assets/image_1.png)

## GUI \(Graphical User Interface\)

GUI는 메뉴 이름 및 버튼 이름을 대괄호\(\[ \]\) 안에 넣고 굵은 글씨로 표시합니다. 여러 메뉴를 순서대로 선택해야 할 때에는 이름 사이에 &gt; 기호를 넣어 표시합니다.

* 이름이 있는 메뉴: 수동 또는 자동 모드의 초기 화면에서 \[메뉴\] 버튼을 터치하십시오.
* 여러 메뉴: 수동 모드의 초기 화면에서 \[설정\] 버튼 &gt; \[5: 초기화 &gt; 7: 유닛 설정\] 메뉴를 터치하십시오.



## 조작키 표기법

기능 조작을 위하여 티치 펜던트의 조작부에서 누르는 키는 홑화살괄호\(&lt; &gt;\)에 넣고 굵은 글씨로 표시합니다.

* &lt;시작&gt; 키를 누르면 로봇에 작성된 프로그램의 자동 운전을 시작합니다.

## 상호 참조

설명서 내에서 연관된 정보로의 바로가기를 제공합니다. 상호 참조는 다음과 같이 굵은 글씨에 큰따옴표\(“ ”\)로 표시합니다.

* 날짜와 시간 정보 변경에 대한 자세한 내용은 “[4.5 날짜 및 시간 설정](../menu/date-time-setting.md)”을 참조하십시오.

## 참고 사항

제품을 사용할 때 알아 두면 좋을 유용한 사항이나 추가적인 정보를 다음과 같이 제공합니다.

{% hint style="info" %}
상태 표시줄에  ![](../_assets/eng-mode.png) 아이콘이 깜빡이면 엔지니어\(engineer\) 모드 상태입니다.
{% endhint %}



### 



# 안전 주의 사항

제품의 올바른 사용과 사용자의 안전을 확보하고 재산상의 피해 방지를 위해 반드시 다음의 안전 주의 사항을 숙지한 후 제품을 사용하시기 바랍니다.

### 위험

{% hint style="danger" %}
\[위험\] 긴박한 위험: 준수하지 않았을 경우 작업자가 사망하거나 중상을 입을 수 있습니다.
{% endhint %}

* 설명서의 제품 설치 내용을 숙지하고 지시 사항을 준수하여 로봇 제품과 기타 장치를 설치하십시오.
* 소프트웨어에 치명적인 오류가 발생하면 즉시 사용을 중단하고 고객지원팀에 연락하십시오.
* 제품의 고장이나 파손 등 문제가 있을 때에는 즉시 사용을 중단하고 고객지원팀에 문의하십시오.



### 경고

{% hint style="warning" %}
\[경고\] 잠재적인 위험: 준수하지 않았을 경우 작업자가 상해를 입거나 제품이 크게 손상되는 등 재산상의 손해를 입을 수 있습니다.
{% endhint %}



* 제어기와 연결하여 사용할 안전 장비는 반드시 안전용 접점 단자 또는 Safety I/O로 설정한 Configurable digital I/O에 이중 신호로 연결하십시오. 일반 접점 단자에 연결하거나 단일 신호로 연결할 경우 규정된 안전 수준을 충족할 수 없습니다.
* 제어기의 내부 브래킷 뒤로 손가락 등의 신체 부위를 집어 넣지 마십시오. 감전이나 상해의 위험이 있습니다.
* 로봇 응용 시스템 제조자나 로봇 사용자는 설명서의 내용을 숙지하고 제품의 운영 교육을 이수하십시오.
* 작업자와 사용자의 안전을 위해 제품 설치 전 반드시 안전 펜스 등 적절한 안전 시설을 마련하십시오.
* 규격 정보를 확인하여 알맞은 고정 나사를 사용하여 지정된 토크로 체결하십시오. 나사가 헐거우면 로봇이 설치 장소에서 분리되어 추락하거나 손상될 수 있습니다.
* 제품의 연결부\(전원 및 케이블\)에 액체나 먼지, 금속 가루 등의 전도성 이물질이 들어가지 않도록 주의하십시오. 또한 연결부를 뾰족한 물체로 찌르거나 케이블 연결 시 무리한 힘을 가하지 마십시오. 연결 단자의 부식 또는 일시적인 단락으로 제품이 폭발하거나 화재가 발생할 수 있습니다.
* 배선 정보를 확인하고 장치 유형에 맞춰 알맞은 단자를 이용해 장치를 연결하십시오. 특히, 안전 장치는 일반 단자에 연결하면 안전 기능을 보장할 수 없으므로 반드시 안전 장치용 단자에 연결하십시오.
* 손상된 케이블을 절대 사용하지 말고 제품 사용 중에는 전원을 분리하지 마십시오. 감전, 화재, 고장, 및 상해의 원인이 될 수 있습니다.
* 제품을 장시간 사용하면 열이 발생하여 화상 등 상해의 위험이 있습니다. 제품을 만져야 할 경우에는 전원을 끄고 1시간 이상 방치하여 제품을 충분히 냉각한 후 작업하십시오.
* 로봇의 움직임에 주의하여 티치 펜던트를 사용하십시오.
* 티치 펜던트에서 치명적인 에러를 경고하는 경우 즉시 비상 정지 스위치로 로봇을 정지하고 원인을 파악하여 에러를 해결하십시오. 에러를 해결할 수 없는 경우 고객지원팀에 문의하십시오.
* 절대 무단으로 제품을 설치, 개조, 분해 및 수리하지 마십시오. 고장 및 사고의 원인이 될 수 있습니다. 또한 이로 인한 제품의 손상 및 파손에 대해 당사는 책임지지 않습니다.



### 주의

{% hint style="warning" %}
\[주의\] 저위험 요소 : 준수하지 않았을 경우 작업자가 경미한 상해를 입거나 제품이 손상되는 등 재산상의 손해를 입을 수 있습니다. 
{% endhint %}



* 제품을 임의로 설치 또는 개조, 분해, 수리하지 마십시오. 또한 당사의 전문가 이외의 사람이 임의로 제품을 개조하거나 부품을 부착하는 행위를 금합니다. 이로 인한 제품 고장 발생 시 무상 서비스 및 품질 보증 서비스를 받을 수 없습니다.
* 자격이 있는 설치 전문가가 해당 국가 및 지역의 관련 규정 및 법규를 준수하여 제품을 설치해야 합니다. 제품을 설치 및 수리할 때에는 고객지원팀에 문의하여 전문가에게 의뢰하십시오.
* 먼지가 많거나 더러운 곳에 제품을 설치 및 사용하지 마십시오. 먼지나 이물질로 인해 제품이 고장 나거나 성능에 이상이 발생할 수 있습니다.
* 자성이 있거나 자성의 영향이 미치는 곳 또는 전자파 장해가 있는 곳에 제품을 설치 및 사용하지 마십시오. 자성에 의해 제품이 손상되거나 성능에 이상이 발생할 수 있습니다.
* 제품 운전 시에는 헐거운 옷이나 장신구를 착용하지 말고, 머리카락이 긴 경우에는 뒤로 묶어 로봇의 관절 등에 끼이지 않도록 주의하십시오.
* 제품 동작 중에는 작동 범위 내에 들어가거나 로봇을 만지지 마십시오. 상해의 위험이 있습니다.
* 제품은 포장된 상태로 운반하여 파손을 피하고 습도가 낮은 건조한 장소에 보관하십시오. 포장 자재 내부에 습기로 제품이 손상되거나 고장 날 수 있습니다.
* 제품은 온도와 습도가 변하기 쉬운 곳을 피하고, 깨끗하고 서늘하며 건조한 곳에 보관하십시오.
* 제품 운반 시에는 올바를 자세를 유지하고 두 명 이상이 함께 작업하십시오. 허리나 팔, 다리 등의 신체 부위에 상해를 입을 수 있습니다.
* 리프팅 장비를 이용해 제품을 운반하는 경우에는 해당 국가 및 지역의 안전 규정 및 장비 사용 지침을 준수하십시오.
* 설명서의 운반 내용을 숙지하고 지시 사항을 준수하여 제품을 운반하십시오. 고객의 제품 운송으로 발생한 제품의 손상 및 파손에 대해 당사는 책임지지 않습니다.



# 1. 로봇 시스템

# 1.1 기본 구성

산업용 로봇이란 “자동 제어에 의한 조작\(manipulation\) 기능 및 이동 동작 기능이 탑재되어 산업 현장에서 다양한 작업을 프로그램으로 실행할 수 있는 기계”입니다. 협동로봇은 산업용 로봇의 한 종류입니다.

로봇 시스템은 로봇 본체와 본체를 제어하는 제어기로 구성됩니다. 제어기에는 로봇 시스템의 설정 및 수동 조작에 사용하는 티치 펜던트가 부착됩니다.

* 로봇: 물체를 운반하거나 부품을 조립하는 등 산업 현장에서 다양한 작업을 수행합니다.
* 제어기: 티치 펜던트로 설정한 프로그램의 설정값에 따라 로봇의 동작을 조정합니다. 제어기의 입출력 포트를 이용해 다양한 외부 장비 또는 장치와 연동할 수 있습니다.
* 티치 펜던트: 로봇 시스템 전체를 관리하는 장치입니다. 로봇에게 특정 자세를 학습시키거나 프로그램을 설정 및 제어할 수 있습니다.

로봇 유형에 따른 로봇 시스템의 기본 구성의 예는 다음과 같습니다.

![그림 1 LCD 로봇 시스템의 기본 구성](../../_assets/image.png)

![그림 2 수직다관절로봇 시스템의 기본 구성](../../_assets/image_6.png)

![그림 3 협동로봇 시스템의 기본 구성](../../_assets/image_8.png)

# 1.1.1 제어기

## 수직다관절로봇 제어기

![그림 4 제어기 앞면\(좌\) / 뒷면\(우\)](../../_assets/image_33.png)

| 번호 | 이름 | 설명 |
| :--- | :--- | :--- |
| ![](../../_assets/c1.png) | 연결부 | 제어기에 기구 및 티치 펜던트를 연결하거나 응용 장치를 내부의 모듈과 연결하는 통로입니다. |
| ![](../../_assets/c2.png) | 전원 스위치 | 제어기의 주전원을 켜거나 끕니다. |
| ![](../../_assets/c3.png) | TP 보관용 고리 | 티치 펜던트를 걸어 보관합니다. |
| ![](../../_assets/c4.png) | 비상 정지 스위치 | 긴급 상황 발생 시 비상 정지 스위치를 눌러 로봇의 동작을 정지시킵니다. |
| ![](../../_assets/c5.png) | 냉각팬 | 제어기 내부의 가열된 공기를 외부로 강제 유출시키는 장치입니다. |

## 협동로봇 제어기

![그림 5 제어기 앞면\(좌\) / 뒷면\(우\)](../../_assets/image_15.png)

| 번호 | 이름 | 설명 |
| :--- | :--- | :--- |
| ![](../../_assets/c1.png) | 로봇 케이블 커넥터 | 통신선과 전원선이 내장되어 제어기를 기구와 연결하는 커넥터입니다. |
| ![](../../_assets/c2.png) | 전원 커넥터 | 제어기에 전원을 공급하는 커넥터입니다. |
| ![](../../_assets/c3.png) | 전원 차단기 | 전원 스위치를 이용해 제어기의 주전원을 켜거나 끕니다. |
| ![](../../_assets/c4.png) | 환풍구 | 제어기의 냉각을 위한 공기 유입 통로입니다. |
| ![](../../_assets/c5.png) | 손잡이 | 제어기의 전면과 후면에 장착되어 운반에 사용합니다. |
| ![](../../_assets/c6.png) | 비상 정지 스위치 | 긴급 상황 발생 시 비상 정지 스위치를 눌러 로봇의 동작을 정지시킵니다. |
| ![](../../_assets/c7.png) | 응용 장치 연결구 | 응용 장치를 내부의 모듈과 케이블로 연결할 경우 사용하는 통로입니다. |
| ![](../../_assets/c8.png) | 티치 펜던트 연결구 | 직결형의 티치 펜던트를 연결하는 통로입니다. |
| ![](../../_assets/c9.png) | I/O 연결 블록 | 주변 기기를 제어기에 연결합니다. |
| ![](../../_assets/c10.png) | 도어 | 도어를 열어 제어기의 측면을 개방합니다. |
| ![](../../_assets/c11.png) | 냉각팬 | 제어기 내부의 가열된 공기를 외부로 강제 유출시키는 장치입니다. |

# 1.1.2 티치 펜던트

티치 펜던트는 TP600과 TP630을 지원합니다. 이 조작 설명서에서는 TP600 모델을 기준으로 사용 방법을 설명합니다.

TP600은 Hi6 제어기 전용으로 개발된 모델로 큰 화면의 터치 스크린을 제공합니다.

![그림 6 TP600 앞면\(좌\) / 뒷면\(우\)](../../_assets/image_16.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">번호</th>
      <th style="text-align:left">이름</th>
      <th style="text-align:left">설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">조작키2</td>
      <td style="text-align:left">로봇의 동작을 제어하고
        명령을 입력하거나 메뉴를
        선택하고 설정합니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">디스플레이</td>
      <td style="text-align:left">터치 스크린으로 로봇의
        동작 상태와 설정 정보를
        확인 및 변경합니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">모드 스위치</td>
      <td style="text-align:left">모드 스위치를 돌려 운전
        모드(
        <img src="../../_assets/sb-manual.png" alt/>수동/
        <img src="../../_assets/sb-auto.png" alt/>자동/
        <img src="../../_assets/sb-remote.png" alt/>원격)를 선택합니다. 티치
        펜던트에서 모드 스위치
        키를 빼면 선택된 운전
        모드로 잠금 설정됩니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">비상 정지 스위치</td>
      <td style="text-align:left">긴급 상황 발생 시 비상
        정지 스위치를 눌러 로봇의
        동작을 정지시킵니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">조그 다이얼</td>
      <td style="text-align:left">조그 다이얼을 돌려 메뉴를
        설정합니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">마운팅 브래킷</td>
      <td style="text-align:left">티치 펜던트를 들거나
        걸어 보관합니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left">인에이블링 스위치</td>
      <td
      style="text-align:left">
        <p>수동 모드에서 티치 펜던트로
          로봇 조작 시, 안전 스위치로
          사용합니다.</p>
        <ul>
          <li>1단, 3단: 로봇 운전이 정지됩니다.
            3단일 경우, 2단을 거치지
            않고 1단으로 복귀합니다.</li>
          <li>2단: 로봇을 조작할 수
            있습니다.</li>
        </ul>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c8.png" alt/>
      </td>
      <td style="text-align:left">케이블 연결 커넥터</td>
      <td
      style="text-align:left">제어기와 연결하기 위한
        케이블을 연결하는 커넥터입니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c9.png" alt/>
      </td>
      <td style="text-align:left">USB 연결 포트</td>
      <td style="text-align:left">이동식 저장 장치 등 USB
        통신으로 접속 가능한
        장치를 연결합니다.</td>
    </tr>
  </tbody>
</table>

TP630은 기존 Hi5a 제어기와 동일한 조작키 사용 환경을 적용한 모델로 TP600의 화면과 유사한 구성의 화면을 제공합니다.

![그림 7 TP630 앞면\(좌\) / 뒷면\(우\)](../../_assets/image_31.png)

## 조작키

<table>
  <thead>
    <tr>
      <th style="text-align:left">조작키</th>
      <th style="text-align:left">이름</th>
      <th style="text-align:left">설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-shift.png" alt/>
      </td>
      <td style="text-align:left">shift</td>
      <td style="text-align:left">
        <ul>
          <li>&lt;shift&gt; 키를 특정 키와 함께
            누르면 해당 키의 기능이
            전환됩니다.</li>
          <li>JOB 편집 창에서 &lt;↑/↓&gt;
            키와 함께 누르면 사용
            중인 화면을 전환할 수
            있습니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-ctrl.png" alt/>
      </td>
      <td style="text-align:left">ctrl</td>
      <td style="text-align:left">&lt;ctrl&gt; 키를 특정 키와 함께
        누르면 해당 키에 정의된
        기능이 실행됩니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-up-dn.png" alt/>
      </td>
      <td style="text-align:left">위/아래</td>
      <td style="text-align:left">수동 모드에서 &lt;↓/↑&gt;
        키를 누르면 스텝 단위로
        전진 또는 후진합니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-stop.png" alt/>
      </td>
      <td style="text-align:left">정지</td>
      <td style="text-align:left">
        <p>&lt;정지&gt; 키를 누르면 자동
          운전 중인 로봇이 일시적으로
          멈춥니다.</p>
        <ul>
          <li>로봇이 정지하면 정지
            램프가 켜지고 시작 램프가
            꺼집니다.</li>
          <li>로봇은 작성된 프로그램의
            경로 수행 중에 정지된
            상태이므로 주변 장치와
            충돌할 위험은 없습니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-start.png" alt/>
      </td>
      <td style="text-align:left">시작</td>
      <td style="text-align:left">&lt;시작&gt; 키를 누르면 로봇에
        작성된 프로그램의 자동
        운전을 시작합니다. 로봇의
        자동 운전이 시작되면
        시작 램프가 켜지고 정지
        램프가 꺼집니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-mot-on.png" alt/>
      </td>
      <td style="text-align:left">모터</td>
      <td style="text-align:left">
        <p>로봇 각 축의 모터에 서보
          전원을 공급합니다.</p>
        <ul>
          <li>수동 모드에서 &lt;모터&gt;
            키를 누르면 모터 램프가
            깜빡입니다.</li>
          <li>자동 모드에서 &lt;모터&gt;
            키를 누르면 모터 램프가
            켜집니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-enter.png" alt/>
      </td>
      <td style="text-align:left">enter</td>
      <td style="text-align:left">
        <ul>
          <li>수치 입력 시 &lt;enter&gt; 키를
            누르면 입력값이 설정에
            적용됩니다.</li>
          <li>허락/거부(Yes/No)의 응답에
            대해 &lt;enter&gt; 키를 누르면
            허락(Yes)이 선택됩니다.</li>
          <li>수동 모드에서 명령문
            수정 시, 문장 커서 상태에서
            &lt;enter&gt; 키를 누르면 명령문
            인수를 편집할 수 있는
            단어 커서 상태로 전환됩니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-esc.png" alt/>
      </td>
      <td style="text-align:left">esc</td>
      <td style="text-align:left">
        <ul>
          <li>키 입력이나 진행 중인
            각종 기능을 취소합니다.</li>
          <li>&lt;esc&gt; 키를 누르면 변경
            내용을 저장하지 않고
            상위 레벨로 전환할 수
            있습니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-left-right.png" alt/>
      </td>
      <td style="text-align:left">왼쪽/오른쪽</td>
      <td style="text-align:left">
        <ul>
          <li>텍스트 입력 시, 커서를
            이전 또는 다음으로 이동합니다.</li>
          <li>단어 커서 상태에서 &lt;←/→&gt;
            키를 누르면 기록된 스텝이나
            다른 기능 인수로 이동합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/key-num.png" alt/>
      </td>
      <td style="text-align:left">
        <p>숫자키</p>
        <p>조그키</p>
      </td>
      <td style="text-align:left">
        <ul>
          <li>숫자를 입력합니다.</li>
          <li>&lt;shift&gt; 키와 함께 누르면
            부호(- / +)나 쉼표(,)를 입력하거나,
            명령문 또는 인수를 삭제할
            수 있습니다.</li>
          <li>&lt;BS&gt;: Backspace. 커서가 입력된
            위치에서 텍스트를 한
            글자씩 지웁니다. 또한
            명령어 편집 시 인수를
            선택하고 &lt;BS&gt; 키를 누르면
            인수 값 전체를 삭제할
            수 있습니다.</li>
        </ul>
        <p>수동 모드에서 모터가
          켜진 상태에서 인에이블링
          스위치를 잡고 있는 동안,
          &lt;enter/esc/←/→&gt; 키와 숫자키는
          ‘조그키’로 동작합니다.</p>
        <ul>
          <li>각 키에 지정된 축의 이름은
            디스플레이의 우측 가장자리에
            표시됩니다.</li>
          <li>&lt;→&gt; 키는 증가(+), &lt;←&gt;
            키는 감소(-) 방향입니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

# 1.2    기본 사용

# 1.2.1 전원 켜기

{% hint style="info" %}
전원을 켜고 끄는 방법은 제어기별로 다를 수 있습니다.
{% endhint %}

#### 수직다관절로봇 제어기

로봇을 기동하려면 로봇 제어기에 전원을 공급해야 합니다.

제어기 좌측의 전원 스위치를 ON 방향으로 돌리십시오. 제어기의 메인 전원이 연결됩니다. 전원이 연결되면 로봇 시스템이 부팅되어 티치 펜던트의 디스플레이가 켜지고 모든 장치가 켜집니다.



![](../../../_assets/image_12.png)

#### 협동로봇 제어기

협동로봇의 전원은 제어기의 전원 커넥터를 통해 공급됩니다.

전원 차단기의 스위치를 밀어 올리십시오. 전원이 연결되면 로봇 시스템이 부팅되어 티치 펜던트의 디스플레이가 켜지고 협동로봇 LED 램프가 흰색으로 켜집니다.

![](../../../_assets/image_23.png)

### 



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

# 1.2.2 전원 끄기

모든 작업을 수행한 후, 로봇을 정지하고 제어기의 전원 버튼을 끄는 모든 동작을 말합니다.

{% hint style="warning" %}
* 로봇을 장시간 사용하지 않을 때에는 엔코더 배터리가 방전될 수 있으므로 로봇을 기준 위치로 이동시킨 후 전원을 해제하십시오.
* 엔코더 배터리에 전압 저하 알람이 발생한 상태에서 전원을 해제하면 엔코더 데이터가 소멸될 수 있으므로 주의하십시오.
{% endhint %}

#### 수직다관절로봇 제어기

1. 티치 펜던트의 &lt;정지&gt; 키를 누르십시오. 운전 중인 로봇이 동작을 멈추고 정지 램프가 켜집니다.

2. 티치 펜던트의 비상 정지 스위치를 누르십시오. 로봇 모터에 서보 전원이 차단되어 모터가 꺼집니다.

![](../../_assets/image_36.png)



3. 제어기 좌측의 전원 스위치를 OFF 방향으로 돌리십시오. 로봇 시스템의 전원이 차단됩니다.

![](../../_assets/image_29.png)

#### 협동로봇 제어기

1. 티치 펜던트의 &lt;정지&gt; 키를 누르십시오. 운전 중인 로봇이 동작을 멈추고 정지 램프가 켜집니다.

2. 제어기의 비상 정지 스위치를 누르십시오. 로봇 모터에 서보 전원이 차단되어 모터가 꺼집니다.



![](../../_assets/image_11.png)



3.  전원 차단기의 스위치를 밀어 내리십시오. 전원이 차단되면 로봇 시스템이 꺼져 티치 펜던트의 디스플레이와 협동로봇의 LED 램프가 꺼집니다.

![](../../_assets/image_288.png)

# 1.2.3 티치펜던트 화면의 언어 변경하기

티치펜던트의 언어가 맞지 않을 경우, 다음의 절차로 변경할 수 있습니다. 다음 예는 한국어 모드를 영어 모드로 변경하는 예입니다.

1.	우버튼 막대의 \[메뉴\] 버튼을 클릭하십시오.

![](../../_assets/image_291.png)

2.	\[9: TP 응용프로그램 종료\]를 선택하십시오.

![](../../_assets/image_293.png)

3.	우 상단의 지구본 아이콘을 클릭하십시오.

![](../../_assets/image_289.png)

4.	팝업 메뉴에서 \[English\]를 선택하십시오.

![](../../_assets/image_282.png)

5.	우하단의 \[run TP\] 버튼을 클릭하고, 8초 정도 기다리십시오.

![](../../_assets/image_294.png)

# 1.2.4 Hi6 티치 펜던트 화면

로봇의 동작을 제어하거나 로봇과 연동된 장치를 관리할 수 있습니다. Hi6 티치 펜던트 화면은 다음과 같이 구성됩니다.

![](../../../_assets/image_34.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">상태 표시줄입니다. 티치
        펜던트의 통신 상태와
        운전 모드, 로봇 시스템의
        상태와 메커니즘을 표시합니다.
        자세한 내용은 “<a href="status-bar.md">1.2.4.1 상태 표시줄</a>”을
        참조하십시오.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">기능 버튼을 이용해 설정값을
        확인하고 변경합니다.
        자세한 내용은 “<a href="function-buttons.md">1.2.4.3 기능 버튼</a>”을
        참조하십시오.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">작업 영역입니다. JOB 프로그램을
        편집하고 모니터링 정보를
        확인하는 등 다양한 작업을
        수행합니다. 여러 작업을
        동시에 수행할 수 있습니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">메뉴 버튼을 이용해 메뉴의
        설정값을 확인 및 변경하고,
        다양한 기능을 실행합니다.
        자세한 내용은 “<a href="menu-buttons.md">1.2.4.4 메뉴 버튼</a>”을
        참조하십시오.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">조그 막대입니다. [좌표계]
        버튼으로 선택한 조그
        수행의 기준 좌표계에
        따라 변경된 축의 이름이
        표시됩니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">
        <p>이력 표시줄입니다. 자세한
          내용은 “<a href="log-bar.md">1.2.4.2 이력 표시줄</a>”을
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

# 1.2.4.1 상태 표시줄

![그림 9 상태 표시줄](../../../_assets/image_1.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">로봇 제어기 플랫폼의
        이름입니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">티치 펜던트와 로봇 제어기
        본체의 COM 모듈 간 이더넷
        통신의 상태를 표시합니다.
        (
        <img src="../../../_assets/flag-comm-ok.png" alt/>: 정상 /
        <img src="../../../_assets/flag-comm-ng.png"
        alt/>: 응답 없음)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
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
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">로봇 시스템의 다양한
        상태를 표시합니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">로봇의 동작 상태를 표시합니다.
        (
        <img src="../../../_assets/flag-mot-on.png" alt/>: 모터 ON /
        <img src="../../../_assets/flag-start.png"
        alt/>: 로봇 재생 중 /
        <img src="../../../_assets/flag-stop.png"
        alt/>: 로봇 정지)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">선택된 로봇 메커니즘의
        모델명을 표시합니다.</td>
    </tr>
  </tbody>
</table>

# 1.2.4.2 이력 표시줄

![그림 10 이력 표시줄](../../../_assets/image_22.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">날짜와 시간 정보가 표시됩니다.
        [메뉴] 버튼 &gt; [08: 날짜, 시간
        설정] 메뉴를 터치하면
        날짜와 시간 정보를 변경할
        수 있습니다. 날짜와 시간
        정보 변경에 대한 자세한
        내용은 “<a href="../../../menu/date-time-setting.md">4.5 날짜 및 시간 설정</a>”을
        참조하십시오.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
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
            내용은 “<a href="../../../operation/error-info/">2.5 에러 정보</a>”를
            참조하십시오.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <p>화면에 소프트 키보드를
          표시합니다. 소프트 키보드의
          사용 방법에 대한 자세한
          내용은 “<a href="../../../programming/prog-edit/statement-edit/softkeyboard.md">3.2.4.4 소프트 키보드</a>”를
          참조하십시오.</p>
        <ul>
          <li>소프트 키보드 사용 중에
            [
            <img src="../../../_assets/bt-dock-softkb.png" alt/>] 버튼을 터치하면 키보드의
            위치를 화면 상단으로
            이동할 수 있습니다.</li>
          <li>소프트 키보드를 숨기려면,
            [
            <img src="../../../_assets/bt-softkb.png" alt/>] 버튼을 터치하십시오.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

# 1.2.4.3 기능 버튼

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>[기록조건] 버튼: move 문 기록
          조건의 기본값을 설정합니다.</p>
        <p>[기록조건] 버튼을 터치한
          후 설정창에서 보간, 이동
          속도와 단위, Accuracy, 툴 번호를
          입력하고 [확인] 버튼(
          <img
          src="../../../_assets/icon-ok.png" alt/>)을 터치하십시오.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/lbt-bar.png" alt/>
      </td>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>[실행단위] 버튼: 수동
          또는 자동 모드에서의
          프로그램 실행 단위를
          설정합니다.</p>
        <p>수동 모드: 원하는 옵션이
          나타날 때까지 [실행단위]
          버튼을 반복해서 터치하십시오.</p>
        <ul>
          <li>
            <img src="../../../_assets/bt-runto-cmd.png" alt/>[cmd]: 명령어 한 행씩 실행합니다.</li>
          <li>
            <img src="../../../_assets/bt-runto-step.png" alt/>[step]: 한 스텝씩 실행합니다.</li>
          <li>
            <img src="../../../_assets/bt-runto-end.png" alt/>[end]: end 명령문까지 실행합니다.</li>
          <li>자동 모드: [실행단위]
            버튼을 터치한 후 설정창에서
            옵션을 설정하십시오.</li>
          <li>
            <img src="../../../_assets/bt-spd_manual (3) (3) (3) (3).png"
            alt/>[1cycle]: end 명령문까지 실행
            후 정지합니다.</li>
          <li>
            <img src="../../../_assets/bt-runto-cont.png" alt/>[cont]: end 명령문까지 실행
            후 스텝 0부터 다시 실행합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <p>[속도조절] 버튼: 사용자의
          안전을 위해 스텝 속도를
          설정합니다.</p>
        <p>[속도조절] 버튼을 터치한
          후 설정창에서 스텝 전후진
          최고 속도와 자동 운전
          속도 비율을 설정하십시오.</p>
        <ul>
          <li>
            <img src="../../../_assets/bt-spd_manual (3) (3) (3) (3) (2).png"
            alt/>수동 모드: 스텝 FWD/BWD 제한
            속도(㎜/sec)를 표시합니다.</li>
          <li>
            <img src="../../../_assets/bt-spd_manual (3) (3) (3) (3) (1).png"
            alt/>자동 모드: 재생 속도(%)를
            표시합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p>[조그 속도 레벨/조그 인칭]
          버튼: 축별 또는 직교 조그의
          속도 레벨과 조그키의
          사용 모드를 설정합니다.</p>
        <ul>
          <li>[
            <img src="../../../_assets/bt-spd-up.png" alt/>/
            <img src="../../../_assets/bt-spd-dn.png" alt/>]: 원하는 축별 또는 직교
            조그의 속도 레벨(1: 저속
            ~ 8: 고속)이 나타날 때까지
            버튼을 반복하여 터치하십시오.
            버튼을 길게 터치하면
            최저 또는 최고 레벨을
            한 번에 설정할 수 있습니다.</li>
          <li>
            <img src="../../../_assets/bt-jog-1.png" alt/>
            <img src="../../../_assets/bt-jog-inch.png" alt/>[1]: 레벨 값을 터치하면
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
        <img src="../../../_assets/c5.png" alt/>
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
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left">
        <p>
          <img src="../../../_assets/bt-gun-off.png" alt/>
          <img src="../../../_assets/bt-gun-on.png" alt/>[건] 버튼: 선택된 건 번호를
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
        <img src="../../../_assets/c7.png" alt/>
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

# 1.2.4.4 메뉴 버튼

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
        <img src="../../../_assets/c1.png" alt/>
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
        <img src="../../../_assets/rbt-bar.png" alt/>
      </td>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
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
        <ul>
          <li>
            <img src="../../../_assets/bt-crd-joint.png" alt/>축(Joint) 좌표계: 조그 막대에
            각 축의 이름이 표시됩니다.
            축 이름 우측의 <b>[-/+]</b> 버튼을
            터치하면 해당하는 축을
            움직일 수 있습니다.</li>
          <li>
            <img src="../../../_assets/bt-crd-robot.png" alt/>로봇(Robot) 좌표계: 조그 막대에
            X, Y, Z, RX, RY, RZ와 부가축이 표시됩니다.
            로봇 좌표계를 기준으로
            로봇의 툴 끝(TCP, Tool Center Point)을
            이동 및 회전할 수 있습니다.</li>
          <li>
            <img src="../../../_assets/bt-crd-user.png" alt/>사용자(User) 좌표계: 조그
            막대에 X, Y, Z, RX, RY, RZ와 부가축이
            표시됩니다. 사용자 좌표계를
            기준으로 로봇의 툴 끝(TCP)을
            이동 및 회전할 수 있습니다.</li>
          <li>
            <img src="../../../_assets/bt-crd-tool (1) (1) (2).png" alt/>툴(Tool) 좌표계: 조그 막대에
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
        <img src="../../../_assets/c3.png" alt/>
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
          <img src="../../../_assets/bt-pos-mod.png" alt/>(<b>&lt;shift&gt;</b> 키 조합 시) 위치
          수정: JOB 프로그램에서
          로봇의 현재 자세를 스텝의
          타겟 포즈로 적용합니다.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <p>명령 입력: 원하는 명령어를
          입력합니다.</p>
        <p><b>[명령입력]</b> 버튼을 터치한
          후 명령 입력창에서 명령어를
          터치하십시오. 현재 커서
          위치의 바로 아래에 명령문이
          입력됩니다. 명령 입력에
          대한 자세한 내용은 “
          <a
          href="../../../programming/prog-edit/statement-input/">3.2.2 명령문 입력</a>”을 참조하십시오.</p>
        <p>
          <img src="../../../_assets/bt-delete.png" alt/>(<b>&lt;shift&gt;</b> 키 조합 시) 위치
          수정: JOB 프로그램에서
          로봇의 현재 자세를 스텝의
          타겟 포즈로 적용합니다.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c5.png" alt/>
      </td>
      <td style="text-align:left">
        <p>속성: 명령문의 속성을
          확인합니다.</p>
        <p>명령문을 터치하여 선택한
          후 <b>[속성]</b> 버튼을 터치하십시오.
          명령문의 속성창이 나타납니다.</p>
        <p>
          <img src="../../../_assets/bt-block-edit.png" alt/>(<b>&lt;shift&gt;</b> 키 조합 시) 블록
          편집: JOB 프로그램에서
          복사하기, 잘라내기, 붙여넣기를
          수행할 수 있는 블록 편집
          모드로 진입합니다. 블록
          편집에 대한 자세한 내용은
          “<a href="../../../programming/prog-edit/statement-edit/block-edit-mode.md">3.2.4.5 블록 편집 모드</a>”를
          참조하십시오.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c6.png" alt/>
      </td>
      <td style="text-align:left"><b>[메뉴]</b>: 프로그램의 서비스
        기능 메뉴를 사용합니다.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c7.png" alt/>
      </td>
      <td style="text-align:left"><b>[설정]</b>: 프로그램의 시스템
        메뉴를 이용해 사용 환경을
        설정합니다.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c8.png" alt/>
      </td>
      <td style="text-align:left">
        <p>즐겨찾기: 코드 번호를
          이용해 미리 지정한 기능을
          빠르게 실행합니다.</p>
        <p><b>[즐겨찾기]</b> 버튼을 터치한
          후 코드 번호를 입력하고 <b>[확인]</b> 버튼을
          터치하십시오. 지정된
          기능이 실행됩니다.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <img src="../../../_assets/c9.png" alt/>
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

# 1.2.4.5 작업 영역

JOB 프로그램을 편집하고 모니터링 정보를 확인하는 등 다양한 작업을 수행하는 작업 영역입니다.

![그림 11 작업 영역 구성](../../../_assets/image_24.png)

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
        <img src="../../../_assets/c1.png" alt/>
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
        <img src="../../../_assets/c2.png" alt/>
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
        <img src="../../../_assets/c3.png" alt/>
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

# 2. 운전

운전은 로봇에게 작업 내용을 지시하고 그 내용을 확인하는 행위를 말합니다. 산업용 로봇에서는 일반적으로 수동\(manual\) 운전 방식과 자동\(auto\) 운전 방식을 사용합니다. 수동 운전은 로봇에 작업 내용을 직접 지시하는 것이고 자동 운전은 지시된 작업 내용을 로봇이 반복하여 실행하도록 하는 것입니다.

# 2.1 수동 운전

수동 운전이란 안전한 속도에서 로봇을 직접 교시하고 확인하는 운전 방법입니다.

# 2.1.1 운전 방법

조그키를 이용하여 로봇에 작업 내용을 지시하고 지시된 작업 내용을 확인하는 방법은 다음과 같습니다.

1. 안전 펜스와 로봇의 동작 범위 내에 사람 또는 장애물 유무를 확인하십시오.

2. 티치 펜던트의 모드 스위치를 돌려 운전 방식을 수동 모드로 설정하십시오.



![](../../_assets/image_40.png)

3. Hi6 티치 펜던트 화면의 상태 표시줄에서 운전 방식이 수동 모드로 설정되어 있는지 확인하십시오.

![](../../_assets/image_37.png)

* 자동 모드로 설정된 경우, 티치 펜던트의 모드 스위치를 돌려 운전 방식을 수동 모드로 설정하십시오.

4. JOB 프로그램창에서 **\[프로그램\]** 버튼을 터치하십시오. 프로그램 선택창이 나타납니다.

![](../../_assets/image_39.png)

5. 프로그램 선택창의 목록에서 프로그램을 선택하거나 프로그램 번호를 입력한 후 **\[확인\]** 버튼을 터치하십시오.

![](../../_assets/image_38.png)

 6. 티치 펜던트의 **&lt;모터&gt;** 키를 누르십시오. 모터 램프가 깜빡이고 로봇 각 축의 모터에 서보 전원 공급을 위한 준비 상태가 됩니다.

7. 티치 펜던트 뒷면의 인에이블링 스위치를 누르십시오. 모터 램프가 켜지고 모터의 브레이크가 해제되어 서보 전원이 공급됩니다. 로봇을 움직일 수 있는 상태가 됩니다.

8. 조그키를 이용해 속도 레벨이나 좌표계의 이동 조건에 따라 로봇을 조작하십시오.

* 로봇의 위치를 저장하려면, 원하는 위치에서 **\[기록\]** 버튼을 터치하십시오. 스텝이 기록됩니다.
* 스텝에 필요한 기능을 기록하려면, **\[명령입력\]** 버튼을 터치하십시오.
* 수동으로 전진 또는 후진하며 기록된 로봇의 위치를 확인하려면 &lt;↓/↑&gt; 키를 누르십시오. &lt;↓/↑&gt; 키를 누르고 있는 동안 로봇이 스텝 단위로 이동합니다. 로봇이 목표 스텝에 도달하면 명령어 앞에 수행 완료 표시\( . \)가 나타나고 정지합니다.



# 2.1.2    운전 속도 조정

수동 모드에서는 스텝 전후진 운전과 수동 조그 조작을 이용해 로봇을 조작합니다. Hi6 티치 펜던트 화면 좌측의 기능 버튼으로 스텝의 전후진 제한 속도\(![](../../_assets/c1.png)\)와 조그의 속도 레벨\(![](../../_assets/c2.png)\)을 확인하고 조절할 수 있습니다.

![](../../_assets/lbt-spd-bar.png)

스텝의 제한 속도를 설정하려면, \[속도조절\] 버튼을 터치한 후 설정창에서 속도값을 입력하십시오. 스텝 전후진 제한 속도는 \[속도조절\] 버튼에 단위\(㎜/sec\)와 함께 숫자로 표시됩니다. 로봇 툴과 링크의 최고 속도는 제한 속도 이하로 제한됩니다.

![](../../_assets/cond-set-step-fwd-bwd-spd.png)

예를 들어, 수동 모드의 제한 속도가 250 ㎜/s로 설정되어 있고 기록된 스텝의 속도가 1000 ㎜/s일 경우 스텝 전후진 운전 시 스텝의 이동 속도는 250 ㎜/s로 제한됩니다. 기록 속도가 100 ㎜/s 일 경우, 기록 속도가 제한 속도를 초과하지 않으므로 로봇은 100 ㎜/s로 이동합니다.

{% hint style="info" %}
자동 모드일 때, \[속도조절\] 버튼에는 스텝 제한 속도\(㎜/sec\) 대신 재생 속도\(%\)가 표시됩니다.
{% endhint %}

조그 속도 레벨\(1: 저속~8: 고속\)을 설정하려면, 원하는 속도 레벨이 나타날 때까지 \[/\] 버튼을 반복하여 터치하십시오. 조그 속도 레벨은 \[/\] 버튼 사이에 숫자로 표시됩니다. 이 때에도 로봇 툴과 링크의 최고 속도는 제한 속도 이하로 제한됩니다.

![](../../_assets/lbt-spd-bar2.png)

{% hint style="warning" %}
\[주의\] 툴 데이터의 길이와 각도가 실제와 다르게 설정되어 있으면 수동 모드에서 툴이 너무 빠르게 동작할 수 있습니다. 로봇을 조작하기 전에 반드시 툴 데이터가 올바르게 설정되어 있는지 확인하십시오.
{% endhint %}



# 2.1.3 스텝 전후진

스텝 전후진이란 수동 모드에서 로봇을 조작하는 방법의 하나로 기록된 프로그램을 재생하는 것입니다. 스텝 전후진으로 로봇을 조작하면 기록된 프로그램의 경로와 상호 인터록 관계를 안전한 속도 범위에서 확인할 수 있습니다.

스텝 전후진 시 실행 단위는 Hi6 티치 펜던트 화면 좌측의 **\[실행단위\]** 버튼에서 확인 및 설정할 수 있습니다.

![](../../_assets/lbt-runto.png)

스텝 전후진 시 실행 단위를 설정하려면, 원하는 옵션이 나타날 때까지 **\[실행단위\]** 버튼을 반복해서 터치하십시오.

![](../../_assets/bt-runto-sw.png)

* **\[cmd\]**: 명령어 한 행씩 실행합니다.
* **\[step\]**: 한 스텝씩 실행합니다.
* **\[end\]**: end 명령문까지 실행합니다.

실행 단위가 **cmd** 또는 **step**으로 설정되어 있을 때, 로봇은 설정된 Accuracy 영역을 무시하고 기록된 스텝까지 도달하지만 **end**로 설정되어 있을 경우에 로봇은 자동 모드에서의 재생 시와 동일한 경로로 동작합니다.

실행 단위를 **cmd** 또는 **step**으로 설정하고 스텝 전후진을 수행할 때는 코너링이 없는 경로상에서 로봇이 동작합니다. 코너링에 대한 자세한 내용은 “[2.3.1.4 Accuracy](../step/step-cmd-param/accuracy.md)”를 참조하십시오.

![그림 12 cmd/step 설정 시 재생 전후진 경로](../../_assets/path-cmd-step-pback-fwd-bwd.png)

실행 단위를 **end**로 설정하고 스텝 전후진을 수행하면 정지 위치에 따라 로봇의 경로가 달라집니다. 즉, 로봇이 코너링이 아닌 다른 곳에서 정지한 후 전진을 실행하면 원래 코너링의 경로를 복구하지만, 후진을 실행하면 기록된 스텝까지 이동하며 이 때 기록된 스텝에서는 정지 후 즉각 이전 스텝으로 이동합니다. 로봇이 코너링에서 정지한 후에는 전후진 시 모두 이전의 코너 경로를 유지합니다.

![그림 13 end 설정 시 재생 전후진 경로](../../_assets/path-end-pback-fwd-bwd.png)

로봇이 코너링에서 정지한 후 전진을 실행하면 원래 코너 경로를 따라 동작합니다. 여기서 다시 후진을 실행하다가 이전 스텝에 다 도달하지 못한 상태에서 다시 전진을 실행할 때는 원래의 코너링의 경로를 만들지 못하는 경우가 있습니다. 즉, 스텝의 거리가 원래 보다 짧아져서 기존의 Accuracy 조건을 만족할 수 없으면 원래의 코너 경로 보다 작게 코너 경로가 만들어집니다.

![그림 14 스텝 후진 후 전진 시 로봇 경로 변경 예](../../_assets/path-step-bwd-then-fwd.png)

스텝 전후진 시의 최고 속도와 펑션 실행 여부를 설정할 수 있습니다. Hi6 티치 펜던트 화면 좌측의 \[실행단위\] 버튼을 터치한 후 설정창에서 속도값과 펑션 실행 옵션을 설정하십시오.

![](../../_assets/cond-set-step-fwd-bwd-spd.png)

* \[2: 스텝 전/후진시 최고속\]: 수동 속도에 설정한 값과 동일합니다.
* \[3: 스텝 전진시 펑션 실행\]: 펑션 실행 옵션을 선택합니다.
  * Off: 스텝 전후진 시 펑션을 실행하지 않습니다. 외부 I/O 조건과 무관하게 로봇 경로만 확인할 수 있습니다. 외부 시스템과의 인터록이 동작하지 않으므로 주의해야 합니다.
  * On: 모든 펑션을 실행합니다. 외부 인터록이 완성된 후 사용해야 합니다.
  * I On: 입력 대기 펑션만 실행합니다. 외부 인터록에 의한 안전 확인이 필요한 경우 사용하십시오.

# 2.2 자동 운전

자동 운전이란 로봇이 작업할 내용을 교시한 후 로봇에게 작업을 시키는 운전 방법입니다.

# 2.2.1 운전 방법

로봇에게 작업 내용을 교시하고 작업을 시키는 방법은 다음과 같습니다.

1.	안전 펜스와 로봇의 동작 범위 내에 사람 또는 장애물 유무를 확인하십시오. 

2.	티치 펜던트의 모드 스위치를 돌려 운전 방식을 자동 모드로 설정하십시오.

![](../../_assets/mode-sw-auto.png)

3.	Hi6 티치 펜던트 화면의 상태 표시줄에서 운전 방식이 자동 모드로 설정되어 있는지 확인하십시오.

![](../../_assets/titlebar-auto.png)

* 수동 모드로 설정된 경우, 티치 펜던트의 모드 스위치를 돌려 운전 방식을 자동 모드로 설정하십시오

4.	초기 화면의 좌측에서 **\[조건설정\]** 버튼을 터치하십시오. 조건 설정창이 나타납니다.

![](../../_assets/image_339.png)



5.	프로그램의 반복 옵션과 로봇의 운전 속도를 설정하십시오.

![](../../_assets/cond-set-cycle-auto-spd.png)

* **\[1: 동작 사이클\]**: 자동 운전 시 실행되는 프로그램의 반복 여부를 설정합니다.
* **\[6: 자동운전 속도비율\]**: 자동 모드에서 프로그램 재생 시 로봇의 운전 속도\(%\)를 설정합니다. 예를 들어, 운전 속도를 100으로 설정하면 스텝의 기록 속도로 로봇이 이동하고 50으로 설정하면 기록 속도의 50% 비율로 로봇이 이동합니다.

6.	티치 펜던트의 **&lt;시작&gt;** 키를 누르십시오. 시작 램프가 켜지고 로봇이 작성된 프로그램에 따라 작업을 수행합니다.



# 2.2.2 운전 속도 조정

자동 운전 시에는 Hi6 티치 펜던트 화면 좌측의 **\[속도조절\]** 버튼에 프로그램 재생 시 로봇의 운전 속도\(%\)가 표시됩니다. 표시된 운전 속도는 스텝에 기록되어 있는 속도에 대한 로봇의 이동 속도의 비율입니다.

![](../../_assets/lbt-auto-spd.png)

{% hint style="info" %}
수동 모드일 때, **\[속도조절\]** 버튼에는 재생 속도\(%\) 대신 스텝 제한 속도\(㎜/sec\)가 표시됩니다.
{% endhint %}

자동 모드에서는 조건 설정의 자동 운전 속도 비율 값을 변경하여 프로그램을 수정하지 않고 로봇의 운전 속도를 조절할 수 있습니다. Hi6 티치 펜던트 화면 좌측의 **\[속도조절\]** 버튼을 터치한 후 설정창에서 \[2: 스텝 전후진시 최고속\] 과 \[6: 자동운전 속도비율\] 옵션의 값을 설정하십시오.

![](../../_assets/cond-set-step-fwd-bwd-spd-auto-spd.png)

# 2.3 스텝

스텝은 작업 프로그램에 기록되어 로봇이 취하는 특정한 자세\(각 축의 위치 또는 툴 끝의 위치\)를 뜻합니다. 즉, 로봇이 움직여 도달한 하나의 위치가 스텝입니다.

로봇은 한 스텝에서 다른 스텝으로 이동하며 다양한 기능을 수행합니다. 로봇이 한 스텝에서 다른 스텝으로 이동하기 위해서는 이동 명령 move와 이동 조건이 필요합니다.

* 이동 명령 move: 로봇 프로그래밍의 기본 단위. 로봇 본체의 이동을 지시하는 명령어입니다. 로봇의 동작에 필요한 최소한의 정보로 구성됩니다.
* 이동 조건: 로봇의 위치, 보간, 속도, Accuracy, 툴 번호 등의 스텝 명령문 인수\(PARAMETER\)



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

# 2.3.1.1 보간

보간은 스텝과 스텝 사이의 보간된 경로를 말하며 \[스텝 N\]의 보간 방법은 \[스텝 N-1\]과 \[스텝 N\] 사이의 경로 형태를 결정합니다.

#### 

#### P-PTP \(Point To Point\) 

툴 끝이 아닌 각 축을 기준으로 두 스텝 사이의 경로를 보간하는 방식으로 일반 보간 방식 중 가장 빠릅니다. 회전형 조인트로 구성된 산업용 로봇의 특성상 툴 끝 경로는 일반적으로 C 자 형태로 형성됩니다.

![그림 15 P-PTP 보간의 툴 끝 경로 예](../../../_assets/image_73.png)

#### 

#### L-직선보간 

직교 공간상에서 두 스텝 사이를 직선으로 이동합니다. 아크 용접 구간 등 직선 경로가 필요한 경우에 사용하며 다음과 같이 손목 자세를 자동으로 바꾸며 이동합니다.

![그림 16 L-직선 보간 예](../../../_assets/image_48.png)

직선보간 시 특정한 조건에서는 로봇이 손목 자세를 자동으로 바꾸지 못합니다. 이 조건을 Singular 자세라고 합니다.

{% hint style="info" %}
자세 보간이 불가능한 Singular 자세는 다음과 같습니다.

* B축이 Dead zone 근처인 경우: Dead zone 설정에 대한 자세한 내용은 “[7.4.5 B축 비사용구역](../../../setting/robot-parameter/b-axis-deadzone.md)”을 참조하십시오.
* B축의 부호가 바뀌는 경우: B축 각도의 부호가 \( - → + \) 또는 \( + → - \) 로 전환되는 경우입니다.
* R2, R1축의 각도 변화가 180도를 초과하는 경우
* S축\(1축\) 회전 중심을 B축\(5축\) 중심이나 툴 끝이 지나가는 경우: 자세는 물론, 궤적 오차나 에러가 발생할 수 있습니다.
* S축의 각도 변화가 180 도를 초과하는 경우
{% endhint %}

#### 

#### C-원호보간

두 스텝 사이를 원호로 생성되는 경로로 이동합니다. 원을 결정하려면 3점이 필요한데 이를 선정하는 기준은 다음과 같습니다.  

* \[스텝 n\]에서 \[스텝 n+1\]로 이동할 때 \[스텝 n+1\]의 보간 방법이 원호보간 C이면 다음 스텝 \[스텝 n+2\]를 참조합니다. 
* \[스텝 n+2\]의 보간 방법이 원호보간 C이면, \[스텝 n\] \[스텝 n+1\] \[스텝 n+2\]로 원을 결정하고 그 중에서 \[스텝 n\] ~ \[스텝 n+1\] 구간의 호를 따라 이동합니다. 
* \[스텝 n+2\]의 보간 방법이 원호보간이 아니면, 이전 스텝 \[스텝 n-1\]을 참조하여 \[스텝 n-1\]\[스텝 n\]\[스텝 n+1\]로 원을 결정하고 그 중에서 \[스텝 n\] ~ \[스텝 n+1\] 구간의 호를 따라 이동합니다.

![그림 17 C-원호보간 예1](../../../_assets/image_96.png)

원의 결정에 필요한 3점 선정 기준을 이용하면 연속원호의 경우에도 동일점 이중등록을 이용하여 프로그램을 작성할 수 있습니다.

이와 같이 이동할 경로를 고려하여 스텝의 보간 방법을 결정하고 동일점 이중등록을 이용하면 원하는 대로 프로그램을 작성할 수 있습니다.

![그림 18 C-원호 보간 예2](../../../_assets/image_101.png)

#### 

#### 정치툴 보간

로봇이 작업물을 소유하고, 외부의 고정된 툴을 이용하여 작업하는 경우에 사용합니다. 이 경우에 보간 동작은 로봇이 소유하고 있는 작업물을 기준으로 이루어집니다.  정치툴 보간의 종류에 대한 자세한 내용은 “[7.3.6.2 정치툴 좌표계](../../../setting/control-parameter/cordsys-reg/stationary-tool-crdsys.md)”를 참조하십시오.

# 2.3.1.2 포즈

포즈는 위치를 기록하는 인수입니다. \[명령입력\] 버튼을 이용하여 이동 명령 move를 입력한 경우는 tg\(target\) 인수에 포즈식을 지정해야 합니다. \[기록\] 버튼을 이용해 move문을 입력한 경우에는 tg 인수가 나타나지 않습니다. \[기록\] 버튼을 터치하는 순간의 로봇 본체의 위치와 자세가 기록되는데 JOB 편집 화면에는 표시되지 않으므로 이것을 숨은 포즈라고 합니다.

Hi6 티치 펜던트 화면 우측의 메뉴 버튼을 이용하여 포즈를 입력하는 방법은 다음과 같습니다.

* \[명령입력\] 버튼을 터치한 후 \[MOTION\]을 선택하고 명령문 입력하십시오.

![](../../../_assets/image_49.png)

* \[속성\] 버튼을 터치한 후 현재의 로봇 포즈 속성을 설정하고 \[확인\] 버튼 터치하십시오.

![](../../../_assets/image_42.png)

포즈 변수와 쉬프트 변수는 다음의 형식으로 저장됩니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">포즈 변수</th>
      <th style="text-align:left">쉬프트 변수</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">(X, Y, Z, Rx, Ry, Rz, {좌표계}, {config.})</td>
      <td style="text-align:left">(X, Y, Z, Rx, Ry, Rz, {좌표계})</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>{좌표계}:
          <br />&quot;base&quot; = 베이스 좌표계
          <br
          />
        </p>
        <p>&quot;robot&quot; = 로봇 좌표계
          <br />
        </p>
        <p>&quot;user{n}&quot; = 사용자 좌표계(n은
          번호)
          <br />
        </p>
        <p>&quot;joint&quot; = 축 좌표계
          <br />
        </p>
        <p>&quot;encoder&quot;= 엔코더</p>
      </td>
      <td style="text-align:left">
        <p>{좌표계}:</p>
        <p>&quot;base&quot; = 베이스 좌표계
          <br
          />
        </p>
        <p>&quot;robot&quot; = 로봇 좌표계
          <br />
        </p>
        <p>&quot;user{n}&quot; = 사용자 좌표계(n은
          번호)
          <br />
        </p>
        <p>&quot;joint&quot; = 축 좌표계</p>
      </td>
    </tr>
  </tbody>
</table>

# 2.3.1.3 속도

로봇의 운전 속도는 다음 4 종의 단위를 사용하여 표시합니다. 모든 보간 방법에서 사용할 수 있습니다.

* ㎜/sec, ㎝/min: 로봇의 툴 끝\(TCP, Tool Center Point\)의 최고 속도를 설정합니다. 로봇의 최고 속도는 위치, 가감속 파라미터 등에 따라 제어기에서 자동으로 계산됩니다. 설정값이 로봇 성능의 최고 속도 한계보다 클 경우, 로봇은 최고 속도 한계로만 동작합니다.  
* sec: 로봇의 이동 시간을 설정합니다. 로봇의 최단 이동 시간은 위치, 가감속 파라미터 등에 따라 제어기에서 자동으로 계산됩니다. 설정값이 로봇 성능의 최단 시간 한계보다 짧을 경우, 로봇은 최단 시간 한계로만 동작합니다.  
* %: 로봇이 낼 수 있는 최고 속도에 대한 로봇의 이동 속도의 비율을 설정합니다. 100%로 설정하면 로봇이 허용 범위 내의 최고 속도로 동작합니다.



# 2.3.1.4 Accuracy

로봇이 목표 스텝을 진행할 때 그 스텝을 통과하는 정밀도\(기록 위치에 대한 접근 정도\)를 결정합니다. 로봇이 목표 스텝으로 이동할 때 발생하는 현재 위치와 기록 위치의 오차가 일정 수치보다 작으면 다음 스텝으로 이동합니다. 이때의 허용 오차값이 Accuracy입니다.

Accuracy에 의해 새롭게 만들어진 Accuracy 범위\(0 ~ 7\) 내에 있는 경로를 코너링 경로라고 합니다. 일반적으로 Accuracy가 클수록 코너링 속도가 빨라지므로 이동 시간 측면에서 유리합니다.

![그림 19 Accuracy에 따른 P2의 경로 변화](../../../_assets/image_53.png)

Accuracy 0이 가장 정밀하고 Accuracy 7은 오차가 가장 큽니다. Accuracy는 목표 스텝 양쪽 궤적 중 짧은 궤적 길이의 1/2보다는 크게 적용되지 않습니다. 즉, 위의 예에서 “Accuracy ≤ min\(P1-P2, P2-P3\) / 2” 수식을 적용할 수 있습니다. 이 수식에서는 TCP 거리로 설명하였으나 각도에서도 동일한 개념을 적용할 수 있습니다.

Accuracy level의 적용 값은 로봇의 경우에는 로봇의 툴 끝 거리 및 자세 각도로, 부가축의 경우에는 직동축은 길이, 회전축은 각도로 정의되며, 이 값은 \[설정 &gt; 3: 로봇 파라미터 &gt; 6: Accuracy\] 메뉴에서 직접 변경할 수 있습니다. Accuracy level의 적용 값에 대한 자세한 내용은 “[7.4.6 Accuracy](../../../setting/robot-parameter/accuracy.md)”를 참조하십시오.

다음의 그림은 Accuracy level 값에 따라 코너링 경로가 어떻게 생성되는지 나타냅니다. 일반적인 6축 다관절 로봇과 부가축이 있는 경우 Accuracy 값은 TCP \(툴 끝 거리\), ORN \(자세 각도\), AUX \(부가축 거리\)를 개별적으로 설정할 수 있습니다. 해당 Accuracy level 값을 모두 만족시켜야 하므로 TCP, ORN, AUX 중 가장 작은 값을 기준으로 코너링 경로를 생성합니다. 코너링 경로는 항상 Convex hull property를 만족하면서 속도 변화에 무관하게 일정한 곡선으로 생성됩니다. 다만, 서보지연에 의해 저속과 고속에서는 수 밀리미터\(㎜\)의 오차가 발생할 수 있습니다.

![그림 20 Accuracy level 값에 따른 코너링 경로 생성](../../../_assets/image_79.png)

{% hint style="info" %}
Accuracy level 값에 따른 코너링 경로 생성 방식은 모든 보간 종류에서 동일하게 적용됩니다. P 보간인 경우에는 TCP 거리 Accuracy가 적용되지만 오차가 발생할 수 있습니다.
{% endhint %}

코너링 경로는 Convex hull property에 의해 다음의 convex polygon 영역을 벗어나지 않습니다.

![그림 21 Convex polygon 영역 내의 코너링 경로의 모든 점](../../../_assets/image_87.png)

# 2.3.1.5 툴 번호

로봇 위치는 툴 끝의 위치와 자세로 결정됩니다. 사용하는 툴의 번호\(0 ~ 31\)를 지정합니다.

# 2.3.1.6 정지 조건

until 다음의 조건식을 만족하면 로봇은 이동을 정지하고 다음 명령\(스텝 또는 펑션\)을 수행합니다.

until 다음의 조건식의 값은 result\(\) 함수의 리턴값을 통해 확인할 수 있습니다. move 동작이 조건식에 의해 종료되었는지 확인할 수 있습니다.

![그림 22 정지 조건의 예](../../../_assets/image_46_1.png)

{% hint style="info" %}
로봇 언어에 대한 자세한 내용은 별도의 "[로봇 언어 기능 설명서](https://hrbook-asoe72.web.app/#/view/doc-hrscript/korean/README)"를 참조하십시오.
{% endhint %}
# 2.3.1.7 주석

스텝에 대한 설명을 주석으로 입력합니다. 주석 내용은 소프트 키보드를 이용해 편리하게 입력할 수 있습니다.

# 2.3.2 스텝 위치 기록 및 변경

\[기록\] 버튼을 이용해 기록된 스텝의 로봇 위치 및 자세를 기록하거나 변경합니다.

# 2.3.2.1 축 좌표 기록 좌표

수동 모드에서 \[설정 &gt; 1: 사용자 환경\] 메뉴의 \[1: POSE 기록 형태\] 옵션이 축 좌표로 설정된 경우, move 명령문에서 \[속성\] 버튼을 터치하십시오. 다음의 속성창이 나타납니다. 엔코더로 기록된 로봇의 자세는 위치만 확인할 수 있고 위치 데이터는 수정할 수 없습니다.

![](../../../_assets/image_94.png)

# 2.3.2.2 베이스 및 로봇 기록 좌표

로봇의 위치와 자세는 좌표계에 따라 다르게 나타낼 수 있습니다. 주행 축이 없는 경우, 일반적으로 베이스 좌표와 로봇 좌표가 동일합니다. 주행 축이 정의된 경우, 로봇 툴의 위치와 자세는 베이스 좌표와 로봇 좌표에 따라 다르게 나타납니다.

수동 모드에서 \[설정 &gt; 1: 사용자 환경\] 메뉴의 \[1: POSE 기록 형태\] 옵션이 베이스 또는 로봇으로 설정된 경우, move 명령문에서 \[속성\] 버튼을 터치하십시오. 속성창에서 로봇 툴의 위치와 자세를 확인할 수 있습니다.

{% hint style="info" %}
Pose 기록 형태를 변경하려면 고객지원팀에 문의하여 전문가에게 의뢰하거나 엔지니어에게 문의하십시오.
{% endhint %}

하나의 툴 끝 위치 및 방향에 대해서, 기구의 특성상 여러 자세가 있을 수 있으므로, 하나의 자세로 정의하려면 로봇 형태\(config.\)를 지정해야 합니다.

협동로봇의 경우, 기구학적 구조에 의해 소프트 리밋에 제한될 수 있습니다. 로봇이 동작하지 않을 때 소프트 리밋을 해제하거나 큰 값으로 설정하여 사용할 수 있습니다.

* auto \(자동\): 현재 로봇이 취하고 있는 자세에 대하여 이후의 항목들을 설정하지 않고 자동으로 결정합니다. 지정하지 않으면 아래의 항목들의 지정여부로 결정합니다.
* back \(뒤쪽\): 로봇의 툴 끝이 로봇 좌표계의 X축-방향인 뒤쪽입니다. 지정하지 않으면 + 방향인 앞쪽입니다.
* down \(하\): H축과 V축의 관계입니다. 지정하면 하, 지정하지 않으면 상입니다.

![그림 23 H축과 V축 자세: 상\(좌\), 하\(우\)](../../../_assets/image_58_1.png)

* flip \(플립\): B축의 좌표가 + 값인 플립입니다. 지정하지 않으면 - 값인 논플립\(non-flip\)입니다. 그림의 적색 화살표는 손목축의 상부 방향을 나타냅니다.

![그림 24 Flip \(좌\) / Non-flip \(우\) 자세](../../../_assets/image_75.png)

* S \(\|S\|&gt;=180\): S축 각도의 절대값이 180도 이상입니다. 지정하지 않으면 180도 미만입니다. 
* B \(\|B\|&gt;=180\): B축 각도의 절대값이 180도 이상입니다. 지정하지 않으면 180도 미만입니다.
* R2 \(\|R2\|&gt;=180\): R2축 각도의 절대값이 180도 이상입니다. 지정하지 않으면 180도 미만입니다.
* R1 \(\|R1\|&gt;=180\): R1축 각도의 절대값이 180도 이상입니다. 지정하지 않으면 180도 미만입니다.

좌표계는 \[포즈변수\].crd로 저장되며\(예: po32.crd\) 다음의 문자열 중 하나가 지정됩니다. 공문자열이면 기본값이 joint로 인식됩니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p>베이스 좌표계 = &quot;base&quot;
          <br
          />
        </p>
        <p>로봇 좌표계 = &quot;robot&quot;
          <br />
        </p>
        <p>축 좌표계 = &quot;joint&quot;
          <br />
        </p>
        <p>엔코더 = &quot;encoder&quot;
          <br />
        </p>
        <p>사용자 좌표계 = &quot;u1&quot; ~ &quot;u10&quot;
          <br
          />
        </p>
      </td>
    </tr>
  </tbody>
</table>

# 2.4 R코드

R코드는 특정한 기능에 할당한 고유의 코드 번호입니다. 자주 사용하는 기능에 고유의 코드 번호를 지정해 두면 해당 기능을 신속하게 사용할 수 있습니다. R코드에 대한 자세한 내용은 “[8 R코드](../r-code/)”를 참조하십시오.

Hi6 티치 펜던트 화면 우측의 \[즐겨찾기\] 버튼을 터치한 후 코드 번호를 입력하고 \[확인\] 버튼을 터치하십시오. 미리 지정된 기능이 실행됩니다.

![](../_assets/image_98.png)

# 2.5 에러 정보

문제가 발생하면 Hi6 티치 펜던트 화면 하단의 이력 표시줄에 알림이 나타나 약 1분 동안 깜빡입니다. 에러 코드와 알림 메시지, 에러 발생 시점을 확인할 수 있습니다.

![](../../_assets/image_89.png)

# 2.5.1 에러 유형

로봇 시스템의 문제\(trouble\)에는 에러와 경고가 있습니다.

* 에러\(error\): 로봇 동작을 멈춰야 할 만큼 중대한 문제로, 알림 메시지의 코드 번호는 E로 시작합니다.

![](../../_assets/image_91.png)

* 경고\(warning\): 로봇 동작은 계속되지만 대응 조치 수행 여부를 확인해야 하는 문제로, 알림 메시지의 코드 번호는 W로 시작합니다.

![](../../_assets/image_102.png)



# 2.5.2 에러 처리

시스템 고장이나 조작 오류 등 다양한 시스템 문제를 확인하고 처리하는 방법은 다음과 같습니다.

* 이력 표시줄의 알림을 확인하십시오. 에러 코드와 알림 메시지, 에러 발생 시점이 나타납니다.

![](../../_assets/image_89.png)

* 이력 표시줄에서 알림을 터치하십시오. 에러 및 경고 이력이 새 창으로 나타납니다.
  * 작업 패널 스택 우측 상단의 \[+\] 버튼을 터치한 후 \[이력\]을 선택해도 에러 및 경고 이력창을 열 수 있습니다.
  * 
    에러 및 경고 이력은 시간순으로 정렬되어 나타나고 가장 최근에 발생한 문제는 하이라이트됩니다.

![](../../_assets/image_74.png)

* Hi6 티치 펜던트 화면 좌측의 \[도움말\] 버튼을 터치하십시오. 에러 코드와 알림 메시지, 문제의 원인과 조치 방법을 확인할 수 있습니다.

![](../../_assets/image_90.png)





# 2.6 사용자 키

Hi6 티치 펜던트 화면 우측의 사용자키 영역의 버튼에 원하는 기능을 할당하여 로봇 티칭 시 편리하게 사용할 수 있습니다.

# 2.6.1 사용자키 영역 전환

원하는 영역이 나타날 때까지 Hi6 티치 펜던트 화면 우측의 \[사용자키\] 버튼을 터치하십시오. 메뉴 버튼 영역이 사용자키 영역으로 전환됩니다. 사용자키 영역에는 키 신호 출력 기능과 스폿 응용 기능이 기본으로 할당되어 제공됩니다.

![그림 25 사용자키 영역 전환](../../_assets/image_66.png)

* &lt;shift&gt; 키를 누른 상태에서 \[사용자키\] 버튼을 터치하면 반대 방향으로 영역을 전환할 수 있습니다.
* 사용자키 영역에는 키 신호 출력 기능과 스폿 응용 기능이 기본으로 할당되어 있습니다.
  * 키 신호 출력 기능 영역은 버튼이 등록되지 않은 초기 상태로 비어 있습니다.
  * 스폿 응용 기능 영역에는 버튼이 등록되어 로봇 티칭 시 사용할 수 있습니다.

# 2.6.2 영역별 버튼 등록

사용자키 영역에 원하는 기능을 버튼으로 등록합니다. 등록할 수 있는 기능은 최대 8개입니다.



# 2.6.2.1 키 신호 출력 기능 영역

원하는 출력 신호를 버튼으로 등록하여 간단히 ON/OFF 할 수 있습니다.

1.	키 신호 출력 기능 영역이 나타날 때까지 \[사용자키\] 버튼을 반복해서 터치하십시오.

2.	&lt;ctrl&gt; 키를 누른 상태에서 \[사용자키\] 버튼을 터치하십시오. 키 신호 출력 설정창이 나타납니다.

3.	버튼에 표시할 기능 이름과 옵션을 설정한 후 \[확인\] 버튼을 터치하십시오.

![](../../../_assets/image_84.png)

* \[제목\]: 버튼에 표시할 기능 이름입니다.
* \[on 변수\]: 신호 출력 변수 또는 숫자형 변수의 이름입니다. 버튼을 ON할 때 값을 ON \(1 대입\)할 변수의 이름입니다.
* \[off 변수\]: 신호 출력 변수 또는 숫자형 변수의 이름입니다. 버튼을 OFF할 때 값을 ON \(1 대입\)할 변수의 이름입니다.
* \[토글\]: 버튼을 터치할 때마다 버튼에 등록한 기능이 활성화 또는 비활성화되도록 설정합니다. 토글 기능을 사용하지 않으면 버튼을 터치하고 있는 동안에만 버튼에 등록한 기능이 활성화됩니다.
* \[자동 모드시 허용\]: 자동 모드에서도 변수값 출력 기능을 허용합니다.
* \[자동 모드시 OFF\]: 자동 모드에서 모든 변수값을 OFF \(0 대입\)합니다.

{% hint style="info" %}
\[fb\] 버튼과 \[do\] 버튼을 이용하면 숫자와 소수점만으로 신호 출력 변수값을 간단히 입력할 수 있습니다. 예를 들어, 2.9를 입력하고 &lt;enter&gt; 키를 누르십시오. fb2.do9로 변환되어 나타납니다. 소수점 없이 9를 입력하면 &lt;enter&gt; 키를 누르면 do9로 변환됩니다.
{% endhint %}

4.	키 신호 출력 기능 영역에서 버튼을 확인하고 각 버튼을 터치하여 설정값이 제대로 적용되는지 확인하십시오.

![](../../../_assets/image_100.png)

{% hint style="info" %}
\[설정 &gt; 제어 파라미터 &gt; 입출력 신호 설정 &gt; 키 신호 출력\] 메뉴에서도 원하는 출력 신호를 키 신호 출력 기능 영역의 버튼에 할당할 수 있습니다. 자세한 내용은 “7.3.2.8 키 신호 출력”를 참조하세요.
{% endhint %}



# 2.6.2.2 스폿 응용 기능 영역

스폿 응용 기능에 대한 자세한 내용은 별도의 “Hi6 제어기 스폿용접 기능 설명서”를 참조하십시오.

# 2.7 좌표계

로봇의 이동 방향을 결정하기 위해 공간상의 좌표를 사용합니다. Hi6 제어기에는 축 좌표계, 로봇 좌표계, 사용자 좌표계, 툴 좌표계가 있습니다.

* 축\(Joint\) 좌표계: 축 이름 우측의 \[-/+\] 버튼을 터치하면 해당하는 축을 움직일 수 있습니다. 오른쪽 버튼은 + 방향, 왼쪽 버튼은 - 방향입니다. 예를 들어, 첫 번째 축을 축 좌표계로 움직일 경우 &lt;esc&gt; 키는 + 방향, &lt;enter&gt; 키는 - 방향이고, 두 번째 축을 움직일 경우 &lt;→&gt; 키는 + 방향, &lt;←&gt; 키는 - 방향입니다.
* 로봇\(Robot\)/사용자\(User\)/툴\(Tool\) 좌표계: 각 좌표계를 기준으로 로봇의 툴 끝\(TCP, Tool Center Point\)을 이동 및 회전할 수 있습니다.



# 2.7.1 조그키

수동 모드에서 사용합니다. 모터가 켜진 상태에서 인에이블링 스위치를 잡고 있는 동안 티치 펜던트의 &lt;enter&gt;, &lt;esc&gt; 및 &lt;←/→&gt; 키와 숫자키는 ‘조그키’로 동작합니다.

![그림 26 티치 펜던트의 조그키](../../_assets/image_95.png)

* 각 키에 지정된 축의 이름은 디스플레이의 우측 가장자리의 조그 막대에 표시됩니다.
* 조작키의 우측 키는 증가\(+\), 좌측 키는 감소\(-\) 방향입니다.

조그 시 선택된 메커니즘이 메커니즘\[0\] 로봇인 경우에 한하여 다음 메커니즘\[1\]의 전체 축 개수가 2축 이하이면 등록된 부가축의 순서에 따라 각각 할당됩니다. 이때 메커니즘\[1\]에서 할당되지 않은 키가 남아 있고 그 다음 메커니즘이 잔여 키에 할당 가능한 축 개수 이내로 되어 있는 경우 순차적으로 할당됩니다.

예를 들어, 부가축 메커니즘의 축 개수에 따른 J7, J8축에 대한 할당 여부는 다음과 같습니다.

| 메커니즘\[0\] | 메커니즘\[1\] | 메커니즘\[2\] | J7축 / J8축 할당 여부 |
| :--- | :--- | :--- | :--- |
| 6축 로봇 | 주행축1 축 | 포지셔너 1축 | J7: 주행축 / J8: 포지셔너 |
| 6축 로봇 | 주행축1 축 | 포지셔너 2축 | J7: 주행축 / J8: 미할당 |
| 6축 로봇 | 주행축2 축 | 포지셔너 2축 | J7: 주행축 1 / J8: 주행축 2 |
| 6축 로봇 | 주행축3 축 | 포지셔너 1축 | J7: 미할당 / J8: 미할당 |

# 2.7.2 축 좌표계

| **축 좌표계** | 로봇 좌표계 | 사용자 좌표계 | 툴 좌표계 |
| :---: | :---: | :---: | :---: |
|  ![](../../_assets/bt-crd2-joint.png)  | ![](../../_assets/bt-crd2-robot.png)  | ![](../../_assets/bt-crd2-user.png)  | ![](../../_assets/bt-crd2-tool.png)  |

1.	수동 모드에서 모터를 켜고 티치 펜던트 뒷면의 인에이블링 스위치를 잡으십시오.

2.	Hi6 티치 펜던트 화면 우측의 \[좌표계\] 버튼을 반복해서 터치하여 축 좌표계를 선택하십시오. 조그 막대에 각 축의 이름이 표시됩니다.

3.	조그키로 로봇을 동작하십시오. 로봇의 각 축이 독립적으로 움직입니다.

![](../../_assets/image_85.png)

{% hint style="info" %}
조그키에 대한 로봇의 진행 방향에 대한 자세한 내용은 “[2.7.1 조그키](jog-key.md)”를 참조하십시오.
{% endhint %}

# 2.7.3 로봇 좌표계

| 축 좌표계 | **로봇 좌표계** | 사용자 좌표계 | 툴 좌표계 |
| :---: | :---: | :---: | :---: |
|  ![](../../_assets/bt-crd2-joint.png)  | ![](../../_assets/bt-crd2-robot.png)  | ![](../../_assets/bt-crd2-user.png)  | ![](../../_assets/bt-crd2-tool.png)  |

1.	수동 모드에서 모터를 켜고 티치 펜던트 뒷면의 인에이블링 스위치를 잡으십시오.

2.	Hi6 티치 펜던트 화면 우측의 \[좌표계\] 버튼을 반복해서 터치하여 로봇 좌표계를 선택하십시오. 조그 막대에 X, Y, Z, RX, RY, RZ와 부가축이 표시됩니다.

3.	조그키로 로봇을 동작하십시오. 로봇이 다음과 같이 움직입니다.

![](../../_assets/image_62.png)

{% hint style="info" %}
* 조그키에 대한 로봇의 진행 방향에 대한 자세한 내용은 “[2.7.1 조그키](jog-key.md)”를 참조하십시오.
* 오른손을 이용하면 로봇 좌표계에서 로봇의 동작을 쉽게 이해할 수 있습니다.

![](../../_assets/crd-direction.png) 

그림 27 좌표계 방향\(좌\) / 회전 방향\(우\)

* 로봇 뒷면에서 오른손 검지 손가락의 진행 방향을 로봇 좌표계의 X방향으로 두면, 엄지 손가락의 진행 방향이 Z방향, 중지 손가락의 진행 방향이 Y방향이 됩니다.
* 오른손 엄지 손가락을 회전 중심축 방향으로 두면, 나머지 손가락을 접은 방향이 회전 방향의 + 방향입니다.
{% endhint %}



# 2.7.4 사용자 좌표계

| 축 좌표계 | 로봇 좌표계 | **사용자 좌표계** | 툴 좌표계 |
| :---: | :---: | :---: | :---: |
|  ![](../../_assets/bt-crd2-joint.png)  | ![](../../_assets/bt-crd2-robot.png)  | ![](../../_assets/bt-crd2-user.png)  | ![](../../_assets/bt-crd2-tool.png)  |

1.	초기 화면 우측의 \[설정\] 버튼 &gt; \[2: 제어 파라미터 &gt; 7: 좌표계 등록 &gt; 1: 사용자 좌표계\] 메뉴를 터치한 후 사용자 좌표계를 등록하십시오.

{% hint style="info" %}
사용자 좌표계 등록 방법에 대한 자세한 내용은 “[7.3.6.1 사용자 좌표계](../../setting/control-parameter/cordsys-reg/user-crdsys.md)”를 참조하십시오.
{% endhint %}

2.	초기 화면 좌측 상단의 \[속도조절\] 버튼을 터치한 후 \[9: 사용자 좌표계 지정\] 옵션에 좌표계를 설정하십시오. 직교 좌표계 대신 사용자 좌표계를 선택할 수 있습니다.

![](../../_assets/image_54.png)

3.	조그키로 로봇을 동작하십시오. 로봇이 다음과 같이 움직입니다.

![](../../_assets/image_103.png)

{% hint style="info" %}
조그키에 대한 로봇의 진행 방향에 대한 자세한 내용은 “[2.7.1 조그키](jog-key.md)”를 참조하십시오.
{% endhint %}

# 2.7.5 툴 좌표계

| 축 좌표계 | 로봇 좌표계 | 사용자 좌표계 | **툴 좌표계** |
| :---: | :---: | :---: | :---: |
|  ![](../../_assets/bt-crd2-joint.png)  | ![](../../_assets/bt-crd2-robot.png)  | ![](../../_assets/bt-crd2-user.png)  | ![](../../_assets/bt-crd2-tool.png) |

1.	수동 모드에서 모터를 켜고 티치 펜던트 뒷면의 인에이블링 스위치를 잡으십시오.

2.	Hi6 티치 펜던트 화면 우측의 \[좌표계\] 버튼을 반복해서 터치하여 툴 좌표계를 선택하십시오. 조그 막대에 X, Y, Z, RX, RY, RZ와 부가축이 표시됩니다.

3.	조그키로 로봇을 동작하십시오. 로봇이 다음과 같이 움직입니다.



* 로봇에 토치를 부착한 경우

![](../../_assets/image_68.png)



* 로봇에 토치를 부착하지 않은 경우

![](../../_assets/image_92.png)

{% hint style="info" %}
조그키에 대한 로봇의 진행 방향에 대한 자세한 내용은 “[2.7.1 조그키](jog-key.md)”를 참조하십시오.
{% endhint %}

# 2.8 축 원점 및 툴 길이 최적화 설정

직선보간 궤적 및 좌표변환 정도의 향상을 위해 축 정수와 툴 길이를 자동으로 설정합니다.

* 3차원상에서 측정하기 어려운 툴 끝까지의 거리를 자동으로 설정할 수 있습니다. 보정되는 파라미터는 H, V, R2, B축의 축 원점과 X, Y, Z방향 툴 길이입니다.
* ‘축 원점 및 툴 길이’와 ‘툴 길이’ 최적화를 실행할 수 있습니다.

{% hint style="warning" %}
로봇 프로그램을 티칭하기 전에 ‘축 원점 및 툴 길이’를 최적화하십시오. 로봇 프로그램이 만들어진 상태에서 ‘축 원점 및 툴 길이’를 최적화하면 기존 프로그램의 위치가 변경될 수 있습니다.
{% endhint %}

축 원점 및 툴 길이 최적화를 설정하는 방법은 다음과 같습니다.

1.	티치 펜던트의 모드 스위치를 이용해 운전 방식을 수동 모드로 설정하십시오.

2.	JOB 프로그램창에서 \[프로그램\] 버튼을 터치한 후 프로그램 번호를 입력하고 \[확인\] 버튼을 터치하십시오.

![](../_assets/image_55.png)

3.	티치 펜던트의 &lt;모터&gt; 키를 누르십시오. 모터 램프가 깜빡입니다.

* 모터가 켜지지 않으면 이력 표시줄에서 에러 메시지를 확인하고 문제를 해결하십시오.

4.	티치 펜던트 뒷면의 인에이블링 스위치를 잡은 채로 조그키를 이용해 로봇을 동작하십시오

5.	로봇의 동작 범위 내 임의의 위치에 뾰족한 침을 두고 로봇의 툴 끝을 침에 일치시키십시오. 로봇 선단부터 일치시킨 툴 끝까지의 길이가 최적화됩니다.

6.	Hi6 티치 펜던트 화면 우측의 \[기록\] 버튼을 터치하여 스텝을 기록하십시오.



![](../_assets/image_105.png)

7.	로봇의 자세를 바꾸고 5 ~ 6번 단계를 4번 이상 반복하십시오.

* 가능한 한 6축 전체를 이용하여 로봇의 자세를 바꾸십시오. 또한 축의 각도는 30 deg 이상 변경하십시오.

8.	\[설정\] 버튼 &gt; \[6: 자동 캘리브레이션 &gt; 1: 축 원점 및 툴 길이 최적화\] 메뉴를 터치하십시오.

![](../_assets/image_52.png)

9.	자동 캘리브레이션용으로 작성한 프로그램 번호, 툴 번호, 스텝 위치 오차 허용 범위를 설정한 후 \[실행\] 버튼을 터치하십시오. 선택된 축 원점 및 툴 길이가 설정됩니다.

![](../_assets/image_319.png)

* 여러 개의 툴을 사용할 때, 두 번째 툴의 자동 캘리브레이션부터는 \[최적화 선택\] 옵션을 툴 길이로 선택하여 실행하십시오. 축 원점 및 툴 길이를 선택하면 먼저 설정한 툴의 정보가 맞지 않게 됩니다.

{% hint style="info" %}
이 기능에 대한 자세한 내용은 “[7.7.1 축 원점 및 툴 길이 최적화](../setting/auto-calibration/axis-origin-tool-length-optimization.md)”를 참조하십시오.
{% endhint %}

# 2.9 툴 데이터 자동 보정

자동 캘리브레이션 기능 등을 이용해 축 원점 및 툴 길이를 결정한 후 툴이 변형되었을 때 간단히 새로운 툴 데이터를 결정할 수 있습니다. 이때, 축 원점\(Axis origin\)은 결정되어 있어야 하고 계속 유지되어야 합니다. 또한 툴 길이를 결정하고 각도 보정을 완료한 후 고정된 기준점을 티칭해 두어야 합니다. 툴 변형이 발생하면 툴을 변경 전에 지정해 둔 기준점에 동일한 자세로 위치시킨 후 툴 데이터 자동 보정을 실행하십시오.

1.	\[설정\] 버튼 &gt; \[3: 로봇 파라미터 &gt; 1: 툴 데이터\] 메뉴를 터치하십시오.

![](../_assets/image_97.png)

2.	\[자동보정\] 버튼을 터치한 후 조그키를 이용하여 툴 끝을 원래의 위치로 이동하십시오.

![](../_assets/image_83.png)

3.	미리 결정해 둔 기준점의 프로그램 번호, 스텝 번호, 설정할 툴 번호를 확인한 후 \[실행\] 버튼을 터치하십시오.

![](../_assets/image_107.png)

{% hint style="info" %}
이 기능에 대한 자세한 내용은 “[7.4.1 툴 데이터](../setting/robot-parameter/tool-data/)”를 참조하십시오.
{% endhint %}

# 3. 프로그램 작성

로봇이 작업을 수행하여 원하는 결과를 얻을 수 있도록 프로그램을 작성하고 관리할 수 있습니다.

# 3.1 프로그램 관리

로봇이 정지된 상태에서, 프로그램을 생성, 수정 및 삭제할 수 있습니다.

1.	JOB 프로그램창에서 \[프로그램\] 버튼을 터치하십시오. 프로그램 선택창이 나타납니다.

![](../_assets/image_61.png)

2.	프로그램을 생성, 수정 및 삭제하십시오.

* 새 프로그램을 추가하려면, \[+\] 버튼을 터치한 후 “3.2 프로그램 작성”을 참조하여 내용을 입력하십시오.

![](../_assets/image_70.png)

* 프로그램을 열어 내용을 확인하고 수정하려면, 프로그램 번호를 입력하거나 목록에서 프로그램을 선택한 후 \[확인\] 버튼을 터치하십시오. 선택한 프로그램이 JOB 프로그램창에서 열립니다.

![](../_assets/image_99.png)

* 프로그램을 삭제하려면, 목록에서 프로그램을 선택한 후 \[-\] 버튼을 터치하십시오.

![](../_assets/image_104.png)

* 파일 목록\(\[메뉴 &gt; 5: 파일관리\]\)에서 프로그램을 삭제할 수 있습니다. 자세한 내용은 “[4.2 파일 관리](../menu/file-manager/file-management.md)”를 참조하십시오.
* R코드\(R117\)를 이용하여 프로그램을 빠르게 삭제할 수 있습니다. 자세한 내용은 “[8.4 R117 프로그램 삭제](../r-code/r117.md)”를 참조하십시오.



# 3.2    프로그램 작성

원하는 결과를 얻기 위해 로봇의 동작을 지시하는 다양한 명령문으로 구성된 프로그램을 작성하고 편집합니다. 프로그램은 수동 모드에서 작성할 수 있습니다.



# 3.2.1 명령문

일반적인 프로그램은 로봇의 이동을 지시하는 스텝 명령문과 이동 후 작업을 지시하는 펑션 명령문으로 구성됩니다.

명령문은 크게 명령어와 부가 항목인 인수\(Parameter\)로 나뉘며 인수에는 명령문에 반드시 필요한 기본 인수와 생략 가능한 선택 인수가 있습니다.

![](../../_assets/image_82.png)

| 번호 | 설명 | 번호 | 설명 |
| :--- | :--- | :--- | :--- |
| ![](../../_assets/c1.png) | 스텝 번호 | ![](../../_assets/c3.png) | 인수 |
| ![](../../_assets/c2.png) | 명령어 | ![](../../_assets/c4.png) | 주석 |

{% hint style="info" %}
인수에 대한 자세한 내용은 “[2.3.1 스텝 명령문 인수](../../operation/step/step-cmd-param/)”를 참조하십시오.
{% endhint %}

명령문을 입력하면 기본 인수에는 기본 설정값이 자동으로 입력되며 변경할 수 있습니다. 선택 인수는 기호\( \_ \)로 표시되며 이곳을 선택하면 인수값을 입력할 수 있습니다. 인수에 따라 화면 우측에 입력 가능한 인수가 버튼으로 나타납니다.

![그림 28 명령문 편집 - 인수값 입력](../../_assets/image_76.png)

명령어 인수를 편집할 때는 티치 펜던트의 조작키와 화면 우측의 메뉴 버튼을 이용하거나 소프트 키보드를 이용하여 변수나 수식, 문자열을 편집할 수 있습니다.

# 3.2.2 명령문 입력

# 3.2.2.1 일반 명령문 입력

1.	수동 모드에서 초기 화면 우측의 \[명령입력\] 버튼을 터치하십시오. 명령 입력창이 나타납니다.

2.	명령문 그룹을 터치하거나 명령어를 입력한 후 목록에서 명령어를 선택하십시오. 현재 커서 위치의 바로 아래에 명령문이 입력됩니다.

![](../../../_assets/image_47_1.png)

* 여러 개의 인수 형태를 가진 명령어의 경우, 우측에 체크 표시\( V \)가 나타납니다. 목록에서 명령어를 터치하면 인수 형태를 확인하고 선택할 수 있습니다.
* 각 명령문에 대한 자세한 내용은 별도의 “[Hi6 로봇언어 기능 설명서](https://hyundai-robotics.gitbook.io/hi6-robot-language/)”를 참조하십시오.



# 3.2.2.2 숨은 포즈의 스텝 명령문 입력

현재 로봇이 취한 자세를 이동 명령으로 입력하려면, Hi6 티치 펜던트 화면 우측의 \[기록\] 버튼을 터치하십시오.

![](../../../_assets/image_65.png)

\[기록\] 버튼으로 명령을 입력하면 일반 명령문 입력 방식과 달리 포즈 변수가 스텝에 나타나지 않으므로 숨은 포즈라고 합니다,



# 3.2.2.3 기록 조건

\[기록\] 버튼으로 명령문을 입력하면 로봇의 현재 자세가 타겟 포즈로 기록되고 이동 명령\(move\) 인수는 \[기록조건\] 버튼으로 미리 설정한 값이 적용됩니다. 명령문의 기록 조건을 설정하는 방법은 다음과 같습니다.

1.	Hi6 티치 펜던트 화면 좌측의 \[기록조건\] 버튼을 터치하십시오. 기록 조건 설정창이 나타납니다.



![](../../../_assets/image_56.png)

 2.	보간, 이동 속도와 단위, 정밀도, 툴 번호, 메커니즘 세트를 설정한 후 \[확인\] 버튼\( \)을 터치하십시오.

![](../../../_assets/image_71.png)

* 위치 기록 시, 기록 조건에 설정한 조건을 기준으로 이동 명령문이 기록됩니다.
* 메커니즘 세트에서는 위치 기록 시 저장할 메커니즘의 구성을 지정합니다.
  * \[메커니즘 세트\] 버튼을 짧게 터치하면, 사전에 정의된 메커니즘 세트 번호가 순차적으로 나타납니다.
  * \[메커니즘 세트\] 버튼을 길게 터치하면, 메커니즘 세트 설정창에서 기존의 세트 구성을 수정하거나 \[+\] 또는 \[-\] 버튼을 이용하여 메커니즘 세트를 추가 및 삭제할 수 있습니다.

![](../../../_assets/image_60.png)





# 3.2.3 명령문 구성

명령문은 주소 영역과 명령문 영역으로 구성됩니다.

![그림 29 명령문의 구성 영역](../../_assets/image_106.png)

| 번호 | 영역 | 설명 |
| :--- | :--- | :--- |
| ![](../../_assets/c1.png) | 주소 영역 | 행 번호\(1 ~ 9999\)와 스텝 번호 \(S1 ~ S999\)가 표시됩니다. |
| ![](../../_assets/c2.png) | 명령문 영역 | 명령문이 표시됩니다. |

티치 펜던트의 &lt;←/→&gt; 키를 눌러 주소 영역과 명령문 영역 사이에서 커서의 위치를 이동할 수 있습니다. &lt;↓/↑&gt; 키를 누르면 선택된 영역 내의 행 사이에서 커서를 위아래로 이동할 수 있습니다.

![그림 30 영역 간 커서 이동\(좌: 주소 영역, 우: 명령문 영역\)](../../_assets/image_86.png)

# 3.2.4 명령문 편집

티치 펜던트의 조작키와 화면 우측의 메뉴 버튼을 이용하여 JOB 프로그램창에서 명령문을 편집합니다. 소프트 키보드를 이용하면 변수나 수식, 문자열을 편집할 수 있습니다.

명령문 영역은 선택된 대상에 따라 커서 상태를 전환하여 명령문을 확인 및 편집할 수 있습니다.

* 문장 커서 상태: 명령문의 한 행 전체가 선택 상태로 명령문을 확인할 수 있습니다. 

![](../../../_assets/image_41.png)

* 명령문 커서 상태: 명령문의 개별 인수가 선택된 상태로 명령문을 확인하고 편집할 수 있습니다.

![](../../../_assets/image_64.png)





# 3.2.4.1 명령문 편집 방법

명령문을 편집하는 방법은 다음과 같습니다.

1.	JOB 프로그램창에서 티치 펜던트의 &lt;←/→&gt; 키를 눌러 명령문 영역을 선택하십시오. 명령문 영역이 문장 커서 상태로 선택됩니다.

2.	문장 커서 상태에서 티치 펜던트의 &lt;enter&gt; 키를 누르십시오. 명령문 커서 상태가 되어 인수가 선택되고 하단의 입력 영역에 선택된 인수값이 나타납니다.


3.	티치 펜던트의 조작키와 화면 우측의 메뉴 버튼을 이용하여 인수값을 편집하십시오.

* &lt;←/→&gt; 키를 누르면 인수 사이에서 커서를 좌우로 이동할 수 있습니다.
* 인수에 따라 화면 우측에 입력 가능한 인수가 버튼으로 나타납니다. 원하는 버튼을 선택하면 간편히 인수를 입력할 수 있습니다.
* 소프트 키보드를 이용하여 변수나 수식, 문자열을 편집할 수 있습니다.

4.	&lt;enter&gt; 키를 누르십시오. 변경 내용이 적용되어 명령문의 인수값이 변경되고 커서가 다음 인수로 이동합니다.

* 변경 내용을 취소하려면, &lt;esc&gt; 키를 누르십시오.

5.	2 ~ 3번 절차를 반복하여 다른 인수를 편집하십시오.

6.	&lt;enter&gt; 키를 눌러 편집을 완료하십시오. 변경 내용이 JOB 프로그램에 저장되고 문장 커서 상태로 돌아갑니다.



# 3.2.4.2 명령문 편집 예

보간 인수를 P \(축 보간\)에서 L \(직선 보간\)로 변경하는 것을 예로 들어, 명령문을 편집하는 방법에 대해 설명합니다.

1.	문장 커서 상태에서 티치 펜던트의 &lt;enter&gt; 키를 누르십시오. 단어 커서 상태가 되어 move 문의 보간 인수인 P \(축 보간\)가 선택됩니다. 입력 영역에는 보간의 현재 설정값인 P가 표시되고 입력 가능한 보간 인수가 화면 우측에 버튼으로 나타납니다.

![](../../../_assets/image_51.png)

2.	화면 우측의 버튼 중 \[L\] 버튼을 터치하십시오. 입력 영역에 L \(직선 보간\)이 표시됩니다. 

![](../../../_assets/image_59.png)

3.	&lt;enter&gt; 키를 누르십시오. 명령문의 보간 인수가 L로 변경되고 커서가 다음 인수로 이동하여 이동 속도가 선택됩니다.

![](../../../_assets/image_69.png)

4.	&lt;enter&gt; 키를 눌러 편집을 완료하십시오. 변경 내용이 JOB 프로그램에 저장되고 문장 커서 상태로 돌아갑니다.



# 3.2.4.3 행 번호 편집 방법

행 번호는 1 ~ 9999 사이의 수로 설정할 수 있습니다.

1.	JOB 프로그램창에서 티치 펜던트의 &lt;←/→&gt; 키를 눌러 주소 영역을 선택하십시오. 주소 영역이 선택됩니다.

* 명령문 영역에서 문장 커서 상태일 경우 &lt;←&gt; 키를 누르면 커서가 주소 영역으로 이동할 수 있습니다. 

![](../../../_assets/image_108.png)

2.	주소 영역에서 &lt;↓/↑&gt; 키를 눌러 행을 선택한 후 행 번호를 편집하십시오.

* 행 번호를 입력하려면, 숫자키를 이용하여 입력 영역에 행 번호를 입력하십시오. 

![](../../../_assets/image_63.png)

* 행 번호를 삭제하려면, &lt;BS&gt; 키를 누르십시오. 입력 영역에서 행 번호의 주소값이 제거됩니다.


3.	&lt;enter&gt; 키를 눌러 편집을 완료하십시오. 변경 내용이 JOB 프로그램에 저장됩니다.
_assets
![](../../../.gitbook/assets/image_67.png)



# 3.2.4.4 소프트 키보드

Hi6 티치 펜던트 화면의 소프트 키보드를 이용하여 변수나 수식, 문자열을 편리하게 입력합니다.

1.	Hi6 티치 펜던트 화면의 이력 표시줄에서 \[![](../../../_assets/bt-softkb-off.png)\] 버튼을 터치하십시오. 화면 하단에 소프트 키보드가 나타납니다.

2.	소프트 키보드를 이용하여 입력 영역에 변수나 수식, 문자열을 입력하십시오. 기존의 인수값이 제거되고 입력한 텍스트가 표시됩니다.

![](../../../_assets/image_78.png)

* 입력 영역 좌측의 \[![](../../../_assets/bt-cursor-left.png)/![](../../../_assets/bt-cursor-right.png)\] 버튼을 터치하면, 커서의 위치를 이동하여 원하는 위치에 텍스트를 삽입할 수 있습니다.
* \[![](../../../_assets/bt-123.png)/![](../../../_assets/bt-symbol.png)\] 버튼을 터치하면 숫자와 기호 및 특수 문자를 입력할 수 있습니다.
* \[![](../../../_assets/bt-lang.png)\] 버튼을 터치하면 입력 언어를 변경할 수 있습니다.
* 티치 펜던트의 &lt;shift&gt; 키를 누른 상태에서 키를 터치하면 대문자 및 기호를 입력할 수 있습니다.
* \[![](../../../_assets/bt-dock-softkb.png)\] 버튼을 터치하면 키보드의 위치를 화면 상단으로 이동할 수 있습니다.

3.	텍스트 편집을 완료하면, 소프트 키보드 우측 하단의 \[![](../../../_assets/bt-softkb.png)\] 버튼을 터치하여 소프트 키보드를 숨기십시오.



# 3.2.4.5 블록 편집 모드

프로그램의 한 행 또는 여러 행을 블록\(Block\)으로 지정하여 복사, 이동 및 삭제합니다.

1.	티치 펜던트의 &lt;shift&gt; 키를 누른 상태에서 JOB 프로그램창 우측의 \[블록편집\] 버튼을 터치하십시오. 블록편집 모드가 활성화됩니다.

2.	티치 펜던트의 &lt;↓/↑&gt; 키로 원하는 행에 커서를 두고 &lt;enter&gt; 키를 누르십시오. 커서가 위치한 행이 블록의 시작행으로 선택됩니다. 

![](../../../_assets/image_80.png)

3.	티치 펜던트의 방향키로 커서를 이동하십시오. 시작행부터 커서를 이동시킨 행까지 블록으로 선택됩니다. 

![](../../../_assets/image_43.png)

4.	화면 우측의 기능 버튼을 이용하여 블록으로 선택한 영역의 명령문을 편집하십시오. 

![](../../../_assets/image_57.png)

* \[잘라내기\]: 블록으로 선택한 영역을 잘라내어 다른 위치에 붙여 넣을 수 있도록 클립보드에 저장합니다.  
* \[복사하기\]: 블록으로 선택한 영역을 복사하여 다른 위치에 붙여 넣을 수 있도록 클립보드에 저장합니다.  
* \[붙여넣기\]: 클립보드에 저장한 영역을 원하는 위치에 붙여 넣습니다. 클립보드에 저장된 명령문을 붙여 넣으려면, 방향키로 커서의 위치를 선택한 후 \[붙여넣기\] 버튼을 터치하십시오. 현재 커서 위치 바로 아래 행에 명령문이 입력됩니다.  
* \[삭제\]: 선택 영역을 삭제합니다.

5.	블록 편집을 완료하면, 티치 펜던트의 &lt;esc&gt; 키를 누르거나 화면 우측의 \[닫기\] 버튼을 터치하여 블록편집 모드를 종료하십시오.



# 4. 메뉴

변수 및 파일 관리 등 프로그램의 각종 서비스 기능 메뉴를 사용할 수 있습니다.

# 4.1 메뉴 사용

1.	수동 또는 자동 모드에서 초기 화면 우측의 \[메뉴\] 버튼을 터치하십시오. 프로그램의 각종 서비스 메뉴가 표시됩니다.

2.	원하는 메뉴를 선택하여 파일 및 프로그램, 티치 펜던트를 관리하거나 로봇 시스템의 상태를 확인하십시오. 

![](../_assets/image_44.png)

* \[5: 파일관리\]: 메인 보드의 내부 메모리와 티치 펜던트 및 이동식 저장 장치의 파일을 관리합니다.
* \[6: 프로그램 변환\]: 작성된 프로그램의 조건 및 위치 등을 일괄 또는 개별 변환합니다.
* \[7: 시스템 진단\]: 로봇과 제어기의 상태를 확인하고 시스템의 버전을 업데이트합니다.
* \[8: 날짜, 시간 설정\]: 제어기의 날짜와 시간을 설정합니다.



# 4.2    파일 관리

메인 보드의 내부 메모리 또는 티치 펜던트나 이동식 저장 장치의 파일을 관리합니다.

1. \[5: 파일관리\] 메뉴를 터치하십시오. 장치별 폴더 목록과 선택한 폴더에 저장된 파일의 목록이 나타납니다.
2. 장치별 폴더 구조와 저장된 파일을 확인하고 관리하십시오.

![](../../_assets/image_116.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>메인 보드의 내부 메모리,
          티치 펜던트, 이동식 저장
          장치의 폴더 목록입니다.
          폴더 구조를 확인할 수
          있습니다.</p>
        <p> [
          <img src="../../_assets/icon-mb.png" alt/>MAIN]: 메인 보드(M/B)에 저장된
          파일은 실제 로봇의 동작에
          사용됩니다.</p>
        <p> [
          <img src="../../_assets/icon-tp.png" alt/>TP] / [
          <img src="../../_assets/icon-usb.png" alt/>USB]: 티치 펜던트(T/P)와 이동식
          저장 장치(USB)는 데이터
          백업 시 사용합니다. [
          <img
          src="../../_assets/icon-usb.png" alt/>USB] 폴더는 티치 펜던트에
          이동식 저장 장치가 연결된
          경우에만 나타납니다.</p>
        <p> 티치 펜던트의 방향키로 폴더
          목록에서 커서를 이동할
          수 있습니다.</p>
        <p> 폴더 목록에서 [
          <img src="../../_assets/icon-gt.png"
          alt/>] 또는 [
          <img src="../../_assets/icon-wedge.png" alt/>]를 선택한 후 &lt;enter&gt; 키를
          누르면 하위 폴더를 표시하거나
          숨길 수 있습니다.</p>
        <p> 폴더를 선택하면 폴더에
          저장된 파일의 목록을
          확인할 수 있습니다.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">선택한 폴더에 저장된
        파일의 목록입니다. 파일별로
        이름과 크기, 최종 수정
        날짜, 보호 여부, 추가 정보를
        확인할 수 있습니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">기능 버튼을 이용해 파일과
        폴더를 관리할 수 있습니다.</td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* R코드의 “R17 파일 관리”와 동일한 기능입니다.
* 이동식 저장 장치를 티치 펜던트에 연결하면 Hi6 티치 펜던트 화면의 상태 표시줄에 \[USB\] 아이콘\(![](../../_assets/icon-usb2.png)\)이 나타납니다.
{% endhint %}

{% hint style="warning" %}
파일을 복사하거나 삭제하는 등의 동작을 수행하는 도중에 티치 펜던트에서 이동식 저장 장치를 절대 분리하지 마십시오. 데이터가 손상될 수 있습니다.
{% endhint %}

# 4.2.1 파일 관리

하나 혹은 여러 파일을 선택하여 복사, 이동 및 삭제합니다.

1.	폴더 목록에서 티치 펜던트의 방향키를 이용해 폴더를 선택하십시오. 선택한 폴더에 저장된 파일 목록이 나타납니다. 

![](../../_assets/image_133.png)

2.	파일 목록에서 원하는 파일을 터치하여 선택하십시오. 

![](../../_assets/image_135.png)

* &lt;ctrl&gt; 키를 누른 상태에서 파일을 터치하면 여러 파일을 하나씩 선택할 수 있습니다.
* &lt;shift&gt; 키를 누른 상태에서 두 파일을 터치하면 두 파일 사이의 모든 파일을 한 번에 선택할 수 있습니다.
* 화면 우측의 \[전체선택\] 버튼을 터치하면 모든 파일을 한 번에 선택할 수 있습니다.
* 파일 선택을 취소하려면 &lt;esc&gt; 키를 누르십시오.



3.	화면 우측의 기능 버튼을 이용하여 선택한 파일을 복사, 이동 및 삭제하십시오.

* \[복사\]: 선택한 파일을 복사하여 다른 폴더에 붙여 넣을 수 있도록 임시 폴더에 저장합니다.
* \[붙여넣기\]: 클립보드에 저장한 파일을 원하는 폴더에 붙여 넣습니다.
* \[잘라내기\]: 선택한 파일을 잘라내어 다른 폴더에 붙여 넣을 수 있도록 임시 폴더에 저장합니다.
* \[삭제\]: 선택한 파일을 삭제합니다. 보호 설정된 파일\(속성에 보호 표시\(W\_\)\)은 삭제할 수 없습니다.

4.	파일을 폴더에 붙여 넣기할 경우, 방향키로 폴더를 선택한 후 \[붙여넣기\] 버튼을 터치하십시오. 선택한 폴더에 파일이 붙여 넣기됩니다. 

![](../../_assets/image_129.png)

* 선택한 폴더에 같은 이름의 파일이 있으면 중복 알림창이 나타납니다. 덮어쓰기 여부를 설정하여 처리하십시오. 

![](../../_assets/image_111.png)

* 파일을 삭제할 경우, \[삭제\] 버튼을 터치한 후 확인창에서 \[확인\] 버튼을 터치하십시오.

![](../../_assets/image_115.png)

# 4.2.2 파일명 및 폴더명 변경

파일 또는 폴더의 이름을 변경합니다. 여러 파일이나 폴더의 이름을 한 번에 변경할 수도 있습니다.

1.	파일\(또는 폴더\) 목록에서 원하는 파일\(또는 폴더\)을 터치하여 선택한 후 화면 우측에서 \[이름변경\] 버튼을 터치하십시오.

_assets
![](../../.gitbook/assets/image_121.png)

2.	입력 영역에 파일\(또는 폴더\) 이름을 입력하십시오.
_assets
![](../../.gitbook/assets/image_128.png)

* 숫자는 티치 펜던트의 조작 키를 이용해 간단히 입력할 수 있습니다. \_assets 커서 이동, 숫자키: 숫자 입력\)
* 숫자를 포함한 텍스트를 입력하려면 이력 표시줄의 \[![](../../.gitbook/assets/image_110.png)\] 버튼을 터치하여 소프트 키보드를 이용하십시오.

3.	&lt;enter&gt; 키를 누르십시오. 목록에 입력한 이름으로 변경되어 나타납니다.

{% hint style="info" %}
* 보호 설정된 파일도 이름을 변경할 수 있습니다.
* 파일의 이름을 변경해도 크기, 수정 날짜, 속성 등의 정보는 기존과 동일하게 유지됩니다.
* R코드의 “R116 프로그램 번호 변경”과 동일한 기능입니다.
{% endhint %}



# 4.2.3 폴더 관리

폴더를 삭제하거나 새 폴더를 추가합니다.

# 4.2.3.1 폴더 삭제

1.	폴더 목록에서 티치 펜던트의 방향키를 이용해 폴더를 선택한 후 화면 우측의 \[삭제\] 버튼을 터치하십시오. 

![](../../../_assets/image_137.png)

2.	확인창에서 \[확인\] 버튼을 터치하십시오. 선택한 폴더와 폴더에 저장된 파일이 모두 삭제됩니다.

![](../../../_assets/image_130.png)



# 4.2.3.2 폴더 생성

1.	폴더 목록에서 티치 펜던트의 방향키를 이용해 폴더를 선택한 후 화면 우측의 \[새 폴더\] 버튼을 터치하십시오. 선택한 폴더의 하위에 새 폴더가 추가됩니다.

![](../../../_assets/image_117.png)

2.	새 폴더의 이름을 입력한 후 &lt;enter&gt; 키를 누르십시오.

![](../../../_assets/image_136.png)

# 4.2.4 파일 보호

프로그램을 변경하거나 삭제할 수 없도록 설정하여 중요한 파일을 보호합니다.

1.	파일을 선택한 후 \[속성\] 버튼을 터치하십시오. 속성 설정창이 나타납니다. 

![](../../_assets/image_125.png)

2.	파일 이름을 확인하고 \[읽기전용\] 체크박스를 터치하여 선택한 후 \[확인\] 버튼을 터치하십시오. 파일 목록의 속성에 보호 표시\(W\_\)가 나타납니다.

![](../../_assets/image_131.png)



# 4.2.5 데이터 백업

메모리 버퍼의 이력을 파일로 저장하고 프로젝트\(project/\)와 이력\(log/\) 폴더를 백업합니다.

1.	폴더 목록의 티치 펜던트\(T/P\) 또는 이동식 저장 장치\(USB\)에서 티치 펜던트의 방향키를 이용해 데이터 백업을 저장할 폴더를 선택하십시오. 

![](../../_assets/image_127.png)

2.	&lt;shift&gt; 키를 누른 상태에서 화면 우측의 \[전체 백업\] 버튼을 터치하십시오. 데이터 백업이 시작됩니다. 

![](../../_assets/image_112.png)

3.	데이터 백업\(약 30 초 소요\)이 완료되면 알림창에서 백업 결과를 확인하십시오.

![](../../_assets/image_138.png)

# 4.2.6 데이터 복원

백업 프로젝트\(project/\) 및 이력\(log/\)을 복원합니다.

1.	폴더 목록의 티치 펜던트\(T/P\) 또는 이동식 저장 장치\(USB\)에서 티치 펜던트의 방향키를 이용해 프로젝트 또는 이력이 백업된 폴더를 선택한 후 화면 우측의 \[복사\] 버튼을 터치하십시오.

![](../../_assets/image_119.png)

2.	폴더 목록에서 티치 펜던트의 방향키를 이용해 \[MAIN\]을 선택한 후 화면 우측의 \[붙여넣기\] 버튼을 터치하십시오. 

![](../../_assets/image_120.png)

3.	중복 ~~~~알림창에서 \[전부\] 체크박스를 터치하여 선택한 후 \[확인\] 버튼을 터치하십시오. 메인 보드에 백업 데이터가 복원됩니다.

![](../../_assets/image_123.png)

 4.	제어기의 전원을 다시 켜십시오.



# 4.3 프로그램 변환

작성된 프로그램의 조건 및 위치 등을 일괄 또는 개별적으로 수정하거나 좌표를 변환하여 새 프로그램을 작성합니다.

1.	\[6: 프로그램 변환\] 메뉴를 터치하십시오. 프로그램 변환 메뉴가 나타납니다.

2.	원하는 메뉴를 선택하여 프로그램의 조건 및 위치 등을 수정하거나 새 프로그램을 작성하십시오.

![](../../_assets/image_141.png)

{% hint style="info" %}
로봇 기동 중에는 \[4: 기록좌표계\], \[5: 좌표변환\], \[6: 미러 이미지\], \[7: 스텝복사\] 메뉴의 사용이 제한됩니다.
{% endhint %}



# 4.3.1 기록 조건

프로그램의 특정 스텝에 기록 조건을 변경 설정하여 기존의 프로그램에 적용하거나 새 프로그램을 생성합니다.

1.	\[6: 프로그램 변환 &gt; 1: 기록조건\] 메뉴를 터치하십시오. 기록 조건 변환 설정창이 나타납니다.

2.	기록 조건 옵션을 설정한 후 \[확인\] 버튼을 터치하십시오.

![](../../_assets/image_374.png)

* \[원본 프로그램\]/\[타겟 프로그램\]: 기록 조건을 변경할 원본 프로그램의 번호\(초기 설정값: 현재 선택된 프로그램\)와 기록 조건을 변경한 후 저장할 새 프로그램의 번호를 입력합니다. 대상 프로그램 번호를 원본 프로그램과 같은 번호로 설정하면 원본 프로그램이 덮어쓰기 되어 새 프로그램으로 대체됩니다.
* \[시작 스텝\]/\[종료 스텝\]: 기록 조건을 변경 적용할 스텝의 범위\(초기 설정값: 1 / 마지막 스텝\)를 설정합니다.
* \[Accuracy\], \[툴\]: 기록 조건을 변경합니다.



# 4.3.2 기록 속도

프로그램의 특정 스텝에 기록 속도를 변경 설정하여 기존의 프로그램에 적용하거나 새 프로그램을 생성합니다.
1.	[6: 프로그램 변환 > 2: 기록속도] 메뉴를 터치하십시오. 기록 속도 변환 설정창이 나타납니다.
2.	기록 속도 옵션을 설정한 후 [확인] 버튼을 터치하십시오.
 
 ![](../../_assets/rec-speed.png)

* [원본 프로그램]/[타겟 프로그램]: 기록 속도를 변경할 원본 프로그램의 번호(초기 설정값: 현재 선택된 프로그램)와 기록 속도를 변경한 후 저장할 새 프로그램의 번호를 입력합니다. 대상 프로그램 번호를 원본 프로그램과 같은 번호로 설정하면 원본 프로그램이 덮어쓰기 되어 새 프로그램으로 대체됩니다.
* [시작 스텝]/[종료 스텝]: 기록 조건을 변경 적용할 스텝의 범위(초기 설정값: 1/마지막 스텝)를 설정합니다.
* [방법]: 속도 지정 방법을 설정합니다.
* [속도지정]: 기록된 속도를 일괄 변환합니다.
* [배율지정]: 기록된 속도의 단위와 [단위] 옵션에서 선택한 속도 단위가 일치할 경우, 기록된 속도에 대한 비율(%)로 변환합니다.
* [단위변환]: 기록된 속도의 단위를 변환합니다.
* [구간]: 기록 속도를 변경 설정할 스텝의 범위에서 적용 구간을 설정합니다.
* [단위]: 속도 단위를 설정합니다. 속도 지정 방법을 [배율지정]으로 선택한 경우에는 스텝에 기록된 속도의 단위와 일치하는 것만 배율의 비율로 변환합니다.
* [속도]: 속도를 설정합니다. 속도 지정 방법을 [배율지정]으로 선택한 경우에는 배율값을 의미합니다.
# 4.3.3 기록 위치

프로그램의 특정 스텝에 숨은 포즈로 기록된 스텝 위치의 좌표계를 변경 설정하여 기존의 프로그램에 적용하거나 새 프로그램을 생성합니다.
1.	[6: 프로그램 변환 > 3: 기록위치] 메뉴를 터치하십시오. 기록 위치 변환 설정창이 나타납니다.
2.	기록 위치 옵션을 설정한 후 [확인] 버튼을 터치하십시오.
 
  ![](../../_assets/rec-pos.png)

* [원본 프로그램]/[타겟 프로그램]: 기록 위치를 변경할 원본 프로그램의 번호(초기 설정값: 현재 선택된 프로그램)와 기록 위치를 변경한 후 저장할 새 프로그램의 번호를 입력합니다. 대상 프로그램 번호를 원본 프로그램과 같은 번호로 설정하면 원본 프로그램이 덮어쓰기 되어 새 프로그램으로 대체됩니다.
* [시작 스텝]/[종료 스텝]: 기록 위치를 변경 적용할 스텝의 범위(초기 설정값: 1 / 마지막 스텝)를 설정합니다.
* [좌표계 형식]: 스텝에 기록된 위치 데이터를 변환(shift)할 좌표계를 선택합니다. 베이스, 로봇, 툴, 사용자 선택 시, 직교 좌표값으로 변환하고, 축 선택 시 축 각도로 변환합니다.
# 4.3.4 기록 좌표계

숨은 포즈로 기록된 스텝 위치의 좌표계를 변경합니다. 해당 스텝에서 퀵오픈 버튼을 누르면 변경된 좌표계를 확인할 수 있습니다. 로봇 기동 중에는 [4: 기록좌표계] 메뉴의 사용이 제한됩니다.
1.	[6: 프로그램 변환 > 4: 기록좌표계] 메뉴를 터치하십시오. 기록 좌표계 변환 설정창이 나타납니다.
2.	기록 좌표계 옵션을 설정한 후 [확인] 버튼을 터치하십시오.
 
   ![](../../_assets/rec-crdsys.png)

* [원본 프로그램]/[타겟 프로그램]: 기록 좌표계를 변경할 원본 프로그램의 번호(초기 설정값: 현재 선택된 프로그램)와 기록 좌표계를 변경한 후 저장할 새 프로그램의 번호를 입력합니다. 대상 프로그램 번호를 원본 프로그램과 같은 번호로 설정하면 원본 프로그램이 덮어쓰기 되어 새 프로그램으로 대체됩니다.
* [시작 스텝]/[종료 스텝]: 기록 좌표계를 변경 적용할 스텝의 범위(초기 설정값: 1 / 마지막 스텝)를 설정합니다.
* [좌표계 형식]: 새로 지정할 좌표계를 선택합니다.
# 4.3.5 좌표 변환

좌표 변환 기능은 작업물(이미지 1)에 프로그램을 티칭한 이후에 이미지 2와 같이 동일한 모양의 작업물이 다른 위치에 있을 경우에도 별도의 티칭 없이 프로그램을 작성할 수 있게 해주는 기능입니다.
 
   ![](../../_assets/rec-conv1.png)

좌표 변환 기능을 사용하기 위해서는 3개의 기준점이 필요합니다. 초기 위치에서 작업물에 3개의 기준점을 표시하여 프로그램A를 작성합니다. 작업물의 위치를 이동한 후 미리 표시해 둔 3개의 기준점을 프로그램 B로 작성합니다.
 
   ![](../../_assets/rec-conv2.png)


{% hint style="warning" %}
* 좌표 변환의 세 기준점에 대한 티칭의 정도는 좌표 변환 프로그램의 정확도에 영향을 미칩니다. 가능한 한 3개의 기준점에 대해 정확하게 티칭하십시오.
* 좌표 변환의 3개의 기준점 사이의 거리는 가능한 한 멀게 설정하십시오.
{% endhint %}


프로그램 A와 프로그램 B의 기준이 되는 3 스텝에서 좌표 변환량을 계산하여 기존 프로그램(프로그램 1)을 새로운 프로그램(프로그램 2)으로 변환합니다.
 

![](../../_assets/rec-conv3.png)


로봇 기동 중에는 [5: 좌표변환] 메뉴의 사용이 제한됩니다. 좌표 변환 기능을 사용하는 방법은 다음과 같습니다.
1.	[6: 프로그램 변환 > 5: 좌표변환] 메뉴를 터치하십시오. 좌표 변환 설정창이 나타납니다.
2.	좌표 변환 옵션을 설정한 후 [확인] 버튼을 터치하십시오.
 
 ![](../../_assets/rec-conv4.png)

* [원본 프로그램]/[대상 프로그램]: 기존의 티칭 프로그램 번호(이미지 1의 프로그램 번호)와 좌표 변환을 수행하여 생성할 새 프로그램 번호(이미지 2의 프로그램 번호)를 설정합니다.
* [이전위치 프로그램]/[변경위치 프로그램]: 좌표 변환의 기준이 되는 3점이 기록된 프로그램 번호(프로그램 A의 번호)와 좌표 변환의 기준이 되는 3점이 기록된 프로그램 번호(프로그램 B의 번호)를 설정합니다.
# 4.3.6 미러 이미지

로봇의 S축 0° 위치에서 Y-Z 평면을 기준으로 S축 위치와 손목축의 자세가 대칭인 프로그램을 작성합니다.
이 기능은 자동차의 본체 용접과 같이 좌우 두 대의 로봇에 동일한 작업을 지시할 때 유용합니다. 먼저 한 대의 로봇에 작업을 티칭한 후 다른 한 대의 로봇에는 티칭한 작업의 프로그램을 열고 미러 이미지로 변환하면 S축에 대칭인 프로그램이 작성됩니다.

   ![](../../_assets/mirror-image1.png)
 
 
{% hint style="info" %}
협동로봇에는 미러 이미지 기능을 지원하지 않습니다.
로봇 기동 중에는 [6: 미러 이미지] 메뉴의 사용이 제한됩니다. 미러 이미지 기능을 사용하는 방법은 다음과 같습니다.
{% endhint %}


1.	[6: 프로그램 변환 > 6: 미러 이미지] 메뉴를 터치하십시오. 미러 이미지 설정창이 나타납니다.
2.	미러 이미지 변환 옵션을 설정한 후 [확인] 버튼을 터치하십시오.

* [원본 프로그램]/[대상 프로그램]: 기존 프로그램 번호와 미러 이미지로 변환하여 생성할 새 프로그램 번호를 설정합니다.

   ![](../../_assets/mirror-image2.png)# 4.3.7 스텝 복사

프로그램의 일부를 다른 프로그램 또는 동일 프로그램으로 복사합니다. 스텝에 기록된 펑션(기능)도 함께 복사됩니다. 로봇 기동 중에는 [7: 스텝복사] 메뉴의 사용이 제한됩니다.

1.	[6: 프로그램 변환 > 7: 스텝복사] 메뉴를 터치하십시오. 스텝 복사 설정창이 나타납니다.
2.	스텝 복사 옵션을 설정한 후 [확인] 버튼을 터치하십시오
 
   ![](../../../_assets/step-copy.png)

* [원본 프로그램]/[대상 프로그램]: 스텝을 복사할 원본 프로그램 번호와 복사한 스텝을 붙여 넣어 생성할 새 프로그램 번호를 설정합니다. 대상 프로그램 번호를 원본 프로그램과 같은 번호로 설정하면 원본 프로그램이 덮어쓰기 되어 새 프로그램으로 대체됩니다.
* [시작 스텝]/[종료 스텝]: 복사할 스텝의 범위(초기 설정값: 1/마지막 스텝)를 설정합니다.
* [투입 스텝]: 복사한 스텝을 붙여 넣을 기준 스텝을 설정합니다. 복사한 스텝은 기준 스텝 바로 다음에 붙여 넣기됩니다.
* [복사 방법]: 복사한 스텝의 진행 방향을 선택합니다.
* [정방향]/[역방향]: 복사한 스텝이 원본 프로그램과 동일한 순서 또는 원본 프로그램의 역순으로 붙여 넣기됩니다.

{% hint style="info" %}
* 보호 설정된 프로그램은 복사할 수 없습니다.
* 복사한 스텝에 END 기능이 기록된 경우, 기능이 함께 복사됩니다. 필요에 따라 기능을 삭제하십시오.
* 복사한 스텝에 복사 범위를 벗어난 스텝으로 점프(GOTO, GOSUB)하는 기능이 기록된 경우, 기능은 복사되지만 번호는 자동으로 변경되지 않습니다. 복사 후 번호를 변경하십시오.
{% endhint %}
# 4.3.7.1 스텝 복사 예

프로그램1의 스텝2 ~ 스텝5를 프로그램2의 스텝2\(투입 스텝으로 설정\)에 정방향과 역방향으로 복사합니다.

대상 프로그램\(프로그램2\)의 투입 스텝\(스텝2\) 바로 다음에 원본 프로그램\(프로그램1\)의 스텝2 ~ 스텝5가 정방향\(원본 프로그램과 동일한 순서\) 또는 역방향\(원본 프로그램의 역순\)으로 삽입됩니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">방법</th>
      <th style="text-align:left">절차</th>
      <th style="text-align:left"></th>
      <th style="text-align:left">상세 과정</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">정방향</td>
      <td style="text-align:left">복사 전</td>
      <td style="text-align:left">
        <p>원본 프로그램</p>
        <p>(프로그램1)</p>
        <p>▼</p>
        <p>▼</p>
        <p>대상 프로그램</p>
        <p>(프로그램2)</p>
      </td>
      <td style="text-align:left">
        <img src="../../../_assets/step-copy-fwd-prv.png" alt/>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">복사 결과</td>
      <td style="text-align:left">프로그램2</td>
      <td style="text-align:left">
        <img src="../../../_assets/step-copy-fwd-nxt.png" alt/>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">역방향</td>
      <td style="text-align:left">복사 전</td>
      <td style="text-align:left">
        <p>원본 프로그램</p>
        <p>(프로그램1)</p>
        <p>▼</p>
        <p>▼</p>
        <p>대상 프로그램</p>
        <p>(프로그램2)</p>
      </td>
      <td style="text-align:left">
        <img src="../../../_assets/step-copy-bwd-prv.png" alt/>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">복사 결과</td>
      <td style="text-align:left">프로그램2</td>
      <td style="text-align:left">
        <img src="../../../_assets/step-copy-bwd-nxt.png" alt/>
      </td>
    </tr>
  </tbody>
</table>

# 4.4 시스템 진단

로봇과 제어기의 상태를 검사하고 관리합니다. 제어기의 모듈별로 버전을 확인하고 업데이트할 수 있습니다.

# 4.4.1 시스템 버전

\[7: 시스템 진단 &gt; 1: 시스템 환경\] 메뉴를 터치하십시오. 시스템 환경 설정창이 나타납니다.

1. 로봇과 제어기의 시스템 환경 정보를 확인하고 관리하십시오.

![](../../../_assets/image_139.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">로봇과 제어기의 시스템
        환경(소프트웨어 버전)
        정보입니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <p>기능 버튼을 이용해 시스템
          환경을 편집하고 관리합니다.</p>
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[버전업]: 제어기 각 모듈의
            버전을 업데이트합니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

# 4.4.1.1 제어기 시스템 업데이트

통합 압축 파일을 이용하여 제어기 각 모듈의 버전을 업데이트합니다.

1.	통합 압축 파일이 저장된 이동식 저장 장치를 티치 펜던트의 USB 슬롯에 연결하십시오. 티치 펜던트에 이동식 저장 장치가 연결되면 상태 표시줄에 \[USB\] 아이콘\(![](../../../_assets/icon-usb2.png)\)이 나타납니다.

2.	시스템 환경 설정창 우측의 \[버전업\] 버튼을 터치하십시오. 버전업 프로그램 실행창이 나타납니다.

3.	드롭다운 메뉴를 터치하여 \[버전 업\] 모드를 선택하고 \[Open\] 버튼을 이용하여 통합 압축 파일을 선택한 후 \[확인\] 버튼을 터치하십시오. 

![](../../../_assets/image_118.png)

4.	업데이트할 모듈을 선택한 후 \[확인\] 버튼을 터치하십시오. 업데이트가 시작됩니다. 

![](../../../_assets/image_109.png)

5.	업데이트가 완료되면 \[확인\] 버튼을 터치하십시오. 버전업 프로그램 실행창이 닫히고 제어기가 자동으로 재시작합니다.

![](../../../_assets/image_114.png)

# 4.5 날짜 및 시간 설정

제어기의 날짜와 시간을 설정합니다.

1.	\[8: 날짜, 시간 설정\] 메뉴를 터치하십시오. 날짜 및 시간 설정창이 나타납니다.

2.	날짜 및 시간 정보를 설정한 후 \[OK\] 버튼을 터치하십시오.

![](../_assets/image_122.png)

* 티치 펜던트의 조작키로 날짜와 시간을 입력하여 설정합니다.
* 방향키를 누르면 날짜와 시간 항목\(연/월/일/시/분/초/오전오후\) 사이에서 커서가 이동합니다.
* 숫자키를 눌러 숫자를 입력합니다. &lt;shift+↑/↓&gt; 키로 수치를 조절할 수도 있습니다.
* 달력에서 날짜를 설정합니다. \[◁/▷\] 버튼을 터치하여 연월을 선택한 후 날짜를 터치하십시오.



# 5. 조건 설정

프로그램을 수정하지 않고 운전 조건만 간편히 변경합니다. 변경한 설정값은 제어기가 재시동되어도 동일하게 유지됩니다.

# 5.1    운전 조건 설정

1.	초기 화면에서 좌측 상단의 \[속도조절\] 버튼을 터치하십시오. 운전 조건 설정창이 나타납니다.

![](../_assets/image_113.png)

{% hint style="info" %}
\[속도조절\] 버튼에는 수동 모드일 때에는 스텝 전후진 제한 속도\(㎜/sec\)가 표시되고, 자동 모드에서는 재생 속도\(%\)가 표시됩니다.
{% endhint %}



2.	다음 절차를 반복하여 운전 조건 설정값을 변경한 후 \[OK\] 버튼을 터치하십시오.

![](../_assets/image_132.png)

a.	티치 펜던트의 방향키로 커서를 이동합니다.

b.	방향키로 원하는 옵션을 선택하거나 숫자키를 눌러 수치를 입력하십시오.

c.	&lt;enter&gt; 키를 누르십시오. 변경 내용이 적용되어 설정값이 변경되고 커서가 다음 항목으로 이동합니다.

# 5.2    운전 조건 설정 정보



* \[1: 동작 사이클\]: 자동 운전 시 실행되는 프로그램의 반복 여부를 설정합니다. 로봇 기동 중에도 설정할 수 있으며 수동 운전 시에서 설정값이 적용되지 않습니다.
  * 1사이클: 작업 프로그램을 1 회 운전 후 종료합니다. 프로그램 END를 만나면 로봇이 정지합니다.
  * 반복: 작업 프로그램을 연속해서 반복 운전합니다. 외부의 정지 조작이 있으면 로봇이 정지합니다.
* \[2: 스탭 전/후진시 최고속\]: 스텝의 전후진 시 제한 속도를 설정합니다. 이 옵션에 대한 자세한 내용은 “[2.1 수동 운전](../operation/manual-operation/)”을 참조하십시오.
* \[3: 스탭 전진시 펑션 실행\]: 스텝 전진 시 작업 프로그램에 기록된 기능의 실행 옵션\(방식\)을 설정합니다.
  * Off: 작업 프로그램에 기록된 END만 실행합니다. END를 제외한 다른 모든 기능은 실행하지 않습니다.
  * On: 작업 프로그램에 기록된 모든 기능을 실행합니다.
  * 1 On: 입력 신호 대기 기능과 프로그램 END 기능만 실행합니다.

{% hint style="warning" %}
스텝 후진 시에는 입력 대기 신호 기능만 실행하고 이외의 모든 기능은 실행하지 않습니다.
{% endhint %}

* \[4: 스텝 후진 후, 전진 시 펑션 재실행\]: 스텝 후진 후 다시 전진할 때 작업 프로그램에 기록된 기능 중 이전에 실행한 기능을 다시 실행하도록 설정합니다.
* \[5: 스텝 전/후진시 경로복구\]: 스텝 전후진 시 경로 복구의 실행 방식을 설정합니다.
  * 무효: 경로 복구를 실행하지 않습니다.
  * 유효: 사용자에게 경로 복구의 실행 여부를 확인하지 않고 수행합니다.
* \[6: 자동운전 속도비율\]: 자동 모드로 프로그램 재생 시 로봇의 운전 속도\(%\)를 설정합니다. 작업 프로그램의 스텝에 기록된 속도를 변경하는 것이 아니라 스텝에 기록된 속도에 대한 로봇의 이동 속도를 1 ~ 100% 범위의 비율\(%\)로 일괄 변경합니다.


{% hint style="info" %}
스텝 후진 시에는 입력 대기 신호 기능만 실행하고 이외의 모든 기능은 실행하지 않습니다.
{% endhint %}

* \[7: 로봇 Lock\]: 로봇을 실제로 움직이지 않고 작업 프로그램을 자동 운전하도록 설정합니다. 주변 기기와의 입출력 상태와 소프트 리미트, 사이클 타임 등을 확인할 수 있습니다.
* \[8: 보간기준\]: 수동으로 로봇을 조그 동작할 때 기준이 되는 툴을 설정합니다. 일반적으로 로봇툴을 보간 기준으로 사용합니다.
  * 로봇툴: 로봇 선단에 부착된 툴을 기준으로 보간 동작을 실행합니다.
  * 정치툴: 바닥면 등에 고정된 툴의 선단을 기준으로 보간 동작을 실행합니다. 정치툴을 보간 기준으로 선택하면 초기 화면 좌측의 툴 번호가 ST0으로 표시됩니다\(![](../_assets/icon-st0.png)\).


{% hint style="info" %}
정치툴을 보간 기준으로 선택한 경우 반드시 정치툴 좌표계를 설정해야 합니다. 자세한 내용은 “[7.3.6.2 정치툴 좌표계](../setting/control-parameter/cordsys-reg/stationary-tool-crdsys.md)”를 참조하십시오.
{% endhint %}

* \[9: 사용자 좌표계 지정\]: 수동 조그 조작 시 직교 동작을 위해 사용자 좌표계 번호\(0 ~ 10\)를 설정합니다. 로봇이 지정된 사용자 좌표계의 X, Y, Z 축 방향으로 직교 좌표계 동작을 수행합니다. 그리고 포즈 모니터링 시 선택한 사용자 좌표계의 좌표값이 툴 선단의 X, Y, Z 좌표값으로 나타납니다.



* 
  0으로 설정하면 화면 우측의 \[좌표계\] 버튼에 로봇 좌표계 아이콘\(![](../_assets/icon-crd-rob.png)\)이 표시됩니다. 사용자 좌표계에 대한 동작이 해제되고 로봇 좌표계에 대한 직교 좌표 동작 및 모니터링을 수행합니다.

![](../_assets/image_126.png)

* 1 ~ 10 사이의 번호로 설정하면 \[좌표계\] 버튼에 사용자 좌표계 아이콘\(![](../_assets/icon-crd-user.png)\)이 표시됩니다. &lt;축조작&gt; 키로 변경된 좌표치 값은 사용자 좌표계를 기준으로 합니다.


![](../_assets/image_134.png)



{% hint style="info" %}
사용자 좌표계 번호는 \[설정 &gt; 2: 제어 파라미터 &gt; 7: 좌표계 등록 &gt;1: 사용자 좌표계\] 메뉴에서 등록할 수 있습니다.
{% endhint %}







# 6. 모니터링

로봇 시스템의 상태와 제어기의 각종 데이터를 확인합니다.

# 6.1 모니터링 기능 사용

1.	작업 영역의 패널 스택 우측 상단의 \[+\] 버튼을 터치하십시오. 패널 선택창이 나타납니다.

![](../_assets/image_145.png)

2.	패널 선택창에서 원하는 모니터링 항목을 선택하여 로봇 시스템의 상태와 제어기의 각종 데이터를 확인하십시오.

![](../_assets/image_155.png)

{% hint style="info" %}
* 패널 선택창에 모니터링 가능한 모든 항목이 나타납니다.
* 모니터링 가능한 항목은 제어기 설정에 따라 다르게 나타납니다.
* 작업 영역의 패널 스택과 창의 사용 방법에 대한 자세한 내용은 “[1.2.4.5 작업 영역](../robot-system/basic-usage/screen-of-the-hi6-tp/work-area.md)”을 참조하십시오.
{% endhint %}







# 6.2 job

패널 선택창에서 \[job\]을 터치하십시오. JOB 프로그램창이 나타납니다. 프로그램을 확인하고 편집 및 삭제하거나 작성할 수 있습니다.

![그림 34 JOB 프로그램](../_assets/image_156.png)

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
      <td style="text-align:left">프로그램의 기본 정보와
        명령문을 표시합니다.
        명령문의 상세 정보를
        확인하고 편집할 수 있습니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[프로그램]: 작성된 프로그램
            목록에서 프로그램을
            선택하거나 삭제합니다.
            <br
            />
          </li>
          <li>[…]: 자동 들여쓰기가
            잘못 적용된 경우 JOB 프로그램의
            자동 들여쓰기를 다시
            수행합니다.
            <br />
          </li>
          <li>프로그램 작성 시 선택한
            명령문의 인수값은 입력
            영역에 표시됩니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
프로그램의 관리 및 작성 방법에 대한 자세한 내용은 “[3 프로그램 작성](../programming/)”을 참조하십시오.
{% endhint %}

# 6.3 포즈

패널 선택창에서 \[포즈\]를 터치하십시오. 로봇의 포즈 정보창이 나타납니다. 로봇 각 축의 현재 각도와 TCP의 좌표값, 엔코더의 현재값과 지령값을 확인할 수 있습니다.

![그림 35 포즈](../_assets/image_142.png)

# 6.4 시스템 입력

패널 선택창에서 \[시스템 입력\]을 터치하십시오. 입력 신호창이 나타납니다.

로봇의 운행과 관련된 신호, 제어기와 로봇의 이상을 감지하기 위해 미리 할당된 입력 신호의 상태를 확인할 수 있습니다.

![그림 36 시스템 입력 - ON/OFF 상태\(좌\) / 값 상태\(우\)](../_assets/image_149.png)

![그림 37 시스템 입력 - 시퀀스 상태](../_assets/image_162.png)

* ON/OFF 상태와 시퀀스 상태에서 현재 입력 중인 신호는 노란색으로 표시됩니다.
* 시퀀스 상태에서는 제어기 시퀀스 신호의 상태만 표시합니다.
* \[ON/OFF\]/\[값\]/\[시퀀스\]: 라디오 버튼을 터치하여 입력 신호창의 표시 방식을 변경할 수 있습니다.

# 6.5 시스템 출력

패널 선택창에서 \[시스템 출력\]을 터치하십시오. 출력 신호창이 나타납니다.

로봇의 운행과 관련된 신호와 브레이크 제어 상태를 확인할 수 있습니다.

![그림 38 시스템 출력 - ON/OFF 상태\(좌\) / 값 상태\(우\)](../_assets/image_159.png)

![그림 39 시스템 출력 - 시퀀스 상태](../_assets/image_161.png)

* ON/OFF 상태와 시퀀스 상태에서 현재 입력 중인 신호는 노란색으로 표시됩니다.
* 시퀀스 상태에서는 제어기 시퀀스 신호의 상태만 표시합니다.
* \[ON/OFF\]/\[값\]/\[시퀀스\]: 라디오 버튼을 터치하여 출력 신호창의 표시 방식을 변경할 수 있습니다.
* \[수동 출력\]: ON/OFF 상태와 시퀀스 상태에서 선택한 신호를 강제로 출력할 수 있습니다.

## 수동 출력

원하는 신호를 선택하여 강제로 출력할 수 있습니다.

1. 시스템 출력 신호창 우측의 \[ON/OFF\] 또는 \[시퀀스\] 라디오 버튼을 터치하여 표시 방식을 ON/OFF 또는 시퀀스 상태로 설정하십시오.
2. 신호창에서 신호를 터치하여 선택한 후 \[수동 출력\] 버튼을 터치하십시오.

![](../_assets/image_146.png)

1. 수동 출력 확인창에서 출력 조건을 확인한 후 \[확인\] 버튼을 터치하십시오.

![](../_assets/image_143.png)

| soN | =1/0 |
| :---: | :---: |
| N: 출력할 신호의 번호 | 출력 상태\(1: 출력, 0: 미출력\) |

1. 선택한 신호의 출력 상태를 확인하십시오. 선택한 신호가 출력 상태로 전환되어 신호창에 노란색으로 표시됩니다.

![](../_assets/image_164.png)

# 6.6 범용 입력

패널 선택창에서 \[범용 입력\]을 터치하십시오. 범용 입력 신호창이 나타납니다.

제어기 내 I/O 보드의 CNIN 커넥터를 통해 입력되는 신호인 범용 입력 신호의 상태를 확인할 수 있습니다.

![그림 40 범용 입력 신호 - ON/OFF 상태\(좌\) / 값 상태\(우\)](../_assets/image_166.png)

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
        <img src="../_assets/c2.png" alt/>
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

![](../_assets/user-input-flow.png)

# 6.7 범용 출력

패널 선택창에서 \[범용 출력\]을 터치하십시오. 범용 출력 신호창이 나타납니다.

제어기 내 I/O 보드의 CNOUT커넥터를 통해 입력하는 신호인 범용 출력 신호의 상태를 확인할 수 있습니다.

![그림 41 범용 출력 신호 - ON/OFF 상태\(좌\) / 값 상태\(우\)](../_assets/image_152.png)

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
            노란색으로 표시됩니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[FB0]: 드롭다운 메뉴를 터치하여
            모니터링할 FB 블록을 선택할
            수 있습니다(FB0 ~ FB15). 최대
            16 개의 I/O 블록을 구성할
            수 있으며 블록은 960 점의
            신호를 모니터링합니다.</li>
          <li>[수동 출력]: 선택한 신호를
            강제로 출력할 수 있습니다.</li>
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
* 내장 PLC로 필드버스 신호 등을 매핑하여 사용하는 경우에는 출력 신호의 On/Off 상태가 다르게 나타날 수 있습니다.
* 출력 신호의 흐름은 다음과 같습니다.
{% endhint %}

![](../_assets/user-input-flow.png)

## 수동 출력

원하는 신호를 선택하여 강제로 출력할 수 있습니다.

1. 범용 출력 신호창 우측의 \[ON/OFF\] 라디오 버튼을 터치하여 표시 방식을 ON/OFF 상태로 설정하십시오.
2. 신호창에서 신호를 터치하여 선택한 후 \[수동 출력\] 버튼을 터치하십시오.

![](../_assets/image_157.png)

1. 수동 출력 확인창에서 출력 조건을 확인한 후 \[확인\] 버튼을 터치하십시오.

![](../_assets/image_147.png)

| FbN | doN | =1/0 |
| :---: | :---: | :---: |
| N: 모니터링할 FB 블록의 번호 | N: 출력할 신호의 번호 | 출력 상태\(1: 출력, 0: 미출력\) |

1. 선택한 신호의 출력 상태를 확인하십시오. 선택한 신호가 출력 상태로 전환되어 신호창에 노란색으로 표시됩니다.

![](../_assets/image_165.png)

# 6.8 전역변수

JOB 프로그램에 global로 정의된 전역 변수를 확인합니다. 또한 변수값을 선택하여 변경할 수 있습니다.

1.	global로 정의된 전역 변수가 포함된 프로그램을 실행한 후 작업 영역의 패널 스택 우측 상단의 \[+\] 버튼을 터치하십시오.

![](../_assets/image_151.png)

2.	패널 선택창에서 \[전역변수\]를 터치하십시오. 프로그램에 포함된 전역 변수 목록이 새 창에 나타납니다.

![](../_assets/image_163.png)

3.	변수 이름과 유형, 값을 확인하십시오. 변수값을 선택하여 변경할 수도 있습니다.

![](../_assets/image_148.png)

# 6.9 지역변수

JOB 프로그램에 var로 정의된 지역 변수를 확인합니다. 또한 변수값을 선택하여 변경할 수 있습니다.

1.	var로 정의된 지역 변수를 포함한 프로그램을 실행한 후 작업 영역의 패널 스택 우측 상단의 \[+\] 버튼을 터치하십시오.

![](../_assets/image_144.png)

2.	패널 선택창에서 \[지역변수\]를 터치하십시오. 프로그램에 포함된 지역 변수 목록이 새 창에 나타납니다.

![](../_assets/image_150.png)

3.	변수 이름과 유형, 값을 확인하십시오. 변수값을 선택하여 변경할 수도 있습니다.

![](../_assets/image_160.png)



# 6.10 가동정보

패널 선택창에서 \[가동정보\]를 터치하십시오. 제어기의 가동 정보창이 나타납니다.

시스템 초기화와 전원 투입, 최근 사이클 시작 직후의 제어기 동작별 누적 시간과 사이클 횟수를 확인할 수 있습니다. 정보 하단의 항목별 \[클리어\] 버튼을 터치하면 가동 정보를 초기화할 수 있습니다.

![그림 42 가동 정보](../_assets/image_170.png)

항목별 조건에 따른 반영 시점은 다음과 같습니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">항목</th>
      <th style="text-align:left">조건</th>
      <th style="text-align:left">반영 시점</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">시스템 초기화 후</td>
      <td style="text-align:left">측정 시간</td>
      <td style="text-align:left">시스템 초기화 후부터
        현재 시점 사이에 제어기가
        가동한 시간</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">모터 ON 시간</td>
      <td style="text-align:left">시스템 초기화 후부터
        현재 시점 사이에 제어기의
        모터가 켜져 있었던 시간</td>
    </tr>
    <tr>
      <td style="text-align:left">전원 투입 후</td>
      <td style="text-align:left">측정 시간</td>
      <td style="text-align:left">
        <p>전원 투입 후부터 현재
          시점 사이에 제어기가
          가동한 시간</p>
        <p>
          <img src="../_assets/op-time1.png" alt/>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">사이클 기록 시간</td>
      <td style="text-align:left">
        <p>전원 투입 후부터 지난
          사이클까지 제어기가
          가동한 시간</p>
        <p>
          <img src="../_assets/op-time2.png" alt/>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">최근 사이클 시작 후</td>
      <td
      style="text-align:left">측정 시간</td>
        <td style="text-align:left">
          <p>사이클 시작(또는 전원
            투입) 후부터 현재 시점
            사이에 제어기가 가동한
            시간</p>
          <p>
            <img src="../_assets/op-time3.png" alt/>
          </p>
        </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">사이클 기록 시간</td>
      <td style="text-align:left">
        <p>사이클 시작(또는 전원
          투입) 후부터 지난 사이클까지
          제어기가 가동한 시간</p>
        <p>
          <img src="../_assets/op-time4.png" alt/>
        </p>
      </td>
    </tr>
  </tbody>
</table>

# 6.11 이력

패널 선택창에서 \[이력\]을 터치하십시오. 이력창이 나타납니다.

에러, 경고, 알림, 운전, 사용자 작동, I/O, 실행에 대한 이력을 확인할 수 있습니다.

![그림 43 이력](../_assets/image_169.png)

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
        <p>목록에 표시할 이력의
          유형을 설정할 수 있습니다.
          원하는 유형의 버튼을
          터치하면 해당 유형에
          속하는 이력만 목록에
          나타납니다.</p>
        <ul>
          <li>[전부]: 모든 유형의 이력을
            확인합니다.</li>
          <li>[+E]/[+W]: 에러 또는 경고 이력을
            확인합니다.
            <br />로봇 시스템에 문제가
            발생하면 문제의 내용과
            발생 시각, 발생 시점의
            프로그램 번호, 스텝 번호,
            축 데이터, 입출력 상태를
            확인하고 기록하여 문제
            이력을 관리합니다. 그리고
            문제의 원인을 분석하거나
            시스템 복구 시 이전에
            발생한 문제의 이력을
            참조합니다.</li>
          <li>[+N]: 알림 이력을 확인합니다.</li>
          <li>[+ST]: 로봇을 운전한 이력을
            확인합니다.
            <br />로봇의 기동, 정지 및 모드
            변경 등 운전과 관련된
            신호가 입력되면 내용과
            시각, 입력 시점의 프로그램
            번호, 스텝 번호, 축 데이터,
            입출력 상태를 기록합니다.
            그리고 로봇 보수 시 로봇
            운전 이력을 참조합니다.</li>
          <li>[+P]: 주기적으로 기록되는
            상태 이력을 확인합니다.</li>
          <li>[+OP]: 조작 이력을 확인합니다.</li>
          <li>[+IO]: 입출력 신호의 변화
            이력을 확인합니다.</li>
          <li>[+H]: JOB 프로그램의 실행 이력을
            확인합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[num.]: 드롭다운 메뉴를 터치하여
            목록에 표시할 이력의
            수(30, 100, 200, 500, 1000)를 조정할 수
            있습니다. 이력의 수를
            선택하면 해당 개수만큼의
            최근 이력을 다시 불러와
            화면에 표시합니다.</li>
          <li>[
            <img src="../_assets/bt-menu.png" alt/>]: 팝업 메뉴를 엽니다.
            <ul>
              <li>log 파일로 저장: 메모리
                버퍼의 최신 이력을 파일로
                저장합니다.</li>
              <li>log 파일 클리어: 메모리
                버퍼의 이력을 클리어하고
                이력 파일을 모두 삭제합니다.(삭제된
                파인 복구할 수 없습니다.)</li>
            </ul>
          </li>
          <li>[
            <img src="../_assets/bt-lock.png" alt/>]: 새로운 이력의 알림을
            끕니다. 잠금 표시를 풀
            때까지 이력은 갱신되지
            않고 현재 상태가 유지됩니다.</li>
          <li>[
            <img src="../_assets/bt-trash.png" alt/>]: 화면에 표시된 이력을
            클리어합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">선택한 유형의 이력 목록입니다.
        유형별 이력의 상세 정보를
        확인할 수 있습니다.</td>
    </tr>
  </tbody>
</table>

# 6.12 히스토리

패널 선택창에서 \[히스토리\]를 터치하십시오. 히스토리창이 나타납니다.

작업 프로그램의 실행 이력과 타임 스탬프가 함께 출력되어 히스토리를 확인할 수 있습니다.

![그림 44 히스토리](../_assets/image_173.png)

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
        <ul>
          <li>[
            <img src="../_assets/bt-refresh.png" alt/>]: 실행 이력을 새로고칩니다.</li>
          <li>[
            <img src="../_assets/bt-lock.png" alt/>]: 새로운 이력의 알림을
            끕니다. 잠금 표시를 풀
            때까지 이력은 갱신되지
            않고 현재 상태가 유지됩니다.</li>
          <li>[
            <img src="../_assets/bt-trash.png" alt/>]: 화면에 표시된 이력을
            클리어합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">작업 프로그램의 실행
        이력과 타임 스탬프입니다.
        실행 작업 프로그램의
        히스토리를 확인할 수
        있습니다.</td>
    </tr>
  </tbody>
</table>

# 6.13 시스템 특성

패널 선택창에서 \[시스템 특성\]을 터치하십시오. 시스템 특성창이 나타납니다. 로봇 시스템의 다양한 데이터를 모두 확인하거나 특정한 정보 유형의 데이터만 확인할 수 있습니다.

![그림 45 시스템 특성](../_assets/image_171.png)

| 번호 | 설명 |
| :--- | :--- |
| ![](../_assets/c1.png) | 로봇 시스템의 데이터를 표시합니다. 상단의 정보 유형을 선택하여 해당 유형의 상세 데이터를 확인할 수 있습니다. |
| ![](../_assets/c2.png) | \[초기화\]: 축별 모션을 제외한 나머지 항목에 한하여, 시스템 데이터의 최대값을 유형별로 초기화할 수 있습니다. |

{% hint style="info" %}
시스템 특성 모니터링 기능은 엔지니어 모드에서만 사용할 수 있습니다.
{% endhint %}

{% hint style="warning" %}
* 엔지니어 모드\(Engineer Mode\)에서는 상태 표시줄에 엔지니어 모드 아이콘\(![](../_assets/eng-mode.png)\)이 깜빡입니다.
* 엔지니어 모드에서 잘못 설정하면 로봇 시스템에 심각한 문제가 발생할 수 있으므로 주의하시기 바랍니다.
{% endhint %}

## 초기화

원하는 정보 유형을 선택하여 데이터의 최대값을 초기화할 수 있습니다.

1. 시스템 특성창 하단의 \[초기화\] 버튼을 터치하십시오.

![](../_assets/image_177.png)

1. 초기화할 정보 유형을 터치하십시오. 선택한 항목의 최대값이 초기화됩니다.

![](../_assets/image_168.png)

# 6.14 태스크

패널 선택창에서 \[태스크\]를 터치하십시오. 태스크창이 나타납니다.

태스크별 동작 주기와 실행 시간 정보를 확인할 수 있습니다.

![그림 46 태스크](../_assets/image_172.png)

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
        <ul>
          <li>[동작 주기]/[실행 시간]:
            태스크별 정보 유형을
            변경합니다.</li>
          <li>[초기화]: 표시된 정보를
            초기화합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">태스크별 동작 주기와
        실행 시간 정보를 표시합니다</td>
    </tr>
  </tbody>
</table>

# 6.15 소프트키보드

패널 선택창에서 \[소프트키보드\]를 터치하십시오. 소프트 키보드창이 나타납니다.

숫자와 문자, 기호 및 특수 기호를 포함한 변수나 수식, 문자열을 입력할 수 있습니다. 소프트 키보드의 사용 방법에 대한 자세한 내용은 “[3.2.4.4 소프트 키보드](../programming/prog-edit/statement-edit/softkeyboard.md)”를 참조하십시오.

![그림 47 소프트 키보드](../_assets/image_176.png)

# 6.16 workcell

패널 선택창에서 \[workcell\]을 터치하십시오. 로봇의 현재 자세가 3D 화면에 나타납니다.

협동로봇의 안전 기능을 설정하면 작업 영역\(![](../_assets/c1.png)\)과 툴 영역\(![](../_assets/c2.png)\), 툴 방향 제약\(![](../_assets/c3.png)\), 로봇 엘보우 영역\(![](../_assets/c4.png)\), 금지 영역\(![](../_assets/c5.png)\)의 설정 상태를 확인할 수 있습니다.

![그림 48 workcell모니터링](../_assets/image_174.png)

* 3D 화면 우측 하단의 \[확대/축소\] 아이콘\(![](../_assets/wc-zoom.png)\), \[이동\] 아이콘\(![](../_assets/wc-pan.png)\), 또는 \[회전\] 아이콘\(![](../_assets/wc-rotate.png)\)을 선택한 후 화면을 드래그하면 카메라가 조정됩니다.
* 설정을 변경한 경우에는 workcell 창을 닫고 다시 열어야 변경한 설정값이 적용됩니다.

# 6.17 도움말

패널 선택창에서 \[도움말\]을 터치하십시오. 제어기의 도움말 창에서 Hi6 제어기의 사용 정보를 확인할 수 있습니다.

![그림 49 도움말](../_assets/image_167.png)

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
        <p>제어기의 도움말 목록입니다.</p>
        <ul>
          <li>[
            <img src="../_assets/icon-gt.png" alt/>]/[
            <img src="../_assets/icon-wedge.png" alt/>]: 하위 항목을 숨기거나
            표시합니다.</li>
          <li>[
            <img src="../_assets/icon-file.png" alt/>]: 하단에 선택한 항목의
            상세 내용을 표시합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">상단의 도움말 목록에서
        선택한 항목의 상세 내용을
        표시합니다.</td>
    </tr>
  </tbody>
</table>

# 6.18 센서 동기

패널 선택창에서 \[센서 동기\]를 터치하십시오. 센서 동기창이 나타납니다.

컨베이어 및 프레스 동기 기능과 관련된 정보를 확인할 수 있습니다. 센서 동기 기능은 \[설정 &gt; 4: 응용 파라미터 &gt; 4: 센서 동기\] 메뉴에서 동기 상태를 컨베이어 또는 프레스로 설정하면 활성화됩니다.

![그림 50 센서 동기 모니터링](../_assets/image_175.png)

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
      <td style="text-align:left">선택한 센서의 컨베이어
        및 프레스 동기 기능과
        관련된 정보를 표시합니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[sensor #1]: 드롭다운 메뉴를
            터치하여 모니터링할
            센서를 선택합니다.</li>
          <li>[수동 초기화]: 센서 관련
            각종 데이터(엔코더 펄스,
            센서 위치, 센서 속도, 작업물
            진입 개수, 동기 재생 상태
            등)를 수동으로 삭제합니다.</li>
          <li>[리밋 스위치 작동]: 리밋
            스위치를 수동으로 입력할
            경우 사용합니다.</li>
          <li>[작업 포지션 입력]: 센서의
            위치값(직선 mm, 원형 deg)을
            수동으로 입력합니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
센서 동기 기능에 대한 자세한 내용은 별도의 “Hi6 센서동기 기능 설명서”를 참조하십시오.
{% endhint %}

# 6.19 프로그램 예약실행

패널 선택창에서 \[프로그램 예약실행\]을 터치하십시오. 예약 실행창이 나타납니다.

외부 신호에 의해 프로그램을 예약하고 예약 순서에 따라 프로그램을 수행할 때, 예약 프로그램 목록에서 상태를 확인하고 변경할 수 있습니다.

![그림 51 프로그램 예약 실행 화면](../_assets/image_179_1.png)

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
        <p>예약 프로그램 목록입니다.
          1 ~ 20 개의 프로그램을 예약
          설정할 수 있습니다.</p>
        <ul>
          <li>원격 모드에서 실행 중인
            프로그램이 종료되면
            예약 순서에 따라 프로그램이
            자동으로 실행됩니다.</li>
          <li>프로그램의 예약 실행이
            종료되면 목록에서 삭제됩니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[편집]: 예약 프로그램
            목록을 편집합니다.</li>
          <li>[삽입]: 예약 프로그램
            목록에 예약 실행할 프로그램을
            추가합니다.</li>
          <li>[삭제]: 예약 프로그램
            목록에서 예약 프로그램을
            삭제합니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* \[프로그램 예약실행\] 항목은 응용 기능 중 센서 동기 기능의 동기 상태를 컨베이어 또는 프레스로 설정한 경우에만 활성화됩니다.
* \[프로그램 예약실행\] 항목은 \[설정 &gt; 2: 제어 파라미터 &gt; 8: 프로그램 예약실행\] 메뉴에서 \[적용 레지스터 개수\] 옵션이 무효로 설정되어 있으면 활성화되지 않습니다.
* 프로그램 예약 실행에 대한 자세한 내용은 별도의 “Hi6 제어기 프로그램 예약 실행 기능 설명서”를 참조하십시오.
{% endhint %}

# 7. 설정

설정 항목에서는 사용자의 정보와 각종 파라미터 정보 등을 확인 및 설정할 수 있습니다.

# 7.1 설정 메뉴 사용

1.	수동 또는 자동 모드에서 초기 화면 우측의 \[설정\] 버튼을 터치하십시오. 프로그램의 설정 메뉴가 표시됩니다.

![](../_assets/bt-setup.png)

2.	원하는 메뉴를 선택하여 사용자의 정보와 각종 파라미터 정보를 확인 및 설정하십시오.

![](../_assets/image_184.png)

* \[1: 사용자 환경\]: 각종 사용자 조건을 확인하고 설정합니다.
* \[2: 제어 파라미터\]: 제어기의 각종 조건을 설정하고 입출력 신호, 통신 정보, 로봇 준비 OK 신호 조건, 원위치 신호 및 좌표계를 설정합니다.
* \[3: 로봇 파라미터\]: 로봇 동작과 관련된 각종 데이터와 축별 원점, 동작 범위 등의 정보를 설정합니다.
* \[4: 응용 파라미터\]: 로봇의 응용 기능을 사용하기 위한 각종 파라미터를 확인하고 설정합니다.
* \[5: 초기화\]: 로봇 시스템의 초기화를 수행합니다. 또한 시리얼 엔코더를 초기화할 수 있습니다.
* \[6: 자동 캘리브레이션\]: 로봇을 올바로 사용하기 위해 교시된 프로그램 및 자동으로 동작하는 움직임을 이용하여 로봇의 축 원점, 툴 길이, 부하 질량, 베이스축 방향 등을 캘리브레이션합니다.



# 7.2 사용자 환경

각종 사용자 조건을 확인하고 설정합니다.

1.	\[1: 사용자 환경\] 메뉴를 터치하십시오. 사용자 환경 설정창이 나타납니다.

2.	사용자 환경을 설정한 후 \[OK\] 버튼을 터치하십시오.

![](../_assets/image_193.png)

* \[1: Pose 기록 형태\]: 숨은 포즈로 기록되는 스텝의 위치 기록 형태를 설정합니다.
  * \[베이스\]/\[로봇\]/\[축각도\]: 베이스 좌표, 로봇, 축각도 값을 기준으로 스텝의 위치를 기록합니다
  * \[U\]: 사용자 좌표계에서의 위치를 기록합니다.
* \[2: 명령어 삭제시 확인\]: 수동 모드에서 명령문 삭제 시 삭제 확인창의 노출 여부를 설정합니다.
* \[3: WAIT\(DI/WI\) 강제해제\]: 입력 신호 대기 또는 용접 완료 신호 대기에서 &lt;shift+F3: WAIT 해제&gt; 키를 이용해 신호 대기 상태의 강제 해제 여부를 설정합니다.
* \[4: 프로그램 스트로브신호 사용\]: 외부 디지털 신호를 수신하여 외부 프로그램 선택 시 외부 프로그램이 선택되는 시점을 설정합니다.
  * \[무효\]: 외부 프로그램 선택 신호만을 읽어 들여 외부 프로그램을 선택합니다.
  * \[유효\]: 프로그램 스트로브가 입력되는 시점에 외부 프로그램 선택 신호를 읽어 들여 외부 프로그램을 선택합니다.



* \[5: 재생 프로그램의 외부갱신\]: 재생 중인 프로그램을 외부\(PC\)에서 수정하여 제어기로 다운로드하는 것의 허용 여부를 설정합니다. \(재생 중인 프로그램 번호에 대해 새로 다운로드된 프로그램은 다음 사이클부터 적용됩니다.\)

{% hint style="warning" %}
재생 중인 프로그램을 외부\(PC\)에서 수정하여 제어기로 다운로드하면 제품이 고장 나거나 성능에 이상이 발생할 수 있습니다. 고객지원팀에 문의하여 전문가에게 의뢰하거나 엔지니어에게 문의하십시오.
{% endhint %}

* \[6: 충돌센서\]: 충돌 센서 동작 시 로봇을 정지시키는 방법을 설정합니다.
  * \[\(1\) 센서처리\]: 충돌 센서가 동작하면 로봇을 비상 정지\(운전 준비 OFF \(모터 OFF\) 상태\)하거나 정지\(운전 준비 ON \(모터 ON\) 상태\)시킵니다.
  * \[\(2\) 신호논리\]: 충돌 센서의 입력 신호 논리를 정논리 또는 부논리로 설정합니다.

{% hint style="info" %}
* 충돌 센서 작동으로 모터가 꺼진 상태에서 \[설정\] 메뉴에 진입하면 모터 ON 및 조그 동작이 가능합니다. 이를 이용하여 충돌한 로봇을 이동시킬 수 있습니다.
* \[센서처리\]가 정지로 설정된 상태에서 충돌 센서가 동작하면 로봇은 조그 동작만 가능합니다.
{% endhint %}

* \[7: cpo\( \) 좌표계\]: 작업 프로그램에서 로봇의 현재 위치를 얻는 포즈식\(cpo\(\)\)을 사용할 때 구해지는 포즈의 좌표계의 기준을 설정합니다.
* \[8: cpo\( \) 선택\]: 작업 프로그램에서 지정한 좌표계\(U/Base/Joint\)를 기준으로 로봇의 현재 위치를 얻는 포즈식\(cpo\(\)\)을 사용할 때 구해지는 현재 위치값의 유형을 설정합니다. 지령값\(로봇의 지령치\(cmd\)\) 또는 현재값\(로봇의 현재치\(cur\)\)을 선택할 수 있습니다.



{% hint style="warning" %}
로봇의 현재치는 서보 지연에 의해 지령치와 오차가 발생할 수 있습니다. 사용 환경과 목적에 맞게 현재 위치값의 유형을 설정하십시오.
{% endhint %}

* \[9: 정지신호 입력시 수동조작\]: 외부 정지 신호 입력 시 조그 동작의 가능 여부를 설정합니다.

# 7.3    제어 파라미터

제어기의 각종 조건을 설정하고 입출력 신호, 통신 정보, 로봇 준비 OK 신호 조건, 원위치 신호 및 좌표계를 설정합니다.

1.	\[2: 제어 파라미터\] 메뉴를 터치하십시오. 제어 파라미터 메뉴가 나타납니다.

2.	원하는 메뉴를 선택하여 제어기의 각종 조건을 확인 및 설정하십시오.

![](../../_assets/image_190.png)

# 7.3.1 제어 환경 설정

제어기의 각종 조건을 설정하여 필요한 작업을 수행합니다.

1.	\[2: 제어 파라미터 &gt; 1: 제어 환경 설정\] 메뉴를 터치하십시오.

2.	제어기의 제어 환경 조건을 설정한 후 \[OK\] 버튼을 터치하십시오.

![](../../_assets/image_180.png)

* \[1: 절전기능\]: 절전 기능의 사용 여부와 대기 시간을 설정합니다.

절전 기능을 사용 설정하면, 자동 모드에서 로봇이 기동 대기, 입력 신호 대기 등의 장시간 동안 운전 정지 상태에 있는 경우 대기 시간이 경과하면 모터의 전원 공급을 차단하여 소비 전력을 절약합니다. 로봇에 운전 명령이 입력되면 자동적으로 절전 기능이 해제되어 모터에 전원을 공급하고 로봇이 동작합니다.

{% hint style="info" %}
절전 기능이 활성화/비활성화되는 과정에서 지연 요소가 발생할 수 있습니다. 로봇의 속도를 예상하여 작업하는 경우에는 절전 기능을 무효로 설정하여 작업하십시오.
{% endhint %}

* \[2: 자동모드에서 경로복구\]: 자동 모드에서 경로 복구 시의 허용 거리와 허용 각도를 설정합니다. 경로 복구 시 거리 및 각도가 설정된 허용 범위 이상인 경우 에러를 검출합니다. 허용 거리를 -1로 설정하면 경로를 복구하지 않습니다.



# 7.3.2 입출력 신호 설정

1.	\[2: 제어 파라미터 &gt; 2: 입출력 신호 설정\] 메뉴를 터치하십시오. 입출력 신호 설정 메뉴가 나타납니다.

2.	원하는 메뉴를 선택하여 입출력 신호의 속성, 신호 할당 등을 설정하십시오.

![](../../../_assets/image_188.png)

# 7.3.2.1 입력 신호 속성

범용 입력 신호에 대한 신호의 논리와 명칭을 설정합니다.

1.	\[2: 제어 파라미터 &gt; 2: 입출력 신호 설정 &gt; 1: 입력 신호 속성\] 메뉴를 터치하십시오.

2.	범용 입력 신호 목록을 확인하고 설정한 후 \[OK\] 버튼을 터치하십시오.

![](../../../_assets/image_185.png)

* \[추가\]: 목록에 새로운 범용 입력 신호를 추가합니다.
* \[삭제하기\]: 목록에서 범용 입력 신호를 삭제합니다.



# 7.3.2.2 출력 신호 속성

범용 출력 신호에 대한 신호의 논리와 펄스 속성, 명칭을 설정합니다.

1.	\[2: 제어 파라미터 &gt; 2: 입출력 신호 설정 &gt; 2: 출력 신호 속성\] 메뉴를 터치하십시오.

2.	범용 출력 신호 목록을 확인하고 설정한 후 \[OK\] 버튼을 터치하십시오.

![](../../../_assets/image_192.png)

* \[추가\]: 목록에 새로운 범용 출력 신호를 추가합니다.
* \[삭제하기\]: 목록에서 범용 출력 신호를 삭제합니다.



# 7.3.2.3    입출력 신호 설정 정보

* \[신호\]: 속성을 적용할 신호입니다. fb 블록의 신호는 블록 번호와 소수점, 신호 번호의 순으로 입력하여 지정합니다. 예를 들어, fb1 블록의 35번 신호를 지정하려면 1.35를 입력하여 설정할 수 있습니다.
* \[부논리\]: 범용 입출력 신호의 정논리와 부논리는 다음과 같습니다.

![](../../../_assets/image_186.png)

* \[펄스 횟수\]: 펄스 횟수입니다. 1 ~ 100 사이의 값으로 설정하면 펄스 출력하고 0으로 설정하면 지연 출력합니다.
* \[펄스ON\]/\[펄스OFF\]: 펄스 출력 또는 지연 출력 시, 출력 신호의 On 시간과 Off 시간입니다. 펄스 속성값에 따른 펄스 출력 예는 다음과 같습니다.
* 펄스 출력 - 횟수: 3, ON 시간: 1 초, OFF 시간; 0.2 초

![](../../../_assets/image_189.png)



* 지연 출력 - 횟수: 0, ON 시간: 1 초, OFF 시간; 0.5 초



![](../../../_assets/image_183.png)

* \[명칭\]: 범용 입출력 신호의 명칭입니다.



# 7.3.2.4 입력 신호 할당

제어기 입력 신호를 이용해 제어기의 상태나 동작을 원격으로 제어할 수 있습니다. 원격 제어 항목에 입력 신호 번호를 할당하는 방법은 다음과 같습니다.

1.	\[2: 제어 파라미터 &gt; 2: 입출력 신호 설정 &gt; 3: 입력 신호 할당\] 메뉴를 터치하십시오.

2.	원격 제어 항목에 입력 신호 번호를 입력한 후 \[OK\] 버튼을 터치하십시오.

![](../../../_assets/image_187.png)

* \[ALL 초기화\]: 모든 원격 제어 항목에 할당된 입력 신호의 번호를 초기화합니다.
* \[ONE 초기화\]: 선택된 원격 제어 항목에 할당된 입력 신호의 번호를 초기화합니다.
* \[채널 초기화\]: 설정한 입력 신호의 입력 채널을 초기화합니다. 채널은 fb0 ~ fb9로 구성되며, fb0인 경우 fb0가 생략되어 표시됩니다.
* \[S\]: 원격 제어를 시스템 입력 신호로 사용할 경우, 시스템 신호를 지정합니다. 시스템 신호는 알파벳 s에 신호 번호를 조합하여 “s+숫자”로 구성됩니다. 예를 들어, 시스템 신호 49는 s49로 설정합니다.



# 7.3.2.5 입력 신호 설정 정보

* 원격\(Remote\) 모드

티치 펜던트의 모드 스위치가 원격\(![](../../../_assets/sb-remote.png)\)으로 선택된 상태에서 원격 모드로 선택되기 위해서는 해당 신호가 on 되어야 합니다. 해당 신호가 off되면 내부 모드로 선택됩니다. 일반적으로 티치 펜던트의 모드 스위치를 원격\(![](../../../_assets/sb-remote.png)\)으로 선택하면 사용자는 원격 모드로 선택되기를 원하기 때문에 기본값은 254로 지정하였고 입력 신호 속성에 해당 신호는 부논리로 지정됩니다.

* 수동\(Teach\) 모드

원격 모드로 선택된 상태에서 해당 신호가 on되면 원격에서 수동으로 로봇을 조작하는 상태가 됩니다. 그런데 일반적으로 이 상태에서 로봇을 조작하는 경우는 없으므로 거의 사용하지 않습니다.

* 자동\(Playback\) 모드

원격 모드로 선택된 상태에서 해당 신호가 on되면 원격에서 자동으로 로봇을 조작하는 상태가 됩니다. 그런데 일반적으로 사용자는 티치펜던트의 모드 스위치를 원격\(![](../../../_assets/sb-remote.png)\)으로 선택하면 원격에서 자동으로 로봇을 조작하기를 원하기 때문에 기본값은 255로 지정하였고 신호 속성에 해당 신호는 부논리로 지정됩니다.

* 외부 기동

원격 자동 모드에서 로봇을 기동\(start\)하기 위해 사용합니다.

* 외부 정지

원격 자동 모드에서 로봇을 정지\(stop\)하기 위해 사용합니다.

* 외부 프로그램 선택

외부에서 기동 동작 시 프로그램 선택 Bit를 읽어 외부 프로그램으로 확정하는 시점은 프로그램 스트로브\(Strobe\) 신호의 사용 여부에 따라 달라집니다.

* 프로그램 스트로브 신호 사용이 유효인 경우: 외부 기동 입력 시 프로그램 스트포브 신호가 On이면 프로그램 선택 Bit를 읽고, 이 값을 프로그램 번호로 확정합니다.  

![그림 52 프로그램 스트로브신호 &amp;lt;유효&amp;gt; 시 외부 프로그램 선택 선도](../../../_assets/io-signal-strobe1.png)

* 프로그램 스트로브 신호 사용이 무효인 경우: 외부 기동 입력 후 프로그램 선택 Bit를 읽고, 이 값이 90 ms 동안 변경되지 않는 경우에 프로그램 번호로 확정합니다.

![그림 53 프로그램 스트로브신호 &amp;lt;무효&amp;gt; 시 외부 프로그램 선택 선도](../../../_assets/io-signal-strobe2.png)

* 프로그램 선택 Bit와 Binary/Discrete \(OFF→Binary\)

프로그램 선택Bit는 외부 기동 신호가 입력되었을 때, 실행할 프로그램을 선택하기 위한 신호 조합입니다. 현재 TP에서 프로그램 HEADER 혹은 END에 커서가 있을 때에만 적용되며, 프로그램 수행 중에는 수행 중인 프로그램을 끝까지 수행하게 됩니다. Binary/Discrete 신호는 프로그램 선택 Bit의 해석을 결정해주는 옵션이며, 0인 경우 Binary로 인식하고, 1인 경우에는 Discrete로 인식합니다. 예를 들어, 프로그램 선택 Bit가 다음과 같이 설정된 경우, 입력에 따른 수행 JOB 예는 다음과 같습니다.

![](../../../_assets/image_181.png)

* 외부 RESET

외부 신호에 의해 티치 펜던트에서 R0 스텝 카운터 리셋 기능을 실행한 것과 동일하게 동작하기 위해 사용합니다. 로봇이 기동 중인 경우에는 이 기능이 동작하지 않으며, 이 기능이 정상적으로 동작하면 프로그램의 처음으로 실행 위치를 이동하고 각종 에러나 경고의 발생 상태를 클리어합니다. 이 기능에 대한 내용은 “[8.2 R0 스텝 카운터 리셋](../../../r-code/r0.md)”을 참조하십시오.

* 저속 지령

외부 신호에 의해 로봇의 이동 속도를 안전 속도\(250mm/s\) 이내로 제한하기 위해 사용합니다.

* 충돌 센서

로봇의 충돌을 검지하고 로봇을 정지하기 위해 사용합니다. \[시스템 &gt; 1: 사용자 환경 &gt; 6: 충돌센서\] 메뉴의 설정과 연계하여 로봇을 정지할 때 조건과 신호의 논리가 결정됩니다.

* 에러/경보 신호 클리어

외부 신호에 의해 각종 에러나 경고의 발생 상태를 클리어합니다.

* 조이스틱 모드

로봇을 수동으로 조그하기 위해 사용합니다. 일반적으로 LCD 매크로 검사 장비에서 사용되며 사용을 위해서는 별도의 기능 설명서를 참고하시기 바랍니다.

* 도어 스위치

안전 펜스의 도어가 개방되었을 때 이동 중인 로봇을 정지하기 위해 사용합니다.

* 화면보호 해제

티치 펜던트를 조작하지 않으면 \[메뉴 &gt; 11: 티치 펜던트 옵션\] 메뉴에서 설정한 화면꺼짐 시간이 경과되면 티치 펜던트가 화면보호 상태로 전환됩니다. 외부 신호에 의해 티치 펜던트의 화면을 켜기 위해 사용합니다.

* 외부 모터 on

외부 조작 패널에서 모터 on을 수행하기 위해 사용합니다.

* 외부 모터 off

외부 조작 패널에서 모터 off를 수행하기 위해 사용합니다.

# 7.3.2.6 출력 신호 할당

제어기 출력 신호를 이용해 제어기에 발생한 이벤트 정보나 상태 정보를 외부로 전달할 수 있습니다. 외부로 전달할 정보에 출력 신호를 할당하는 방법은 다음과 같습니다.

1.	\[2: 제어 파라미터 &gt; 2: 입출력 신호 설정 &gt; 4: 출력신호 할당\] 메뉴를 터치하십시오.

2.	정보 항목에 출력 신호 번호를 입력한 후 \[OK\] 버튼을 터치하십시오.

![](../../../_assets/image_182.png)

* \[ALL 초기화\]: 모든 정보 항목에 할당된 출력 신호의 번호를 초기화합니다.
* \[ONE 초기화\]: 선택된 정보 항목에 할당된 출력 신호의 번호를 초기화합니다.
* \[채널 초기화\]: 설정한 출력 신호의 입력 채널을 초기화합니다. 채널은 fb0 ~ fb9로 구성되며, fb0인 경우 fb0가 생략되어 표시됩니다.
* \[이전 태스크\]/\[다음 태스크\]: 이전 또는 다음 태스크 화면으로 이동합니다.
* \[S\]: 원격 제어를 시스템 입력 신호로 사용할 경우, 시스템 신호를 지정합니다. 시스템 신호는 알파벳 s에 신호 번호를 조합하여 “s+숫자”로 구성됩니다. 예를 들어, 시스템 신호 49는 s49로 설정합니다.



# 7.3.2.7 출력 신호 설정 정보

* 원격\(Remote\) 모드

티치 펜던트의 모드 스위치가 원격\(![](../../../_assets/sb-remote.png)\)으로 선택된 상태로 입력 신호 할당에서 원격 모드에 설정된 신호가 on으로 입력되었을 때 비로소 원격 모드 상태가 됩니다. 이 상태를 외부로 출력하고자 할 때 사용합니다.

* 수동\(Teach\) 모드

제어기의 조작 모드가 수동 모드인 상태를 외부로 출력하고자 할 때 사용합니다.

* 자동\(Playback\) 모드

제어기의 조작 모드가 자동 모드인 상태를 외부로 출력하고자 할 때 사용합니다.

* 모터 ON

MOTOR ON 입력에 의해 각각의 모터에 전원이 공급되고 구동할 준비가 되었을 때 이 상태를 외부로 출력하고자 할 때 사용합니다.

* 로봇 준비 OK

현재 제어기의 상태가 \[설정 &gt; 2: 제어 파라미터 &gt; 4: 로봇 준비 조건\] 메뉴에서 설정된 조건이 모두 만족할 때 이 상태를 외부로 출력하고자 할 때 사용합니다.

* 기동 중

수동 모드에서 스텝 전후진 동작이나 자동 모드에서 기동 입력에 의해 로봇이 기동할 때 이 상태를 외부로 출력하고자 할 때 사용합니다.

* 로봇 동작 중\(Moving\)

로봇이 이동 중일 때 이 상태를 외부로 출력하고자 할 때 사용합니다.

* 일시 정지 중\(Hold\)

기동 중 신호의 출력과 상반되게 로봇이 정지 중일 때 이 상태를 외부로 출력하고자 할 때 사용합니다.

* 비상 정지 중

티치 펜던트 또는 제어기 전면에 장착된 비상 정지 버튼이 입력된 상태를 외부로 출력하고자 할 때 사용합니다.

* 비상 정지 중\(외부\)

시스템 보드와 연결된 외부 비상 정지가 입력된 상태를 외부로 출력하고자 할 때 사용합니다

* 저속 모드 중

입력 신호 할당에서 저속 지령에 설정된 신호가 on인 경우나 수동 모드에서는 로봇이 안전 속도에서 동작하며 이 상태를 외부로 출력하고자 할 때 사용합니다.

* 프로그램 END

작업 프로그램에서 사이클 END가 수행되면 이 상태를 외부로 출력하고자 할 때 사용합니다.

* 종합 이상

제어기에서 발생되는 에러는 시스템 오류에 의해 발생하는 에러와 사용자의 조작 실수에 의해 발생하는 에러로 구분됩니다. 시스템 오류에 의해 에러가 발생할 때 이 상태를 외부로 출력하고자 할 때 사용합니다. 시스템 오류에 의해 발생하는 에러는 1 ~ 999와 2000 ~ 7999 이내에 해당합니다.

* 조작 에러

제어기에서 발생되는 에러는 시스템 오류에 의해 발생하는 에러와 사용자의 조작 실수에 의해 발생하는 에러로 구분됩니다. 사용자의 조작 실수에 의해 에러가 발생할 때 이 상태를 외부로 출력하고자 할 때 사용합니다. 참고로 시스템 오류에 의해 발생하는 에러는 1 ~ 999와 2000 ~ 7999 이내에 해당합니다.

* 경고 발생

제어기에서 경고가 발생하면 이 상태를 외부로 출력하고자 할 때 사용합니다.

* 충돌 센서

입력 신호 할당에 설정된 충돌 센서 입력이 on되어 로봇에 충돌이 발생되었을 때 이 상태를 외부로 출력하고자 할 때 사용합니다.

* 스텝 SET 경보

자동 모드에서 현재 선택된 커서의 위치가 이전에 실행했던 위치와 다른 경우는 위험할 수 있으므로 이 상태를 외부로 출력하고자 할 때 사용합니다.

* 인터록 이상

작업 프로그램의 WAIT 명령문에서 대기한 시간이 \[시스템 &gt; 2: 제어 파리미터 &gt; 1: 제어 환경 설정\] 메뉴의 \[인터록 이상 시간\] 옵션에 설정된 시간을 초과하면 이 상태를 외부로 출력하고자 할 때 사용합니다.

* 에러/경고 출력 Bit, 에러/경고 출력 선택, 에러/경고 출력 STRB

에러/경고 출력 Bit, 에러/경고 출력 STRB, 종합 이상, 조작 에러, 경고 발생 신호는 다음의 시퀀스를 참조하십시오.

![그림 54 16비트 출력](../../../_assets/image_550.png)

* 외부 RESET ACK

입력 신호 할당에 설정된 외부 RESET 신호가 on되면 이 상태를 외부로 출력하고자 할 때 사용합니다. 이 신호는 200ms동안 on된 후 자동으로 off됩니다.

* 프로그램 에코 Bit

입력 신호 할당에 설정된 프로그램 선택 Bit에 의해 프로그램이 선택되었을 때 선택된 프로그램 번호를 외부로 출력하고자 할 때 사용합니다.

* 프로그램 ACK

원격 모드에서 외부 기동 입력에 의해 로봇이 기동할 때 이 상태를 외부로 출력하고자 할 때 사용합니다. 이 신호는 200ms동안 on된 후 자동으로 off됩니다.

* 아크 용접 이상

아크 용접과 관련하여 에러가 발생한 경우에 이 상태를 외부로 출력하고자 할 때 사용합니다.

* 아크 용착 경보

아크 용접 중 용착이 발생한 경우에 이 상태를 외부로 출력하고자 할 때 사용합니다. 이 신호는 200ms동안 on된 후 자동으로 off됩니다.

* 로봇락 상태\(유효=ON\)

\[조건설정\]에서 로봇 Lock 설정 상태를 외부로 출력하고자 할 때 사용합니다.

* 필드버스 이상, 필드버스 IDLE

CC-LINK, 디바이스넷 등의 필드 버스 통신 보드를 사용할 때 통신의 상태를 외부로 출력하고자 할 때 사용합니다.

* 배터리\(백업, 엔코더\) 전압저하

메인 보드에 장착된 SRAM 상태를 유지하기 위한 백업 배터리나 각각의 모터에 장착된 엔코더 값을 유지하기 위한 엔코더 배터리에 전압 저하가 발생한 상태를 외부로 출력하고자 할 때 사용합니다.

* 토크모니터링

로봇 6축에 인가되는 토크값을 외부로 출력하고자 할 때 사용합니다. 외부로 출력되는 토크값은 1/2 배율의 % 값입니다.

* 그리스 주유 알람

그리스 주유가 필요한 상태를 외부로 출력하고자 할 때 사용합니다.

* 평균 부하율 이상 알람

로봇이 작업 중 평균치 부하율을 초과하였는지 상태를 외부로 출력하고자 할 때 사용합니다.

# 7.3.2.8 키 신호 출력

원하는 출력 신호를 키 신호 출력 기능 영역의 버튼에 할당하여 간단히 출력 신호를 켜거나 끄도록 설정할 수 있습니다.

1. \[2: 제어 파라미터 &gt; 2: 입출력 신호 설정 &gt; 5: 키 신호 출력\] 메뉴를 터치하십시오.
2. 버튼에 표시할 기능 이름과 옵션을 설정한 후 \[확인\] 버튼을 터치하십시오.

![](../../../_assets/image_45.png)

* \[fb\] / \[do\]: 숫자와 소수점만으로 신호 출력 변수값을 간단히 입력합니다.

예를 들어, 2.9를 입력한 후 &lt;enter&gt; 키를 누르십시오. fb2.do9로 변환되어 나타납니다. 소수점 없이 9를 입력하고 &lt;enter&gt; 키를 누르면 do9로 변환됩니다.

{% hint style="info" %}
Hi6 티치 펜던트의 사용자키 영역에서도 원하는 출력 신호를 버튼에 등록할 수 있습니다. 자세한 내용은 “2.6.2.1 키 신호 출력 기능 영역”를 참조하세요.
{% endhint %}

# 7.3.2.9 DIO 블록 할당

제어기의 범용 입출력 신호를 사용하는 방법을 설정합니다. 사용 안함\(None\), PLC, Fieldbus에 연결하여 사용할 수 있습니다.

1.	\[2: 제어 파라미터 &gt; 2: 입출력 신호 설정 &gt; 6: DIO 블록 할당\] 메뉴를 터치하십시오.

2.	선택된 FB 주소의 DIO 블록을 연결 설정한 후 \[OK\] 버튼을 터치하십시오.

![](../../../_assets/image_45.png)

* \[None\]: 선택된 FB 주소의 DIO 블록을 할당하지 않습니다. 제어기의 초기 설정값으로 아무것도 선택하지 않을 경우 None으로 설정됩니다.
* \[PLC\]: 선택된 FB 주소의 DIO 블록을 PLC로 연결하여 사용합니다. PLC 동작은 MULTIPROG 프로그램을 이용합니다.
* \[Fieldbus\]: 선택된 FB 주소의 DIO 블록을 PCI 통신 카드\(Fieldbus\)로 연결하여 사용합니다. DIO 블록을 PCI 통신 카드로 연결할 경우 PCI 보드 선택창이 활성화됩니다.

{% hint style="info" %}
\[PLC\]와 \[Fieldbus\]를 동시에 사용하는 경우. Multiprog 프로그램과 \[Fieldbus\]의 슬롯번호가 중복되지 않도록 유의하여 주시기 바랍니다.
{% endhint %}



# 7.3.2.10    복수 신호 출력

출력 신호\(최대 16개\)를 하나의 그룹으로 생성하여 데이터를 각각의 신호로 출력할 수 있습니다.

데이터는 바이너리 포맷으로 출력의 on 또는 off를 결정합니다. 예를 들어, 다음 화면에서 do41과 do43을 출력하기 위한 데이터는 바이너리로 0101 \(십진수 5\)입니다.

1. \[2: 제어 파라미터 &gt; 2: 입출력 신호 설정 &gt; 7: 복수 신호 출력\] 메뉴를 터치하십시오.
2. 출력 신호 그룹의 이름과 신호, 스트로브를 설정하십시오.

![](../../../_assets/image_47.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>출력 신호 그룹 목록에서
          선택한 그룹의 상세 정보입니다.
          그룹 이름과 설명, 신호
          및 스트로브를 설정할
          수 있습니다.</p>
        <ul>
          <li>[ALL 초기화]/[ONE 초기화]: 모든
            신호 또는 선택된 신호의
            설정값을 -1로 초기화합니다.</li>
          <li>[채널 초기화]: 설정된
            신호의 출력 채널을 초기화합니다(0
            ~ 9: 디지털 신호).</li>
          <li>[범위 지정]: 시작 신호와
            종료 신호를 지정하여
            신호를 빠르게 설정합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[+]/[-]: 새로운 출력 신호 그룹을
            추가하거나 출력 신호
            그룹을 삭제합니다.</li>
          <li>출력 신호 그룹 목록입니다.
            그룹 이름을 선택하면
            상세 정보를 확인 및 편집할
            수 있습니다.</li>
          <li>[페이지 복사]/[페이지
            붙여넣기]: 출력 신호 그룹
            정보를 복사하여 다른
            그룹에 붙여 넣습니다.</li>
        </ul>
        <p>목록에서 복사할 그룹의
          이름을 선택하고 [페이지
          복사] 버튼을 터치한 후
          값을 적용할 그룹의 이름을
          선택하고 [페이지 붙여넣기]
          버튼을 터치하십시오.</p>
      </td>
    </tr>
  </tbody>
</table>

예를 들어, 위의 화면의 설정과 같이 구성된 작업 프로그램이 실행되면 다음과 같이 동작합니다.

![그림 55 작업 프로그램 실행 예](../../../_assets/image_58.png)

S1에서 S2로 출발하여 S2의 accuracy ok가 되었을 때 지정된 그룹의 신호와 함께 스트로브 신호를 출력합니다. 200 ms 경과 후 스트로브 신호는 off 됩니다. \(스트로브 신호는 200 ms의 펄스 신호\)

# 7.3.2.11    복수 신호 입력

입력 신호\(최대 16개\)를 하나의 그룹으로 생성하여 각각의 신호 입력으로 데이터를 얻을 수 있습니다.

데이터는 바이너리 포맷으로 입력의 on 또는 off에 따라 결정됩니다. 예를 들어, 다음 화면에서 di41과 di43이 on이고 이외의 모든 신호가 off일 경우 데이터는 0101 \(십진수 5\)입니다.

1. \[2: 제어 파라미터 &gt; 2: 입출력 신호 설정 &gt; 8: 복수 신호 입력\] 메뉴를 터치하십시오.
2. 입력 신호 그룹의 이름과 신호를 설정하십시오.

![](../../../_assets/image_46.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>입력 신호 그룹 목록에서
          선택한 그룹의 상세 정보입니다.
          그룹 이름과 설명, 신호를
          설정할 수 있습니다.</p>
        <ul>
          <li>[ALL 초기화]/[ONE 초기화]: 모든
            신호 또는 선택된 신호의
            설정값을 -1로 초기화합니다.</li>
          <li>[채널 초기화]: 설정된
            신호의 입력 채널을 초기화합니다(0
            ~ 9: 디지털 신호).</li>
          <li>[범위 지정]: 시작 신호와
            종료 신호를 지정하여
            신호를 빠르게 설정합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[+]/[-]: 새로운 입력 신호 그룹을
            추가하거나 입력 신호
            그룹을 삭제합니다.</li>
          <li>입력 신호 그룹 목록입니다.
            그룹 이름을 선택하면
            상세 정보를 확인 및 편집할
            수 있습니다.</li>
          <li>[페이지 복사]/[페이지
            붙여넣기]: 입력 신호 그룹
            정보를 복사하여 다른
            그룹에 붙여 넣습니다.
            <br
            />목록에서 복사할 그룹의
            이름을 선택하고 [페이지
            복사] 버튼을 터치한 후
            값을 적용할 그룹의 이름을
            선택하고 [페이지 붙여넣기]
            버튼을 터치하십시오.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

예를 들어, 위의 화면의 설정과 같이 구성된 작업 프로그램이 실행되면 다음과 같이 동작합니다.

![그림 56 작업 프로그램 실행 예](../../../_assets/image_50.png)

S1에서 S2로 출발한 후 wait 명령문을 실행합니다. S2의 accuracy ok가 되기 이전에 wait 조건이 만족하면 빨간색 경로로 로봇이 이동하지만 그렇지 않는 경우 S2 위치에서 wait 조건이 만족할 때까지 계속 대기합니다.

# 7.3.3 시리얼 포트

시리얼 포트 통신에 필요한 정보를 설정합니다.

1. \[2: 제어 파라미터 &gt; 3: 시리얼 포트\] 메뉴를 터치하십시오.
2. 시리얼 포트별 파라미터를 설정하십시오.

![](../../_assets/image_204.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">시리얼 포트 목록에서
        선택한 포트의 상세 정보입니다.
        포트 이름과 파라미터
        값을 설정할 수 있습니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[+]/[-]: 새로운 시리얼 포트를
            추가하거나 시리얼 포트를
            삭제합니다.</li>
          <li>시리얼 포트 목록입니다.
            포트 이름을 선택하면
            상세 정보를 확인 및 편집할
            수 있습니다.</li>
          <li>[페이지 복사]/[페이지
            붙여넣기]: 시리얼 포트
            정보를 복사하여 다른
            포트에 붙여 넣습니다.
            <br
            />목록에서 복사할 포트
            정보의 이름을 선택하고
            [페이지 복사] 버튼을 터치한
            후 값을 적용할 포트의
            이름을 선택하고 [페이지
            붙여넣기] 버튼을 터치하십시오.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
다음의 정보를 참고하여 시리얼 포트의 용도를 설정하십시오.

* Sensor: 비전 센서와 접속하여 시프트 데이터 수신
* LVS: 용접선 추종을 위한 레이저 비전 센서 연결
* MODBUS: Hi6 제어기의 MODBUS 슬레이브 기능 사용
{% endhint %}

# 7.3.4 로봇 준비 조건

로봇의 준비 완료 시 \[설정 &gt; 2: 제어 파라미터 &gt; 2: 입출력 신호 설정 &gt; 4: 출력신호 할당\]의 \[로봇 준비 OK\] 항목의 신호 출력을 위한 조건을 설정합니다.

1.	\[2: 제어 파라미터 &gt; 4: 로봇 준비 조건\] 메뉴를 터치하십시오.

2.	로봇 준비 조건을 설정한 후 \[OK\] 버튼을 터치하십시오.

![](../../_assets/image_88.png)

# 7.3.5 원위치 등록

로봇의 임의 자세를 원위치로 등록하여 로봇이 이 위치에 들어왔을 때 원위치 신호를 출력 신호란에 출력할 수 있습니다. 원위치는 축별 자세로 지정하고 8 개까지 등록하여 사용할 수 있으며 축별 마진을 추가로 설정할 수 있습니다.

1. \[2: 제어 파라미터 &gt; 5: 원위치 등록\] 메뉴를 터치하십시오.
2. 원위치 탭을 선택하고 사용 여부와 출력 신호, 축각도와 범위를 설정하십시오.

![](../../_assets/image_124.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>탭에서 선택한 원위치의
          상세 정보입니다. 사용
          여부와 출력 신호, 축각도와
          범위, 설명을 설정할 수
          있습니다.</p>
        <ul>
          <li>[사용 여부]: 사용 여부를
            설정합니다.</li>
          <li>[출력 신호]: 출력 신호
            번호를 입력합니다.</li>
          <li>[축각도]/[범위]: 원위치에서
            로봇의 축각도와 범위를
            입력합니다.</li>
          <li>범위가 0으로 설정된 경우,
            해당 축에 대해서는 원위치
            검사를 수행하지 않습니다.</li>
          <li>범위는 원위치 포인트의
            + 방향과 - 방향의 범위로
            사용합니다. 예를 들어,
            범위를 0.5로 설정하면 원위치
            신호의 출력 범위는 1이
            됩니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[현재 로봇 포즈]: 현재
            로봇 자세의 축각도와
            범위가 자동으로 입력됩니다.</li>
          <li>[프로그램/스텝]: 프로그램과
            스텝 번호를 입력하면
            해당 스텝의 축각도와
            범위가 자동으로 입력됩니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

# 7.3.6 좌표계 등록

1.	\[2: 제어 파라미터 &gt; 6: 좌표계 등록\] 메뉴를 터치하십시오. 좌표계 등록 메뉴가 나타납니다.

2.	원하는 메뉴를 선택하여 사용자 좌표계나 정치툴 좌표계에 대한 좌표계를 설정하십시오.

![](../../../_assets/image_179.png)

# 7.3.6.1 사용자 좌표계

사용자 좌표계는 사용자\(User\)가 지정하는 위치에 설정하는 좌표계입니다. 사용자 좌표계를 사용하기 위해 먼저 사용자 좌표계 정의를 위한 3개의 기준 스텝을 티칭한 후 티칭된 프로그램 번호와 사용자 좌표계 번호를 지정하여 사용자 좌표계를 등록합니다.

다음 절차에 따라 3개의 기준 스텝을 티칭하십시오.

![그림 57 사용자 좌표계 정의를 위한 3개의 기준 스텝 티칭 방법](../../../_assets/image_197.png)

1. 사용자 좌표계의 원점 정의: 임의의 한 점을 티칭하십시오.
2. 사용자 좌표계의 X축 정의: 가능한 한 원점과의 거리가 200 ㎜ 이상 떨어진 지점의 X축 선상에 임의의 한 점을 티칭하십시오.
3. 사용자 좌표계의 XY 평면 정의\(Y축과 Z축 방향 결정\): 가능한 한 원점과의 거리가 200 ㎜ 이상 떨어진 지점의 X축과 Y축으로 이루어지는 평면상에 임의의 한 점을 티칭하십시오.

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

1. \[2: 제어 파라미터 &gt; 6: 좌표계 등록 &gt; 1: 사용자 좌표계\] 메뉴를 터치하십시오.
2. 사용자 좌표계 이름과 프로그램 번호, 축별 원점과의 거리 및 각도를 설정하십시오.

![](../../../_assets/image_153.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">사용자 좌표계 목록에서
        선택한 좌표계의 상세
        정보입니다. 좌표계 이름과
        설명, 티칭된 프로그램
        번호, 축별 원점과의 거리
        및 각도를 설정할 수 있습니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[+]/[-]: 새로운 사용자 좌표계를
            추가하거나 사용자 좌표계를
            삭제합니다.</li>
          <li>사용자 좌표계 목록입니다.
            좌표계 이름을 선택하면
            상세 정보를 확인 및 편집할
            수 있습니다.</li>
          <li>[페이지 복사]/[페이지
            붙여넣기]: 사용자 좌표계
            정보를 복사하여 다른
            좌표계에 붙여 넣습니다.
            <br
            />목록에서 복사할 좌표계
            정보의 이름을 선택하고
            [페이지 복사] 버튼을 터치한
            후 값을 적용할 좌표계의
            이름을 선택하고 [페이지
            붙여넣기] 버튼을 터치하십시오.</li>
          <li>[JOB 계산]: 사용자 좌표계를
            정의하기 위해 티칭한
            프로그램을 기반으로
            사용자 좌표계를 계산합니다.
            <br
            />[등록을 위한 프로그램
            번호] 옵션에 티칭한 프로그램의
            번호를 입력한 후 [JOB 계산]
            버튼을 터치하면 사용자
            좌표계의 원점과 각도가
            계산됩니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

# 7.3.6.2 정치툴 좌표계

로봇 툴은 로봇 선단에 부착된 툴입니다. 일반적으로 로봇은 로봇에 부착된 툴을 이용하여 작업을 수행합니다. 대표적인 것으로 아크 용접이 있습니다. 아크 용접 툴은 통상적으로 로봇 선단에 부착되며 외부에 고정되어 있는 작업물에 용접을 수행할 때 사용합니다.

이에 반해서 정치툴\(Stationary Tool\)은 작업하는 툴이 로봇이 아닌 외부에 부착되어 있는 것으로, 이 경우에는 로봇이 작업물을 핸들링하여 외부에 고정된 툴에 위치시킴으로써 작업을 수행하게 됩니다. 정치툴을 이용한 대표적인 작업은 실링 작업입니다. 통상적으로 실링 작업은 외부에 부착된 툴이 실링에 필요한 용제를 일정한 양으로 토출하면 로봇이 작업물을 들고 실링에 필요한 궤적을 생성하여 작업합니다.

![그림 58 실링 작업 예](../../../_assets/image_154.png)

이 궤적을 생성하기 위해 로봇은 자체에 부착된 툴이 아닌 외부에 부착된 툴을 기준으로 직선 \(L\) 및 원호 \(C\) 보간을 수행합니다. 이때 정치툴 보간 기능을 사용합니다.

정치툴 보간 기능을 이용하면 로봇이 취부한 작업물의 자세가 변경되어도 정치툴의 작업물 상의 이동 경로는 직선 및 원호를 유지할 수 있습니다. 이와 같이 외부 툴의 이동 경로가 중요한 작업에는 반드시 정치툴 보간 기능을 이용합니다.

정치툴 보간 기능을 이용하려면 정치툴 좌표계를 반드시 설정해야 합니다.

정치툴 좌표계를 설정하는 방법은 다음과 같습니다.

1. \[2: 제어 파라미터 &gt; 6: 좌표계 등록 &gt; 2: 정치툴 좌표계\] 메뉴를 터치하십시오.
2. 원하는 탭을 선택하고 정치툴 좌표계의 위치를 등록하십시오.

![](../../../_assets/image_200.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">정치툴 좌표계는 탭을
        선택하여 총 4 개(tool 0 ~ tool 3)를
        설정할 수 있습니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[자동설정]: 현재의 TCP 위치를
            정치툴 좌표계의 위치로
            설정합니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

* 현재 TCP 위치를 정치툴 좌표계 위치로 설정

로봇 베이스 좌표계를 기준으로 TCP를 정확히 찾은 후 그림과 같이 정치툴과 로봇툴을 일치시키고 \[자동설정\] 버튼으로 자동 설정 기능을 실행하십시오. 현재의 TCP 위치가 등록됩니다.

![그림 59 \[자동설정\] 버튼을 이용한 티칭 방법](../../../_assets/image_178.png)

* 정치툴 좌표계를 이용한 프로그램 작성

정치툴 보간 스텝으로 기록하려면 스텝을 SL 또는 SC로 기록합니다. Hi6 티치 펜던트 화면 좌측 상단의 \[기록조건\] 버튼을 이용하여 기록 조건을 SL \(정치툴 직선보간\) 또는 SC \(정치툴 원호보간\)로 변경하여 사용할 수 있습니다.

예를 들어, 정치툴 좌표계 1번을 등록하고 사용하는 경우에는 다음과 같이 프로그램을 작성할 수 있습니다.

![](../../../_assets/image_93.png)

{% hint style="info" %}
정치 서보건 사용 시에는 정치툴 보간 기능이 필요하지 않습니다. 서보건 용접에서는 정치 서보건에 대한 작업물의 이동 경로가 직선 혹은 원호로 만들어질 필요가 없고 용접점만 중요하기 때문입니다.
{% endhint %}

# 7.3.7 프로그램 예약 실행

프로그램을 예약 실행하는 방법에 대한 자세한 내용은 “Hi6 제어기 프로그램 예약 실행 기능 설명서”를 참조하십시오.

# 7.3.8 자동 백업 및 복원

제어기의 데이터를 자동으로 백업하고 복원하는 방법에 대한 자세한 내용은 “Hi6 제어기 자동 백업 기능 설명서”를 참조하십시오.

# 7.3.9 산업용 통신 \(필드버스\)

산업용 통신\(필드버스; Fieldbus\)을 사용 설정합니다.

1.	사용할 통신에 따라 “Hi6 제어기 보수 설명서”를 참조하여 PCI 카드 장착 및 슬롯 번호\(1 ~ 4\)를 설정하십시오.

2.	“7.3.9.1 펌웨어 설정”을 참조하여 산업용 통신 펌웨어를 설정하십시오.

3.	제어기의 전원을 끈 후 다시 켜십시오.

4.	필요한 경우, “7.3.9.2 산업용 통신 설정”을 참조하여 부가 설정을 수행하십시오.



# 7.3.9.1 펌웨어 설정

산업용 통신에 사용할 펌웨어를 설정합니다.

1.	\[2: 제어 파라미터 &gt; 11: 산업용 통신 &gt; 1: 펌웨어 설정 &gt; 1 채널\] 메뉴를 터치하십시오. 펌웨어 설정 화면이 나타납니다.

2.	원하는 탭을 선택하고 통신 방식\(Master / Slave\)과 프로토콜을 설정한 후 \[OK\] 버튼을 터치하십시오. 펌웨어 설정이 완료됩니다.

![](../../../_assets/image_454.png)



{% hint style="warning" %}
펌웨어 설정 완료 시 슬롯 1 ~ 4에 설정된 CONGIF 파일이 모두 삭제됩니다. 사용 중 통신 펌웨어를 변경하려면 기존의 CONFIG 설정을 별도로 백업해 두고 필요한 경우 복원하여 사용하십시오.
{% endhint %}

3.	제어기의 전원을 끈 후 다시 켜십시오.

{% hint style="warning" %}
* 펌웨어의 사용 설정 시 제어기의 전원을 끈 후 다시 켜야만 설정값이 시스템에 적용됩니다.
{% endhint %}



# 7.3.9.2 산업용 통신 설정

\(추후 기능 제공\) 통신 방식을 CC-Link 슬레이브로 설정하면, 제어기 내부에서 각 통신별로 상세 정보를 설정할 수 있습니다.

{% hint style="info" %}
통신 정보는 현대로보틱스 인터넷 웹사이트\(www.hyundai-robotics.com\)에서 “Sycon.net” 프로그램을 이용해 설정하십시오.
{% endhint %}

# 7.3.9.3 모니터링

산업용 통신에서 사용 설정된 펌웨어와 통신의 설정 정보 및 동작 상태를 모니터링합니다.

1.	\[메뉴\] 버튼 &gt; \[19: 산업용 통신 모니터링\] 메뉴를 터치하십시오. 보드별 산업용 통신 모니터링 화면이 나타납니다.

2.	원하는 탭을 선택하여 펌웨어, 통신 장치 및 통신 구성의 상세 정보를 확인하십시오.

![](../../../_assets/image_195.png)

{% hint style="info" %}
\[재시작\] 버튼을 이용하여 PCI 통신 카드의 산업용 통신을 다시 시작할 수 있습니다.
{% endhint %}

# 7.4 로봇 파라미터

로봇 동작과 관련된 각종 데이터와 축별 원점, 동작 범위 등의 정보를 설정합니다.

1.	\[3: 로봇 파라미터\] 메뉴를 터치하십시오. 로봇 파라미터 메뉴가 나타납니다.

2.	원하는 메뉴를 선택하여 로봇 본체의 각종 파라미터를 확인하고 설정하십시오.

![](../../_assets/image_205.png)

# 7.4.1 툴 데이터

로봇의 R1축 플랜지\(Flange\)를 기준으로 TCP \(Tool Center Point\)의 거리와 각도를 설정하고, 툴의 중량, 무게 중심과 이너셔를 등록합니다. \[1: 툴 데이터\] 메뉴를 이용해 수동으로 등록할 수 있습니다.

다른 방법으로, 툴 길이는 자동 캘리브레이션 기능을 이용하여 설정할 수 있고, 툴의 중량과 무게 중심, 이셔너는 부하추정 기능을 이용하여 등록할 수 있습니다.

직선 또는 원호와 같은 보간 동작 시에는 TCP 점을 기준으로 궤적을 생성하므로 티칭 작업 전에는 툴의 길이와 각도를 정확하게 설정해야 합니다.

Hi6 제어기는 로봇의 동역학을 기반으로 제어합니다. 툴의 중량과 중심, 이너셔를 정확하게 설정해야 로봇이 빠르고 안전하게 동작할 수 있습니다. 툴의 중량과 중심, 이너셔 값이 정확하지 않거나 틀린 경우, 로봇의 성능과 수명에 심각한 문제가 발생할 수 있습니다.

특히 툴 체인지 기능을 사용하는 경우에는 각 툴에 대한 정보뿐만 아니라 분리된 상태의 툴에도 할당한 별도의 번호까지 모든 툴 체인저 관련 툴 정보를 입력하여 사용해야 합니다. 그리고 핸들링 작업 시에도 작업물의 탈착 상태를 각 툴 번호에 할당하여 사용해야 합니다.

툴의 길이는 플랜지 좌표계에서 방향별 길이입니다. \(X축 방향 길이: Xt / Y축 방향 길이: Yt / Z축 방향 길이: Zt\)

![그림 61 로봇 형태별 플랜지 좌표계](../../../_assets/image_213.png)

툴의 각도는 플랜지 좌표계에서 방향별 자세 변환량입니다. \(X축 방향 각도: Rx / Y축 방향 각도: Ry / Z축 방향 각도: Rz\)

![그림 62 툴 각도: Rotating Rx \(좌\) / Rotating Ry \(중간\) / Rotating Rz \(우\)](../../../_assets/image_211.png)

즉, 툴의 길이 및 각도는 플랜지 좌표계를 기준으로 설정됩니다. 툴 길이는 플랜지 좌표계의 중심에서 TCP까지의 거리를 설정합니다.

툴의 자세는 위와 같이 설정된 툴 각도에 따라 툴 플랜지 좌표계를 기준으로 X, Y, Z 방향을 순차적으로 회전시킨 값입니다.

Rxyz = Rot\(z, Rz\)Rot\(y, Ry\)Rot\(x, Rx\)

* Rxyz: 툴 플랜지를 기준으로 한 툴의 자세 회전 행렬
* Rot\(z, Rz\): 플랜지 좌표계의 Z축으로 Rz만큼 회전시키는 회전 행렬
* Rot\(y, Ry\): 플랜지 좌표계의 Y축으로 Ry만큼 회전시키는 회전 행렬
* Rot\(x, Rx\): 플랜지 좌표계의 X축으로 Rx만큼 회전시키는 회전 행렬

# 7.4.1.1 툴 데이터 설정

수동으로 로봇의 R1축 플랜지를 기준으로 TCP \(Tool Center Point\)의 거리와 각도를 설정하고, 툴의 중량, 무게 중심과 이너셔를 등록하는 방법은 다음과 같습니다.

1. \[3: 로봇 파라미터 &gt; 1: 툴 데이터\] 메뉴를 터치하십시오.
2. 툴 데이터의 이름과 중량, 축별 상세 조건, 허용 비율을 설정하십시오.

![](../../../_assets/image_223.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">툴 데이터 목록에서 선택한
        툴 데이터의 상세 정보입니다.
        툴 데이터 이름과 설명,
        중량, 축별 상세 조건, 허용
        비율을 설정할 수 있습니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
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
            <img src="../../../_assets/tool-data-auto-calib.png" alt/>
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
            <img src="../../../_assets/tool-angle-auto-calib.png" alt/>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
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

# 7.4.1.2 툴 데이터 설정 정보

* \[중량\]: 툴의 중량\(㎏\)
* \[길이\]: 툴의 길이\(㎜\). 자동 캘리브레이션 기능 또는 자동 보정 기능을 이용하여 설정할 수 있습니다.
* \[각도\]: 툴의 각도\(deg\). 자동 캘리브레이션 기능 또는 각도 보정 기능을 이용하여 설정할 수 있습니다.
* \[중심\]: 플랜지 중심을 기준으로 툴의 무게 중심 위치\(㎜\). 부하 추정 기능을 이용하여 설정할 수 있습니다.
* \[이너셔\]: 툴 좌표에 대한 툴의 관성 모멘트\(㎏·㎡\). 부하 추정 기능을 이용하여 설정할 수 있습니다.
* 허용 비율: \(고부하 모드 적용 로봇 모델에 한함\) 기준 허용값 대비 현재 설정의 비율. 허용 비율에 따른 로봇 동작은 다음과 같습니다.

| 구분 | 정상 | 고부하 모드 | 예외 허용 모드 | 재생 불가\(대형\) |
| :--- | :--- | :--- | :--- | :--- |
| 중량 비율 \(%\) | ~ 100 | 100 ~ 120 | 100 ~ 120 | 120 ~ |
| 모멘트 비율 \(%\) | ~ 100 | 100 ~ 110 | 100 ~ 115\(150\) | 115\(150\) ~ |
| 이셔너 비율 \(%\) | ~ 100 | 100 ~ 130 | 100 ~ 150\(600\) | 150\(600\) ~ |

{% hint style="info" %}
허용 비율은 로봇 모델과 제어기 소프트웨어 버전에 따라 변경될 수 있습니다.
{% endhint %}



# 7.4.2 축 원점

각 축의 기구학적 원점 위치를 등록할 수 있습니다.

1. \[3: 로봇 파라미터 &gt; 2: 축 원점\] 메뉴를 터치하십시오.
2. 각 축의 기구학적 원점 위치를 설정하십시오.

![](../../_assets/image_212.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>각 축의 기구학적 원점
          위치의 상세 정보입니다.
          축의 엔코더와 위치를
          설정할 수 있습니다.</p>
        <ul>
          <li>S축: 로봇과 주변 지그의
            설치 상황에 따라 S축 원점을
            변경합니다.</li>
          <li>R1축: 툴의 부착 방향에
            따라 R1축 원점을 변경합니다.</li>
          <li>H, V, R2, B축: 자동 캘리브레이션
            기능을 이용하여 자동으로
            설정할 수 있습니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[적용]: 선택된 축 정보에
            선택한 원점 위치를 적용합니다.</li>
          <li>[전체적용]: 모든 축 정보에
            선택한 원점 위치를 적용합니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
* 축 원점 설정은 로봇의 직교 동작 정확도에 영향을 미칩니다. 가능한 한 정확한 값으로 변경하십시오.
* 축 원점 설정이 변경되면 기존에 작성된 프로그램의 위치가 변경되므로 축 원점 설정은 반드시 초기 설치 단계에서만 실행하십시오.
* 엔코더 옵셋 설정이 변경되면 축 원점을 새로 설정해야 하므로 반드시 엔코더 옵셋 설정을 완료한 후에 축 원점을 설정하십시오.
{% endhint %}

{% hint style="info" %}
공장 출하 시에는 각 축의 기구학적 원점 위치가 표준값\(0X400000\)으로 설정되어 있습니다.
{% endhint %}

# 7.4.3 소프트 리밋

로봇 사용 환경에 따라 각 축의 동작 범위를 조정합니다.

1. \[3: 로봇 파라미터 &gt; 3: 소프트 리밋\] 메뉴를 터치하십시오.
2. 각 축의 동작 범위를 설정하십시오.

![](../../_assets/image_214.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">각 축의 동작 범위의 상세
        정보입니다. 축의 최소와
        최대 동작 범위와 현재
        축 위치를 설정할 수 있습니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[현재값]: 현재 로봇의
            위치를 기준으로 각 축의
            동작 범위를 설정합니다.</li>
          <li>[ALL 초기화]: 모든 축의 동작
            범위를 초기화합니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
공장 출하 시에는 로봇 각 축의 동작 범위가 최대로 설정되어 있습니다.
{% endhint %}

# 7.4.4 엔코더 옵셋

현재 엔코더의 위치를 엔코더의 원점 위치\(0X400000위치\)로 설정할 수 있습니다. 로봇 각 축의 기준 위치\(각 축의 스케일이 부착된 위치\)에서 엔코더의 원점을 결정합니다.

1. \[3: 로봇 파라미터 &gt; 4: 엔코더 옵셋\] 메뉴를 터치하십시오.
2. 각 축의 위치를 조정하여 엔코더 옵셋값을 설정하십시오. 엔코더 옵셋값은 헥사값\(Hexa값, 16진수\)으로 기록됩니다.

![](../../../_assets/image_222.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">각 축의 엔코더 옵셋값의
        상세 정보입니다. 축의
        보정된 엔코더 값과 현재
        엔코더 값, 현재 위치를
        설정할 수 있습니다.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[단일 초기화]/[전체 초기화]: 선택된
            축 또는 모든 축의 엔코더
            옵셋값을 초기화합니다.</li>
          <li>[보정값 계산]: 선택한
            축의 엔코더 옵셋값을
            보정합니다.</li>
          <li>[이전 보정값]: 선택한
            축의 보정 전 엔코더 옵셋값을
            불러 옵니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
공장 출하 시 엔코더 옵셋값이 설정됩니다. 모터나 엔코더 교환 등 필요한 경우에만 엔코더 옵셋값을 재설정하십시오.
{% endhint %}

# 7.4.4.1 엔코더 옵셋값 활용

현재의 작업 프로그램을 백업하고 시스템을 초기화\(\[설정 &gt; 5: 초기화 &gt; 1: 시스템 초기화\]\)한 후에도 기존의 프로그램을 계속해서 사용하려면 로봇은 초기화 이전의 기준 위치 정보를 유지해야 합니다. 엔코더 옵셋값을 기록해 두면 로봇의 이전 위치 정보를 불러 올 수 있습니다.

시스템 초기화 후에 엔코더 옵셋값을 헥사값으로 직접 입력하십시오. 소프트 키보드를 이용하여 간편히 입력할 수 있습니다.

만약, 엔코더 옵셋값을 축 위치값\(mm 또는 degree\)으로 기록해 둔 경우에는, &lt;Shift&gt; 키를 누른 상태에서 \[ONE 초기화\] 버튼을 터치하여 나타난 입력창에 축 위치값을 입력한 후 \[확인\] 버튼을 터치하십시오.

![](../../../_assets/image_208.png)

{% hint style="info" %}
축 위치 입력창의 기본 설정값은 기준 자세 값입니다. 축 위치 값을 입력하지 않고 저장하면 현재 엔코더의 위치가 원점 위치\(0X400000\)로 설정됩니다.
{% endhint %}

# 7.4.5 B축 비사용구역

B축의 0도 부근에서는 R1축 회전 중심축과 R2축의 회전 중심축이 거의 평행이 되는데, 로봇의 TCP가 직선이나 원호와 같은 보간 동작을 하면 작은 움직임에도 손목 축이 급격히 동작하게 됩니다.

B축의 비사용 구역을 설정합니다.

1.	\[3: 로봇 파라미터 &gt; 5: B축 비사용구역\] 메뉴를 터치하십시오.

2.	비사용 구역의 판단 각도와 보간 처리 방식을 설정한 후 \[OK\] 버튼을 터치하십시오.

![](../../_assets/image_206.png)

* \[설정값\]: B축 비사용 구역의 판단 각도를 입력합니다.
* \[비사용구역의 보간처리\]: 로봇의 궤적이 보간 동작으로 B축 비사용 구역을 통과해야 하는 경우, 에러 처리 및 로봇의 정지 여부를 설정합니다.



# 7.4.6 Accuracy

로봇의 목표 스텝 진행 시 스텝을 통과하는 정밀도인 Accuracy 레벨의 상세 조건을 설정합니다.

1. \[3: 로봇 파라미터 &gt; 6: Accuracy\] 메뉴를 터치하십시오.
2. Accuracy 레벨별 툴 끝 위치\(TCP\)와 자세를 설정하십시오.

![](../../_assets/image_215.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>Accuracy 레벨별 상세 정보입니다.
          Accuracy 레벨의 툴 끝 위치(TCP)와
          자세를 설정할 수 있습니다.</p>
        <ul>
          <li>Accuracy 레벨은 0부터 7까지
            설정할 수 있으며 Accuracy 레벨은
            스텝 명령문 인수의 하나로
            기록됩니다.</li>
          <li>Accuracy 레벨 0 ~ 6: 각 레벨에 TCP
            거리 및 자세, 부가축의
            거리 및 각도를 입력합니다.
            <br
            />LCD 로봇과 같이 직선 또는
            원호 보간을 지원하지
            않는 로봇의 경우에는
            부가축과 동일한 방법이
            적용됩니다.</li>
          <li>Accuracy 레벨 7: 제어기에서
            자동으로 값이 계산되어
            나타나므로 직접 입력하지
            않아도 됩니다.
            <br />Accuracy 레벨 7을 사용하면 스텝
            거리의 1/2 조건을 만족하는
            최대의 코너링 경로가
            생성됩니다. LCD 핸드의
            진출입와 같이 로봇을
            최대한 부드럽고 빠르게
            동작시키고자 할 때 Accuracy
            레벨 7을 유용하게 사용할
            수 있습니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[전체 초기화]: 모든 Accuracy 레벨의
            TCP 거리와 자세를 초기화합니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
* “2.3 스텝”의 내용에 대한 이해를 바탕으로 Accuracy 레벨에 접근하면 더 쉽게 사용할 수 있습니다.
* 서보건과 이퀄라이저 리스건의 용접 스텝에서는 설정된 Accuracy 레벨에 관계없이 제어기에서 자동으로 제한합니다.
{% endhint %}

# 7.4.7 축별 부가중량

로봇의 기본 축에 장착된 트랜스포머나 배선용 지지대 등에 대한 정보를 등록합니다.

1.	\[3: 로봇 파라미터 &gt; 7: 축별 부가중량\] 메뉴를 터치하십시오.

2.	기본 축 탭을 선택하고 장착된 부가 중량 정보를 설정한 후 \[OK\] 버튼을 터치하십시오.

![](../../../_assets/image_219.png)

{% hint style="warning" %}
로봇에 트랜스포머나 배선용 지지대 등이 장착되어 부가 중량이 있을 경우에는 반드시 각 축의 부가 중량 정보를 등록하십시오. 부가 중량을 정확히 등록하지 않으면 툴 부하 추정 시 오차가 커질 수 있습니다.
{% endhint %}

# 7.4.7.1 각 축의 좌표계 원점

각 축의 X, Y, Z 방향은 로봇 좌표계와 동일한 방향으로 설정되어 있습니다. 각 축의 좌표계 원점은 다음을 참조하십시오.

![그림 63 로봇 형태별 각 축의 좌표계 원점](../../../_assets/image_484.png)

# 7.4.8 충돌검지\(추후 기능 제공\)

Hi6 제어기에는 로봇이 비정상적인 조건에서 동작하게 되거나 이상 동작을 하게 될 때의 안전 장치로 과전류, 과부하, 과속도, 위치 편차 에러 검지 기능과 충돌검지 기능이 있습니다. 이 두 기능이 상호 보완적으로 작용하여 로봇의 안전성을 높입니다.

Hi6 제어기에는 모델 기반의 충돌검지 기능을 기본으로 제공합니다. 모델 기반의 충돌검지 기능은 로봇이 동작 중에 정상적으로 발생해야 하는 토크와 실제 측정되는 토크의 차이를 로봇의 동역학 모델을 기반으로 계산하여 충돌을 검지합니다. 민감도를 설정하여 충돌에 대한 반응성을 조절할 수 있으며 로봇이 저속으로 움직일 때 발생하는 외부와의 접촉도 검지할 수 있습니다.

그러나 충돌검지 기능은 로봇 축에서의 충돌을 검지하므로 로봇에 충격이 전달되지 않는 경우에는 충돌이 검지되지 않습니다. 이외에 충돌검지 기능 사용 시 주의해야 할 사항은 다음과 같습니다.

* 충돌검지 기능은 모터가 켜진 상태에서만 동작합니다.
* 반드시 부하추정을 실행한 후에 충돌검지 기능을 사용하십시오.
* 툴 중량 및 축별 부가 중량이 실제와 다를 경우, 오검지가 발생할 수 있습니다.
* 부하추정 및 센서기반/센서리스 힘 제어 기능 수행 시 충돌을 검지하지 않습니다.
* 로봇에 부착되지 않은 포지셔너, 정치건, 지그 등의 충돌은 검지할 수 없습니다.
* 특주형 로봇은 모델 기반의 충돌검지 기능을 지원하지 않습니다.

충돌검지 기능을 설정하는 방법은 다음과 같습니다.

1. \[3: 로봇 파라미터 &gt; 14: 충돌검지\] 메뉴를 터치하십시오.
2. 충돌검지 기능의 사용 여부와 민감도 등을 설정하십시오.

![](../../../_assets/image_210.png)

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
        <img src="../../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>충돌검지 기능의 사용
          옵션 정보입니다. 이 기능의
          사용 여부와 민감도, 저속
          충돌검지 기능 사용 여부를
          설정할 수 있습니다.</p>
        <ul>
          <li>[기능 사용]: 충돌검지
            기능의 사용 여부를 설정합니다.</li>
          <li>[민감도]: 충돌검지 민감도를
            설정합니다. 값이 클수록
            충격에 민감하게 동작합니다.(기본
            설정값: 100%)</li>
          <li>[저속 충돌 검지]: 저속
            충돌검지 기능의 사용
            여부를 설정합니다.
            <ul>
              <li>[기준 시간]: 충돌로 판단하기
                위한 기준 시간을 설정합니다.
                기준 시간 동안 충격력이
                발생하면 충돌로 판단합니다.</li>
              <li>[링크 속도]: 저속으로
                판단하기 위한 기준 속도를
                설정합니다. 기준 링크
                속도 이하에서만 저속
                충돌을 검사합니다.</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[단일]: 변경 내용을 저장합니다.</li>
          <li>[전체 초기화]: 모든 사용 옵션
            설정값을 초기화합니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

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
          <img src="../../../_assets/coldet-sensitivity.png" alt/>
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

# 7.4.9 조그인칭 레벨 설정

이동 거리를 지정하여 동작을 제한할 수 있습니다. 수동 모드에서 조그키로 원하는 거리만큼 이동할 때 유용합니다.

1.	\[3: 로봇 파라미터 &gt; 11: 조그인칭 레벨설정\] 메뉴를 터치하십시오.

2.	조그인칭 레벨별로 거리와 각도를 설정한 후 \[OK\] 버튼을 터치하십시오.

![](../../../_assets/image_217.png)

# 7.4.9.1 조그인칭 기능의 주요 기능

* 인칭 가능 좌표계
  * 축 좌표계 인칭: 각 축의 이동 거리\(㎜\)와 각도\(deg\)를 지정한 만큼만 이동합니다.
  * 직교 좌표계 인칭
  * 툴 좌표계 인칭
  * 사용자 좌표계 인칭: X, Y, Z 위치\(㎜\)와 Rx, Ry, Rz 자세\(deg\)에 대해 지정한 만큼만 이동합니다.
* 인칭 거리 속도 레벨 기존의 조그 속도와 동일한 레벨에 인칭 거리를 설정할 수 있어 8 단계의 속도를 선택할 수 있으며 각 단계에 인칭 거리를 설정할 수 있습니다.



# 7.4.9.2 인칭 조그 조작

인칭 기능은 조그키 ONE PUSH 당 최대 이동 거리를 초과하여 움직이지 않게 하는 기능입니다.

인칭 거리에 도달한 이후에도 계속 조그키를 누르고 있다가 손을 떼면 로봇이 인칭 거리까지 감속하여 정지하고 움직이지 않습니다.

![그림 64 인칭 거리 도달 후 키에서 손을 뗀 경우](../../../_assets/image_209.png)

인칭 거리에 도달하기 전에 조그키에서 손을 뗀 경우에는 조그키에서 손을 뗀 시점부터 로봇이 감속하여 정지합니다. 이때는 일반 조그 모드와 동일합니다.

![그림 65 인칭 거리 도달 전 키에서 손을 뗀 경우](../../../_assets/image_216.png)

{% hint style="info" %}
축 좌표계에서 속도 레벨 1은 엔코더 1 bit씩 이동하도록 고정되어 있습니다.
{% endhint %}

# 7.5 응용 파라미터

1.	\[4: 응용 파라미터\] 메뉴를 터치하십시오. 응용 파라미터 메뉴가 나타납니다.

2.	원하는 메뉴를 선택하여 로봇 응용 기능의 사용을 위한 각종 파라미터를 확인하고 설정하십시오.

![](../_assets/image_218.png)

{% hint style="info" %}
각 메뉴의 사용 방법에 대한 자세한 내용은 별도의 응용 기능별 “기능 설명서”를 참조하십시오.
{% endhint %}

# 7.6 초기화

로봇 제어기가 정상적으로 동작하지 않는 경우 시스템을 초기화합니다. 반드시 현대로보틱스 로봇의 초기화 설정 경험이 있는 엔지니어가 시스템 초기화를 수행해야 합니다.

1.	\[5: 초기화\] 메뉴를 터치하십시오. 초기화 메뉴가 나타납니다.

2.	원하는 메뉴를 선택하여 로봇 시스템 및 시리얼 엔코더의 초기화를 수행하십시오.

![](../../_assets/image_249.png)

{% hint style="info" %}
\[초기화\] 메뉴의 일부 항목은 특정 유형의 부가축을 선택한 경우에만 지원됩니다.
{% endhint %}

{% hint style="info" %}
* 시스템을 초기화하려면 고객지원팀에 문의하여 전문가에게 의뢰하거나 자격을 갖춘 엔지니어에게 문의하여 오조작을 예방하십시오.
* 시스템을 초기화하면 제어기에 저장된 모든 데이터와 프로그램이 삭제됩니다. 시스템을 초기화하기 전에 데이터와 프로그램을 백업해 두고 필요한 경우 복원하여 사용하십시오. 데이터 백업과 복원에 대한 자세한 내용은 “[4.2.5 데이터 백업](../../menu/file-manager/data-backup.md)”과 “[4.2.6 데이터 복원](../../menu/file-manager/data-restore.md)”을 참조하십시오.
{% endhint %}



# 7.6.1 시스템 초기화

1.	Hi6 티치 펜던트 화면의 상태 표시줄에서 운전 방식이 수동 모드로 설정되어 있는지 확인하십시오.

![](../../_assets/image_233.png)

* 자동 모드로 설정되어 있는 경우, 티치 펜던트의 모드 스위치를 돌려 수동 모드로 설정하십시오.

![](../../_assets/image_230.png)

2.	\[5: 초기화 &gt; 1: 시스템 초기화\] 메뉴를 터치하십시오.

3.	저장된 데이터를 확인한 후 \[초기화\] 버튼을 터치하십시오. 제어 파라미터 파일과 기계 파라미터 파일을 포함한 모든 데이터와 프로그램이 삭제되고 초기 설정값으로 복원됩니다.

![](../../_assets/image_224.png)

# 7.6.2 로봇 타입 선택


1.	\[5: 초기화 &gt; 2: 로봇타입 선택\] 메뉴를 터치하십시오. 또는 Hi6 티치 펜던트 화면 우측 상단의 \[메커니즘\] 버튼을 터치하십시오.

2.	로봇 모델 선택창에서 로봇을 선택한 후 \[확인\] 버튼을 터치하십시오.

![](../../_assets/image_251.png)

* 로봇 모델 목록을 스크롤하여 모델명을 확인하거나 모델명을 직접 입력하여 검색할 수 있습니다.
* 로봇 용도 버튼을 터치하면 해당 용도에 속한 로봇만 목록에서 확인할 수 있습니다.
* 신규 로봇 모델을 선택하면 기계 파라미터 파일\(hi6\_porj.json\)이 초기 설정값으로 복원되고 각종 이력 파일도 초기화됩니다.
* 주행축이나 서보건과 같은 부가축이 포함된 시스템을 선택한 경우, 부가축의 개수를 설정하십시오. 부가축이 없이 로봇축만으로 구성된 시스템의 경우에는 0을 입력하면 됩니다.

![](../../_assets/image_232.png)

{% hint style="warning" %}
* 로봇 본체와 제어기는 하나의 시스템으로 구성되어 출하됩니다. 이 때문에 로봇 제어기에는 시스템을 함께 구성하는 로봇의 구동 용량에 맞는 드라이브가 장착됩니다.
* 시스템을 초기화하여 재설정할 경우에는, 공장 출하 시에 초기값으로 설정된 로봇 모델을 반드시 확인하여 올바른 모델로 설정하십시오.
{% endhint %}

3.	Hi6 티치 펜던트 화면 우측 하단의 \[즐겨찾기\] 버튼을 터치한 후 즐겨찾기 창의 입력 영역에 314를 입력하고 \[확인\] 버튼을 터치하십시오.

![](../../_assets/image_254.png)

{% hint style="warning" %}
* 엔지니어 모드\(Engineer Mode\)에서는 상태 표시줄에 엔지니어 모드 아이콘\( \)이 깜빡입니다.
* 엔지니어 모드에서 잘못 설정하면 로봇 시스템에 심각한 문제가 발생할 수 있으므로 주의하시기 바랍니다.
{% endhint %}

4.	Hi6 티치 펜던트 화면 우측 하단의 \[설정\] 버튼 &gt; \[3: 로봇 파라미터 &gt; 4: 엔코더 옵셋\] 메뉴를 터치하십시오.

![](../../_assets/image_238_1.png)

5.	엔코더 옵셋 보정을 수행하십시오. 로봇 위치가 기준 자세가 아니더라도 모터를 켜기 위해서는 임시로 엔코더 옵셋을 설정해야 합니다.

![](../../_assets/image_239.png)

{% hint style="info" %}
* 엔코더 옵셋 설정은 통상적으로 로봇을 기준 자세로 이동한 상태에서 수행합니다.
* 시스템 초기화 시에는 로봇의 위치가 기준 자세가 아니어도 엔코더 옵셋 설정을 수행하십시오. 그렇지 않으면 모터가 켜지지 않아 로봇을 구동할 수 없습니다.
{% endhint %}

6.	제어기의 전원을 껐다가 켠 후 모터에 전원을 공급하십시오.

7.	수동 모드에서 저속으로 안전하게 로봇을 기준 자세로 움직인 후 5 ~ 6번 단계를 참조하여 다시 엔코더 옵셋 보정을 수행하십시오.

* 엔코더 옵셋 설정에서는 현재 엔코더의 위치가 0X400000으로\(16 진수\) 설정됩니다.
* 모터가 고장 나 교체할 경우 같은 위치에서 엔코더 옵셋 설정을 수행하면 기록된 프로그램을 동일하게 사용할 수 있습니다.

8.	티치 펜던트의 &lt;프로그램&gt; 키를 눌러 프로그램 9999번을 선택한 후 한 스텝을 기록하십시오. 로봇을 기준 위치로 간편하게 이동할 수 있습니다.



{% hint style="warning" %}
* 협동로봇 초기화에 대한 자세한 내용은 “협동로봇 안전 기능 설명서”를 참조하십시오.
* 시스템을 초기화하려면 고객지원팀에 문의하여 전문가에게 의뢰하십시오.
* 시스템을 초기화하면 제어 파라미터 파일, 기계 파라미터 파일을 포함한 모든 데이터와 프로그램이 삭제됩니다. 시스템을 초기화하기 전에 데이터를 백업해 두면 필요한 경우 복원하여 사용할 수 있습니다. 데이터 백업과 복원에 대한 자세한 내용은 “[4.2.5 데이터 백업](../../menu/file-manager/data-backup.md)”과 “[4.2.6 데이터 복원](../../menu/file-manager/data-restore.md)”을 참조하십시오.
{% endhint %}



# 7.6.3 용도 설정

작업 용도를 선택하고 작업 용도에 맞게 사용자 키 및 입출력 할당 신호를 초기화합니다.

1.	\[5: 초기화 &gt; 3: 용도설정\] 메뉴를 터치하십시오.

2.	작업 용도를 선택하고 용도에 맞춰 환경 조건을 설정한 후 \[OK\] 버튼을 터치하십시오. 선택한 작업 용도 관련 명령어를 사용할 수 있으며 관련 메뉴에 접근할 수 있습니다.



# 7.6.3.1 Spot Welding

작업 용도를 스폿용접으로 선택하면 스폿 용접 관련 명령어를 사용할 수 있으며 스폿 용접 관련 메뉴에 접근할 수 있습니다.

![](../../../_assets/image_247.png)

1.	\[스폿용접\]을 유효로 설정하십시오. 다른 용도는 무효 처리됩니다.

2.	\[사용자키 초기화\] 드롭다운 메뉴와 \[입출력할당 초기화\] 드롭다운 메뉴를 클릭하여 스폿으로 설정하십시오.



# 7.6.3.2 Arc Welding

작업 용도를 아크용접으로 선택하면 아크 용접 관련 명령어를 사용할 수 있으며 아크 용접 관련 메뉴에 접근할 수 있습니다.

![](../../../_assets/image_240.png)

1.	\[아크용접\]의 용접기 유형\(아날로그 또는 디지털\)을 설정하십시오. 다른 용도는 무효 처리되고 화면 하단에 시스템에서 지원하는 용접기가 목록으로 나타납니다.

2.	용접기 목록을 확인한 후 용접기 번호를 설정하십시오.

3.	\[사용자키 초기화\] 드롭다운 메뉴와 \[입출력할당 초기화\] 드롭다운 메뉴를 클릭하여 아크로 설정하십시오.



# 7.6.4 시리얼 엔코더 리셋

시리얼 엔코더는 내부 메모리에 엔코더 회전수 정보를 저장합니다. 모터의 에러 상태를 해제하거나 엔코더의 영점을 리셋하여 엔코더의 회전수를 0으로 클리어할 수 있습니다.

1. \[5: 초기화 &gt; 4: 시리얼 엔코더 리셋\] 메뉴를 터치하십시오.
2. 각 축의 엔코더 리셋 모드를 설정하고 상태를 확인한 후 리셋을 실행하십시오.

![](../../_assets/image_231.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>축별로 엔코더 리셋 사용
          여부와 모드를 설정합니다.</p>
        <ul>
          <li>[무효]: 시리얼 엔코더
            리셋을 실행하지 않습니다.</li>
          <li>[에러해제]: 엔코더 회전수를
            클리어하지 않고 모터의
            엔코더 관련 에러만 해제합니다.</li>
          <li>[엔코더 리셋]: 모터의
            엔코더 관련 에러를 해제하고
            엔코더의 영점을 리셋하여
            회전수를 클리어합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[실행]: 시리얼 엔코더
            리셋을 실행합니다.</li>
          <li>[전축선택]: 모든 축을
            한 번에 선택합니다.</li>
          <li>[전축해제]: 모든 축의
            선택을 한 번에 해제합니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
* 로봇 시스템의 초기화 설정 수행 시에 엔코더 리셋을 수행하고 로봇이 정상 동작 중에는 절대 엔코더 리셋을 수행해서는 안 됩니다. 다만, 통신 이상 등의 엔코더 관련 에러가 발생하거나 엔코더 배터리가 소실된 경우에는 엔코더 리셋을 수행할 수 있습니다. 이때에는 기존의 로봇 원점 위치와 달라지지 않도록 로봇 프로그램의 실제 위치를 확인하여 작업하십시오.
* 제어기와 엔코더에 전원이 공급되지 않으면 엔코더의 위치 정보가 손실되어 로봇 작업 프로그램 사용에 문제가 발생할 수 있습니다. 이를 해결하기 위해 시리얼 엔코더에 전용 배터리를 부착하여 제어기의 전원 상태에 관계없이 위치 정보를 기록합니다. 엔코더 배터리에 전압 에러가 발생하면 반드시 제어기의 전원이 켜져 있는 상태에서 배터리를 교체하여 위치 정보의 손실을 예방하십시오.
{% endhint %}

# 7.6.5 부가축 파라미터 설정

로봇 외에 사용할 수 있는 부가축에는 로봇의 베이스축\(주행축\), 서보건축, 포지셔너축, 지그축이 있습니다. 부가축 사양별 상세 내용은 “부가축 기능 설명서”를 참조하십시오.

사용 중인 부가축의 사양 및 구성 등 파라미터를 설정하는 방법은 다음과 같습니다.

1. \[5: 초기화 &gt; 5: 부가축 파라미터 설정\] 메뉴를 터치하십시오.
2. 부가축의 사양 및 구성 등 파라미터를 설정하십시오.

![](../../_assets/image_236.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>부가축의 상세 파라미터
          설정 정보입니다. 부가축
          이름과 사양, 구성 등을
          확인하고 설정할 수 있습니다.</p>
        <ul>
          <li>[부가축]: 사용 중인 부가축의
            이름입니다.</li>
          <li>[축 사양]: 부가축의 사양입니다.
            사양에 따라 부가축 용도별로
            개발된 별도의 기능을
            사용할 수 있습니다.</li>
          <li>[축 구성]: 부가축의 메커니즘
            형태입니다. 일부 축 사양에는
            사전에 등록된 메커니즘
            형태를 지정할 수 있습니다.
            대표적으로 포지셔너의
            경우 표준 포지셔너 모델을
            선택할 수 있습니다.</li>
          <li>[축 위치]: DSP 보드에서 해당
            축이 연결된 위치입니다.
            배선이 연결된 사양에
            따라 BD 번호, DSP 번호, 축 번호,
            브레이크 번호를 순차적으로
            배선된 사양에 따라 지정합니다.</li>
          <li>[감속비]: 부가축 모터와
            링크의 감속비 정보입니다.
            <ul>
              <li>감속비 부호는 부가축
                링크가 (+) 방향으로 움직일
                때의 모터 샤프트의 회전
                방향에 따라 설정합니다.
                샤프트를 정면에서 보았을
                때 반시계방향(CCW)으로
                회전하면 (+) 부호, 시계방향(CW)으로
                회전하면 (-) 방향입니다.</li>
              <li>감속비 분자항의 파라미터는
                링크의 이동 거리(㎜ 또는
                deg)이며, 분모에 해당하는
                파라미터는 링크의 이동
                거리에 대응하는 모터의
                회전수입니다. 설정 항목의
                파라미터는 정수 형태로
                정의됩니다. 소수점으로
                나타나는 파라미터의
                경우 일정 배수를 분자와
                분모에 곱해 정수로 감속비를
                설정하십시오.</li>
            </ul>
          </li>
          <li>[소프트리밋]: 부가축의
            최소와 최대 동작 범위입니다.</li>
          <li>[AMP 사양]: 부가축 엠프 사양입니다.</li>
          <li>[모터 사양]: 부가축에
            연결된 모터의 모델명입니다.</li>
          <li>[가감속 파라미터]: 부가축의
            최고 속도와 가속 시간입니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[+]/[-]: 새로운 부가축을 추가하거나
            부가축을 삭제합니다.</li>
          <li>부가축 목록입니다. 부가축
            이름을 선택하면 상세
            파라미터를 확인 및 편집할
            수 있습니다.</li>
          <li>[페이지 복사]/[페이지
            붙여넣기]: 부가축 정보를
            복사하여 다른 부가축
            데이터에 붙여 넣습니다.
            <br
            />목록에서 복사할 부가축
            정보의 이름을 선택하고
            [페이지 복사] 버튼을 터치한
            후 값을 적용할 부가축의
            이름을 선택하고 [페이지
            붙여넣기] 버튼을 터치하십시오.</li>
          <li>[회전 반경]: 부가축이
            회전축인 경우, 조그 시
            선속도 제한을 위한 회전
            반경을 설정합니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

# 7.6.6 메커니즘 설정

메커니즘은 조그 조작 시 조그키가 할당되는 그룹으로 활용됩니다. 또한 스텝의 위치 기록 또는 편집 시 개별적으로 구분짓는 최소 단위 축들의 집합입니다. 메커니즘을 설정하면 각 축의 그룹별로 메커니즘 번호\(M\# \)가 할당됩니다.

엔드리스 기능의 사용 여부 및 포지셔너 그룹을 설정하는 방법은 다음과 같습니다.

1.	\[5: 초기화 &gt; 6: 메터니즘 설정\] 메뉴를 터치하십시오.

2.	축별로 메커니즘 번호와 포지셔너 그룹 번호, 엔드리스 기능의 사용 여부를 설정한 후 \[OK\] 버튼을 터치하십시오.

![](../../_assets/image_235.png)

* \[메커니즘\]: 드롭다운 메뉴를 터치하여 축의 메커니즘 번호를 설정합니다.
  * 축 사양이 로봇인 경우 메커니즘 번호가 M0으로 고정됩니다.
  * 부가축부터 메커니즘 번호를 M1 ~ M7 사이의 값으로 지정할 수 있습니다.
  * 동일한 메커니즘 번호로 설정된 축은 동일한 그룹으로 관리됩니다.
  * 부가축의 조그를 위해서 \[메커니즘\] 버튼을 이용하여 메커니즘 그룹을 전환합니다. 이때 조그키를 누르면 해당 메커니즘의 축의 순서대로 조그가 됩니다.
* \[포지셔너그룹\]: 포지셔너 그룹 번호를 설정합니다. 축 사양이 포지셔너로 설정된 축만 포지셔너 그룹 번호를 설정할 수 있습니다.
* \[엔드리스\]: 축에서 엔드리스 기능의 사용 여부를 설정합니다.

{% hint style="info" %}
설정된 메커니즘 단위는 멀티태스킹에서 개별 태스크에 할당되어 구동될 수 있는 최소 단위입니다. 개별 태스크에는 복합적인 메커니즘의 조합이 할당될 수 있습니다.
{% endhint %}

#### 

#### 포지셔너 그룹 지정 규칙

* 낮은 축부터 순서대로 그룹을 지정하십시오.
* 동기를 하지 않는 그룹은 무효로 지정하십시오.
* 포지셔너의 동일 그룹은 2축까지만 지원합니다. 3축을 동일 그룹으로 지정하지 마십시오.
* 그룹 설정을 재정의하면 이전에 지정되었던 포지셔너의 캘리브레이션 데이터가 무효화되므로 포지셔너의 캘리브레이션을 재실행하십시오.

#### 메커니즘 조그 규칙

* Hi6 제어기는 총 8개의 조그키를 제공합니다.
* 메커니즘은 조그 조작 시 하나의 그룹으로 활용됩니다.
* 메커니즘 번호를 \[M0\]으로 선택할 경우에는 예외적으로 7/8축 조그키가 동작하며, 다음 메커니즘을 포함한 총 축의 수가 8축 이내인 범위에서 M1 및 M2를 조작할 수 있습니다. 이 경우에도 메커니즘 번호를 \[M1\]으로 설정하면 M1의 구성 요소만 별도로 조그 조작할 수 있습니다.
* 활용 예는 다음과 같습니다.

예1\) M0: Robot \(1 ~ 6축\), M1: 주행축\(7축\), M2: 서보건\(8축\)

* \[M0\] 선택 ⇒ 1 ~ 6축 조그키: M0, 7축 조그키: M1, 8축 조그키: M2
* \[M1\] 선택 ⇒ 1축 조그키: M1
* \[M2\] 선택 ⇒ 1축 조그키: M2

예2\) M0: Robot \(1 ~ 6축\), M1: 주행축\(7축\), M2: 서보건\(8 ~ 9축\)

* \[M0\] 선택 ⇒ 1 ~ 6축 조그키: M0, 7축 조그키: M1
* \[M1\] 선택 ⇒ 1축 조그키: M1
* \[M2\] 선택 ⇒ 1 ~ 2축 조그키: M2

예3\) M0: Robot \(1 ~ 7축\), M1: 주행축\(8축\), M2: 서보건\(9 ~ 10축\)

* \[M0\] 선택 ⇒ 1 ~ 7축 조그키: M0, 8축 조그키: M1
* \[M1\] 선택 ⇒ 1축 조그키: M1
* \[M2\] 선택 ⇒ 1축 조그키: M2



# 7.7 자동 캘리브레이션

올바른 로봇 사용을 위해 교시된 프로그램 및 자동으로 동작하는 움직임을 이용하여 로봇의 축 원점, 툴 길이, 부하 질량, 베이스축 방향을 찾을 수 있습니다. 이렇게 캘리브레이션된 값은 로봇에 자동으로 반영됩니다.

1.	\[6: 자동 캘리브레이션\] 메뉴를 터치하십시오. 자동 캘리브레이션 메뉴가 나타납니다.

2.	원하는 메뉴를 선택하여 로봇의 축 원점, 툴 길이, 부하 질량, 베이스축 방향 등의 캘리브레이션을 수행하십시오.

![](../../_assets/image_257.png)

# 7.7.1 축 원점 및 툴 길이 최적화

축 원점 및 툴 길이 최적화는 외부 측정센서를 사용하지 않고 로봇 각 축의 원점 및 툴 길이를 캘리브레이션하는 기능입니다.

뾰족한 팁 2 개를 준비하여 하나는 외부에 고정하고 다른 하나는 툴에 고정한 후 외부의 고정 팁을 기준으로 로봇의 툴 끝의 자세만 바꿔 여러 점을 로봇 프로그램으로 기록합니다. 이때 축 원점과 툴 길이를 모두 찾아내려면 7 점, 툴 길이만 찾아내려면 4 점 이상을 교시해야 합니다.

![그림 68 축 원점 및 툴 길이 최적화 기능 교시 방법](../../_assets/image_228.png)

축 원점 및 툴 길이 최적화 기능을 이용하면 CAD데이터가 없는 툴 길이 X, Y, Z뿐만 아니라 로봇 H, V, R2, B축의 원점을 최적화하여 찾아낼 수 있습니다.

{% hint style="warning" %}
축 원점 및 툴 길이 최적화 기능을 사용하면 엔코더 옵셋 및 툴 길이가 변경되어 기존에 교시된 프로그램의 작업 위치가 변경됩니다. 그러므로 축 원점 및 툴 길이 최적화는 반드시 교시 프로그램 작성 전에 수행하십시오.
{% endhint %}

{% hint style="info" %}
* 축 원점 및 툴 길이 최적화 기능에서 교시의 정확도는 최대 스텝 위치 오차 결과의 정확성과 비례합니다. 따라서 뾰족한 두 팁을 준비하여 이 두 팁을 가능한 한 정확히 일치하는 교시 작업이 요구됩니다. 툴 끝과 공간상의 고정점의 일치 정확도가 육안 확인 시 0.5 ㎜ 이내가 되도록 합니다.
* 스텝의 자세가 유사하지 않도록 스텝별로 가능한 한 30 deg 이상 차이를 둔 자세를 설정하여 티칭하십시오.
* 스텝의 손목 축\(R2, B, R1\)을 가능한 한 크게 동작시키고 스텝별 손목 축의 각도 차이를 충분히\(가능한 한 크게\) 두고 티칭하십시오.
{% endhint %}

축 원점 및 툴 길이 최적화 기능의 사용 방법은 다음과 같습니다.

1. \[6: 자동 캘리브레이션 &gt; 1: 축 원점 및 툴 길이 최적화\] 메뉴를 터치하십시오.
2. 최적화 대상을 선택하고 상세 옵션을 설정하십시오.

![](../../_assets/image_234.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>부가축의 상세 파라미터
          설정 정보입니다. 부가축
          이름과 사양, 구성 등을
          확인하고 설정할 수 있습니다.</p>
        <ul>
          <li>[최적화 선택]: 최적화
            대상을 설정합니다.
            <ul>
              <li>[툴 길이]: 로봇의 툴 길이
                값을 보정합니다. 로봇
                원점이 정확히 설정된
                경우에는 툴 길이만 보정할
                수 있습니다.</li>
              <li>[축 원점 및 툴 길이]: 로봇의
                원점과 툴 길이 값을 모두
                보정합니다. 통상적으로
                로봇을 설치하고 최초에
                정확한 원점을 설정하고자
                할 때 사용합니다.</li>
            </ul>
          </li>
          <li>[프로그램 번호]: 동일점을
            여러 자세로 기록한 프로그램의
            번호를 설정합니다.</li>
          <li>[툴 번호]: 자동 설정하려는
            툴의 번호입니다. 설정용
            프로그램에 기록되어
            있는 툴 번호와 일치해야
            합니다.</li>
          <li>[스텝위치 오차 허용범위]:
            자동 캘리브레이션 결과의
            오차 범위를 설정합니다(초기
            설정값 0.6 ㎜). 예상 오차가
            오차 범위 내이면 자동으로
            정수 데이터를 갱신하고
            오차 범위를 벗어나면
            정수의 반영 여부를 사용자에게
            알려 확인 후 처리합니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[실행]: 설정 정보를 바탕으로
            최적화를 실행합니다.
            최적화 결과는 [최대스텝
            위치 오차]에 나타납니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="warning" %}
로봇의 원점과 툴 길이 값을 모두 보정하면 모든 로봇의 원점이 변경되어 기존에 작성된 프로그램의 위치가 변경되므로 주의하십시오.
{% endhint %}

{% hint style="info" %}
* 로봇 각 축의 원점 및 툴 길이는 설정 메뉴에서도 설정할 수 있습니다.
  * 툴 길이: \[설정 &gt; 3: 로봇 파라미터 &gt; 1: 툴 데이터\]
  * 각 축의 원점: \[설정 &gt; 3: 로봇 파라미터 &gt; 2: 축 원점\]
* 각도보정 기능\(\[설정 &gt; 3: 로봇 파라미터 &gt; 1: 툴 데이터\]\)을 이용해 툴 각도를 보정할 경우, 축 원점 및 툴 길이 최적화 기능을 먼저 실행한 후 각도 보정을 실행하십시오. 정확한 툴 데이터를 설정할 수 있습니다.
{% endhint %}

# 7.7.2 포지셔너 캘리브레이션

포지셔너\(Positioner\) 캘리브레이션은 로봇 외부에 설치된 지그 장치 동작에 동기화하여 로봇이 추종하거나 그 지그 장치에 대해 상대적인 직선 또는 원호 동작을 가능하게 하는 기능입니다. 포지셔너 캘리브레이션 기능에 적용되는 외부 지그 장치를 포지셔너 또는 스테이션\(Station\)이라고 합니다.

포지셔너 캘리브레이션 기능을 이용하면 로봇 작업 영역의 제한으로 인한 작업의 어려움을 보완할 수 있습니다. 즉, 작업물이 포지셔너 위에 고정되어 있는 상태에서 포지셔너가 이동하더라도 로봇은 이 포지셔너의 움직임을 추종하면서 작업물 위에서 직선 또는 원호 동작을 할 수 있습니다.

1축 포지셔너는 3 점, 2축 포지셔녀는 5 점을 교시하여 포지셔너의 캘리브레이션을 수행하면 간단히 포지셔너의 좌표계를 설정할 수 있습니다.

![그림 69 1축 표지셔너\(좌\) / 2축 포지셔너\(우\)](../../_assets/image_244.png)

포지셔너 캘리브레이션 기능의 주요 기능 정보는 다음과 같습니다.

| 주요 기능 | 설명 |
| :--- | :--- |
| 포지셔너 그룸 | 1 ~ 4 그룹 지원 |
| 포지셔너 축 수 | 1축 포지셔너, 2축 포지셔너 지원\(회전축\) |
| 보간 방식 | 직선 보간, 원호 보간 지원 |

{% hint style="info" %}
* 포지셔너 캘리브레이션 기능은 포지셔너 그룹이 설정된 상태에서 사용할 수 있습니다.
* 자세한 내용은 “Hi6 제어기 포지셔너 동기 기능 설명서”를 참조하십시오.
{% endhint %}

# 7.7.3 부하추정 기능

부하추정 기능이란 로봇의 선단에 부착된 툴의 물성치\(질량, 중심 위치, 이너셔\(Inertia\)\)를 일정한 동작을 거쳐 자동으로 산출하는 기능입니다.

제어기에는 로봇 본체의 정보\(각 링크의 질량, 질량 중심, 이너셔\)가 등록되어 있습니다. 그러나 툴은 필요에 따라 로봇의 선단에 부착하여 사용하므로 툴 정보를 입력해야 합니다. 로봇을 안전하게 사용하기 위해 필요한 툴의 물성치 정보에는 툴 질량\(㎏\), 중심 위치, 이셔너가 있습니다.

CAD 데이터에 툴의 물성치 정보가 있으면 작업 프로그램의 \[설정\] 버튼 &gt; \[3: 로봇 파라미터 &gt; 1: 툴 데이터\] 메뉴를 터치하여 툴 질량과 중심, 이너셔를 직접 입력할 수 있습니다.

![](../../_assets/image_241.png)

툴 데이터의 설정 정보는 다음과 같습니다.

![그림 71 툴 데이터](../../_assets/image_502.png)

* \[중량\]: 로봇 선단에 장착되는 툴의 총 중량\(㎏\)입니다.
* \[중심\]: 로봇 플랜지 면의 중심에서 툴의 무게 중심 위치까지의 x, y, z 방향의 거리\(㎜\)입니다.
* \[이너셔\]: 툴 좌표에 대한 툴의 관성 모멘트\(㎏·㎡\)입니다. 관성 모멘트는 무게 중심을 기준으로 x, y, z축 둘레의 질량 분포에 따라 결정되고 부하 질량이 회전축에서 멀리 분포할수록 커집니다.
* 툴 데이터 좌표계: 이너셔와 중심은 x, y, z축 방향에 대한 값으로 표기합니다.

그러나 많은 경우, CAD 데이터에서 툴의 질량과 이너셔, 무게 중심 등의 물성치를 확인하기 어렵습니다. 이때, 로봇 제어기에서 부하추정 기능을 이용하여 툴의 물성치를 확인할 수 있습니다.

![](../../_assets/image_256.png)

1.	\[6: 자동 캘리브레이션 &gt; 4: 부하추정 기능\] 메뉴를 터치하십시오.

2.	\[축별 부가중량\] 버튼을 터치한 후 축별 부가 중량 정보를 입력하십시오.

부가 중량이 있는 상태에서 부하추정 기능을 수행하면 로봇에 장착된 모든 중량물이 선단에 있는 것으로 판단합니다. 정확한 부하추정을 위해 축별 부가 중량 정보를 입력해야 합니다.

3.	로봇의 주축을 움직여 로봇을 안전한 영역으로 이동시킨 후 \[주축 자세지정\] 버튼을 터치하십시오.

4.	\[손목축 동작영역\] 버튼을 터치한 후 부하추정 동작에서 사용할 손목축의 동작 영역을 지정하십시오. 주변 시설이나 로봇 본체와 간섭이 발생하지 않는 동작 영역에서 부하추정을 수행할 수 있습니다.

\[손목축 동작영역\] 버튼이 지원되지 않을 경우, 이 단계를 생략하고 다음 단계를 수행하십시오

5.	\[확인운전\] 버튼을 터치하십시오. 로봇이 저속으로 동작하는 동안 주변 시설이나 로봇 본체의 간섭 여부를 확인할 수 있습니다.

6.	로봇에 장착된 툴의 번호를 입력한 후 \[정상운전\] 버튼을 터치하십시오. 부하추정을 수행하여 툴의 물성치가 산출됩니다.

7.	부하추정 결과를 확인한 후 \[종료\] 버튼을 터치하십시오. 산출된 툴의 물성치가 툴 번호에 등록됩니다.

{% hint style="info" %}
* 부가 중량이란 로봇 선단에 장착되는 툴을 제외한, 용접 드레싱 및 용접 신호선 중계 박스 등과 같이 사용자가 로봇에 장착하는 모든 장치의 무게입니다.
* 손목축 동작영역 기능은 일부 로봇에서는 지원되지 않습니다.
* 손목축 동작영역 기능의 설정값에 따라 부하추정 기능이 실행되지 않을 수 있으니 주의하십시오.
* 
  부하추정 기능에 대한 자세한 내용은 “부하추정 기능 설명서”를 참조하십시오.
{% endhint %}



# 7.7.4 베이스축 캘리브레이션

베이스축 캘리브레이션 기능은 축의 설치 방향을 캘리브레이션하는 기능입니다.

로봇 좌표계의 한 방향\(X, Y, Z\)과 정확히 일치하도록 베이스 축을 설치하는 것은 거의 불가능합니다. 베이스축 캘리브레이션 기능을 이용하여 제어기에서 베이스 축의 방향을 계산하여 베이스 축을 포함한 시스템의 직선보간 궤적 성능을 향상시킬 수 있습니다.

로봇을 베이스 축에 설치한 후 로봇이 설치된 임의의 베이스 축의 방향 벡터를 찾아 위치보간을 수행할 수 있게 합니다.

![그림 73 베이스 축 캘리브레이션](../../../_assets/image_513.png)

일반적으로 베이스 축은 로봇을 작업 위치로 이동하는데 사용합니다. 특수한 경우, 로봇이 베이스 축으로 이동하면서 직선 궤적이 보장되어야 하는 경우에도 베이스 축을 사용할 수 있습니다.

* 2 대의 베이스 축 캘리브레이션 로봇이 작업물을 반송하는 경우\(멀티 로봇 향후 지원\)
* 베이스 축을 동작하며 보간 동작을 해야 하는 경우

# 7.7.4.1 베이스 축 초기 설정

1.	수동 모드에서 초기 화면 우측의 \[설정\] 버튼 &gt; \[5: 초기화 &gt; 5: 부가축 파라미터 설정\] 메뉴를 터치하십시오.

2.	부가축의 사양 및 구성 등 파라미터를 설정한 후 \[OK\] 버튼을 터치하십시오.

* \[축 사양\]: 부가축의 사양을 베이스로 선택합니다.
* \[축 구성\]: 부가축의 메커니즘 형태를 임의로 선택합니다.
* 그외 파라미터: 기구 설계치와 제어기 구성 사양에 맞게 설정합니다.

{% hint style="info" %}
* 시스템 초기화 시에도 부가축 설정 메뉴가 나타나 베이스 축의 초기 설정을 할 수 있습니다.
* 부가축 파라미터 설정 메뉴는 일반 사용자에게 지원되지 않는 엔지니어용 기능입니다. 부가축 파라미터 설정 메뉴에 대한 자세한 내용은 엔지니어에게 문의하시기 바랍니다.
{% endhint %}

{% hint style="warning" %}
첫 번째 베이스 축에 한하여 캘리브레이션 기능을 사용할 수 있으며 부가축 파라미터 설정 시 축 구성을 임의로 설정할 수 있습니다. 첫 번째 베이스 축을 제외한 나머지 베이스 축에는 축 구성을 임의로 설정하지 마십시오.
{% endhint %}

# 7.7.4.2 베이스축 캘리브레이션 프로그램 티칭

1.	공간 상의 기준점을 마련하여 첫 번째 기준점을 기록하십시오.

2.	베이스 축을 200 ㎜ 이상 이동하여 동일점을 두 번째 스텝으로 기록하십시오.

3.	2번 단계에서 이동한 방향과 동일한 방향으로 200 ㎜ 이상씩 이동하며 동일점을 세 번째와 네 번째 스텝으로 기록하십시오.

![](../../../_assets/image_526.png)



{% hint style="warning" %}
* 로봇 캘리브레이션\(축 원점 및 툴 길이 최적화\)이 완료된 툴을 이용하여 주행축 캘리브레이션 프로그램을 티칭하십시오.
* 스텝 기록 시 베이스축 캘리브레이션을 위한 툴 번호로 기록하십시오.
* 기록 스텝 간 베이스축의 이동 거리는 가능한 한 멀게 설정하여 위치를 기록하십시오.
{% endhint %}

# 7.7.4.3 베이스축 캘리브레이션 실행

1.	\[6: 자동 캘리브레이션 &gt; 6: 베이스축 캘리브레이션\] 메뉴를 터치하십시오.

2.	베이스축 캘리브레이션용 프로그램 번호를 입력한 후 \[자동설정\] 버튼을 터치하십시오.

![](../../../_assets/image_259.png)

3.	베이스축의 설치 방향 벡터값을 확인한 후 \[OK\] 버튼을 터치하십시오.

# 7.7.4.4 베이스축 캘리브레이션 후 조작

베이스축 캘리브레이션 후에 베이스축을 조그 조작하면 생성된 베이스 축의 방향 벡터로 주행한 거리가 현재의 좌표값으로 환산됩니다.

![그림 74 베이스축 캘리브레이션 후 조작](../../../_assets/image_519.png)

1. 작업 영역의 패널 스택 우측 상단의 \[+\] 버튼을 터치한 후 패널 선택창에서 \[포즈\]를 터치하십시오. 베이스축의 이동에 따른 좌표계의 환산값이 나타납니다.
2. 베이스축을 조그 조작하십시오. 베이스축 방향으로 주행한 거리가 X, Y, Z 값으로 환산되어 포즈 정보창에 나타납니다
3. 통상적인 방법으로 스텝을 기록하고 재생하십시오.

{% hint style="warning" %}
조그 좌표계를 툴 좌표계로 설정하고 베이스축을 조그 조작하여 베이스축의 정상 캘리브레이션 여부를 확인하십시오. 툴 끝 고정 동작이 실행되면 베이스축이 정상적으로 캘리브레이션된 것입니다.
{% endhint %}

# 7.7.5 중력방향 자동 설정

Hi6 제어기는 동역학 기반의 제어기이므로 중력 방향을 설정하는 것이 중요합니다.

일반적으로 로봇의 설치 방향은 다음과 같이 중력 방향에 수직입니다. 로봇이 지면에 비스듬한 방향으로 설치된 경우 중력 방향을 로봇 제어기에 설정해야 합니다. 이때 중력 방향 자동 설정 기능을 사용할 수 있습니다.

![그림 75 지면에 놓인 로봇의 중력 방향\(좌\) / 경사면에 놓인 로봇의 중력 방향\(우\)](../../_assets/image_503.png)

중력 방향을 설정하는 방법은 다음과 같습니다.

1. 외부에 추를 달아 중력 방향을 표시하고 중력의 작용 방향으로 두 점\(Step1, Step2\)을 교시하십시오.
2. \[6: 자동 캘리브레이션 &gt; 8: 중력방향 자동 설정\] 메뉴를 터치하십시오.
3. 프로그램 번호를 입력한 후 \[실행\] 버튼을 터치하십시오. 방향 벡터가 계산되어 나타납니다.

![](../../_assets/image_250.png)

4. 방향 벡터값을 확인한 후 \[OK\] 버튼을 터치하십시오. 이 방향이 중력 방향으로 재설정됩니다.

# 7.7.6 로봇과 툴 캘리브레이션

로봇과 툴 캘리브레이션 기능은 3차원 측정기로 로봇의 위치를 측정할 수 있는 환경에서 사용합니다.

1.	로봇의 툴 끝에 측정할 위치를 선정한 후 로봇의 위치와 자세를 다양하게 움직이면서 15 점 이상의 위치를 측정하고 로봇 위치를 프로그램으로 기록하십시오.

![](../../_assets/image_245.png)

2.	측정한 로봇의 위치 데이터\(측정점 데이터\)를 X, Y, Z 형식으로 정리하여 파일\(형식: ASCII, 확장자: MSR\)을 생성하십시오.

![](../../_assets/image_258.png)

3.	위치 데이터 파일을 이동식 저장 장치에 저장한 후 이동식 저장 장치를 티치 펜던트에 연결하십시오. Hi6 티치 펜던트 화면의 상태 표시줄에 \[USB\] 아이콘\(![](../../_assets/icon-usb2.png)\)이 나타납니다.

4.	\[6: 자동 캘리브레이션 &gt; 9: 로봇과 툴 캘리브레이션\] 메뉴를 터치하십시오.

5.	\[탐색기\] 버튼을 터치하여 위치 데이터 파일을 선택한 후 측정에 사용한 로봇 프로그램을 설정하십시오.

![](../../_assets/image_225.png)

6.	\[OK\] 버튼를 터치하십시오. 로봇과 툴 캘리브레이션 실행 화면으로 전환됩니다.

7.	로봇과 툴 캘리브레이션 실행 화면에서 \[실행\] 버튼을 터치하십시오. 캘리브레이션 결과가 나타납니다.

![](../../_assets/image_253.png)

8.	캘리브레이션 결과를 확인한 후 \[OK\] 버튼을 터치하십시오. 캘리브레이션 결과값이 축 원점과 툴 정수에 자동으로 적용됩니다.

9.	\[3: 로봇 파라미터 &gt; 1: 툴 데이터\] 메뉴를 터치하여 로봇 캘리브레이션 실행 결과를 확인할 수 있습니다.

![](../../_assets/image_252.png)

{% hint style="info" %}
캘리브레이션 파라미터의 2 ~ 5축\(H, V, R2, B축\)의 축 원점과 툴 길이 X, Y, Z 값은 기본으로 선택되어 있습니다. 툴만 캘리브레이션하려면 각 축의 값을 선택 해제한 후 실행하십시오.
{% endhint %}





# 8. R코드

프로그램의 내용 수정이나 제어기의 설정 상태 변경과 같이 자주 사용하는 기능의 조작 절차를 특정한 서비스 코드\(R코드\)로 지정해 두고 간편하게 사용할 수 있습니다.

R코드는 Reset\(리셋\)과 Rapid\(빠른\)의 R에 번호를 조합하여 “R+No.” 형식으로 구성됩니다.



# 8.1 R 코드 사용

R코드를 이용하여 지정된 기능을 실행하는 방법은 다음과 같습니다.

1.	Hi6 티치 펜던트 화면 우측의 \[즐겨찾기\] 버튼을 터치하십시오. 즐겨찾기 창이 나타납니다. 

![](../_assets/bt-favorite.png)

2.	목록에서 코드 번호를 선택하거나 입력 영역에 코드 번호를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오. 선택한 R코드에 지정된 기능이 실행됩니다.



![](../_assets/image_242.png)



# 8.2 R0 스텝 카운터 리셋

즐겨찾기 창에서 0을 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

![](../_assets/image_271.png)

스텝 카운터를 초기화하여 STEP0으로 이동합니다. 또한 다음의 기능을 실행할 수 있습니다.

* 플레이백 실행 상태 클리어
* 종합 이상 신호, 램프 끄기
* 경보 신호 끄기
* WAIT 대기 상태 클리어
* 각종 응용 기능 상태 및 신호 클리어 등

{% hint style="info" %}
로봇 기동 중에는 R0 코드를 사용할 수 없습니다.
{% endhint %}

# 8.3 R115 프로그램 복사

메인 보드의 JOB 프로그램을 메인 보드의 다른 프로그램으로 복사합니다. 복사할 프로그램 번호를 입력한 후에 복사될 프로그램 번호를 입력하십시오.

1.	즐겨찾기 창에서 115를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

2.	복사할 프로그램\(원본\) 번호와 복사될 프로그램\(대상\) 번호를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오. 프로그램이 복사됩니다.

![](../_assets/image_262.png)

* 복사될 프로그램과 동일한 번호의 프로그램이 이미 존재하는 경우에는 해당 파일로의 덮어쓰기 여부를 선택해야 합니다.
* 복사할 원본 파일이 없으면 알림 메시지\(“원본 파일이 존재하지 않습니다.”\)가 나타납니다.

{% hint style="info" %}
자동 모드에서는 R115 코드를 사용할 수 없습니다. 반드시 수동 모드에서 사용하십시오.
{% endhint %}



# 8.4 R117 프로그램 삭제

내부 메모리의 프로그램을 개별적으로 삭제합니다.

1.	즐겨찾기 창에서 117을 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

2.	삭제할 프로그램 번호를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오. 삭제 확인창이 나타납니다.

![](../_assets/image_280.png)

* 삭제할 파일이 없으면 알림 메시지\(“파일이 존재하지 않습니다.”\)가 나타납니다.
* 보호 설정된 프로그램을 삭제하려하면 알림 메시지\(“보호된 파일입니다.”\)가 나타납니다

3.	삭제 확인창에서 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오. 선택한 프로그램이 삭제됩니다.

{% hint style="info" %}
자동 모드에서는 R117 코드를 사용할 수 없습니다. 반드시 수동 모드에서 사용하십시오.
{% endhint %}

# 8.5 R210 스폿건 번호 선택

복수의 스폿 용접건\(서보건 또는 공압건\) 사용 시 사용할 스폿건을 선택합니다.

1.	즐겨찾기 창에서 210을 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

2.	사용할 스폿건 번호를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

![](../_assets/image_279.png)

* Hi6 티치 펜던트 화면 좌측의 \[건\] 버튼에 선택한 스폿건 번호가 표시됩니다.
* 스폿건 번호를 변경하면 스폿건 대응 툴 번호에 지정된 툴 번호가 자동으로 변경됩니다. 스폿건 대응 툴 번호는 \[설정 &gt; 4: 응용파라미터 &gt; 1: 스폿용접 &gt; 1: 건번호 대응 툴번호, 건타입 설정\] 메뉴에서 확인할 수 있습니다.

{% hint style="info" %}
* 로봇 기동 중에는 R210 코드를 사용할 수 없습니다.
* 스폿 용접 환경\(\[설정 &gt; 5: 초기화 &gt; 3: 용도설정\] 메뉴의 \[스폿용접\] 항목을 유효로 설정\)에서만 스폿건 번호를 설정할 수 있습니다.
* 선택한 스폿 용접건은 수동으로 건개폐 및 건가압 동작을 실행할 수 있습니다. 스폿 용접 기능에 대한 자세한 내용은 “Hi6제어기 스폿용접 기능 설명서”를 참조하십시오.
{% endhint %}

# 8.6 R211 서보건 가압력 설정

서보건 가압 실행 시 가압력을 수동으로 설정합니다.

1.	즐겨찾기 창에서 211을 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

2.	서보건 가압력을 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

![](../_assets/image_273.png)

* 용접 조건 파일의 가압력은 변경되지 않습니다.
* 입력한 가압력이 서보건 파라미터의 전류 가압력 테이블의 상한치보다 크거나 작으면 경고 메시지가 나타납니다.

{% hint style="info" %}
* 로봇 기동 중에는 R211 코드를 사용할 수 없습니다.
* 스폿 용접 환경\(\[설정 &gt; 5: 초기화 &gt; 3: 용도설정\] 메뉴의 \[스폿용접\] 항목을 유효로 설정\)에서만 스폿건 번호를 설정할 수 있습니다.
* 서보건 가압력 수동 설정에 대한 자세한 내용은 “Hi6제어기 스폿용접 기능 설명서”를 참조하십시오.
{% endhint %}

# 8.7 R212 서보건 이동전극 마모량 프리셋

서보건 이동전극의 마모량을 수동으로 설정합니다.

1.	즐겨찾기 창에서 212를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

2.	이동전극의 마모량을 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

![](../_assets/image_272.png)

{% hint style="warning" %}
설정값을 전극의 실마모량 보다 크거나 작게 설정하면 가압력 불일치나 작업물 간섭 등을 유발할 수 있으므로 주의하십시오.
{% endhint %}

{% hint style="info" %}
* 로봇 기동 중에는 R212 코드를 사용할 수 없습니다.
* 스폿 용접 환경\(\[설정 &gt; 5: 초기화 &gt; 3: 용도설정\] 메뉴의 \[스폿용접\] 항목을 유효로 설정\)에서만 스폿건 번호를 설정할 수 있습니다.
* 서보건 이동전극의 마모량 수동 설정에 대한 자세한 내용은 “Hi6제어기 스폿용접 기능 설명서”를 참조하십시오.
{% endhint %}

# 8.8 R213 서보건 고정전극 마모량 프리셋

서보건 고정전극의 마모량을 사용자가 수동으로 설정하는 기능입니다. 

1.	즐겨찾기 창에서 213를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

2.	고정전극의 마모량을 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

![](../_assets/image_267.png)

{% hint style="warning" %}
설정값을 전극의 실마모량 보다 크거나 작게 설정하면 가압력 불일치나 작업물 간섭 등을 유발할 수 있으므로 주의하십시오.
{% endhint %}

{% hint style="info" %}
* 로봇 기동 중에는 R213 코드를 사용할 수 없습니다.
* 스폿 용접 환경\(\[설정 &gt; 5: 초기화 &gt; 3: 용도설정\] 메뉴의 \[스폿용접\] 항목을 유효로 설정\)에서만 스폿건 번호를 설정할 수 있습니다.
* 서보건 고정전극의 마모량 수동 설정에 대한 자세한 내용은 “Hi6제어기 스폿용접 기능 설명서”를 참조하십시오.
{% endhint %}

# 8.9 R214 동시 용접건 선택

복수의 스폿 용접건\(서보건 또는 공압건\)으로 동시에 용접 작업에 사용할 스폿 용접건 번호를 선택합니다.

1.	즐겨찾기 창에서 214를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

2.	동시 사용할 용접건의 번호를 모두 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

![](../_assets/image_277.png)

* Hi6 티치 펜던트 화면 좌측의 \[건\] 버튼에 선택한 스폿건 번호가 표시됩니다.
* 유형이 서로 다른 스폿 용접건을 선택하면 알림 메시지\(“현재 선택된 GUN의 건 타입을 잘못 설정하였습니다.”\)가 나타납니다.

{% hint style="info" %}
* 로봇 기동 중에는 R214 코드를 사용할 수 없습니다.
* 스폿 용접 환경\(\[설정 &gt; 5: 초기화 &gt; 3: 용도설정\] 메뉴의 \[스폿용접\] 항목을 유효로 설정\)에서만 스폿건 번호를 설정할 수 있습니다.
* 스폿 용접건의 설정 상태는 \[설정 &gt; 4: 응용파라미터 &gt; 1: 스폿용접 &gt; 1: 건번호 대응 툴번호, 건타입 설정\] 메뉴에서 확인할 수 있습니다.
  * 멀티 씽크 건으로 선택되면 수동 가압/개폐 동작을 기존에 선택된 건과 함께 동시에 동작됩니다.
  * 멀티 씽크 건으로 선택되면 GUN LED가 ON되어 있을 경우 SPOT 명령도 멀티 씽크 스폿 형식으로 기록됩니다.
* 선택한 스폿 용접건은 수동으로 조작할 수 있습니다. 스폿 용접 기능에 대한 자세한 내용은 “Hi6제어기 스폿용접 기능 설명서”를 참조하십시오.
{% endhint %}



# 8.10 R215 스폿용접조건 가압력 설정

서보건 용접 시 필요한 가압력을 용접 조건 테이블에 설정합니다. \[설정 &gt; 4: 응용파라미터 &gt; 1: 스폿용접 &gt; 4: 용접데이터 \(조건, 시퀀스\) &gt; 2: 용접조건\] 메뉴에서도 가압력을 설정할 수 있습니다.

1.	즐겨찾기 창에서 215를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

2.	용접조건 번호를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

![](../_assets/image_276.png)

3.	서보건 가압력을 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

![](../_assets/image_264.png)

# 8.11 R220 패널 두께 설정\(Sv\)

서보건 스폿용접 스텝의 기록을 위한 패널 두께를 수동으로 설정합니다.

서보건의 고정전극만 패널에 맞닿은 상태에서 MOVE문과 SPOT 명령문을 동시에 기록하는 원터치 기록을 실행하면 이동전극의 위치는 패널 두께와 마모량을 고려하여 MOVE문에 자동으로 기록됩니다.

1.	즐겨찾기 창에서 220을 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

2.	패널 두께를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

![](../_assets/image_265.png)

{% hint style="info" %}
수동 패널 두께 설정에 대한 자세한 내용은 “Hi6제어기 스폿용접 기능 설명서”를 참조하십시오.
{% endhint %}

# 8.12 R358 서보툴 체인지

서보툴 체인지 시스템에서 서보툴을 수동으로 접속 및 분리합니다.

서보툴 체인지 시스템에서 서보툴을 변경하려면 물리적인 ATC \(자동 툴 체인지\) 장치를 이용하여 전원, 각종 신호 라인을 분리하거나 접속해야 합니다.

서보툴이 서보건인 경우 수동으로 체인지 작업을 수행하려면, 모터가 켜진 상태에서\(인에이블링 스위치 On\) 로봇을 접속 및 분리할 서보건 거치대로 이동한 후 체인지 작업을 실시합니다. 서보툴이 포지셔너 등의 다른 유형인 경우 접속 및 분리 작업을 위한 준비가 완료된 상태에서 체인지 작업을 실시합니다.

R358 서보툴 체인지 파라미터와 예는 다음과 같습니다.

![](../_assets/image_261.png)

R358 코드를 이용한 서보툴 체인지 설정 방법은 다음과 같습니다.

1.	즐겨찾기 창에서 358을 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

2.	체인지 동작 번호\(0: 분리, 1: 접속, 2: 고정\)를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

![](../_assets/image_274.png)

3.	체인지할 용접건 번호를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오. Hi6 티치 펜던트 화면 좌측의 \[건\] 버튼에 선택한 용접건 번호가 표시됩니다.

![](../_assets/image_269.png)

{% hint style="info" %}
* 자동 모드에서는 R358 코드를 사용할 수 없습니다. 반드시 수동 모드에서 사용하십시오.
* 스폿건 번호를 변경하면 스폿건 대응 툴 번호에 지정된 툴 번호가 자동으로 변경됩니다. 스폿건 대응 툴 번호는 \[설정 &gt; 4: 응용파라미터 &gt; 1: 스폿용접 &gt; 1: 건번호 대응 툴번호, 건타입 설정\] 메뉴에서 확인할 수 있습니다.
* 모터가 켜진 상태에서만 서보툴 체인지 설정을 할 수 있습니다.
* 서보툴 체인지에 대한 자세한 내용은 “Hi6제어기 스폿용접 기능 설명서”를 참조하십시오.
{% endhint %}

# 8.13 R359 서보툴 엔코더 전원 ON Relay

서보툴 체인지 시스템에서 서보건을 적용한 경우, 최초 서보건 장착 시 서보건 축의 엔코더를 리셋하기 위해 실행합니다.

1.	즐겨찾기 창에서 359를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

2.	1을 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오. 엔코더에 전원이 투입됩니다.

![](../_assets/image_263.png)

{% hint style="info" %}
* 자동 모드에서는 R359 코드를 사용할 수 없습니다. 반드시 수동 모드에서 사용하십시오.
* 서보건 엔코더의 강제 전원 투입을 해제하려면 제어기의 전원을 끈 후 다시 켜야 합니다. 따라서 엔코더 리셋이 종료되면 제어기의 전원을 껐다 켠 후 서보건 수동 결합을 진행하십시오.
* 서보툴 엔코더 전원 설정 기능은 일반 사용자에게 지원되지 않는 엔지니어용 기능입니다. 이 기능에 대한 자세한 내용은 엔지니어에게 문의하시기 바랍니다.
* 서보툴 엔코더 전원 설정에 대한 자세한 내용은 “Hi6제어기 스폿용접 기능 설명서”를 참조하십시오.
{% endhint %}

{% hint style="warning" %}
엔코더 전원이 강제로 투입된 상태에서는 절대 서보건을 기계적으로 결합하거나 분리하지 마십시오.
{% endhint %}

# 8.14 R361 조그인칭 레벨 설정

R361 조그인칭 레벨 설정 정보는 다음과 같습니다.

![](../_assets/image_541.png)

현재 설정된 레벨의 인칭 거리를 변경하는 방법은 다음과 같습니다.

1.	즐겨찾기 창에서 361을 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

2.	조그인칭 레벨의 단위\(0: 거리, 1: 각도\)를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

![](../_assets/image_270.png)

3.	1을 입력한 경우, 인칭 각도를 입력한 후 \[확인\] 버튼을 터치하거나 &lt;enter&gt; 키를 누르십시오.

![](../_assets/image_266.png)

{% hint style="info" %}
* 자동 모드에서는 R361 코드를 사용할 수 없습니다. 반드시 수동 모드에서 사용하십시오.
* R361 코드를 이용해 설정한 인칭 거리는 현재 설정되어 있는 조그레벨에 대해 설정됩니다. 따라서 현재 조그속도 레벨이 8인 경우, 8i에 해당하는 인칭 거리가 변경됩니다.
* 조그인칭 키가 활성화\(LED On\)된 상태에서만 조그인칭 동작이 가능합니다.
* 조그인칭 레벨 설정 기능은 일반 사용자에게 지원되지 않는 엔지니어용 기능입니다. 이 기능에 대한 자세한 내용은 엔지니어에게 문의하시기 바랍니다.
{% endhint %}

# 9. 속성

아크용접 작업 프로그램을 티칭할 경우 전압, 전류 등 용접 관련 조건뿐만 아니라 위빙과 Retry/Restart, 용접기의 특성 등 아크 전용 기능의 세부적인 설정이 필요합니다. 또한 기본적으로 스텝이나 보조점의 위치를 확인할 경우도 있습니다.



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

# 9.2 move-스텝 위치

작업 프로그램에서 현재 선택된 행에 있는 스텝의 위치를 확인하거나 수정합니다.

# 9.2.1 숨은 포즈 move문

숨은 포즈 move문\(\[기록\] 버튼으로 기록된 스텝, 즉 포즈 변수를 포함하지 않는 move문\)에서 현재 스텝의 위치를 확인하거나 수정합니다.

1. 숨은 포즈로 기록된 이동 명령\(move문\)에서 \[속성\] 버튼을 터치하십시오. 현재 스텝의 위치가 나타납니다.
2. 현재 스텝의 위치를 확인하고 수정하십시오.

![](../../_assets/image_275.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>현재 스텝의 위치 정보입니다.
          이름과 좌표값, 좌표계
          형식 등을 확인하고 설정할
          수 있습니다.</p>
        <ul>
          <li>[이름]: 현재 스텝의 번호입니다.
            스텝 번호를 입력한 후
            &lt;enter&gt; 키를 누르면 해당
            스텝으로 이동합니다.</li>
          <li>좌표값: 현재 스텝의 좌표값입니다.</li>
          <li>커서키를 이용해 항목을
            선택합니다.</li>
          <li>원하는 항목에서 값을
            입력한 후 &lt;enter&gt; 키를 눌러
            변경 내용을 반영합니다.</li>
          <li>좌표계 형식이 엔코더로
            설정된 경우에는 좌표값이
            변경되지 않습니다.</li>
          <li>[좌표계]: 현재 스텝의
            위치를 표현할 좌표계
            형식입니다.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[이전]/[다음]: 이전 또는
            다음 스텝의 정보를 표시합니다.</li>
          <li>[원래값]: 현재 스텝의
            원래 숨은 포즈값을 표시합니다.</li>
          <li>[현재 로봇 포즈]: 현재
            로봇이 취하고 있는 자세의
            값을 표시합니다.</li>
          <li>[로봇 이동]: [로봇 이동]
            버튼을 터치하여 기록된
            스텝의 위치로 로봇을
            움직입니다. (조그)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

1. \[기록\] 버튼을 터치하십시오. 작업 프로그램에 변경 내용이 저장되고 작업이 종료됩니다.
2. &lt;esc&gt; 키를 눌러 종료하면 변경 내용이 저장되지 않습니다.

{% hint style="info" %}
* \[로봇 구성 형태\]를 미지정으로 설정하는 경우 로봇은 현재 위치에서 가장 가깝게 로봇 형태를 지정합니다.
* 로봇 구성 형태에 따른 지정은 “[2.3.2.2 베이스 및 로봇 기록 좌표](../../operation/step/step-pose-modify/base-robot-crd-sys.md)”를 참조하십시오.
{% endhint %}

# 9.2.2 포즈기록 move문, 포즈 대입문

포즈 변수를 포함하는 move문 또는 포즈 변수 대입문에서 포즈 변수값을 편집합니다.

1. 포즈 변수로 기록된 이동 명령\(move문\)에서 \[속성\] 버튼을 터치하십시오. 포즈 변수 설정 화면이 나타납니다.
2. 현재 포즈 변수를 확인하고 수정하십시오.

![](../../_assets/image_260.png)

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
        <img src="../../_assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>현재 포즈 변수 정보입니다.
          이름과 좌표값, 좌표계
          형식 등을 확인하고 설정할
          수 있습니다.</p>
        <ul>
          <li>[이름]: 현재 포즈 변수의
            이름입니다.</li>
          <li>좌표값: 현재 포즈 변수의
            좌표값입니다.
            <ul>
              <li>커서키를 이용해 항목을
                선택합니다.</li>
              <li>원하는 항목에서 값을
                입력한 후 &lt;enter&gt; 키를 눌러
                변경 내용을 반영합니다.</li>
              <li>좌표계 형식이 엔코더로
                설정된 경우에는 좌표값이
                변경되지 않습니다.</li>
            </ul>
          </li>
          <li>[좌표계]: 현재 포즈 변수의
            위치를 표현할 좌표계
            형식입니다.</li>
          <li>[로봇 구성 형태]: 로봇의
            위치를 기술할 때 그 기구의
            특성상 복수의 해가 존재하므로,
            그 형태를 유일하게 기술하기
            위한 로봇 형태(Configuration)를
            지정한 것입니다.
            <ul>
              <li>좌표계 형식이 베이스
                또는 로봇으로 설정된
                경우에만 사용할 수 있습니다.</li>
              <li>로봇 구성 형태에 대한
                자세한 내용은 “<a href="../../operation/step/step-pose-modify/">2.3.2 스텝 위치 기록 및 변경</a>”을
                참조하십시오.</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[확인]: 변경 내용을 저장합니다.</li>
          <li>[이전]/[다음]: 이전 또는
            다음 변수의 정보를 표시합니다.</li>
          <li>[원래값]: 현재 스텝의
            원래 숨은 포즈값을 표시합니다.</li>
          <li>[현재 로봇 포즈]: 현재
            로봇이 취하고 있는 자세의
            값을 표시합니다.</li>
          <li>[로봇 이동]: [로봇 이동]
            버튼을 터치하여 기록된
            포즈 변수의 위치로 로봇을
            움직입니다. (조그)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

1. \[기록\] 버튼을 터치하십시오. 작업 프로그램에 변경 내용이 저장되고 작업이 종료됩니다.
2. &lt;esc&gt; 키를 눌러 종료하면 변경 내용이 저장되지 않습니다.

# 9.3 스폿용접 펑션

프로그램 작성 중 SPOT 명령문을 기록했을 때, 수동 모드에서 스폿용접 펑션 위치에 커서를 두고 \[속성\] 버튼을 터치하면 응용 파라미터의 설정 메뉴 화면에서 \[1: 스폿용접\] 메뉴가 하이라이트 표시됩니다. 스폿용접 기능을 이용하면, 서보건으로 스폿용접할 때, 용접 조건과 용접 시퀀스의 내용을 빠르게 수정할 수 있습니다.

![그림 77 스폿용접 펑션](../_assets/image_278.png)

{% hint style="info" %}
* \[설정\] 버튼 &gt; \[4: 응용 파라미터 &gt; 1: 스폿용접\] 메뉴를 터치하여 스폿용접 기능을 사용할 수 있습니다.
* 스폿용접 기능에 대한 자세한 내용은 “Hi6 제어기 스폿용접 기능 설명서”를 참조하십시오.
{% endhint %}

# 10. 로봇 언어

로봇 언어에 대한 자세한 내용은 "[Hi6 로봇언어 기능 설명서](https://hrbook-asoe72.web.app/#/view/doc-hrscript/korean/README)"를 참조하십시오.
# 별첨

  


# 산업안전보건기준에 관한 규칙 및 안전검사 고시

당해 산업용 로봇은 산업안전보건기준에 관한 규칙 및 안전검사 고시(검사 대상일 경우)의 검사 기준을 고려하여 설치하여야 한다.

"[산업안전보건기준에 관한 규칙](https://hrbook-hrc.web.app/#/view/rules-on-occupational-safety-and-health-standards/korean/README)"
# 품질보증

"[품질보증](https://hrbook-hrc.web.app/#/view/quality-assurance/korean/README)"
