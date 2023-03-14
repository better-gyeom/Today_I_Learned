## 기본 세팅

1. 가상환경 생성
   - python -m venv venv
2. 가상환경 활성화
   - source venv/Scripts/activate
   - tap을 이용해서 문서가 있는지 확인 가능
3. 가상환경에 설치된 모듈 문서로 남기기
   - pip freeze > requirements.txt
4. 장고 설치
   - pip install django==version
-----------

## 장고 프로젝트 세팅

1. 프로젝트 생성
   - django-admin startproject <name> .
2. 앱 생성
   - python manage.py startapp articles
3. [아묻따] settings.py -> installed_apps에 'articles' 추가
   - `,`(쉼표) 까먹지 말기
   - articles 오타 조심하기