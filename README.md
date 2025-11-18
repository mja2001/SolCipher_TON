# SolCipher_TON
"A TON-based port of SolCipher: Privacy-first dApp for secure, encrypted document sharing. Uses client-side AES-256-GCM encryption, TON smart contracts for access control, IPFS/TON Storage, and wallet-based permissions with expiry/revocation."
# SolCipher_TON: Secure Document Sharing on TON

[![TON](https://img.shields.io/badge/Built%20for-TON-blue)](https://ton.org/) [![Hackathon](https://img.shields.io/badge/The%20Open%20Hack-2025-green)](https://dorahacks.io/hackathon/theopenhack2025)

## Overview
This is a port of the original [SolCipher](https://github.com/mja2001/SolCipher) from Solana to TON (The Open Network). It enables privacy-focused sharing of encrypted documents between TON wallets. Key features:
- Client-side encryption (AES-256-GCM) with keys derived from wallet signatures.
- Decentralized storage via IPFS or TON Storage.
- On-chain access control using TON smart contracts (built with Tact).
- Set expiry dates, revoke access, and support batch uploads.
- Consumer-friendly UI for uploading, sharing, and viewing.

Built as a submission for [The Open Hack 2025](https://dorahacks.io/hackathon/theopenhack2025), emphasizing scalable, low-cost dApps on TON.

## Tech Stack
- **Blockchain**: TON (Tact for contracts, TonWeb for interactions).
- **Frontend**: React with @tonconnect/ui-react for wallet integration.
- **Encryption**: CryptoJS (AES-256-GCM).
- **Storage**: Web3.Storage (IPFS) or TON Storage Client.
- **Dependencies**: Node.js, Yarn.

## Setup
1. Clone: `git clone https://github.com/mja2001/SolCipher_TON.git`
2. Install: `yarn install`
3. Env: Copy `.env.example` to `.env` and fill in `WEB3_STORAGE_TOKEN`, `TON_RPC_ENDPOINT`.
4. Run frontend: `yarn dev`
5. Deploy contracts: Use TON CLI or Blueprint – see `/contracts/README.md`.

## Usage
- Connect TON wallet (e.g., Tonkeeper).
- Upload file: Encrypt, store on IPFS, record metadata on TON.
- Share: Specify recipient wallet and expiry.
- View: Authorized users decrypt and download.

## Development
- Contracts: See `contracts/access_control.tact` (example from port guide).
- Tests: `yarn test`

## Hackathon Submission
Submitted via DoraHacks: [Link to BUIDL] (add after submission).
Demo: [Vercel URL] (deploy and add).

## Contributing
Fork and PR! Issues welcome.

License: MIT
