# STER Liquidity Pools and Locks

This page documents STER's two liquidity pools, every lock on the liquidity SDV has provided, and the full history of liquidity actions, including errors and how they were corrected.

Last updated: October 2, 2026.

---

## 🔹 The Two Pools

| | SOL-STER pool | STER-USDC pool |
|---|---|---|
| **Exchange** | Raydium | Raydium |
| **Pool address** | `3kbkFHgKcwWrHCFYt1rXeY81YzC23cnHbHxMucBnpvBm` | `G4BqFYJ3kZe7GKJwNk4eNWrbVYBqz5n6Cs7FWKsKot15` |
| **LP token** | `5uFe5w2HCQSb9XBF6VMbqcM9HVkfCwLbA8LMbNz38PvC` | `3RGPYknxDMpBHkKjnmh66AjCZsNPLXAuvkbtuHE3dYcA` |
| **Pooled assets (October 2, 2026)** | 791,198,623 STER and 22.33 SOL | 809,169,162 STER and 2,790.02 USDC |
| **Liquidity (October 2, 2026)** | About $5,400 | About $5,500 |
| **Solscan** | https://solscan.io/account/3kbkFHgKcwWrHCFYt1rXeY81YzC23cnHbHxMucBnpvBm | https://solscan.io/account/G4BqFYJ3kZe7GKJwNk4eNWrbVYBqz5n6Cs7FWKsKot15 |
| **Live market data** | https://dexscreener.com/solana/3kbkfhgkcwwrhcfyt1rxey81yzc23cnhbhxmucbnpvbm | https://dexscreener.com/solana/g4bqfyj3kze7gkjwnk4enwrbvybqz5n6cs7fwkskot15 |

Each pool issues its own LP token. Whoever holds a pool's LP tokens can withdraw that share of the pool's liquidity. A lock places LP tokens in an escrow account until a set date.

---

## 🔹 Locks on SDV's Liquidity

SDV's liquidity in both pools is locked in four positions.

### SOL-STER pool

