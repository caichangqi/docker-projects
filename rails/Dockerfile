FROM ruby:2.3.3
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
RUN mkdir /code
WORKDIR /code
RUN gem install rails
EXPOSE 3000

RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.2.0/dumb-init_1.2.0_amd64
RUN chmod +x /usr/local/bin/dumb-init

CMD ["dumb-init", "/bin/bash", "-c", "bundle install & rails server -b '0.0.0.0'"]