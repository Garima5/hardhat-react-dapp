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
     Create React App
Npx create-react-app <name>
     Cd into the folder
nstall dependencies:
Npm install ethers hardhat @nomiclabs/hardhat-waffle ethereum-waffle chai @nomiclabs/hardhat-ethers
  Npx hardhat
After compiling, all items are stored in a folder called artifacts - hence create it’s path in config file
Set up Networks - To use Metamask with hardhat, set the chain id in networks - localhost. If we need to test it on Ropsen network - we need to set chain id for that as well
Solidity code goes into the contract directory - Greeter.sol already exists
To compile:
Npx hardhat compile - This compiles Sc into artifacts directory
Hardhat gives us a local node to deploy our code. It provides us with a set of accounts which can be viewed as:
Npx hardhat node
To deploy the contract:
Npx hardhat run scripts/deploy.js –network localhost
Connecting to Metamask:
Change chain to local host
Import one of the accounts from listed accounts
Connecting front end and react app:
Npm start
In app.js:
Import abi
Store the address of contract
Write functions in App()
If you write another contract - add it to deploy.js and continue as above 
