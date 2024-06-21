# MyToken Project
## Overview
The MyToken project is a simple Solidity smart contract that demonstrates the creation and management of a basic ERC20-like token. This project aims to help developers understand the fundamental concepts of token creation, minting, and burning within the Ethereum blockchain ecosystem.

## Description
MyToken is a smart contract written in Solidity, designed to introduce users to basic token operations on the Ethereum blockchain. The contract includes functionalities to mint new tokens, burn existing tokens, and track balances. The project provides a straightforward entry point for those new to Solidity and Ethereum smart contracts, allowing them to grasp the essentials before moving on to more complex implementations.

## Getting Started
### Installing
To run the MyToken contract, you'll need to use Remix, an online Solidity IDE. Follow these steps to get started:

1. Open your web browser and go to Remix website at https://remix.ethereum.org/.
2. Create a new file by clicking the "+" icon in the left-hand sidebar.
3. Save the file with a .sol extension (e.g., MyToken.sol).
4. Copy and paste the following code into the file:

'solidity'

       // SPDX-License-Identifier: MIT
       pragma solidity 0.8.18;

       contract MyToken {
       // Public variables to store token details
       string public tokenName = "MyToken";
       string public tokenAbbrv = "MTK";
       uint256 public totalSupply;

       // Mapping to store balances
       mapping(address => uint256) public balances;

       // Mint function to create new tokens
       function mint(address _to, uint256 _value) public {
        totalSupply += _value;
        balances[_to] += _value;
       }

       // Burn function to destroy tokens
       function burn(address _from, uint256 _value) public {
        require(balances[_from] >= _value, "Insufficient balance to burn");
        totalSupply -= _value;
        balances[_from] -= _value;
       }
       }



   

### Executing Program
To compile and deploy the MyToken contract:

1. Click on the "Solidity Compiler" tab in the left-hand sidebar.
2. Ensure the "Compiler" version is set to 0.8.18 (or a compatible version).
3. Click the "Compile MyToken.sol" button.
4. After successful compilation, click on the "Deploy & Run Transactions" tab in the left-hand sidebar.
5. Select the MyToken contract from the dropdown menu.
6. Click the "Deploy" button to deploy the contract.


Once deployed, you can interact with the contract by calling its functions:

+ Minting Tokens

  + Enter the recipient address and the number of tokens to mint.
  + Call the mint function to create new tokens.
+ Burning Tokens

  + Enter the address from which tokens should be burned and the number of tokens to burn.
  + Call the burn function to destroy the specified amount of tokens.
## Help
If you encounter any issues, consider the following tips:

+ Ensure that the Solidity version in Remix matches the pragma statement in your code.
+ Verify that you have sufficient permissions to execute mint and burn functions.
+ Check the balances and totalSupply variables to ensure correct token operations.
+ For additional help, you can use the following command to get more information about the contract functions:

 'solidity'

    // Not applicable in this context, but you can use Remix's built-in debugger and console for troubleshooting.


## Authors
Ambesh Dubey

## License
This project is licensed under the MIT License - see the js-assigment.md file for details.














