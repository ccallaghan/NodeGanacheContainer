# VS Code remote container for etherium playground

How to use this project -> https://code.visualstudio.com/docs/remote/containers#_managing-extensions

This VS code env contains a docker compose file that creates a ganache eth blockchain for testing and developing against.
Also contains a node version 16 container for developing code against this blokchain.

Documentation for the ganache container can be found here -> https://hub.docker.com/r/trufflesuite/ganache-cli

Some useful commands:

To test if the blockchain is working properly, open a console and run:

```
curl -H "Content-Type: application/json" -X POST --data \
        '{"id":1337,"jsonrpc":"2.0","method":"evm_snapshot","params":[]}' \
        http://localhost:8545
```

To see the etherium accounts created on the blockchain

```
curl -H "Content-Type: application/json" -X POST --data \
        '{"id":1337,"jsonrpc":"2.0","method":"eth_accounts","params":[]}' \
        http://localhost:8545
```