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
 
 We used Puppeth to create an ethereum private network named mamadou by running puppeth and selecting the option to configure a new genesis block.
We did choose the Clique (Proof of Authority) consensus algorithm and pasted the addresses of the 2 accounts we created earlier into the list 
of accounts to seal as well into the list of accounts to pre-fund. We did choose no for pre-funding the pre-compiled accounts 
(0x1 .. 0xff) with wei and completed the rest of the prompts.
Then, we did choose the manage existing genesis option and exported the genesis configurations to create the mamadou.json file.
With the genesis block creation complete, we initialized the nodes with the genesis' json file using geth.

./geth init estatenet.json --datadir node1
./geth init estatenet.json --datadir node2 
This step enables the to be used to beging mining blocks.




 
