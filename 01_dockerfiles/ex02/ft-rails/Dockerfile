FROM ruby:2.3.0

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y nodejs
RUN apt-get install -y rails
RUN gem pristine --all
ONBUILD  RUN mkdir -p /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD ADD app /opt/app
ONBUILD RUN gem install rdoc-data
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed
# docker build -t ft-rails .