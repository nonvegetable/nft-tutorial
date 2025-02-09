# NFTee Smart Contract

A simple ERC721 NFT (Non-Fungible Token) smart contract built using Solidity and Foundry. This contract mints a single NFT to the deployer's address upon deployment.

## Description

NFTee is a basic implementation of the ERC721 standard using OpenZeppelin contracts. The contract creates an NFT collection with the name "NFTee" and symbol "ITM". Upon deployment, it automatically mints token ID #1 to the deployer's address.

## Prerequisites

- [Foundry](https://book.getfoundry.sh/getting-started/installation)
- [Node.js](https://nodejs.org/)
- A Sepolia testnet RPC URL (e.g., from QuickNode)
- A wallet private key with some Sepolia ETH

## Installation

1. Clone the repository:
```bash
git clone github.com:nonvegetable/nft-tutorial.git
cd foundry-app
```

2. Install dependencies:
```bash
forge install
```

3. Create a `.env` file in the root directory with the following variables:
```
QUICKNODE_RPC_URL="your-rpc-url"
PRIVATE_KEY="your-private-key"
```

## Deployment

To deploy the contract to Sepolia testnet:

```
# Set environment variables in PowerShell
$env:QUICKNODE_RPC_URL="your-rpc-url"
$env:PRIVATE_KEY="your-private-key"

# Deploy the contract
forge create --rpc-url $env:QUICKNODE_RPC_URL --private-key $env:PRIVATE_KEY src/NFTee.sol:NFTee --broadcast
```

## Contract Details

- Name: NFTee
- Symbol: ITM
- Standard: ERC721
- Features: 
  - Automatic minting of token #1 to deployer
  - Standard ERC721 functionality (transfer, approve, etc.)

## Security

- The `.env` file is included in `.gitignore` to prevent sensitive data from being committed
- Never share or commit your private keys
- This is a basic implementation for learning purposes
```
