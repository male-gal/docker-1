FROM ruby

RUN apt-get update && apt-get install nodejs -y && \
apt-get autoclean -y && apt-get clean -y && \
gem install rails

ONBUILD COPY hello_world/ /opt/app

ONBUILD RUN bundle update && \
bundle install

WORKDIR /opt/app
