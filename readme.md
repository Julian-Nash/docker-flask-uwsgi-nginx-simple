### Simple Flask app running behind Nginx & uWSGI in a Docker container

Clone the repo:

```sh
git clone https://github.com/Julian-Nash/docker-flask-uwsgi-nginx-simple.git
```

To develop locally, create a new virtual env in the `flask` directory & run the app:

```sh
cd app
python -m venv env
source env/bin/activate
pip install -r requirements.txt
export FLASK_APP=run.py
export FLASK_ENV=development
flask run
```

Go to - http://127.0.0.1:5000


To run the container locally:

```sh
docker-compose up --build
```

Go to - http://127.0.0.1/

### Notes

`nginx` logs and `uwsgi` logs will be logged to `log/nginx` and `log/uwsgi` respectively. This can be changed by changing the `volume` mounts in the `docker-compose.yml`.

Alternatively, delete the `volumes` to have Docker log to `Stdout`.