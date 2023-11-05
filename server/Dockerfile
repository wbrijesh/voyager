FROM golang:1.21@sha256:cffaba795c36f07e372c7191b35ceaae114d74c31c3763d442982e3a4df3b39e

WORKDIR /usr/src/voyager-server

RUN go install github.com/cosmtrek/air@latest

COPY go.mod ./
RUN go mod download && go mod verify
COPY . .

EXPOSE 3000
