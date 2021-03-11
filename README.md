# Service Yamdb

Service – databases of reviewing films, books, music and REST API for it 

## Getting Started

Clone this repository: 
```
git clone https://github.com/Bytlot/infra_sp2.git
```

### Prerequisites

Requirements before start:

[Docker](https://docs.docker.com/get-docker/)

[Docker-compose](https://docs.docker.com/compose/install/)


### Installing

Installing steps:

Build and run:
```
$ docker compose up
```
Collect static:
```
$ docker-compose exec web python manage.py collectstatic --noinput
```
Make migration:
```
$ docker-compose exec web python manage.py migrate --noinput
```
Fill database from fixtures:
``` 
$ docker-compose exec web python manage.py loaddata fixture.json
```
Create supruser:
```
$ docker-compose run web python manage.py createsuperuser
```

## Admin access

Admin panel available after project started at http://localhost/admin/


## API Documentation

API Documentation available after project started at http://localhost/redoc

## Built With

Project powered Django, PostgreSQL, Gunicorn and NGINX


## Authors

* **Viktor Ermolov** - *Initial work* - (https://github.com/Bytlot)

## License

This project is licensed under the MIT License.

## Acknowledgments

Yandex.Praktikum
