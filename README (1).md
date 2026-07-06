# RakshaNet — Decentralized Trust Mesh for Banking
**IDBI Innovate 2026 · Wildcard Open Track 05 (Disruptive Technology / Open Innovation / Industry Transformation)**

RakshaNet is a privacy-preserving, decentralized fraud-intelligence mesh combined with a continuous behavioural trust engine. It lets banks share fraud *signals* — never raw customer data — in real time, and replaces one-time login checks with a trust score that runs throughout a session, call, or transaction.

## The problem
Three fraud epidemics are currently failing for the same structural reason — banks can't see across each other, and can't see past the login screen:
1. **Digital-arrest / coercion scams** — a legitimate, authenticated customer is manipulated into transferring money during or after a scam phone call. Fraud detection built around login checks never sees this.
2. **Mule accounts** — flagged at one bank, reopened at another the same day, because banks don't share fraud signals in real time.
3. **Duplicate invoice financing** — the same invoice discounted at two or three lenders (a pattern behind several major Indian NBFC blowups), because no cross-lender check exists outside a single TReDS platform.

RBI's Central Fraud Registry is retrospective and manual. Every bank's fraud ML is siloed to its own customers. Nobody solves this continuously, in real time, across institutions — because that would mean sharing raw customer data, which no bank will ever agree to.

## The solution — five layers
1. **Signal Layer** (per-bank, on-prem) — behavioural biometrics, device fingerprints, call metadata, transaction graphs. Raw data never leaves the bank.
2. **Privacy Layer** — salted hashing / Bloom filters convert signals into irreversible fingerprints.
3. **Decentralized Consortium Ledger** — a permissioned DLT (Hyperledger Fabric-style) where member banks/NBFCs/TReDS platforms publish only fingerprints, matched via private set intersection.
4. **Continuous Trust Engine** — a live trust score (0–100), recalculated throughout a session or call, not just at login.
5. **Adaptive Response Layer** — proportionate friction: silent monitoring → nudge → step-up auth → hold + human callback → block, across app, IVR, branch, and video KYC.

## What this prototype demonstrates
Three flagship, fully interactive scenarios:
- **Live Session Monitor** — watch a trust score drop in real time as a "digital arrest" coercion pattern unfolds (long unknown call → new payee → urgent large transfer), triggering an adaptive intervention before money moves.
- **Cross-Bank Fraud Mesh** — simulate a new account opening at IDBI, querying the consortium ledger, and getting back a hash-matched mule-account flag — without ever seeing the flagging bank's customer data.
- **Trade Finance Shield** — simulate an SME submitting an invoice for discounting, and the mesh catching that it was already discounted at another lender two days ago.

## How to use the demo
Open `index.html` → try each of the three tabs → click the scenario button in each to run the simulation.

## Tech (this prototype)
- Frontend: HTML5, CSS3, vanilla JavaScript — fully client-side, no backend or API keys required
- All scenarios are scripted simulations over synthetic data, built to demonstrate the decision logic and user experience of each layer

## Path to production
| Layer | Demo (this build) | Production (IDBI sandbox → consortium) |
|---|---|---|
| Behavioural biometrics | Scripted signals | On-device SDK + server-side ML |
| Privacy-preserving matching | Simulated hash comparison | Private Set Intersection / ZK-proof matching |
| Decentralized ledger | Simulated JSON store | Hyperledger Fabric permissioned consortium chain |
| Trust scoring | Rule-based simulation | Real-time ML risk model |
| Integration | Static web demo | IDBI sandbox APIs, IVR gateway, video KYC systems |
| Governance | N/A | Multi-bank onboarding, audit trail, RBI-aligned data-sharing framework |

## Rollout plan
- **Phase 1 — Pilot (6–8 weeks):** IDBI-internal, single channel (app only), no consortium needed yet.
- **Phase 2 — Integration (4–6 months):** Multi-channel (app + IVR + video KYC), real-time ML trust engine.
- **Phase 3 — Consortium Scale (ongoing):** Onboard partner banks/NBFCs onto the shared ledger under a formal governance framework — positioning IDBI as an infrastructure anchor, similar to NPCI's role for UPI.

## Team
[Add your name, role, and contact here]

## License
Built for IDBI Innovate 2026 submission purposes.
