# Docker

docker pull
docker images
docker run -it alpine /bin/sh 可以互動
docker run -d -it alpine /bin/sh 可以detache
docker stop
docker ps
docker attach
escape sequence Ctrl+P followed by Ctrl+Q
docker build -t myimage .
docker run -d -p 80:80 myimage