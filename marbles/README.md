# Xooa Marbles Smart Contract

This page provides an overview to Xooa Marbles Smart Contract functionalities.

This smart contract runs on `Hyperledger Fabric` and is written in `GoLang`.

Originally created by IBM and forked from [here](https://github.com/IBM-Blockchain-Archive/marbles).

## Overview

This smart contract provides 9 functions:
  
  * InitMarble
  * TransferMarble
  * TransferMarbleBasedOnColor
  * ReadColor
  * QueryMarblesByOwnerColor
  * QueryMarbles
  * GetHistoryForMarbles
  * GetMarblesByRange
  * Delete


#### InitMarble

InitMarble method is used to create a new Marble.
This method expects four arguments `[ "<name>", "<color>", "<size>", "<owner>" ]`.


#### TransferMarble

This method transfers a marble to a new owner.
This method expects two arguments `[ "<name>", "<owner>" ]`.


#### TransferMarbleBasedOnColor

This method transfers a given color marble to a new owner.
This method expects two arguments `[ "<color>", "<owner>" ]`.


#### ReadMarble

This method is used to get the details of a marble.
This method expects an argument `[ "<name>" ]`.
It returns the color, docType, name, owner, and size.


#### QueryMarblesByOwner

This method is used to query marbles for the owner.
This method expects an argument `[ "<owner>" ]`.
It returns the key and record object which contains color, docType, name, owner, and size.


#### QueryMarbles

This method is used to perform a query for marble using a selector criteria.
This method expects an argument `[ { "selector" : { "<key>" : "<value>" } } ]`.
It returns payload containing the key and record object which contains color, docType, name, owner, and size.


#### GetHistoryForMarbles

This method is used to get the history of transfers of a marble.
This method expects an argument `[ "<name>" ]`.
It returns the history of transfers of a marble.


#### GetMarblesByRange

This method is used to perform a range query based on the start and end keys provided.
This method expects an argument `[ "<startKey>", "<endKey>" ]`.
It returns payload containing the key and record object which contains color, docType, name, owner, and size.


#### Delete

This method is used to delete a marble.
This method expects an argument `[ "<name>" ]`.


## Deploy the Xooa-Marbles smart contract 
 
1. Follow the instructions here: https://docs.xooa.com/start.html#deploy-the-smart-contract-app, selecting the **Xooa-Marbles** as the smart contract.

2. Record the **API Token** when it is shown: you will need it to authorize API requests from swagger.

   > **Tip:**  to regenerate the API token: 
   >
   > 1. Go to the **Identities** tab in the App. 
   > 2. Click **Actions** for the identity for which token is to be regenerated.
   > 3. Select **Regenerate API Token**, and then click on **Generate**.


## Explore the Xooa-Marbles smart Contract end-points

1. Go to the **API** tab, and  under API Explorer paste API Token and click **Authorize API** .

2. Scroll below and select any endpoint and click **Try it out**.

3. In the **body** field, replace placeholder with your own data to store in the blockchain.

4. Click **Execute**. 

> **Congrats!** You have saved data in a blockchain using **Xooa**.

5. To view your transaction as part of the blockchain, go to [https://xooa.com/blockchain](https://xooa.com/blockchain/ledger?utm_source=samplesRepo) or navigate to **Ledger** from your Xooa console.

6. Navigate to **Transactions** tab.

7. You can expand the data field to see your transactions.


## What is swagger.json and it's purpose

Swagger is used to simplify API development and is used by Xooa for defining REST APIs. 
Using swagger Xooa provides you an interface to make API requests.
Place **swagger.json** file along with your Smart Contract and Xooa will pick it up while deploying and will integrate it with your app.

### Steps to access [swagger](https://docs.xooa.com/API.html)

1. Go to [https://xooa.com/blockchain](https://xooa.com/blockchain/custom-smart-contracts?utm_source=samplesRepo) or navigate to **Custom Smart Contracts** from your Xooa console.

2. Click **Deploy New** or select an existing app to upgrade.

3. Once the app is deployed or upgraded successfully, Navigate to **API** tab and select **Sandbox** option and there you will find API Explorer.

4. Paste API token in the required input box and click on **Authorize API** to access swagger REST APIs.