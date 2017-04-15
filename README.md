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

1. First, `cd` into your project directory. If you are following this tutorial, make sure you are in the `truffletest` folder
2. Now, run `truffle compile` to compile your contract. Here, truffle will either successfully compile or give you some errors that need correcting. This is what successful compilation looks like for our project: 
```
Compiling ./contracts/ConvertLib.sol...
Compiling ./contracts/Greeter.sol...
Compiling ./contracts/MetaCoin.sol...
Compiling ./contracts/Migrations.sol...
Writing artifacts to ./build/contracts
```
3. Next, we want to put our contract on the network to be mined. Call `truffle migrate` to migrate the contracts to the address specified in `truffle.js`. In our project, this is `localhost:8548`. This step will return the following upon success: 
```
Using network 'development'.

Running migration: 1_initial_migration.js
  Deploying Migrations...
  Migrations: 0x523d5b8fa3ff5946b8c0802a5c8520b1be0346e3
Saving successful migration to network...
Saving artifacts...
Running migration: 2_deploy_contracts.js
  Deploying ConvertLib...
  ConvertLib: 0x33ced344ba01047eef8a9b6393a754fbd8259cf5
  Linking ConvertLib to MetaCoin
  Deploying MetaCoin...
  MetaCoin: 0x7743b55487e04751a384c39bd7cefc05a20222c8
  Deploying greeter...
  greeter: 0xaa5a2306dcea9157f30ab4d9ce4317619f604763
Saving successful migration to network...
Saving artifacts...
```
4. We can call functions from our contract using `truffle console`. This command should enter you into a console that will look like this: `truffle(development)>`
5. From here, we access our contract by saving the contract to a variable: 
`var greeter = greeter.at("0xaa5a2306dcea9157f30ab4d9ce4317619f604763");`
6. Finally, **call** the method on the greeter contract that we want `greeter.greet()`. NOTE: For **transactions**, you would want to read more on [this page](http://truffle.readthedocs.io/en/beta/getting_started/contracts/#reading-writing-data).

# Questions

If there are any changes you'd like to suggest or issues you are having, reach out to me at [alimousa@berkeley.edu](mailto:alimousa@berkeley.edu)
