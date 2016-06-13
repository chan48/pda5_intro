### 파이썬 데이터 분석 5기 도커 가상환경 사용하기

첫 수업에서 소개드렸던 docker toolbox에서의 python3 jupyter notebook image를 재실행하는 방법입니다.

먼저 첫 수업시간에, docker toolbox 설치후 rothnic/anaconda-notebook 이미지를 run 한 이후의 실행순서입니다.<br>
> 아래는 수업시간에 하였던 과정입니다. <br><br>
>**도커 jupyter notebook 이미지 가져오기**<br>
>docker pull rothnic/anaconda-notebook<br>
>**도커 이미지 실행**<br>
>docker run -it -p 8888:8888 --name="python35(혹은 원하는 이름)" rothnic/anaconda-notebook <br>


-조교인 저의 실행환경은 윈도우즈7 입니다. 환경이 다를 수 있으니 실행이 안되시면 문의 메일 부탁드립니다.-

1.Docker Quickstart Terminal을 실행합니다.<br>
<img width="239" height="256" src="/images/docker_1.png"></img><br><br>
2.정상적으로 실행되었다면 다음과 같은 화면에서 IP가 제대로 출력이 됩니다.<br>
<img width="600" src="/images/docker_2.png"></img><br><br>
3."docker-machine ssh"를 입력하여 가상머신을 실행합니다.<br>
<img width="600" src="/images/docker_3.png"></img><br><br>
4.'rothnic/anaconda-notebook' 이미지를 정상적으로 가져오셨다면 "docker ps -a" 명령어 실행시 docker 위에 올린 container들을 확인하실 수 있습니다.<br>
여기서 container의 이름은 제가 임의대로 python으로 설정하였습니다<br>
<img width="600" src="/images/docker_4.png"></img><br><br>
5.이미지의 첫 실행에서는 "docker run -it -p 8888:8888 rothnic/anaconda-notebook"이라는 긴 명령어를 사용하였지만 일단 한번 실행 하신이후에는 다시 저와 같은 긴~ 명령어를 실행할 필요는 없습니다.<br>
<img width="600" src="/images/docker_5.png"></img><br><br>
6."docker restart python"-제가 명명한 rothnic/anaconda-notebook의 이름은 python 입니다- 를 통해서 올려놓은 컨테이너를 다시 실행시킵니다.<br>
<img width="600" src="/images/docker_6.png"></img><br><br>
7.STATUS 에 UP [시간]이 나온다면 해당 컨테이너가 docker-machine위에서 실행되는 것입니다.<br>
다른 이미지(컨테이너)가 실행중이지 않는다면 'http://192.168.99.100:8888'로 접속합니다.
<img width="600" src="/images/docker_6-1.png"></img><br><br>
8.해당 container에 정상적으로 접속한다면 아래와 같은 화면이 나옵니다.<br>
notebook을 통해 파이썬 코드를 실행하고 싶으시면 우측 'new'에서 python3를 클릭하시면 python3 버전의 notebook이 실행됩니다.
<img width="600" src="/images/docker_7.png"></img><br><br>
9.새로운 jupyter notebook에서 해당 코드를 입력하면서 실습합니다.
<img src="/images/docker_8.png"></img><br><br>
10.상단 notebook 이름을 클릭하면 notebook의 이름변경 가능합니다.
<img src="/images/docker_9.png"></img><br><br>

