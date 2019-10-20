# Build image
```
docker build -t load-balanced-app .

```

# Run 2 Instance of the images

```
docker run -e "MESSAGE=First instance" -p 8081:3000 -d load-balanced-app
docker run -e "MESSAGE=Second instance" -p 8082:3000 -d load-balanced-app
```
