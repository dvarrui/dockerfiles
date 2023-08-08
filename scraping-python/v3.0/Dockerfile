FROM opensuse/tumbleweed

MAINTAINER dvarrui 2.0

RUN zypper refresh
RUN zypper in -y python311
RUN zypper in -y python311-pip
RUN zypper in -y MozillaFirefox

RUN pip install --upgrade pip
COPY requirements.txt .
RUN pip install -r ./requirements.txt

COPY temp/geckodriver /usr/local/bin
RUN chmod +x /usr/local/bin/geckodriver

CMD ["/bin/bash"]
