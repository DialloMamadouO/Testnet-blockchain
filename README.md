# Testnet Blockchain
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
 
 We created an ethereum private network named mamadou by running Puppeth and selecting the option to configure a new genesis block.
We did choose the Clique (Proof of Authority) consensus algorithm and pasted the addresses of the 2 accounts we created earlier into the list 
of accounts to seal as well into the list of accounts to pre-fund. We did choose no for pre-funding the pre-compiled accounts 
(0x1 .. 0xff) with wei and completed the rest of the prompts.
Then, we did choose the manage existing genesis option and exported the genesis configurations to create the mamadou.json file.
With the genesis block creation complete, we initialized the nodes with the genesis' json file using geth.

./geth init mamadou.json --datadir node1
./geth init mamadou.json --datadir node2 

This step enables the nodes to be used to beging mining blocks.

Let's now start minind by running the nodes in seperate terminal windows with the commands:

-start node1
./geth --datadir node1 --mine --minerthreads 1 

-start node2
./geth --datadir node2 --port 30304 --rpc --bootnodes "enode://ac261a3f6ba54c01b2df930c5257369eefe180f63082617cbde0099a95b326a3d478ff139
8bbc95e85f3f5ed1fb72d5b98bd0e616b2880d872dfcef062b2def9@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock





 
