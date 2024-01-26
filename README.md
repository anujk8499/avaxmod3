# MyToken Smart Contract

This repository contains the source code for the MyToken (MYT) ERC-20 token smart contract. MyToken is built on the Ethereum blockchain using the Solidity programming language. The smart contract includes features such as minting, burning, and ownership management.

## Features

1. **Token Standard:** MyToken complies with the ERC-20 token standard, providing interoperability with various decentralized applications (DApps) and platforms.

2. **Burnable:** Token holders can burn (destroy) their own tokens, reducing the total supply.

3. **Minting:** The owner has the exclusive ability to mint new tokens and distribute them to specified addresses.

4. **Ownership:** The smart contract inherits from the Ownable contract, ensuring that ownership of the contract is securely managed.

## Getting Started

To deploy and interact with the MyToken smart contract, follow these steps:

1. **Prerequisites:**
    - Install [Node.js](https://nodejs.org/) and [npm](https://www.npmjs.com/).
    - Install [Hardhat](https://hardhat.org/) for local development and testing.
    - Install dependencies using `npm install`.

2. **Deployment:**
    - Deploy the smart contract to the Ethereum network using Hardhat.
    ```bash
    npx hardhat run scripts/deploy.js --network <network-name>
    ```

3. **Interacting with the Contract:**
    - Utilize Ethereum wallets or web3 libraries to interact with the deployed MyToken smart contract.
    - Use the provided functions such as `transfer`, `mint`, and `burn` based on your requirements.

## Smart Contract Details

- **Name:** MyToken
- **Symbol:** MYT
- **Decimals:** 18
- **Initial Supply:** 100 MYT
- **Owner:** The address specified during contract deployment

## Examples

### Minting

```solidity
// Mint 100 MYT to a specified address
myToken.mint(addressToMint, 100 * 10 ** myToken.decimals());
```

### Burning

```solidity
// Burn 50 MYT from the sender's balance
myToken.burn(50 * 10 ** myToken.decimals());
```

### Transferring

```solidity
// Transfer 20 MYT to another address
myToken.transfer(recipientAddress, 20 * 10 ** myToken.decimals());
```

