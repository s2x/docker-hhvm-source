# docker-hhvm-source
Just a docker container with debian ready to build hhvm. It should be usefull for developers who want to contribute to hhvm but have problem with setting up env. 

## Requirements
* git
* [docker](https://docs.docker.com/engine/installation/#docker-variants) and [docker-compose](https://docs.docker.com/compose/install/)
* lot of time and fast internet connection

## Instalation
* `git clone https://github.com/s2x/docker-hhvm-source.git`
* `cd docker-hhvm-source`
* `git clone git://github.com/facebook/hhvm.git --depth=1` or `git clone git://github.com/your-fork/hhvm.git --depth=1`
* `cd hhvm`
* `git submodule update --init --recursive`
* `cd ..`
* `docker-composer up -d`

## Building

* First check if container is running `docker ps | grep "dockerhhvmsource_hhvm_1"`
* log in contailer `docker exec -ti dockerhhvmsource_hhvm_1 /bin/bash`
* `cd /hhvm`
* `cmake .`
* `make -j{threads}` for example 4 threads `make -j4`

## Testing
* `cd /hhvm.hphp`
* `./hhvm/hhvm test/run test/quick`
