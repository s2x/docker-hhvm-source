# docker-hhvm-source
Just a docker container with debian ready to build hhvm. It should be usefull for developers who want to contribute to hhvm but have problem with setting up env. 

## Requirements
* git
* docker and docker-compose
* lot of time and fast internet conneciion

## Instalation
* ```git clone https://github.com/s2x/docker-hhvm-source.git```
* ```cd docker-hhvm-source```
* ```git clone git://github.com/facebook/hhvm.git --depth=1``` or ```git clone git://github.com/your-fork/hhvm.git --depth=1```
* ```cd hhvm```
* ```git submodule update --init --recursive```
* ```cd ..```
* ```docker-composer up```
