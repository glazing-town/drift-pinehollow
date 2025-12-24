# Drift Pinehollow — Architecture Notes

Design notes covering Base alignment and read-only constraints.

---

## Base Alignment

Drift Pinehollow is Base-first:

- Supported networks: **Base Mainnet** and **Base Sepolia**
- Public RPC endpoints and explorer URLs are treated as configuration
- Explorer links should always resolve to BaseScan (mainnet or sepolia)

Network metadata should be loaded from a config file (e.g. `config/base.networks.json`)
and must not be duplicated across code.

---

## Read-only Constraints

This project is intentionally constrained to **read-only operations**:

Allowed:
- ETH balance checks
- Contract code presence checks
- Block number / chain metadata reads
- Token metadata reads (symbol/decimals) if needed

Not allowed in the core scope:
- Sending transactions
- Signing messages as a required step
- Managing private keys
- Mutating onchain state

These constraints keep validation deterministic and reduce operational risk.

---

## Dependency Choices

Guidelines:
- Prefer Base ecosystem packages where applicable
- Keep the set minimal and easy to remove
- Avoid overlapping libraries that solve the same job
- Treat network config as data, not logic

---

_Last updated: initial scaffold_
