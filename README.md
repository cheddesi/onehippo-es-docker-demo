# OneHipp and Elaticsearch integration containerized demo
This project is fully containerized demo of Integrating OneHippo CMS with Elasticsearch as indexing platform.
## About the OneHippo integration with Elasticsearch
Following diagrams represents the integration approach followed in this demo.

![OneHippoES Setup](images/onehippoesint.png)

## About the container setup
Follow diagram presents the services part of this demo pack.

![Containers Setup](images/containers.png)

## Pre-requisites
This demo setup was tested with Docker Toolbox for windows on Windows 10 OS.
Should be usable on Docker for Mac or Docker for Windows as well.

Following setting must be enabled on docker machine to run elasticsearch in production mode.
```sh
docker-machine ssh default
sudo sysctl -w vm.max_map_count=262144
exit
```
Allocate enough RAM to the docker machine. 4GB is recommended.
## Running the demo
1. Clone the git repo to local machine
```sh
git clone https://github.com/cheddesi/onehippo-es-docker-demo.git
```
2. Navigate to the directory that contains docker-compose.yml file.
```sh
cd onehippo-es-docker-demo
```
3. Run the containers
```sh
docker-compose up -d
```
4. Check whether the containers started successfully or not
```sh
docker ps
```
You can check the logs of individual containers with following commands
```sh
docker logs es01
docker logs kibana01
docker logs hippo01
```
## Appendix
* LINKS to git repos
  * https://hub.docker.com/r/cheddesi/onehippo-es-demo/
  * https://github.com/cheddesi/camel-events-support
* LINKS to helpful articles
* Instructions to generate own certs