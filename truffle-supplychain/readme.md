# Xooa SupplyChain Log Smart Contract (Using Truffle Framework)

# Overview
	This smart contract provides 5 functions:
  * addOrder
  * isExistingOrder
  * getOrderCount
  * getOrderIdAtIndex
  * getOrderById

#### addOrder
addOrder method is used to store order in the ledger.
This method creates a transaction in the blockchain ledger and stores the key value pair.
If it succeeds in creating the transaction it returns a response with transactionId

#### isExistingOrder
isExistingOrder method is used to verify order already exists in ledger.
This method expects a single argument as the orderId whose existance is to check.
If it succeeds it returns a response as true.

#### getOrderCount
getOrderCount method is used to fetch all count if all the orders
If it succeeds it returns a response with total orders count

#### getOrderIdAtIndex
getOrderIdAtIndex method is used to fetch the orderId at given index
This method expects a single argument as a index
If it succeeds it returns a response with orderId at given index

#### getOrderById
getOrderById method is used to fetch the details about the given orderId
This method expects a single argument as orderId whose details want to fetch
If it succeeds it returns a response with details of given orderId