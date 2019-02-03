![1](https://user-images.githubusercontent.com/44438752/52175983-cc506a80-27ef-11e9-89a9-72ae4c45eeea.JPG)

윈도우에서는 한 줄의 끝이 **CR(Carriage Return)**과 **LF(Line Feed)인 **CFLF**로 이루어지는 반면에, 
유닉스 시스템에서는 **LF(Line Feed)** 로 이루어 지기에 Git에서 어느 쪽을 택해야할지 혼란이 온것이다.
이를 해결하기 위해서는 이를 자동으로 변환해주는 **core.autocrlf**의 기능 켜주면 된다.

윈도우 사용자는 다음과 같은 명령어를 입력하면 된다. 시스템 전체가 아닌 해당 프로젝트에만 적용하고 싶으면 **-global**을 빼주면 된다.  
    
