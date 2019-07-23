# Build CryptoStar Dapp on Ethereum

This project is build cryptostar dapp that implements a star notary smart contract, where the information about people's favourite stars in the sky can be managed by means of the blockchain.



## Token Info

* ERC-721 token name : "Star Token"

* ERC-721 token symbol : "STR"

* Contract Address in Rinkeby Network : 0x3e5DC2e7377DBf7e010C0A2bbe80a9f255259212

  ```
     Replacing 'StarNotary'
     ----------------------
     > transaction hash:    0x161712d01f4965e5b62b8b46ec2462dea22180aec53aec2061174ef99dde0584
     > Blocks: 0            Seconds: 6
     > contract address:    0x3e5DC2e7377DBf7e010C0A2bbe80a9f255259212
     > block number:        4783950
     > block timestamp:     1563889164
     > account:             0xF09c02c1cA4B098B2ADA2669A22142d8baF44f88
     > balance:             18.652191792
     > gas used:            2329966
     > gas price:           10 gwei
     > value sent:          0 ETH
     > total cost:          0.02329966 ETH
  ```

  

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

To install the software, you need to doownload the following:

1. Install [Node.js](https://nodejs.org/en/) on your computer.
2. Clone or download the repository to your local computer.
3. Open the terminal and install the packages: `npm install`

If you want deploy the smart contract to Rinkeby network, you need to the following:

1. The Metamask's backup phrase is required.
2. [Infura](https://infura.io/) Project ID

### Installing

The procedure to obtain development environment:

```
npm install --save truffle-hdwallet-provider
npm install --save openzeppelin-solidity
```

Run the truffle develope. *Truffle Develop started at http://127.0.0.1:9545/*

And You can get Accounts and Private Keys.

```
truffle develope
```

Type compile on truffle(develope) console. This compiles the smart contract.

```
compile
```

Deploy the smart contract on the your private network.

```
migrate --reset
```

To run the front-end of the Dapp, You have to type following command on New Terminal.

```
cd app
```

Start the webpack-dev-server  *Project is running at http://localhost:8080/*

```
npm run dev
```

Open that url in your browser to access the front-end of the Dapp.



### Deploy the Smart Contract to Rinkeby Network

If you want deploy the smart contract to Rinkeby network, you need to the following:

* You have to type your infura Project ID to `const infuraKey = {Infura POJECT ID}` in truffle-config.js file.
* Type Metamask's backup phrase to `const mnemonic = {METAMASK SEED}` in truffle-config.js file.
* Type `truffle migrate —reset —network rinkeby` on the terminal.



## Running the tests

Explain how to run the automated tests for this system.

* You can run the unit test smart contract by `test` command on truffle console.

```
truffle(develop)> test
Using network 'develop'.


Compiling your contracts...
===========================
> Everything is up to date, there is nothing to compile.



  ✓ can Create a Star (107ms)
  ✓ lets user1 put up their star for sale (145ms)
  ✓ lets user1 get the funds after the sale (202ms)
  ✓ lets user2 buy a star, if it is put up for sale (202ms)
  ✓ lets user2 buy a star and decreases its balance in ether (146ms)
  ✓ can add the star name and star symbol properly (87ms)
  ✓ lets 2 users exchange stars (179ms)
  ✓ lets a user transfer a star (122ms)
  ✓ lookUptokenIdToStarInfo test (74ms)

  9 passing (1s)
```



## Built With

* [Node.js](https://nodejs.org/en/) - The JavaScript used.
* [Truffle](https://truffleframework.com/) v5.0.26 - A development framework for Ethereum.
* [openzeppelin-solidity]() v2.1.2 - Library for secure smart contract development.

## Authors

* **Mingu Kang** - [Github](https://github.com/minqukanq)
