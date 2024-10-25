# Merkle Airdrop

## Overview

**Merkle Airdrop** is a decentralized application (dApp) that allows users to efficiently claim their allocated tokens by verifying their eligibility using a Merkle proof and cryptographic signature validation. The use of Merkle trees ensures gas-efficient and secure token distribution to eligible claimers without requiring large amounts of on-chain data.

### Key Features:
- **Merkle Tree Validation**: Utilizes a Merkle tree to verify users' eligibility with minimal on-chain data, ensuring cost-effective and secure claims.
- **Token Claims**: Allows users to claim their allocated tokens based on cryptographic proofs and signatures.
- **Signature Validation**: Implements EIP-712 signature validation for additional security.
- **Optimized for Efficiency**: Reduces gas costs and on-chain storage through cryptographic proof mechanisms.

## Tech Stack

- **Smart Contract**: Solidity
- **Testing Framework**: Foundry
- **Libraries**: OpenZeppelin Contracts (for ERC20, SafeERC20, and MerkleProof)

## Contracts

### BagelToken (ERC20)
The `BagelToken` contract is an ERC20 token implementation that acts as the airdrop token in this project. It includes minting capabilities, restricted to the contract owner.

### MerkleAirdrop

The `MerkleAirdrop` contract is responsible for managing the airdrop functionality, including:
- **Claim Verification**: Verifies users’ eligibility using a combination of Merkle proofs and EIP-712 signatures.
- **Token Distribution**: Transfers tokens to users upon successful verification.
- **Data Integrity**: Maintains a Merkle root for verifying the integrity of the claim process.


## Getting Started

### Prerequisites
- **Foundry**: A fast, portable Ethereum development toolkit.

### Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/viktor81562/Airdrop-MerkleTree.git
   cd Airdrop-MerkleTree

2. **Install dependencies**
   ```bash
   forge install

3. **Compile**
   ```bash
   forge build

3. **Run Tests**
   ```bash
   forge test

4. **Deployment**
   ```bash
   forge script script/DeployMerkleAirdrop.s.sol

4. **Generating Merkle Proofs**
   ```bash
   forge script script/GenerateInput.s.sol
   forge script script/Merkle.s.sol
   forge script script/ClaimAirdrop.s.sol
