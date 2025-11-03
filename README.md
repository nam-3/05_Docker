🐳 05_docker

Docker 학습을 위한 정리 문서입니다.
각 단계별 학습 노션 페이지는 아래 링크를 통해 이동할 수 있습니다.

📘 학습 목차

1️⃣ IT 인프라 기본 지식

2️⃣ 컨테이너와 Docker

3️⃣ 도커 설치

4️⃣ 도커 이미지 & 컨테이너 관리

5️⃣ Dockerfile

6️⃣ 이미지 레지스트리

7️⃣ docker-compose

⚙️ 자주 사용하는 Docker 명령어

💡 실습 중 자주 사용하는 명령어를 모아둔 섹션입니다.

# 컨테이너 실행
docker run -d --name myweb -p 80:80 nginx

# 네트워크 생성
docker network create mydbnet

# MariaDB 컨테이너 실행
docker run -d --name mydb -p 3306:3306 \
    -e MARIADB_ROOT_PASSWORD=password \
    -v dbvol:/var/lib/mysql:Z \
    --network=mydbnet \
    mariadb

# 실행 중인 컨테이너에 쉘 접속
docker exec -it myweb /bin/bash

📦 명령어 옵션 정리
옵션	설명
-d	백그라운드(detached) 모드로 실행
-p	포트 포워딩 (호스트:컨테이너)
-v	볼륨 마운트 (데이터 영속성 확보)
--network	사용자 정의 네트워크 연결
docker exec -it	컨테이너 내부 명령 실행 (인터랙티브 쉘)
