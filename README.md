# Inbox Smart Contract Project

## Overview

This project demonstrates a simple smart contract written in Solidity and deployed using Web3.js. The contract, `Inbox`, allows users to store and update a message on the Ethereum blockchain. The project includes testing, deployment, and compilation processes.

## Prerequisites

- **Node.js** (v14 or later recommended)
- **npm** (comes with Node.js)
- **Ganache** (for local Ethereum blockchain testing)
- **Infura** account (for deploying on testnets like Goerli or mainnet)
- **Mnemonic phrase** (for accessing Ethereum accounts)
- **MetaMask** (optional, for account management)

## Project Structure

- **contracts/**: Contains the Solidity contract (`Inbox.sol`).
- **compile.js**: Script for compiling the Solidity contract.
- **deploy.js**: Script for deploying the compiled contract to a blockchain network.
- **test/**: Contains tests for the contract using Mocha.
- **package.json**: Lists project dependencies and scripts.

## Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd inbox-updated
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

## Compilation

To compile the smart contract, run:

```bash
node compile.js
```

This generates the ABI and bytecode required for deployment in the `compile.js` script.

## Deployment

1. Update the deployment script (`deploy.js`) with your **mnemonic phrase** and **Infura URL**:

   ```javascript
   provider = new HDWalletProvider('YOUR_MNEMONIC', 'YOUR_INFURA_URL');
   ```

2. Deploy the contract:

   ```bash
   node deploy.js
   ```

3. Note the deployed contract address printed in the console.

## Testing

To test the contract:

1. Start Ganache:

   ```bash
   ganache-cli
   ```

2. Run the tests:
   ```bash
   npm test
   ```

The tests verify:

- Contract deployment
- Default message functionality
- Ability to update the message

## Project Details

### Contract: Inbox

- **State Variable**:

  - `message`: A `string` to store the message.

- **Constructor**:

  - Sets the initial message during contract deployment.

- **Functions**:
  - `setMessage(string memory newMessage)`: Updates the message.

### Tools and Dependencies

- **Solidity Compiler (solc)**: Used for compiling the contract.
- **Web3.js**: Used for interacting with Ethereum nodes.
- **Ganache**: Provides a local Ethereum blockchain for testing.
- **HDWalletProvider**: Enables account management and signing transactions.
- **Mocha**: JavaScript test framework for contract testing.

### Key Files

- `contracts/Inbox.sol`: The smart contract source code.
- `deploy.js`: Script for deploying the contract.
- `test/Inbox.test.js`: Contains tests for the `Inbox` contract.
- `compile.js`: Script for compiling the contract.

## Dependencies

- `@truffle/hdwallet-provider`
- `ganache`
- `mocha`
- `solc`
- `web3`

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

## Author

Developed by [Your Name].
