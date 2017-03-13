## Instruction

```
docker-compose build
rm src/*
docker run --rm -v $(pwd):/app composer/composer create-project --prefer-dist laravel/laravel src
docker-compose up
```