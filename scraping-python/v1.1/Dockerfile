FROM python:3.10-buster

MAINTAINER dvarrui 1.0

RUN apt update -y
RUN apt install -y apt-utils
RUN apt install -y firefox-esr

RUN pip install --upgrade pip
COPY requirements.txt .
RUN pip install -r ./requirements.txt

COPY temp/geckodriver /usr/local/bin
RUN chmod +x /usr/local/bin/geckodriver

CMD ["/bin/sh"]
