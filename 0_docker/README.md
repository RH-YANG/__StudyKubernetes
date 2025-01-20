
## 개요
- 컨테이너 기본 사용법을 익히기 위한 실습코드이다.
- 웹서비스를 구성할 수 있다.
- 두가지 프레임워크(django, flask)로 예제를 확인할 수 있다.

.
## 실습 절차
1. 가상머신을 만들때 NAT 네트워크를 지정한다.
2. 실습에 사용된 80,81번 포트 포워딩을 등록한다.
   호스트 IP는 비워둠
   게스트 IP는 네트워크주소인 10.0.2.0 또는 생성된 사설IP를 입력한다.
3. vm 내부에서 도커를 설치하여 도커 호스트를 생성한다.
4. 하단의 다양한 명령어를 사용해보면서 실습을 진행한다.


&nbsp;
---
.

#### docker compose 관련 명령
- docker compose up -d --build
  이미지를 빌드하면서 백그라운드 실행한다.
- docker compose down
  생성된 컨테이너를 모두 종료한다

.

#### 파이썬 가상환경 관련 명령
- pyenv activate <id>
  가상환경을 실행한다
- source deactivate
  환경에서 빠져나온다

.

#### 디버그 관련 명령
- docker logs <id>
  해당 컨테이너에 들어가 출력된 로그를 확인한다
- docker container exec -it <id> /bin/bash
  해당 컨테이너에 들어가 터미널을 실행한다.

.

#### 컨테이너 관련 명령
- docker container run --name postgrestest \
  --network mynetwork03 \
  -e POSTGRES_PASSWORD=P@ssw0rd \
  --mount type=volume,source=myvolume03,target=/var/lib/postgresql/data \
  -d mypostgres03
- docker container run -d --name flasktest \
  --network mynet02 myflask02
- docker container run -d --name nginxtest \
  --network mynet02 \
  -p 81:81 mynginx02f   