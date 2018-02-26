# Small Docker Image

## Requirements

In order to use this repository you need the following:

- Docker https://www.docker.com/docker-mac

## Using Small Docker Image

Clone or copy the repo and do the following:

    $ cd /path/to/repo
    $ docker build -t node-vanilla .
    $ docker run -p 3000:3000 -ti --rm --init node-vanilla
    $ Visit http://localhost:3000
