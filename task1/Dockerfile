FROM golang:1.23 AS builder
WORKDIR /src
COPY tcp_server.go .
RUN CGO_ENABLED=0 go build -o /bin/tcp_server ./tcp_server.go

FROM scratch
COPY --from=builder /bin/tcp_server /bin/tcp_server
CMD ["/bin/tcp_server"]