# Token Contract 

## Overview

This Solidity smart contract, named "Token," is designed to manage a custom ERC-20 token called "Degen" (symbol: DGN). The contract includes functionality for minting, burning, transferring tokens, and redeeming apparel items using the tokens. Additionally, the contract allows the owner to update the fees associated with different types of apparel.

## Contract Features

### ERC-20 Token Standard

The contract implements the ERC-20 standard for fungible tokens, providing basic functionalities like transfer, mint, and burn.

### Ownable

The contract uses the Ownable pattern, ensuring that only the contract owner can execute certain privileged functions, such as minting new tokens and updating apparel fees.

### ERC-20 Burnable

This contract extends the ERC-20 Burnable extension from the OpenZeppelin library, allowing token holders to burn their own tokens.

### Apparel Redemption

The contract introduces a feature to redeem various types of apparel (e.g., Shirt, Jeans, Sneakers) using the tokens. Each type of apparel has a specific fee and inventory associated with it. Users can burn tokens to acquire apparel, subject to availability.

### Events

The contract emits the `LogMessage` event to provide feedback on successful token burns, apparel redemptions, and updates to apparel fees.

## Functions

1. **mintTokens(address account, uint256 span)**
   - Only callable by the owner.
   - Mints a specified number of tokens and assigns them to the specified account.

2. **burnTokens(uint256 span)**
   - Allows token holders to burn a specified number of their own tokens.

3. **transferTokens(address recipient, uint256 span)**
   - Allows token holders to transfer tokens to another address.

4. **redeemApparel(string memory apparelType, uint256 numUnits)**
   - Allows users to redeem apparel by burning the required tokens.
   - Checks the availability of the chosen apparel and deducts the inventory accordingly.

5. **updateApparelFee(string memory apparelType, uint256 newFee)**
   - Only callable by the owner.
   - Updates the fee associated with a specific type of apparel.

## Usage

1. **Deploying the Contract**
   - Deploy the contract to the Ethereum network.

2. **Minting Tokens**
   - Use the `mintTokens` function to mint tokens for specific accounts.

3. **Burning Tokens**
   - Token holders can burn their own tokens using the `burnTokens` function.

4. **Transferring Tokens**
   - Token holders can transfer tokens to other addresses using the `transferTokens` function.

5. **Redeeming Apparel**
   - Users can redeem apparel by calling the `redeemApparel` function, specifying the type of apparel and the desired quantity.

6. **Updating Apparel Fees**
   - Only the owner can update the fees associated with different types of apparel using the `updateApparelFee` function.

## Author 

ankushsingharoy6@gmail.com
