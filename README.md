# commit 메시지 수정
---> git commit --amend
vim 에디터
### 저장 하고 종료 : ESC ---> :wq
### 저장하지 않고 종료 : ESC ---> :q!
## 변경 사항이 없을 때 나가기 : ESC ---> :q
(메시지를 변경하지 않아도 타임스탬프가 변경되기 때문에 해시값이 바뀐다)

commit의 Hash(해시)값 확인
---> git log --oneline
Hash 값? : 식별 값 : 1. 고유한 값 2. 변경 불가능

====================================================

revert & reset

git revert : 특정 commit을 없었던 일로 만드는 작업
주의) second commit 없었던 일로 되는데, second commit 삭제되지 않고 새로운 commit 작성

git reset : 이전 commit으로 되돌리기
1. --soft : commit의 기록이 staging area에 남아있다.
2. --mixed : commit 기록이 working directory에 남아있다.
3. --hard : commit에 기록된 내역들을 모두삭제

===================================================

staging area에서  working directory로 되돌리기
1. git rm --cahced a.txt : git 저장소에 commit이 없는 경우
2. git restore --staged a.txt : git 저장소에 commit이 존재하는 경우