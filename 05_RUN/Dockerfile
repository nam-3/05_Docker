# 베이스 이미지
FROM ubuntu:24.04

# nginx 설치
# update 작업을 제일 먼저 해줘야 함
# 목록 업데이트 (apt repository, 패키지 디렉토리) 가져와야함
# 여기엔 없어서 한 번 가져와야 함
# == yum update
RUN apt -y update && apt -y upgrade
# -q, --quiet : 조용하게 설치
RUN apt -q -y install nginx

# apt clean && apt autoremove

# 서비스 되는 포트 지정
# nginx를 80 포트로 서비스함 * 포트가 실제 열리는 건 아님, 
# 확인하려면 history 혹은 이미지 제작한 사이트 접속
EXPOSE 80

# 서버 실행(foreground 실행)
CMD ["nginx", "-g", "daemon off;"]
