# Changelog

All notable changes to the STER ecosystem repository are documented in this file.
This project follows a simple, date-based changelog format.

---

## [2026-10-02]
### Changed
- Rewrote `README.md` with the exact total supply, the revoked mint authority, both pool addresses, a lock summary, and current contact channels
- Rewrote `lp.md` to cover both liquidity pools and all four liquidity locks, and added Events 6 to 8 to the liquidity history
- Rewrote `treasury.md` to list all five SDV wallets with addresses and balances and to document the Founders Allocation lock
- Rewrote `verify.md` with working links and steps for checking the locks
- Rewrote `ecosystem.md` to list the ten live properties and current STER utility
- Rewrote `governance.md` to state what is fixed on-chain and what SDV controls
- Replaced the January 2026 `roadmap.md`
- Added contact details to `SECURITY.md` and `SUPPORT.md`

### Corrected
- `lp.md` listed `AvDg7yXhcR15ryRycqJipBdqwchKJ7yirx831KBew1Zz` as the lock contract. That address is not the lock contract. The Streamflow contract links are now given.
- `README.md` and `verify.md` labeled `3kbkFHgKcwWrHCFYt1rXeY81YzC23cnHbHxMucBnpvBm` as the LP token mint. It is the SOL-STER pool address.
- `verify.md` linked the Treasury wallet to an address that does not exist.
- `airdrops.md` contained a leftover drafting note, now removed.

### Removed
- Descriptions of daily micro-swaps, "volume shaping," and "liquidity smoothing" from the Master wallet. SDV discontinued that practice around April 2026.
- Per-wallet rules that no longer matched how the wallets are used. A treasury policy will replace them when it is adopted.

---

## [2026-05-20]
### Added
- Added `INCIDENT-REPORT-DEC9-2025.md` documenting the December 9, 2025 accidental liquidity removal and its correction
- Updated `lp.md` with the full liquidity history

---

## [2026-01-13]
### Changed
- Updated `treasury.md`, `ecosystem.md`, `governance.md`, `lp.md`, and `branding`

---

## [2026-01-12]
### Added
- Created `CONTRIBUTING.md` with contribution guidelines
- Added `SECURITY.md` outlining responsible disclosure
- Added `LICENSE` (MIT)
- Added `roadmap.md` with completed, active, and upcoming phases
- Added `ecosystem.md` providing a high-level overview
- Added `verify.md` with step-by-step Solscan verification
- Added `lp.md` documenting liquidity pool transparency
- Added `treasury.md` documenting treasury wallet transparency
- Added `airdrops.md` for Airdrop #1 transparency
- Upgraded `README.md` to a full ecosystem landing page

### Improved
- Strengthened repo structure for clarity and transparency
- Established consistent formatting across all documentation files

---

## [2026-01-11]
### Added
- Initial repository creation
- Placeholder README
