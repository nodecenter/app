# Nodecenter
Main app execution: raises the API and the UX in order to offer the user the ability to handle its *blockchain* nodes.

## Execution

```shell script
make run
```

```shell script
docker-compose up
```

And click [here](http://localhost:8080) to see your app running!

# Voting
To see the voting process and proceed to vote, you need to expose an extra RPC API, run this commands on a shell with a running node to enable it:

```shell script
docker stop Node_Local
docker rm Node_Local
docker run -p 8545:8545 -p 30303:30303/tcp -p 30303:30303/udp --name Node_Local blockvalley/local --rpc --rpcaddr 0.0.0.0 --rpcapi eth,web3,net,clique
```
