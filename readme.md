### Simple Flask app running behind Nginx & uWSGI in a Docker container

```sh
git clone https://github.com/Julian-Nash/docker-flask-uwsgi-nginx-simple.git
```

```sh
docker-compose up --build
```

http://127.0.0.1/

### Notes

`nginx` logs and `uwsgi` logs will be logged to `log/nginx` and `log/uwsgi` respectively.