| Lock | Platform | Amount | Unlocks | Details |
|------|----------|--------|---------|---------|
| Original lock | Streamflow | 3,058.976512612 LP tokens (73.85%) | December 20, 2026 | Immutable. Cannot be canceled. [View contract](https://app.streamflow.finance/contract/solana/mainnet/8G9mtRAR6cikVMbEQJqnYDQrR2yjb7zQUj5MRLGCqC4x) |
| Second lock | Streamflow | 1,077.540742669 LP tokens (26.02%) | July 18, 2028 | Cannot be canceled or transferred. Recipient: SDV Treasury wallet. [View contract](https://app.streamflow.finance/contract/solana/mainnet/FxGfzfe3WC9Qfd1ixNcyKy2ZLmw6EYQqUHDdYS99qodh) |

As of October 2, 2026, these two locks hold 99.87% of all SOL-STER LP tokens. The remaining 0.13% (5.387703713 LP tokens) is held by Streamflow as its fee on the second lock. Streamflow's public dashboard for this LP token shows the same figure: https://app.streamflow.finance/token-dashboard/solana/mainnet/5uFe5w2HCQSb9XBF6VMbqcM9HVkfCwLbA8LMbNz38PvC

Current holders: https://solscan.io/token/5uFe5w2HCQSb9XBF6VMbqcM9HVkfCwLbA8LMbNz38PvC

### STER-USDC pool

| Lock | Platform | Amount | Unlocks | Details |
|------|----------|--------|---------|---------|
| First lock | Streamflow | 906,099.47 LP tokens (61.1%) | December 20, 2026 | Immutable. Cannot be canceled, but can be transferred. [View contract](https://app.streamflow.finance/contract/solana/mainnet/DMiCqBQtrRRZGj88NSgvTM1GT7a9FjXJ2Y5JLQiin4mt) |
| Second lock | Jupiter Lock | 576,777.654137 LP tokens (38.9%) | December 20, 2028 | Created October 2, 2026. Cannot be canceled. The recipient cannot be changed. Recipient: SDV Treasury wallet. [View lock](https://lock.jup.ag/escrow/DLL28qsmqkvPDhZ3eNKpUcSRq5PSbVx5YWd5wh5nGpYu) |

As of October 2, 2026, these two locks hold all STER-USDC LP tokens except 0.000146 of a token left in the SDV Treasury wallet.

Current holders: https://solscan.io/token/3RGPYknxDMpBHkKjnmh66AjCZsNPLXAuvkbtuHE3dYcA

### What happens on December 20, 2026

Two locks expire on December 20, 2026. SDV intends to claim both positions and relock them for two more years.

---

## 🔹 Correction to an Earlier Version of This Page

An earlier version of this page listed `AvDg7yXhcR15ryRycqJipBdqwchKJ7yirx831KBew1Zz` as the lock contract. That address is not the lock contract. The correct Streamflow contract links are in the tables above.

The earlier version also described only the SOL-STER pool. The STER-USDC pool and its locks are now included.

---

## 🔹 Liquidity History

### Event 1 — Initial LP Creation
- **Date:** November 27, 2025
- **Action:** LP created on Raydium (STER-WSOL)
- **Amount:** ~2,000 STER + 3.52 WSOL
- **Status:** ✅ Completed successfully

---

### Event 2 — Accidental LP Removal (Operational Error)
- **Date:** December 9, 2025
- **Action:** REMOVE LIQUIDITY — accidental
- **Amount:** 1,999.246221 STER + 3.51867335 WSOL
- **Transaction:**
`4cEQrur99eepPgSVySQVoEkCBuv333KrwLxamhEGmFMsPfUFowrk6eKQ8ouaBW9gF23St1eHTAFppnFmd6eVdkdN`
- **Cause:** Operational error by the token issuer — parameters entered in wrong order during a swap attempt. This was not intentional. No user funds were stolen or misappropriated.
- **Duration of outage:** Approximately 12-16 hours (discovered the following morning)
- **Status:** ⚠️ Error — corrected within 24 hours (see Event 3)

The full report is in [INCIDENT-REPORT-DEC9-2025.md](INCIDENT-REPORT-DEC9-2025.md).

---

### Event 3 — LP Fully Restored (Correction)
- **Date:** December 10, 2025
- **Action:** CREATE POOL + ADD LIQUIDITY — intentional correction
- **Amount:** 500,000,000 STER + 3.65 WSOL = approximately $1,011.20 USD
- **Transaction:**
`2kvwjU2qJZy6yGCSbYW9yiHonKe85HgHJ3gpv2iQm86BY2UGe8TXPsLihBfrK7BoCaF8A1iLsgNaBKHEyXN7Kmgs`
- **Note:** Liquidity restored exceeded original amount — more WSOL and significantly more STER were added than were present before the error
- **Status:** ✅ Fully corrected — pool operational

---

### Event 4 — Additional LP Added
- **Date:** January 2026
- **Action:** Additional liquidity added to strengthen pool depth
- **Amount:** 762,000,000 STER + 3.861 WSOL = approximately $975 USD
- **Status:** ✅ Completed successfully

---

### Event 5 — Additional LP Added
- **Date:** February 2026
- **Action:** Additional liquidity added
- **Amount:** 3,058 LP Tokens = approximately $874 USD
- **Status:** ✅ Completed successfully

---

### Event 6 — STER-USDC Liquidity Added and Held Unlocked
- **Date:** About January 14, 2026
- **Action:** Liquidity added to the STER-USDC pool from the SDV Master wallet. The resulting 576,777.654137 LP tokens were moved to a separate SDV wallet, `DKUqEhg1kEp6DowxPtxRksixp6bQMMwKj5Gnbv4DMyYb`.
- **Note:** These LP tokens were not placed in a lock at that time. They were about 38.9% of the STER-USDC LP tokens. They stayed in that wallet, unmoved, until Event 8.
- **Status:** ⚠️ Held unlocked until October 2, 2026 (see Event 8)

---

### Event 7 — SOL-STER Liquidity Added and Locked to 2028
- **Date:** July 18, 2026
- **Action:** Additional liquidity added to the SOL-STER pool, and the new LP tokens locked on Streamflow until July 18, 2028
- **Deposit transaction:**
`2T8U2kLiYipjR5A8JB1YWhJtRKE8P9QNinxNdanxoNrhvreQ9Hogic9V1u6cNVHaMBxDniZvVLsnms1ZiDhxpa1R`
- **Status:** ✅ Completed successfully

---

### Event 8 — Remaining STER-USDC LP Locked
- **Date:** October 2, 2026
- **Action:** The 576,777.654137 STER-USDC LP tokens from Event 6 were locked on Jupiter Lock until December 20, 2028
- **Terms:** Full amount unlocks on one date. Cannot be canceled. The recipient cannot be changed. Recipient: SDV Treasury wallet.
- **Status:** ✅ Completed successfully

---

## 🔹 Rules for LP Management

- No LP tokens are used for operational expenses
- No LP tokens are used for marketing or incentives
- No LP tokens are used for micro-trades
- Any future LP adjustments will be documented in this file
- All LP actions are verifiable on Solscan

---

## 🔹 Verification

Steps for checking each pool and lock yourself are in [verify.md](verify.md).

---

STER is committed to transparent, stable, and verifiable liquidity management, including honest documentation of errors and how they were corrected.
