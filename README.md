# Small Docker Image

## Requirements

In order to use this repository you need the following:

- Docker https://www.docker.com/docker-mac

## Using Small Docker Image - node-vanilla

Clone or copy the repo and do the following:

    $ cd /path/to/repo
    $ docker build -t node-vanilla .
    $ docker run -p 3000:3000 -ti --rm --init node-vanilla
    $ Visit http://localhost:3000
    $ docker history node-vanilla

    $ There is a COPY and a RUN statements in the Dockerfile. 
      So you should expect to see at least two layers more than the base image

## Using Small Docker Image - node-multi-stage

Clone or copy the repo and do the following:

    $ cd /path/to/repo
    $ docker build -t node-multi-stage .
    $ docker run -p 3000:3000 -ti --rm --init node-multi-stage
    $ Visit http://localhost:3000
    $ docker history node-multi-stage

    $ The first part of the Dockerfile creates three layers. 
      The layers are then merged and copied across to the second and final stage.  
      Two more layers are added on top of the image for a total of 3 layers.


## Using Small Docker Image - node-distroless

Clone or copy the repo and do the following:

    $ cd /path/to/repo
    $ docker build -t node-distroless .
    $ docker run -p 3000:3000 -ti --rm --init node-distroless
    $ Visit http://localhost:3000
    $ docker history node-distroless

    $ An image without all the extra unecessary binaries

## Using Small Docker Image - node-alpine

Clone or copy the repo and do the following:

    $ cd /path/to/repo
    $ docker build -t node-alpine .
    $ docker run -p 3000:3000 -ti --rm --init node-alpine
    $ Visit http://localhost:3000
    $ docker history node-alpine

    $ A Linux distribution with a smaller size
