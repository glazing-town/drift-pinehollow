# Drift Pinehollow (Built for Base)

Drift Pinehollow is a browser-first Base inspection tool designed for developers who need quick confirmation of Base network health and public onchain state without performing transactions.

## Network coverage

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

## Repository layout

- app/drift-pinehollow.ts  
  Browser script that connects a Coinbase Wallet and performs read-only Base RPC queries.

- docs/architecture.md  
  Design notes covering Base alignment and read-only constraints.

- docs/validation-log.md  
  Sequential notes recorded during Base Sepolia testnet validation.

- scripts/sample-addresses.json  
  Example addresses used for repeatable inspection.

- contracts/  
  Solidity contracts deployed to Base Sepolia for testnet validation:
  - contract.sol — minimal deployment verification contract  
  - imports.sol — simple stateful interaction contract  

- package.json  
  Dependency manifest referencing Base and Coinbase repositories.

- README.md  
  Primary technical documentation.

## Functional overview

This tool allows you to:
- Connect a Coinbase Wallet via EIP-1193  
- Validate Base chainIds (8453 / 84532)  
- Inspect ETH balances and transaction counts  
- Review recent block activity  
- Follow Basescan links for verification  

All functionality is strictly read-only.

## Dependency overview

Drift Pinehollow integrates official tooling:
- Coinbase Wallet SDK for wallet access  
- OnchainKit references for Base-aligned primitives  
- viem for typed, efficient RPC reads  
- Multiple Base and Coinbase GitHub repositories  

## License

MIT License

Copyright (c) 2025 YOUR_NAME

## Author socials:

GitHub: https://github.com/glazing-town 

Email: glazing.town-09@icloud.com 

x: https://x.com/ManalZayer  

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract imports.sol address:  
0x80C0Fa60DB2d1306702Ce2A4A80Dc4EA5C7245f6

Deployment and verification:
- https://sepolia.basescan.org/address/0x80C0Fa60DB2d1306702Ce2A4A80Dc4EA5C7245f6
- https://sepolia.basescan.org/0x80C0Fa60DB2d1306702Ce2A4A80Dc4EA5C7245f6/0#code  

Contract contract.sol address:  
0x5c5CAb5cd6b23d9C687474a3a8dFa6872AbA87C0

Deployment and verification:
- https://sepolia.basescan.org/address/0x5c5CAb5cd6b23d9C687474a3a8dFa6872AbA87C0
- https://sepolia.basescan.org/0x5c5CAb5cd6b23d9C687474a3a8dFa6872AbA87C0/0#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
