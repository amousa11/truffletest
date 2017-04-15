# Truffle Basics Tutorial

A truffle tutorial by [Ali Mousa](https://github.com/amousa11) and [Collin Chin](https://github.com/collinc97)

## Setup

* Ethereum Client (original uses testrpc) v3.0.3
* [TestRPC](https://github.com/ethereumjs/testrpc)(Optional, but helpful for local tests)
* [Truffle v3.1.2](http://truffle.readthedocs.io/en/beta/)
* Npm 4.3.0 / Nodejs v6.10.0

## Deployment 
When you have a contract you are happy with you can follow these steps to deploy. 

For this example, we will assume you are running a TestRPC network on your local machine. For deployment on other networks, change the settings in truffle.js.

1. `cd` into your project directory. If you are following this tutorial, make sure you are in the `truffletest` folder
2. Now, run `truffle compile` to compile your contract. Here, truffle will either successfully compile or give you some errors that need correcting. This is what successful compilation looks like: ```
Compiling ./contracts/ConvertLib.sol...
Compiling ./contracts/Greeter.sol...
Compiling ./contracts/MetaCoin.sol...
Compiling ./contracts/Migrations.sol...
Writing artifacts to ./build/contracts
```
