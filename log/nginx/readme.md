Directory for nginx logs

A better choice in production may be to change the `volumes` section in the `docker-compose.yml` under the `nginx` service to the following:

```yml
volumes:
  - ./var/log/nginx:/var/log/nginx
```

Just make sure this directory exists before running `docker-compose up --build`