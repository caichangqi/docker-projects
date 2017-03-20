## Create rails iamge
docker build -t rails .

## Create rails app
docker run --rm -p 3000:3000 -v /tmp:/code rails new blog
cd blog
docker run --rm -p 3000:3000 -v /tmp/blog:/code

## Run rails
docker run --rm -p 3000:3000 -v /tmp/blog:/code


