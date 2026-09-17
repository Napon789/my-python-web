# my-python-web

Flask app served with Gunicorn inside Docker.

## Project structure

```
my-python-web/
├── app.py
├── templates/
│   └── index.html
├── static/
│   └── style.css
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
├── .dockerignore
└── .gitignore
```

## Run with Docker Compose (recommended)

```bash
docker compose up --build
```

Open http://localhost:5000

## Run with plain Docker

```bash
docker build -t my-python-web .
docker run -p 5000:5000 my-python-web
```

## Run locally without Docker

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python app.py
```
