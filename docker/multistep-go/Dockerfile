FROM golang:alpine AS build-env
ADD . /src
WORKDIR /src
RUN go build -o go-hello .

# final stage
FROM alpine
WORKDIR /app
COPY --from=build-env /src/go-hello /app/
ENTRYPOINT ./go-hello