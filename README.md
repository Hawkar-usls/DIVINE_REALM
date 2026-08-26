<div align="center">

# DIVINE_REALM
### Interactive Gaming × Scientific/Public-Good Compute Gateway Prototype

![Status](https://img.shields.io/badge/status-active%20prototype-2ea043)
![Class](https://img.shields.io/badge/class-scientific%20compute%20gateway-8250df)
![License](https://img.shields.io/badge/license-evaluation%20only-d29922)

</div>

## Try the compute-layer demo

**GitHub Pages surface:** [`playgrid.html`](playgrid.html)

It wraps the existing DIVINE_REALM slot prototype with explicit scientific-compute consent, CPU caps, immediate revoke, visible simulated work receipts, and a Golem-compatible scientific Requestor bridge model.

## Status

**Active public prototype / partnership demo.** DIVINE_REALM is a Telegram WebApp-compatible slot-style interaction shell exploring how a conventional game can be paired with an **independent scientific/public-good compute gateway**.

The current public build uses local browser simulation for game state. It **does not yet claim to execute real scientific workloads**, does not provide real-money gambling, and is not a certified production deployment.

```text
MATURITY = WORK_IN_PROGRESS
PROJECT_CLASS = INTERACTIVE_GAMING_SCIENTIFIC_COMPUTE_PROTOTYPE
TELEGRAM_WEBAPP = TRUE
REAL_MONEY_GAMBLING = FALSE
CURRENT_VALUE_STORAGE = LOCAL_SIMULATION_ONLY
SCIENTIFIC_COMPUTE_GATEWAY = PUBLIC_DEMO / PARTNERSHIP_PILOT_STAGE
GOLEM_SCIENCE_BRIDGE_MODEL = ADDED
SCIENTIFIC_RESULT = NOT_CLAIMED
PRODUCTION_READINESS = NOT_ESTABLISHED
```

## Concept

```text
GAME / TELEGRAM WEBAPP
          |
          +----------------------> REGULATED RNG / PAYOUT
          |
          +----------------------> SCIENTIFIC COMPUTE GATEWAY
                                     |
                                     +--> approved research Requestor
                                     +--> Golem / other approved provider
                                     +--> upstream result + receipt
                                     +--> Impact Ledger
```

The compute lane is deliberately separated from gambling mathematics. Compute completion, compute speed, scientific output, or client-device power must never change RNG outcome, payout, odds, RTP, or bonus eligibility.

A production pilot can route authenticated requests through a server-side/approved-companion gateway. A Telegram/browser demo must not pretend to be a native BOINC, Folding@home, Yagna, or Golem worker when it is not one.

## Golem science bridge

```text
CONSENT
  ↓
PLAYGRID GATEWAY
  ↓
APPROVED SCIENTIFIC REQUESTOR
  ↓
YAGNA / GOLEM
  ↓
SCIENTIFIC WORKLOAD
  ↓
VERIFIED UPSTREAM RECEIPT
  ↓
IMPACT LEDGER
```

See [`.janus/PLAYGRID_GOLEM_SCIENCE_MODEL.json`](.janus/PLAYGRID_GOLEM_SCIENCE_MODEL.json).

**Truth boundary:** Golem is distributed compute infrastructure, not itself a vaccine-discovery project. A real scientific workload must be supplied and accepted by a compatible research Requestor/project before any scientific impact claim is made.

## Why it may matter

The proposal is not “gambling proves science” and not “play more to help science.” It is a reusable infrastructure layer that can let an operator, aggregator, sponsor, data center, distributed-compute market, and approved workload owner account for **real, capped, verifiable computation alongside already-authorized gameplay**.

Potential value includes:

- verifiable scientific/public-interest campaigns;
- a reusable platform-level integration rather than one isolated slot;
- a route connecting gaming platforms to distributed/cloud/data-center capacity;
- independently auditable workload receipts;
- product differentiation without altering certified RNG logic.

See [`PARTNERSHIP_BRIEF.md`](PARTNERSHIP_BRIEF.md) for the architecture, scale examples, proof-of-compute receipt, scientific boundary, and pilot gates.

## Responsible-gaming boundary

Scientific contribution must not be used as pressure to gamble longer or lose more. Compute is governed by consent/device policy rather than spin count; responsible-gaming limits override any compute campaign.

## Scientific boundary

A workload is considered scientifically useful only when its owner/research partner accepts it under a real protocol. DIVINE_REALM does not itself certify medical or scientific value.

## Evaluation & IP

- [`LICENSE.md`](LICENSE.md) — public-demo evaluation license; no production/commercial license is granted.
- [`IP_NOTICE.md`](IP_NOTICE.md) — copyright / public-private boundary and production-sensitive material guidance.
- [`PROJECT_STATUS.json`](PROJECT_STATUS.json) — machine-readable maturity and deployment boundary.

Publication on GitHub is not a claim that the underlying method is patented or patent-pending. Commercial or scientific deployment requires separate written agreements and independent legal, regulatory, security, platform-policy, scientific-partner, ethics, and responsible-gaming review.
