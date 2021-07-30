```
~ $ docker run -d --name dowd-1.3 devopsdockeruh/simple-web-service:ubuntu
357fa697d4238bfec02da0535ac6f49acdbdd959abbca0dd64e0ff6ea1b51734

~ $ docker exec -it dowd-1.3 bash
root@357fa697d423:/usr/src/app# ls
server  text.log
root@357fa697d423:/usr/src/app# tail -f ./text.log
2021-07-30 16:55:48 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-07-30 16:55:50 +0000 UTC
2021-07-30 16:55:52 +0000 UTC
2021-07-30 16:55:54 +0000 UTC
2021-07-30 16:55:56 +0000 UTC
2021-07-30 16:55:58 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-07-30 16:56:00 +0000 UTC
2021-07-30 16:56:02 +0000 UTC
2021-07-30 16:56:04 +0000 UTC
2021-07-30 16:56:06 +0000 UTC
2021-07-30 16:56:08 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-07-30 16:56:10 +0000 UTC
2021-07-30 16:56:12 +0000 UTC
2021-07-30 16:56:14 +0000 UTC
2021-07-30 16:56:16 +0000 UTC
2021-07-30 16:56:18 +0000 UTC
```