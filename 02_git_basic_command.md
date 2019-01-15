# 2) Git basic command  (git 명령어 정리) 

## 1. 먼저 github에 가입후,

    git config --global user.name "Write your name"
    git config --global user.eamil "Write your email"

이는 반드시 Github.com을 가입할 때 사용한 이메일이어야한다.


## 2. 이제 로컬 장소를 만들자. ~/를 입력하면 로컬 컴퓨터의 최상위 단계 디렉토리가 보일 것이다.

    mkdir ~/MyProject 


## 3. 다음의 디렉토리로 옮겨간다.

    cd ~/MyProject


## 4. 이 디렉토리가 로컬 깃 저장소라고 컴퓨터에 말해준다.
    
    git init 


## 5-1. 로컬 저장소와 깃허브 저장소를 연결한다. remote는 origin의 설명자이며 origin은 로컬 컴퓨터가 아닌 온라인 어딘가를 가리킨다는 것이다.
    git remote add origin https://github.com/username/myproject.git


## 5-2. 원격 저장소의 별명을 설정할 수 있고, 여러개의 원격 저장소를 로컬 저장소로 저장할 수 있다.

    git remote add memo https://github.come/username/memo.git


## 6. 로컬 저장소가 알고있는 원격 저장소의 모든 항목을 보여준다.
    
    git remote -v


## 7-1. 기존 원격 저장소 URL을 변경할 수 있다.

    git remote set-url origin https://github.com/username/myproject2.git


## 7-2. 기존 원격 저장소 URL을 삭제할 수 있다.

    git remote rm 원격 저장소 별명


## 8. 원격 저장소를 지역 저장소로 복제할 수 있다.

    git clone https://github.com/git/git.git


## 9. github에 올릴 파일 하나를 로컬저장소에 붙여넣는다. 파일을 수정하고 반영하고자 할 때도 이 명령어를 사용한다.

    git add new.md
 

## 9-1. 파일의 이름을 수정할 때의 명령어이다.

    git mv 원래파일이름 변경할파일이름


## 10. git add 명령어로 새로운 파일을 인식후, commit으로 버전관리를 시작하게 된다. 그러나 아직, 원격저장소에는 반영되지 않았다.

    git commit -m "변경된 내용사항쓰기"


## 11. 원격저장소에 파일을 적용시킨다. -u는 원격저장소로부터 업데이트를 받은 후 push를 한다는 의미이므로 습관적으로 사용하는 것이 좋다.

    git push -u origin master

