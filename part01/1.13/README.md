Create the image.

```
~ $ docker build . -t dowd-1.13
Sending build context to Docker daemon   42.5kB
Step 1/6 : FROM golang:1.16-alpine
1.16-alpine: Pulling from library/golang
5843afab3874: Already exists
3d8dd7cab735: Already exists
4cac70760d29: Already exists
1edffed539bd: Pull complete
a4005d2dc874: Pull complete
Digest: sha256:44b551e001a9662629a094952546702d4fe9625a4ba55113dd928c2858bead6d
Status: Downloaded newer image for golang:1.16-alpine
 ---> 7762f5dece68
Step 2/6 : WORKDIR /usr/src/app
 ---> Running in 675ed1ba2057
Removing intermediate container 675ed1ba2057
 ---> 2e590eb748ae
Step 3/6 : EXPOSE 8080
 ---> Running in f59f741ba8ac
Removing intermediate container f59f741ba8ac
 ---> 579da086407c
Step 4/6 : COPY . .
 ---> 25220a9cbabb
Step 5/6 : RUN go build
 ---> Running in ace1ea40a992
.....

~ $ docker images
REPOSITORY                          TAG                 IMAGE ID            CREATED             SIZE
dowd-1.13                           latest              a5bb937eb29b        2 minutes ago       447MB
```

Run container.

```
~ $ docker run -d -p 8080:8080 dowd-1.13
881ae0267f7601b2b056b3d0c6d3f36608f12f54b374bb804b90cf55b6a63964
```

Visiting `localhost:8080/ping`

![Output images](https://github.com/nathanramli/devops-with-docker/blob/main/part01/1.12/website.png?raw=true)
