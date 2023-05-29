FROM golang:1.20 AS builder

WORKDIR /usr/src/app 

COPY . .

RUN go build fullcycle.go

FROM scratch

WORKDIR /usr/src/app

COPY --from=builder /usr/src/app/ .

CMD ["./fullcycle"]