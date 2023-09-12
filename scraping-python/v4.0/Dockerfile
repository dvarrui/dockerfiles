FROM opensuse/tumbleweed

MAINTAINER dvarrui 4.0

RUN zypper refresh
RUN zypper in -y python311
RUN zypper in -y python311-pip
RUN zypper in -y MozillaFirefox

# RUN pip install --upgrade pip
COPY requirements.txt .
RUN pip install -r ./requirements.txt --break-system-packages

COPY temp/geckodriver /usr/local/bin
RUN chmod +x /usr/local/bin/geckodriver

CMD ["/bin/bash"]
