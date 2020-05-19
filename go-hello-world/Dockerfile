FROM golang:alpine as builder

RUN apk update

COPY . .

RUN go build hello.go

FROM scratch

COPY --from=builder /go/hello /usr/bin/hello

CMD ["hello"]
