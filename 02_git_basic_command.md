# 2) Git basic command  (git 명령어 정리) 
<br /><br />   
## 1. 먼저 github에 가입후, 다음을 쓴다.

    git config --global user.name "Write your name"
    git config --global user.eamil "Write your email"

이는 반드시 Github.com을 가입할 때 사용한 이메일이어야한다.

<br /><br />
## 2. 로컬 저장폴더 생성

    mkdir ~/MyProject 
이제 로컬 장소를 만들자. ~/를 입력하면 로컬 컴퓨터의 최상위 단계 디렉토리가 보일 것이다.

<p><p>
## 3. 디렉토리 바꾸기
    cd ~/MyProject

다음의 디렉토리로 옮겨간다.

<p><p>
## 4. 이 디렉토리가 로컬 깃 저장소라고 컴퓨터에 말해줌.
    
    git init 

<p><p>
## 5-1. 로컬 저장소와 깃허브 저장소를 연결.
    git remote add origin https://github.com/username/myproject.git
 remote는 origin의 설명자이며 origin은 로컬 컴퓨터가 아닌 온라인 어딘가를 가리킨다는 것이다.

<p><p>
## 5-2. 다른 원격저장소 생성

    git remote add memo https://github.come/username/memo.git
원격 저장소의 별명을 설정할 수 있고, 여러개의 원격 저장소를 로컬 저장소로 저장할 수 있다.

<p><p>
## 6. 로컬 저장소가 알고있는 원격 저장소의 모든 항목을 보여줌.
    
    git remote -v

<p><p>
## 7-1. 기존 원격 저장소 URL 변경

    git remote set-url origin https://github.com/username/myproject2.git

<p><p>
## 7-2. 기존 원격 저장소 URL 삭제

    git remote rm 원격 저장소 별명

<p><p>
## 8. 원격 저장소를 지역 저장소로 복제.

    git clone https://github.com/git/git.git

<p><p>
## 9-1. github에 올릴 파일 하나를 로컬저장소에 copy. 

    git add new.md
 파일을 수정하고 반영하고자 할 때도 이 명령어를 사용한다.
 
<p><p>
## 9-2. 파일의 이름을 수정.

    git mv 원래파일이름 변경할파일이름

<p><p>
## 10. commit 버전관리
    
    git commit -m "변경된 내용사항쓰기"
git add 명령어로 새로운 파일을 인식후, commit으로 버전관리를 시작하게 된다. 그러나 아직, 원격저장소에는 반영되지 않았다.

<p><p>
## 11. 원격저장소에 파일을 적용.

    git push -u origin master
 -u는 원격저장소로부터 업데이트를 받은 후 push를 한다는 의미이므로 습관적으로 사용하는 것이 좋다.
