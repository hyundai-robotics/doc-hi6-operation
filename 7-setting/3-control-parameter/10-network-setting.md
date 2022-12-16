# 7.3.10 네트워크

이더넷 네트워크 설정을 할 수 있습니다.

1.	\[2: 제어 파라미터 &gt; 9: 네트워크 &gt; 1: 사용환경 설정 \]으로 진입하십시오.

2.	LAN(Public)에서 각 파라미터 설정이 가능합니다. 클래스 C형의 IP 주소를 바탕으로 구성하십시오.

3.	Public LAN은 포트포워딩이 가능합니다.

4.	설정 파라미터들은 제어기 재부팅시 적용됩니다.

![](../../_assets/image_551.png)

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
      <td style="text-align:left">LAN 포트 설정 탭입니다. LAN(Public)은 수정이 가능하며, LAN1(이더캣), LAN2(T/P-main)은 수정이 불가능합니다.
	  </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../_assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <br />포트설정을 변경합니다. IP, 서브넷 마스크, 게이트웨이는 수정이 가능합니다.
          <li><b>IP : </b> 연결할 IP 주소를 설정합니다.</li>
          <li><b>서브넷 마스크 : </b> 서브넷 마스크를 설정합니다. 클래스 C기준 255.255.255.0을 사용합니다.</li>
          <li><b>게이트웨이 : </b>게이트웨이를 설정합니다. 3번째 정보까지는 IP주소와 동등합니다. 4번째 주소를 0 혹은 255로 설정하면 Broadcast가 가능합니다.
          </li>
        </ul>
      </td>
    </tr>
	<tr>
      <td style="text-align:left">
        <img src="../../_assets/c3.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>포트포워딩 선택 : </b> 포트포워딩 기능을 활성화합니다. 포트포워딩 기능은 LAN3(Public)탭에 있습니다. LAN1(이더캣)은 적용되지 않습니다.</li>
        </ul>
      </td>
    </tr>
	<tr>
      <td style="text-align:left">
        <img src="../../_assets/c4.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li><b>[OK]</b>: 설정을 저장합니다. 시스템을 재부팅한 후 변경사항이 적용됩니다.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}

포트포워딩은 IP나 포트를 라우터를 통하여 다른 IP나 포트로 전달하는 기능입니다. Hi6 제어기는 포트포워딩 기능이 있습니다.

예시) Device1(192.168.1.10 | 255.255.255.0 | 192.168.1.1)은 T/P(192.168.2.X | 255.255.255.0 | 192.168.2.X)와 3번째 주소값이 다름에도 연결이 가능합니다.

아래의 정보는 포트포워딩 설정방법을 다룹니다.

* 지원 IP : 클래스 C 형식(192.168.XX.XX) 장비들은 포트포워딩에 사용 가능합니다.
* 지원 서브넷 : 각 포트는 3번째 스텝까지 같아야합니다. 이를테면 LAN3(Public)는 192.168.1.X IP와 연결됩니다.
* 기본 게이트웨이 : 192.168.X.1이 초기 설정값이며, 192.168.X.255로 설정시 브로드캐스팅이 가능합니다.

{% endhint %}
