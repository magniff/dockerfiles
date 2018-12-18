FROM ubuntu:latest


# basic refresh and tool installation
RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install python3 python3-venv vim git curl wget sudo htop


# add user magniff and configure
RUN useradd -ms /bin/bash magniff
USER magniff


# setup vim and bash stuff
COPY .vimrc /home/magniff/.vimrc
COPY .bashrc /home/magniff/.bashrc
RUN mkdir /home/magniff/shared /home/magniff/workspace


# install vim plugin manager
RUN git clone https://github.com/VundleVim/Vundle.vim.git /home/magniff/.vim/bundle/Vundle.vim
RUN vim +PluginInstall +qall 1>/dev/null 2>/dev/null


WORKDIR /home/magniff

