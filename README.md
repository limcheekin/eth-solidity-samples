# Ethereum dApps Next.js Boiletplate [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

<p>
  <img alt="made for ethereum" src="https://img.shields.io/badge/made_for-ethereum-771ea5.svg">
  <img alt="to the moon" src="https://img.shields.io/badge/to_the-moon-fab127.svg">
  <img alt="MIT license" src="https://img.shields.io/badge/license-MIT-blue.svg">
</p>

The project contains samples of Ethereum Smart Contract in Solidity.

## Smart Contract Development
The project is bootstrapped with [Truffle](https://www.trufflesuite.com/truffle) using `truffle init` command.

Steps to run the smart contracts locally:
1. Clone the github repository. This also takes care of installing the necessary dependencies.
    ```bash
    git clone git@github.com:limcheekin/eth-solidity-samples.git
    ```

2. Install Truffle globally.
    ```bash
    npm install -g truffle
    ```

3. Run the development console in the eth-solidity-samples directory.
    ```bash
    truffle develop
    ```

4. Compile and migrate the smart contracts. Note inside the development console we don't preface commands with `truffle`.
    ```bash
    compile
    migrate
    ```

5. Truffle can run tests written in Solidity or JavaScript against your smart contracts. Note the command varies slightly if you're in or outside of the development console.
    ```bash
    // If inside the development console.
    test

    // If outside the development console.
    truffle test
    ```
6. Run with MetaMask
    
    As `truffle develop` exposes the blockchain onto port `9545`, you'll need to add a Custom RPC network of `http://localhost:9545` in your MetaMask to make it work.

7. Deploy smart contract to Rinkeby testnet
    - Install dependencies in the root directory.
        ```bash
        npm i
        # or
        yarn
        ```
    - Create a `.env` file with Infura Project ID and private key of your Rinkeby account, for example:
        ```
        INFURA_PROJECT_ID=b874a2f145f84dc5a8466e5490816789
        RINKEBY_PRIVATE_KEY=e0adc9a1b4818153aa47fee3f5160179bbb4f14157a971c133c22e2e35f88c9e
        ```
    - Run the `truffle migrate --network rinkeby` command to deploy smart contract to Rinkeby network.

## Continuous Integration
The repository setup Continuous Integration build pipeline with GitHub Actions. Please refer to [Continuous Integration Setup](doc/ContinuousIntegrationSetup.md) for more information.