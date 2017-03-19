FROM ruby
RUN apt-get update -qq && apt-get install -y nodejs
RUN mkdir /code
RUN gem install bundler
WORKDIR /code
RUN printf "source 'https://rubygems.org'\ngem 'github-pages', group: :jekyll_plugins\n" >> Gemfile
RUN bundler install
VOLUME /code
EXPOSE 4000