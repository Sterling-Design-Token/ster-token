# How to Verify STER on Solscan

This guide walks you through verifying the STER token, metadata, liquidity pool, and transactions directly on Solscan.  
Everything is fully on‑chain and publicly viewable.

---

## 🔹 1. Verify the STER Mint

**Mint Address:**  
`ByzUhVTPHNqy7ZSKtTMq6v5Y4jG91FUmF18NTSeLCK7E`  
https://solscan.io/token/ByzUhVTPHNqy7ZSKtTMq6v5Y4jG91FUmF18NTSeLCK7E

On the mint page, confirm:

- Token name: **STER**  
- Decimals: **6**  
- Supply: **1.84T**  
- Creator: Verified program  
- Metadata: Matches the URI below  

---

## 🔹 2. Verify Metadata

**Metadata URI:**  
`https://gateway.irys.xyz/ynN88u3MnIJhWVfJHgUSpPoc-jIUMblsMGvYQk2soik`

This file contains:

- Token name  
- Symbol  
- Description  
- Image  
- Attributes  

This ensures the token is authentic and not a spoofed mint.

---

## 🔹 3. Verify the Liquidity Pool

**LP Token Mint:**  
`3kbkFHgKcwWrHCFYt1rXeY81YzC23cnHbHxMucBnpvBm`  
https://solscan.io/account/3kbkFHgKcwWrHCFYt1rXeY81YzC23cnHbHxMucBnpvBm

On this page, confirm:

- LP token supply  
- Holders  
- Pool activity  
- Raydium AMM program involvement  

**Raydium Pool:**  
https://raydium.io/swap/?inputMint=sol&outputMint=ByzUhVTPHNqy7ZSKtTMq6v5Y4jG91FUmF18NTSeLCK7E

---

## 🔹 4. Verify Transactions

To verify any STER transaction:

1. Copy the transaction signature  
2. Paste it into Solscan search  
3. Confirm:
   - Token transfers  
   - Source and destination wallets  
   - Amounts  
   - Program used (Token Program / Raydium AMM)  

For Airdrop #1, all TXIDs are listed here:  
https://github.com/Sterling-Design-Token/ster-token/blob/main/airdrops.md

---

## 🔹 5. Verify the Treasury Wallet

The Treasury wallet is used for ecosystem operations, airdrops, and LP actions.

**Treasury Wallet:**  
https://solscan.io/account/STER-Advisors

Cross‑reference with:  
https://github.com/Sterling-Design-Token/ster-token/blob/main/treasury.md

---

## 🔹 Summary

You can verify STER by checking:

- Mint  
- Metadata  
- LP  
- Transactions  
- Treasury wallet  
- Transparency logs in this repo  

Everything is on‑chain, public, and fully auditable.
