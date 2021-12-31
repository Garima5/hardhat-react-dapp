# Basic Sample Hardhat Project

This project demonstrates a basic Hardhat use case. It comes with a sample contract, a test for that contract, a sample script that deploys that contract, and an example of a task implementation, which simply lists the available accounts.

Try running some of the following tasks:

```shell
npx hardhat accounts
npx hardhat compile
npx hardhat clean
npx hardhat test
npx hardhat node
node scripts/sample-script.js
npx hardhat help
```
# Steps to be followed to recreate this project

### Prerquisites: Node, React and Metamask should be installed on the system

### Steps to recreate this project:
1. Create React App
```
Npx create-react-app <name>
```
2. Cd into the folder
3. Install dependencies:
```
Npm install ethers hardhat @nomiclabs/hardhat-waffle ethereum-waffle chai @nomiclabs/hardhat-ethers
```
4. Create a hardhat project 
```
Npx hardhat
```
5. Choose -> Create a simple project. This should create some files to set up our code for Smart contracts
6. Next we need to create an artifacts folder. After compiling, all items are stored in it. Create it’s path in config file: in hardhat.config.js, add the following after solidity:
```
paths:{
    artifacts:'./src/artifacts'
  },
```
7. Next we need to set up Networks - To use Metamask with hardhat, set the chain id in networks. (If we need to test it on Ropsen network - we need to set chain id for that as well)
In hardhat.config.js add
```
networks:{
    hardhat:{
      chainId:1337
    }
  }
```
8. Rename src/sample_script.js to src/deply.js
9. Solidity code goes into the contract directory - Greeter.sol already exists
10. To compile:
```
Npx hardhat compile
```
This compiles Sc into artifacts directory
11. Hardhat gives us a local node to deploy our code. It provides us with a set of accounts which can be viewed as:
```
Npx hardhat node
```
12. To deploy the contract:
```
Npx hardhat run scripts/deploy.js –network localhost
```
13. Connecting to Metamask:
```
Change chain to local host on Metamask
Import one of the accounts from listed accounts
```
14. Connecting front end and react app:
```
Npm start
```
15. In app.js:
Import abi 
```
import Greeter from './artifacts/contracts/Greeter.sol/Greeter.json'
```
Store the address of contract
Write functions in App()
If you write another contract - add it to deploy.js and continue as above 
