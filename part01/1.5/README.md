```
~ $ docker pull devopsdockeruh/simple-web-service:alpine
alpine: Pulling from devopsdockeruh/simple-web-service
ba3557a56b15: Pull complete
1dace236434b: Pull complete
4f4fb700ef54: Pull complete
Digest: sha256:dd4d367476f86b7d7579d3379fe446ae5dfce25480903fb0966fc2e5257e0543
Status: Downloaded newer image for devopsdockeruh/simple-web-service:alpine
docker.io/devopsdockeruh/simple-web-service:alpine

~ $ docker run -d --name dowd-1.5 devopsdockeruh/simple-web-service:alpine
a2c8674d187de6e912f6440e3b843809db01a8223f3898be26449a8243b022ec

~ $ docker exec -it dowd-1.5 sh
/usr/src/app # ls
server    text.log
/usr/src/app # tail -f text.log
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-07-30 17:48:30 +0000 UTC
2021-07-30 17:48:32 +0000 UTC
2021-07-30 17:48:34 +0000 UTC
2021-07-30 17:48:36 +0000 UTC
2021-07-30 17:48:38 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-07-30 17:48:40 +0000 UTC
2021-07-30 17:48:42 +0000 UTC
```

Images size comparison.
Alpine has a smaller size.

```
devopsdockeruh/simple-web-service   ubuntu              4e3362e907d5        4 months ago        83MB
devopsdockeruh/simple-web-service   alpine              fd312adc88e0        4 months ago        15.7MB
```