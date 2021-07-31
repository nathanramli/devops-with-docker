Create the image.

```
~ $ docker build . -t dowd-1.11
Sending build context to Docker daemon  44.54kB
Step 1/6 : FROM openjdk:8-alpine
8-alpine: Pulling from library/openjdk
e7c96db7181b: Pull complete
f910a506b6cb: Pull complete
c2274a1a0e27: Pull complete
Digest: sha256:94792824df2df33402f201713f932b58cb9de94a0cd524164a0f2283343547b3
Status: Downloaded newer image for openjdk:8-alpine
 ---> a3562aa0b991
Step 2/6 : WORKDIR /usr/src/app
 ---> Running in 467f7507a9cd
Removing intermediate container 467f7507a9cd
 ---> 28a2f089567a
Step 3/6 : EXPOSE 8080
 ---> Running in adadaa98ea86
Removing intermediate container adadaa98ea86
 ---> 88d8ee449374
Step 4/6 : COPY . .
 ---> 08defbbc6181
Step 5/6 : RUN ./mvnw package
 ---> Running in 964d5c794484
.....

~ $ docker images
REPOSITORY                          TAG                 IMAGE ID            CREATED             SIZE
dowd-1.11                           latest              0b79bb118a69        3 minutes ago       190MB
```

Run container.

```
~ $ docker run -d -p 8080:8080 dowd-1.11
8525691d8b985c527f8e76c29f065d5881365cd25e475dce91265986e7124465
```

Visiting `localhost:8080`

![Output images](https://github.com/nathanramli/devops-with-docker/blob/main/part01/1.11/website.png?raw=true)
