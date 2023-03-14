## 기본 세팅

0. 프로젝트를 위한 폴더 생성 후 vscode로 열기
   1. `mkdir 프젝폴더명`
   2. ✨ `.gitignore` 파일 생성
   3.  touch .gitignore : 터미널 명렁어
   4.   gitignore.io 에서 `visualStudioCode`, `python`, `django` 선택해서 복붙
1. 가상환경 생성
   1.  `python -m venv 가상환경 폴더명`
2. 가상환경 활성화
   1.  `source venv/Scripts/activate`
   2.  tap을 이용해서 문서가 있는지 확인 가능
   3.  맥 : `source venv/Bin/activate`
   4.  상단에 (venv) 확인
   5.  pip list를 통해 정상인지 확인(패키지가 없으면 정상)
3. 장고 설치
   1. `pip install django==version`
   2. 만약 문서가 제공된다면 `pip install -r requirements.txt`
4. 가상환경에 설치된 모듈 문서로 남기기
   1. `pip freeze > requirements.txt`

-----------
 
## 장고 프로젝트 시작

1. 프로젝트 생성
   1. `django-admin startproject <name> .`
   2. 마지막에 .이 있는 경우는 현재 폴더에 바로 생성, 없는 경우는 <name> 폴더 만들고 그 내부에 생성
2. 앱 생성
   1.  `python manage.py startapp <name>`
   2.  앱 이름은 복수형으로 작성하는 것을 권장
3. [아묻따] settings.py -> installed_apps에 앱 이름을 문자열 형태로 저장
   1. `,`(쉼표) 까먹지 말기
   2. articles 오타 조심하기