# Bank DApp: ETH + AVAX: Module-2

Simple contract with 2-3 functions. Then show the values of those functions in frontend of the application.


## Getting Started

### Executing program
# Steps to run the codebase 

$ npm install
$ npm start

navigate browser to localhost:3000

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
        BankApp.sol - You can view the smart contract used in this code 
        bank_app_abi.json - The ABI file of the smart contract.

The smart contract is deployed on Test BSC Network.

### Contract Address -0x5FbDB2315678afecb367f032d93F642f64180aa3

## Flow of the smart contract

1. Firstly connect your wallet by clicking on the "Connect Wallet" button (Make sure you have test BNB in your wallet).
2. You need to create an account by clicking on the "Create Account" button.
3. You can check whether your account is listed on the network by clicking on the "Check Account Exists" button.
4. Next, you can deposit the balance into your account by entering the number in the textbox.
5. You can check the balance in the bank account using the "Account Balance" button.
6. You can transfer your funds in the bank account to another bank account (Make sure that account is also listed on the network).
7. You can withdraw funds using the "Withdraw" button.

   
## In App.js you can find all these functions

connectWalletHandler - For connecting the MetaMask wallet.
AccoutChangedHandler - Changing the account from MetaMask can trigger this function.
chainChangedHandler - Changing the chain network in MetaMask can trigger this function.
updateEthers - This function helps in communicating with the ABI, deployed smart contract, and the provider network of MetaMask.

```javascript
let tempProvider = new ethers.providers.Web3Provider(window.ethereum);
let tempSigner = tempProvider.getSigner();
let tempContract = new ethers.Contract(contractAddress, simple_token_abi, tempSigner);
```

createAccount - Creates the Account in the Bank DApp.
checkAccountExists - Checks if the Account is listed in the DApp.
AccountBalance - Checks the balance of the account in the Bank.
DepositBalance - For depositing the balance from your MetaMask wallet account to the bank account.
WithdrawBalance - For withdrawing the balance from your bank account to the MetaMask wallet address.
TransferHandler - For transferring the funds between accounts in the bank. Make sure both banks are listed on the network.
--------------------------------------------
## Tech Stack

React Js
Solidity

## Authors

Contributors' name and contact info

- [Gautham]
- [bgautham27@gmail.com]

## License

This project is licensed under the MIT License
-----------------------------


