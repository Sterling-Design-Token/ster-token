# STER Governance

This page states who operates STER, what can no longer be changed by anyone, and how changes to SDV's own holdings are recorded.

Last updated: October 2, 2026.

---

## 🔹 Who Operates STER

STER is issued and operated by Sterling Design Ventures LLC (SDV), a South Carolina limited liability company. SDV makes all operating decisions. STER has no on-chain governance and no token-holder voting.

---

## 🔹 What No One Can Change

| Item | Status |
|------|--------|
| **Supply** | Fixed. The mint authority was revoked on September 20, 2026, so no new STER can be created. |
| **Holder balances** | The token has no freeze authority, so no holder's STER can be frozen. |
| **Token details** | The metadata is immutable. The name, symbol, and metadata link cannot be changed. |
| **Founders Allocation** | Locked until November 27, 2028. The lock cannot be canceled and its recipient cannot be changed. |
| **Liquidity locks** | None of the four liquidity locks can be canceled. See [lp.md](lp.md). |

---

## 🔹 What SDV Controls

- The five SDV wallets listed in [treasury.md](treasury.md), which together hold 99.59% of the supply. Four of them are unlocked.
- Liquidity positions when their locks expire. SDV intends to relock the two positions that expire on December 20, 2026 for two more years.
- The ten ecosystem properties listed in [ecosystem.md](ecosystem.md).

---

## 🔹 How Changes Are Recorded

- Every transfer from an SDV wallet is public on Solscan.
- Liquidity actions are recorded in [lp.md](lp.md), including errors and their corrections.
- Changes to this repository are recorded in [CHANGELOG.md](CHANGELOG.md).

A written treasury policy covering each wallet's purpose, limits on movements, and regular public reporting is in preparation. It will be published in this repository when it is adopted.

---

## 🔹 Changes From Earlier Versions of This Page

- Earlier versions described four wallets and a separate launch-day LP wallet with fixed rules for each. Those descriptions no longer matched how the wallets are used, and they have been removed until the treasury policy is published.
- Earlier versions said the Master wallet made daily micro-swaps for "routing verification," "volume shaping," and "liquidity smoothing." SDV discontinued that practice around April 2026.
