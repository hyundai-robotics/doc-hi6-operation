# 11.1.5 기타 폴더들

## apps/

MAIN측에서 실행되는 플러그인(plug-in) 앱들이 설치, 저장되는 폴더입니다.


## fbrr/

파일 기반 로봇정보 레지스트리 (File Based Robot Registry) 폴더입니다.  
각 로봇 기구 모델별 정보 파일(.fbr)들이 보관됩니다. 새로운 모델 정보 파일을 추가하면, 시스템 초기화 시 해당 모델을 선택하여 로봇 시스템을 구성할 수 있습니다.


## gather/

시계열 데이터를 수집하는 게더링 (gathering) 기능의 결과 파일 (.GDT) 저장 폴더입니다.


## help/

로봇언어 HRScript의 html 도움말이 저장되는 폴더입니다.


## roblang/

로봇언어 HRScript의 문법 파일이 저장되는 폴더입니다.

* procs_?.json

  category별 프로시저 문법 파일

* funcs_?.json

  category별 함수 문법 파일

* svars_?.json

  category별 시스템 변수 문법 파일
