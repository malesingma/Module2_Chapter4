
# Maths

This is used to create a frountend and display the working of 2 funtions.


## Description

This is used to create a frountend on the heading "Maths".
This is used to run 2 funtions one to find sum of the multiples from a number(here it is 4 mutiples of 5)and the other one is to check if the number is odd or even.If the number is even then it prints the sum of first 5 even number and if its odd then it prints the sum of first 5 odd numbers(the number given here is 42 so the number is even).

## Requirements

1)Node.js

2)Metamask wallet extension installed in your browser

3)Rinkeby Test Network

4)Ether balance in your Rinkeby wallet


# Starter Next/Hardhat Project

After cloning the github, you will want to do the following to get the code running on your computer.

1. Inside the project directory, in the terminal type: npm i
2. Open two additional terminals in your VS code
3. In the second terminal type: npx hardhat node
4. In the third terminal, type: npx hardhat run --network localhost scripts/deploy.js
5. Back in the first terminal, type npm run dev to launch the front-end.

After this, the project will be running on your localhost. 
Typically at http://localhost:3000/


# Steps to run the codebase 

$ npm install
$ npm start

navigate browser to localhost:3000

-----------------------------
## Tech Stack

React Js
Solidity

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

# Structure of files in the codebase

src Folder -
    Contracts - 
        BankApp.sol - You can view the smartcontract used in this code 
        bank_app_abi.json - The abi file of the smartcontract.

The smart contract is deployed on Test BSC Network.

### Contract Address - 0x59eFE99aA926a79edEA31F7ED3b2661b1F9e2F62

## Flow of smart contract

1.Firstly connect your wallet by clicking on connectwallet button(Make sure you have test BNB in your wallet).
2.You need to create the account by clicking on createAccount  button
3.You can check whether your account is listed in the network by clicking on checkAccountExists Button
4.Next you can deposit the balance into your account by entering the number in the textbox.
5.You can check the balance in the bank account using Account Balance button.
6.You can transfer your funds in the bank account to another bank account(Make sure that account is also listed in the network)
7.You can withdraw funds using Withdraw button.



## In App.js you can find all these functions

connectWalletHandler - For connecting the metamask wallet
AccoutChangedHandler - Chainging account from metamask can cause this function to work
chainChangedHandler - Chainging the chain network in the metamask can cause this function to work
updateEthers - This function helps in communicating with the abi,deployed smart contract and the provider network of the metamask

### `let tempProvider = new ethers.providers.Web3Provider(window.ethereum);`
###	`let tempSigner = tempProvider.getSigner();`
### `let tempContract = new ethers.Contract(contractAddress, simple_token_abi, tempSigner)` - These are the steps for integrating Smartcontract with the Frontend.

createAccount - Creates the Account in the Bank Dapp
checkAccountExists - Checks if the Account is listed in the Dapp
AccountBalance - Checks the balance of the account in the Bank
DepositBalance - For depositing the balance from your metamask wallet account to bank account
WithdrawBalance - For Withdrawing the balance from your bank account to metamask wallet address 
TransferHandler -For transferring the funds between accounts in the bank. Make sure both the banks are listed in the network.

## License

This code is licensed under the [MIT](https://choosealicense.com/licenses/mit/) license.See the LICENSE file for more information.
