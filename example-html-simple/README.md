
## Build Web Server Docker Image

```
docker build -t my-webserver .
```

## Command to run Docker

```
docker run -it --rm -p 8080:80 --name web my-webserver
```
