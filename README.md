
This page provides a step-by-step tutorial to deploy a sample app with Xooa's blockchain platform-as-a-service (PaaS).

**Project documentation:** <https://docs.xooa.com>

# Overview

This repository contains blockchain smart contracts, also known as chaincodes. Use the Xooa console to deploy it.

Xooa provides a permanent cloud end-point for the smart contracts, enabling cloud-to-cloud integration, while retaining blockchain's peer-to-peer capabilities.

|Directory                |Description                          |
|----------------|-------------------------------|
|[balance-transfer-java](https://github.com/Xooa/samples/tree/master/balance-transfer-java)|Sample smart contract runs on `Hyperledger Fabric` and is written in `Java`. Provides `Invoke`, `query` and `delete` functions. Originally created by IBM and forked from [here](https://github.com/hyperledger/fabric-samples).
|[balance-transfer-node](https://github.com/Xooa/samples/tree/master/balance-transfer-node)          |Sample smart contract runs on `Hyperledger Fabric` and is written in `JavaScript`. Provides `Invoke`, `query` and `delete` functions. Originally created by IBM and forked from [here](https://github.com/hyperledger/fabric-samples).
|[ethereum](https://github.com/Xooa/samples/tree/master/ethereum)          |Sample smart contract runs on `Ethereum` and is written in `Solidity`. Provides `Get` and `Set` functions. 
|[get-set](https://github.com/Xooa/samples/tree/master/get-set)          |Sample smart contract runs on `Hyperledger Fabric` and is written in `GoLang`. Provides `Get`, `Set` and `GetVersion` methods. Originally created by IBM and forked from [here](https://hyperledger-fabric.readthedocs.io/en/release-1.2/chaincode4ade.html#pulling-it-all-together).
|[marbles](https://github.com/Xooa/samples/tree/master/marbles)          |Sample smart contract runs on `Hyperledger Fabric` and is written in `GoLang`. Provides 9 functions to interact with marbles app. Originally created by IBM and forked from [here](https://github.com/IBM-Blockchain-Archive/marbles).
|[smartthings](https://github.com/Xooa/samples/tree/master/smartthings)          |Sample Groovy files  to deploy on smartThings platform. Integrate blockchain to smartThings.
|[truffle-supplychain](https://github.com/Xooa/samples/tree/master/truffle-supplychain)          |Sample smart contract runs on `Ethereum` and is written in `Solidity` using `Truffle framework`. Provides 5 functions to interact with supply chain app.

## Deploy the smart contract


1. Log in to the Xooa blockchain console at [https://xooa.com/blockchain](https://xooa.com/blockchain?utm_source=samplesRepo).
2. Go to [**Apps**>**Deploy New**](https://xooa.com/blockchain/new-app).
3. Select the method to deploy smart contract from. For example, use **Xooa Github** to deploy one of the samples provided by Xooa. Tap **Next**.
  > For accesing **Private Git Repos**, click or tap **Authorize Private Github Access**.

<p align="center"><img src="https://github.com/Xooa/samples/blob/master/images/deploy1.gif" alt="deploy" width="700px"/></p>

4. Select the Smart Contract you want to deploy, and then click **Deploy**.

5. Relax:  Xooa is doing the blockchain heavy lifting. You will be redirected to app dashboard when the deployment completes.

<p align="center"><img src="https://github.com/Xooa/samples/blob/master/images/identity1.gif" alt="identity creation" width="700px"/></p>

6.  Navigate to **Identities** tab, click or tap **Add New**, enter name for Identity  and set permissions to Read+Write. 

7. Copy and store the **API Token** value. You need it to authorize API requests. API Token cannot be dispalyed after you closed the window, but it may get regenerated. 

> **Note:** Xooa.yaml is an optional configuration file used by Xooa platform to configure smart contracts. This file should be in the root directory of the Repo, if being used. This file tells Xooa the programming language, blockchain implementation, and path of the smart contract.

___

## Explore the end-points for the smart Contract

1. Go to the **Details** tab, click **Explore API's**.

2. Enter **API Token** in the field in navigation pane. This is used to authenticate all API calls.

3. Go to the **Smart Contract > Invoke Smart Contract Function** from the navigation pane.

<p align="center"><img src="https://github.com/Xooa/samples/blob/master/images/invoke1.gif" alt="Invoke" width="700px"/></p>

4. In the **fcn** field, enter the Smart Contract function name you wish to Invoke. 
For example, if using this repo **get-set** smart contract to store data in blockchain `set` should be entred as the **fcn** field value 

5. In the **body** field, enter the data in the format expected by the smart contract. 
For example, if using this repo **get-set** smart contract to store data in blockchain ledger using the **set** function, the body should be entered as: 

    `[ "<key>", "<value>" ]`

6. Click or tap  **try**.

7. To view your transaction in the blockchain Ledger, from your Xooa dashboard, go to **Ledger**.

8.  Go to the **Transactions** tab.
You can expand the data field to see your transactions.
