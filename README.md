# Docker com PHP + MYSQL 

O objetivo desse projeto é criar um ambiente simples e fácil para o desenvolvimento, também como aprendizado.
Nele temos o 

> **PHP + MYSQL + NGINX**


# Comandos

Crie a pasta **www** na raiz do projeto, é por lá que o contêiner vai mapear os arquivos da sua maquina.

## Rodar em segundo plano

    docker compose up -d

## Entrar no container meu-php

    docker exec -it meu-php /bin/bash

## Criar o projeto laravel

    composer create-project --prefer-dist laravel/laravel meu-projeto .

## Composer
    composer install

## Migração

    php artisan migrate
## Conexão com o banco (.env)
Altere as configurações do mysql no **docker-compose.yml**

    DB_CONNECTION=mysql
    DB_HOST=mysql
    DB_PORT=3306
    DB_DATABASE=meu_banco
    DB_USERNAME=user
    DB_PASSWORD=senha

### permissão para a pasta storage caso dê erro

    chmod 775 -R storage

### permissão para a pasta vendor caso dê erro

    chmod 775 -R vendor