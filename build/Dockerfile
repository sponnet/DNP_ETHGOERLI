FROM ethereum/client-go:stable

RUN apk update && \
    apk add git && \
    rm -rf /var/cache/apk/*

USER root


RUN git clone https://github.com/goerli/testnet.git 
#RUN ln -s /home/geth/bin/parity /usr/local/bin/parity



ENTRYPOINT /cmd/geth --datadir /ethgoerlidnpdappnodeeth_data/goerli/geth init ./geth/goerli.genesis







