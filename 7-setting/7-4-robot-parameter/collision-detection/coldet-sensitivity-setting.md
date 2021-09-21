# 7.4.8.1 충돌검지 민감도 설정

충돌검지 민감도는 JOB 프로그램에서 명령어로 조정할 수 있습니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#xD56D;&#xBAA9;</th>
      <th style="text-align:left">&#xB0B4;&#xC6A9;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">&#xBA85;&#xB839;&#xC5B4;</td>
      <td style="text-align:left">ColDet Sensitivity</td>
    </tr>
    <tr>
      <td style="text-align:left">&#xC124;&#xBA85;</td>
      <td style="text-align:left">&#xCDA9;&#xB3CC;&#xAC80;&#xC9C0; &#xBBFC;&#xAC10;&#xB3C4; &#xBCC0;&#xACBD;</td>
    </tr>
    <tr>
      <td style="text-align:left">&#xC785;&#xB825; &#xBC29;&#xBC95;</td>
      <td style="text-align:left">command &#x2192; MOTION &#x2192; colsense</td>
    </tr>
    <tr>
      <td style="text-align:left">&#xBB38;&#xBC95;</td>
      <td style="text-align:left">ColDet Sensitivity=100</td>
    </tr>
    <tr>
      <td style="text-align:left">&#xD30C;&#xB77C;&#xBBF8;&#xD130;</td>
      <td style="text-align:left">0 ~ 200 (0: &#xAE30;&#xB2A5; &#xBB34;&#xD6A8;, &#xBBFC;&#xAC10;&#xB3C4;
        &#xAC12;&#xC774; &#xD074;&#xC218;&#xB85D; &#xCDA9;&#xACA9;&#xC5D0; &#xBBFC;&#xAC10;&#xD558;&#xAC8C;
        &#xB3D9;&#xC791;)</td>
    </tr>
    <tr>
      <td style="text-align:left">&#xC608;</td>
      <td style="text-align:left">
        <p>[&#xCDA9;&#xB3CC;&#xAC80;&#xC9C0;] &#xBA54;&#xB274;&#xC5D0;&#xC11C; &#xBBFC;&#xAC10;&#xB3C4;&#xB97C;
          100%&#xB85C; &#xC124;&#xC815;&#xD55C; &#xACBD;&#xC6B0;</p>
        <p>S1 ~ S2: &#xBBFC;&#xAC10;&#xB3C4; 100%&#xB85C; &#xAC80;&#xC9C0; / S3 ~
          S4: &#xBBFC;&#xAC10;&#xB3C4; 50%&#xB85C; &#xAC80;&#xC9C0;</p>
        <p>
          <img src="../../../.gitbook/assets/coldet-sensitivity.png" alt/>
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

