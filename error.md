### 1. CRLF error
![1](https://user-images.githubusercontent.com/44438752/52175983-cc506a80-27ef-11e9-89a9-72ae4c45eeea.JPG)

윈도우에서는 한 줄의 끝이 **CR(Carriage Return)**과 **LF(Line Feed)인 **CRLF**로 이루어지는 반면에, 
유닉스 시스템에서는 **LF(Line Feed)** 로 이루어 지기에 Git에서 어느 쪽을 택해야할지 혼란이 온것이다.
이를 해결하기 위해서는 이를 자동으로 변환해주는 **core.autocrlf**의 기능 켜주면 된다.

윈도우 사용자는 다음과 같은 명령어를 입력하면 된다. 시스템 전체가 아닌 해당 프로젝트에만 적용하고 싶으면 **-global**을 빼주면 된다.  
    
    git config --global core.autocrlf true


### 2. remote 저장소에 push할 때 error

![1](https://user-images.githubusercontent.com/44438752/52176262-b349b880-27f3-11e9-95ab-101d6d7dc635.JPG)
push 하기 이전에 **git pull**을 해서 원격저장소의 최신상태를 유지한 상태에서 push를 했어야 한다.
이럴 경우,

    git pull origin master
    git commit -a
    git push origin master
