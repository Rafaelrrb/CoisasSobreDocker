FROM golang:1.7.3 as build
WORKDIR /app
COPY main.go .
RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo - o main
#CMD ["./main"]

# terminal 
# sudo docker build -t rrborba/go-app:simples .

# imagem compacta
FROM alpine:3.14
WORKDIR /app
COPY --from=build /app/main .
CMD ["./main"]