FROM ruby:2.5.5

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y rails
RUN apt-get install -y git
RUN gem pristine --all
ONBUILD  RUN mkdir -p /opt/app
# ONBUILD WORKDIR /home
# ONBUILD RUN cd /home && git clone https://github.com/smarwise/docker-rails-app.git app
ONBUILD RUN git clone https://github.com/smarwise/docker-rails-app.git /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN for i in `gem list --no-versions`; do gem uninstall -aIx $i; done
ONBUILD RUN gem install rake
ONBUILD RUN gem pristine --all
ONBUILD RUN bundle update
ONBUILD RUN chmod go-w  /usr/local/bundle
# ONBUILD RUN rake db:migrate
# docker build -t ft-rails .
# docker container run -it -p 3000:3000 ruby bash