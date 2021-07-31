Create a text.log file

```
~ $ touch text.log
```

Run docker container

```
~ $ docker run -d -v "$(pwd)/text.log:/usr/src/app/text.log" devopsdockeruh/simple-web-service:ubuntu
07fc4dbd6f33403e1fdfc1427a61e521350c41ffe38112c01d1a0082d2262dd7
```

Check `text.log`

```
~ $ cat text.log
2021-07-31 17:33:53 +0000 UTC
2021-07-31 17:33:55 +0000 UTC
2021-07-31 17:33:57 +0000 UTC
2021-07-31 17:33:59 +0000 UTC
2021-07-31 17:34:02 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-07-31 17:34:04 +0000 UTC
2021-07-31 17:34:06 +0000 UTC
2021-07-31 17:34:08 +0000 UTC
2021-07-31 17:34:10 +0000 UTC
2021-07-31 17:34:12 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-07-31 17:34:14 +0000 UTC
2021-07-31 17:34:16 +0000 UTC
2021-07-31 17:34:18 +0000 UTC
2021-07-31 17:34:20 +0000 UTC
2021-07-31 17:34:22 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-07-31 17:34:24 +0000 UTC
2021-07-31 17:34:26 +0000 UTC
2021-07-31 17:34:28 +0000 UTC
2021-07-31 17:34:30 +0000 UTC
2021-07-31 17:34:32 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-07-31 17:34:34 +0000 UTC
2021-07-31 17:34:36 +0000 UTC
2021-07-31 17:34:38 +0000 UTC
```