# Futuresmeme

**Futuresmeme** is a 5,000-piece collection of 2D pixel-art robots from the future, each carrying its own agent identity. Every image is generated and stored **100% on-chain** as SVG (no IPFS, no external image files).

- **Network:** BNB Smart Chain (BSC), tested on BSC Testnet first
- **Max supply:** 5,000 (token IDs 1 to 5000)
- **Mint gate:** only wallets that hold a SPACE ID **Agent ID** (`.ai`) can mint. The contract checks `balanceOf(msg.sender) > 0` on the Agent ID registry `0x60B9262456dE011F7d15a54CdD8c48bAaa8B022F` (BSC mainnet).
- **Public page:** static GitHub Pages site in [`docs/`](docs/), no backend and no wallet connect.

> Status: in development. Contract addresses will be listed here after deployment.

## Repository layout

| Path | What it holds |
| --- | --- |
| `contracts/` | Solidity ^0.8.24 contracts (OpenZeppelin ERC721 + Ownable + ReentrancyGuard) |
| `test/` | Foundry tests |
| `script/` | Deploy scripts (testnet and mainnet), configured through environment variables |
| `art/` | Human-readable pixel-art sources for every trait |
| `tools/` | Generators (art source to compact on-chain bytes) |
| `docs/` | GitHub Pages site (`index.html`, `llms.txt`) |

## Security

No private key or seed phrase is ever stored in this repository. `.env` files are git-ignored. Mainnet deployment is done from the owner's Binance Agentic Wallet with explicit confirmation.

## License

MIT
