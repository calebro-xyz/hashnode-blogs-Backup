## Proof of Work versus Proof of Stake consensus mechanisms


## Introduction

As you may already know, a blockchain is a distributed, decentralized, and immutable ledger that enables the recording of transactions in a computer network.

This means a blockchain network is not under the control of one person or organization, instead it relies on thousands of participants to keep data secure, unchangeable, and distributed.

To do this, the nodes (the computers that make up a blockchain) must have a way to determine whether a transaction is valid before adding it to the blockchain network. This is known as a consensus mechanism.

## Consensus mechanism

A consensus mechanism or a consensus algorithm is a system of agreement in which nodes decide which transactions to add to the blockchain. In cryptocurrency, consensus mechanisms have financial incentives.

There are several consensus mechanisms such as Proof of Work, Proof of Stake, Proof of Authority, Proof of Capacity, Proof of Burn, and Proof of Action.

 In this article, I will be diving deeper into the two most popular consensus mechanisms, Proof of Work and Proof of Stake.

### Proof of Work

![mining.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1662559914203/fggf8riDM.jpg align="left")

In the Proof of Work consensus algorithm, validators are required to use a significant amount of energy to solve a cryptographic equation first to validate a transaction and then get incentivized every time a new block is added to the network. This is popularly referred to as cryptocurrency mining.

#### The “Work”

The work in PoW involves miners engaging in trial and error effort to find a valid nonce that will be then used to solve the hash of the specific block. The miner who finds the nonce leading to a block hash first is then rewarded crypto or the native token of the blockchain. Blocks with valid nonce are then added to the network(chain) and the process is then repeated.

In Bitcoin, a new block is created every 10 minutes. To maintain this, the mining difficulties are then modified based on the computational power dedicated to mining the block, through a process known as difficulty adjustment. This means the more computing power is dedicated to mining a block, the more difficult it is to find the nonce and complete the hash.

Before being adopted by Satoshi Nakamoto as the consensus mechanism for the Bitcoin Blockchain, Proof of Work was initially used to prevent spam emails and DDOS (distributed denial of service). PoW remains the most widely adopted consensus mechanism with blockchains such as Bitcoin, Terra, Ethereum 1.0, and Dogecoin. 

#### Pros 

Enhanced Security - It is nearly impossible for malicious actors to create a valid block. This is because it will need them to control 51% of the hash rate and even if they did, the financial gains would be much lower than the computing power used. 

Financial incentives - Validator nodes that successfully validate a block of transaction and propagate it to the network are rewarded using cryptocurrency or tokens.

Low barrier to entry - Unlike PoS which requires participants to have a large number of tokens first, PoW makes it easy for any beginner with a computer to set up a validator node.

#### Cons 

Environmental sustainability - PoW is an energy-intensive consensus mechanism. A single Bitcoin transaction uses about 1400 Kwh equal to the power consumption of an average U.S. household over 50 days. This has even led to some countries completely banning the mining of cryptocurrencies.

No financial Penalty - PoW does not financially penalize malicious actors who try to disrupt the network or create invalid blocks instead their time, energy, and computing power is just depleted means and the attackers are not completely deterred.

Not scalable - Most PoW blockchains are not fast enough to handle current blockchain market demands, this is because a lot of energy is dedicated to solving complex cryptographic challenges and not necessarily validating transactions.

Centralization - Due to the need for high computing power in PoW, only a few participants have the resources and infrastructure to set up validator nodes. Leaving the control of the blockchain network in the hands of a few whales.

### Proof of Stake 

![proof of stake](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRq7Vz32z-vJPRtBYvu-1kN_cXxKBbRocMVSsnF0-PNHJTDF63EfKhQB9ZMJOms5qCUlU4&usqp=CAUalign="center")

In proof of Stake, a validator has to stake an agreed number of cryptocurrencies or tokens before they are allowed to validate a transaction. In case the validator is not able to validate the transaction or tries to act maliciously, they lose some of the staked amounts.

The PoS protocol randomly picks a validator node that is delegated the opportunity to validate a block of transactions. The higher the amount staked the higher, the higher the chances of being selected as a validator.

Participants with a smaller amount of tokens can combine effort and create a staking pool, to maximize their chances of getting selected to validate a block of transactions. The rewards are then distributed based on how much you contributed to the staking pool.

Ethereum, the second largest blockchain is shifting from PoW to PoS blockchain known as Beacon Chain. Validator nodes will be first required to deposit 32 ETH(ethereum blockchain native token) or more in a deposit contract. They are then added to a queue, which controls the number of validators in the network.

When the validator successfully validates a block of transactions, afterward they can cast a vote known as attestation and propagate the block to the rest of the network. If the staked amount falls below 16 ETH because of penalties they are therefore disqualified from acting as a validator.

Most newer blockchains prefer PoS to Pow. Blockchain networks using PoS are Ethereum 2.0(Beacon Chain), Polkadot, Cardano, and Avalanche.

#### Pros

Low consumption - Since PoS randomly picks validators and does not need validators to compete to solve complex cryptographic equations, the energy consumption is relatively very low. For example, the Ethereum network is estimated to cut its energy consumption by 99% when it completely moves from a PoW to a PoS mechanism.

Financial Penalty - In PoS, the staked amount acts as collateral in case a validator tries to create invalid blocks or abandons the validation process. They are so penalized according to the contract of the network. This enhances the integrity of the blockchain network.

Scalable - In PoS, if the volume of transactions in need of validation increases, the reward for staking increases too. This encourages participants in the network to stake more thus increasing the transaction throughput.

#### Cons 

Centralization - Dominance by large token holders threatens the decentralization of PoS blockchain networks.

PoS consensus mechanism has not been tested compared with PoW which still is used in 62% of the blockchain networks since 2009. This means there could be more limitations to the algorithm that cannot be detected at this point.

## The Final Thought

I have outlined in this article the two main consensus mechanisms used by the majority of blockchains. Proof of Stake and Proof of Work.

In addition, I have listed each consensus mechanism's benefits and drawbacks. This article is neither a piece of financial advice nor an endorsement of one consensus algorithm over the other. 

