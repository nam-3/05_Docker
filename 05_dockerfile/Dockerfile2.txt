# 베이스 이미지
FROM ubuntu:latest

# RUN 명령의 실행
RUN echo shell 형식입니다.
RUN ["echo", "Exec 형식입니다."]
RUN ["/bin/bash", "-c", "echo 'Exec 형식에서 bash를 사용하였습니다.'"]
