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

![](../../../.gitbook/assets/image%20%28210%29.png)

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#xBC88;&#xD638;</th>
      <th style="text-align:left">&#xC124;&#xBA85;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c1.png" alt/>
      </td>
      <td style="text-align:left">
        <p>&#xCDA9;&#xB3CC;&#xAC80;&#xC9C0; &#xAE30;&#xB2A5;&#xC758; &#xC0AC;&#xC6A9;
          &#xC635;&#xC158; &#xC815;&#xBCF4;&#xC785;&#xB2C8;&#xB2E4;. &#xC774; &#xAE30;&#xB2A5;&#xC758;
          &#xC0AC;&#xC6A9; &#xC5EC;&#xBD80;&#xC640; &#xBBFC;&#xAC10;&#xB3C4;, &#xC800;&#xC18D;
          &#xCDA9;&#xB3CC;&#xAC80;&#xC9C0; &#xAE30;&#xB2A5; &#xC0AC;&#xC6A9; &#xC5EC;&#xBD80;&#xB97C;
          &#xC124;&#xC815;&#xD560; &#xC218; &#xC788;&#xC2B5;&#xB2C8;&#xB2E4;.</p>
        <ul>
          <li>[&#xAE30;&#xB2A5; &#xC0AC;&#xC6A9;]: &#xCDA9;&#xB3CC;&#xAC80;&#xC9C0;
            &#xAE30;&#xB2A5;&#xC758; &#xC0AC;&#xC6A9; &#xC5EC;&#xBD80;&#xB97C; &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>[&#xBBFC;&#xAC10;&#xB3C4;]: &#xCDA9;&#xB3CC;&#xAC80;&#xC9C0; &#xBBFC;&#xAC10;&#xB3C4;&#xB97C;
            &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;. &#xAC12;&#xC774; &#xD074;&#xC218;&#xB85D;
            &#xCDA9;&#xACA9;&#xC5D0; &#xBBFC;&#xAC10;&#xD558;&#xAC8C; &#xB3D9;&#xC791;&#xD569;&#xB2C8;&#xB2E4;.(&#xAE30;&#xBCF8;
            &#xC124;&#xC815;&#xAC12;: 100%)</li>
          <li>[&#xC800;&#xC18D; &#xCDA9;&#xB3CC; &#xAC80;&#xC9C0;]: &#xC800;&#xC18D;
            &#xCDA9;&#xB3CC;&#xAC80;&#xC9C0; &#xAE30;&#xB2A5;&#xC758; &#xC0AC;&#xC6A9;
            &#xC5EC;&#xBD80;&#xB97C; &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.
            <ul>
              <li>[&#xAE30;&#xC900; &#xC2DC;&#xAC04;]: &#xCDA9;&#xB3CC;&#xB85C; &#xD310;&#xB2E8;&#xD558;&#xAE30;
                &#xC704;&#xD55C; &#xAE30;&#xC900; &#xC2DC;&#xAC04;&#xC744; &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;.
                &#xAE30;&#xC900; &#xC2DC;&#xAC04; &#xB3D9;&#xC548; &#xCDA9;&#xACA9;&#xB825;&#xC774;
                &#xBC1C;&#xC0DD;&#xD558;&#xBA74; &#xCDA9;&#xB3CC;&#xB85C; &#xD310;&#xB2E8;&#xD569;&#xB2C8;&#xB2E4;.</li>
              <li>[&#xB9C1;&#xD06C; &#xC18D;&#xB3C4;]: &#xC800;&#xC18D;&#xC73C;&#xB85C;
                &#xD310;&#xB2E8;&#xD558;&#xAE30; &#xC704;&#xD55C; &#xAE30;&#xC900; &#xC18D;&#xB3C4;&#xB97C;
                &#xC124;&#xC815;&#xD569;&#xB2C8;&#xB2E4;. &#xAE30;&#xC900; &#xB9C1;&#xD06C;
                &#xC18D;&#xB3C4; &#xC774;&#xD558;&#xC5D0;&#xC11C;&#xB9CC; &#xC800;&#xC18D;
                &#xCDA9;&#xB3CC;&#xC744; &#xAC80;&#xC0AC;&#xD569;&#xB2C8;&#xB2E4;.</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../../../.gitbook/assets/c2.png" alt/>
      </td>
      <td style="text-align:left">
        <ul>
          <li>[OK]: &#xBCC0;&#xACBD; &#xB0B4;&#xC6A9;&#xC744; &#xC800;&#xC7A5;&#xD569;&#xB2C8;&#xB2E4;.</li>
          <li>[ALL &#xCD08;&#xAE30;&#xD654;]: &#xBAA8;&#xB4E0; &#xC0AC;&#xC6A9; &#xC635;&#xC158;
            &#xC124;&#xC815;&#xAC12;&#xC744; &#xCD08;&#xAE30;&#xD654;&#xD569;&#xB2C8;&#xB2E4;.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

