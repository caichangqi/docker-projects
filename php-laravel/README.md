## Instruction

### Build

```bash
docker-compose build
rm src/*
docker run --rm -v $(pwd):/app composer/composer create-project --prefer-dist laravel/laravel src
docker-compose up
```

### Create project

```bash
rm -rf src/*
docker run --rm -v $(pwd):/app composer/composer create-project --prefer-dist laravel/laravel src
```

Don't forget chagne env after create project

### Run migrate

```bash
docker-compose run php php artisan migrate
```

### PHPUnit

```bash
docker-compose run php ./vendor/bin/phpunit
```