Building images.
```
~ $ docker build . -t curler
Sending build context to Docker daemon  3.072kB
Step 1/7 : FROM ubuntu:18.04
 ---> 39a8cfeef173
Step 2/7 : RUN apt-get update
 ---> Using cache
 ---> 04879742c91d
Step 3/7 : RUN apt-get --yes install curl
 ---> Using cache
 ---> 2c619fda785f
Step 4/7 : WORKDIR /app
 ---> Using cache
 ---> 4d5d2b1b8544
Step 5/7 : COPY fetch.sh .
 ---> Using cache
 ---> 3b5597061b5f
Step 6/7 : RUN chmod +x fetch.sh
 ---> Running in 5dd5238181f5
Removing intermediate container 5dd5238181f5
 ---> 4061b0161ffd
Step 7/7 : CMD fetch.sh
 ---> Running in 857e9e001273
Removing intermediate container 857e9e001273
 ---> 165dd8b26d3f
Successfully built 165dd8b26d3f
Successfully tagged curler:latest
```

Checking images.
```
~ $ docker images
REPOSITORY                          TAG                 IMAGE ID            CREATED             SIZE
curler                              latest              165dd8b26d3f        2 minutes ago       115MB
```

Run container.
```
~ $ docker run -it curler
Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="https://www.helsinki.fi/">here</a>.</p>
</body></html>
```