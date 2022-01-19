# POA_Development_Chain

Create a README.md in your project directory and create documentation that explains how to start the network.

1. To start the network make sure to create node address for the network.
./geth --datadir node1 account new
./geth --datadir node2 account new

2. Next you want to run puppeth, here you want to create a genesis block(a starting block for the network). 

3. You want to create us the two node wallets you created to use in the seal step and the prefund step, also make a three digit id code for your network(this will be important when connecting to my crypto). also make sure you don't add a prefund amount and put a password if you want.

4. Then export the genesis configuration, here you will see the files to start the network.

5. ctrl+c to exit puppeth. Use geth in order to initialize the nodes.
./geth --datadir node1 init networkname.json
./geth --datadir node2 init networkname.json

6. when you initialize nodes you should se successful after initializing.

7. Now you must start your nodes.
./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --rpc --allow-insecure-unlock
8. make sure to record the endode when you start the first node. and paste it into the node2 geth. (--mine begins the nodes mining process)
./geth --datadir node2 --unlock "SEALER_TWO_ADDRESS" --mine --port 30304 --bootnodes "enode://SEALER_ONE_ENODE_ADDRESS@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock

9. In mycrypto make sure to conect to your nodes(the recording of chain id and network name). Also refer to "mycrypto screen-shots" for visual in structions.

10. When you get on mycrypto, make sure to click on "change network"(refer to "mycrypto folder"). then click on "add custome node"(refer to "mycrypto folder").

11. make sure network is custom and add the url in the "mycrypto folder". once eveything is filled out, connect to you network. then you want to connect to Keystone file and add you node link that's in your blockchain network. put in your pasword if you made one. then you should see a large amount of eth in your wallet.

12. make a transaction between your two nodes and Congratulations you've made a succesful transaction on your testnet.

