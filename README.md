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
