FROM ruby:latest
RUN apt-get update &&\
    gem install rails sqlite 3  &&\
    apt-get install node.js -y
ONBUILD ADD	app /opt/app
ONBUILD RUN bundle install && rake db:migrate
