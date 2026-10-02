# How to Verify STER Yourself

This guide shows how to check the STER token, its liquidity pools, the locks, and SDV's wallets using public tools. Nothing here requires connecting a wallet. If any site asks you to connect a wallet or approve a transaction, close it.

Last updated: October 2, 2026.

---

## 🔹 1. Verify the STER Mint

**Mint address:**
`ByzUhVTPHNqy7ZSKtTMq6v5Y4jG91FUmF18NTSeLCK7E`
https://solscan.io/token/ByzUhVTPHNqy7ZSKtTMq6v5Y4jG91FUmF18NTSeLCK7E

On the token page, confirm:

- Symbol: **STER**
- Decimals: **6**
- Supply: **1,844,674,087,559**
- Mint authority: not set (revoked September 20, 2026)
- Freeze authority: not set

With no mint authority, no new STER can be created. With no freeze authority, no holder's STER can be frozen.

---

## 🔹 2. Verify the Metadata

**Metadata URI:**
`https://gateway.irys.xyz/ynN88u3MnIJhWVfJHgUSpPoc-jIUMblsMGvYQk2soik`

The file contains the token name, symbol, description, and image. The on-chain metadata is marked immutable, so these details cannot be changed.

---

## 🔹 3. Verify the Liquidity Pools

**SOL-STER pool:**
`3kbkFHgKcwWrHCFYt1rXeY81YzC23cnHbHxMucBnpvBm`
https://solscan.io/account/3kbkFHgKcwWrHCFYt1rXeY81YzC23cnHbHxMucBnpvBm

**STER-USDC pool:**
`G4BqFYJ3kZe7GKJwNk4eNWrbVYBqz5n6Cs7FWKsKot15`
https://solscan.io/account/G4BqFYJ3kZe7GKJwNk4eNWrbVYBqz5n6Cs7FWKsKot15

On each pool page:

1. Confirm the pooled STER and the pooled SOL or USDC.
2. Find the row labeled **LP Token** and click the link beside it.
3. On the LP token page, click the **Holders** tab.
4. The holders list shows who can withdraw liquidity. Locked LP tokens are held by escrow accounts belonging to Streamflow or Jupiter Lock, not by an ordinary wallet.

---

## 🔹 4. Verify the Liquidity Locks

**Streamflow locks:**

- SOL-STER, unlocks December 20, 2026: https://app.streamflow.finance/contract/solana/mainnet/8G9mtRAR6cikVMbEQJqnYDQrR2yjb7zQUj5MRLGCqC4x
- STER-USDC, unlocks December 20, 2026: https://app.streamflow.finance/contract/solana/mainnet/DMiCqBQtrRRZGj88NSgvTM1GT7a9FjXJ2Y5JLQiin4mt

On each contract page, confirm the status, the amount, and the unlock date.

**Jupiter Lock positions:**

1. Go to https://lock.jup.ag/
2. In the search box, paste the SDV Treasury wallet, `BzF7JYXXJV5Arxhz8sQLeLKbRVu8qMd54jYiKCpV5edK`, to find the STER-USDC lock that unlocks December 20, 2028.
3. Paste the Founders wallet, `ByU6iuYR3rCVtrp1pb9szxTeq6BmSH3pPnhYZ9V7ygMV`, to find the Founders Allocation lock that unlocks November 27, 2028.

The full list of locks is in [lp.md](lp.md) and [treasury.md](treasury.md).

---

## 🔹 5. Verify SDV's Wallets

The five SDV wallet addresses and their balances are listed in [treasury.md](treasury.md). Open each address on Solscan and compare.

---

## 🔹 6. Verify a Transaction

1. Copy the transaction signature.
2. Paste it into the search box at https://solscan.io/
3. Confirm the token, the amount, and the sending and receiving wallets.

Airdrop transactions are listed in [airdrops.md](airdrops.md).

---

## 🔹 Summary

| To check | Look at |
|----------|---------|
| Supply cannot grow | Mint authority on the token page |
| Holders cannot be frozen | Freeze authority on the token page |
| Liquidity cannot be withdrawn early | LP token holders and the lock pages |
| What SDV holds | The five wallets in treasury.md |
