# Eth-avax-module-3

# ERC20 Token Contract

The MyToken contract is an ERC-20 token implementation with additional features built on the Ethereum blockchain using Solidity. It utilizes the OpenZeppelin library to inherit functionality from the ERC20 and Ownable contracts, providing a secure and standardized token implementation.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Usage

The contract provides an interface (`IERC20`) and an implementation (`ERC20`) for an ERC20 token. 

### Prerequisites

- Solidity compiler version: ^0.8.0


## Overview

The MyToken contract represents a fungible token, compliant with the ERC-20 standard. Each token has a unique name and symbol, making it easily distinguishable and tradable on various decentralized applications (DApps) and exchanges.

## Deployment
To deploy the MyToken contract, you need to provide the following information:

name: A string representing the name of the token (e.g., "My Token").
symbol: A string representing the symbol of the token (e.g., "MTK").
During deployment, the contract creator will receive an initial supply of 0 tokens. The contract owner (deployer) can then mint new tokens and manage the token supply.

### Functions

## mint
The mint function allows the contract owner to create and issue new tokens to a specified account. Only the contract owner has permission to mint new tokens.

function mint(address account, uint256 amount) public onlyOwner
account: The address to which the new tokens will be credited.
amount: The number of tokens to mint and assign to the specified account.


## burn
The burn function enables token holders to destroy their own tokens. By calling this function, tokens are permanently removed from the sender's account.

function burn(uint256 amount) public
amount: The number of tokens to burn.


## transfer
The transfer function allows token holders to send tokens to other addresses.

function transfer(address recipient, uint256 amount) public override returns (bool)
recipient: The address to which the tokens will be transferred.
amount: The number of tokens to transfer.


## transferFrom
The transferFrom function allows approved spenders to transfer tokens on behalf of token holders. This function is typically used when interacting with other contracts that require spending tokens on behalf of their users.

function transferFrom(address sender, address recipient, uint256 amount) public override returns (bool)
sender: The address from which the tokens will be transferred.
recipient: The address to which the tokens will be transferred.
amount: The number of tokens to transfer.
Additional Information
The decimals function has been overridden to return a constant value of 0. This means that the token has 0 decimal places, and the smallest unit of the token is 1.

The MyToken contract inherits from the ERC20 and Ownable contracts from the OpenZeppelin library, providing additional functionalities such as balance tracking, allowance management, and owner-specific functions.

## Disclaimer

This contract is provided as-is without any warranties or guarantees. Use at your own risk.

