![Empty open cardboard box.](image.png)

# placeholder-container
Placeholder container image e.g. for spinning up ECS services.
Returns 200 on all paths. Port is configurable via `NGINX_PORT`.

## Build
``` sh
image_name="placeholder:1"
docker build -t $image_name --platform linux/amd64 .
```

## Test
``` sh
port=2137
docker run -it --platform linux/amd64 -e NGINX_PORT=$port -p $port:$port $image_name
```

Then, try to access: http://localhost:2137
