# DegenToken 

## Overview

This repository contains Ethereum smart contracts for the DegenToken (DTK) and GroceryContract. DegenToken is an ERC-20 token that provides functionalities for creating and redeeming grocery contracts. GroceryContract is a simple contract that represents a grocery with a specified charge.

## Contracts

### DegenToken

DegenToken is an ERC-20 token with additional functionalities to interact with GroceryContracts. It includes the following features:

- **Token Name:** DegenToken
- **Symbol:** DTK

#### Constructor

- `constructor()`: Initializes the DegenToken with the name "DegenToken" and symbol "DTK".

#### Functions

1. **createGrocery**

   - `createGrocery(string memory groceryName, uint256 charge) external onlyOwner`: Allows the owner to create a new GroceryContract with a specified name and charge.

2. **redeemGrocery**

   - `redeemGrocery(string memory groceryName) external payable`: Allows users to redeem a grocery by providing the grocery name and required payment. Tokens are burned from the user, and the payment is transferred to the contract owner.

3. **transferTokens**

   - `transferTokens(address redeemer, uint256 total) external`: Allows the owner to transfer tokens to a specified address.

4. **mint**

   - `mint(address to, uint256 total) external onlyOwner`: Allows the owner to mint new tokens and send them to a specified address.

5. **burn**

   - `burn(uint256 total) external`: Allows users to burn their own tokens, reducing the total supply.

### GroceryContract

GroceryContract is a simple contract representing a grocery with a specified charge.

#### Constructor

- `constructor(uint256 _charge)`: Initializes the grocery contract with the specified charge.

## Getting Started

1. Deploy the DegenToken contract.
2. Create grocery contracts using the `createGrocery` function.
3. Users can redeem groceries using the `redeemGrocery` function, burning tokens and transferring payment to the contract owner.
4. Token transfers, minting, and burning can be performed using the corresponding functions.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
