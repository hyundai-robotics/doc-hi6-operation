# 11.1.2 project/


로봇의 설정, 교시, 상태가 보관되는 가장 중요한 폴더입니다.  
제어기 시스템을 백업, 복원할 때는 이 폴더가 핵심입니다.


## project/

각종 설정 파일들과 제어기의 전원 OFF (정전) 직전에 저장되는 상태 백업 파일들이 보관되는 폴더입니다.
상태 백업은 아래와 같은 목적으로 제어기 전원 OFF 시 저장되는 정보입니다.

	- 전원 OFF 전 작업을 전원 ON 후 이어서 수행   
	  (단, 로봇 응용이나 플러그인 등 복잡한 작업의 경우, 이어서 할 수 없는 경우도 있습니다.)
	- 전원 OFF의 신호 출력을 전원 ON 후 유지


* arc_weld.json
  
  아크 용접 응용 설정 파일

* arc_weld_bkup.json
  
  전원 OFF 직전의 아크 용접 응용 상태 백업 데이터

* calibration.json

  로봇 캘리브레이션 설정 파일

* context.json

  모든 task의 .job 실행 문맥.  
  즉, 실행 커서가 진행된 위치, .job들이 call된 이력과 인수값, 지역변수값 등

* dout.json

  전원 OFF 직전의 범용 digital 신호 출력값

* force_control.json

  힘 제어 설정

* hi6_proj.json
  
  메인 프로젝트 파일. 대부분의 기본 기능 설정이 여기에 저장됨.

* kw.json

  전원 OFF 직전의 내장PLC kw 릴레이값

* maintenance.json

  각종 유지보수 정보, 시스템 정보
  로봇 모델, 축 수, 가동 시간, 소프트웨어 버전, 잔여 메모리와 스토리지, 시스템 코드, 시스템 thread별 수행 시간

* motion_bkup.bin

  전원 OFF 직전의 로봇 모션과 관련된 백업 데이터

* mw.json
  
  전원 OFF 직전의 내장PLC mw 릴레이값

* playback_bkup.bin

  전원 OFF 직전의 .job 실행과 관련된 백업 데이터

* sealing.json

  실링 응용 설정 파일

* sout.json

  전원 OFF 직전의 시스템 신호 출력값

* spot_weld.json

  스폿 용접 응용 설정 파일

* spot_weld_bkup.json

  전원 OFF 직전의 스폿 용접 응용 상태 백업 데이터

* svtool_change.json

  서보 툴 체인지를 위한 부가축 설정 파일

* version.json

  소프트웨어 버전업 후 첫 부팅 시 해야할 데이터 업데이트의 판단을 위한 정보. (현재 버전번호)
  

## project/jobs/
  
교시 프로그램 (.job) 들이 보관되는 폴더입니다.


## project/lads/
  
내장PLC 래더 프로그램 (.lad) 들이 보관되는 폴더입니다.


## project/safety/
  
(Hi7 제어기 이상) 안전기능(Functional Safety)의 설정 파일이 보관되는 폴더입니다.

* safety_parameter.json

  안전기능의 설정 파일

* safety_parameter.json.cert

  안전기능 설정의 인증 파일.  
  올바른 암호와 함께 설정을 저장했을 때, 유효한 인증이 발급됩니다. 유효하지 않으면, 제어기가 동작하지 않습니다.


## project/vars/

변수와 alias들이 보관되는 폴더입니다.

* aliases.json

  로봇언어 alias 파일

* *.csv

  최상위 배열 파일들 (comma-separated values 포맷)

* vars.json

  전역변수 파일
