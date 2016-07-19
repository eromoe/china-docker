FROM ubuntu:14.04

ADD . /code
WORKDIR /code

# set system source

# RUN wget http://mirrors.163.com/.help/sources.list.trusty
# RUN curl -K http://mirrors.163.com/.help/sources.list.trusty -o output.txt
# RUN mv /etc/apt/sources.list /etc/apt/sources.list.backup
RUN mv ./conf/sources.list.trusty.aliyun /etc/apt/sources.list

# set pip srouce
RUN cp ./conf/pip.conf /etc/pip.conf

# set node srouce
RUN echo "registry = https://registry.npm.taobao.org" >> /etc/npmrc

# apt-get update updates the list of available packages and their versions, but it does not install or upgrade any packages. apt-get upgrade actually installs newer versions of the packages you have

RUN apt-get --yes update
# RUN apt-get --yes install build-essential libssl-dev
RUN apt-get --yes install git supervisor python-virtualenv uwsgi uwsgi-core uwsgi-plugin-python sqlite3
RUN apt-get --yes install nodejs npm