FROM debian 
LABEL maintainer=@mattdube
ARG DEBIAN_FRONTEND=noninteractive
RUN /bin/bash -c 'source $HOME/.bashrc ; echo $HOME'
RUN apt-get update --fix-missing
RUN apt-get install -y apt-utils
RUN apt-get install -y wget bzip2 ca-certificates \
    libglib2.0-0 libxext6 libsm6 libxrender1
