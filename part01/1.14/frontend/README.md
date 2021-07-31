Create the image.

```
~ $ docker build . -t dowd-1.14-frontend
Sending build context to Docker daemon  729.1kB
Step 1/9 : FROM node:14-alpine
 ---> d93b35a67404
Step 2/9 : WORKDIR /usr/src/app
 ---> Running in a8f457143168
Removing intermediate container a8f457143168
 ---> 632684de0a4c
Step 3/9 : EXPOSE 5000
 ---> Running in af3711e7451a
Removing intermediate container af3711e7451a
 ---> 8befd7fb6916
Step 4/9 : COPY . .
 ---> bd44bb721257
Step 5/9 : ENV REACT_APP_BACKEND_URL=http://localhost:8080
 ---> Running in 6e64ecbd6b6d
Removing intermediate container 6e64ecbd6b6d
 ---> 0c2a9c29c185
Step 6/9 : RUN npm install
 ---> Running in 7e02fe014fd9
.....

~ $ docker images
REPOSITORY                          TAG                 IMAGE ID            CREATED              SIZE
dowd-1.14-frontend                  latest              0768068f689a        About a minute ago   343MB
dowd-1.14-backend                   latest              82cef02bb3e2        3 minutes ago        447MB
```

Run container.

```
~ $ docker run -d -p 5000:5000 dowd-1.14-frontend
2708c146560fa56426cd580352d96f29830f954569ccfd037afd2324c390bda0
```