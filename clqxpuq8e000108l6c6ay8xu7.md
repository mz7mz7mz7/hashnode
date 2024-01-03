---
title: "Blockchain immutability: Behind smart contracts"
datePublished: Tue May 29 2018 10:00:00 GMT+0000 (Coordinated Universal Time)
cuid: clqxpuq8e000108l6c6ay8xu7
slug: blockchain-immutability-behind-smart-contracts
canonical: https://espeo.eu/blog/ethereum-smart-contract/
tags: immutable, blockchain, immutability, smart-contracts

---

#### **The Ethereum smart contract has taken the world by storm, with its wide** [**adoption for ICOs.**](https://espeoblockchain.com/blog/how-start-an-ethereum-ico/https://espeoblockchain.com/blog/how-start-an-ethereum-ico/) **Smart contracts are, in essence, computer programs executed in a sandboxed environment, so one that restricts them. That restriction provides special functions and properties: the famous blockchain immutability is one of them. Let’s dive into those.**

## **Blockchain immutability**

As I wrote, one of the defining properties of smart contracts like the Ethereum smart contract is that their code is **immutable** . Blockchain immutability means that parties agree to the terms or “code” of the contract, that code can’t be changed by any party unilaterally.

The result of the execution of the smart contract is similarly unchangeable. Of course, that happens once the agreed-on code is executed and produces a result. The result should be objectively verified by the other party to that contract, or even by an external party. For example, this could be a regulator or observer. Only then you can be 100% certain it’s valid.

## **Free from external factors**

The immutability of the results of the executed smart contracts stems from what I’ve mentioned at the beginning. What’s important is the context in which the smart contract is executed: **sandboxes** . **That means the contract is free from the influence of any external factors**. An environment like that guarantees the *determinism* of computational results.

T he only factors that influence the result are the **input data to the smart contract, and the data stored within the smart contract environment** . By the latter, I’m referring to the data that was stored there when smart contract was instantiated for the first time. Or, by the previous execution iterations of the same contract. In some smart contract environments (like Ethereum) smart contracts can also communicate with each other and influence the execution of one another. However, **this is still done in controlled and deterministic way.**

## **The Ethereum smart contract’s not the only one. Other implementations**

Various implementations of smart contracts seek to leverage their benefits. **Bitcoin’s** smart contract language (script) is intentionally limited in complexity. The logic that can be expressed in it is very restricted. On the other hand, we have the Ethereum smart contract. The set of the operations that can be executed within the **Ethereum Virtual Machine** is much broader. Almost any reasonable algorithm or logic could be expressed in it, though there are still limitations on the number of operations per invocation.

Going even further, **Hyperledger Fabric** has no restriction on the complexity of the smart contract logic or the number of operations. That means it’s very powerful. However, it it also greatly increases the risk of node consensus divergence if that power isn’t used properly. Generally speaking, the level of **expressiveness** is a feature of a particular implementation. It can vary, providing different levels of security and strength for particular use cases.  
It’s worth knowing the **consensus doesn’t have to be immediate**. Depending on the implementation, it might take around 1 hour (Bitcoin) to reach the semi-final consensus, or be almost immediate (Hyperledger Fabric). That’s despite the fact that once the consensus is reached, the smart contract execution result is **provable and immutable.**

## **Controlled access**

Some smart contracts need to have **access to structured data from the outside of their environment** . In most implementations, controlled access to that data can be provided by privileged actors. They’re able to fetch the data needed at the specified time. Then, they can provably transform the data to a format that can be processed by the smart contract. Actors like that are called **Oracles**. They’re an inherent part of the productive smart contract ecosystem. They don’t change the other properties of the smart contracts. Oracles also work in the same sandboxed environment as the other smart contracts. Once the data is provided, it can’t be modified and is ‘provable’ forever.

## **Can smart contracts function without a blockchain?**

If we want to execute smart contracts with the listed properties, they need to have access to some form of history inalterability. At the least, we’d need a way to prove that the history was changed and the observed results can’t be trusted any longer.

**Blockchain** is one technique that gives that particular feature but there’s research being done on other techniques. One of them is **DAG** (directed acyclic graph) where the smart contract transactions form a graph of relations (not being part of the chain of blocks). Yet another approach was undertaken by the [**Corda**](https://www.corda.net/) platform. There are no blocks in Corda, and transactions are exchanged directly between interested parties in the form of cryptographically signed sets of data.

Blockchain immutability brings many advantages to [various industries](https://espeoblockchain.com/blog/crypto-payments-digital-cash/), and is one of the features that inspire our clients to get on the blockchain. So, the Ethereum smart contract and the blockchain platform are what we deal with every day at Espeo Blockchain. That, and much more. If you’d like to leverage blockchain immutability in your project, we’re interested! Let us know in the box below.