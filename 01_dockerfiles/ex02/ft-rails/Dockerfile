FROM ruby:2.5

LABEL maintainer="smarwise<smarwise@student.wethinkcode.co.za>"

RUN apt-get update -qq && apt-get install -y nodejs postgresql-client
RUN gem install rails --version 4.2.4

ENV RAILS_VERSION 5.2.3
ENV RAILS_ENV=development

RUN mkdir -p /opt/app
WORKDIR /opt/app

ONBUILD ADD app /opt/app

ONBUILD RUN bundle install
ONBUILD RUN rails db:create
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed
#docker build -t ft-rails:on-build .