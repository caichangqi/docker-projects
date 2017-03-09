## Create rails iamge
docker build -t rails .

## Run rails
docker run -it --rm -p 3000:3000 -v /tmp/blog:/code rails /bin/bash

## First time
rails new app
cd app
rails server
