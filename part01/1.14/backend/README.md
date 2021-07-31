Create the image.

```
~ $ docker build . -t dowd-1.14-backend
Sending build context to Docker daemon   42.5kB
Step 1/7 : FROM golang:1.16-alpine
 ---> 7762f5dece68
Step 2/7 : WORKDIR /usr/src/app
 ---> Running in 3624e274a0ba
Removing intermediate container 3624e274a0ba
 ---> f6bf6b29c545
Step 3/7 : EXPOSE 8080
 ---> Running in b95716de9b3d
Removing intermediate container b95716de9b3d
 ---> c3fb3cdc0fa6
Step 4/7 : COPY . .
 ---> b1648ed4b221
Step 5/7 : ENV REQUEST_ORIGIN=http://localhost:5000
 ---> Running in 1f950286c96e
Removing intermediate container 1f950286c96e
 ---> 784b0adb8dd2
Step 6/7 : RUN go build
 ---> Running in 3e6ca748ec2b
.....

~ $ docker images
REPOSITORY                          TAG                 IMAGE ID            CREATED              SIZE
dowd-1.14-backend                   latest              82cef02bb3e2        About a minute ago   447MB
```

Run container.

```
~ $ docker run -d -p 8080:8080 dowd-1.14-backend
f4cbdc143b3fd6995d3ce75ab57027ba192b4fe45fea7b93fe13a83c7c50f1b7
```