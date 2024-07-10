# ETH-AVAX

# MyToken Smart Contract

## Overview

This project involves creating a simple ERC-20-like token contract on the Ethereum blockchain. The smart contract will manage a token with public variables for token details, a mapping to track balances, and functions to mint and burn tokens.

## Requirements

1. **Public Variables**
   - Token Name
   - Token Abbreviation
   - Total Supply

2. **Mapping**
   - A mapping of addresses to balances (`address => uint`)

3. **Mint Function**
   - Takes an address and a value as parameters.
   - Increases the total supply by the given value.
   - Increases the balance of the specified address by the given value.

4. **Burn Function**
   - Takes an address and a value as parameters.
   - Decreases the total supply by the given value.
   - Decreases the balance of the specified address by the given value.
   - Ensures that the balance of the specified address is greater than or equal to the value to be burned.

## Contract Details

### Public Variables

- **Token Name**: Name of the token.
- **Token Abbreviation**: Abbreviation of the token.
- **Total Supply**: Total supply of the token.

### Mapping

- **Balances**: A mapping of addresses to their token balances.

### Functions

1. **mintFunc(address address_, uint value)**
   - Increases the total supply by the specified value.
   - Increases the balance of the specified address by the specified value.

2. **burnFunc(address address_, uint value)**
   - Decreases the total supply by the specified value.
   - Decreases the balance of the specified address by the specified value.
   - Ensures the balance of the specified address is greater than or equal to the value to be burned.

