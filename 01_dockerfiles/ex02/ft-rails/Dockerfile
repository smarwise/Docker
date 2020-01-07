FROM ruby

RUN gem install sqlite3
RUN apt-get update
RUN apt-get -y install nodejs
RUN gem install rails
RUN rails new blog