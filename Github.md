## Git bash 몇가지 명령어

- ls : bash가 실행된 환경에서의 목록 확인
- clear : bash 화면 지우기
- mkdir : make directory, 디렉토리 만들기
    - ex) mkdir 폴더명
- cd : change directory, 디렉토리 이동
    - ex) cd 위치
- cd .. : 상위 폴더로 이동
- pwd : print working directory, 주소 확인
- 알파벳 일부분 쓰고 tap키를 누르면 일치하는 단어로 자동완성
- find -name 파일명 : 파일 찾기
- bash : cli 프로그램
- rmdir : remove directory
    - ex) rmdir 폴더명
- rm : 파일을 삭제하는 명령어
- rm -rf : not empty directory 강제 삭제
    - -r : recursive 재귀적으로 반복해 나가는 방식
    - -f : force 문제가 있어도 물어보지 말고 삭제(가급적 안쓰는 것이 좋음 아주 조심)
- 드래그 하면 복사가 됨
- touch : 파일을 생성하는 명령어
- start, open : 폴더/파일을 여는 명령어 (윈도우,맥)
- ls -a : 숨겨진 파일까지 리스트로 보여줌 (-는 옵션을 뜻한다)

## Repository

특정 디렉토리를 버전 관리 하는 저장소

- git init 명령어로 로컬 저장소를 생성
- .git 디렉토리에 버전 관리에 필요한 모든 것이 들어있음
---

*저장소에 파일 올리는 법*

```bash
#local repo -> github repo

mkdir git_test   #폴더 추가
cd git_test   #이동
git init   #local repo 생성
touch README.md   #README.md파일 생성
git add README.md   #working->staging
git commit -m "README.md"   #staging->local repo

#github에서 repo생성 후 3개 입력
git remote add origin https://github.com/주소 #github repo 와 지정되어있는  local repo (.git) 연결하는 명령어
git branch -M main
git push -u origin main #local repo->github repo

#앞으로 계속 추가할 때
git add 파일명
git commit -m "message"
git push origin main
```

```bash
#github repo -> local repo

#github에서 repo생성 후
git clone 주소
```

*생길 수 있는 변수들*

1. git init를 desktop에 생성해버렸다.
   
        rm -rf .git

2. 변경한 내용을 알고 싶을 때

        git diff 파일명

3. 상태를 돌리고 싶을 때 (unstaging)

        git restore --staged 파일명

4. 현재 상태를 알고 싶을 때

        git status

5. 기록을 확인하고 싶을 때

        git log

6. github repo (업데이트된)자료를 local repo로 가져오고 싶을 때 

        git pull

7. 연결 확인 (local 과 github)

        git remote -v

8. commit message 수정

        git commit --amend

9. 정보가 필요할 때
    
        git [명령어] --help

10. 