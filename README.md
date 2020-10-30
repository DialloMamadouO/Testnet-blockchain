### Testnet Blockchain
In this project, we will set up a testnet blockchain using the following:
Puppeth, to generate a genesis block.
Geth, to create keys, initialize nodes, and connect the nodes together.
The Clique Proof of Authority algorithm.
## Custom testnet blockchain set up
In order to set up  the custom testnet, we will use the following:
•	Puppeth, to generate a genesis block.
•	Geth, to create keys, initialize nodes, and connect the nodes together.
•	The Clique Proof of Authority algorithm.
Using Geth, we will generate two new nodes with new account addresses that will serve as our pre-approved sealer addresses.

 ./geth account new --datadir node1
 
 ./geth account new --datadir node2



 
