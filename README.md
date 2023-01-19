# NFT-Collection

## Details


## Getting Started
You can interact with the deployed testnet app here: https://nft-collection-uo3l.vercel.app/
To mint an NFT your wallet address must be whitelisted - to do this, please visit this Whitelist site that runs on Goerli as well: https://whitelist-dapp-goerli-eight.vercel.app


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
Select an empty hardhat config. JavaScript has been used originally as the language and the default options have been chosen for the rest.
Copy and paste the text from the [hardhat-config-copy.js](./hardhat-config-copy.js) file into the newly generated hardhat.config.js file after deleting its default content.
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

#### Possible errors
If you get the following error:
```bash
Error HH600: HardhatError: HH600: The selected network "goerli" doesn't exist.
```
It means that you haven't set up a goerli endpoint on Quicknode. See the [Quicknode documentation](https://www.quicknode.com/guides/ethereum/quicknode-ethereum-rpc-endpoints/) for more details. Of course, you can use any other Ethereum endpoint instead.

If you get the following error:
```bash
Error: Cannot find module '@nomicfoundation/hardhat-toolbox'
```
Install the missing dependency:
```bash
npm install @nomicfoundation/hardhat-toolbox
```

Error Private Key to long:
```bash
Invalid account: #0 for network: goerli - private key too long, expected 32 bytes
```
Check if you have copied the private key correctly. It should be 64 characters long.
If it's still not working, check if you added a 0x prefix to the private key, either in your .env file or in the hardhat.config.js file.
Also check if you've added a semicolon at the end of the private key in your .env file. If so: remove it.