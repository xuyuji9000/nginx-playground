This folder documents the learning about nginx path traversal.

# Steps

1. Start Nginx locally

    ``` shell
    podman run -d -p 8080:80 docker.io/library/nginx

    curl localhost:8080
    ```

2. `exec` into the running container 

    ``` shell
    podman exec -it CONTAINER_NAME /bin/bash
    ```

# Reference

- [nginx](https://hub.docker.com/_/nginx)

    > Docker Hub official page for nginx

