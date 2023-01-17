# NFT-Collection

## Details


## Getting Started

### Prerequisites
Have Node.js installed on your computer. This project was developed using Node.js v18.7.0.

Have the Whitelist contract deployed on the network you want to use. See the [Whitelist contract]() for more details.

Set up a goerli endpoint on Quicknode. See the [Quicknode documentation](https://www.quicknode.com/guides/ethereum/quicknode-ethereum-rpc-endpoints/) for more details. Of course, you can use any other Ethereum endpoint instead.
### Installing Dependencies for the Blockchain part

```bash
npm init --yes
npm install --save-dev hardhat
npx hardhat 
```
Select JavaScript as the language and choose the default options for the rest.

```bash
npm install @openzeppelin/contracts
npm install dotenv

```
Add private key and quicknode endpoint to .env file. See the [.env-example file](hardhat-tutorial/.env-example) for more details.
Run:
```bash
npx hardhat compile
npx hardhat run scripts/deploy.js --network goerli
```

