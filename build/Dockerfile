FROM ethereum/client-go:stable

RUN apk update && \
    apk add git && \
    rm -rf /var/cache/apk/*

USER root

RUN git clone https://github.com/goerli/testnet.git 


ENTRYPOINT  geth --datadir /ethgoerlidnpdappnodeeth_data/goerli/geth init testnet/geth/goerli.genesis && \
            echo NODES `cat testnet/bootnodes.txt | sed -n -e 'H;${x;s/\n/,/g;s/^,//;p;}'` && \
            geth --datadir /ethgoerlidnpdappnodeeth_data/goerli/geth --bootnodes `cat testnet/bootnodes.txt | sed -n -e 'H;${x;s/\n/,/g;s/^,//;p;}'`







