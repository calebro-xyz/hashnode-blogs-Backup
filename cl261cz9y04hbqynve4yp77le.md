## How Data Is Processed and Stored in the Blockchain

As blockchain technology is taking over the web, users are still finding it challenging to understand the difference between conventional web technologies and web3 technologies.

In this article, we’ll break down where the blockchain is stored and how data is processed in it.

## Fundamentals of Blockchain Technology

![blockchain blue blocks](https://cdn.hashnode.com/res/hashnode/image/upload/v1648007628346/PQuEs7rpq.jpg)

Blockchain, simply put, is a database that’s shared and synchronized across several computers in a network. In a blockchain, transactions are securely stored in a peer-to-peer network of computers, also known as nodes. It utilizes a hash, which is an unchangeable cryptographic signature. Hashing transforms every type of data into a unique set of characters, improving the blockchain's integrity. The key features of blockchain technology are transparency, security, and immutability. This means that once a transaction is recorded, it can’t be changed or deleted.

To clearly understand where the blockchain is stored, we must first have a clear picture of how the traditional web stores and processes information.

## How Data Is Stored Traditionally

In the traditional web, computers store data in centralized databases with tables, rows, and columns that can be read, written, updated, or deleted by the database administrator.

Centralized databases are easier to manage and are very scalable; however, lack transparency, security, and integrity. This is very unlike blockchain networks, which are transparent and immutable.

## How Transactions Happen in the Blockchain

For a transaction to take place in the blockchain, three components of the blockchain have to be present: nodes, blocks, and miners.

### 1. Nodes

![peer-to-peer network of nodes](https://media.giphy.com/media/bTrTnPMPq8UORCrBWG/giphy.gif)

A node can be any computer that is connected to a blockchain network to validate and relay transactions. All nodes on a blockchain are linked together, and they frequently exchange the most recent data with one another, ensuring that all nodes are up to date.

The three primary roles of nodes are: 
Verifying transactions on the blockchain, and accepting or denying them based on authenticity.
Storing block transactions on the blockchain.
Sharing transaction information with other nodes on the blockchain.

### 2. Blocks

In a blockchain, a block is a single, unique unit of transactional records. Blocks can be differentiated based on their role in the network.

- **Genesis block**: The founding block in a network. In other words, the first block in the blockchain. This block makes the network immutable by allowing the creation and linking of subsequent blocks.

- **Valid blocks**: Blocks that have been mined and are now part of the blockchain. Valid blocks contain transactions that have been validated/verified by miners.

- **Orphan blocks**: Blocks that are no longer part of a blockchain network. Orphan blocks are rejected blocks that are created when numerous blocks are mined at the same time but are not added to the blockchain.

3. Miners

The process of adding new transactions on the blockchain is called **mining**. Miners validate/verify transactions, which are then added to a blockchain. 

### How a Transaction Happens

A blockchain transaction life-cycle has three stages: authentication, authorization, and proof-of-work (PoW).

#### 1. Authentication

Before any transaction takes place, a user has to successfully authenticate themselves using their wallet’s private keys. The most popular authenticating method is using a seed phrase.

A seed phrase is a randomly selected set of words that represent a long string of random numbers and letters (your private key). 

A private key looks like this:

`0C28FCA386C7A227600B2FE50B7CAE11EC86D3BF1FBE471BE89827E19D72AA1D`

This is a bit hard to memorize, so instead, we use a seed phrase as such:

`spare govern hawk eternal decline session load grace peasant west bargain always meadow ensure quality hill neglect hand toss lyrics stereo call snap about`

Usually, accessing your wallet with a seed phrase is easier than using your private key because it’s easier to remember. Seed phrase authentication enhances the anonymity and privacy of blockchain transactions, since there is no central authority managing authentication.

#### 2. Authorization

Authorization refers to every node on the network agreeing with each other in order to approve a transaction. In other words, in the blockchain, consensus must be reached for a transaction to be validated. The nodes will approve a transaction once it meets the criteria that’s set by the smart contract.

After the transaction is approved, it’s stored on the blockchain. Once a transaction is stored on the blockchain, it cannot be changed.

#### 3. Proof-of-Work (PoW)

In short, proof-of-work is a complex algorithm that’s used by cryptocurrency miners to validate transactions. With this algorithm, you can confirm the transactions to create new blocks in the blockchain. 

The miners compete against each other to complete this complex algorithm because they’re compensated financially every time a new block is added to the chain. This is because it takes a lot of computational power to solve these complex algorithms.

> Proof-of-Stake (PoS): Proof-of-stake is the alternative consensus mechanism used in blockchain. With proof-of-stake, the members holding the largest amount of the network’s native currency have the most power to validate transactions.

## How Data Is Stored in the Blockchain

In the blockchain, data is accessed, validated, and recorded by all nodes in the network. So what are the actual contents of a block and what type of data is stored in the blockchain?

A block has two sections: a header and a body. The header is part of the block that contains information used to identify a block, while the body is the part of the block that contains the data (transactions).

### Block Header

A block header contains the metadata associated with the block. 

The metadata is:

* **Version of the block**. A 4-byte field that contains the block's version number. The block’s version number specifies the rules to validate a block. For example, in Bitcoin, there are 4 block versions, with each version being an improvement of the previous block’s rules. 

* **Hash of the previous block**. The block’s identity. It’s a unique set of strings that identifies a specific block and ties it to the following block, forming a chain of blocks. In other words, every new block is generated from the previous block’s hash.

![structure and content of blocks](https://www.nist.gov/sites/default/files/images/2019/09/25/blockchain.png)

* **Time**. The timestamp when a block is being hashed.

* **Merkle tree**. A Merkle tree is a data structure algorithm in which each node is marked with a block's cryptographic hash. A Merkle tree uses a Merkle root mathematical formula to validate data in the network. This is for efficient and secure verification data in the blockchain.

* **Bits**. Stores a difficulty target, which is a 4-byte file that specifies the difficulty of the mathematical problem miners solve in order to validate transactions.

* **Nonce**. A nonce (number used once) is a random number that gets the hash of a block. Locating the nonce is what miners do when they validate blocks. The difficulty target must be equal to or less than the nonce for the block to be validated.

This metadata is public in the Bitcoin network, and can always be further explored and viewed using blockchain explorers like [Etherscan](https://etherscan.io/) or [Blockchair](https://blockchair.com/).

### Block Body

The block’s body is where all the transactions of a block are stored. A single block can hold up to 500 transactions, which is the case in the Bitcoin network. The larger the size of a block, the faster the transactions in the blockchain.

## Types of Blockchain and How They Store Data

Different blockchains have different data structures. Let’s review how data is structured in Bitcoin and the Ethereum network.

### Bitcoin

![bitcoin physical coin](https://cdn.hashnode.com/res/hashnode/image/upload/v1648024835843/Qu0QgLiLi.jpg)

Bitcoin was the first cryptocurrency and also the first practical application of blockchain technology. Transactions in Bitcoin can be modeled using Unspent Transaction Output (UTXO). UTXO refers to the amount of Bitcoin left after a transaction takes place.

A UTXO database stores the change from Bitcoin transactions. This database's initial state is 0. The database fills up with change entries from several transactions, as the number of transactions grows.

Any outputs that remain unspent by the time a transaction is complete are deposited back into a database as inputs to use in a subsequent transaction.

The following metadata is supplied in every Bitcoin transaction:

- **tx_in count**: The number of transaction inputs in total.

- **tx_ins**: Keeps a list of all transaction inputs.

- **tx_out count**: The number of transaction outputs in total.

- **tx_outs**: List of all transaction outputs.

- **Script witnesses**: This file contains a serialization of all SegWit transaction witness data.

- **Lock time**: Specifies **when** a transaction can be included in the blockchain. It’s a 4-byte value that specifies the block number or timestamp for the transaction until it’s locked. It's usually set to 0, which means the transaction is valid as soon as the block is completed. 

### Ethereum

![ethereum logo](https://cdn.hashnode.com/res/hashnode/image/upload/v1648007984625/oFSiormtE.jpg)

Bitcoin's major limitation was scalability, meaning that a single block in the Bitcoin network could hold only 1MB of data. The Ethereum network was built using the **trie** data structure to solve performance and scalability challenges that the Bitcoin network faced.

A *trie*, often known as a digital tree, is a data-structure method that contains a set of strings connected by links between nodes. The Ethereum network has four tries: state, storage, transaction, and receipt tries.

* **State trie**: Stores temporary network data such as account keys, number of transactions, addresses and account balance. The state trie's data is continually updating as transactions happen. Basically, a state trie maps addresses to account statuses.

* **Storage trie**: Stores smart contract data. It holds account data, such as account balance and number of transactions associated with the account. Each Ethereum account has a storage trie of its own. 

* **Transaction trie**: A transaction trie is specific to each block. Transaction trie captures transaction request vectors like gas value, transaction value, gas limit, recipient, and nonce.

* **Receipt trie**: Holds post-transaction data, such as amount of gas used, post-transaction state, and transaction logs. 

## Conclusion

In this article, we broke down how transactions in the blockchain network take place and the components necessary for it to work. We also explored types of blockchains and how they store data. 

Learn more about web3, NFTs, blockchain, and DAOs on [Hashnode’s web3 blog](https://web3.hashnode.com)


