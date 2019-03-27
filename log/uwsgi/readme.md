Directory for uWSGI logs

A better choice in production may be to change the `volumes` section in the `docker-compose.yml` under the `flask` service to the following:

```yml
volumes:
  - ./var/log/uwsgi:/var/log/uwsgi
```

Just make sure this directory exists before running `docker-compose up --build`