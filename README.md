# sensu

Installing 1.9.0 via Docker

## Docker Compose

```
docker-compose stop && docker-compose rm && docker-compose build && docker-compose up -d
docker-compose ps
docker-compose exec sensu bash
```

## RABBITMQ

```
docker run -d --name rabbitmq -p 5672:5672 rabbitmq
```

## Sensu

```
docker build -t sensu_core_1.9.0 -f Dockerfile.sensu .
docker run -d --name sensu -p 4567:4567 -p 3030:3030 -p 3031:3031 sensu_core_1.9.0
```

## Uchiwa

```
docker build -t uchiwa_1.7.0 -f Dockerfile.uchiwa .
docker run -d --name uchiwa -p 3000:3000 uchiwa_1.7.0
```
