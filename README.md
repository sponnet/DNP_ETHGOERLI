# Görli testnet DAppnode package

Implements the install instructions for the Görli testnet as a DAppNode package

- https://github.com/goerli/testnet
- https://dappnode.io/


## Prerequisites

- git

   Install [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) commandline tool.

- docker

   Install [docker](https://docs.docker.com/engine/installation). The community edition (docker-ce) will work. In Linux make sure you grant permissions to the current user to use docker by adding current user to docker group, `sudo usermod -aG docker $USER`. Once you update the users group, exit from the current terminal and open a new one to make effect.

- docker-compose

   Install [docker-compose](https://docs.docker.com/compose/install)
   
**Note**: Make sure you can run `git`, `docker ps`, `docker-compose` without any issue and without sudo command.


## Buidling

`docker-compose -f docker-compose-ethgoerli.yml build`

## Running

### Start

`docker-compose -f docker-compose-ethgoerli.yml  up -d`

### View logs

`docker-compose -f docker-compose-ethgoerli.yml  logs -f`

### Stop

`docker-compose -f docker-compose-ethgoerli.yml down`

## Note

This is early stage software - the testnet is not operational yet

## TODO's

- Add a way to add the validator account to docker image upon build


