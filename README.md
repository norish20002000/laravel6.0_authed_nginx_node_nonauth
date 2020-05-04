# docker-laravel

## clone後手順
```bash
$ docker-compose up -d --build
$ docker-compose exec app composer install
$ docker-compose exec app cp .env.example .env
$ docker-compose exec app php artisan key:generate
$ docker-compose exec app php artisan migrate
$ docker-compose run node npm install
$ docker-compose run node npm run dev
```
