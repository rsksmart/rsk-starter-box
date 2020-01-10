# RSK Starter Box

## Description

This box comes with everything you need to start using Truffle on RSK Network. It includes network configs for Mainnet and Testnet.

## Installation

First ensure you are in a new and empty directory.

1. Install Truffle globally

    ```
    npm install -g truffle
    ```

2. Run the unbox command. This will install all necessary dependencies.

    ```
    truffle unbox rsksmart/rsk-starter-box
    ```

3. Run the development console.

    ```
    truffle develop
    ```

4. Compile and migrate the smart contracts. Note inside the development console we don't preface commands with truffle.

    ```
    compile
    migrate
    ```

**NOTE**: This box is not a complete dapp.

##RSK

### Setup an account & Get RBTC

To get an address please go [here](https://developers.rsk.co/rsk/architecture/account-based/).
If you are in RSK Testnet you can get tRBTC from our [Faucet](https://faucet.testnet.rsk.co/). For RSK Mainnet go [here](https://www.rsk.co/#exchanges-rsk).

### Setup the gas price
You should check the gas price that you have to use in order send a transactions for any RSK Network. RSK has the property minimum gas price, which tells the minimum gas price that you have to use to pay for a transaction.

To get the stats for Mainnet go [here](https://stats.rsk.co/) and Testnet go [here](https://stats.testnet.rsk.co/)

### Connect to RSK

1. Copy your mnemonic to `truffle-config.js`

    ```
    // truffle-config.json

    const HDWalletProvider = require('@truffle/hdwallet-provider');

    //Put your mnemonic here, take care of this and don't deploy your mnemonic into production!
    const mnemonic = 'A_MNEMONIC';
    ```

2. Check the gas price of the network and update it if it is necessary in `truffle-config.js`


3. Run the development console for any RSK network.

    ```
    # Console for Mainnet
    truffle console --network mainnet

    # Console forn Testnet
    truffle console --network testnet
    ```

4. Compile and migrate the smart contracts. Note inside the development console we don't preface commands with truffle.

    ```
    compile
    migrate
    ```