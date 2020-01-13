FROM ruby:2.3

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y rails
RUN apt-get install -y git
RUN pwd
ONBUILD  RUN mkdir -p /opt/app
ONBUILD WORKDIR /home
ONBUILD RUN cd /home && git clone https://github.com/smarwise/docker-rails-app.git app
ONBUILD ADD app /opt/app
ONBUILD WORKDIR /opt/app
# ONBUILD RUN gem install bundler
# ONBUILD RUN bundle inst0all
# ONBUILD RUN rake db:migrate
# docker build -t ft-rails .
# docker container run -it -p 3000:3000 ruby bash