FROM golang:latest as builder

WORKDIR /app
COPY ./ ./
RUN go mod download

RUN dpkg --add-architecture amd64 \
    && apt update \
    && apt-get install -y --no-install-recommends gcc-x86-64-linux-gnu libc6-dev-amd64-cross

RUN CGO_ENABLED=1 CC=x86_64-linux-gnu-gcc GOARCH=amd64 GOOS=linux go build -o main

FROM --platform=linux/amd64 ubuntu
COPY --from=builder /app/main .
ENTRYPOINT ["/main"]
EXPOSE 8000