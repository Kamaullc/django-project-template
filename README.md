# Django Project Template

A minimal Django project to use as a starting point for new projects.

## Usage

    python -m venv .venv && source .venv/bin/activate
    pip install -r requirements.txt
    python manage.py migrate
    python manage.py runserver

- `config/` – project settings and URLs
- `core/` – starter app with a `/health/` endpoint and a test

Run tests: `python manage.py test`

## Deploying to Heroku

The project includes a `Procfile` (gunicorn, with migrations on release), WhiteNoise for static files, and `DATABASE_URL` support.

    heroku create
    heroku addons:create heroku-postgresql
    heroku config:set SECRET_KEY="$(python -c 'import secrets;print(secrets.token_urlsafe(50))')" DEBUG=False ALLOWED_HOSTS=<your-app>.herokuapp.com
    git push heroku main

Settings read `SECRET_KEY`, `DEBUG` (default `True`), `ALLOWED_HOSTS` (comma-separated) and `DATABASE_URL` from the environment.
