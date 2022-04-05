FROM python:3
USER root

RUN apt-get update
#RUN apt-get -y install locales && localedef -f UTF-8 -i ja_JP ja_JP.UTF-8
#ENV LANG ja_JP.UTF-8
#ENV LANGUAGE ja_JP:ja
#ENV LC_ALL ja_JP.UTF-8
#ENV TZ JST-9
#ENV TERM xterm

RUN apt update
RUN apt-get install -y vim less
RUN apt install
RUN pip install --upgrade pip
RUN pip install --upgrade setuptools
RUN pip install --upgrade selenium
RUN pip install chromedriver-binary==100.*
RUN pip install python-dotenv
RUN wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
RUN apt install --fix-broken ./google-chrome-stable_current_amd64.deb -y
RUN which google-chrome
# Ubuntuのビープ音停止
RUN sed -i 's/# set bell-style none/set bell-style none/g' /etc/inputrc

WORKDIR /src
#ENTRYPOINT [] 