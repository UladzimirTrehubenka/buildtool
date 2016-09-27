# Collection of Docker images to compile the Go projects

This repository provides the set of the Docker images used to compile the Go projects.

## Build

The build of the Docker image require the [docker](https://docs.docker.com/engine/installation/)
engine and the ```make``` utility as pre-requisites. As the requirements are satisfied, use the
following command to compile the Docker image of version ```v1```:
```sh
make v1
```

## Usage

To compile the Go binary using the provided tool, you could start with the following command,
where ```project``` variable defines the Go project:
```sh
docker run --rm -v $(pwd):/go/src/${project} \
    infoblox/buildtool:v1 go build -o binary
```
