FROM golang:1.16-alpine

WORKDIR /app

COPY go.mod ./
RUN go mod download

COPY *.go ./

RUN go build -o /go-hello

EXPOSE 8080

CMD [ "/go-hello" ]