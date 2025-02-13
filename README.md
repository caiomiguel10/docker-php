# docker-php


# comandos
# rodar em segundo plano
docker compose up -d


# criar a pasta www no Host, o container mapeia os arquivos dela

# entrar no container meu-php
docker exec -it meu-php /bin/bash

# rodar o comando para criar um projeto laravel
composer create-project --prefer-dist laravel/laravel meu-projeto

# composer
composer install

# altere o .env de acordo com as configurações do banco mysql dentro do docker-compose.yml
# essas são padrão
      HOST: mysql
      MYSQL_ROOT_PASSWORD: root 
      MYSQL_DATABASE: meu_banco  
      MYSQL_USER: user  
      MYSQL_PASSWORD: senha




