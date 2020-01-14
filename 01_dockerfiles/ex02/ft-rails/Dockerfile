FROM ruby

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y rails
RUN apt-get install -y git
RUN gem pristine --all
RUN ruby -v
RUN rails -v
RUN bundler -v
ONBUILD  RUN mkdir -p /opt/app
ONBUILD RUN git clone https://github.com/smarwise/docker-rails-app.git /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN gem pristine --all
# docker build -t ft-rails .
# docker container run -it -p 3000:3000 ruby bash