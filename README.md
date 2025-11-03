# 🐳 05_docker

Docker 학습 정리 노트입니다.  
아래 링크를 통해 각 주제별 노션 페이지로 이동할 수 있습니다.

---

## 📘 학습 목차

1️⃣ [IT 인프라 기본 지식](https://www.notion.so/1-IT-26a1400eefa5801a9312d7a2d53cf788?pvs=21)  
2️⃣ [컨테이너와 Docker](https://www.notion.so/2-Docker-26a1400eefa5806996e3e7be168274f9?pvs=21)  
3️⃣ [도커 설치](https://www.notion.so/3-26a1400eefa580c6814cce2905e0871b?pvs=21)  
4️⃣ [도커 이미지 & 컨테이너 관리](https://www.notion.so/4-26b1400eefa58003952bc3f0ff4144c5?pvs=21)  
5️⃣ [Dockerfile](https://www.notion.so/5-Dockerfile-26f1400eefa580c6aef8c0a0e1a3c9b9?pvs=21)  
6️⃣ [이미지 레지스트리](https://www.notion.so/6-2721400eefa5807eb0e3c1677b59609a?pvs=21)  
7️⃣ [docker-compose](https://www.notion.so/7-docker-compose-2721400eefa580fca21bc3c86a3a3658?pvs=21)

---

## ⚙️ 외워야 하는 Docker 명령어

도커 실습 중 자주 사용되는 명령어를 모아두었습니다.

```bash
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

# 컨테이너에 쉘 프로세스 실행
docker exec -it myweb /bin/bash
