FROM continuumio/miniconda3
RUN conda install -y mamba -c conda-forge

ADD ./environment.yml .
RUN mamba env update --file ./environment.yml &&\
    conda clean -tipy
COPY ./IntroductoryCourse/lesson_code /notebooks
# Create the environment:
#COPY environment.yml .
#RUN conda env create -f environment.yml

