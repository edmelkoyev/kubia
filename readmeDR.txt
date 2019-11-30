$ docker build -t kubia .

$ docker run --name kubia-container -p 8080:8080 -d kubia

$ docker logs -f [crtId]

$ docker inspect kubia-container

$ docker exec -it kubia-container bash

$ docker stop kubia-container
$ docker rm kubia-container

Set tag
$ docker tag kubia edmelkoyev/kubia

Push to docker Hub
$ docker push edmelkoyev/kubia

