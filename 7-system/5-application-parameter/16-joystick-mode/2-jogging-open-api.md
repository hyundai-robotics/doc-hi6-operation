# 7.5.16.2 조깅(open-api)

open-api 통신에 대해서는 별도의 설명서를 참고하십시오. <br>
로봇 조깅을 위해서 사용되는 url주소와 body에 대한 정보는 하기와 같습니다 .

* url : POST /project/robot/joystick/joy
* body <br>
    axis : double형 배열로 구성. axis[0]는 J1에 해당하며 값이 -1이면 왼쪽, +1이면 오른쪽으로 이동을 의미함<br>


{% hint style="info" %}
300ms 동안 데이터 수신이 없으면 조깅 동작을 중단합니다. 
{% endhint %}
