FROM python:2.7

ADD . /code
WORKDIR /code

# set system source

RUN mv ./conf/sources.list.trusty.aliyun /etc/apt/sources.list

# set pip srouce
RUN cp ./conf/pip.conf /etc/pip.conf

# set node srouce
RUN echo "registry = https://registry.npm.taobao.org" >> /etc/npmrc

RUN apt-get --yes update
RUN apt-get --yes install git supervisor python-virtualenv uwsgi uwsgi-core uwsgi-plugin-python sqlite3
RUN apt-get --yes install nodejs npm