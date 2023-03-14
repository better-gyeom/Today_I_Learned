## 기본 세팅

0. 프로젝트를 위한 폴더 생성 후 vscode로 열기
   - `mkdir 프젝폴더명`
   - ✨ `.gitignore` 파일 생성
     - touch .gitignore : 터미널 명렁어
     - gitignore.io 에서 `visualStudioCode`, `python`, `django` 선택해서 복붙
1. 가상환경 생성
   - `python -m venv 가상환경 폴더명`
2. 가상환경 활성화
   - `source venv/Scripts/activate`
   - tap을 이용해서 문서가 있는지 확인 가능
   - 맥 : `source venv/Bin/activate`
   - 상단에 (venv) 확인
   - pip list를 통해 정상인지 확인(패키지가 없으면 정상)
3. 장고 설치
   - `pip install django==version`
   - 만약 문서가 제공된다면 `pip install -r requirements.txt`
4. 가상환경에 설치된 모듈 문서로 남기기
   - `pip freeze > requirements.txt`

-----------
 
## 장고 프로젝트 시작

1. 프로젝트 생성
   1. `django-admin startproject <name> .`
2. 앱 생성
   - `python manage.py startapp articles`
3. [아묻따] settings.py -> installed_apps에 'articles' 추가
   - `,`(쉼표) 까먹지 말기
   - articles 오타 조심하기