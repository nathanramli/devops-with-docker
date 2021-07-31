Create the image.

```
~ $ docker build . -t dowd-1.12
Sending build context to Docker daemon  729.1kB
Step 1/8 : FROM node:14-alpine
 ---> d93b35a67404
Step 2/8 : WORKDIR /usr/src/app
 ---> Running in 08ee0a7daec0
Removing intermediate container 08ee0a7daec0
 ---> 5669f05fad1a
Step 3/8 : EXPOSE 5000
 ---> Running in 69d75aa4946a
Removing intermediate container 69d75aa4946a
 ---> f253e6056f93
Step 4/8 : COPY . .
 ---> 7c3b5c94b5ce
Step 5/8 : RUN npm install
 ---> Running in 98cf0711eaab
.....

~ $ docker images
REPOSITORY                          TAG                 IMAGE ID            CREATED             SIZE
dowd-1.12                           latest              1364206a3303        2 minutes ago       343MB
```

Run container.

```
~ $ docker run -d -p 5000:5000 dowd-1.12
6ebe42776eaf8d79d81bfd6cf8070e528570ae09f94810377341de15a8cc441c
```

Visiting `localhost:5000`

![Output images](https://github.com/nathanramli/devops-with-docker/blob/main/part01/1.12/website.png?raw=true)
