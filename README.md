# Flask + PostgreSQL + Docker

## Spuštění

1. Spusťte build a start:

```
docker-compose up --build
```

2. Aplikace poběží na http://localhost:5000

## Práce s databází

Pro inicializaci databáze spusťte v kontejneru:

```
docker-compose run web flask shell
>>> from app import db, create_app
>>> app = create_app()
>>> with app.app_context():
...     db.create_all()
```

## Výchozí přihlašovací údaje k databázi
- user: postgres
- password: postgres
- db: postgres
- host: db

