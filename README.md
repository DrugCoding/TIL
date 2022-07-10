# TIL (Today I Learned)
# 절대 규칙
- 무슨 일이 있어도 하루 1commit
- 간단하게라도 꼭 정리하기
---
## 7/5 - Git의 시작
- 로컬저장소 만드는 단계
  - git init
  - git add
  - git status
  - git commit -m "커밋 메시지"
  - git log (--oneline , --2 --oneline)

## 7/6 - Github의 시작
- 원격저장소 만들기
  - Your repositories 에 들어가서 만든다.
- 로컬저장소에 원격저장소 등록
  - git remote add origin <원격저장소 주소>
    - 주소가 잘 들어갔는지 확인 명령어 : git remote -v
- 로컬저장소의 커밋을 원격저장소로 올리기
  - git push origin master
- git pull 과 git clone
  - 로컬저장소가 있을 때 pull / 통째로 받아와야 할 때 clone
  
## 7/7 - Git branch 그리고 협업
- branch 생성
  - git branch "branch name"
- branch 이동
  - git chechout "branch name"
    - 브랜치 생성과 동시에 이동 : git checkout -b "branch name"
- branch 목록 확인
  - git branch
- branch 이동해서 작업 후 marge
  - git checkout "blabla" --add commit--> git checkout master --> git marge blabla (꼭 원래의 HEAD에 와서 marge 할 것)
- branch 삭제
  - git branch -d "blabla" (다 쓴 branch는 제거해도 commit이 사라지지는 않음)
- branch conflict(브랜치 충돌)
  - 혼자 쭉 하는경우/다른 파일을 수정하는 경우 상관없음
  - 같은 파일을 수정하는 경우 conflict 일어남
    - 충돌 된 부분 수정 --> git add . --> git commit (code 보고 닫는다)