
## Build Laravel Docker Images

Build Laravel Images from docker file (make sure execute this command in same folder)

```
docker build -t my-laravel-image .
```

## Command to run Docker

Run Laravel you just build
```
docker run -it --rm -p 8181:8080 --name laravel my-laravel-image:latest
```
