FROM ubuntu:latest


# basic refresh and tool installation
RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install python3 python3-venv vim git curl wget sudo


# add user magniff and configure
RUN useradd -ms /bin/bash magniff
USER magniff
WORKDIR /home/magniff


COPY .vimrc /home/magniff/.vimrc
COPY .bashrc /home/magniff/.bashrc

