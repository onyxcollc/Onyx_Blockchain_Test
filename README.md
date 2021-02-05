# ZBank_Blockchain_Test

<img src="Screen_Shot/blockchain_pic.jpg"/>

---

## Background

Project is to set up a private testnet that you and your team of developers can use to explore potentials for blockchain at the ZBank.

In order to set up the tesnet, you will need to use the following skills:

* Puppeth, to generate block.
* Geth, a command-line tool, to create keys , initialize nodes and connect the nodes together. 
* The Clique Proof of Authority 
---

### Build Node

One of the first things you would want to do to create your POA is to create your 2 node's first, by using the the command line the terminal 

(./geth --datadir node1 accounnt new).
Make sure you save your address, secret key , and private key. 

You would also want to init both node's after you create your network with this command line  ( ./geth --datadir node1 init networkname.json )

<img src="Screen_Shot/node_creation.jpg"/>

---

### Genesis Block Creation
 To create a new genesis block ( puppeth ) is needed. command line ( ./puppeth ).
 Follow the prompts to complete the genesis; you should pre-fund the pre-compiled account also. 
 Export genesis configuration.

<img src="Screen_Shot/configured_genesis.jpg"/>


---

### Node Activated 
Next you would need to init node 1 and node 2 with the command line (  ./geth --datadir node1 init networkname.json ).

Run the nodes in separate terminal with the command line 

1. ./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --rpc --allow-insecure-unlock

2. ./geth --datadir node2 --unlock "SEALER_TWO_ADDRESS" --mine --port 30304 --bootnodes "enode://SEALER_ONE_ENODE_ADDRESS@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock

<img src="Screen_Shot/nodes_activated.PNG"/>

---


### Transaction Results

In conclusion  POA had some minor issues trying to complete transactions, but the block chain was build successfully. 
<img src="Screen_Shot/Transaction.PNG"/>



---
