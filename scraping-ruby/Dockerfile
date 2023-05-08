FROM ruby:3.1

MAINTAINER dvarrui 1.0

RUN apt update -y
RUN apt install -y apt-utils
RUN apt install -y firefox-esr

COPY Gemfile .
RUN bundle install

COPY temp/geckodriver /usr/local/bin
RUN chmod +x /usr/local/bin/geckodriver

CMD ["/bin/sh"]

