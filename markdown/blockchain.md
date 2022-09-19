
<a href="projects.html" class="backButton">
  <img src="images/whitearrowleft.png" alt="back arrow">
</a>

# Blockchain
---
This is a simple version of a blockchain containing blocks which rely on each other to form a chain by using the previous blocks hash. It also contains wallets with a 
coinbase and ability to make transactions between these wallets. The project was made by following a guide to create a simple blockchain which can be found 
<a href="https://medium.com/programmers-blockchain/create-simple-blockchain-java-tutorial-from-scratch-6eeed3cb03fa">here</a>. A sample of the terminal output when run 
which creates blocks, wallets, performs transactions between these wallets, and verifies that the blockchain is still valid can be found below:
        
```text
Creating and Mining Genesis block...
Transaction Successfully added to Block
Block Mined!!! :0fd1bf3c22b794ceb66370b08089010eacf3d34e37d02e2ee8d645a70ca3ddc6

WalletA's balance is: 100.0

WalletA is Attempting to send funds (40) to WalletB...
Transaction Successfully added to Block
Block Mined!!! :00229bf506b8a36877bc07155b67456029c97eaffb9993db2e24ea3031dd81e1

WalletA's balance is: 60.0
WalletB's balance is: 40.0

WalletA Attempting to send more funds (1000) than it has...
#Not Enough funds to send transaction. Transaction Discarded
Block Mined!!! :050c9859955059b2478827c6ccb02e7898667ba26abc87b921aaa61d103a16ee

WalletA's balance is: 60.0
WalletB's balance is: 40.0

WalletB is Attempting to send funds (20) to WalletA...
Transaction Successfully added to Block

WalletA's balance is: 80.0
WalletB's balance is: 20.0
Blockchain is valid
```
<a href="https://www.github.com/cladnic/simpleblockchain" target="_blank" class="repository">
    <span>source code</span>
    <img src="images/whitegithubbtnimg.png" alt="github image">
</a>