# Docker-Images
Clone this repository to your local machine.

The environment.yml file isn't used, but is included as a reference. 

You need to have docker installed.
You can build the image using this command from the new `Docker-Images` directory:

`docker build -t intuitive-bayes-3 intuitive-bayes-3`

The build takes a few minutes to complete. 

conda and mamba are installed, and mambe is used to install the required python libraries.

The base image is from:
https://github.com/jupyter/docker-stacks

The new image contains a default docker user, jovyan. 

You can attach your local course files to your docker image, so when you run jupyter lab they are available.

In this example, I have cloned the course repository into the projects folder of my home directory. I then attach that directory to the docker container. 

`docker run -v /home/mattdube/projects/IntroductoryCourse:/home/jovyan/projects/IntroductoryCourse -it --rm -p 8888:8888 intuitive-bayes-3 start.sh jupyter lab`

