Go to build directory, and then run.

```
~ $ docker build . -t web-server
Sending build context to Docker daemon   2.56kB
Step 1/2 : FROM devopsdockeruh/simple-web-service:alpine
 ---> fd312adc88e0
Step 2/2 : CMD server
 ---> Running in e489f194f220
Removing intermediate container e489f194f220
 ---> 17a1cecc13ae
Successfully built 17a1cecc13ae
Successfully tagged web-server:latest
```

Check the image.
```
~ $ docker images
REPOSITORY                          TAG                 IMAGE ID            CREATED              SIZE
web-server                          latest              17a1cecc13ae        About a minute ago   15.7MB
```

Run the image.
```
~ $ docker run web-server
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:   export GIN_MODE=release
 - using code:  gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /*path                    --> server.Start.func1 (3 handlers)
[GIN-debug] Listening and serving HTTP on :8080
```