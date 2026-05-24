# Solana ZK Compression Token

In 2026, managing state-rent costs on Solana is a crucial consideration for large-scale enterprise deployments. **ZK Compression**, developed by Light Protocol in partnership with Helius, reduces the cost of storing on-chain accounts, tokens, and PDAs by up to 99%. 

Instead of traditional uncompressed accounts, data is stored off-chain inside ledger logs, while a rolling cryptographic state root remains on-chain inside a secure Merkle tree checked via Zero-Knowledge validity proofs.

## Features
- **Cost Reduction:** Generates compressed token accounts up to 5000x cheaper than native SPL Token accounts.
- **Photon API Integration:** Ready-to-use RPC interactions configured to interact with the Helius Photon ZK indexer.
- **Two-way Composability:** Complete architecture enabling smooth packing and unpacking between compressed and standard SPL state.
- **Flat Layout:** Everything needed for script execution and smart contract interaction is contained inside the root directory.

## Getting Started
1. Install client dependencies: `npm install`
2. Set up your Helius RPC endpoints and base58 secret key credentials within `.env`.
3. Execute the minting script: `node mintCompressed.js`

## Tech Stack
- TypeScript / Node.js
- @solana/web3.js
- @lightprotocol/zk-compression-pkgs (Light Token API equivalents)
- Helius Photon Indexer RPC
