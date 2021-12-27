# 2) Git basic command  (git 명령어 정리) 

<br /> 

## 1. 먼저 github에 가입후, 이메일 설정

    git config --global user.name "Write your name"
    git config --global user.email "Write your email"

이는 반드시 Github.com을 가입할 때 사용한 이메일이어야한다.

<br />

## 2. 로컬 저장폴더 생성

    mkdir ~/MyProject 
이제 로컬 장소를 만들자. ~/를 입력하면 로컬 컴퓨터의 최상위 단계 디렉토리가 보일 것이다.

<br />

## 3. 디렉토리 바꾸기
    cd ~/MyProject

다음의 디렉토리로 옮겨간다.

<br />

## 4. 이 디렉토리가 로컬 깃 저장소라고 컴퓨터에 말해줌
    
    git init 

<br />

## 5. 로컬 저장소와 깃허브 저장소를 연결.
    git remote add origin https://github.com/username/myproject.git
 remote는 origin의 설명자이며 origin은 로컬 컴퓨터가 아닌 온라인 어딘가를 가리킨다는 것이다.

<br/>

## 5-1. 다른 원격저장소 생성

    git remote add memo https://github.come/username/memo.git
원격 저장소의 별명을 설정할 수 있고, 여러개의 원격 저장소를 로컬 저장소로 저장할 수 있다.

<br/>

## 5-2. 기존 원격 저장소 URL 변경

    git remote set-url origin https://github.com/username/myproject2.git

<br/>

## 5-3. 기존 원격 저장소 URL 삭제

    git remote rm 원격 저장소 별명

<br/>

## 6. 로컬 저장소가 알고있는 원격 저장소의 모든 항목을 보여줌
    
    git remote -v

<br/>

## 7. 원격 저장소를 지역 저장소로 복제

    git clone https://github.com/git/git.git
    
<br/>

## 8. github에 올릴 파일 하나를 로컬저장소에 copy

    git add new.md
 파일을 수정하고 반영하고자 할 때도 이 명령어를 사용한다.
 
<br/>
## 8-1. 파일의 이름을 수정

    git mv 원래파일이름 변경할파일이름

<br/>

## 8-2. add 했던거 취소

    git reset HEAD~

<br/>

## 9. commit 버전관리
    
    git commit -m "변경된 내용사항쓰기"
git add 명령어로 새로운 파일을 인식후, commit으로 버전관리를 시작하게 된다. 그러나 아직, 원격저장소에는 반영되지 않았다.

<br/>

## 9-1. repository에 처음 commits할 내용 만들때
   
    touch initial
    git add initial
    git commit -m "initial commit"
touch는 create하는 것을 의미. 

## 10. 원격저장소에 파일을 적용

    git push -u origin master
 -u는 원격저장소로부터 업데이트를 받은 후 push를 한다는 의미이므로 습관적으로 사용하는 것이 좋다.
 master는 branch 이름. branch가 별로 의미 없을 때는 그냥 master 사용. branch 날려버리면 branch 안에 작업 들을 한꺼번에 날릴 수 있어 큰 프로젝트나 협업작업할 때 편리.
 
<br/>

## 12. 원격파일 로컬저장소에 저장

    git pull origin master
   
<br/>

## 13. master외의 branch 생성하고 싶으면,

     git branch <branchname>
     
## 14. branch 이동
    git checkout <branchname>
    
## 15. merge
    git merge <branchname>
    
## 16. ammend (commit 수정)
    git add <filename>
    git commit --amend
    
## 17. stash (commit하기는 싫고, 잠깐 임시저장 해놓고 싶을 때)
    git stash save <이름>
    git stash apply
    
## 18. git reset (위험하니까 혼자 쓰는 브랜치에서만 사용하자)
    git log --oneline -5
    git reset --hard <버전명>
    git push --force
    
## 19. revert (특정한 커밋의 변경사항을 되돌려줘서 새로운 커밋을 만듬, master 브랜치에서 force하는 건 위험하니까)
    git revert <버전명>
    
## 20. Cherry-pick (특정 커밋 하나만 가져와서 현재 브렌치에 붙임)
    git log # 가져오고 싶은 commit 이름 확인
    git checkout <branch name> # cherry-pick으로 추가하려는 branch로 이동
    git cherry-pick <버전명>
 
## 21. 현재 git 상황 체크
    git status
    
## 22. git log로 커밋 확인
    git log
