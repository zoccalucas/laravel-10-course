# Setup Docker Laravel 10 com PHP 8.1

## Passo a passo:

-   Clone Repositório

```sh
git clone https://github.com/zoccalucas/laravel-10-course.git laravel-10
```

```sh
cd laravel-10
```

-   Crie o Arquivo .env

```sh
cp .env.example .env
```

-   Atualize as variáveis de ambiente do arquivo .env

```dosini
APP_NAME=EspecializaTi
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=nome_que_desejar_db
DB_USERNAME=nome_usuario
DB_PASSWORD=senha_aqui

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```

-   Suba os containers do projeto

```sh
docker-compose up -d
```

-   Acesse o container app

```sh
docker-compose exec app bash
```

-   Instale as dependências do projeto

```sh
composer install
```

-   Gere a key do projeto Laravel

```sh
php artisan key:generate
```

-   Acesse o projeto
    [http://localhost:8989](http://localhost:8989)

## Referências:

[Curso de Laravel 10](https://www.youtube.com/watch?v=AN-LZuw2GIc%26list=PLVSNL1PHDWvQ1N6fqhQ5HQzFtN-xrkjNU%26ab_channel=CarlosFerreira-EspecializaTi)

[Documentação Laravel](https://laravel.com/docs/10.x)
