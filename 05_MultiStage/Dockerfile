# 1단계: 개발 환경
FROM golang:alpine AS builder

WORKDIR /go/src/app
COPY main.go .

RUN go mod init
RUN go build -o webserver .

# 2단계: 실행 환경
FROM scratch
WORKDIR /app
COPY --from=builder /go/src/app/ /app/

CMD ["./webserver"]