FROM debian 
LABEL maintainer=@mattdube
ARG DEBIAN_FRONTEND=noninteractive
RUN /bin/bash -c 'source $HOME/.bashrc ; echo $HOME'
RUN apt-get update --fix-missing
RUN apt-get install -y apt-utils
RUN apt-get install -y wget bzip2 ca-certificates \
    libglib2.0-0 libxext6 libsm6 libxrender1
RUN echo 'export PATH=/opt/conda/bin:$PATH' > /etc/profile.d/conda.sh && \
wget --quiet \
    https://repo.anaconda.com/miniconda/Miniconda3-py39_4.10.3-Linux-x86_64.sh -O ~/miniconda3.sh && \
    /bin/bash ~/miniconda3.sh -b -p /opt/conda && \
    rm ~/miniconda3.sh
