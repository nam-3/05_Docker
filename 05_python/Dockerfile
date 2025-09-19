FROM python:3.8-slim-buster
# 파이썬3 사용 시 가장 많이 사용하는 베이스 이미지
# hub.docker.com 들어가면 나와있음

# /app 폴더가 컨테이너에 없으면 생성해줌
WORKDIR /app

COPY requirements.txt requirements.txt

RUN pip3 install -r requirements.txt

# 나머지 파일을 복사해라
COPY . .

# --host=0.0.0.0 옵션 없을 시 : 로컬에서만 요청 가능
# 옵션 지정 시 컨테이너에서도 요청 가능
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0"]


