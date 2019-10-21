# Build image
```
docker build -t load-balanced-app .

```
## Where
- build Build the image
- -t Tag the images (to identify it)
- . find Dockerfile in current directory.

# Run 2 Instance of the images

```

docker run --name first-app -e "MESSAGE=First instance" -p 8081:3000 -d load-balanced-app
docker run --name second-app -e "MESSAGE=Second instance" -p 8082:3000 -d load-balanced-app
docker run --name backup -e "MESSAGE=We will be back soon!" -p 8083:3000 -d load-balanced-app
```
## Where
- run create a container name load-balanced-app from the image.
- -e Enviroment key=value
- -p Expose to the host compuater host-port:docker-port
- -d Run on background


