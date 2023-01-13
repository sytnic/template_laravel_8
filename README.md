# Project

- Laravel 8.83.27 
- PHP 7.4.32
- Apache 
- MySQL 5.7.39
- Docker

## Запуск Docker & Laravel

! Подготовить env

Запуск контейнеров

    docker-compose build
    docker-compose up -d

Вход в контейнер

    cd /d E:\
    cd develop_train\dockerphp\medlite
    dir
    docker ps
    docker exec -it container_id bash 
    (не работает в GitBash, работает в cmd)

    # apt-get install nano

    chown -R www-data:www-data *

В терминале в папке с проектом

    ls -la
    composer install

Установка ключа для запуска Laravel

    php artisan key:generate

> Запуск Laravel в браузере

    127.0.0.1:8080

## Выяснение ошибок (если необходимо)

Для выяснения ошибок
  
    docker-compose logs

Остановка и Удаление контейнеров

    docker-compose down 

Вход в контейнер и миграция

    docker ps
    docker exec -it container_id bash

## Запуск миграций

! Остановить и запустить контейнеры, затем:

    php artisan migrate

> Проверка в браузере

    127.0.0.1:8080/adminer.php

## Остановка контейнеров

    docker-compose stop
