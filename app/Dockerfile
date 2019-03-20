FROM ruby:2.4
RUN apt-get update && apt-get install libv8-dev nodejs -y
RUN gem install rails
RUN gem install bundler

COPY . /app
WORKDIR /app
RUN bundle install
