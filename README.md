# git-practice
git 연습용 원격 저장소

원격 저장소에서 협업하는 방법

시도해보는 방법 
※반드시 연습용 원격 저장소에서 연습하기 

연습용 원격 저장소 링크 : https://github.com/KIT452/git-practice

1. fork한 레포 clone하기

2. clone한 레포에 원격 저장소 알리기
`git remote add upstream https://github.com/KIT452/git-practice.git`

3. 모든 remote가 제대로 설정되었는지 확인하기  
`git remote -v`  
`origin` 으로는 fork한 본인의 저장소  
`upstream` 으로는 원래 원격 저장소  
가 나오면 제대로 설정끝

4. `git branch -v`
현재 어떤 브랜치가 있는지 확인
`develop` <- 존재하면 OK

5. `git checkout -b feature/android/home` <- 사용하는 마일스톤명으로 할 때 변경할 것!
branch를 생성하면서 branch로 이동하는 명령어

6. 개발 진행 후 git add 후, commit 메시지 작성
  - add 시에는 반드시 본인이 변경한 파일만 추가됐는지 git status로 확인 必

7. git push origin feature/android/home <-원격 저장소로 PR을 보내는 것

8. git push 한 이후에 본인의 fork한 저장소에 들어가면 compare&mare가 자동으로 뜸. 버튼을 누르면 PR 창이 뜸. 또는 new pr 버튼으로 직접 생성도 가능.
  - 병합할 대상은 반드시 develop 브랜치로 설정
  - pr 관련 링크 https://velog.io/@werds7890/Pull-request-%EC%BD%94%EB%93%9C%ED%95%A9%EC%B9%98%EA%B8%B0merge

9. 기본적으로 스프린트가 업로드 될 때 처음 할 일
```
git fetch upstream 
git checkout develop
git merge upsream/develop
git push
```
를 사용해서 원격저장소의 있는 값들을 업데이트 해야함!
