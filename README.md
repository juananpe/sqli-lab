# Dockerized SQLi Lab (ii)

Based on:
- SQLi Labs https://github.com/Audi-1/sqli-labs
- Alpine-based LAP Server with PHP extensions https://github.com/EvilFreelancer/alpine-apache-php5 


## Where do I put my files?

- MySQL Dump -> dump/
- vulnerable php app -> html/public

Note: the database volume will be stored in ./database

### How to start the lab?

login, pass and db name are hardcoded in `docker-compose.yml` and `html/public/includes/config.inc`. To start the lab, just run:

```
$ docker-compose up -d
```

Wait a minute before trying to connect to  http://localhost:8888 (otherwise, you will get "Connection refused" errors from MariaDB/MySQL)


### How to stop the lab?
If you want to stop your containers without removing them from docker:
```
$ docker compose down
```
If you want to stop your containers and remove them from docker:
```
docker-compose rm -fsv
```


