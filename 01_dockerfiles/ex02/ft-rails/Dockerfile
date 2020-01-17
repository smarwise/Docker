FROM ruby:2.5.5

RUN apt-get update
RUN apt-get install -y rails build-essential
# RUN gem install puma
ONBUILD RUN rails new /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN rm -rf Gemfile.lock
ONBUILD RUN bundle update
ONBUILD EXPOSE 3000
###stop here######ersion
# ONBUILD RUN rake db:migrate
# docker build -t ft-rails .
# docker container run -it -p 3000:3000 ruby bash
# RUN wget https://cache.ruby-lang.org/pub/ruby/2.5/ruby-2.5.5.tar.bz2
# RUN tar xvf ruby-2.5.5.tar.bz2