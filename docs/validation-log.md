# Drift Pinehollow — Validation Log

Sequential notes recorded during Base Sepolia testnet validation.

---

## 2025-12-24 — Sepolia Validation Pass #1

**Network:** Base Sepolia  
**Chain ID:** 84532  
**RPC:** https://sepolia.base.org  
**Explorer:** https://sepolia.basescan.org

### Step 1 — Sanity checks
- [ ] Confirm network config includes Base Sepolia (84532)
- [ ] Confirm explorer URL resolves to Sepolia BaseScan
- [ ] Confirm app/network selector uses config, not hardcoded values

### Step 2 — RPC connectivity
- [ ] Fetch latest block number
- [ ] Re-fetch after a short pause; ensure it can advance
- [ ] If RPC is flaky, switch to fallback and repeat

### Step 3 — Read-only probes
Using `scripts/sample-addresses.json`:
- [ ] Read ETH balance for `exampleEOA`
- [ ] Read contract code for `exampleContract`
- [ ] Validate zero address handling (no crashes)
- [ ] Validate burn address handling (no crashes)

### Step 4 — Explorer verification
- [ ] Open `exampleEOA` in Sepolia BaseScan
- [ ] Open latest block in Sepolia BaseScan
- [ ] Confirm no mainnet links appear during Sepolia runs

### Notes
- Treat chainId/RPC/explorer changes as **high-risk**
- Prefer fixing config over adding conditional logic

---
