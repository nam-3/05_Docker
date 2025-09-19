# 베이스 이미지
FROM ubuntu

# 이미지 레이어 세개 만들어짐 ↓

# nginx 설치
RUN apt-get update && \
apt-get install -y -q nginx

# # 파일 복사
COPY index.html /usr/share/nginx/html

# nginx 시작
# 레이어와 상관없음
CMD ["nginx", "-g", "daemon off;"]

