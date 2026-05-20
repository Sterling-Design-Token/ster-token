# STER Incident Report — December 9, 2025
## Liquidity Pool Accidental Removal & Restoration

**Report Type:** Operational Incident — Post-Mortem
**Date of Incident:** December 9, 2025
**Date of Correction:** December 10, 2025
**Date of Report:** May 20, 2026
**Status:** RESOLVED ✅

---

## Summary

On December 9, 2025 — approximately 12 days after the STER token launched — the token issuer
accidentally removed nearly all liquidity from the STER-WSOL pool on Raydium as a result of
an operational error. The error was discovered the following morning and corrected immediately.
Liquidity was fully restored with a greater amount than was present before the incident.
No user funds were stolen or misappropriated at any point.

This report is published in the interest of full transparency and to provide verifiable
on-chain documentation of both the incident and its resolution.

---

## Timeline

| Time | Event |
|------|-------|
| November 27, 2025 | STER token launched — initial LP created on Raydium |
| December 9, 2025 | Accidental LP removal executed by issuer |
| December 9-10, 2025 | LP outage — approximately 12-16 hours |
| December 10, 2025 | Error discovered — LP immediately recreated and restored |
| December 10, 2025 | Public transparency announcement published on Facebook and Discord community |
| December 10, 2025 | Facebook post URL: https://www.facebook.com/sterling.design.2023/posts/pfbid026fHqVXAkb5R6h3ACy8BE6d6oPpv3AJahW2e1icUKHprc8rx4DXZytJhPP6vxXerbl |

---

## What Happened

The token issuer, operating as a first-time Solana token creator, was attempting to
execute a routine operation on the Raydium platform. Due to inexperience with the
platform interface, the parameters of the operation were entered in the wrong order,
resulting in the accidental removal of the LP position rather than the intended action.

**This was an operational error, not a deliberate act.**

There was no intent to harm holders, manipulate the market, or conduct a rug pull.
The issuer was not aware the removal had occurred until the following morning.

---

## On-Chain Evidence

### Error Transaction — Liquidity Removal
**Transaction Hash:**
`4cEQrur99eepPgSVySQVoEkCBuv333KrwLxamhEGmFMsPfUFowrk6eKQ8ouaBW9gF23St1eHTAFppnFmd6eVdkdN`

**Verify on Solscan:**
https://solscan.io/tx/4cEQrur99eepPgSVySQVoEkCBuv333KrwLxamhEGmFMsPfUFowrk6eKQ8ouaBW9gF23St1eHTAFppnFmd6eVdkdN

| Field | Value |
|-------|-------|
| Action | REMOVE LIQUIDITY |
| STER Removed | 1,999.246221 STER |
| WSOL Removed | 3.51867335 WSOL |
| Wallet | Master wallet (same wallet used for all LP operations) |
| Intent | Accidental — operational error |

---

### Correction Transaction — Pool Recreated & Liquidity Restored
**Transaction Hash:**
`2kvwjU2qJZy6yGCSbYW9yiHonKe85HgHJ3gpv2iQm86BY2UGe8TXPsLihBfrK7BoCaF8A1iLsgNaBKHEyXN7Kmgs`

**Verify on Solscan:**
https://solscan.io/tx/2kvwjU2qJZy6yGCSbYW9yiHonKe85HgHJ3gpv2iQm86BY2UGe8TXPsLihBfrK7BoCaF8A1iLsgNaBKHEyXN7Kmgs

| Field | Value |
|-------|-------|
| Action | CREATE POOL + ADD LIQUIDITY |
| STER Added | 500,000,000 STER |
| WSOL Added | 3.65 WSOL |
| USD Value | Approximately $1,011.20 |
| Wallet | Same Master wallet — same issuer |
| Intent | Deliberate correction — full restoration |

---

## Impact Assessment

| Category | Impact |
|----------|--------|
| User funds stolen | NONE |
| Holder balances affected | NONE — token balances unchanged |
| Trading availability | Suspended approximately 12-16 hours |
| Price impact | Temporary — pool restored to normal function |
| Liquidity after restoration vs before | GREATER — more liquidity added than was present before error |
| Permanent harm to any holder | NONE |

---

## Key Facts for Security Reviewers

1. **Same wallet executed both transactions** — the removal and the restoration were
   performed by the same Master wallet, confirming this was an error-and-correction
   sequence by the same party, not a coordinated rug pull followed by a cover-up.

2. **Restoration exceeded original liquidity** — a genuine rug pull would not restore
   liquidity. The fact that more liquidity was added than was present before the error
   is the clearest evidence of intent to correct rather than exploit.

3. **No funds left the ecosystem** — the WSOL and STER remained in the issuer's
   control throughout and were immediately redeployed to recreate the pool.

4. **Public transparency announcement made** — the STER Discord community was
   notified of the incident and correction at the time it occurred.

5. **No pattern of repeat behavior** — this was a single isolated incident. The pool
   has remained stable and continuously funded since December 10, 2025.

6. **Additional liquidity added subsequently** — two further LP additions were made
   in January and February 2026, demonstrating continued commitment to pool stability.

---

## Why Automated Systems Flagged This

Blockchain security scanners use pattern-matching algorithms to identify behavior
associated with rug pulls. The December 9th event produced an on-chain pattern —
a large liquidity removal followed by a price crash — that matches rug pull heuristics.

However, the context that automated systems cannot evaluate includes:

- The same wallet immediately restored the liquidity
- The restoration amount exceeded the original
- No funds were transferred to external wallets
- A public transparency announcement was made
- The pool has been stable for over five months since

The flag is an artifact of pattern-matching applied without contextual awareness.
This document provides that context in full.

---

## Corrective Actions Taken

1. ✅ LP fully restored within 24 hours of the error
2. ✅ Additional liquidity added in January 2026
3. ✅ Additional liquidity added in February 2026
4. ✅ Public transparency announcement published on Facebook — December 10, 2025
   https://www.facebook.com/sterling.design.2023/posts/pfbid026fHqVXAkb5R6h3ACy8BE6d6oPpv3AJahW2e1icUKHprc8rx4DXZytJhPP6vxXerbl
5. ✅ Formal dispute filed with Blockaid — Ticket [WXV6K9-4ZPN3]
5. ✅ Honeypot classification successfully removed following dispute
6. ✅ This formal incident report published to GitHub for permanent public record
7. ✅ lp.md updated to include full chronological LP history

---

## Current Security Classification Status

| Platform | Flag | Status |
|----------|------|--------|
| Blockaid — Honeypot | Removed | ✅ Resolved |
| Blockaid — Rug Pull | Active | ⏳ Dispute in progress — Ticket WXV6K9-4ZPN3 |
| Trust Wallet | Partially resolved | ⏳ In progress |
| Solflare | Submitted | ⏳ Awaiting response |
| Phantom | Spam flag | ⏳ Resolves organically with holder growth |

---

## Statement from the Issuer

Sterling Design Ventures LLC acknowledges the December 9, 2025 liquidity removal error
fully and without reservation. It was a mistake made by an inexperienced operator learning
the mechanics of Solana liquidity pools. It was not malicious. It was not a rug pull.
It was corrected as quickly as it was discovered.

We publish this report because we believe transparency — including transparency about
mistakes — is the foundation of community trust. We have nothing to hide and everything
to gain by being honest about what happened.

---

*Published by Sterling Design Ventures LLC*
*May 20, 2026*
*Contact: info@sterlingdesign.us*
