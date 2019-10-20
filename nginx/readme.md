# Run

```
docker build -t load-balance-nginx .
docker run -p 3006:80 -d load-balance-nginx
```