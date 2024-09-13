docker build -t tcp_server .

docker run -d --name tcp_server -p 3333:3333 tcp_server

docker logs tcp_server

docker kill tcp_server

docker rm tcp_server

